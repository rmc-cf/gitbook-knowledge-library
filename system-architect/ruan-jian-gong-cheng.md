# 软件工程

### 软件危机

软件危机具体表现为：（进成功质维文）

* <mark style="color:purple;">进度</mark>难预测
* <mark style="color:purple;">成本</mark>难控制
* <mark style="color:purple;">功能</mark>难满足
* <mark style="color:purple;">质量</mark>难保证
* <mark style="color:purple;">软件</mark>难维护
* <mark style="color:purple;">文档</mark>资料缺

### 软件工程定义

* IEEE

将<mark style="color:purple;">系统化、严格约束的、可量化</mark>的方法应用于软件开发、运行和维护

* Fritz Bauer

<mark style="color:purple;">建立并使用完善的工程化原则</mark> 以较经济的手段在实际机器上有效运行的可靠软件的一系列方法



## 软件过程模型

### 瀑布模型

特点：因果关系紧密项链 进行审查和确认 有利于人员的组织管理 有利于软件开发方法和工具的研究

缺点：

（1）软件需求<mark style="color:purple;">完整性、正确性难确定</mark>

（2）<mark style="color:purple;">严格串行化</mark>模型 需要相当<mark style="color:purple;">长时间才能获取</mark>看得见系统 ，<mark style="color:purple;">需求变更将会带来巨大损失</mark>

（3）基本原则是每个阶段<mark style="color:purple;">一次性完全解决该阶段</mark>工作，实际上是<mark style="color:purple;">不现实</mark>

### 原型化模型（快速原型）

两个阶段：

* 原型开发阶段
* 目标软件开发阶段

原型作用不同：

* 抛弃型原型 （需求确认手段）
* 演化性原型

### 螺旋模型

在快速原型基础上扩展

每个阶段分为四部分：

（1）目标设定

（2）风险分析

（3）开发和有效性验证

（4）评审

特点：支持<mark style="color:purple;">大型软件开发</mark> 适用于面向规格说明、面向过程和面向对象的软件开发方法，也适用于几种开发方法组合

### 敏捷模型

* <mark style="color:purple;">适应</mark>性的 而非预设性
* <mark style="color:purple;">面向人</mark>的 而非面向过程的
* 强调开发中相关人员之间的信息交流，提倡面对面交流，面对面交流低于文档成本。
* 按照高内聚、低耦合的原则将项目分成小组

敏捷方法核心思想：

（1）适应型

（2）以人为本

（3）迭代增量式的开发（原型开发思想为基础）

主要敏捷方法：

（1）极限编程 XP

基础、价值观：<mark style="color:purple;">交流、朴素、反馈和勇气</mark>

（2）水晶序列方法 （以<mark style="color:purple;">人</mark>为中心）

（3）Scrum 侧重<mark style="color:purple;">项目管理</mark> （有效率开发软件）

（4）FDD（特征驱动开发方法）（三要素：<mark style="color:purple;">人、过程和技术</mark>）

关键项目角色：<mark style="color:purple;">项目经理、首席架构设计师、开发经理、主程序员、程序员和领域专家</mark>。

过程：开发整体对象模型、构造特征列表、计划特征开发、特征设计、特征构建

### 统一过程模型 RUP&#x20;

* 重量级过程 二维的软件开发模型
* 9个核心工作流：

（1）业务建模（2）需求（3）分析与设计（4）实现（5）测试（6）部署（7）配置与变更管理（8）项目管理（9）环境

一个循环4阶段：（交出细狗）

* <mark style="color:purple;">初始</mark>阶段：定义最终产品视图和业务模型 确定系统范围
* <mark style="color:purple;">细化</mark>阶段：设计确定系统体系结构 指定工作计划和资源要求
* <mark style="color:purple;">构造</mark>阶段：构造产品并继续演进需求直至提交
* <mark style="color:purple;">移交</mark>阶段：产品提交用户

### （角色 活动 制品 工作流）

特点：用例驱动、体系结构为中心（多方面）、迭代和增量

### 软件能力成熟度模型CMMI

用于指导软件开发过程的改进和进行软件开发能力的评估

<mark style="color:purple;">5个成熟度等级</mark>：

（1）L1初始级

