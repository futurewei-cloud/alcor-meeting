# Alcor Open Source Community Meeting 9/02/2020

Meeting Recording: https://youtu.be/k9s2Y6wjNT0

## Status Update##

**Scalability Framework**
- Current testing effort, not fully E2E: 
10,000 messages in 5 seconds, single thread. The test is tested according to extreme scenarios with 30 seconds latency (10K Ports, 100K neighbors)

- The test did not run fully E2E, potential reason for the 30s latency might be: The destination is unreachable and it takes a long time to establish a connection.

- Other Potential Latency Factors
  - DPM Latency 
  - Latency when serializing messages in dpm and deserializing messages in ACA
  - Transmission delay in Grpc pipeline
  - ACA (Not in this test)
  - OVS (Not in this test)

- Dependency : DPM final design after L2 and L3 are 
distinguished.
- Action: Turn on debug mode when running the test in DPM, can see what actions take the most time.

**L3 Routing Workflow**
- https://github.com/er1cthe0ne/alcor/blob/security_group/docs/modules/ROOT/images/router_e2e_workflow.png
- Scenario A: Create green subnet P1 on host 1, then red subnet P2 ON host 2, both subnets connected to the same router (so they can communicate, L3 neighbor) 
- Scenario C: VPC only, routing rule added for green subnet, green subnet p1 on host 1, red subnet p2 on host 2     
- Considering adding a southbound resource table, can be on DPM or can have multiple tables to synchronize information.  So we don't need to go to port manager to look for the information when a rule is updated in subnet. Potential solution: subscription (needs to be real time)

**Data Plane Manager and Port Manager Contract**

- https://github.com/futurewei-cloud/alcor/pull/364
- Contract looks good overall, will Update neighbor entry to neighbor relationship. Will make change and update PR 364. 

**Message Queue Design Discussion**

- https://github.com/futurewei-cloud/alcor/issues/369
- Will work to verify the solution of grouping by host first

**DHCP**
- Fixed an issue, so DHCP server can reply to the first DHCP request message. Found another issue, currently working on it. 

**USTC**
- Chenmin: Working on performance testing on MQ in local environment, next step will integrate Pulsar into DPM. 
- Luyao: Working on the agent side, environment is ready. Will start development work soon. (POC: Eric and Piaoping)


