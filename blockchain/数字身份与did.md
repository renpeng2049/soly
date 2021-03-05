## 数字身份的发展现状
随着互联网的出现和普及，身份有了另外一种表现形式，即数字身份。数字身份的演进经历了四个阶段，分别是：中心化身份、联盟身份、以用户为中心的身份以及自我主权身份。

### 中心化身份
中心化身份是由单一的权威机构进行管理和控制的。中央集权化的机构，像是1988年成立的IANA（Internet Assigned Number Authority，互联网号码分配局）管理着国际互联网中使用的IP 地址、域名和许多其他参数。

### 联盟身份
20 世纪末，数字身份的发展获得了重大进展。中心化身份导致的身份数据的混乱而零碎等弊端，催生出了联盟身份这种由多个机构或联盟管理控制的身份体系。简单地说，用户的在线身份数据具备了一定程度的可移植性，例如允许用户登录某个网站时，可以使用其他网站的账户信息，类似于QQ、微信或者微博的跨平台登录。

### 以用户为中心的身份
以用户为中心的身份，希望实现用户可以通过授权、许可来决定身份的存储、正常使用以及在跨服务跨平台业务中的使用。因此侧重于三个元素：用户的许可、互操作性以及基于用户对数据的完全掌控。

### 自我主权身份
自我主权身份是以用户为中心的身份的进阶阶段，二者的共同之处在于，都以用户完全掌控自己的身份数据为出发点，但自我主权身份更进一步，数据的收集、存储和使用都去中心化地分布在一个生态系统中，同时对于个人身份的验证，允许其他的普通用户发表含有他人身份信息的声明（即下文将提到的“可验证声明”）。自我主权身份提供了三个必需的元素：单独控制、安全性和完全可移植性。它取消了上述三个阶段的集中外部控制。身份完全由个人(或组织)拥有、控制和管理。从这个意义上说，个人是他们自己的身份提供者——没有外部的一方可以声称为他们“提供”身份，因为身份本质上是他们的。个人的数字存在是独立于任何单一组织的。

## DID
传统的身份管理系统基于集中权限，例如公司的目录服务，证书颁发机构或者域名注册。从加密信任验证的角度来看，每一个集中式权限机构都是一个信任根，要使身份管理跨系统工作，需要实现联合身份管理。

分布式账本技术（区块链技术:DLT）的出现，为完全分散的身份管理提供了机会，在分散的身份系统中，实体可以自由的使用任何共享的信任根。全球分布式账本，分散式P2P网络或者其他具有类似功能的系统，提供了管理信任根的方式，既没有集中权限也没有单点故障。结合使用，DLT和分散式身份系统使任何实体都能够在任意数量的独立信任根的基础上创建和管理自己的标识符。

实体由分布式标识符（DID）标识，并且可以通过可验证的证明内容（例如:数字签名，生物识别等）进行身份认证。DID指向DID文档，每个DID文档中包含一组服务端点，用于与DID标识的实体进行交互。遵循隐私设计，任何实体可以根据不同的需求申请任意数量的DID,以尊重实体所需的身份，角色和背景的分离。

### DID的优势
1. 去中心化：基于区块链，避免了身份数据被单一的中心化权威机构所控制。
2. 身份自主可控：基于DPKI （分布式公钥基础设施），每个用户的身份不是由可信第三方控制，而是由其所有者控制，个人能自主管理自己的身份。
3. 可信的数据交换：身份相关数据锚定在区块链上，认证的过程不需要依赖于提供身份的应用方。

> 去中心化身份标识(Decentralized Identifier，DID)是一种新类型的标识符，具有全局唯一性、高可用性可解析性和加密可验证性。DIDs通常与加密材料(如公钥)和服务端点相关联，以建立安全的通信信道。DIDs对于任何受益于自管理、加密可验证的标识符(如个人标识符、组织标识符和物联网场景标识符)的应用程序都很有用。例如，当前W3C可验证凭据的商业部署大量使用DIDs来标识人员、组织和事物，并实现许多安全和隐私保护保证。 ——W3C 文档
## 可验证声明（Verifiable Claims）
可验证声明用来证明实体的某些身份属性，它可以作为一个数据单元进行存储和传输，并可被任何实体验证。




## TODO 信任模型梳理
https://www.w3.org/TR/vc-data-model/#trust-model

The verifiable credentials trust model is as follows:
1. The verifier trusts the issuer to issue the credential that it received. To establish this trust, a credential is expected to either:
   + Include a proof establishing that the issuer generated the credential (that is, it is a verifiable credential), or
   + Have been transmitted in a way clearly establishing that the issuer generated the verifiable credential and that the verifiable credential was not tampered with in transit or storage. This trust could be weakened depending on the risk assessment of the verifier.
2. All entities trust the verifiable data registry to be tamper-evident and to be a correct record of which data is controlled by which entities.
3. The holder and verifier trust the issuer to issue true (that is, not false) credentials about the subject, and to revoke them quickly when appropriate.
4. The holder trusts the repository to store credentials securely, to not release them to anyone other than the holder, and to not corrupt or lose them while they are in its care.

This trust model differentiates itself from other trust models by ensuring the:
1. Issuer and the verifier do not need to trust the repository.
2. Issuer does not need to know or trust the verifier.

