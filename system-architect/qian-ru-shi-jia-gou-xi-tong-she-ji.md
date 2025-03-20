# 嵌入式架构系统设计

从描述语言、非功能性需求描述、需求和架构的一致性等三个方面，用300字以内的文字说明软件需求到架构的映射存在哪些难点。

(1)软件需求通常以非正规的自然语言形式频繁获取。而软件架构则更倾向于使用一种更为正式、结构化的语言来描述系统的组件接口、通信和交互方式。\
(2)非功能属性(如性能、安全性、可用性等)在软件需求中通常被描述为系统属性，但在架构模型中形成规约却较为困难。这是因为非功能属性往往涉及多个系统组件和交互，需要综合考虑多个方面，而架构模型则可能更侧重于描述系统的结构和功能。\
(3)从软件需求映射到软件架构的过程中，保持一致性和可追湖性也是一个复杂的任务。由于单一的软件需求可能涉及多个软件架构的关注点，而一个架构元素也可能对应多个软件需求，因此确保它们之间的映射关系是准确且可追溯的非常重要。



嵌入式实时操作系统实时性 评价指标\
<mark style="color:blue;">中断响应和延迟时间</mark>\ <mark style="color:blue;">任务切换时间</mark>\ <mark style="color:blue;">信号量混洗时间</mark>

嵌入式系统发展历程\
<mark style="color:blue;">1 单片微型计算机SCM阶段 单片机时代</mark>\ <mark style="color:blue;">2 微控制器 MCU阶段</mark>\ <mark style="color:blue;">3 片上系统 SoC</mark>\ <mark style="color:blue;">4 以Internet 为基础的嵌入式系统</mark>\ <mark style="color:blue;">5 在智能化 云技术推动下的嵌入式系统</mark>

自顶向下：从系统层级开始标识结构对象，<mark style="color:purple;">逐步降低抽象层级</mark>，容易确保开发者工作没有偏离用例中所规定的需求。

自底向上：专注于<mark style="color:purple;">域</mark>的构造 首先<mark style="color:purple;">确定域的关键类和关系</mark> ，最终开发者会到达子系统级的抽象。

嵌入式系统初始化过程：\ <mark style="color:blue;">片级初始化->板级初始化->系统级初始化</mark>

1 嵌入式系统以<mark style="color:purple;">应用</mark>为中心 <mark style="color:purple;">计算机技术</mark>为基础\
2 一般由<mark style="color:blue;">嵌入式处理器 相关支撑硬件 嵌入式操作系统 支撑软件 及 应用软件</mark>组成\
3 典型架构可分为 <mark style="color:purple;">层次化模式架构</mark> <mark style="color:purple;">递归模式架构</mark>
