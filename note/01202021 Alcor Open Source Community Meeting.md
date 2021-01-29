# Alcor Open Source Community Meeting 01/20/2021

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


        