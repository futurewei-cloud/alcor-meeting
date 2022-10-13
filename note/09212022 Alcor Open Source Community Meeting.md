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

* Luyao shared the work from last week
    *   Finished building large-scale testing environment with 5 servers and 1 PC. 
        * Server 3 : Openstack controller
        * Server 4,5,6: Distrinet worker
        * Server 7: Distrinet master
        * Pc1: Distrinet client 
    * Shared the physical network topology for testing
        * We can start 400 vhosts in the underlay network in the preliminary result
        * Separately, we can also create 200 namespaces in a single container 
        * We will combine test 1 and test 2 in one testing scenario 
* Yangyu shared academic paper reading takeaway
    * CrystalNet: Faithfully Emulating Large Production Networks

### ML for Network

* Lilong shared update on the clustering testing model
    * IP address distribution
    * Name split, make label with the second filed of the name
    * Label combination
    * Todo: find the correlation between the sources

* Weidong shared academic paper reading takeaway
    * Knowledge-Enhanced Hierarchical Graph Transformer Network for Multi-Behavior Recommendation 