# Alcor Open Source Community Meeting 11/25/2020

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

1. Alcor and Zeta Integration
    * Zeta Integration Implementation #158 https://github.com/futurewei-cloud/alcor-control-agent/pull/158 
        1. Resolve the "alcor" submodule conflict and get your branch to compile in the CI environment
        2. Address the feedbacks left in this PR
        3. Can we still do remote IP specific outports (current implementation) at the source node and destination node or we have to switch to generic vxlan outport for current non zeta port plus zeta support port? Need to try it with manual rules to confirm.
		4. Current Work: 
            1) The goal is get this change to merge in as long as it doesn't break existing functionality
            2) Ensure all test cases are passing: Test cases: https://github.com/futurewei-cloud/alcor-control-agent/wiki/How-to-run-the-full-suite-of-aca_tests
        5. Incremental Changes/ Next steps:
            1) Think about the operation needed for add/delete group rule, direct path rule, outports. Think about how to manage the lifetime of them. - Suggested to use cache to list port numbers. 
            2) Come up with the efficient data structure to store the needed info, don't want to use two data structure to store similar info. Except for the cache of valid oam udp port for quick check under ACA_OVS_Control::parse_packet
   * Documentation on Zeta+ACA environment setup and test cases  https://github.com/futurewei-cloud/alcor-control-agent/issues/163: Address comment in PR, ensure test cases can covered all designs https://github.com/futurewei-cloud/alcor-control-agent/pull/170

2. Alcor Status Update
    * DHCP enhancement to include GW info: https://github.com/futurewei-cloud/alcor-control-agent/issues/159 -  Feature completed
    * ARP responder for L2/L3 neighbors: https://github.com/futurewei-cloud/alcor-control-agent/issues/117 - 
        * PR raised for current work. Need help looking into the code. Eric will help looking into the code. 
        * Added some unit tests, more testing needed. 
        * Not familiar with socket programming,  Can also try verify the code using TCP dump. (Set up debug session with Jianwei offline)
    * DPM v2.0 implementation follow-up: Cache layer implementation and PM change
        * Currently working on Cache layer implementation and PM change, will try to have all the changes out by the end of this week (Cache layer change first) 
    * Security Group host implementation update (cont'd):  https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
        * May need to reassign work due to current priority
    * Pulsar DPM Client: https://github.com/futurewei-cloud/alcor/pull/481
        * Two more functions to add for Pulsar client and address comments in PR

3. Scalability test framework & Report review: 
	* https://github.com/futurewei-cloud/alcor/issues/439
	* https://github.com/futurewei-cloud/alcor/issues/425 
    * https://github.com/futurewei-cloud/alcor/issues/283

4. Design Discussion 
    * Southbound scale-out: MQ implementation update (cont'd): https://github.com/futurewei-cloud/alcor/issues/404  https://github.com/futurewei-cloud/alcor/issues/405
    * MQ deep dive: https://github.com/VanderChen/open-doc/blob/master/pulsar%20design1119.docx
        * Keyshared mode workflow plan discussion 
            * Option 1: Host IP + Character as msg key
            * Option 2: Host IP as msg key, conflicted host not subscribed
            * Todo: Regroup, determine hash collision probability
    * Multiple writing issue in Control Plane
        * Open Issue:  
            * Forward or direct path
            * Too many zookeeper clusters
            * How to handle on demand rules
        * Todo:
            * Get keyshared working, consider the hash and then to see how to modify source code
    * Alcor Support various dp: https://github.com/futurewei-cloud/alcor/issues/478

    