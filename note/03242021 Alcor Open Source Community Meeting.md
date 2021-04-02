# Alcor Open Source Community Meeting 03/24/2021

1. Alcor on-demand Demo
    * On-demand demo by Rio. The team was able to decrease latency from 2 second to 50ms. 

2. MQ Design and Implementation Discussion  https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc

    * How will gRPC notify new nodes to subscribe to topic?
        * For DPM to notify ACA, suggest adding service API (gRPC). Liguang will design the API and update the schema for Chenmin and Luyao to continue with the implementation. 
    * Removing multi-task topic?
        * Look into related information on how this will impact large scale VPC scenario. If no sufficient information is found, can proceed with the implementation and test it out the result. 
    * Local cache and query related question
        * Reach out to Piaoping on Slack if running into questions
    * Task Allocation: https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc#task-allocation


3. New Proposal with USTC

    * Topic 1: SDN southbound scalability
        * May 2020 -April 2021: MQ-based scaling path
        * May 2021 - TBD: SDN performance framework (control and data plane)
    Topic 2 : Theoretical Research
        * VPC slicing assignment: MINLP, MQ-based
        * ML algorithm for on-demand programming
    Topic 3: Alcor SDN verification engine
        * Enable state verification, closed loop control and zero-touch operation 
        * Analysis for static verification or Synthesis for runtime verification (flow id, vni id, latency analysis, potential bottleneck diagnosis)