<mark style="color:purple;">过程随意且混乱</mark> 成功<mark style="color:purple;">依赖组织人员能力与英雄主义</mark> 经常<mark style="color:purple;">超出预算和成本</mark>

（2）L2已管理级

确保<mark style="color:purple;">策划、文档化、执行、监督</mark>和控制项目级的过程

（3）L3已定义级

能根据自身<mark style="color:purple;">定义标准流程</mark>，并且制度化，同时企业开始进行<mark style="color:purple;">项目积累</mark>，企业<mark style="color:purple;">资产的收集</mark>

（4）L4量化管理级（与L3区别是性能的可预测）

建立了产品质量、服务质量以及<mark style="color:purple;">过程性能的定量目标</mark>

（5）L5优化级

关注于通过<mark style="color:purple;">增量式与创新式</mark>过程与技术改进，不断<mark style="color:purple;">改进过程性能</mark>，能对<mark style="color:purple;">组织级绩效</mark>进行关注

## 软件需求

### 业务需求

* 组织机构或客户对系统、产品高层次的目标要求

### 用户需求

* 用户使用产品必须要完成的任务
* 用户对软件产品的期望

两者构成额用户原始需求文档的内容

### 功能需求

* 开发人员必须实现的软件功能

## 需求工程活动

（1）需求<mark style="color:purple;">获取</mark>

（2）需求<mark style="color:purple;">分析</mark>

（3）<mark style="color:purple;">形成</mark>需求规格（需求<mark style="color:purple;">文档化</mark>）

（4）需求<mark style="color:purple;">确认与验证</mark>

（5）需求<mark style="color:purple;">管理</mark>

## 需求获取

用户、开发者之间为了<mark style="color:purple;">定义新系统</mark>而进行的交流。

<mark style="color:purple;">需求获取</mark>是获得系统<mark style="color:purple;">必要的特征</mark>，是获得<mark style="color:purple;">用户能接受</mark>、<mark style="color:purple;">系统必须满足</mark>的约束。

常见方法：用户<mark style="color:purple;">面谈</mark>、需求<mark style="color:purple;">专题讨论会</mark>、问卷调查、现场观察、原型化方法、<mark style="color:purple;">头脑风暴</mark>法

* 软件需求文档应该精确描述要交付的产品 这是一个基本原则，严格控制软件项目

## 需求追踪

（1）正向跟踪

检查<mark style="color:purple;">《产品需求规格说明书》</mark>中的每个需求是否能在<mark style="color:purple;">后继工作成果中找到对应点</mark>

（2）逆向跟踪

检查设计文档、代码、测试用例等<mark style="color:purple;">工作成果</mark>是否都能<mark style="color:purple;">在《产品需求规格说明书》找到出处</mark>

* 正向跟踪和逆向跟踪合称为“双向跟踪”
* <mark style="color:purple;">需求跟踪矩阵</mark>保存<mark style="color:purple;">了需求与后继工作成果</mark>的对应关系
* 使用<mark style="color:purple;">配置管理工具</mark>实现<mark style="color:purple;">需求跟踪</mark>

### 结构化方法SASD

<mark style="color:purple;">面向功能</mark>的软件开发方法或<mark style="color:purple;">面向数据流</mark>的软件开发方法

结构化开发方法提出了一组<mark style="color:purple;">提高软件结构合理性</mark>的准则

针对软件生存周期各个不同阶段有（1）结构化分析SA（2）结构化设计（SD）（3）结构化编程（SP）



### 数据流图DFD

也称为<mark style="color:purple;">过程建模</mark>和<mark style="color:purple;">功能建模</mark>方法

核心是<mark style="color:purple;">数据流</mark>

以图形方式刻画和表示一个具体业务中<mark style="color:purple;">数据处理过程</mark>和<mark style="color:purple;">数据流</mark>&#x20;

由4中基本元素组成：数据流、处理/加工、数据存储和外部项

