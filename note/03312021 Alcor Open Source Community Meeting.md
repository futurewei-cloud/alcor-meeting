# Alcor Open Source Community Meeting 03/31/2021

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

1. Collaboration Topics Discussion
    * Topic 1: SDN Southbound Scalability
    * Topic 2: Theoretical Research
        * VPC slicing assignment: MINLP, MQ-based
        * ML algorithm for on-demand programming
    * Topic 3: Alcor SDN verification engine

2. MQ Implementation Update
    * Min: Will divide work into a few PRs
    * Testing Metrics: will begin testing after codes are merged
        * 100,000 VPC, single pod creation latency 
        * Large VPC, latency for multiple pod creations
        * In large VPC, how many pods we can create in a minute? 
