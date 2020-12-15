# Alcor Open Source Community Meeting 12/09/2020

1. Alcor and Zeta Integration
    * https://github.com/futurewei-cloud/alcor-control-agent/pull/172 
        * Address comment in PR
        * Ensure no regression, all tests passing 
    * Integration: https://github.com/futurewei-cloud/alcor-control-agent/pull/170  
        * Update Zeta environment setup, Rio will help with environment setup
        * Push change and add test cases
    * Testing: 
        * Dec - ACA + Zeta
        * Jan - Integrate with Alcor Controller for completed E2E testing

2. Team Issue Triage https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc - 
    * Feature request, ETA
    * Slack Status Update Channel - weekly update

3. Status Update
    * ARP responder for L2/L3 neighbors: https://github.com/futurewei-cloud/alcor-control-agent/issues/117
    * DPM v2.0 implementation follow-up: Cache layer implementation and PM change https://github.com/futurewei-cloud/alcor/pull/486 - merged
    * Security Group host implementation update (cont'd):  https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
    * Pulsar DPM Client follow-up: https://github.com/futurewei-cloud/alcor/issues/490  https://github.com/futurewei-cloud/alcor/issues/494 
        * Two follow up items: 
            * Ensure no regression
            * DPM Issue: https://github.com/futurewei-cloud/alcor/issues/494 

4. Scalability test framework & Report review
    * https://github.com/futurewei-cloud/alcor/issues/439
        * 393 closed. Working on 3 other parts
            * [Scalability Test] Part 2: Alcor E2E Performance Report #496
            * [Scalability Test] Part 3: Latest Platform E2E Performance Report
            * [Scalability Test] Part 4: Re-Evaluate DPM Concurrency in Large VPC scenario #499
        * Alcor E2E Southbound test comparison 
            * Large scale testing
            * Testing specific scenarios
    * https://github.com/futurewei-cloud/alcor/issues/425 
    * https://github.com/futurewei-cloud/alcor/issues/283

5.  Design Discussion
    * MQ deep dive: https://github.com/VanderChen/open-doc/blob/master/pulsar%20design1119.docx
    * Alcor Support various dp: https://github.com/futurewei-cloud/alcor/issues/478