1. 签名方式演变
2. 数据保存方式演变


## TODO ioa、微软身份认证、uport对比

## TODO 撤销vc

## TODO 选择性披露

## TODO 智能合约权限架构

## TODO 挑战challenge

## TODO 一般用例
「人是社会关系的总和」。通过对实体进行DID、凭证（Credential）的生成及绑定，可以更加准确完善地描述实体身份、实体间关系，并有效提高实体间信息流转的真实性和效率。

### 案例一：新入职员工背景调查
#### 背景
合作方是一家中小企业，在招聘员工时需要对员工的学历信息、之前雇主信息进行真实性验证。存在的问题是：对员工而言，需要去每个机构花费大量时间精力获取最新版的材料。对企业而言，材料的获取和流转的过程中可能遭到篡改，而且缺乏验证材料真实性的手段。

参与方：

1. 员工
2. 学校
3. 前雇主公司
4. 现雇主公司

#### 流程
1. 员工、学校、公司分别进行DID注册及KYC认证。
2. 员工向学校学校申请学历证明凭证（Credential）、学位证明凭证（Credential）。
3. 员工向前雇主公司申请工作证明凭证（Credential）、离职证明凭证（Credential）。
4. 员工将这些凭证（Credential）挂到自己的个人主页上，或者直接提交给现雇主公司。
5. 现雇主公司通过凭证验证（Verify）接口对上述凭证（Credential）进行验证。
6. 验证通过，现雇主公司发放入职offer。

### 案例二：数据共享
#### 背景
当前，不同机构间存在着大量用户数据流通的需求。然而，由于各个机构之间通常难以组建有效的信任合作机制，因此，各机构间难以将各自保管的用户数据安全可信地授权共享给其他机构。通过did解决方案，可帮助机构间进行可信数据授权及共享，使得各机构可基于全面的数据为用户提供更高质量的服务。

参与方：

1. 用户
2. 数据持有机构
3. 数据使用机构
4. 身份证明机构

#### 流程
1. 在身份证明机构、数据持有机构、数据使用机构间搭建区块链网络，机构作为节点接入并注册DID。
2. 由身份证明机构为用户进行KYC并生成DID
3. 用户授权数据使用机构使用自己的数据
4. 由身份证明机构为用户生成授权凭证（Credential），标明授权对象、数据属主、有效期、授权内容等属性，并使用用户私钥进行签名；身份证明机构可选择将授权凭证生成摘要并写入区块链，达到增信目的
5. 数据使用机构出示授权凭证给数据持有机构
6. 数据持有机构通过凭证验证（Verify）接口，验证授权凭证
7. 验证通过，数据持有机构将数据发送给数据使用机构


## 问题
1. 自主身份相对于传统身份管理的优缺点？

2. issuer可以作恶吗？
   验证者信任issuer，和他所签发的vc。
   issuer一般来自现实世界的机构、企业和其他可验证实体，issuer要表明自己身份，要么来自更权威的信任实体背书，要么尽可能全面的出示现实世界可验证的关联信息。
   
   如果再这种情况，issuer还出现作恶的情况，那么这不是技术的原因，而是背后使用的人的问题。
3. 区块链如何杜绝中间人攻击？
4. 存证与RSA accumulate两种方案的优劣？
5. 区块链发票的实现原理？
6. did恢复策略？


## 思考
1. 现实世界的信任，使用政府、媒体等公共机构提供的信息，外加亲身体验即可进行确认，虽然也不是100%确保可信。而网络世界中，信任的问题更加突出，任何信息都可以随意复制，修改然后再分发。
2. 各个网络服务提供商（互联网公司）都提供一套自己的数字身份与权限管理功能，数据分散不互通，且容易丢失与泄露；
3. 网络世界身份认证的另一方面，是基于中心化证书颁发机构的PKI体系，但是PKI多用于商业场景，成本不菲。而且CA机构在架构中存在中心化风险（CA机构攻击事件）。
4. 借助分布式账本技术，可以实现数据共享、去中心化，（DPKI），为可信网络提供基础存储传播信任能力。
5. 信任根还是来自于现实世界各可信机构，政府、中心化证书颁发机构。

### 与微信等中心化身份系统场景对比分析
| 编号 | 场景                                               | 微信场景                                             | did场景                              |
|------|----------------------------------------------------|------------------------------------------------------|--------------------------------------|
|    1 | 用户采用微信/did账号登录APP                        | 拉起微信                                             | 拉起did ua                           |
|    2 | 用户确认授权某些信息                               | 在微信中同意授权                                     | 在did ua中选择相应的vc，同意授权     |
|    3 | 302到APP server端，APP Server端调用API获取用户信息 | APP Server请求微信获取token，调用微信API获取用户信息 | APP Server到链上获取相关信息，验证vc |
|    4 | APP server保存用户信息，维护登录态，并返回jwt到APP | 无                                                   | jwt是否可以直接使用vc?               |

did在作为第三方登录时，与微信等中心化身份系统没有太多的区别，主要的优势还是在于可验证性、选择性披露等。
倒是作为jwt的新形式，可以挖掘创新点。 
