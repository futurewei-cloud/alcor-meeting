## Alcor Open Source Community Meeting 7/3/2020 ##
 
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