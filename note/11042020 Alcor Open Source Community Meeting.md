# Alcor Open Source Community Meeting 11/04/2020

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
    * Topics
        * USTC Issues discussion and Q&A
        * ACA North Bound contract discussion
            * At subnet level may have more overhead, adding VPC level when possible
            * Consider if zgc_id (uuid) in contract helps as ZGC signature to detect change
    * Action Items:
        * Minli - Submit OAM processing draft PR for early comment. Send out info regarding to bucket flow hash
        * Huaqing - Issue #161: Take on task for ACA packaging and remote deployment to avoid build on target host
        * Qianyu - Issue # 161 Add Unicast table in ACA OVS
2. Open-Source L3 E2E demo
    * showed that cross subnet ports can ping each other through the horizon UI
3. Feature request for DHCP enhancement: https://github.com/futurewei-cloud/alcor-control-agent/issues/159
    * discussed the requirement and changes needed in alcor control agent
4. ARP responder for L2/L3 neighbors: https://github.com/futurewei-cloud/alcor-control-agent/issues/117
    * addressed the task owner's question regarding to whether we need internal vlan ID and if ACA have access to it
5. Scalability test framework update (cont'd): https://github.com/futurewei-cloud/alcor/issues/439 https://github.com/futurewei-cloud/alcor/issues/425 https://github.com/futurewei-cloud/alcor/issues/283
    * discussed the current thinking and next steps
6. Southbound scale-out: MQ implementation update (cont'd): https://github.com/futurewei-cloud/alcor/issues/404  https://github.com/futurewei-cloud/alcor/issues/405
    * followed up on the current status and timeline for completion
7. Security Group host design discussion and update (cont'd):  https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
    * Need to confirm whether 1130 target can be made