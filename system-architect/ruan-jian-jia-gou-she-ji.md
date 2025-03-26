# 软件架构设计

软件架构风格是特定应用领域的**惯用模式**，架构定义一个**词汇表和一组约束**



## 软件架构风格

性能 安全性 可修改性 可用性



| 数据流风格   | 批处理、管道-过滤器        |
| ------- | ----------------- |
| 调用/返回风格 | 主程序/子程序、面向对象、层次结构 |
| 独立构件风格  | 进程通信、事件驱动系统(隐式调用) |
| 虚拟机风格   | 解释器、规则系统          |
| 仓库风格    | 数据库系统、黑板系统、超文本系统  |

### 数据流风格

**优点**

1、松耦合【高内聚-低耦合】; 2、良好的重用性/可维护性; 3、可扩展性【标准接口适配】; 4、良好的隐蔽性; 5、支持并行。

**缺点**

1、交互性较差; 2、复杂性较高; 3、性能较差(每个过滤器都需要解析与合成数据)；

**典型实例**

传统编译器、网络报文处理

### **调用/返回风格**

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

。。。。。。。。等等

仓库分为数据库系统和黑板系统

数据库系统：以<mark style="color:purple;">数据</mark>为中心

黑板系统：<mark style="color:purple;">可更改性和可重用性</mark>、可<mark style="color:purple;">重用的知识源</mark>，容错性和健壮性，使用中心数据触发内部逻辑部件

缺点：测试困难;<mark style="color:purple;">不能</mark>保证<mark style="color:purple;">有好的解决方案</mark>;<mark style="color:purple;">难以建立</mark>好的<mark style="color:purple;">控制策略，低效，开发困难</mark>;<mark style="color:purple;">缺少并行</mark>机制

**闭环控制架构(过程控制)**：<mark style="color:purple;">解决简单闭环控制问题</mark>

简单案例：<mark style="color:purple;">空调温控、定速巡航</mark>

### **C2风格**

C2架构的基本规则:\
构件和连接件都有<mark style="color:purple;">一个顶部和一个底部</mark>。\
构件的<mark style="color:purple;">顶部</mark>要连接到<mark style="color:purple;">连接件的底部</mark>，构件的<mark style="color:purple;">底部</mark>要连接到<mark style="color:purple;">连接件的顶部</mark>，构件之间<mark style="color:purple;">不允许直连</mark>。\
一个连接件可以和<mark style="color:purple;">任意数目的其他构件和连接件</mark>连接。当两个连接件进行直接连接时，必须由<mark style="color:purple;">其中一个的底部到另一个的顶部</mark>

### 层次架构风格

构件组成一个层次结构，连接件通过<mark style="color:purple;">决定层间如何交互的协议</mark>来定义。每层<mark style="color:purple;">为上一层提供服务</mark>，<mark style="color:purple;">使用下一层的服务</mark>，<mark style="color:purple;">只能见到</mark>与自已<mark style="color:purple;">邻接的层</mark>。通过层次结构，可以将大的问题分解为若干个渐进的小问题逐步解决，可以隐藏问题的复杂度。修改某一层，最多影响其相邻的两层（通常只能影响上层）。

层次结构优点：

1. 支持基<mark style="color:purple;">于可增加抽象层</mark>的设计，允许将一个复杂问题<mark style="color:purple;">分解成一个增量步骤序列</mark>的实现。
2. 不同的层次处于不同的抽象级别，越靠近底层，抽象级别越高；越靠近顶层，抽象级别越低。
3. 由于每一层<mark style="color:purple;">最多只影响两层</mark>，同时只要给相邻层提供相同的接口，允许每层用不同的方法实现，同样为软件复用提供了强大的支持。

缺点：

1. 并<mark style="color:purple;">不是</mark>每个系统都可以很<mark style="color:purple;">容易的划分为分层</mark>的模式。
2. <mark style="color:purple;">很难找到</mark>一个<mark style="color:purple;">合适的、正确的</mark>层次抽象方法。



### 虚拟机体系结构风格

基本思想：人为构建一个运行环境，环境上解析运行自定义一些语言

* 解释器体系风格

例子：专家系统

* 规则系统体系风格（规则集、规则解释器、规则/数据选择器及工作内存）

### 独立构件体系风格

* 进程通信体系风格
* 事件系统体系风格

## 软件架构复用

原因：减少开发工作、减少开发时间以及降低开发成本，提高产品质量具有更好的互操作性，维护更加简单

* 机会复用：发现有可复用的资产，就对其进行复用
* 系统复用：开发之前，进行规划，决定哪些需要复用

### 复用基本过程

（1）构造/获取可复用的软件资产

（2）管理资产

（3）使用可复用资产

### 特定领域软件体系结构DSSA

（1）垂直域：定义一个特定的系统族，内的多个系统，中可作为系统的可行解决方案的一个通用软件体系结构

（2）水平域：定义了多个系统和多个系统族功能区域中的共有部分，在子系统级上涵盖多个系统族的特定部分功能。

在垂直域定义的DSSA只能应用于一个成熟的、稳定的领域，但这个条件难满足，若将领域分割成较小的范围，则相对更容易。

### 基本活动

