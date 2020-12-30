# Alcor Open Source Community Meeting 12/23/2020

1. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc
2. Status Update
    * ARP responder for L2/L3 neighbors (Luyao): https://github.com/futurewei-cloud/alcor-control-agent/issues/117  Vlag tag message not received, need to look into it. 
    * PM & DPM v2.0 implementation follow-up (Piaoping)
        *  PR https://github.com/futurewei-cloud/alcor/pull/515   (DONE)
            *  Subnet deletion issue: https://github.com/futurewei-cloud/alcor/issues/505 
            * Legacy fields cleanup: https://github.com/futurewei-cloud/alcor/issues/462
            * GW port change: https://github.com/futurewei-cloud/alcor/issues/506
            * Port reuse issue: https://github.com/futurewei-cloud/alcor/issues/513
        *  One port supports multiple neighbors & Fix port update failure: https://github.com/futurewei-cloud/alcor/pull/521 (DONE) Will impact Xiaoyan's work, need to look into it. 
        * PM Cache Issue: https://github.com/futurewei-cloud/alcor/issues/522
            * look into this issue -  failed to delete subnet entity, throwing exception gateway port not found. May be related to the Cache in PM. 
        * PM setRS issue: https://github.com/futurewei-cloud/alcor/issues/524
    * Node Mgr change to support per-node MQ configuration: https://github.com/futurewei-cloud/alcor/issues/490 (Min Chen)
        * Proxy is done, PR not sent yet, do we need to add rollback? (No rollback needed)
    * IP address replacement: https://github.com/futurewei-cloud/alcor/issues/218 (Xiaoyan) 
        * Working to address comments in PR.  
3. Scalability Test Framework & Report review (Jianwei & Wei)
    * Current status: Got 6-7 machines, currently working on setting up envionment. 
    * Test cases:
        * API functionality for VPC, subnet, port, router, security group
            * create, update, delete latency
        * Concurrency: Keep adding qps and record latency to see how the system is handling.
        * Mix scenes: create port/vpc/subnet at the same time.
    * https://github.com/futurewei-cloud/alcor/issues/439
    * https://github.com/futurewei-cloud/alcor/issues/425 
    * https://github.com/futurewei-cloud/alcor/issues/283

4. Design Discussion
    * SDN GW design: https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/gateway_integration.adoc
    https://github.com/futurewei-cloud/alcor/pull/517 （Add another design diagram, Xiaoyan to start looking into it) 

# Alcor Open Source Community Meeting 12/27/2020

1. Design Discussion
    * Agenda: MQ deep dive: https://github.com/issacyxw/mqdesign/blob/main/pulsar%20design1221.docx 
        * Continue with the work, and start implementation.

