## 06/17/2020 Alcor Open Source Community Meeting
 
### Status Update
 
* Jianwei: Support multi-params query
  * Integration with Nova design API is added.
  * Not merged yet, flow up is not there yet.
  * List security groups - list by project ID.
  * Will focus on initial integration with Nova. Will make changes as needed.
 
* Yuanwei: Elastic IP Manager
  * Made updates on the Elastic IP manager and presented
  * Design Review:
    * Step 1:
        * Split into a number (100-500) of buckets according to a fixed algorithm
        * Each bucket carries some available IP addresses in the IPV4 address pool
        * Randomly selects a bucket for each EIP allocation request
        * Add Lock to the bucket
        * And in this bucket, you can choose one of the available IPs to assign to the IP address
    * Step 2:
        * Each bucket should record its own assignable address, so that when an EIP assignment request for this bucket is selected, an available address can be quickly obtained.
    * Step 3:
        * Each bucket should also record itself and the assigned address, so that when the address pool range changes, it can more easily update the address that can be assigned to each bucket.
    * Step 4:
        * Random bucket selection: If the bucket is full, there should be a global entry to record which buckets and no assignable addresses. To maintain which bucket is full, lock and update when the last available address is divided, or update and update according to the available address of each bucket when the address pool is updated.
        * When Assigning EIP: When an EIP is released, the bucket is updated, from full to not full, you also need to lock and refresh. The scenario of not selecting a newly available bucket is acceptable.
    * Step 5:
        * When the address pool is relatively small, these buckets that are not assigned to available addresses can be treated as buckets that do not have assignable addresses.
    * Step 6:
        * feasible algorithm for gating is to obtain the assigned bucket number according to the corresponding integer of each address to 64. The advantage of this algorithm is that when the address pool changes, the assigned address recorded in each bucket does not need to change
 
   * Action Item:
      * Look into hash algorithm as an alternative solution
      *  EIP and VM applications are closely related. Discuss how to apply for an IP address to the entire Alcor extranet. Need a relatively new solution
 
* Piaoping: Network ACL FWAAS
  * Industry Analysis
  * Key Take Away for model selection
    * The smaller the granularity, the better. We want to have it on the pod level.
    * Needs to ensure functionalities are compatible
    * More flexible Model for extension
 
* Wunan: DHCP Design
  * Sync on the design for DHCP and addressed some blocking issues
  * Will continue on implementation.