# Alcor Open Source Community Meeting 11/03/2021

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

### USTC Work Report Update ###

* VPC-based implementation for Message Queue Scale Path (Min Chen/Luyao Luo)
    * Min: 
        * PR #625 Grpc for GoalState V2 merged into main repository
        * Addressed comments for PR #695 Pulsar for GoalState V2
        * E2E Testing - Pulsar for GoalState V2
        * Next: Finish PR #685 and VM similarity strategy/solution plan
    * Luyao/Jin Fang
        * Solved the bugs related to Pulsar version, and updated codes
		* PR #238 submitted - added keyshared mode and listener monitoring
        * Next: Verify whether pulsar consumer can correctly receive GoalState and update status
* Scalability test framework for 1M nodes regions and 100k ports VPC (Jiawei Liu/Hanfeng Zhang)
    * Finished testing the environment for Maxinet and the research on Distrinet 
    * Finished the stress test on the server for Mininet 
    * Next: 
        * Set up environment for Distrinet, and get familiar with the code and logic.   
        * Mininet customized topology stress test
* ML-based on-demand programming (Shuang Liang) 
    *  Analyzed the logic of VM connectivity in VPC through the change on route table, and designed a simple judgement program flow
    * Research on other similar solutions in the market
    * Read and analyzed the json file from the testing data 
    * Next: VM connectivity in depth analysis 



