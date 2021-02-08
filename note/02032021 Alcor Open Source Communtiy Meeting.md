# Alcor Open Source Community Meeting 02/03/2021

1. Zeta and Alcor Update
    * Zeta deployment issue debug (Rio, Xiaoyan) 
2. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc
3. Status Update
    * MQ lib fix (Luyao) - update to newer gRPC version 
    * Node Mgr change to support per-node MQ configuration (Min Chen): https://github.com/futurewei-cloud/alcor/issues/490 - created 3 test cases, local tests passed, currently awaiting PR review from Piaoping.
    * VPC Mgr change for Zeta Integration (Xiaoyan): https://github.com/futurewei-cloud/alcor/pull/545 Code merged, remaining issue on gateway manager transaction.  Continue to work on integration with Zeta. 
    * MQ deep dive cont'd (Xuwei): https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc Design doc updated, data schema is linked to UML diagrams with highlighted field.  Will continue to update design doc based on today's dicussion.

4. Design Discussion
    * Distributed Transaction: rollback mechanism flow dicussion (Piaoping)
    * AGA design: https://github.com/futurewei-cloud/alcor/pull/546 (Eric) Design review