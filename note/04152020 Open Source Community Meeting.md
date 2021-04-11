## Alcor System Monitoring Research/Alcor控制平面的监控系统
 
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

### 设计Alcor控制平面的监控系统
1. Net Data: 在控制平面的所有主机建立host Netdata 服务，收集各docker上tenant netdata的监控数据，并由management plane的prometheus server定期从host Netdata 上主动拉去
2. Push Gateway: 为每个控制器实例建立一个push gateway, 各位服务上的tenant netdata将监控数据push到gateway上，并由management plane 的prometheus server 定期从host Netdata 上主动拉取。
3. Prometheus server: 直到 Istio 1.4为止， Istio的服务级别直播都是由称为mixer的中央组件提供的。 Prometheus server 从mixer telemetry 获取 service level metrics, 从proxy直接获取Proxy level lmetrics.
 
### 算法
1. 基于局部的最大剩余能力调度（Locality-based Max residual Capacity)
    * 假设VPC server是多套的， 一个VPC的所有请求都map到多个控制器实例的一个。以VPC力度进行分配，每个实例管控下面的具体节点，只是管控这个VPC关联的计算节点。以VPC为力度的映射。
    * 入口分发摸摸看需要维护各控制器实例映射的VPC。
    * 映射的VPC超载了，我们就用这个算法调到其他的实例。
    * 新来的实例调到负载较轻的实例。
1. 最大剩余能力调度 (Max Residual Capacity)
    * 每个实例的处理能力不一样， 考虑到剩余的能力调度做动态带哦东，通过控制器当前负载来估计控制器的情况。
1. 控制器实例剩余能力计算方法
    * 控制器由多个docker下的微服务构成， 根据各个docker的资源使用量数据（cpu, 内存使用）表征该微服务实例的当前资源使用量。剩余能力=资源最大配额-资源使用量/单位请求瓶颈资源使用量
    * 根据调用的平凡程度来设置一个权重，（使用越频繁权重越高）， 这个值作为该看那个之前实例的剩余能力
 
### 问题
1. 能力多个实例，算法来调度，对于某个VPC，哪个调度比较优化和均衡。一套实例每套微服务都能横向拓展，如果是加一套微服务有什么优势?
    * 多套：第一套已经是负载不够才由第二套，这样没有必要去调度，后来都在第二套。这里是没有调度，因为第一套满了，去第二套。不存在一个调度的问题。
    * 把租户的VPC映射到第一个实例，就很难改，不光是调度问题，还需要迁移数据到第二个实例才能调度。（migration问题, 不仅仅是调度的问题)。 
 
## Alcor Community Update
* 4/15 community update: 0.3 release
* 4/30 Planning L2 Networking
* 5/30 Planning L3 Networking and Security
* Slack Channel