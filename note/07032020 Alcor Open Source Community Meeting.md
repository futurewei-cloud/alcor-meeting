## Alcor Open Source Community Meeting 7/3/2020 ##
 
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

 Meeting Recording: https://youtu.be/kAhdNIQ_CnU

### Status Update
 
**DHCP**
 
* Make sure to rebase the branch to get the latest code and address PR comments.
 
**Demo** (James)

* ACA talking to OVS
* Will share code structure soon
* Question:
  * Does every node has a controller?
    * An Openflow controller is run on each compute node. When the Alcor controller needs some information, it will send a goal state downstream to the agent, agent will decide what to do with the information it has.
  * How does routing work in this case? Do we still consider ACL and firewall rule?
     * There's a router design in PR. When we get the first packet, the packet will be sent to Openflow controller according to the Openflow rule.
     * More details regarding ACL and firewall will be shared. 
 
**Nova Integration**

* Can now start pod successfully. Since there is no host ID associated at the moment, DPM will not be called
* Need to make changes to security group, the format is not the same as openflow.
* Integration will include subnet, port, security group and VPC.
 
**Performance Tuning**
 
* Mac manager optimization (Piaoping, Jianwei)  Currently only tested in local environment. Waiting for K8S environment.
* K8S environment - in progress
* Test create, update, delete for VPC, subnet, security group and port on latency and throughput.
* We do not have southbound implementation and monitoring yet. For 715, will focus on running a simple script to manually test performance.
* Align with neutron test cases to test out Alcor's performance.
 
**Action Item**
 
* Alcor Cross-point deployment on K8S
* Mac Manager bottleneck
* Perf-test items (VPC, Subnet, port, security group)