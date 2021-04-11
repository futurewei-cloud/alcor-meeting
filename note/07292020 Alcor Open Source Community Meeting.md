# Alcor Open Source Community Meeting 7/29/2020 #

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

Meeting Recording: https://youtu.be/Id5nwcvEyzE

### Bug/Blocking issues
 
* Service Token (Solution ready) - https://github.com/futurewei-cloud/alcor/issues/332
* Service log, port delete and create issue
* Refactoring port manager
  * Problem of ignite deadlock, appeared in the K8S environment
     * Did not set up timeout limit for read, which caused the blockage. 
 
 
### Status/PR Update
* Elastic IP Openstack Integration
   * Had the PR out
   * Next step is E2E test
* Mac Manager Selector (Will merge next week)
  
    * One more item left: batch performance testing
  
* Network ACL Manager (Not priority, will start next week)

* DHCP
  * Almost ready for E2E
  * More discussion on unit test on Slack Channel.
 
### Items in Planning
* Southbound Distribution
* MQ
* Agent