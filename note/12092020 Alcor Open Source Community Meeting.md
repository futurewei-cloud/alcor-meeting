# Alcor Open Source Community Meeting 12/09/2020

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

1. Alcor and Zeta Integration
    * Implement multiple nodes with KVM
    * USTC - Current setting up lab environment 
    * The function of the data plane will be introduced next week for testing. 
    * ACA workflow is there, will need to have all test cases done.  

2. Announcement of v0.10 release: https://github.com/futurewei-cloud/alcor/releases/tag/v0.10-alpha

3. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc

4. Status Update
    * ARP responder for L2/L3 neighbors (Luyao): https://github.com/futurewei-cloud/alcor-control-agent/issues/117 
        * Spent some times on testing
        * Next step:  add functions to add/remove entry in 4, also add functions to receive and send arp packet, similar to ACA_Dhcp_Server::ACA_Dhcp_Server
    * DPM v2.0 implementation follow-up (Piaoping): 
        * Move forward to DPM v2.0 APIs: https://github.com/futurewei-cloud/alcor/issues/508 : NetworkConfiguration: adoptoing a few fields and URL
        * Legacy fields cleanup: https://github.com/futurewei-cloud/alcor/issues/462 ： updated per Eric's request
        *  GW port change: https://github.com/futurewei-cloud/alcor/issues/506 : Updated changes 
            * Will have a workflow out
        *  Subnet deletion issue: https://github.com/futurewei-cloud/alcor/issues/505
            * Will look into the issue, currently if there's a VM, cannot delete VPC/subnet
        * Port reuse issue: https://github.com/futurewei-cloud/alcor/issues/513 : Look into the issue
    * Node Mgr change to support per-node MQ configuration: https://github.com/futurewei-cloud/alcor/issues/490 (Min Chen)
        * Changes needed: 
            * Add two new fields on web entity (NodeInfo) and UTs change
		    * Node Metadata Manager => DPM (async call) and new API in DPM for node registration
		    * Fallback mechanism: DPM to retrieve missing data from NMM in case of cache miss
    * IP address replacement: https://github.com/futurewei-cloud/alcor/issues/218 (Xiaoyan)  - should be ready for testing by next Friday
    * MQ deep dive cont'd (Xuwei): https://github.com/VanderChen/open-doc/blob/master/pulsar%20design1119.docx
        * Included keyshared mode, can now support our need. 
5. Scalability Test Framework & Report Review (Jianwei & Wei)
    * https://github.com/futurewei-cloud/alcor/issues/439
	* https://github.com/futurewei-cloud/alcor/issues/425 
    * https://github.com/futurewei-cloud/alcor/issues/283
    * Got 10 more machines, will try to finish implementation in two weeks 

6. Design Discussion:
    * SDN GW Design: https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/gateway_integration.adoc
    * Alcor Support various dp: https://github.com/futurewei-cloud/alcor/issues/478
        