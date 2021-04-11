# Alcor Open Source Community Meeting 9/09/2020

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

Meeting Recording: https://youtu.be/N1frLy55_6k

## Status Update ##

**Scalability test framework update**
- The script is finished. The Hash code piece of object was incorrectly filled, which caused a conflict. Made the fix and tested again. 
- Will continue to verify
  - the message send from service to DPM, and message send down from DPM
  - as neighbors numbers continue to grow, keep track of DPM latency (1 port with multiple requests)
- Have 25 servers ready for testing

**Southbound scale-out: MQ topic design and workflow**
- Finalize on PM and DPM contract https://github.com/futurewei-cloud/alcor/pull/364 

**DHCP - next steps**
- PR Merged last week, no blocking issues
- Pending items: https://github.com/futurewei-cloud/alcor-control-agent/issues/126

**Host DVR mac optmization**
- Updated the design based on suggestion from Yuanwei, implemented and verified the solution in ACA. (Confirmed that the new idea is working) Improved the workflow

**VPC APIs in public clouds**
- how to use VPC in openstack? https://github.com/futurewei-cloud/alcor/issues/379 
- Request for a list of APIs 

**Discussion of subnet static route**
- Do we need this function (subnet static route)
  - Not in current operation
  - This function will be postponed. 

**End to End Testing** 
- Need API Gateway change for E2E testing
- VPC scenario 
