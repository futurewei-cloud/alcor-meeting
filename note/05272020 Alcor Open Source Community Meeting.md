## 05/27/2020 Alcor Open Source Community Meeting 

Meeting Recording: https://youtu.be/gu_uaFl7dMQ

1. Quick Update/Sync
    1. Piaoping: Who provides the information for neighbor?
        1. Information is filled in during pod creation.
        1. The subnet / port manager is the DPM client. Whoever picks it up should be the person who created the Pod to receive this information
2.  Root Manager - API
    1. When is vpc routing used?
        1. After the routing table is separated, it is equivalent to that I can associate it with other flow tables. If the routing field is written into the VPC, it can be used as a custom field of the subnet.
3.  Southbound messages distribution Dataset  (Yunwei)
4.  API  - focus on core scenarios
5.  Keystone Integration
    1. PR submitted
    1. Finished 60% of the testing
    1. Cache selection
    1. Action items: environment setup guide