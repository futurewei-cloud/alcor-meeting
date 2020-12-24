# Alcor Open Source Community Meeting 12/16/2020

1. Zeta ACA Integration
    * Update Zeta envrionment setup file #170 - update PR per Eric's comment
    * Script for Zeta + ACA Test #173  - testing status sharing
        * Wanchen - Pull upstream PR and start a new branch to get the latest udpate
        * Action Items: 
            * Make changes on test cases, do validation. 
            * Rio: Improve the test by adjusting the total port amount through parameters
    * Add vxlan-generic support #180
        * Address comments: explain static numbers, new concurrent hash table, move zeta specifc code to zeta app file

2. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc

3. Status Update

    * ARP responder for L2/L3 neighbors (Luyao): https://github.com/futurewei-cloud/alcor-control-agent/issues/117 PR raised, some discussions going on in GitHub, no blocking issue
    * DPM v2.0 implementation follow-up (Piaoping): 
        * Move forward to DPM v2.0 APIs: https://github.com/futurewei-cloud/alcor/issues/508 (PR: https://github.com/futurewei-cloud/alcor/pull/512) Merged. 
        *  Legacy fields cleanup: https://github.com/futurewei-cloud/alcor/issues/462 Merged with  PR 512
        *  GW port change: https://github.com/futurewei-cloud/alcor/issues/506 Merged with PR 512
        * Subnet deletion issue: https://github.com/futurewei-cloud/alcor/issues/505  (PR: https://github.com/futurewei-cloud/alcor/pull/515) Issue with field, made initial fix, will look into other potential issue and make the fix. 
        * Port reuse issue: https://github.com/futurewei-cloud/alcor/issues/513 
    * Node Mgr change to support per-node MQ configuration: https://github.com/futurewei-cloud/alcor/issues/490 (Min Chen)
        * Todo - 
            * Add two new fields on web entity (NodeInfo) and UTs change
		    * Node Metadata Manager => DPM (async call) and new API in DPM for node registration
		    * Fallback mechanism: DPM to retrieve missing data from NMM in case of cache miss (PR next week)
    * IP address replacement: https://github.com/futurewei-cloud/alcor/issues/218 (Xiaoyan) - Code implementation done, working on e2e testing offline. Will raise a PR soon.
    * MQ deep dive cont'd (Xuwei): https://github.com/VanderChen/open-doc/blob/master/pulsar%20design1119.docx - design review , big picture on the workflow, more discussion will be needed to breakdown tasks

4.  Scalability test framework & Report review (Jianwei & Wei): (Not discussed) 
	* https://github.com/futurewei-cloud/alcor/issues/439
	* https://github.com/futurewei-cloud/alcor/issues/425 
    * https://github.com/futurewei-cloud/alcor/issues/283

5. Design Discussion
    * SDN GW design: https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/gateway_integration.adoc  https://github.com/futurewei-cloud/alcor/pull/517 (Next meeting)
    * Alcor Support various dp: https://github.com/futurewei-cloud/alcor/issues/478 (Not discussed) 
