# Alcor Open Source Community Meeting 02/24/2021

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

1. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc

2. Status Update
    * Gateway manager Design Discussion
        * Yuanwei to look into the design, see how we are going to integrate gateway manager with NGP and transit gateway features
    * MQ Design https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.pdf
        * Will finalize design and start implementation
    * Ping test between ACA container fail with core dump 216 (Debug) https://github.com/futurewei-cloud/alcor-control-agent/issues/216
        * ping failed after ARP responder return success
        * core dump at the end of parent test (not 100% repro)
        * Luyao to repro the issue
    * DPM optimizes response entity and aggregates response on resource level #480  - Work in Progress (Xiaoyan) 
    * NCM Design https://github.com/er1cthe0ne/alcor/blob/design/AGA/docs/modules/ROOT/pages/infra_services/NCM_design.adoc
    * Security Group Implementation - discussed what was missing from previous implementation