* 领域分析：获得领域模型
* 领域设计：获得DSSA。形成重用基础设施的规约
* 领域实现：依据领域模型和DSSA开发和组织可重用信息。反复地、逐步求精

参与人员：领域专家、领域分析人员、领域设计人员和领域实现人员

### DSSA建立过程

并发、递归、反复

* 一组需要回答的问题
* 一组需要的输入
* 一组将产生的输出和验证标准

（1）定义领域范围（2）定义领域特定元素（3）定义领域特定设计和实现需求约束（4）定义领域模型和体系结构（5）产生、搜集可重用的产品单元

| 架构风格名称 | 数据处理方式                   | 系统拓展方式                   | 处理性能                                                              |
| ------ | ------------------------ | ------------------------ | ----------------------------------------------------------------- |
| 仓库     | 数据存储在中心仓库，处理流程独立，支持交互式处理 | 数据与处理解耦合，可动态添加和删除处理组件    | <p>劣势：数据与处理分离，需要加载数据，性能降低</p><p>优势：数据处理组件之间一般无依赖关系，可并发调用，提高性能</p> |
| 管道过滤器  | 数据驱动机制，处理流程事先确定，交互性差     | 数据与处理紧密关联，调整处理流程需要系统重新启动 | <p>劣势:需要数据格式转换，性能降低<br>优势:支持过滤器并发调用，性能提高</p>                      |



管道-过滤器：\
<mark style="color:purple;">交互方式</mark>：顺序交互（前一个构件的输出作为后一个构件的输入）\
<mark style="color:purple;">数据结构</mark>：基于数据流结构 构件之间传递数据结构可能是结构体等常规数据结构\
<mark style="color:purple;">控制结构</mark>：数据流顺序传递\
<mark style="color:purple;">扩展方法</mark>：顺序结构，通过接口适配扩展

数据仓库：\
<mark style="color:purple;">交互方式</mark>：星型交互（构件和一个共享数据库进行数据）\
<mark style="color:purple;">数据结构</mark>：基于数据库结构的 构件之间传递数据是基于关系数据库\
<mark style="color:purple;">控制结构</mark>：面向应用，由业务功能驱动\
<mark style="color:purple;">扩展方法</mark>：直接通过数据库内增加数据 通过模型适配 更加灵活

数据仓库风格更加灵活\
数据仓库风格更加使用

* 虚拟机风格
  * 解释器风格
    * 提供灵活的解析引擎 适用复杂流程的处理
    * 满足数据协议兼容性需求 具有良好的灵活性
    *
*   独立构件风格

    * 进程通讯风格
    * 隐式调用风格
      * 简化构件间的交互复杂度 降低系统耦合度
      * （采用开源消息中间件作为连接构件 有效解决耦合问题 迭代过程效率高 有效解决耦合问题）
      * 基于消息中间件 能够让系统的构件化思路 得到良好实施 带来了非常清晰的数据流转结构 简化了编码难度 降低本项目二次开发的难度

    通过消息订阅 和 发布控制系统间信息交互 降低系统耦合度 提高系统的可修改性
* B/S架构风格（基于浏览器和服务器的架构）
  * 使用http协议进行通信交互 降低了系统推广和维护
  * 使用了大量的前端缓存技术和websocket技术 满足用户实时性需求 用户体验好 及时生效

采用服务器冗余和心跳检测策略 增加可用性

Lambda\
<mark style="color:purple;">批处理层</mark>\
核心功能：<mark style="color:purple;">存储数据集 和 生成BatchView</mark>\
<mark style="color:purple;">加速层</mark>\
<mark style="color:purple;">存储实时视图并处理传入的数据流 以便更新这些视图</mark>\
<mark style="color:purple;">服务层</mark>\
用于<mark style="color:purple;">响应用户的查询请求</mark> 合并batch view 和 real-time view中的结果数据集到最终数据集

Lambda架构优缺点\
优点：\
<mark style="color:blue;">容错性好</mark>\ <mark style="color:blue;">查询灵活度高</mark>\ <mark style="color:blue;">易伸缩</mark>\ <mark style="color:blue;">易扩展</mark>

缺点：\
<mark style="color:blue;">全场景覆盖带来的编码开销</mark>\ <mark style="color:blue;">针对具体场景重新离线训练收益不大</mark>\ <mark style="color:blue;">重新部署和迁移成本高</mark>

大数据工作面临的五个挑战：\
<mark style="color:blue;">1 数据获取问题</mark>\ <mark style="color:blue;">2 数据结构问题</mark>\ <mark style="color:blue;">3 数据集成问题</mark>\ <mark style="color:blue;">4 数据分析 组织 抽取 建模是大数据本质的功能性挑战</mark>\ <mark style="color:blue;">5 如何呈现数据分析的结果 与并非技术的领域专家进行交互</mark>

大数据分析步骤\
<mark style="color:blue;">1 数据获取/记录</mark>\ <mark style="color:blue;">2 信息抽取/清晰/注记</mark>\ <mark style="color:blue;">3 数据集成/聚集/表现</mark>\ <mark style="color:blue;">4 数据分析/建模</mark>\ <mark style="color:blue;">5 数据解释</mark>
