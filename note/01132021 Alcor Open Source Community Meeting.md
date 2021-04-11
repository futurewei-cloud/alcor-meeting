# Alcor Open Source Community Meeting 01/13/2021

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
    * Data path integration #189 Discussion, PR #191
        * Address comments in #191
2. SDN GW Design Discussion https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/gateway_integration.adoc
https://github.com/futurewei-cloud/alcor/pull/517
3. ARP responder for L2/L3 neighbors (Luyao): https://github.com/futurewei-cloud/alcor-control-agent/issues/117
    * Address minor comment in PR #167
4. Node Manager change to support per-node MQ configuration  https://github.com/futurewei-cloud/alcor/issues/490 
    * Min to sync with Piaoping if there are any questions
5. MQ Design and algorithm discussion
    * https://github.com/issacyxw/mqdesign/blob/main/MQ.docx
    * Finalize design, review design and start implementation asap
6. Southbound Routing Discussions
    *  Distribute revision number start from the top level microservices to ACA, work needs to be added
    * Pros and Cons between full amount update vs incremental update