# Alcor Open Source Community Meeting 8/18/2021, 8/19/2021



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

**08/18/2021 Meeting Notes**

1. ML for NCM Planning
    * Algorithm part
        * Actively send down network configuration
            * Automatically send down network configuration when there's a request
        * Semantic merging/semantic checking of network configuration
            * Semantic merging: combine similar requests 
            * Semantic checking: Different types of network configurations are checked to see if there are any contradictions
    * Engineering work
        * Consistency check of network configuration
            * Deployment
                * Information collecting
                * Model reasoning
                * Incremental training
2. Current work update
    * VPC-based implementation for Message Queue scale path (Min Chen/Luyao) 
        * Goal state v2:  need to test the code with Jenkins.  Some logic from VPC as topics still missing
        * ACA code - working on it, made changes on Pulsar version and a couple of files.  
    * Scalability test framework for 1M nodes regions and 100K ports VPC (Jiawei/Min Chen)
        * Functional testing (Fangjin) 
            * Local environment for ACA and control plane has been set up. Waiting for Luyao's work to be completed for ACA and Alcor integration
            * Will begin Jenkins testing
        * Large scale performance testing
            * Function deployment in container：Function deployment in container: Was able to created docker pulsar server and client in local environment.  Was able to create and send down a topic, but ran into issue on the server side.  
            * Researching - The topology of the container
            * Action Item: will begin actual testing first


**08/19/2021 Meeting Notes**

* Research Paper Discussion
    * Message Delivery Paper 
    * Zeta - a Scalable and Robust East-West Communication Framework in Large Scale Clouds
    * Andromeda: Performance, Isolation, and Velocity at Scale in Cloud Network Virtualization