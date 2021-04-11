# Alcor Open Source Community Meeting 7/13/2020, 7/15/2020 #

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
 
Meeting Recording: 

* 7/13: https://youtu.be/7RiXpPjIGzU
* 7/15: https://youtu.be/jdKdo9Dcdqk


##  7/13 Status Update 

### E2E Debug Session

* K8S Deployment (Multiple Instances)
    * There's situation with lost data.
    * Deployment issue
* Integration with Keystone
    * There are some problems when registering the Alcor service here. (Issue is solved)

### Quick Summary (End of meeting)

* API gateway  (checked)
* Port manager (checked) #295
* Integration with Keystone (Checked)
* Currently can run performance test with 3 nodes cluster. Will merge to 20-25 node cluster soon.

##  7/15 Status Update 

* Keystone integration is done.
* Mac Manager Performance
    * Need to do batch testing
* Refractor
    * Piaoping: Will finish refactoring this week. Need this information to see which manager needs to be improved
* DHCP
    * OpenFlow dependency has been checked in
    * Will be helpful to have the interface from Wunan first
    * Target this month to deliver this task
    * Without DHCP, can only provide static IP address to VM for testing
* Performance Test
    * I/O is a bottleneck at 97-98% utilization rate
    * When creating topics in the early stage, it will be particularly long about 7-9 minutes before throughput starts to show number. During this time, only the number of topics will rise.
    * Another way we tried is if we do not delete the topics. We just disconnect and reconnect, the throughput rate is okay.
    * Action Items: Get the get the parameters for the target we defined previously, and finalize the model selection soon. Will determine the model selection based on the parameters and the architecture. Can also look into some researches to help making the decision.
* Next Steps
    * Initiating the discussion for 1130 milestone.
       * Southbound distribution design and implementation