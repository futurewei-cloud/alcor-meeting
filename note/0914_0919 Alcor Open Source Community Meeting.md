# Alcor Open Source Community Meeting 09/14/2022


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


## 09/14/2022

### Distrinet
* Explore the extensibility of Distrinet based on Neutron
	
    * Jiawei shared the E2E demo for distrinet. The team provided feedback and had a discussion. 
	
### ML for Network
	
* Luyao shared the update on the model and result for the recommendation model
* Lilong shared the result for the clustering model
* Next: Put together a slide that includes the process on how we got the above results, ad-hoc meeting to be scheduled

## 09/19/2022 (Ad-hoc)

### ML for Network 

* Clustering and Recommendation Testing Process and Algorithms Sharing

    * Lilong shared the clustering testing process (dataset, matric, data pre-process, algorithm, result, label)
        * After clustering, one cluster has one subnet label or more, so does name label, one name/subnet label may appear in multiple clusters.
    * Luyao shared the recommendation testing process
        * Dataset preparation with sample config dataset 
        * Model used CNN+Personalized Attention, SIGKDD'19 (Need to look into the paper further)
        * Training process
        * Test 
        * Other algorithms
    * Will continue working on the testing 
