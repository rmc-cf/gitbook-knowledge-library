# 大数据

1. **存储：主要包括HDFS、Kafka**\
   HDFS是Hadoop提供的分布式存储框架，它可以用来存储海量数据
2. **计算：主要包括MapReduce、Spark、Flink**\
   MapReduce是Hadoop提供的分布式计算框架，它可以用来统计和分析HDFS上的海量数据
3. **联机查询OLAP：包括kylin、impala等**
4. **随机查询NoSQL：包括Hbase、Cassandra等**
5. **挖掘、机器学习和深度学习等技术：包括TensorFlow、caffe、mahout**

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

**HDFS**：(<mark style="color:purple;">Hadoop分布式文件系统</mark>)，它可以用来存储海量数据，适合运行在通用硬件上的分布式文件系统(Distributed File System)。HDFS是一个高度容错性的系统，适合部署在廉价的机器上。 HDFS能提供高吞吐量的数据访问，非常适合大规模数据集上的应用，【通常用于处理离线数据的存储】。

**Hbase**: 分布式、面向列的开源数据库，适合于非结构化数据存储。【实时数据和离线数据均支持】。

**Flume**: 高可用/可靠，<mark style="color:purple;">分布式海量日志采集、聚合和传输的系统</mark>，Flume支持在日志系统中定制各类数据发送方，用于收集数据;同时，Flume提供对数据进行简单处理，并写到各种数据接受方(可定制)的能力。

**Kafka**：一种高吞吐量的分布式发布订阅消息系统，它可以处理消费者在网站中的所有动作流数据。

**ZooKeeper**：开放源码的分布式应用程序协调服务，是Hadoop和Hbase的重要组件。它是一个为分布式应用提供一致性服务的软件，提供的功能包括：配置维护、域名服务、分布式同步、组服务等。

### Lambda架构

* <mark style="color:purple;">**批处理层**</mark>(Batch Layer)：两个核心功能，<mark style="color:purple;">存储数据集</mark>和<mark style="color:purple;">生成Batch View</mark>。
* <mark style="color:purple;">**加速层**</mark>(Speed Layer)：<mark style="color:purple;">存储实时视图并处理传入的数据流，以便更新这些视图</mark>。
* **服务层**(Serving Layer)：用于响应用户的查询请求，合并 Batch View 和 Real-time View 中的结果数据集到最终的数据集。
