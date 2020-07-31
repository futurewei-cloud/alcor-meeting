# Alcor Open Source Community Meeting 7/29/2020#

Meeting Recording: https://youtu.be/Id5nwcvEyzE

### Bug/Blocking issues
 
* Service Token (Solution ready) - https://github.com/futurewei-cloud/alcor/issues/332
* Service log, port delete and create issue
* Refactoring port manager
  * Problem of ignite deadlock, appeared in the K8S environment
     * Did not set up timeout limit for read, which caused the blockage. 
 
 
### Status/PR Update
* Elastic IP Openstack Integration
   * Had the PR out
   * Next step is E2E test
* Mac Manager Selector (Will merge next week)
  
    * One more item left: batch performance testing
  
* Network ACL Manager (Not priority, will start next week)

* DHCP
  * Almost ready for E2E
  * More discussion on unit test on Slack Channel.
 
### Items in Planning
* Southbound Distribution
* MQ
* Agent