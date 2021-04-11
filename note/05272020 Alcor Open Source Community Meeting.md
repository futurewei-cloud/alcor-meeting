## 05/27/2020 Alcor Open Source Community Meeting 

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

Meeting Recording: https://youtu.be/gu_uaFl7dMQ

1. Quick Update/Sync
    1. Piaoping: Who provides the information for neighbor?
        1. Information is filled in during pod creation.
        1. The subnet / port manager is the DPM client. Whoever picks it up should be the person who created the Pod to receive this information
2.  Root Manager - API
    1. When is vpc routing used?
        1. After the routing table is separated, it is equivalent to that I can associate it with other flow tables. If the routing field is written into the VPC, it can be used as a custom field of the subnet.
3.  Southbound messages distribution Dataset  (Yunwei)
4.  API  - focus on core scenarios
5.  Keystone Integration
    1. PR submitted
    1. Finished 60% of the testing
    1. Cache selection
    1. Action items: environment setup guide