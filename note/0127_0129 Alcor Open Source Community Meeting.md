# Alcor Open Source Community Meeting 01/27/2021

1. Zeta and Alcor Update
    * Update to use the latest Alcor gateway schema #207
    * From Zeta side: depdendencies are all cleared, can start testing, also working on code clean up and doc preparation. 
    * Alcor: Eric to drive the documentation from Alcor side
    * Zeta test demo 

2. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc

3. Status Update
    * ARP responder for L2/L3 neighbors (Luyao): https://github.com/futurewei-cloud/alcor-control-agent/issues/117 (merged) Done, no remaining work.
    * Node Mgr change to support per-node MQ configuration (Min Chen): https://github.com/futurewei-cloud/alcor/issues/490 
        * Review and dicuss the issue of node manager (node manager can't start after new changes)
        * Will run the test locally before pushing code 
    * GW Mgr (Xiaoyan): https://github.com/futurewei-cloud/alcor/pull/541 (merged) 
        * Remaining item: Gateway manager rollback mechanism 
        * Will start integration test shortly

    * MQ deep dive cont'd (Xuwei): https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc
        * Added new diagrams, discussion on new changes
        * Will start building out local envrionment for development, and start testing at the same time
4. Design Review
    * AGA design review: https://github.com/futurewei-cloud/alcor/pull/546

# Alcor Open Source Community Meeting 01/2/2021

1. Network Gateway Platform overview 
2. Discussion on how Alcor and Zeta can partner with Network Gateway Platform 