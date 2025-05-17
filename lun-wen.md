# 论文

## 模版

<mark style="color:red;">自定义文本</mark> <mark style="color:purple;">固定话术</mark> <mark style="color:orange;">选题技术</mark>

### 摘要

* 本人于2023年**年3月**月参与**项xxxx目，该系统是xxxx**。在该项目组中我担任<mark style="color:purple;">架构师</mark>，主要负责<mark style="color:purple;">整体架构设计和中间件选型</mark>。本文以该演进项目为例，主要讨论<mark style="color:orange;">系统安全架构设计</mark>及其应用在本项目中的具体应用。本项目通过采用<mark style="color:orange;">面部识别和证件照片验证等生物特征技术</mark>解决<mark style="color:orange;">客户因为证件丢失</mark>,<mark style="color:orange;">被他人盗用证件办理业务后用于从事非法活动的问题</mark>:通过采用<mark style="color:orange;">基于角色的访问控制</mark>来<mark style="color:orange;">限制</mark>营业员的<mark style="color:orange;">业务受理范围和用户的业务受理范围</mark>;通过采用<mark style="color:orange;">访问控制列表</mark>技术实现该运营商的<mark style="color:orange;">网上商城业务</mark>，<mark style="color:orange;">拓展</mark>了<mark style="color:orange;">新业务领域</mark>，<mark style="color:orange;">增加</mark>了该运营商的<mark style="color:orange;">收入</mark>。项目最终顺利上线，获得一线员工和用户的一致好评。\
  【注意:实际写作中相关项目情况应介绍清楚，摘要字数(包括标点符号)一般写 280 到 300 字】

### 正文

* 随着<mark style="color:red;">人工智能领域AI和电商的大洪流</mark>**的迅猛发展，需求的快速变化，**，经过认真调研后决定采用<mark style="color:red;">平滑演进的方式</mark>来实现**系统，因此**。

【项目背景内容可分2段写，第1段简要说明下项目来龙去脉】

* **系统是**业务的核心系统，包括了**等几十个菜单。该系统实现了**，整合了**技术。以**实现了该系统的**的建设，与甲方共建**多个专题建设。本项目组共**人，我在项目中担任系统架构师职位，主要负责整体架构设计及中间件选型，项目于**年**月成功启动。整个项目共耗时**个月，第一版于**年**月顺利通过验收。同时也实现了\*\*等重点业务。【第2段对系统整体情况进行细致介绍，项目背景第 1、2 段内容可以写 400 到 450 字】

### 大量理论知识结合项目论述

xxxxxxxx

例子：

<figure><img src=".gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 小结

通过上述<mark style="color:orange;">鉴别服务和访问控制方案</mark>的实施，该系统于2023**年8**月完成第一个版本的顺利验收。上线后虽然出现了某些特殊用户到某个营业厅办理不了某些业务需要到指定的营业厅才能办理的场景，但是并没有发生<mark style="color:orange;">角色越权</mark>行为，没有给集团带来经济损失。项目至今仍然保持着每月一次或者两次的版本迭代，顺利实现了1.0 到 2.0 架构演进的平滑式过渡，得到了甲方的肯定，实践证明鉴别服务和访问控制方案适用于该项目安全架构的实现。\
当然，在系统的后期运行维护过程中，也陆续发现了一些问题和不足，在<mark style="color:orange;">服务调用链上没有做访问量控制</mark>，<mark style="color:orange;">没有做调用链剥离</mark>，当推广的某一<mark style="color:orange;">业务量突然上来</mark>后，会导致<mark style="color:orange;">调用链崩溃</mark>而不可用，也会因为运维修复大量数据重跑某些业务，导致关键业务崩溃，波及实时业务。同时也导致了很多异常数据，给运维人员增加了工作量。在后续的改进方案中<mark style="color:orange;">对重点调用链进行了剥离，并做了访问量控制</mark>。运维大批量的数据修复工作只能在晚上执行。运维人员对数据库的一切增删改查操作均需要有日志记录，并定期将该运维人员的操作日志发给该运维人员确认是否是本人操作，确保生产数据的安全性。
