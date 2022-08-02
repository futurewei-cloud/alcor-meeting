# Alcor Open Source Community Meeting 06/22/2022


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

1. Distrinet work update

    * Chenmin shared the testing plan for the Distrinet scale push - includes testing on bare metal and on Distrinet 
        * Algorithm
            * MQ: MQ with node granularity
            * E2E: End to end 
        * Testing metrics
            * Latency
            * Redundancy 
            * Control plane load 
        * Testing scenarios
            * Large VPC
            * Multiple VPCs 
    * Jiawei discussed with the team on the 3 different ways to proceed with the embedding neutron work 
    * Issue discussion: Explore the upper size of Distrinet cluster #45 https://github.com/futurewei-cloud/distrinet/issues/45

2. ML for Network 
    * Lilong shared the plan on relying on the collected traffic information to do VM/tenant clustering
        * VM to VM overlay traffic information
        * VM and tenant attribute messages
        * Other types of information that change over time



