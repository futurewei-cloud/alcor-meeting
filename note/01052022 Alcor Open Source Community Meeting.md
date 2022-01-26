# Alcor Open Source Community Meeting 01/05/2022


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

Meeting Notes:

1) Southbound Discussion
    * Chenmin: 
        * Completed and shared the cross-host dynamic topic sending for southbound demo
        * Issuse dicussion: Map vpcId to hostIp in MulticastGoalStateV2 #728 https://github.com/futurewei-cloud/alcor/pull/728
        * Completed the topicinfocache design and submitted PR
    * Luyao:
        * Submitted PR: Add grpc thread for pulsar subscribe info #274 https://github.com/futurewei-cloud/alcor-control-agent/pull/274
        * Next: Complete code review, help with large scale testing, and get familiar with southbound work
    * Fangjin:
        * MQ gtest now in the main repo.
        * Completed a test on using gRPC channel to test the dynamic message subscriptions
2)  Large Scale Cloud Emulator:
    * Jiawei: 
        * Implemented a simple version for the custom topology
        * Still working on the document on how to configure the distrinet terminal
        * Discussion topic update: Understanding Linux bridges created by Distrinet #3 https://github.com/futurewei-cloud/Distrinet/discussions/3 
    * Hanfeng: 
        * Worked on a document to summerize previous work, also helped on setting up the test envrionment on Git
        * Disucssion topic update:  Create lxc image for alcor-control-agent (aca) #6 https://github.com/futurewei-cloud/Distrinet/discussions/6
    * Yangyu:
        * Working on the distrinet process automated script 
3) ML-based on-demand programming 
    * Discussed on the deliverables of ML-based on-demand programming
    * Liangshuang: Shared few findings from papers, will find a time to present all findings
4) Large scale testing document discussion (Chenmin) 
    * Scalability
    * Robustness

