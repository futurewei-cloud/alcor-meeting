# Alcor Open Source Community Meeting 01/20/2021

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

## Status Update ##

1. Zeta and Alcor Update
    * Issue 183
        * Multiple ports pinging
        * Segmentation Error
        * Add validation code
    * Zeta Demo, test cases will be finalized
    * Zeta Perf test to showcase latency and scale 
2. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc
3. Status Update 
    * ARP responder for L2/L3 neighbors (Luyao): https://github.com/futurewei-cloud/alcor-control-agent/issues/117 
        * https://github.com/futurewei-cloud/alcor-control-agent/pull/167  addressed blocking isue, will make change and merge soon
    * Node Mgr change to support per-node MQ configuration: https://github.com/futurewei-cloud/alcor/issues/490 (Min Chen)
        * Issues: Exceptional handling, attribute look up  based on Host IP. Will adress these two issues and check in code in a week
    * GW Mgr: https://github.com/futurewei-cloud/alcor/pull/541 (Xiaoyan)
        * Developed a few interfaces for Zeta
        * Found some issues related rollback mechanism to  after unit test code, will dicuss more on this 
    * MQ Deep Dive cont'd (Xuwei): https://github.com/futurewei-cloud/alcor/pull/542
        * Service Design PR #542 
            * Reviewed designs, update document based on discussion (topic diagram update, subscription flowchart, pod creation flowchart, exception handling when grpc-mq fail) Will push changes within this two weeks
4. Discussions
    * Distributed transaction solution analysis and discussion 
    * When two VMs migration requests arrive almost at the same time, procssing time is out of order, initial solution disucssion. 


        