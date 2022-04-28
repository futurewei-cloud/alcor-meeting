# Alcor Open Source Community Meeting 04/27/2022


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
USTC: Min Chen, Jiawei Liu, Yang Chengyuze, Shuang Liang, ZhanHan Feng, Yuyan, Yangyu Wang, Luyao Luo, JianXianqiang, and Gongming Zhao
Futurewei: James Chung and Zhen Zeng

Meeting Notes:

Large-scale cloud emulator:
1.	Jiawei Liu describes and explain his related issues.
2.	Jiawei shows the deployment architecture for the test with K6 and python scripts in his PR.
3.	J980419xq demo the distrinet with his docker provisioner modification. 
4.	Min Chen explains the code to containerize ACA with lxc container.
5.	Min Chen describes the problem to containerize ignite db.
6.	Min Chen explains his related PRs.
7.	James Chung mentions the tasks for next milestone:
a.	Real test environment for Alcor+ACA with distrinet topology
b.	Performance test on distrinet + docker container on virtual and physical environment
c.	VMs (namespace) in docker containers
d.	Complete K6 scripts for perf test scenarios  

ML:
1.	Luyao, Zhen and James discuss the dataset from USTC data center and proposed the ideas to classify the dataset.
2.	Yuyan and Zhen discuss the data model and potential data schema for the network configuration dataset.
3.	Zhen gives the expectation for next meeting about the ML projects. 
