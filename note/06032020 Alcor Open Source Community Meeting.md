## 06/03/2020 Alcor Open Source Community Meeting
 
### Status Update
 
1. Pod Manager - PR Submitted
1. Security Group - Will review PR
    1. Binding
       1. Need to check the default security group
       1. Need to add this interface
       1. Modify the security group of the pod: when modifying, first remove the original one, then bind the new one, and then add an interface.
          1. When creating a pod, when there's no security group, it' okay to use default security group.
          1. When updating the pod, unbind the previously bounded security group, and then bind the new security group.
1. Elastic IP Manager
    1. Discussion (Will discuss more after design doc is finished)
       1. There are relatively few IPV4s. If customers don’t pay for it,  outbound connection also needs to be distributed. IPV4s will not be exclusive, they will be publicly shared by multiple tenant.
          1. How to allocate IPV4 when not requesting?  - Assign IP and pod range to host
          1. Hard to calculate cost if EIP is shared across tenant.
          1. Not sure we need the multi-tenant scenario at the moment
1. Api Gateway - Support Authentication with OpenStack KeyStone (Jianwei)
    1. Problem: After we put token in the cache, we let it age naturally and delete it. Currently, we do not have an interface in the pod to support aged cache token.
    1. Api Gateway and OpenStack KeyStone Integration
       1. Focus on authentication
       1. Add a filtering layer in Api Gateway, the filter will interact with KeyStone. It will first verify Alcor token and then proceed to verify customer's token.
       1. Authorization: What permissions do users have?
1. Microservices Advantage
    1. Scale out
    1. Large scale region
    1. Latency will be optimized in series
    1. Solve the coupling issue of database
1. Testing (Xuwei, Chenming) - Will discuss once the environment is set up
    1. Testing Environment
       1. Focus on Pulsar and RocketMQ testing
       1. Run 3 VM, 3 instances for each test
    1. Measuring Metrics
       1. Latency
       1. Throughput (Producer, consumer, message/s/producer, topics, size of payload
       1. Consider use cases?
       1. consider the time of placing orders?