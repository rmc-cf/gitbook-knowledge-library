# 项目管理



项目<mark style="color:purple;">范围定义</mark>是<mark style="color:purple;">生产项目计划</mark>的<mark style="color:purple;">基础</mark>。

步骤：<mark style="color:purple;">范围计划编制->范围定义->创建WBS->范围确认->范围控制</mark>

范围管理就是要<mark style="color:purple;">确定项目的边界</mark>，即，要确定哪些工作是项目应该做的，哪些工作不应该包括在项目中。这个过程用于确保项目干系人对作为项目结果的产品或服务，以及开发这些产品所确定的过程有一个共同的理解。

WBS，工作分解结构，把项目整体或者主要的可交付成果分解成<mark style="color:purple;">容易管理、方便控制</mark>的若干个子项目，子项目需要继续<mark style="color:purple;">分解为工作包</mark>。持续这个过程，直到整个项目都分解为<mark style="color:purple;">可管理的工作包</mark>，这些工作包的总和就是项目的<mark style="color:purple;">所有工作范围</mark>。创建WBS的目的是<mark style="color:purple;">详细规定项目的范围</mark>，<mark style="color:purple;">建立范围基准</mark>。

常用方法：<mark style="color:purple;">专家估算、三点估算法、功能点估算、自上而下估算、自下而上估算</mark>。其中常用的是三点估算法，其公式为：

<div data-full-width="true"><figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure></div>

采用分解技术来定义活动，就是要把项目工作包<mark style="color:purple;">分解成更小的、更易于管理的组成部分，即活动</mark>。为完成工作包而必须开展的工作。定义活动过程最终输出的是<mark style="color:purple;">活动</mark>，而非可交付成果。<mark style="color:purple;">可交付成果是创建工作分解结构过程的输出</mark>。

WBS、WBS词典与活动清单，既可依次编制，也可同时编制。WBS和WBS词典是制定最终活动清单的依据。WBS中的每个工作包都需分解成活动，以便通过这些活动来完成相应的可交付成果。让团队成员参与分解，有助于得到更好更准确的结果。

WBS分解的<mark style="color:purple;">基本要求</mark>：

<mark style="color:blue;">WBS的工作包是可控和可管理的，不能过于复杂</mark>\ <mark style="color:blue;">任务分解也不能过细，一般原则WBS的树形结构不超过6层</mark>\ <mark style="color:blue;">每个工作包要有一个交付成果</mark>\ <mark style="color:blue;">每个任务必须有明确定义的完成标准</mark>\ <mark style="color:blue;">WBS必须有利于责任分配</mark>

制定进度计划：\
关键路径法（CPM）：是项目整个路径中<mark style="color:purple;">最长的路径</mark>，是项目<mark style="color:purple;">完成的最短时间</mark>。<mark style="color:purple;">关键路径可以有多个，但是越多，项目风险越大</mark>。向关键路径要时间，向<mark style="color:purple;">非关键路径要资源</mark>。

总时差【即：松弛时间】：在<mark style="color:purple;">不延误总工期</mark>的前提下，该活动的<mark style="color:purple;">机动时间</mark>。活动的总时差等于该活动最迟完成时间与最早完成时间之差，或该活动最迟开始时间与最早考试时间之差。

**Gantt**甘特图，又称为横道图、条状图（Bar chart），通过条状图来显示<mark style="color:purple;">项目、进度和其他时间相关的系统进展</mark>的内在关系随着时间进展的情况。以提出者亨利·劳伦斯·甘特（Henry Laurence Gantt）先生的名字命名。

甘特图按内容不同，分为计划图表、负荷图表、机器闲置图表、人员闲置图表和进度表五种形式。

优点：甘特图<mark style="color:purple;">直观简单，易制作及理解</mark>，能很清晰地表示出<mark style="color:purple;">每一项任务的起始时间与结束时间</mark>，一般<mark style="color:purple;">适用比较简单的小型项目</mark>，可用于WBS的任何层次、<mark style="color:purple;">进度控制、资源优化、编制资源和费用计划</mark>。

缺点：<mark style="color:purple;">不能系统的表达</mark>一个项目所包含的<mark style="color:purple;">各项工作之间的复杂关系</mark>，<mark style="color:purple;">难以进行定量的计算和分析</mark>，以及计划的优化等。

\----------------------------------------------------------------------------------------------------------------------

<mark style="color:purple;">PERT图</mark>用于求项目关键路径松弛时间。

关键路径：能够完成整个项目的<mark style="color:purple;">最长路径</mark>

松弛时间：一个任务能够<mark style="color:purple;">空闲歇息的时间，在不影响总工期</mark>的前提下

最早开始时间：某段工程开始点之前最长的输入流之和\
最晚开试：关键路径-开始点到最后整个工程最后结束点的距离\
最早结束：某段工程结束点之前最长的输入流之和\
最晚结束：关键路径-该结束点到整个工程最后结束点的距离\
松弛时间=最晚开始-最早开始②-①\
松弛时间=最晚结束-最早结束④-③\
松弛时间=关键路径-所求活动在的最长路径



## 成本管理

成本管理过程包括：<mark style="color:purple;">成本估算、成本预算与成本控制</mark>

成本预算：Cost Budget，将总的成本估算分配到各项活动和工作包上，来建立一个成本的基线\
成本估算：Cost Estimate，对完成项目活动所需资金进行近似的估算\
成本控制：Cost Control，成本控制是一个监视项目状态的过程，以更新项目成本并管理成本基线的更改\
成本类型，或叫成本分类

直接成本：项目团队<mark style="color:purple;">差旅费、工资、物料及设备使用费</mark>等\
间接成本：税金\
沉没成本：一种历史成本，对<mark style="color:purple;">现有决策而言是不可控</mark>成本\
变动成本：随着<mark style="color:purple;">生产量、工作量、或时间而变</mark>的成本\
机会成本：利用一定时间或资源生产一种商品时，便<mark style="color:purple;">失去利用这些资源生产其他最佳替代品</mark>的成本
