## 05/20/2020 Alcor Open Source Community Meeting 

Meeting Recording:https://youtu.be/Or9PWONCook

### Community Update 

1. 5/20 Community update
    1. Ignite usage
    2. Code refactor
    3. Fundamental and house cleanup
    4. Documentation
2. Active Community involvement
    1. 9 active under review
    2. A lot of discussion and debate to ensure solid design and code quality
3. Alcor 6/30 Planning
    1. New Microservices
    2. APIs – L3 Networking and security
    3. Agent Development
        1. Designs out, implementation delayed for host agent 

### Southbound messages distribution design 

https://github.com/futurewei-cloud/alcor-meeting/blob/master/new_proposal/05132020_new_proposal.pptx

1. Research
    1. Kafka
        1. A 100 * 100-scale Kafka cluster requires 100 Kafka clusters under new requirements (100w computing nodes). The overhead is obviously unacceptable. There is too much message redundancy on the southbound computing nodes, and the overhead is large under the Alcor architecture. (100*100规模的Kafka集群，在新的需求（100w计算节点）下需要100个Kafka集群，开销显然无法接受，南向计算节点上消息冗余过多，Alcor架构下开销大。)
            1. Decoupling management pod and infra pod (解耦management pod与infra pod)
            2. Divide Infra pods with AZ granularity (以AZ为粒度划分Infra pod)
            3. Kafka deployment and definition of topic and partition (Kafka部署及topic、partition定义)
        2. Detailed Description 拓展性说明 
            1. The Infra Pod layer can be expanded horizontally, the split tasks can be handed over to idle instances, and the overall load can be increased to increase the instance (Infra Pod层可水平拓展，拆分的任务可交给空闲实例，整体负载较大可增加实例)
            2. Kafka layer instance natural expansion (Kafka层实例自然拓展)
        3. Partition logic: 100W node = 10 Kafka * 200Topic * 50Partition * 10 node aggregation
            1. 200 topics have not been tested, is only based on research. 
            2. For most requests, Topics is based on nodes. 

        4. Deployment 
            1. Kafka deployment: Assuming there are 3 AZs, we set up 3 or 4 Kafka clusters for each AZ (a total of 10 Kafka clusters), each Kafka cluster is responsible for about 10W computing nodes to the south.
                1. Messages for hosts: Topics within Kafka are divided into 200 topics for each Kafka cluster. Each topic corresponds to the NCA of 500 designated computing nodes in the south, and each NCA occupies a consumer group independently. Partition division, each topic is divided into 50 partitions, the producer puts the message of every 10 designated computing nodes into a partition, and the partition is specified when the producer sends the message. Each NCA passes the consumer.assign (Arrays .asList (p)); Manually specify the partition field to find the specific partition under the topic that contains this NCA message. The partition selection of producer and consumer can be specified by the same hash function, so that the code is unified
                2. Public resources (such as ELB): set up additional Topics to specify this type of public resources. All resources of this type are placed in the same consumer group to the south. The group subscribes to the Topic of the resource. The number of partitions in the Topic is set to the number of resources.
                3. Multicast information of security group type: Create topics with VPC as the granularity, all such messages are put into the topic corresponding to VPC, and all NCA subscribes to the topic of VPC of the vm it contains
            
            2. We use redis to maintain the Kafka cluster corresponding to each host and VPC. Producers and consumers use the same hash function to calculate specific topics and partitions, thus unifying the consumer-side code and settings




    2. RocketMQ
        1. Compared with Kafka, the performance of RocketMQ has less effect with the increase of the number of topics, and it is more suitable for this project. RocketMQ can divide tags under the topic, corresponding to the partition usage in the previous Kafka scheme
        2. Tag can be divided under the topic in RocketMQ, corresponding to the partition usage in the previous Kafka scheme
        3. Distinguish the message type: for the host, security group type multicast message, public resource message
            1. Messages for hosts: Topics within RocketMQ are divided into 200 topics for each RocketMQ cluster. Each topic corresponds to the NCA of 500 designated computing nodes in the south. Each NCA occupies a consumer group independently. Tag division. Each topic is divided into 50 tags. The producer puts the message of every 10 designated computing nodes into a tag.
            2. Public resources (such as ELB): RocketMQ specifically sets up additional topics for some public resources (such as ELB). Each topic specifies a specific public resource through a specific tag, and all such resources are placed in the same consumer group to the south. The Tag of this resource is a request to consume public resources in an even-sharing manner.
            3. Multicast information of security group type: create multiple Topic-specific multicast service information such as security group messages and other VPC granularity. Each topic tag subdivides specific VPC, and the sender sends the security group message to the tag corresponding to a certain VPC , Southbound NCA subscribes to the VPC to which all VMs under this host belong, and pulls the security group information.
        4. feedback
            1. Take in consideration of load balancing, may not be able to connect RocketMQ directly, 
            4. In what scenario will a topic have multiple tags?
                1. Taobao, Taobao Fresh, if there is a tag, Taobao Fresh will be sent with priority (with tag)
                3. Queue corresponds to the partition of Kafka.
                4. Need to have very clear business logic while using RocketMQ. Easy to lose message if they have the same topic, same tag and belong to the same customer group.
                5. We first send messages according to queue, we use tag to do filtering, can be used together or individually

    3. Pulsar
        1. Introduction
            1. The parallelism of messages within Topic also use partitions in different broker design patterns
            2. Message persistence is provided by Apache BookKeeper, the message will not be deleted unless a finish return signal is received.
            4. Topic has four subscription models, we use the key-shared model
        2. Performance
            1. One cluster can satisfy one million topics, and one VPC can correspond to one topic
            2. Message size： The maximum allowable size of a single frame 5 MB.
        3. The impact of the number of topics in each namespace on performance has not been verified or relevant information has been found
        4. Multicast message design
            1. Infrastructure Node needs to complete the message copy, and put the copied message into the Topic
            2. For now, it is impossible to copy messages within Pulsar, so that messages under a topic are repeatedly sent to all subscribed consumers.
        5. Distribution design
            1. Consumer logic: Each NCA acts as a consumer, and each consumer subscribes to the topics corresponding to all the VPCs present in the host machine.
                1. For example, if the VPC1 and VPC2 VMs exist in the host machine of NCA1, then they subscribe to the topics corresponding to VPC1 and VPC2
        6.  Detailed Description
            1. For newly added VPC, that is, add a topic and add a subscription rule to the corresponding consumer
            2. For VPC expansion, for example, adding a VM to a new host machine, that is, adding a topic subscription to the consumer corresponding to the new host machine
            3. For large VPC delivery bottlenecks, you can increase the number of partitions corresponding to the topic
            4. For new host machine, add a consumer
        7.  Feedback
            1. If the cluster has 10,000 nodes, it needs to be copied 10,000 times, which is too much.
            2. Is the setting multiple partitions or one partition?
                1. When a partition and a VPC are large, a physical node is used to establish a link. This may be problematic. The larger scene needs to be considered.
            3. If you can support millions of topics, why choose VPC as the topic rather than the host?
                1. Consider the Northbound request.
                2. If a node, a topic, need to send many times
            4. Not particularly suitable for the existing architecture. Advantages? 
                1. There are four subscription modes. The previous subscription mode is reproducible and can be distributed without keys. For consumers, whether the subscription model can be mixed, need to look into it.
                2. In Key-shared mode, this cannot be consumed repeatedly, in other modes, it can be consumed repeatedly.  
                    1.Can multiple modes be used to subscribe to the same topic? (Need to test to confirm.)
            5. Millions, one host corresponds to one topic, and messages are sent to topics 百万级，一个主机对应一个topic，有消息发给topics， 
                1. generally, the number of hosts will be smaller than VPC, and VPC will keep changing
            6. We may need both VPC and host granularity. 
            7. The configuration situation is based on VPC granularity, mainly broadcast, and unicast is also required.
                1. Broadcasting is from north to south, and unicast may be used from south to north.
                2. Is it safe to broadcast with RocketMQ? Can unicast go from VPC?

### Discussion


1. When can we have something out? 
    1. E2E
    2. Security Group
    3. Performance test 
2. How do we test the solution?
    1. for large scale 
    2. simulation test to compare with OpenStack 
    3. Yuanwei - will have a simple dataset 
3. Feature requests and communication
    1. Will create requests on GitHub 
4. OpenStack with OpenStack Nova
    1. Can support multiple network types, vxlan is the default option. 
    2. Integration with OpenStack Nova 
        1. Focus on core functions and main APIs
            1. APIs (about 10）
        2. use cases and parameters
        3. E2E scenerios for VM creation
        4. Identify the interface, what is there and what is not, during the integration process, the customer passes the token, we transfer it to the project id
5. Action Items
    1. Benchmark/performance result for each of the options discussed above
    2. Continue discussion on open community platforms.
    


                
                    
                





        
