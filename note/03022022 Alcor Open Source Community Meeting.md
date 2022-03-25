# Alcor Open Source Community Meeting 03/02/2022


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

### Meeting Notes

* Southbound Discussion - Min 
    * Shared testing result using Pulsar-Perf and compared test result with our implementation- Min 
        * Will follow up with more discussion in later meetings

*  Large-scale cloud emulator - Jiawei, James, Yangyu, Hanfeng
    * Implement Clos topology and simple performance test  PR out https://github.com/futurewei-cloud/Distrinet/pull/19
        * Topology setup completed
        * Pingall test
        * Topo check
        * E2E bandwidth test 
    * Create lxc image for alcor-control-agent (ACA) https://github.com/futurewei-cloud/Distrinet/issues/14 - compiling issue, should be addressed soon
    * The performance and limitation of mininet in a single machine https://github.com/futurewei-cloud/Distrinet/issues/15 - Currently stuck in node creating/generating stage, should be unblock in a week
    * The performance and limitation of distrinet https://github.com/futurewei-cloud/Distrinet/issues/17 - hit issues about the remotely bare-metal machine setup, will raise the issue encountered on GitHub

* Machine Learning Discussion - Min, Yuyan
    * Working on model optimization. The result on the data we used previously for testing our model did not turn out well.  Currently testing our model with a different dataset. 

* Alcor Release v1.0 Overview https://github.com/futurewei-cloud/alcor/releases/tag/v1.0-beta

