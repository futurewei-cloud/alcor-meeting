# Alcor Open Source Community Meeting 09/01/2021

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
    * Chenmin - Connect the last two goal state v1 v2 ports together and implement it
        * Question regarding: Add unicast GS and MulticastGS based on GoalState V2 #625https://github.com/futurewei-cloud/alcor/pull/625  (Question regarding VPCid)
    * Fangjian: Functional testing question
        * Testing is looking good for gRPC and MQ. How to deal with scenario where we switch from large scale testing to small scale testing?
            * Testing will need to be based on the testing framework, needs to set up on the testing framework first
        * Next step focus:
            * Start setting up the environment in local machines before getting into anything else
    * NSDI paper discussions (Qianyu)
