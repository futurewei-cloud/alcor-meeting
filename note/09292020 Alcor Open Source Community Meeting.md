# Alcor Open Source Community Meeting 9/29/2020

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

Meeting Recording: https://youtu.be/Qrrkmwtjcp0

1. Scalability test framework update
    * JianWei presented the scalability test result based on the current DPM code on GitHub master and a dumb down version Alcor Control Agent written in Java.
    * With a big goal state message, (e.g. one port create plus ton of neighbor info), DPM processing time took longer than expected. XiaoDong already has change to improve DPM, the action item is for him to merge his change to master so that JianWei can use.
2. Southbound scale-out: MQ implementation update
	* PiaoPing will continue to drive this. Liguang has disabled the pulsar producer during port manager code merge due to conflict, therefore PiaoPing should look into reenabling it.
	* Eric provided feedback to the pulsar consumer change in Alcor Control Agent, it is looking good but needed automatic test. LuYao understood the request and will provide test code based on Eric’s suggestion.
3. Security Group host design discussion: https://github.com/er1cthe0ne/alcor/blob/doc%2Fsecurity_group/docs/modules/ROOT/pages/high_level/security_group_host_design.adoc
	* Went through the design doc, PiaoPing needs to spend some time to research and understand the technical approach.
	* There is agreement that security group implementation has a big scaling concern, especially with security group rules linked to remote security group. 
	* The design will focus on improving the scaling issue and do better than neutron today.
4. 11/30 release planning and discussion: https://github.com/futurewei-cloud/alcor-int/wiki/Alcor-v1.0-Release-Plan
	* There are a lot of work for everyone to do, the plan is a little aggressive, everyone will try their best to focus on the important tasks.
	* We may adjust the plan and assignment when needed.  
