# Alcor Open Source Community Meeting 8/17/2020, 8/19/2020

Meeting Recording: 
8/17: https://youtu.be/VltgKOQ-Z10
8/19: https://youtu.be/kSeuoPYYWgA

## 8/17/2020 Meeting Note ##
* Southbound Workflow Design Discussion https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/southbound_workflow.adoc

  * Southbound services partitioning
  * Communication model
  * Messaging model based on goal state
  * Southbound programming workflow
  * Concurrency and event ordering

## 8/19/2020 Meeting Note

**Status Update**

* DHCP: Unit test is done. Working to set up the environment for verification.

* Route Manager Design: https://github.com/cj-chung/alcor/blob/cj-alcor/docs/modules/ROOT/pages/mgmt_services/route_manager.adoc

* Southbound Flow Table: Needs to look into the concerns of having too many VPC topics. Possible solution: fragmentation. Will share the desgn soon.

* Mac Manager PR (needs to be reviewed)

* Collaboration with USTC
    * VPC Fragmentation
    * Pulsar client server implementation
    * ACA and DPM 

**Work Items**

* Route Manager 830 (James)
* Port Manager (Piaoping)
* Dataplane Manager (Xiaodong)
* Subnet, VPC Manager (James)
* ACA Integration (Eric)
* Code Complete for Integration 
* E2E Integration Testing (after all items are done for 830)