* 数据流：用一个<mark style="color:purple;">箭头描述数据的流向</mark> 箭头上标注的内容可以是<mark style="color:purple;">信息说明或数据项</mark>
* 处理：表示对数据的<mark style="color:purple;">加工和转换</mark>，用矩形框表示，<mark style="color:purple;">指向</mark>处理的数据流为该处理的<mark style="color:purple;">输入数据</mark>，<mark style="color:purple;">离开</mark>处理的数据流为该处理的<mark style="color:purple;">输出数据</mark>。
* 数据存储：表示用<mark style="color:purple;">数据库形式</mark>（或者<mark style="color:purple;">文件形式存储</mark>的数据），对其进行的存取分别指向或离开数据存储的箭头表示。
* 外部项：也称为<mark style="color:purple;">数据源</mark>或者<mark style="color:purple;">数据终点</mark>。描述系统数据的提供者或者数据的使用者。用<mark style="color:purple;">圆角框</mark>或者<mark style="color:purple;">平行四边形框</mark>表示。

建立[DFD](ruan-jian-gong-cheng.md#shu-ju-liu-tu-dfd)图的目的是描述系统的功能需求

建模过程和步骤：

（1）明确目标 确定系统范围

（2）建立顶层DFD图

（3）构建第一层DFD分解图

（4）开发DFD层次结构图

（5）检查确认DFD图

顶层图被逐渐细化

### 数据字典

用户可以访问的记录数据库和应用程序元数据的目录。目的是对数据流程图中的各个元素做出详细的说明。数据字典是对描述数据的信息集合，是对系统中使用的所有数据元素定义的集合。

* 数据字典是对系统中使用所有数据元素定义的集合
* 最重要的作用是作为分析阶段中的工具。给数据流图上每个元素加以定义和说明。数据流图上所有元素的定义和解释的文字集合就是数据字典。

各部分描述：

（1）数据项：图中数据块数据项说明。不可再分的数据单位。若干数据项构成一个数据结构

（2）数据结构：反映数据之间的组合关系

（3）数据流：是数据结构在系统内传输的路径。

（4）数据存储：数据流图中数据块的数据存储特性说明。数据流的来源和去向之一。

（5）处理过程：功能块的说明。

### 结构化设计SD

面向<mark style="color:purple;">数据流</mark>的方法 以<mark style="color:purple;">数据流图和数据字典</mark>等文档作为<mark style="color:purple;">基础</mark>

### <mark style="color:purple;">耦合</mark>&#x20;

<mark style="color:purple;">从低到高</mark>

* 非直接耦合：两个模块之间没有直接关系
* 数据耦合：一组模块借助<mark style="color:purple;">参数表传递简单数据</mark>
* 标记耦合：一组模块通过<mark style="color:purple;">参数表传递记录复杂数据</mark>（<mark style="color:purple;">数据结构</mark>）
* 控制耦合：模块之间传递的信息中包含用于<mark style="color:purple;">控制模块内部逻辑</mark>的信息
* 通信耦合：一组模块共用了一组输入信息，或者它们的输出<mark style="color:purple;">需要整合</mark>以形成完整数据，即<mark style="color:purple;">共享了输入或输出</mark>。
* 公共耦合：多个模块都<mark style="color:purple;">访问同一个公共数据环境</mark>，公共的数据环境可以是<mark style="color:purple;">全局数据结构、共享的通信区、内存的公共覆盖区</mark>等。
* 内容耦合：一个模块<mark style="color:purple;">直接访问另一个模块的内部数据</mark>；一个模块不通过正常入口转到另一个模块内部；两个模块有一部<mark style="color:purple;">分程序代码重叠</mark>；一个模块有<mark style="color:purple;">多个入口</mark>等

### <mark style="color:purple;">聚合</mark>

从高到低

* 功能内聚：完成<mark style="color:purple;">单一功能</mark>，各个部分<mark style="color:purple;">协同工作，缺一不可</mark>
* 顺序内聚：处理<mark style="color:purple;">元素相关</mark>，必须<mark style="color:purple;">顺序执行</mark>
* 通信内聚：所有处理元素<mark style="color:purple;">集中在一个数据结构区域</mark>上
* 过程内聚：处理<mark style="color:purple;">元素相关</mark>，必须按<mark style="color:purple;">特定次序</mark>执行
* 时间内聚：必须在<mark style="color:purple;">同一时间间隔内</mark>执行
* 逻辑内聚：<mark style="color:purple;">逻辑上相关</mark>的一组任务
* 偶然内聚：一组<mark style="color:purple;">没有关系或松散关系</mark>的任务

