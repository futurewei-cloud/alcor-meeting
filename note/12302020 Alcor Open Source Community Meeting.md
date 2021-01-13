# Alcor Open Source Community Meeting 12/30/2020

1. Team Issue Triage: https://github.com/futurewei-cloud/alcor/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc

2. Status Update
    * ARP responder for L2/L3 Neighbors (Luyao) https://github.com/futurewei-cloud/alcor-control-agent/issues/117
        * Action Items/Remainining Works (Testing)
            * Action Items Addressed in PR 167
                1. add more comments in code for anything that's not simple, it will help us to maintain the code moving forward
			    2. address the feedbacks in this PR
			    3. fix up the test environment, likely to use two machines, so really exercise this new feature, add test instruction in the test file, share the test results in this PR
                4. confirm the existing aca_tests are still passing with this change, share the result in this PR, instruction here: https://github.com/futurewei-cloud/alcor-control-agent/wiki/How-to-run-the-full-suite-of-aca_tests
    * PM & DPM v2.0 implementation follow-up (Piaoping): 
        * PM cache issue: https://github.com/futurewei-cloud/alcor/issues/522
        * PM setRS issue: https://github.com/futurewei-cloud/alcor/issues/524
        * Port creation issue: https://github.com/futurewei-cloud/alcor/issues/527
    * Node Mgr change to support per-node MQ configuration: https://github.com/futurewei-cloud/alcor/issues/490 (Min Chen) (Not discussed)
    * IP address replacement: https://github.com/futurewei-cloud/alcor/issues/218 (Xiaoyan)
        * Fixed and refinement of some issues for IP address #218
        * Design a test case for update fixedlPs of the port
        * Ignite support batch insertion #226 is done
        * Sort out the interaction between other microservices and PortManager of creating a port
        * Will work on GatewayManager

3. Discussion
    * MQ deep dive cont'd (Xuwei): https://github.com/issacyxw/mqdesign/blob/main/pulsar%20design1221.docx
    * SDN GW design: https://github.com/futurewei-cloud/alcor/blob/master/docs/modules/ROOT/pages/high_level/gateway_integration.adoc https://github.com/futurewei-cloud/alcor/pull/517