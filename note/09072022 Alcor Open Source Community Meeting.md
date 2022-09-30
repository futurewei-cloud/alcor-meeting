# Alcor Open Source Community Meeting 09/07/2022


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
* Explore the extensibility of Distrinet based on Neutron
    * Successfully built the self-service Openstack of ovs-agent and passed the L3 test on the VM side
    * Successfully transferred the work from provider network to self-service network, was able to test for L2, but not for L3.  
    * Next: Need to prepare milestone report that will show the advantage of Distrinet work (using this testing environment, how many more machines we can simulate, ultimately cutting down the cost for testing ) 
### ML for Network
* Work Update
    * Lilong: We can only use data of subnet and subnet name from the ground truth. 
    * Luyao shared updates on the recommendation system, currently working in local environment, will upload the demo
    * Weidong shared dataset experiment updates
        * Experiment with Transformer base
        * Experiment with Yelp
        * Experiment with ML 10M 