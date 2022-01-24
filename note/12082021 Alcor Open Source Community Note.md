# Alcor Open Source Community Meeting 12/08/2021


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

1. USTC Work Report Update
    * VPC-based implementation for Message Queue Scale Path (Min Chen/Luyao Luo)
        * Min: 
			1) Specify the topic subscription by ACA through gRPC. (Completed)
				1) Including adding a new gRPC channel to send topic info, adding topic Info sending logic to achieve the dynamic assignment of topic
			2) Topic into cache design for DPM to reduce number of topicinfo sending requests (Completed)
			3) VM similarity strategy/solution plan - revising IP
			4) Next:
				1) DPM Topic Info Cache implementation
				2) Dynamic topic testing  
				3) VM Similarity strategy/solution plan improved version
		* Luyao
			1) Pulsar related testing
				1) Goal state v1 can be configured through Pulsar, ping was successful. 
				2) Goal state v2 can also be configured successfully but is not able to identify whether it came from v1 or v2. 
					a) Can try to switch everything over from Goal state v1 to goal state v2
				3) Logic for dynamic switching - interface completed, will begin implementation soon 
		* Fangjian
			1) Two bugs have been addressed
			2) Added message channel support for goal state v2 
			3) Tested the message channel to accept messages in unicast mode
			4) Next:
				1) Help Luyao with dynamic subscription testing
	* ML-based on-demand programming (Shuang Liang)
		* Made changes on the model per last meeting's discussion, added request configuration - the configure sequence is based on similar VMs to make predictions on purchase behaviors
		ii. Currently using data to test the feasibility of the model
			
	* Scalability test framework for 1M nodes regions and 100k ports VPC (Jiawei Liu/Hanfeng Zhang)
		* Jiawei: Distrinet demo environment done - Set up the environment for 1 client, 1 master and two worker node. 
			1) Next : will work on the customized configuration of the terminal for distrinet
		* Hanfeng: 
			1) Distrinet's code prepartion for alcor controller replacement, 
			2) double check on the performance impact for large scale testing, 
			3) determine a suitable topology, determine the ratio of switches and switches, switches and terminals in each layer
		* Yangyu
			1) Finish the basic learning of distrinet 
			2) Currently working on an automated script to start up distrinet environment
