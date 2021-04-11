# Alcor Open Source Community Meeting 10/20/2020

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

1. Alcor Project Community Update 10/20/2020
    * Alcor Project 
        * Cloud-Native Architecture
            * Alcor Controller Innovation
            * Alcor Agent Innovation
        * Alcor Component Snapshot and Development Status
        * Performance Comparison with OpenStack Neutron
        * Migration Plan from Neutron
        * Open Source Community Involvement
        * Planning for Second Half of 2020
2. Announcement of feature/issue tracking on GitHub
    * Will run Alcor project entirely on GitHub, new issues will be opened and assigned to owners
3. Subnet Level Programming Path https://github.com/futurewei-cloud/alcor/pull/429
    * The current port manager design sends down message base on port level. Currently, we have new use cases to update the routing rule status for the subnet. We will need to add a new programming path for the new use case - design in dicussion. 
4. Current Work Update
    * Scalability test framework update (cont'd): https://github.com/futurewei-cloud/alcor/issues/439 https://github.com/futurewei-cloud/alcor/issues/425 https://github.com/futurewei-cloud/alcor/issues/283
    * Southbound scale-out: MQ implementation update (cont'd): https://github.com/futurewei-cloud/alcor/issues/404  https://github.com/futurewei-cloud/alcor/issues/405
    * Security Group host design discussion and update (cont'd):  https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
    * SG deletion issue update: https://github.com/futurewei-cloud/alcor/issues/413
        * Problem addressed, solution dicussion. 