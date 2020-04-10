# 集群横向扩展技术需求与设计方案整体方案
 
Meeting Recording:https://www.youtube.com/playlist?list=PL_7gYB_Le9d0y4WTuWcH7tQGrVmESC2X_
 
## 整体方案：多个控制器实例是以active-active mode 的微服务的形式遍布于多个az中，从而达到伸缩性强以及高可用性特点。

可能存在的问题：

* 各vpc一次性提交大量配置请求的保序要求无法满足
  * 需要重新考虑是否有大量的VPC请求的实际场景
      * vpc本身改动很少，创VPC也很少，子网也比较少，包括安全组
* 控制平面API gateway 的北向请求分发
  * 同样需要考虑需求是否存在, 如果要做全局的排序， 对scalability的影响太大了。
  * 如果有实际的场景需求，可以考虑atomic clock，也可以参考其他的保序方法。（例如说：直接查resource的status；后续依赖对象 (EP 微服务)看子网状态存不存在，是否可以往下走。
* 南向处理
  * 需要考虑的问题：分区是以什么力度来建的，比如说节点，partition，等。 要有一个折中的方案。如果是kakfa的话。 以NCA为力度划分区，计算节点太多区，是否能够撑住。
* 动态调度优化 （没有深入讨论）
 
## Alcor 需求以及痛点
 
### 需求
* Gateway manager
* Message port (kafka)
* Alcor data Model
* Alcor event ordering handling
 
### 痛点
* LBLM - locality based mapping的细化来考虑VPC控制器的实时健康数据
  * mapping的数量
  * VPC的个数
  * 设计多维度的算法：考虑VPC的quota和VPC是否要发到固定的controller 实例等场景。
* 监控系统
  * 拿到数据后，再来判断具体设计
  * 调研普罗米修斯，node的监控。API gateway分发的算法细化，深化。（算法 partition manager这一层）
* 微服务开发
  * VPC manager, 把database换到ignite,
  * root manager, subnet manager 和mac manager。