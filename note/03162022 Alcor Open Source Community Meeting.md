# Alcor Open Source Community Meeting 03/16/2022


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

### Participants ###

USTC: Jiawei Liu, Min Chen, Luyao Luo, Seven Wang, zhanhan feng, Shuang Liang, Feng Jin, Yangyu Wang
Futurewei: James Chung, Zhen Zeng, Yan Mo, Liguang Xie

### Meeting notes ### 

Large-scale cloud emulator:
* James went over issues on https://github.com/futurewei-cloud/Distrinet for Milestone M1 (due at 3/9) and new issues for Milestone M2 (due at 3/30).
* Yan Mo gave a demo for ACA+OVS docker container creation.
* Jiawei, James, and Min Chen discussed how to arrange the tasks to modify the test scripts in Jenkins and Test controller and how to migrate scripts to K6.
* Min Chen, Jiawei and James discuss the issue of creating ACA Lxd image. 

Southbound discussion:
* Min Chen proposed the solution to solve the number of port calculation for a large VPC in ignite database through SQL query function. 
* Min Chen and James discussed the issue to create Pulsar server in Jenkins environment. The current solution is to create a host process on the Jenkins worker node.

