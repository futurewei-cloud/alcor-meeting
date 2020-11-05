# Alcor Open Source Community Meeting 10/28/2020


1. Zeta-Alcor integration status update
    * Phrase one release: https://github.com/futurewei-cloud/alcor-control-agent/issues/152
        * This release should inlcude both subnet and cross subnet communication.
        * Ready for integration with ACA.
    * Todo: 
        * Sprint 3 expectation: control plane e2e integration
            * Items: normal gateway, ovn path, testing envrionment.
2. Subnet-Level Programming Path
    * New proposal: https://github.com/futurewei-cloud/alcor/pull/429 
        * Create full cache, mapping in DPM instead
3. Scalability test framework (con'd)
    *   https://github.com/futurewei-cloud/alcor/issues/439 
    * https://github.com/futurewei-cloud/alcor/issues/425 
    * https://github.com/futurewei-cloud/alcor/issues/283
4. Southbound scale-out: MQ implementation update (con'd) https://github.com/futurewei-cloud/alcor/issues/404  https://github.com/futurewei-cloud/alcor/issues/405
    * Jianwei: Pulsar machine for single node test result: 
        * One port, ten thousand neighbors, each simulates one thousand, dpm 500-600 milliseconds, down time.
        * MQ does not support well for large data packets, and needs to be tested again.
    * Pulsar Testing Update
        * The optimization of DPM message processing has been tested
        * gRPC channel testings have been done in the local, will try that in the envrionment.
        * Continue testing to verify whether new features have improved scale


5. Security Group host design discussion and update (cont'd): 
    *  https://github.com/futurewei-cloud/alcor/pull/390
https://github.com/futurewei-cloud/alcor-control-agent/pull/156 draft PR to address some comments

6. ARP responder for L2/L3 neighbors: 
    * Feature request: https://github.com/futurewei-cloud/alcor-control-agent/issues/117


    