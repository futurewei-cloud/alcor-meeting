# Alcor Open Source Community Meeting 08/31/2022


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

## Meeting Notes

### Distrinet
* Explore the extensibility of Distrinet based on Neutron 
   * Work update
        * Change the default driver in OpenStack from KVM to fake driver, and started successfully
        * Following the last meeting's discussion, fake driver started the VM for namespace rewrite, and passed the verification on the physical host. 
        * Utilized compute node for container creation - completed, and passed the verification (host network mode and non-host network mode)
        * Paper research
            * Phantom - Co-opting Linux Processes for High Performance Network Simulation
            * CrystalNet: Faithfully Emulating Large Production Networks 
    * Demo for (item 1-3) 
    * Next Step: End to end demo ready by 9/14, have testing data ready for report 
### ML for Network
* Work Update
    * After completing data processing last week, have been testing data this week. 
    * Next: focus on data processing to compare the difference between actual data and the data collected from the model 