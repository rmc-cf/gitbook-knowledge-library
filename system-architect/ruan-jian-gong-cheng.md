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
