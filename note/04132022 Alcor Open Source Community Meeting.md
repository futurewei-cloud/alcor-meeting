# Alcor Open Source Community Meeting 04/13/2022


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


Meeting Notes
1. Futurewei gives a demo (meshnet) - Zhen
2. Merak Architecture Overview
    * Create a demo case with simple topology with ACA and OVS #22 https://github.com/futurewei-cloud/Distrinet/issues/22 
    * Deploy the Alcor microservices as lxd/lxc containers in distrinet #23 https://github.com/futurewei-cloud/Distrinet/issues/23 - List the order for compilation, and do functional test 
    * Deploy Alcor k8s cluster and connect microservices to ACA containers #24 https://github.com/futurewei-cloud/Distrinet/issues/24 - Need to test with ACA
    *  Investigate the possibility of replacing lxc/lxd with docker #25 https://github.com/futurewei-cloud/Distrinet/issues/25 - First version of code out, need to test. reference: https://github.com/futurewei-cloud/Distrinet/pull/29
    * Integrate Test Controller (k6 or python scripts) to generate requesting payload #26 https://github.com/futurewei-cloud/Distrinet/issues/26 Made change on Jenkins, have not test yet.
3. Zhen gaven an overview of the ML project.
4. USTC update status of ML project
5. Q&A, other issues discussion 
