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

1. Jiawei shared the work progress for the ongoing distrinet work items

 * Distrinet scale push (Chenmin)
    * Current progress:
        * RYU cluster setup completed
        * Tested using 10 RYU cluster, client master (2 cores + 2G) , and worker node (32 cores + 64G)
            * Result:
                * Single master scale is known to be greater than linear 400, will continue to follow up 
                * Single master + 1 worker - did not exceed 700
                * Single master + 2 workers - greater than 750, but did not make it to 800
    * Next steps
        * Will upgrade client configuration before proceeding for more testing 
        * Will turn off controllers and see if it affects the scale test

 * Embedding Neutron
    * Current progress
        * Successfully implemented the OpenStack yoga version in local environment  (Completed using devstack, 1 control node and 1 compute node)
        * Comparison of the acquisition and method of OpenStack token
        * OpenStack CLI and API 
        * Simple test for OpenStack to use API to get security group
        * OpenStack and neutron architecture learning
    * Note: may need more time for this milestone 

2. Luyao shared the work update for ML for network
    * Complete configuration release prediction process
        * Phrase 1: Academic paper learning and researching, data processing, data collecting
        * Phrase 2: Generate a user classification algorithm: Do benchmarks on different browsing datasets, produce classification algorithms, and then see how many performance integrations there are
        * Phrase 3: Generate a configuration recommendation algorithm
    * Use the algorithm on current dataset and hope to meet expected performance 

3. Academic Paper Learning & Sharing
    * Yuheng shared learning from paper: An Online Classification of Users Activities Using Machine Learning on Network Traffic 
    * Lilong shared learning from paper: Cloud Cluster: Unearthing the Functional Structure of a Cloud Service 
