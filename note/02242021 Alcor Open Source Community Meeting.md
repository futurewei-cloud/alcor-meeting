# Alcor Open Source Community Meeting 02/24/2021

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