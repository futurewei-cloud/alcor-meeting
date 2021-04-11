# Alcor Open Source Community Meeting 11/18/2020

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

## Status Update

1. Alcor-Zeta Integration
    * Interface-Zeta Integration Implementation https://github.com/futurewei-cloud/alcor-control-agent/pull/158
        * Eric to merge his change for port delete 
        * Also includes a minor change on the contract
    * Improve ACA Deployment Model #161 https://github.com/futurewei-cloud/alcor-control-agent/issues/161 : Work arrangement needed
    * https://github.com/futurewei-cloud/alcor-control-agent/issues/162 - No further question at the moment
    * https://github.com/futurewei-cloud/alcor-control-agent/issues/163 - Make sure E2E is working locally. Focus on how to scale, also needs to have a unified envrionment. (Qianyu and Huaqing to work on this together)

2. DHCP Enhancement to include GW info https://github.com/futurewei-cloud/alcor-control-agent/issues/159
    * Jianwei:  DHCP new features: https://github.com/futurewei-cloud/alcor-control-agent/pull/164 
    * Will focus on ACA on demand rule after port delete is finished
3. ARP responder for L2/L3 neighbors: https://github.com/futurewei-cloud/alcor-control-agent/issues/117 
    * Luyao: Coding is almost finished, will push PR today

4. Security Group Host Implementation Update (cont'd) https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc

    * No update due to priority change
5. DPM v2.0 implementation follow up https://github.com/futurewei-cloud/alcor/pull/472 (merged)
    * Piaoping: updated comments in the PR
    * Will need to add DPM cacahe layer (will focus on subnet level port cache) after subnet manager and router manage is done for E2E testing. 
6. Pulsar DPM Client:  https://github.com/futurewei-cloud/alcor/pull/481
    * Worked with Chengmin on the code, PR sent
    * Passed test locally

## Scalability Test Framework & Report Review

1. https://github.com/futurewei-cloud/alcor/issues/439
2. https://github.com/futurewei-cloud/alcor/issues/425 
3. https://github.com/futurewei-cloud/alcor/issues/283
4. Data Plane - Use cases to be added: 
    * Divide neighbor messages into multiple dpm
    * Create 1000, 10,000 ports at the same time to get throughut, latency data and compare the data with normal path. 
5. Pulsar Testing - 3 nodes and 6 nodes data

## Design Discussion

1. Southbound scale-out: MQ implementation update (cont'd): https://github.com/futurewei-cloud/alcor/issues/404  https://github.com/futurewei-cloud/alcor/issues/405
2. Subnet-level programming path: https://github.com/futurewei-cloud/alcor/pull/429
3. Alcor Support various dp: https://github.com/futurewei-cloud/alcor/issues/478
