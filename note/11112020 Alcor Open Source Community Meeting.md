# Alcor Open Source Community Meeting 11/11/2020

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

1. Alcor-Zeta Integration
* Topics: 
    * USTC setup 10 nodes OpenStack Cluster with 1 control node
    * USTC concern about long lasting TCP connection between compute node and Gateway for Openflow update
        * Answer: Gateway inject/change Compute node flow through existing networking control path
            * Alcor controller -> ACA on compute node -> OVS, or
            * Neutron controller -> Neutron OVS agent on compute node -> OVS
    * USTC ask development language - Answer: Compute side mostly script, python is fine, may have some C, depends on scoping result
    * Futurewei: Explained inband flow table update mechanism when instance down, reference sent to slack channel
    * Futurewei: Continue working on consolidated system design
* Action Items:
    * USTC - Collect OpenStack version and Compute node distro & Kernel version
    * USTC - Test basic networking with Router (Neutron) and Geneve tunnel encap
    * USTC - Test flow table "learn" action for inline flow table update w.r.t. topic 4 above. 
    * FW - Complete consolidated system design before next meeting for detailing and task breakdown
2. Scalability Test Results Review - First milestone achieved and on track to 1000X scalability goal
    * Verify control plane performance between Infra services and ACA,  in both mega VPC scenario (up to 1 million ports per VPC)  and 1 million compute nodes
    * Run a comprehensive analysis on latency for gRPC fast path and MQ scaling path, and show each's comfort zone, panic zone and the boundary of two control paths under various test scenarios (e.g., VPC size, batched port size, DPM concurrency level, and MQ machine pool)
    * With the guidance of scalability results, Alcor's next step to improve scalability becomes more clear - including infra service partitioning,  multi-control path switching, and concurrency improvement in DPM
 
2.	Design Review
    * Southbound scale-out design
        * Liguang talked about partitioning and deploying infra services based on DC physical topology
        * The community brainstormed about three possible options which are pod-based partition, splitting of DPM into two microservices (message dispatcher and GS distributor), or two layers (message conversion and distribution) and discussed each's pros and cons.
        * iii.	Next step: FW team will discuss more in house and detail the design
    * EIP/SNAT design kickoff
        * Eric showed a high-level design including requirement, customer scenarios, and two design approaches
        * Liguang described the high-level idea of distributed SNAT design
        * One major concern on distributed SNAT is resolved (compute node is already configured with external network connection)
        * Next step: Wei will follow up to collect more feedback and drive the design
    * ACA modular software architecture 
        * Discussed the gap between Openflow/OVS and production env
        * One option is to further modularize ACA to mitigate the risk for production adoption
        * Next step: Eric to follow up on ACA modular architecture as we are collecting more feedback from the community
    * MQ scaling path deep-dive
        * Reviewed four different subscription modes in Pulsar
        * Brainstormed about a design based on key-shared mode and per-host message key - a critical design to reduce the number of MQ topic 
        * Next step: Xuwei to detail the design (particularly on the algorithm of reducing key hash collision) 
 
3.	Implementation Status Update
    * DPM v2.0 is out for review - Piaoping/Kevin
        * Cut message processing latency by 99% compared to v1.0 implementation
        * Done with port create and routing rule update,  pending on port update/delete
        * Action Items
            * Improve UT coverage (next step: Kevin to provide more existing test scenarios and samples and to support transition to v2.0 implementation)
            * Add cache layer in DPM 2.0 (next step: Piaoping add Ignite support to DPM and integrate with subnet-layer programming path)
            * Make PM change (Piaoping/Liguang) to adopt the new DPM contract
            * Liguang to review the PR and provide feedback
    * Security Group host implementation - Piaoping
        * No update due to change of priority
    * DHCP enhancement to include GW IP and DNS - Jianwei
        * Coding almost done, need testing to confirm change
    * ARP responder for L2/L3 neighbors - Luyao
        * On track, target to send out a PR for review this week
    * DPM pulsar client - Min
        * Hit a blocking issue in development/test (while it can't be reproduced in the scalability test)
        * Next step: Min to show more exception trace on Slack and follow up with Piaoping
        * ETA: Fix the issue and update PR by Saturday
 
4.	Misc: 
    * USTC team to provide regular status update on Slack to get timely help from the community
