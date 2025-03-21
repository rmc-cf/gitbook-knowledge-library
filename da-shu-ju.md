# 大数据

1. **数据存储层：主要包括**<mark style="color:blue;">**HDFS、Kafka**</mark>\
   HDFS是Hadoop提供的分布式存储框架，它可以用来存储海量数据
2. **数据计算层：主要包括**<mark style="color:blue;">**MapReduce、Spark、Flink**</mark>\
   MapReduce是Hadoop提供的分布式计算框架，它可以用来统计和分析HDFS上的海量数据
3. **联机查询OLAP：包括kylin、impala等**
4. **随机查询NoSQL：包括Hbase、Cassandra等**
5. **挖掘、机器学习和深度学习等技术：包括TensorFlow、caffe、mahout**

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**HDFS**：(<mark style="color:purple;">Hadoop分布式文件系统</mark>)，它可以用来<mark style="color:purple;">存储海量数据</mark>，适合运行在通用硬件上的分布式文件系统(Distributed File System)。HDFS是一个<mark style="color:purple;">高度容错性</mark>的系统，适合<mark style="color:purple;">部署在廉价的机器</mark>上。 HDFS能<mark style="color:purple;">提供高吞吐量的数据访问，非常适合大规模数据集上的应用</mark>，【通常用于处理<mark style="color:purple;">离线数据的存储</mark>】。

**Hbase**: <mark style="color:purple;">分布式、面向列</mark>的开源数据库，适合于<mark style="color:purple;">非结构化数据存储</mark>。【<mark style="color:purple;">实时数据和离线数据</mark>均支持】。

**Flume**: 高可用/可靠，<mark style="color:purple;">分布式海量日志采集、聚合和传输的系统</mark>，Flume支持在日志系统中定制各类数据发送方，用于收集数据;同时，Flume提供对数据进行简单处理，并写到各种数据接受方(可定制)的能力。

**Kafka**：一种<mark style="color:purple;">高吞吐量的分布式发布订阅消息系统</mark>，它可以处理消费者在网站中的所有动作流数据。

**ZooKeeper**：开放源码的分布式应用程序协调服务，是Hadoop和Hbase的重要组件。它是一个为<mark style="color:purple;">分布式应用提供一致性服务</mark>的软件，提供的功能包括：配置维护、域名服务、分布式同步、组服务等。



## Lambda架构（生存、更蠢、象兵）&#x20;

生成存储、存储更新、响应合并

<figure><img src=".gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

* <mark style="color:purple;">**批处理层**</mark>(Batch Layer)：两个核心功能，<mark style="color:purple;">存储数据集</mark>和<mark style="color:purple;">生成Batch View</mark>。
* <mark style="color:purple;">**加速层**</mark>(Speed Layer)：<mark style="color:purple;">存储实时视图并处理传入的数据流，以便更新这些视图</mark>。
* <mark style="color:purple;">**服务层**</mark>(Serving Layer)：用于<mark style="color:purple;">响应用户的查询请求</mark>，<mark style="color:purple;">合并 Batch View 和 Real-time View 中的结果数据集</mark>到最终的数据集。

#### 优缺点

**其优点：**\
 容错性好、查询灵活度高 、易伸缩、易扩展

**其缺点：**\
 全场景覆盖带来的编码开销。 针对具体场景重新离线训练一遍，益处不大。重新部署和迁移成本很高。



## Kappa架构（shiwu树）（实时服务数据）

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

* 输入数据直接由实时层的<mark style="color:purple;">实时数据处理引擎</mark>对源源不断的源数据进行处理;
* 再由服务层的服务后端进一步处理以提供上层的业务查询。
* 而<mark style="color:purple;">中间结果的数据都是需要存储</mark>的，这些数据<mark style="color:purple;">包括历史数据与结果数据</mark>，统一<mark style="color:purple;">存储在存储介质</mark>中。

#### 4.2 优缺点 <a href="#id-42__72" id="id-42__72"></a>

**其优点：**\
 将<mark style="color:purple;">实时和离线</mark>代码<mark style="color:purple;">统一</mark>起来了；<mark style="color:purple;">方便维护</mark>而且<mark style="color:purple;">统一了数据口径</mark>；<mark style="color:purple;">避免</mark>了Lambda架构中<mark style="color:purple;">与离线数据合并的问题</mark>。

**其缺点：**\
 (1)消息中间件<mark style="color:purple;">缓存的数据量和回溯数据</mark>有<mark style="color:purple;">性能瓶颈</mark>。\
 (2)在实时数据处理时，遇到大量不同的实时流进行关联时，非常<mark style="color:purple;">依赖实时计算系统的能力</mark>，很可能因为数据流<mark style="color:purple;">先后顺序问题，导致数据丢失</mark>。\
 (3)Kappa在抛弃了离线数据处理模块的时候，同时<mark style="color:purple;">抛弃了离线计算更加稳定可靠</mark>的特点。

### Lambda架构与Kappa架构对比

| 对比内容     | Lambda架构                                                                                                                       | Kappa架构                                                                                                                                                             |
| -------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 复杂度      | 需要<mark style="color:purple;">维护两套系统</mark>(引擎)，<mark style="color:purple;">复杂度高</mark>                                        | 只需要<mark style="color:purple;">维护一套系统</mark>(引擎)，<mark style="color:purple;">复杂度低</mark>                                                                            |
| 开发、维护成本  | <mark style="color:purple;">开发、维护成本高</mark>                                                                                    | <mark style="color:purple;">开发、维护成本低</mark>                                                                                                                         |
| 计算开销     | 需要一直运行<mark style="color:purple;">批处理和实时计算</mark>，计算开销大                                                                        | <mark style="color:purple;">必要时</mark>进行<mark style="color:purple;">全量计算</mark>，计算开销相对较小                                                                            |
| 实时性      | 满足<mark style="color:purple;">实时</mark>性                                                                                       | 满足<mark style="color:purple;">实时</mark>性                                                                                                                            |
| 历史数据处理能力 | <mark style="color:purple;">批式全量处理</mark>，<mark style="color:purple;">吞吐量大</mark>，历史数据处理能力<mark style="color:purple;">强</mark> | <mark style="color:purple;">流式全量处理</mark>，<mark style="color:purple;">吞吐量相对较低</mark>，历史数据处理相对较<mark style="color:purple;">弱</mark>                                  |
| 使用场景     | 直接支持批处理，更<mark style="color:purple;">适合对历史数据分析查询</mark>的场景，期望<mark style="color:purple;">尽快得到分析结果</mark>，批处理可以更直接高效地满足这些需求。    | <mark style="color:purple;">不是</mark>Lambda的<mark style="color:purple;">替代</mark>架构，而是简化， Kappa放弃了对批处理的支持，更擅长业务本身为增量数据<mark style="color:purple;">写入场景</mark>的分析需求。 |
