# Alcor Open Source Community Meeting 01/20/2022


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


Participants: 
Jiawei Liu, Min Chen, Luyao Luo, Hanfen Zhan, Shuang Liang, Feng Jin, Yangyu Wang, James Chung, Zhen Zeng, Liguang Xie

Meeting notes: 

* Large-scale cloud emulator:
    1) James went over discussion topics and issues on https://github.com/futurewei-cloud/Distrinet and gave instructions on how to respond to the topics and issues on GitHub, how to give ETA etc.
    2) Jiawei gave a demo on how to set up a customized topology, completed scripts to set up topology. Next step: program physical network, test data plane connectivity, and submit a PR to GitHub
    3) Yangwu/Hanfeng Wang completed deployment scripts. Next step: Raise a PR for the deployment scripts; Yangwu will also work on performance limitation of Distrinet on single physical server.

* Southbound discussion:
    1) James/Liguang/Min went over and resolved pending items of PR #695, and merged PR. Next step: Min continued to work on PR #726 and #728, and added new MQ support for Jenkins. 
    2) Luyao discussed questions with Liguang on ACA PR #274. Next step: Luyao to try reuse the same gRPC server on ACA to host two services. 
    3) Min discussed his design on on-demand messages modeling and recommendation. Next step: Min to upload design doc on Google Group. 
