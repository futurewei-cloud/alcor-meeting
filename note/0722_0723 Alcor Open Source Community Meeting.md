# Alcor Open Source Community Meeting 7/22/2020, 7/23/2020 #

Meeting Recording: 

* 7/22: https://youtu.be/dyLgxtqTGtE
* 7/23: https://youtu.be/N9nnrKACH8s


## 7/22/2020 Weekly Community Meeting ##
 
### Discussion/ Status Update ###
 
**Southbound Workflow of Port Provisioning**

* https://github.com/xieus/alcor/blob/docs/workflow/docs/modules/ROOT/pages/high_level/southbound_workflow.adoc
* DPM- Stateless
* Full increment
* Southbound
  *  Zoning - cross section at PM and DPM
  *  Out of order -  consistent data
 
**RocketMQ and Pulsar Performance Test**
 
* RocketMQ
  * Test Result
    * Setting JVM memory parameters has no effect on the results
    * Use ONEWAY to test the TPS limit of the broker. The data is almost the same as before
    * When the broker is running, the topic is constantly added, and the topic creation speed will slow down, and there will still be problems at 10,000.
  *  Actions Items:
     * Check if bandwidth is full
     * Try to build all the topics first when running broker
     * Broker, when establish a connection, create topics, send messages, and the sender is not disconnected. Do you use a new connection every time or the original connection?
 
* Pulsar
   * Test Result
     * In terms of performance, the topic has increased to 70,000 levels. But there will still be a problem of lookup timeout on the client side. (More than 30,000 MS will report an error)
     * After Broker kill -9 on Bare Metal, there is no automatic reply (the official recommendation is to use K8S and enable liveness probe on brokers). There is no solution for bare metal, and manual restart is required. The manual restart time is the normal start time.
     * After the broker kill -9, there will be an exception that cannot be connected to the client side. Need to set up a pulsar proxy to solve it.  Currently testing, and an error will be reported at the moment.
     * After the broker kill -9 manually restart the broker and client, the data will not be lost. However, when the data is too large, the statistics seem to be abnormal, including the decrease of the number of msg_in, and we are trying to do statistics by maintaining shared variables.
   * Actions
      * Find the bottle neck for TPS to drop significantly around 50,000 -70,000 topics
      * Can Pulsar's bucket be tuned? Change the bucket parameters
* Conclusion
      * Organize the data under a set of specific scenarios for both Pulsar and RocketMQ. There are several dimensions. We will look TPS change and curve change, and make the decision.
        * Topics increase
        * Sending frequency
        * Subscribe frequency
 
**DCHP**

* Design alignment https://github.com/futurewei-cloud/alcor-control-agent/blob/f265d4534921c9eb8b0516acbe9bdc82b21e27b3/docs/Understanding_DHCP.pdf
 
**Port Manager (Piaoping)**

* The port manager code is up. Measured the performance, on the privateIP side, when the range is divided into many IPs, the allocation is stored in the range.
* Working on Refactoring
* Will test in K8S
* Run ignite E2E test for connections and stability
* Will integrate with Mac manager and test together
 
**Mac Manager (Jianwei)**

* Tested with ignite, 3 pods cluster.  OPS can reach 200,000 per second. (Read and Write)
* Get the data for the impact of each micro service on database for both read and write, then do comparison
* Mac addresses does not allow conflict, 16M is not enough
 
**Security Group**

* Next focus for E2E integration
* Requirements -need this from API gateway to DPM
 
**EIP**

* Merged new PR. Almost complete. Will submit a new PR including API gateway change.
* Can be integrated with OpenStack
 
 
## 7/23/2020 Debug Session ##
 
**Items**

* Issue with API Authorization
* Security Group (Support for Hidden API to address the issue with binding security group)
* Port Manager (Logs - client, create port debug log)
* Mac Manager  - Create 65000 in batches at once to test for throughput and Latency
 
 
 
 
 
 
 
 
 