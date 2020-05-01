## 04/29/2020 Alcor Open Source Community Meeting

Meeting Recording: https://youtu.be/jSjbGXZbHuo

1. Status Update
   1. Kaidong : Added unit test, issue with ignite server restart, client will not reconnect
   2. Piaoping: current limitation - an example would be, there are 100 nodes in a topic and there are 100 topics in a share. The worst situation is having to send the message for each of the connection. (100 topics * 100 nodes)
   
2. Southbound messages distribution design base on Kafka
   1. Logic - message spilit by VPC
      1. Prerequisites: Each management pod can specify the mapping relationship between VM and NCA in the VPC in the message 各managementpod能指定消息中的VPC中VM与NCA的映射关系
      2. For messages from the management pod, split the message at the VPC granularity and send it to each infra pod 对于来自management pod的消息，以VPC为粒度拆分消息，发送到各infra pod。
      3. The Infra pod is split according to the granularity of the VM, and then split into the corresponding kafka according to the host machine where the VM is locatedInfra pod 按照VM的粒度拆分，然后按照VM所在的host machine 拆分放入相应kafka
   
   2. 100*100 scale Kafka Cluster : Under the new demand (1 million computing nodes), 100 kafka clusters are needed, and the overhead is obviously unacceptable. There is too much redundancy on the southward computing nodes, and the overhead is large under the alcor architecture. 100*100 规模的kafka集群，在新的需求 (100万计算节点）下需要100各kafka集群， 开销显然无法接受，南向计算节点上冗余过多，alcor架构下
      1. Decoupling management pod and infra pod 解耦management pod 与infra pod
      2. Divide into clusters with cluster (fault tolerance across AZ) as granularity以cluster  (跨AZ容错） 为粒度划分为infra pod
      3. Kafka deployment, define topic and partition kafka部署以及topic, partition 定义


   3. Expandability拓展性说明
      1. The Infra pod layer can be expanded horizontally, the split tasks can be handed over to idle instances, and the overall load can be increased to increase instances. Infra pod层可水平拓展， 拆分的任务可交给空闲实例，整体负载较大可增加实例
      2. Kafka layer instances expand naturally Kafka 层实例自然拓展


   4. Parttion Logic 划分逻辑
      1. 1M nodes = 10Kafka * 200 Topics * 50 Partition * 10 Node aggregation 100万节点 = 10kafka *200 TOPic*50Partition*10节点聚合


   5. Parameters 四个参数
      1. Kafka deployment-If there are 3 AZs, we set up 3-4 Kafka clusters for each AZ (a total of 10 Kafka clusters), each Kafka cluster is responsible for about 100,000 computing nodes to the south Kafka 部署 - 假如有3个AZ， 我们为每个AZ建立3-4个kafka集群（总共10个kafka集群）， 每个kafka集群负责南向大约10万个计算节点
      2. Topic division within kafka-create 200 topics for each Kafka cluster, each topic corresponds to the NCA of 500 designated computing nodes in the south, each NCA occupies a consumer group independently kafka内topic划分 - 为每个Kafka集群建立200个topic, 每个topic对应南向的500个指定的计算节点的NCA， 每个NCA独立占据一个消费者组
      3. Partition division-each topic is divided into 50 partitions, the producer puts the message of every 10 designated computer points into a partition, when the producer sends a message, the partition is specified, and the constructor of the producerRecord can have four parameters. These are topic, int type partiiton values, key, value, we can directly specify the incoming second parameter to specify the partition of a NCA message map Partition的划分 - 每个topic下划分50个partition，生产者将每10个指定额计算机点的消息放入一个partition内， 在生产者发送消息时指定partition, producerRecord的构造方法可以有四个参数，分别是topic, int类型的partiiton值， key, value, 我们直接指定传入的第二个参数即可指定某NCA的消息映射的分区
      4. Kafka for some public resources such as ELB-specifically set up additional topics to specify this type of public resources, all resources of this type are placed in the same consumer group south, the topic that subscribes to this resource, the number of partitions in the topic is set to this resource numberKafka为一些公共资源 例如ELB - 专门设立额外的topic指定该累公共资源， 南向所有该类资源放入同一个consumer group, 该订阅该资源的topic, topic内partition数设为该资源数。


3. Action Items
   1. Performance data from current production (how large is the volume of message southbound distribution,  hundreds? Or millions? )
   2. Evaluate different solutions other than Kafka, and pick the one that's most suitable in our case. (Some message are event guarantee, but Kafka does not provide that. )
   3. Collaboration Scope for this project, some potential topics:
      1. Expanding Alcor
      2. Messages
      3. Database
      4. Agent
      5. Control plane
 