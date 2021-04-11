## Alcor Control Plane Southbound Configuration Proposal 04/22/2020

    MIT License
    Copyright(c) 2020 Futurewei Cloud

    Permission is hereby granted,
    free of charge, to any person obtaining a copy of this software and associated documentation files(the "Software"), to deal in the Software without restriction,
    including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and / or sell copies of the Software, and to permit persons
    to whom the Software is furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
    WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Video Recording: https://www.youtube.com/watch?v=bbmkhBWWg8U&feature=youtu.be

1. Control plane southbound configuration Proposal 控制平面南向配置下发
    1.  Partition by VPC: Deploy multiple sets of VPC service controller instances, use the LBMRC algorithm designed in 3.2 to map the VPC to a specified instance, and the instance is responsible for all the configuration of the VPC. 
        - 部署多套 VPC service 控制器实例，使用 3.2 设计的 LBMRC 算法将 VPC 映射到指定的一个实例内，该实例负责该 VPC 的全部配置下发
    2.  The control plane is separated from north to south, and the south is composed of multiple south-facing modules. Each infrastructure pod and messaging pod as a southbound module, each southbound module maps a part of the computing nodes, and enters the upper NCA of these computing nodes. (kafka binding) 
        - 控制平面南北向分开，南向由多个南向模块构成，每个 infrastructure pod 以及 messaging pod 作为一个南向模块，每个南向模块映射一部分计算节点，与这些计算节点的上 NCA 进行连(kafka 绑定).

2. Pain points
    1. Southbound - For example, there are 100 nodes in a group, the group needs to receive all the messages from the 100 nodes when many times the messages from the 99 nodes are not needed.
    2. Northbound - With 100  topics, the VPC is very huge. Issue raises when the same message is sent to all 100 topics creating 100 connections. This will be an problem when we scale out.
    3. Host
        - Single Kafka cluster connection limit
        - Single redis cluster connection limit
        - Redis VPC and host mapping table split
        - Controller needs to send a single message to multiple Kafka clusters and multiple topics
3. Infrastructure services scale-out
    1. Infrastructure Services
        - Decoupled from Management Services
        - Could be reused by multiple types of management services
        - Partitioned by physical topology of data center (AZ, DC, cluster)
        - Topics
            - MQ deployment (per region, per AZ, per DC?)
            - MQ topic grouping
            - MQ partitioning
4. Focus
    1. Focus on the southbound issues/tasks
    2. Topics grouping and partitioning
        - Avoid pulling unnecessary information
    3. Southbound normal case
    4. Research
        - Message queue
        - Alternate solution for Kafka
        - ReplicaSet


