# Alcor Open Source Community Meeting 7/8/2020 #
 
Meeting Recording: https://youtu.be/CZhIScJI3B4
 
## Status Update
 
### Performance Test
* RocketMQ performance is looking better than Pulsar.
* Pulsar Bottleneck (Memory Bottleneck)
  * Problem: After default parameter of 4G is updated to 16G, we ran into errors, the test will fail.
  * Next steps:
     * Check the reboot time of broker zookeeper after the test fails.
     * IO Usage, Network Usage
     * Confirm whether the client side memory is full

### DHCP
* Updated PR (comment addressed) 
* Dependency is almost ready to be merged. (Packet in and packet out using open flow rules)
 
### Integration Test
 
* DPM PR is merged.
* Kubernetes YAML file is completed.
* Will work on the final verification to check for any potential issues.
 
### Mac Manager
* Issues for dicussions
  * The default range of 16 million is using 2T of cache, takes about 200-300 ms for updates
  * Every time a MAC is generated, 20 new MACs will be generated, and the MAC pool will be updated every time. 4000-5000 ms
  * Port size will be reduced only after the third time. When MAC is allocated, it is taken out from MAC pool,  but mac is not removed from the pool.
  * Inquiries and updates should be locked to avoid conflicts.
* Next steps
  * Include concurrency data in the PR to better analysis latency distribution.
 
## Future Direction
 
* Southbound Distribution
* Verification and Performance Testing