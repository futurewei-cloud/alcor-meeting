# Alcor Open Source Community Meeting 8/12/2020 

Meeting Recroding: https://youtu.be/lCA5AW37si8

## Status Update

1. Current Release Status Overview
1. DHCP Implementation (Eric, Wunan)
1. Security Group
    * Pain points: security model and policy
        * For example, there is a policy which allows security group B to be able to access security group A. When a change is made in security group B,  security group A also needs to be aware of the change. So when a change is made, specification needs to be reassembled, and full goal state needs to be sent down. 
    * Will work on a security design and implementation on the  Alcor Controller Agent side 
1. Planning for the Second Half of 2020
	* Southbound Communication Performance Test
		* Simulate 10,000 computing nodes and created the connection on Pulsar, see how much workloads and requests Pulsar can handle. 
	* Southbound Communication Test Cases/Scenarios Reports (Yuanwei) 
        * Scalability  -  bottlenecks are mostly on the southbound, how to support large scale distribution
        * Functionality - whether Alcor functionalities can support a very large scale VPC/servers
    * USTC Collaboration - needs a detail plan for southbound communication
		* Complete the model (gRPC as fast path, MQ as scale path, will set the boundary between fast path and scale path according to the actual data.) 
		* Large Scale - 1 VPC/100 VMs
		* For asynchronous calls, need to ensure that the southbound distribution can maintain order
5. Action Items
    * DHCP Implementation (Wunan, Eric) 
    * Security Group Design and Implementation (Eric) 
    * Large Scale Performance Test Case for Alcor (Yuanwei)
    * Southbound Communication Design (Liguang, Yuanwei)
    * When an API call comes, needs to set up tenant ID for verification (Jianwei)
		
			
			
