# Alcor Open Source Community Meeting 12/22/2021


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

## Status Update ##

1. VPC-based implementation for Message Queue Scale Path (Min Chen/Luyao Luo)
    * Luyao: Completed the interface of dynamic topic subscription  and the memory storage of topicinfo 
        * Did a demo on the e2e scenario where two ports can ping each other
    * Fangjin: 
        * Test the message channel to accept messages in unicast mode - completed 
        * Add message channel support for goal state v2 - completed 
        * Currently working on: Testing the messaging functionality of dynamic subscriptions

2. ML-based on-demand programming 
    * Yuyan: Dataset and Model 
        * Dataset:  Processed Google's dataset into one that fits our model
        * Model: As for model implementation, there's no issue on the code, but need more time on data processing.
        * Will summerize all the work in a document
    * Liangshuang: Completed the part of the code module that reads the goal state information and builds the topology map
        * No data yet, currently processing data
        * Shuang also gave a brief overview on the goal state logic 
        * Next: Share te document on current work
3. Scalability test framework for 1M nodes regions and 100k ports VPC 
    * ZhanHanfeng:
        * Organize previous works and outputs in a docuement, including the 6000 servers set up for the server room 
        * Learn the interaction logic between distrinet and RYU, add a layer for Alcor controller, this will not replace the orgional RYU controller since they are different layers of controller (virtual and physical)
    * Wangyangyu
        * Plan to finish the local automated build script for distrinet 
        * Start testing on both local and sever envrionment


