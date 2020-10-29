# Alcor Open Source Community Meeting 10/20/2020

1. Alcor Project Community Update 10/20/2020
    * Alcor Project 
        * Cloud-Native Architecture
            * Alcor Controller Innovation
            * Alcor Agent Innovation
        * Alcor Component Snapshot and Development Status
        * Performance Comparison with OpenStack Neutron
        * Migration Plan from Neutron
        * Open Source Community Involvement
        * Planning for Second Half of 2020
2. Announcement of feature/issue tracking on GitHub
    * Will run Alcor project entirely on GitHub, new issues will be opened and assigned to owners
3. Subnet Level Programming Path https://github.com/futurewei-cloud/alcor/pull/429
    * The current port manager design sends down message base on port level. Currently, we have new use cases to update the routing rule status for the subnet. We will need to add a new programming path for the new use case - design in dicussion. 
4. Current Work Update
    * Scalability test framework update (cont'd): https://github.com/futurewei-cloud/alcor/issues/439 https://github.com/futurewei-cloud/alcor/issues/425 https://github.com/futurewei-cloud/alcor/issues/283
    * Southbound scale-out: MQ implementation update (cont'd): https://github.com/futurewei-cloud/alcor/issues/404  https://github.com/futurewei-cloud/alcor/issues/405
    * Security Group host design discussion and update (cont'd):  https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
    * SG deletion issue update: https://github.com/futurewei-cloud/alcor/issues/413
        * Problem addressed, solution dicussion. 