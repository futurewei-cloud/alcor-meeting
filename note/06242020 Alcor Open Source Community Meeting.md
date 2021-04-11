## 06/24/2020 Alcor Open Source Community Meeting
 
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
### Status Update

Meeting Recording: https://youtu.be/zq4LWLLHfJI

1. Status Update
     1. Testing for RocketMQ:
        i.Action Items:
              1. Find the limit for topics, 10,000 topics limit is not enough.
              2. Verify whether producer is the bottleneck of the slowdown from the client side  when sending request.
              3. Add data for latency
              4. Find the upper limit of the topics, for example, if the topics limit is almost reached at 200,000 small topics, add another 100 big topics to see how the performance turns out.
              5. Change the ratio of producer and consumer and get test result
                 1. 1 producer 10 consumers
                 2. 1 producer 50 consumers
                 3. 1 producer 100 consumers
     1. DHCP Design
        1. Eric: Turned ACA into open flow controller, got the dependency. Will work on some proof of concept work. Will have a PR ready this week.
        2. Wu Nan: The code is there, but have not run it yet. Will use local for now and change the database later.
           1. Update goal state,  adding network ID will make the architecture more flexible.
              1. Not a blocking issue
        3. Network Status Handler
           1. An function to track operation status and collect elapsed time. After the data is collected, will send to DPM.
     2. Nova Integration
        1. Found few issues during testing
           1. Query
              1. When querying, it will return all fields. While neutron only returns a few, currently working on adding filtering mechanism (code is done, testing phrase)
                 1. Also run into other issues when applying filtering like: Take subnet as an example, overwrite a submit to database, and update only allows to update some of the fields. The submit field is optional. Subnet updates will check all fields.
              2. Ignite is updated to client mode, but client mode has limited functions. It does not support querying by parameters.  We changed it to ignite mode which is relatively heavy but fully functional. This can meet the needs of query, but needs to look into the performance.
              3. Will get more performance data and determine the bottleneck.
2.  630 Major Focus
     1. Elastic IP Manager
     2. Nova Integration
     3. Network Echo
3. Blocking Issue/Questions
     1.  Liguang: For bucket configured at 512, if the corresponding slash is 23, then we are okay. If it's slash 24, there may be an IP address segment that does not have so many buckets. When we do random bucket generation, there's a big chance the IP segment will fall under the 256.
         1.  Yuanwei: Will take into consideration of this and update the design and code.
     2. Want to see the E2E deployment? Is the environment available? 
        1. Will release a deployment file after implementing auto-deployment. 
 