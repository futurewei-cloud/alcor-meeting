# Alcor Open Source Community Meeting 8/26/2020 

Meeting Recording: https://youtu.be/Hq677md2Osc

## Status Update

**Scale Test Plan**
* Support large-scale scenario verification
* Feedback: 
    *  The service of dpm and fast path and normal fast path is a logical concept? 
        * The thought is to build it as entity. The main reason is that so we don’t need to split each partition. If a message needs to be synchronized with many partitions, each upper-level microservice must send multiple copies to different DPM partitions. The number of partitions is larger.
    *  For fast path, it’s better for the node manager to interact directly with the DPM fast path service of the second-layer infrastructure. The division is clearer. The problem is that fast path has two more hops. How much impact does it have on performance?
        * Fast path can integrate with DPM. 
        * Normal path should be separated out. 
    * Test Use Cases Schedule
        * Will focus on the GRPC perf-test first while the development work is ongoing for MQ. 
  

**DHCP**
* Remaining Tasks for 830: https://github.com/futurewei-cloud/alcor-control-agent/issues/102
    * Unit test and functional test : Testing for verification (manual test should be fine too) 
    * Test cases: Verify when a new VM is created, whether filing DHCP request can be intercepted and returned automatically
    * E2E Test 
    * Compatibility for both CentOS and Ubuntu (After 830)
* Question 
    * The compilation is passed, the environment is set up, the mapping table of DHCP and mac, how to put the mapping table in?
    * Program DHCP sever using goal state message.

**Route Manager** 
* Route Manager Design: https://github.com/cj-chung/alcor/blob/cj-alcor/docs/modules/ROOT/pages/mgmt_services/route_manager.adoc (James) 
    * Key workflow:https://github.com/cj-chung/alcor/blob/cj-alcor/docs/modules/ROOT/pages/mgmt_services/route_manager.adoc#key-workflow

**Port Manager** 

* Why do we need to distinguish between L3 and L2 neighbors?
https://github.com/futurewei-cloud/alcor/issues/363
* Contract for PM and DPM: https://github.com/futurewei-cloud/alcor/pull/366
* Sample for DPM (Piaoping) 

**Dataplane Manager**

* PM and DPM contract, workflow (Xiaodong)

**USTC Collaboration** 
* Dataplane 
* ACA 
* VPC Approximation (After 915)


