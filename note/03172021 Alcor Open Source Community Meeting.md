# Alcor Open Source Community Meeting 03/17/2021

1. MQ design (Xuwei): https://github.com/issacyxw/alcor/blob/master/docs/modules/ROOT/pages/mq_services/message_queue_system.adoc
    * Tasks assigned
        * Luyao: Working on ACA subscribes and receives messages, function calls 
        * Chenmin: Pulsar related interfaces and functions
            * Focus on DPM cache, assume information is provided in the cache, make decision bases on the number of ports, and work on the algorithm. 
        * Jiawei: will pick up on the implementation soon
2. On-demand workflow demo 
    * Demo setup: 1 NCM instance, 1 test controller to simulates DPM, 2 ACA host, each will run a pod, (host 1, pod 1, host 2 pod 2)
    * Flow: When traffic management sends message to NCM, Host 1 will not know about pod 2 in host 2. Communication will be on demand, ACA will not receive all messages. 