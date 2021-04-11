# Alcor Open Source Community Meeting 8/4/2020, 8/5/2020 #
 
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
 
* 8/4: https://youtu.be/nQZNMf4Sfpg
* 8/5: https://youtu.be/DZ2b1mFl8rk
 
 
## 8/4/2020 Debug Session ##
 
**Private IP Manager Subsequent Allocate/Release Failure**
 
* Problem: there are two IP manager instances. The first instance caught the first allocation.
  * Successfully Deleted initially
  * Was able to run the second instance allocation successfully in 19 seconds
  * But after 8 seconds, delete was not done successfully, error: claim resource not found.
* Will look into the problem, and see if distributed lock can address the issue. Also going to look into other manager to see if there's similar issue.
 
**Port Manager**
 
* Review the new port manager
* Port manager interaction with EIP is needed for when IP is being listed. (Not needed during creation)
 
**Action Items**
 
* (Piaoping) Neighbor Issue https://github.com/futurewei-cloud/alcor/issues/335
* (Piaoping) Private IP manager subsequent allocate/release failure
* Test the new network configuration
* (Liguang) Review the new port manager
 
## 8/5/2020 Weekly Community Meeting ##
 
**Pulsar and RocketMQ Result**
 
* RocketMQ
   *  The data has improved going from 1 broker to 3 broker for 100-3000 topics
   * Latency is still high
   * 3 brokers are running in 3 machine with their own IO
 
**Alcor Demo (E2E)**
 
* Currently support, subnet, port, network. Will soon to support security E2E, floating IP and router.
 
**DHCP Server Support**
 
* Eric: https://github.com/futurewei-cloud/alcor-control-agent/issues/102  (Close down on 4a, 4b, Wunan will focus on Unit test)
  * Next Step: E2E Environment and Perf-test analysis
 
**Stress Test Data Review**
 
* Deployed 150 VMs at the same time, a set of operation
  * Network
  * Subnet
  * Deploy VM
  * Delete VM
 
* Result
  * Neutron:  20 seconds for the entire set of operation
  * Alcor: 5.6 seconds, cut latency by 25% when comparing to neutron data. flat curve, more room to go, will need to add more machines.
  * Alcor 2400 VM deployments, average 35 seconds
 
**August Planning**
 
* Network Resources, E2E Implementation
   * Router
   * Security Group
   * Floating IP

 
* Southbound Distribution Design and Prototype POC
  * Prioritize project on large scale. Interested in seeing the latency for large scale deployment. (Yuanwei will come up with a detailed target plan and test cases)
 
**Blocking Issue**
 
* Cross-node communication is not fully communicated
* Unit test - verify token test https://github.com/futurewei-cloud/alcor/pull/340
* Security check request delete - check whether it's admin issue