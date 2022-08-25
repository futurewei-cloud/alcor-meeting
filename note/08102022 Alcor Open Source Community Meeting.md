# Alcor Open Source Community Meeting 08/10/2022


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


## Meeting Notes

1. James shared 730 releases: https://github.com/futurewei-cloud/merak/releases/tag/v0.1-alpha 
    * Scneario Manager
    * Merak Topoology
    * Merak Network
    * Merak Compute
    * Merak Agent
    
2. Distrinet Work Update
    * Explore the upper size of Distrinet cluster
        * A stable cluster can now reach a scale of 8k. For a 10K scale cluster start up, there's about 12% package loss.  - For the current priority, we will stop the testing for now. 
    
    * Explore the extensibility of Distrinet based on Neutron
        * Deployment test based on Kola project and previously built devstack
            * Continue to fix bugs of mounting libvirt runtime on docker container, looks like it can be solved by enabling systemd in container. (WIP)
            * After reading Kolla exported docker file of nova-compute container, we found build nova-compute from a private file, so it will not work for us. 
            * Tried to install libvirt in container and enable it, this worked for nova-compute service. Now controller can discover container as a compute node. 
        * Instead of using devstack, build our own distributed OpenStack to further explore 
        * Next up:
            * Consolidated two options discussed above, organize the dockerfile that starts the compute node in the container 
            * Attempt to replace and start inside the Distrinet 
            * Bottleneck: Use cases and the type of information sequences generated are limited 

    * Explore more scenarios based on K6
        * Current status: 
            * Finished organizing the code
            * Finished configuration setup on couple use cases for southbound on demand communication
            * Bottlenecks: Use cases and the type of information sequences generated are limited 
        * Next: 
            * Wrapping up working code
            * Further expand the testing scenarios based on requirements 
    
3. Academic Paper Discussion
    * Performance Evaluation of K-means Clustering Algorithm with Various Distance Metrics 

4. Min Chen shared the proposal for dual paths for the Distrinet scale test and discussed the engineering work needed. 

