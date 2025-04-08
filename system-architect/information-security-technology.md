# 信息安全技术

**信息安全基础** ☆☆&#x20;

<mark style="color:purple;">机密性</mark>： 网络信息不泄露给非授权的用户 实体或程序 能够防止非授权者获取信息。&#x20;

<mark style="color:purple;">完整性</mark>： 网络信息或系统未授权不能进行更改&#x20;

<mark style="color:purple;">可用性</mark>： 合法许可的用户能够及时获取网络信息或服务&#x20;

<mark style="color:purple;">可控性</mark>： 可以控制授权范围内的信息流向及行为方式&#x20;

<mark style="color:purple;">可审查性</mark>： 对出现的信息安全问题提供调查的依据和手段

<mark style="color:purple;">信息安全的范围包括设备安全 数据安全 内容安全和 行为安全</mark>

安全措施的目标： <mark style="color:purple;">访问控制 认证 完整性 审计 保密</mark>



**信息加密技术** ☆☆☆

<mark style="color:purple;">对称加密</mark> （加密解密使用同一密钥）

特点：<mark style="color:purple;">加密强度不高 效率高 密钥分发困难</mark>

用途： 消息明文进行加密传送&#x20;

例子：&#x20;

<mark style="color:purple;">DES</mark>：替换+易位 56位密钥 64位数据块 速度快 密钥易产生&#x20;

<mark style="color:purple;">3DES</mark>：(3重DES) 两个56位的密钥&#x20;

<mark style="color:purple;">RC-5</mark>

<mark style="color:purple;">IDEA</mark>：128位密钥 64位数据块 比DES加密性好 对计算机功能要求低&#x20;

<mark style="color:purple;">AES</mark>：高级加密标准



<mark style="color:purple;">非对称加密</mark>（公开密钥加密）<mark style="color:purple;">密钥必须成对使用（公钥加密 私钥解密）</mark>&#x20;

特点： 加密速度慢 但强度高 密钥分发容易&#x20;

用途： 对密钥加密 做数字签名&#x20;

例子：

<mark style="color:purple;">RSA</mark> 计算量极大 难破解

<mark style="color:purple;">ECC</mark> 椭圆曲线算法&#x20;

<mark style="color:purple;">Elgamal</mark> 安全性依赖于计算机有限域上离散对数这个难题



**密钥管理技术** ☆☆

<mark style="color:purple;">数字证书</mark>&#x20;

<mark style="color:purple;">版本信息 序列号</mark>（唯一）&#x20;

<mark style="color:purple;">有效期</mark>UTC&#x20;

<mark style="color:purple;">所有人名称</mark>X.500&#x20;

公开密钥 证书发行者对证书<mark style="color:blue;">签名</mark>

CA：认证中心&#x20;

RA：注册审批机构

&#x20;KMC：密钥管理中心&#x20;

<figure><img src="../.gitbook/assets/Pasted image 20250208105234.png" alt=""><figcaption></figcaption></figure>

访问控制类型&#x20;

1 基于对象的访问控制 <mark style="color:purple;">控制策略和控制规则</mark>是OBAC访问控制系统的核心所在&#x20;

2 基于角色的访问控制 RBAC由<mark style="color:purple;">用户U 角色R 会话S 和 权限P</mark>四个基本要素组成&#x20;

3 基于任务的访问控制 TBAC模型由<mark style="color:purple;">工作流 授权结构体 受托人集和许可集</mark>四部分组成&#x20;

4 基于属性的访问控制 ABAC是根据主体的属性、客观的属性、环境的条件以及访问策略对主体的请求操作进行授权许可或拒绝

**计算机信息系统安全保护等级划分**

1 用户自主保护级 （普通互联网用户） 对公民 法人 和其它组织权益有损害&#x20;

2 系统审计保护级 （内联网或国际网进行商务活动 保密） 对<mark style="color:purple;">公民 法人 和其他组织有严重损害 或 损害社会秩序和公共利益 但不损害国家安全</mark>

3 安全标记保护级 （各级国家机关 金融 邮电通信） 对社会秩序和公共利益造成损害 或对<mark style="color:purple;">国家安全造成损害</mark>

&#x20;4 结构保护级 （中央级国家机关 广播电视部门 科技企业 国防建设 国家重点科研机构） 对社会秩序和公共利益造成损害 或对 <mark style="color:purple;">国家安全造成严重损害</mark>

5 访问验证保护级 （国防 依法对计算机信息系统特殊隔离的单位）<mark style="color:purple;">对国家安全造成特别严重的影响</mark>



**安全架构**&#x20;

信息安全面临威胁

<mark style="color:purple;">被动性攻击： 网络监听 非法登录 信息截取</mark>

<mark style="color:purple;">主动性攻击： 数据篡改 假冒身份 拒绝服务 重放攻击 散播病毒 主动抵赖</mark>

<mark style="color:purple;">被动攻击：收集信息为主 破坏保密性 （通过对系统进行长期监听 利用统计分析方法对注入通信频度、通信的信息流向）</mark>

<mark style="color:purple;">主动攻击： 中断（破坏可用性）篡改（破坏完整性）伪造（破坏真实性）</mark>



**安全模型** ☆☆☆

BLP模型

简单安全规则： 安全级别低的主题不能读安全级别高的客体 星属性安全规则： 安全级别高的主题不能往低等级的客体写

Biba模型

星完整性规则： 完整性级别低的主体不能对完整性高的客体写数据 简单完整性规则： 完整性级别高的主体不能从完整性级别低的客体读取数据

Chinese Wall 模型&#x20;

1 与主体曾经访问过的信息属于<mark style="color:blue;">同一公司数据集合</mark>的信息 即<mark style="color:blue;">墙内信息可以访问</mark>

2 属于一个<mark style="color:blue;">完全不同的利益冲突组</mark>的可以访问&#x20;

3 主体对一个客体进行写的前提是主体<mark style="color:blue;">未对任何属于其他公司数据集</mark>进行访问过



**区块链技术** ☆☆☆

你去开治安

特点： <mark style="color:purple;">去中心化 开发性 自治性 安全性（信息不可纂改） 匿名性（去信任）</mark>

分类： <mark style="color:blue;">公有链 私有链 联盟链</mark>

asdsadd

(1)消息摘要的作用是什么?对摘要加密的作用是什么? 答:消息摘要的作用是防篡改，因为摘要是单向不可逆的，一旦篡改就得不到原来的摘要了对摘要进行加密，其实就是我们常说的数字签名的过程，数字签名是利用发送方的私钥对摘要进行加密的过程，我们一般称之为数字签名，这个过程是为了标识发送者身份，保证发送者身份不可抵赖。



(2)提高安全性的策略有哪些?&#x20;

答:提高安全性的手段包括:身份认证、限制访问、检测攻击、维护完整性等。



(3)时间戳在区块链里怎么理解??

答:时间戳在区块链中是一个重要的元数据，用于记录区块的产生时间、验证区块链的有效性以及支持难度调整算法。时间戳的存在确保了区块链中的时间顺序和数据的不可篡改性。



(4)数字水印是什么?&#x20;

答:数字水印指把一些标识信息直接嵌入数字载体当中(包括多媒体、文档、软件等)，且不影响原载体的使用价值，也不容易被探知和再次修改。数字水印可以被生产方识别和辨认，通过隐藏在载体中的信息，从而达到保护版权的目的。数字水印技术主要是用于数字版权保护。

