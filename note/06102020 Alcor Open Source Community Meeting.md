## 06/10/2020 Alcor Open Source Community Meeting
 
### Status Update

Meeting Recording: https://youtu.be/f3rTRiqSAGM

1. Announcement

     1. GitHub Code Coverage is now enabled for Alcor
     1. Average - 40% coverage
     1. Highest - Port manager 70% coverage 

2. Alcor Status
     1. Port Manager
        1. VPC ID is corresponds to all pod id, and will get host id and host ip based on this
        1. Network configuration
        1. Integration changes
        1. DPM basic scenarios have been tested
        1. Port manager and DPM integration
    
     1. Piaoping
        1. Binary object
            1. Share doc for both options
            1. Implement with first version and test it out.
        1. Problem with Ignite when integrating 7-8 microservices
            1. Update ignite version

     1. Security Group Manager
        1. Most functions complete, some improvement to address, will revisit all the comments

     1. Proposal for Alcor Integration with Nova
        1. doc is almost ready for merge

     1. Elastic IP manager
        1. Finalizing doc, need to make some changes and update the architecture
        1. In IP allocation corresponding doc, v6 is independent, v4 will split the range into small ranges

3. USTC Collaboration
     1. Submitted test script PR for Pulsar, will do the same for RocketMQ and submit PR, new machines will be available for testing
     1. Scenario for testing:
         1. In a large vpc scenario, there are multiple TOPICS, as the topic increases, the performance parameters obtained and the attenuation index
         1. Will finalize the test plan proposal and share
 