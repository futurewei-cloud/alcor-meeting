# Alcor Open Source Community Meeting 8/17/2020, 8/19/2020

    MIT License
    Copyright(c) 2020 Futurewei Cloud

    Permission is hereby granted,
    free of charge, to any person obtaining a copy of this software and associated documentation files(the "Software"), to deal in the Software without restriction,
    including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and / or sell copies of the Software, and to permit persons
    to whom the Software is furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
    WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

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


