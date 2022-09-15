# Alcor Open Source Community Meeting 08/24/2022


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

### Distrinet

1. Explore the extensibility of distrinet base on neutron (Jiawei)

    * Made changes to the nova source code, familiarize with the Openstack create server workflow, (including interaction and scheduling algorithm) 
	* After evaluation, decided to modify the source code based on the fake driver. Currently cannot start the server successfully, discussed the errors for starting the server 
	* Clarified the debug steps for Devstack
    * Modification based on https://github.com/venkataanil/nova_fake_driver
    * Built a yoga versions of Openstack using self-service network and ovs-agent. (Using 3 nodes)due to time limitations, the connectivity of the previously built containers has not been tested.
    * Next: Will come up with Detail estimation of all work items 

2. Debug session on the container issue (driver nova not connected to controller) 

### ML for Network
1. Shared the recent update after looking at the actual dataset 
2. Academic paper learning sharing
    * Knowledge-Enhanced Hierarchical Graph Transformer Network for Multi-Behavior Recommend 
    * TemPEST: Soft Template-Based Personalized EDM Subject Generation through Collaborative Summarization
    * Meta-Transfer Learning for Low-Resource Abstractive Summarization 
    * LogAnomaly:Unsupervised Detection of Sequential and Quantitative Anomalies in Unstrctured Logs  

