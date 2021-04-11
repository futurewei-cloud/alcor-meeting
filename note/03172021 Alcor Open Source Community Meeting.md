# Alcor Open Source Community Meeting 03/17/2021

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

1. MQ design (Xuwei): https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc
    * Tasks assigned
        * Luyao: Working on ACA subscribes and receives messages, function calls 
        * Chenmin: Pulsar related interfaces and functions
            * Focus on DPM cache, assume information is provided in the cache, make decision bases on the number of ports, and work on the algorithm. 
        * Jiawei: will pick up on the implementation soon
2. On-demand workflow demo 
    * Demo setup: 1 NCM instance, 1 test controller to simulates DPM, 2 ACA host, each will run a pod, (host 1, pod 1, host 2 pod 2)
    * Flow: When traffic management sends message to NCM, Host 1 will not know about pod 2 in host 2. Communication will be on demand, ACA will not receive all messages. 