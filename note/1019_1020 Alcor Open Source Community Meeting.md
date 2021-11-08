# Alcor Open Source Community Meeting 10/19/2021, 10/20/2021



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

## 10/19/2020 Meeting Note ##

### Zeta Project Collaboration Discussion ###
* Zeta project brief overview/communication from previous communication 
* Zeta current project status
* Zeta testing reports
* Zeta paper -  a scalable and robust VM-to-VM communication Fabric in multi-tenant
* Current item:
    * Zeta second stage: zeta needs to use XDP technology to cache the network function chain in the gateway cluster
    * Zeta and ACA integration
* Future collaboration direction
    * Zeta will also need to support stateful network function (Fault tolerance stateful gateway)
    * Research on different solutions for programming switch 

## 10/20/2020 Meeting Note ##

* VPC-based implementation for Message Queue Scale Path (Min Chen/Luyao Luo)
    * Min: PR #1 merged/jenkins passed PR #2 submitted (#695)
    * Luyao: ACA PR submitted and under review
        * Integration test plan:
            * Step 1: Use PostMan to test basic API functionality (pub & sub)
            * Step 2: Basic E2E test cases: port creation/update, routing rule etc.
            * Step 3: Run Jenkins job (Ping Liguang and Prasad on Slack)
* Scalability test framework for 1M nodes regions and 100k ports VPC (Jiawei Liu/Hanfeng Zhan/Jing Fan)
    * Jiawei/Hanfeng: Maxinet Worker node registration failure; Maxinet not well maintained and working only on Ubuntu 14.02
    * Next Step: Distrinet is good alternative; try MiniNet to get max $ of containers per host; Reimage containers with truncated ACA.
* ML-based on-demand programming (Yan Yu/Shuang Liang/Chen Min)
    * Yu: Present a paper for online retail recommendation system and its ML algorithm (static catalog + customer purchase history)
    * Shuang: Discuss one example of public cloud deployment