# Alcor Open Source Community Meeting 01/06/2021

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

1. Zeta and Alcor Integration
    * Zeta Inegration Implementation #149
        * Implementation merged at #180
    * Add test validation code in aca_test_zeta programming.cpp #183
        * Add test validation code #187
    * Action Items:
        * E2E workflow for dataplane, ad finish dataplane and control plane profiling in the next two weeks.
1. Status Update
    * Node Mgr change to support per-node MQ configuration: https://github.com/futurewei-cloud/alcor/issues/490 (Min Chen)
        * Add unit test for node manager and test in local. 
    * ARP Responder for L2/L3 Neighbors (Luyao) https://github.com/futurewei-cloud/alcor-control-agent/issues/117
        * 70-80% done, will make changes according to Eric's comment and test again
    * MQ Deep Dive https://github.com/issacyxw/mqdesign/blob/main/pulsar%20design1221.docx
        * Start working on the algorithm, will move to implementation after alogorithm is being reviewed.
    * SDN GW design: https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/gateway_integration.adoc https://github.com/futurewei-cloud/alcor/pull/517 (edited) 
        * James to follow up with Xiaoyan on Slack, and provide the needed API information 