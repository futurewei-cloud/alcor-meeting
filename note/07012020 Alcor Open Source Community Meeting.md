## 07/1/2020 Alcor Open Source Community Meeting
 
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

Meeting Recording: https://youtu.be/s8erd-OTF4c 

### Status Update
 
**Overall Status Update**

- Network E2E integration (control plane, pod manager, DPM, host agent) is done. We were able to deploy 20 pod with one call.
- Kubernetes deployment using controller,  the initial process is done.  Control plane service can be deployed at 2-3 work nodes.
- Will work on performance test, to see how we scale out, to support higher throughput rate and reduce latency at the same time.
- Piaoping : Did we include ignite in the cluster?
    * Current test did not include ignite in every microservice, this will be added later. Each micro service will have its own database (both logically and physically). (Not limit to ignite)
 
 
**DHCP Host**

* Eric: working on POC, will make ACA into open flow controller, got all the dependencies. One PR wil be ready this week to unblock the dependency for Wunan.
  * Packet - done
  * Open the packet (open flow message format)
  * Send back (almost done)
* Wunan: Will address all comments in the PR. Will look into concurrency to address the processing state in parallel issue.
 
**Nova Integration**

* For integration, we are able to register Alcor in OpenStack.
* One blocking issue is not able to create Pod. (Will address in issue 260) Because problem with root, cannot create pod successfully.  Missing an API in master (Issue 253). 
* Security group is also added.
* After pod issue is addressed, the remaining items are routing and floating IP. Will work on a finalized design plan.
* Question:
  * Is the defined root manager similar to Neutron?
    * Not the same. But subject to changes.
    * Corresponding root list to neutron (Issue 252)
  * For one server, if there are many nodes, will this impact the performance of the server?
    * It's possible, but we are not sure how big the impact would be.
    * Client mode is connected to all real time information.
* If there are too many nodes on the client side which caused the reduced performance, this will conflict with our intend to use microservices. Need to do more research on this.
  * When there's changes on schema, we do not need to restart database.
  * Current support all query with parameters
  * Look into client factory and ignite factory
  * Use client mode by default for now.
 
**Elastic IP Manager**

* Basic functionalities are there, need to work on association with pods, EIP and pod binding.
* Batch creation/ batch deletion
* How to deliver EIP?
* When making major chances, the key point is to ensure the services will still be up and running.
 
**Network Echo**
 
* Need to wait for the query PR to merge. Have an interface ready for easy integration.
* Looked into other listed plans, such as LB.
 
**Performance Test Result for Pulsar and RocektMQ**

* Problem
  * Too many connections
  * Pulsar , limited number of single-machine connections

* Next Step
  * Test how many topics can be ran in one connection. Adopt a round robin approach, 100 topics are sent in turn.
  * Test how many topics can be supported in one cluster 
  * Test how many consumers are in cluster
  * Also look into the index of CPU usage, the sending rate of CPU utilization, the memory of
  * Need to make decision on model selection. (DPM to agent workflow), will have initial design.
 
* Other Items
  * Internal DNS microservices
  * DNS manager
  * RBAC manager
 