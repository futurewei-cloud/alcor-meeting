# Alcor Open Source Community Meeting 9/23/2020

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

Meeting Recording: https://youtu.be/l8nhz85_M70

## Status Update ## 

1. Scalability test framework update 
    * Yuanwei: Will test on gRPC first, aim to have an initial result by the end of Sept. 
    * Test Key Aspects: https://github.com/futurewei-cloud/alcor/pull/384 (Test report, not finalized) 
        * How many long running gRPC connections can 1 DPM handles?
        * Send goal state using multiple connections, test how long it takes to send 10,000 hosts concurrently.
        * How does the size of goal state affect concurrent traffic?
    * Question: Are we only testing using 1 DPM?
        * Yes, currently, we are just testing 1 DPM. If 1 DPM limit is high enough, we will do fragmentation on this. 
2. Southbound scale-out: MQ implementaiton update
    * Chenmin: finished coding, currently working on unit tests. Will send a PR shortly. 
    * Luyao: https://github.com/futurewei-cloud/alcor-control-agent/pull/133 Review in progress, CI problem is fixed.
    * Piaoping: https://github.com/futurewei-cloud/alcor/pull/366  Review in progress

3. Security Group host design discussion: 
    * https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
    * Requirements: scalability, update needs to be fast, stateful security group (meaning allowed ingress traffic are allowed to flow out and vice versa)
    * Design Approach: The Security Group design uses OVS and OpenFlow, building on the latest Neutron OVS firewall rule approach.
    * Next Steps: Piaoping to look into the design and sync up with Eric.
4. On demand OVS rules:
    * https://github.com/futurewei-cloud/alcor-control-agent/issues/134
    * Will need this on demand ovs feature if we are using the security group approach.
    * Next steps: Jianwei to look into PR 134. 
5. Goal State Slicing and On Demand Goal State Programming
    *  Context: 
        * Alcor uses MQ as a scaling path for large-scale VPC deployment which could include a large number of ports, neighbor ports, SGs and NACLs.
        * For a subnet of compute nodes or storage nodes, the OVS Row table is huge as the scale of a few GBs. This causes intensive delay for control plane, at the time of host OS reboot, ACA cold start or restart, as host agent would normally need trigger massive redownload of all information in the host. 
    * Goal:
        * GS slicing: MQ scaling path supports GS slices that contains a portion of full GS in the VPC, so that we can speed up port provisioning in the large VPC scenario.
        * On-demand GS programming:
            * MQ scaling path supports on-demand granular GS programming. ACA doesn't need to pull full GS from MQ, and instead, only subscribe to get a particular slice of interest
            * When as ACA instance cold starts or restarts, it can request a specific topic (host_id or host_group id)+ version which could pull the delta instead of a full GS.
        * Next Steps: Look into the pain points in this area.