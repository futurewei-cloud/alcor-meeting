# Alcor Open Source Community Meeting 05/12/2021


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


1. Alcor 430 Release https://github.com/futurewei-cloud/alcor/releases/tag/v0.14-alpha

    *   This release focuses on enabling new workflow, fundamental improvement and code stabilization. Some highlight of the v0.14-alpha release:
        * Deliver 2 new microservices & refactor 1 existing microservice for performance gain  
        * Proof of concept for new on-demand workflow with Network Configuration manager and ACA on-demand engine
		* Introduce SDN gateway manager and finish E2E integration with Cloud Zeta gateway
		* Onboard new Goal State V2 for messaging performance improvement with various refined protobuff message changes
		* Streamline build, test and deployment pipeline and support integrated testing for both control and data plane
        * Code stabilization with 20+ bug fix
2. Topics: Discuss latest process for MQ scaling path implementation
    * [Data Plane Mgr] Support vpc-mode pulsar message queue #613 https://github.com/futurewei-cloud/alcor/pull/613
        * Host resource mapping - line 58-59
        * Filling will be depending on TC
    * Add grpc channel to notify node subscribe MQ #612 https://github.com/futurewei-cloud/alcor/pull/612
        * Add in unsubscribe, otherwise ACA will keep accumulating. Define all APIs in advance 
    * Goal State to ACA latency
        * Add time stamp in the code before sending and after the request is returning
3. Future Planning/Discussion
    * Implementation and optimization of XDP offloading for network services
    * Design and Implementation of Message Service Algorithm
    * Design and Implementation of Network Service Test Platform
    
