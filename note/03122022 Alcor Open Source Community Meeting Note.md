# Alcor Open Source Community Meeting 03/12/2022


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
1. Distrinet M1 Milestone Overview
	1. Create lxc image for alcor-control-agent (aca) https://github.com/futurewei-cloud/Distrinet/issues/14 - installation issue 
	2. The performance and limitation of distrinet #17 https://github.com/futurewei-cloud/Distrinet/issues/17  node creating issue 
	3. Implement Clos topology in Distrinet and Simple performance test #21 https://github.com/futurewei-cloud/Distrinet/pull/21
2. Distrinet Milestone 2 Discussion and General Q&A
    1. Create a demo case with simple topology with ACA and OVS #22 https://github.com/futurewei-cloud/Distrinet/issues/22
    2. Deploy the Alcor microservices as lxd/lxc containers in distrinet #23 https://github.com/futurewei-cloud/Distrinet/issues/23  - research on the workload and hopefully can be done in one deployment file 
    3. https://github.com/futurewei-cloud/Distrinet/issues/24 https://github.com/futurewei-cloud/Distrinet/issues/24 
    4. Integrate Test Controller (k6 or python scripts) to generate requesting payload #26 https://github.com/futurewei-cloud/Distrinet/issues/26
        i. Test controller enhancement: https://github.com/futurewei-cloud/alcor/pull/743
    5. Todo: Time estimate for M2