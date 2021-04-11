# Alcor Open Source Community Meeting 03/03/2021

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