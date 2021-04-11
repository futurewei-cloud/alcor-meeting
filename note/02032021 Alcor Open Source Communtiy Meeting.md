# Alcor Open Source Community Meeting 02/03/2021

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