# Alcor Open Source Community Meeting 03/03/2021

1. Status Update
    * MQ design (Xuwei): https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc
        * Implementation in progress
    * NCM understanding and implementation (Xiaoyan/Piaoping): https://github.com/er1cthe0ne/alcor/blob/design%2FAGA/docs/modules/ROOT/pages/infra_services/NCM_design.adoc
        * clarification on how messages might be sent down in wrong orders

2. Requirements from Users
    * Service Agent
        * Synchronously deliver configuration to the service bearer, easy to obtain and persist the actual effective status of each node configuration
        * Same services processing will be merged together, to improve computing node resources and to improve resource utilization
    * Service DB to support database by tenant
        * When the business continues to grow on a large scale, different combinations of configurations can be divided into different databases for storage to avoid the database becoming a bottleneck
    * Southbound synchronization middleware
        * Solve the current performance bottleneck encountered in the southbound distribution of Kafka clusters
        * Shield the specific implementation method of configuration distribution to reduce service  design/development cost