# Alcor Open Source Community Meeting 10/13/2021, 10/14/2021



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

**10/13/2021 Meeting Notes**

1. Overlay Edge Use Case Introduction

**10/14/2021 Meeting Notes**

1. Univeristy Collaboration (USTC)

* VPC-based implementation for Message Queue scale path (Min Chen/Luyan Luo)
    * Min: Submit PR #1 to upgrade GS v1.0 to GS v2.0 by 10/16. Submit PR #2 to add Pulsar support to DPM by 10/18. 
    * Start integration test by 10/22 
* Scalability test framework for 1M nodes regions and 100K ports VPC (Jiawei Liu/Hanfeng Zhan/Jing Fan)
    * Jiawei/Hanfeng: Set up Maxinet in 3 nodes following quick setup guide; Hitting a blocking issue of a missing folder "pox";
    * Target: Prepare a Maxinet demo by next Meeting 10/22
* ML-based on-demand programming (Yan Yu/ Shuang Liang/ Chen Min)
    * Min: Present a draft design based on online retail recommendation system and leverage VM-VM similarity
    * Shuang: Working on historical data modeling for VM-VM connectivity that covers network neighborhood, routing, security group
    * Yu: Working on modeling historical data as vectors and GoalState recommendation algorithm.
    * Target
        * Start a paper presentation starting from next week 10/22 (bi-weekly)
        * ETA for project ETA: 10/22