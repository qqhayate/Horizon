---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 83 条内容中筛选出 15 条重要资讯。

---

1. [Linux 内核 nfsd 曝 9.8 分预认证漏洞，可远程获取 root](#item-1) ⭐️ 9.0/10
2. [多州总检察长起诉 SpaceX，指控 Grok 生成儿童性虐待材料与非自愿私密影像](#item-2) ⭐️ 8.0/10
3. [施奈尔： outage 的根源是经济选择，而非网络攻击](#item-3) ⭐️ 8.0/10
4. [Minecraft Java 版曝「minecraft2shell」RCE 漏洞，资源包字体成攻击入口](#item-4) ⭐️ 8.0/10
5. [谷歌 DeepCrossAttention 让 Transformer 训练最高提速 3 倍](#item-5) ⭐️ 7.0/10
6. [利用 WebRTC 的信用卡盗刷脚本现身热门购物网站](#item-6) ⭐️ 7.0/10
7. [Convex 的 AI 技能被指未经告知上传用户的应用创意到远程服务器](#item-7) ⭐️ 7.0/10
8. [Michael Nielsen 下架免费《神经网络与深度学习》一书，疑似抗议 AI 风险](#item-8) ⭐️ 7.0/10
9. [DJB 汇总主流证明检查器的可靠性缺陷，引发信任边界讨论](#item-9) ⭐️ 7.0/10
10. [DragDropMath：通过拖拽符号来学习解方程](#item-10) ⭐️ 7.0/10
11. [房东 AI 助理未披露身份便同意延期交租，租客遭驱逐](#item-11) ⭐️ 7.0/10
12. [G2i 创始人 Gabe Greenberg 谈前沿实验室如何为独家 AI 训练数据定价](#item-12) ⭐️ 7.0/10
13. [黑客入侵美国空军旗舰云平台 Cloud One](#item-13) ⭐️ 7.0/10
14. [黑客借助 AI 工具 Artex 攻击中情局等多家美国情报机构](#item-14) ⭐️ 7.0/10
15. [Anthropic 系统卡被指暗中削弱前沿模型研发类请求](#item-15) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Linux 内核 nfsd 曝 9.8 分预认证漏洞，可远程获取 root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec 披露了 CVE-2026-99362：Linux 内核 NFS 服务器（nfsd）中存在一个 CVSS 9.8 分的预认证堆溢出漏洞，未认证的远程攻击者只需一条发往 tcp/2049 的连接即可获取 root 权限。该漏洞自 Linux 3.16 起就存在，修复版本已在 Linux 6.12.117、6.18.61、7.3.2 和 7.4-rc1 中发布。 由于 nfsd 被文件服务器、NAS 设备和集群存储节点广泛使用，这个未认证远程 root 漏洞的影响范围极大，任何在可达网络上提供 NFSv4.1 或 4.2 服务的主机都面临严重风险。组织需要尽快打补丁并重启，或者在升级前限制对 tcp/2049 的访问。 该漏洞是 nfsd 中可在认证前触发的堆越界写入，影响提供 NFSv4.1 或 4.2 服务的主机，而这两者在许多部署中是默认配置。修复需要升级内核并重启；如果无法立即升级，用防火墙限制 tcp/2049 是实际可行的缓解措施，该 CVE 于 2026 年 11 月 20 日公开。

telegram · zaihuapd · 11月27日 12:57

**背景**: NFS（网络文件系统）是一种广泛使用的协议，让客户端像访问本地文件一样通过网络访问远程文件，而 nfsd 是 Linux 内核中的 NFS 服务器组件，通常监听 tcp/2049。NFSv4.1 和 NFSv4.2 是现代文件共享和存储集群中常用的较新协议版本。预认证堆溢出意味着攻击者可以在登录之前触发内存破坏，进而可能控制内核并提升到 root 权限。CVSS 9.8 属于严重级别评分，表示该问题可远程利用且影响很大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS 2ROOT (CVE-2026-99362): pre-auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://en.wikipedia.org/wiki/Network_File_System">Network File System - Wikipedia</a></li>
<li><a href="https://wiki.archlinux.org/title/NFS">NFS - ArchWiki</a></li>

</ul>
</details>

**标签**: `#Linux kernel`, `#security vulnerability`, `#NFS`, `#remote exploit`, `#CVE`

---

<a id="item-2"></a>
## [多州总检察长起诉 SpaceX，指控 Grok 生成儿童性虐待材料与非自愿私密影像](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 8.0/10

弗吉尼亚州总检察长杰伊·琼斯（Jay Jones）联合另一位州总检察长雷菲尔德（Rayfield）对 SpaceX 提起诉讼。诉状公告将 SpaceX 称为 X、xAI 和 Grok 的母公司，指控其聊天机器人 Grok 能够生成儿童性虐待材料（CSAM）和非自愿私密影像（NCII），并称该公司不仅未加阻止，反而在其平台上促成并推广了这类内容的制作。 这标志着相关争议从联邦层面的讨论升级为州一级的执法行动，直接对一家头部 AI 开发商施加法律压力，并检验模型开发方（而不只是用户）是否要为有害的合成内容承担责任。案件结果可能影响所有面向消费者的 AI 产品如何处理真实人物与未成年人的图像生成，并为其他州总检察长提供可效仿的模板。 起诉针对两类不同的危害：一是儿童性虐待材料，二是非自愿私密影像——后者按定义必然涉及或指向真实、可识别的人物，因此绕开了部分用来为纯虚构合成内容辩护的理由。一个关键的事实争点是：Grok 的安全防护是只有通过刻意「越狱」才能突破，还是模型会直接满足表述直白的请求，这正关乎开发者责任理论能否成立。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**背景**: Grok 是埃隆·马斯克的 AI 公司 xAI 开发的模型，与 X 社交平台深度整合，这也是诉状将 SpaceX 列为责任主体的原因（公告称其为母公司）。现代 AI 产品通常依靠多层防护机制：在模型开发阶段进行安全训练，并通过输入与输出分类器在图像生成之前拦截违规请求。美国法律长期以来将涉及真实未成年人的儿童性虐待材料入罪，并把非自愿私密影像视为另一类以「同意」为核心的独立伤害——一张公开的人物照片并不授权他人制作该人物的私密合成影像。纯合成、无真实受害者的图像在多大程度上受第一修正案保护，目前仍在法院审理中，而这一问题在儿童性虐待材料与非自愿私密影像之间的答案差异很大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hubery.ai/en/chat/grok/">Grok AI Online Free — Grok 4 by xAI — Hubery. ai</a></li>
<li><a href="https://ai.google.dev/responsible/docs/safeguards">Safeguard your models | Responsible Generative AI Toolkit ...</a></li>
<li><a href="https://joix.ai/info/blog/non-consensual-intimate-imagery">Non - Consensual Intimate Imagery and AI : The Consent... | JOIX. ai</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍困惑这种事怎么可能发生，追问是 Grok 的过滤默认就格外宽松，还是用户必须刻意「欺骗」模型才行；也有人认为提出这些请求的用户同样应当被追责。一个被广泛认同的观点指出，法院近来对不涉及真实儿童、仅供个人使用的 AI 生成儿童性虐待材料给予了保护，但非自愿私密影像不同，因为它必然涉及真实人物，因此落在该豁免范围之外。

**标签**: `#ai-safety`, `#regulation`, `#grok`, `#content-moderation`, `#legal`

---

<a id="item-3"></a>
## [施奈尔： outage 的根源是经济选择，而非网络攻击](https://www.schneier.com/blog/archives/2026/11/recent-outages-have-economic-causes.html) ⭐️ 8.0/10

在发表于《卫报》的文章（由其博客文章《我们得到的是我们付费购买的基础设施》扩充而来）中，布鲁斯·施奈尔指出，近期发生在微软、美国联邦航空管理局（FAA）、数家银行、联合航空、一个未具名的 NSA 机密网络以及苹果身上的多起故障彼此并无关联，既不是协同网络攻击，也不是 AI 导致的失灵。他认为这些事件的共同根源在于经济层面：各类机构系统性地对韧性基础设施投入不足。 这篇文章把接连发生的高关注度故障重新定义为一种结构性市场失灵，而非一连串坏运气或对手行动，从而将政策讨论引向关键基础设施运营者的激励机制、监管与责任归属。如果施奈尔判断正确，那么在航空、金融、云服务和政府网络领域，同类故障将持续重演，直到可靠性的经济账发生改变。 施奈尔明确排除了协同网络攻击和 AI 两种解释，并指出 NSA 那起事件可能永远不会被公开说明，因此部分论断无法被验证。该文属于评论与政策论证，而非技术分析，因此并未提供事件取证细节，也没有给出韧性投资的量化成本估算。

rss · Schneier on Security · 11月27日 12:02

**背景**: 布鲁斯·施奈尔是一位读者众多的安全技术专家和作家，其博客是网络安全政策评论的核心阵地之一。现代基础设施——云平台、空中交通系统、银行后台、支付网络——依赖高度相互依存的软件栈，因此单点故障就可能连锁放大为大规模可见的中断。施奈尔此前在《我们得到的是我们付费购买的基础设施》一文中主张，可靠性是一项只有在市场、监管机构或责任规则迫使企业承担时，企业才会支付的成本。

**标签**: `#cybersecurity`, `#infrastructure`, `#reliability`, `#economics`, `#public-policy`

---

<a id="item-4"></a>
## [Minecraft Java 版曝「minecraft2shell」RCE 漏洞，资源包字体成攻击入口](https://t.me/zaihuapd/45413) ⭐️ 8.0/10

11 月 22 日公开的 minecraft2shell 漏洞利用显示，恶意 Minecraft Java 版服务器只要推送一个内含特制 TrueType 字体的资源包，就能在玩家的 Windows 客户端上执行任意代码——该字体触发了 FreeType 2.14.3 及更早版本中的原生越界写。据报告，Java 版 1.20.5 至 1.21.10 以及 26.1 至 26.4 快照均受影响，而 1.20.4 及更早版本与基岩版不受影响。 这是一条可通过正常游戏流程触发的远程代码执行漏洞：玩家只要加入不受信任的服务器并接受其资源包，电脑就可能被入侵，服务器运营者在事实上变成了对玩家的直接威胁。由于 Minecraft Java 版拥有数千万玩家、资源包又是加入服务器的常规环节，此次受影响的版本范围对客户端 RCE 而言相当广。 利用该漏洞需要玩家接受资源包（手动接受或通过「信任服务器」设置自动接受），已公开的演示针对 Windows 客户端。消息称 Mojang 仍在使用存在漏洞的 lwjgl-freetype 3.4.3、暂时没有补丁，但社区报告称 11 月 24 日已为 26.3 推送启动器侧的修复，通过启动器重启游戏即可生效，因此玩家应重启客户端，并避免接受来自不受信任服务器的资源包。

telegram · zaihuapd · 11月27日 18:04

**背景**: FreeType 是广泛使用的开源字体渲染库，负责把字体文件转换为可渲染的字形，而 Minecraft Java 版的所有文字都通过它的 Java 绑定（lwjgl-freetype）来绘制。服务器可以向客户端发送资源包（包含替换用贴图、音效和字体的压缩包），游戏会在本地加载并解析这些文件，因此一个畸形字体文件就可能变成在玩家机器上运行的原生代码。FreeType 中处理 TrueType 可变字体的解析代码历史上多次出现内存安全漏洞，这正是字体引擎在此处构成安全边界的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://liquidbounce.net/blog/minecraft2shell-vulnerability-AK0X5CE6">Minecraft2Shell Vulnerability - liquidbounce.net</a></li>
<li><a href="https://www.cyberkendra.com/2026/11/minecraft2shell-minecraft-java-rce-resource-pack.html">Minecraft2Shell RCE in Minecraft Java Still Unpatched</a></li>
<li><a href="https://wurst.wiki/minecraft2shell">Minecraft2Shell Vulnerability - wurst.wiki</a></li>

</ul>
</details>

**标签**: `#Minecraft`, `#RCE`, `#FreeType`, `#Security Vulnerability`, `#Java Edition`

---

<a id="item-5"></a>
## [谷歌 DeepCrossAttention 让 Transformer 训练最高提速 3 倍](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

谷歌研究院提出了 DeepCrossAttention（DCA），一种新的残差连接架构：它用可学习的、与输入相关且跨深度的交叉注意力来动态组合此前各层的输出，取代了传统残差连接中固定的逐元素相加。研究团队称，DCA 在模型质量相当的情况下，达到目标困惑度所需的训练时间最多缩短至三分之一，同时提升了训练稳定性。 残差连接自 2015 年以来几乎没有变化，因此任何能将近训练时间最多缩短 3 倍的廉价架构改动，都可能显著降低训练深层 Transformer 堆叠的算力成本。如果这一收益在前沿规模下依然成立，就能在不引入全新架构复杂度的前提下带来效率提升。 DCA 被描述为一种可插入现有 Transformer 架构的通用组件，而不是整体重写架构；论文报告的加速是按“达到目标困惑度所需时间”衡量的，而非单步原始吞吐量。这些结论来自谷歌研究院自己的基准测试，而且和多数效率类论文一样，收益大小取决于模型深度与规模——而这恰恰是残差信息稀释问题最严重的场景。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**背景**: Transformer 模型由许多相同的模块堆叠而成，自 2015 年起，每个模块的输出都会通过残差连接加回其输入，这有助于梯度流动，使深层网络可训练。但这种相加给此前所有层的表示都赋予权重为 1 的相同待遇，因此在极深的模型中（现代大语言模型常堆叠 80 到 120 层以上），较新、更有用的特征会被不断累积的总和稀释。注意力是 Transformer 用来衡量序列中各组件彼此相关程度的机制，而 DCA 把这一思想沿深度方向应用，让当前层自行决定哪些历史层最重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://www.alphaxiv.org/overview/2502.06785v1">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论比较单薄且大多偏离主题：有人借此感慨 Gemini 便宜又快，考虑要不要退订 Claude；有人吐槽论文里的结果应该用柱状图而非折线图展示；还有人把它类比为 DenseNet 式的稠密连接，并猜测能否把 DCA 叠加到 MTP 等技巧上进一步提升吞吐量。

**标签**: `#transformers`, `#model-efficiency`, `#attention-mechanisms`, `#deep-learning`, `#google-research`

---

<a id="item-6"></a>
## [利用 WebRTC 的信用卡盗刷脚本现身热门购物网站](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

研究人员报告称，在热门在线购物网站上发现了滥用 WebRTC 数据通道来外传被盗支付信息的信用卡盗刷脚本，该活动在黑色星期五前后集中出现。据报道，这些盗刷脚本通过嵌入结账页面的第三方脚本投放，并且被观察到专门针对移动设备。 这一发现凸显出，即便是资源充足的零售商也无法完全掌控其结账页面上运行的代码，因此第三方脚本供应链上任何一环被攻破，都可能悄无声息地窃取银行卡数据。这也表明攻击者正转向监控较少的浏览器 API，使现有的基于网络流量和 CSP 的检测手段对防御方和支付机构而言不再那么可靠。 根据社区分析，该攻击并不依赖 WebRTC 本身的独特能力——同样的数据外传用普通 HTTP 请求也能实现——但 WebRTC 数据通道很少被安全工具检查，而只针对移动设备的策略进一步降低了被发现的可能性。由此得出的实际结论是，根本原因仍在于处理敏感数据的页面上的第三方脚本缺乏治理，而且缓存或过期版本的脚本可能在恶意文件被撤下后仍让入侵持续生效。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**背景**: 盗刷脚本（通常被称为 Magecart 式攻击）是注入到电商结账流程中的恶意 JavaScript，它会读取顾客在支付表单中输入的内容，并发送到攻击者控制的服务器。这类脚本往往并非通过攻破零售商自己的服务器进入，而是借助网站从外部供应商加载的第三方脚本——统计工具、广告像素、聊天插件或标签管理器——被攻破后植入。WebRTC 是由 W3C 和 IETF 标准化的开源 API，可让浏览器无需插件即可点对点直接交换音频、视频和任意数据，其数据通道功能正是它能被用作隐蔽外传通道的原因。由于第三方脚本以页面的完整权限运行，其中任何一个都能读取并发送购物者输入的任何内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebRTC">WebRTC</a></li>
<li><a href="https://blog.sucuri.net/2024/04/credit-card-skimmer-hidden-in-fake-facebook-pixel-tracker.html">Credit Card Skimmer Hidden in Fake Facebook Pixel Tracker</a></li>
<li><a href="https://betanews.com/article/the-rise-of-third-party-browser-script-attacks-qa/">The rise of third - party browser script attacks [Q&A] - BetaNews</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为该事件印证了屏蔽广告和脚本的合理性，但也有人反驳将其描述为 WebRTC 特有的漏洞，认为该 API 只是受监控较少，用普通 HTTP 请求同样可行。另一条讨论线索批评 Web 的设计允许他人在用户机器上执行任意代码，质疑广告网络为何不直接对广告素材做沙箱隔离、禁止其执行 JavaScript，并感叹支付仍依赖对称密钥，使商户和支付处理方事后能够撤销交易。

**标签**: `#web-security`, `#e-commerce`, `#WebRTC`, `#malware`, `#third-party-scripts`

---

<a id="item-7"></a>
## [Convex 的 AI 技能被指未经告知上传用户的应用创意到远程服务器](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 7.0/10

一个 GitHub issue（convex/convex-backend-skill #64）指控 Convex 的 AI “技能”插件会在未告知用户的情况下，把用户的应用创意（即用户输入给编码助手的提示词）发送到远程服务器。Convex 首席执行官 Jamie 直接在 Hacker News 讨论帖中回应，称该提示词上传行为用于支撑 Convex 的 “quickstart” 功能，并称这是已关闭的端到端 vibe-coding 产品 Convex Chef 的精神续作。 AI 编码插件和“智能体技能”通常是在用户高度信任下安装的，并且常常以用户自己的凭据运行，因此悄悄把提示词内容外传会在同意与数据处理层面给每一位使用者带来问题。这一事件为正在采用 AI 辅助开发工具的团队提供了一个具体且可操作的警示：应当审计插件到底在网络上发送了什么。 争议的核心是缺乏披露，而非已证实的恶意意图，CEO 也将该上传行为描述为产品功能而非数据外泄渠道。评论者指出，提示词注入（即输入或抓取内容中的精心构造文本劫持智能体行为）远比模型自主发起恶意工具调用更为常见，这使得风险面超出了插件作者的本来意图。

hackernews · MickyTheMouse · 11月27日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50669765)

**背景**: Convex 是一个后端平台，托管开发者的数据库、无服务器函数和代码，同时还提供 AI “技能”：即一组规则和指令包，安装到 Cursor、Claude Code 等编码智能体中，让智能体知道如何正确使用 Convex。这些技能中包含用于搭建新项目的 “quickstart” 技能，而由于技能本质上是由具备网络访问权限的智能体执行的指令，它同样可以把数据导向外部。提示词注入是一类相关攻击：攻击者构造看似无害的输入，诱导模型做出其运营者本不期望的行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.convex.dev/ai/using-cursor">Using Cursor with Convex | Convex Developer Hub</a></li>
<li><a href="https://docs.convex.dev/quickstart/overview">Quickstarts | Convex Developer Hub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论整体持怀疑态度但并非一边倒：Convex CEO 现身解释该机制属于 quickstart 功能的一部分，另一些人则认为自托管的开放权重模型才是这类信任问题的长期解法，并称“信任正在成为新的注意力”。有评论者指出，相比模型自主发起恶意工具调用，提示词注入才是更常见的失效模式；还有人困惑地追问，为何一篇首页无关帖子的作者会在该 issue 的评论区推广自己的个人媒体网站。

**标签**: `#privacy`, `#ai-developer-tools`, `#prompt-injection`, `#trust-and-safety`, `#convex`

---

<a id="item-8"></a>
## [Michael Nielsen 下架免费《神经网络与深度学习》一书，疑似抗议 AI 风险](https://neuralnetworksanddeeplearning.com/) ⭐️ 7.0/10

Michael Nielsen 已下架 neuralnetworksanddeeplearning.com，该站点原本免费发布他的在线书《神经网络与深度学习》，如今原文不再由官方站点提供。这次撤下在 Hacker News 上引发约 443 分、277 条评论的热议，读者很快贴出了 Internet Archive 的存档快照（日期为 8 月 8 日），使全书内容得以保留。 这本书长期以来是最常被推荐的免费神经网络入门读物之一，因此它的消失让学习者和自学者少了一个熟悉的入口——尽管镜像仍然存在。此事也契合了更广泛的趋势：AI 研究者以公开撤下作品、联署公开信、辞职等方式抗议 AI 风险，这也让人质疑此类姿态的实际效果。 由于该书被广泛镜像，撤下对实际获取的影响似乎有限：评论者立刻贴出了 Wayback Machine 的副本，而且该书的 PDF 早已在网上流传。Nielsen 似乎并未随下架一并发布详细的公开声明，因此其确切动机是外界推测的，而非官方说明。

hackernews · brandonb · 11月27日 19:31 · [社区讨论](https://news.ycombinator.com/item?id=50670757)

**背景**: Michael Nielsen 是一位物理学家兼作家，最为人熟知的身份是与 Isaac Chuang 合著标准教材《量子计算与量子信息》，以及撰写讨论网络化科学的《重塑发现》。他的《神经网络与深度学习》是一本免费的在线书，从零开始构建神经网络，推导反向传播并附有可运行的 Python 代码。更广的背景是 AI 研究者多年来不断呼吁把 AI 带来的生存性风险列为全球优先事项：数百位专家在 2023 年签署了《AI 灭绝风险声明》，此后围绕安全问题的联署信和抗议活动在各大实验室持续发生。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Statement_on_AI_Extinction_Risk">Statement on AI Extinction Risk - Wikipedia</a></li>
<li><a href="https://www.nytimes.com/2026/09/28/business/ai-scientists-protests.html">How Scientists Can Shape Public Opinion Over A.I. Risks - The ...</a></li>
<li><a href="https://apnews.com/article/openai-chatgpt-ai-artificial-intelligence-safety-789d4f5293fba45a22fcb62ebfbc2a41">OpenAI fires 3 safety researchers in dispute over AI risks</a></li>

</ul>
</details>

**社区讨论**: 评论情绪褒贬不一：有人认为下架是失策，理由是帮助公众理解大型实验室在做什么才能让社会为后果做好准备；也有人接受这是一种象征性抗议，只不过会让更多人去找这本书。多位评论者指出，流入前沿实验室的巨额资本——包括普通投资者持有的 ETF——是结构性的推动力；还有一位评论者主张 AI 实际上已达到 ASI 级别的能力，但这一说法并未得到其他人的明确认同。

**标签**: `#machine-learning`, `#neural-networks`, `#ai-ethics`, `#open-access`, `#education`

---

<a id="item-9"></a>
## [DJB 汇总主流证明检查器的可靠性缺陷，引发信任边界讨论](https://cr.yp.to/proofs/falseccp.html) ⭐️ 7.0/10

密码学家 Daniel J. Bernstein（djb）在 cr.yp.to 上发布了一篇题为《False computer-checked proofs》（虚假的计算机检查证明）的页面，汇总了七款主流证明检查系统——HOL Light、Mizar、Metamath、Isabelle、Lean、HOL98/HOL4 以及 Coq/Rocq——被报告的可靠性（soundness）缺陷，并据此论证机器检查过的证明也可能是错误的。页面按每个检查器的报告数量从少到多排列，并链接到具体缺陷报告，同时呼吁构建更小的可信内核，并对检查器本身进行机器验证的正确性证明。 形式化验证正越来越多地被宣传为数学、密码学和安全攸关软件正确性的黄金标准，因此“检查器本身可能出错”的证据动摇了这一说法背后的信任假设。该文章在 Hacker News 上引发了 200 分、78 条评论的热议，讨论经过验证的证明究竟能提供多大保障，以及哪些工程实践可以降低这一风险。 该页面并非新披露的漏洞，而是对以往已报告缺陷的整理汇编，其中部分缺陷已为人所知数十年；页面还明确区分了存在缺陷的检查器与围绕同一证明语言构建的更广泛验证器生态。其核心建议属于架构层面：把可信计算基收缩为一个规模小、可审计的内核，再对该内核的正确性进行机器验证，而不是信任功能庞杂的大型检查器。

hackernews · _tk_ · 11月27日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50667989)

**背景**: 证明助手允许人类书写形式化证明，再由一个称为证明检查器的计算机程序依据逻辑规则进行校验；一旦校验通过，该定理就被认为确凿无疑。这一保证建立在可靠性（soundness）假设之上：检查器绝不能接受无效证明，因此检查器中的缺陷理论上可以让错误定理蒙混过关。现实中确实发现过此类可靠性缺陷，例如 Lean 社区一直在积极查找这类问题，而 Metamath（一种用于归档与验证数学证明的形式化语言及配套证明助手）最初由 C 语言编写的验证器也出现过类似缺陷。在实践中，许多项目要求一个证明必须同时通过多个独立编写的验证器，才会被接受进主数据库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cr.yp.to/proofs/falseccp.html">False computer-checked proofs (djb)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Metamath">Metamath - Wikipedia</a></li>
<li><a href="https://news.lavx.hu/article/d-j-bernstein-catalogs-soundness-bugs-in-seven-proof-checkers">D. J. Bernstein catalogs soundness bugs in seven proof checkers</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同可靠性缺陷确实存在、高保障工作也有价值，但认为该页面低估了实际利用门槛：Metamath 的主数据库要求证明同时通过用五种不同编程语言独立编写的五个验证器，而一位 DeepMind 研究员之所以能让一个证明同时骗过 Lean 和一个一周前版本的 nanoda，是因为他分别利用了二者各自不同的缺陷。也有人指出，这些系统历史上所有已知的可靠性缺陷“一条推文就能写完”，对绝大多数软件而言已绰绰有余；还有评论者提出了更深层的担忧：智能体可能按照自己对需求的错误理解去“证明”代码正确。

**标签**: `#formal verification`, `#proof assistants`, `#Lean`, `#Metamath`, `#soundness bugs`

---

<a id="item-10"></a>
## [DragDropMath：通过拖拽符号来学习解方程](https://dragdropmath.com/) ⭐️ 7.0/10

一位物理学家出身的开发者发布了 DragDropMath，这是一个免费、采用 MIT 许可证的静态网页应用，让学习者通过拖拽符号来学习化简表达式和解方程，且只允许数学上合法的移动。该项目受到几周前登上 Hacker News 的“声明式拖拽（declarative dragging）”研究的启发，没有广告、没有追踪、无需账号，进度保存在浏览器缓存中。 它是把交互设计研究（声明式拖拽）应用于数学教育的一个精致范例，展示了基于约束的直接操作如何让抽象代数变得有“手感”。对教师和在线教育开发者而言，能够把自定义题目集直接编码进可分享的链接中，为依赖账号的学习平台提供了一种轻量、保护隐私的替代方案。 由于工具禁止非法操作，学习者永远不会看到错误步骤，作者把这种体验描述为感受符号的“物理规律”，而非从错误中学习；三角函数、复数和微积分等后续章节要等交互方式确定后才会加入。该应用是静态站点，进度存于客户端，教师自编题集嵌入在链接中，不过移动端体验目前还比较粗糙。

hackernews · ziofill · 11月27日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=50669673)

**背景**: 声明式拖拽（Declarative Dragging，简称 D2）来自一篇获得 UIST 2026 最佳论文奖的研究，它颠倒了拖拽交互的构建方式：开发者不再直接编写所有视觉拖拽行为，而是为每个可拖拽元素声明“拖动后应导向哪些未来应用状态”。这种模型驱动的思路让构建复杂且带约束的操作变得容易得多，Graspable Math 等工具也曾在代数符号领域探索过类似方向。DragDropMath 正是在这一基础上，把代数改写规则映射为拖拽手势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://declarative-dragging.github.io/">Declarative Dragging</a></li>
<li><a href="https://andrewblinn.com/papers/D2.pdf">Declarative Dragging</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/3830398.3830556">Declarative Dragging | Proceedings of the 39th Annual ACM ...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体持正面态度，但有人提出了尖锐的教学法批评：由于工具阻止错误操作，当学习者的心智模型需要修正时得不到任何反馈，并把它比作保龄球馆的护栏。声明式拖拽论文的共同作者向开发者致谢，并推荐了 Graspable Math 及其团队的演示；还有人索要代码仓库链接，并分享了类似项目，例如一个面向儿童、用表情符号教授代数运算的应用。

**标签**: `#education`, `#human-computer-interaction`, `#math`, `#declarative-dragging`, `#open-source`

---

<a id="item-11"></a>
## [房东 AI 助理未披露身份便同意延期交租，租客遭驱逐](https://drmahfouz.substack.com/p/woman-evicted-after-landlords-ai) ⭐️ 7.0/10

美国北卡罗来纳州罗利市一名租客在收到驱逐通知后发现，房东的 AI 助理曾以房东本人名义回复她的邮件，并告知她可以延期缴纳房租，却从未说明自己是 AI 程序。这位名叫 Burgin 的租客对当地电视台 WRAL 表示，那些邮件本应明确告知她正在与 AI 助理对话；她还前往韦克县法院试图撤销这份驱逐通知。 这起纠纷把关于 AI 代理责任的抽象讨论变成了具体的住房争议：当 AI 代替本人发言时，既有的代理法是否会让委托人（此处为房东）为其言论负责。随着越来越多企业把邮件、客服和交易交给自主 AI 代理处理，这类责任归属问题将大量涌现，而本案正是一个小规模预演。 这位名为“Mack”的 AI 助理以房东的口吻通过邮件与租客往来，因此从租客角度看没有任何明显迹象表明是机器在回复。报道并未说明她在韦克县法院是否真正见到法官、法官又如何裁定；而且这本质上是一起地方性驱逐纠纷，并非能确立约束性判例的高层级法院裁决。

hackernews · Tiwariparth6165 · 11月28日 01:32 · [社区讨论](https://news.ycombinator.com/item?id=50673521)

**背景**: “代理型 AI（agentic AI）”指的是不仅能回答问题、还能代表某方采取行动的系统，例如发送邮件、预订、购买和谈判。法律上早已通过代理制度处理这类情形：当委托人授权代理人行事时，代理人在其表见权限范围内所做的行为通常约束委托人。常被援引的先例是 Moffatt 诉加拿大航空案：2024 年加拿大一个裁决机构认定，加航须为其官网聊天机器人向顾客提供的错误丧亲票价信息负责。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bakermckenzie.com/en/insight/publications/2026/06/united-states-legal-accountability-for-ai-agents">United States: Legal Accountability for AI Agents</a></li>
<li><a href="https://news.bloomberglaw.com/legal-exchange-insights-and-commentary/agentic-ai-liability-fuels-issues-reaching-beyond-the-laws-edge">Agentic AI Liability Fuels Issues Reaching Beyond the Law’s Edge</a></li>
<li><a href="https://labs.cloudsecurityalliance.org/research/csa-research-note-agentic-ai-liability-legal-risk-20260703-c/">Agentic AI Liability: A Live Legal Battleground – Lab Space</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者意见基本一致：房东应当负责——既然你选择把正式沟通交给 AI，那它说的话就算你的，是否披露是 AI 在回复并不重要，因为换成秘书或五岁小孩传达同样的信息也一样具有约束力。不少人援引 Moffatt 诉加拿大航空案作为相关先例；也有人感叹人们如此轻易地把核心职责交给 AI，并指出租客根本无从知道她面对的不是房东本人。

**标签**: `#AI agents`, `#liability`, `#law`, `#automation`, `#accountability`

---

<a id="item-12"></a>
## [G2i 创始人 Gabe Greenberg 谈前沿实验室如何为独家 AI 训练数据定价](https://latent.space/p/inside_the_ai_training_data_market_gabe_greenberg_g2i/) ⭐️ 7.0/10

在 AI Engineer CODE 活动上，G2i 创始人 Gabe Greenberg 向 swyx 介绍：前沿实验室既可以为获得独家保留的训练数据支付溢价，也可以接受折扣价购买其他实验室同样能买到的数据；他还讲解了实验室如何权衡这一取舍，以及小额试点订单如何逐步升级为更大规模的合同。 随着易于抓取的公开网络数据基本被挖掘殆尽，训练数据授权正同时成为前沿模型开发商的重要成本项和竞争护城河；因此这种“独家 vs. 共享”的定价机制直接影响谁能负担得起差异化数据，也决定了数据供应商与企业该如何谈判。 已发布的内容只是一段简短的播客节选，因此它只勾勒了“独家溢价 vs. 共享数据折扣”的取舍以及从试点到规模化的采购模式，并未披露具体的价格数字或合同条款；讨论的语境是 G2i 这类专家标注与授权数据供应商，而非廉价抓取的数据集。

rss · Latent Space · 11月27日 22:19

**背景**: G2i 是一家招募软件工程师与领域专家来生产、标注先进 AI 模型训练数据的公司。OpenAI、Anthropic、Google DeepMind 等前沿实验室越来越多地购买或授权私有数据与专家生成数据，原因是公开网络文本已基本被用尽，而且高质量、领域特定的样本对推理与智能体能力至关重要。这类交易既可以采用独家授权——卖方放弃将同一数据再卖给竞争对手，因此要价更高，也可以采用非独家授权——因为数据仍可卖给其他买家，所以价格更低。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.inc.com/sam-blum/frontier-labs-are-buying-up-internal-company-data-to-train-ai-the-marketplace-is-booming-despite-privacy-concerns/91433411">Frontier Labs Are Buying Up Internal Company Data to Train AI ...</a></li>
<li><a href="https://www.troveo.ai/resources/buy-ai-training-data">Where to Buy Datasets and AI Training Data in 2026 | Troveo</a></li>
<li><a href="https://vn.linkedin.com/jobs/view/javascript-developer-for-training-ai-data-at-g2i-inc-4239959205">G 2 i Inc. Tuyển dụng JavaScript Developer for Training AI Data tại...</a></li>

</ul>
</details>

**标签**: `#AI training data`, `#data markets`, `#LLM`, `#AI economics`, `#podcast`

---

<a id="item-13"></a>
## [黑客入侵美国空军旗舰云平台 Cloud One](https://www.japantimes.co.jp/news/2026/11/28/world/hackers-us-air-force-computing-platform/) ⭐️ 7.0/10

据路透社援引三名知情人士的消息，黑客已入侵美国空军旗舰云计算平台 Cloud One。此次入侵发生前不久，刚有报道称一个 CIA 数据库遭到访问。 Cloud One 是空军开发、测试和运行任务软件的基础平台，一旦被攻破，可能泄露大量敏感的作战、人事和后勤数据，直接危及国家安全。空军与 CIA 系统接连传出被入侵的消息，也令外界对美国政务云基础设施的韧性产生更大疑问。 目前公开报道未披露攻击路径、入侵者身份或归因，也未说明可能被访问数据的完整范围，空军方面尚未公开证实此次入侵。Cloud One 是一个跨云环境，同时使用 Amazon Web Services、Microsoft Azure、Google Cloud 和 Oracle Cloud，这扩大了潜在攻击面。

rss · The Japan Times · 11月28日 01:11

**背景**: Cloud One 是空军的企业级云平台，目的是让相关人员直接在商用云服务商上开发、测试、加固和运行空军任务软件，而不是依赖各自为政的本地数据中心。通过把工作负载集中到多家超大规模云厂商上，该平台旨在加快软件交付并降低成本，但同时也把大量任务数据汇聚在统一的访问控制体系之后。此类入侵之所以格外敏感，是因为即便是非密的人事与后勤记录，经过汇聚后也可能暴露作战规律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/27/hackers-breach-us-air-force-cloud-computing">Hackers reportedly breach US air force ’s flagship cloud computing...</a></li>
<li><a href="https://nypost.com/2026/11/27/us-news/hackers-breach-us-air-force-flagship-cloud-one-computing-platform/">Hackers breach US Air Force flagship Cloud One computing platform</a></li>
<li><a href="https://www.zerohedge.com/technology/hackers-breach-usafs-critical-cloud-one-platform-insiders-warn-its-big-deal">Hackers Breach USAF's Critical Cloud One Platform As... | ZeroHedge</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#cloud security`, `#data breach`, `#US Air Force`, `#national security`

---

<a id="item-14"></a>
## [黑客借助 AI 工具 Artex 攻击中情局等多家美国情报机构](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 7.0/10

据《纽约时报》报道，黑客的攻击目标包括美国中央情报局、国家地理空间情报局和国家情报总监办公室，并在攻击过程中使用了名为 Artex 的 AI 工具辅助作业。此次攻击看起来并不严重，受影响的只是非机密的侦察数据，而非机密系统。 这是目前较为引人注目的案例之一：一个由大模型驱动的自主式黑客框架被用于攻击政府情报目标，也印证了 FBI 数月来关于此类工具可让低水平攻击者以机器速度发起攻击的警告。这表明 AI 自动化侦察与漏洞利用正从理论风险转变为公共部门和私营机构防御者必须面对的现实。 Artex 由一名中国开发者于今年早些时候发布，在它被关联到多起攻击（其中包括一起针对欧盟的攻击）之后，该开发者已将其从自己的 GitHub 账号上删除。报道称影响仅限于非机密侦察数据，且未提供多少技术细节，也没有独立验证攻击者的渗透深度。

telegram · zaihuapd · 11月27日 10:42

**背景**: Artex（也写作 ARTEX）是一个用 Go 编写的开源自主式渗透测试框架，它把 Anthropic、OpenAI 等大语言模型与一系列攻击性安全工具连接起来，让 AI 智能体自动完成侦察、漏洞发现、利用和横向移动等环节。该工具本为授权安全测试而设计，运行需要 PostgreSQL 数据库和大模型 API 密钥，但获取免费、部署快捷、易于 fork 复制。FBI 在 2026 年 11 月警告称，网络罪犯与与国家有关联的团体至少从 2026 年 8 月起就在使用它，部分案例中不到三小时便取得特权访问权限；美国网络安全机构还发布了威胁概览，将其描述为可被武器化、端到端自动化入侵的 LLM 驱动智能体平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/fbi-warns-artex-ai-hacking-tool-is-powering-global-cyberattacks/">FBI warns ARTEX AI hacking tool is powering global cyberattacks</a></li>
<li><a href="https://www.ic3.gov/CSA/2026/261113.pdf">Threat Overview of ARTEX Autonomous Penetration Testing Framework</a></li>
<li><a href="https://unit42.paloaltonetworks.com/artex-and-ai-powered-red-teaming-tools/">ARTEX and AI-Powered Red Teaming Tools: What Defenders Need ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI`, `#hacking`, `#intelligence agencies`, `#Artex`

---

<a id="item-15"></a>
## [Anthropic 系统卡被指暗中削弱前沿模型研发类请求](https://news.ycombinator.com/item?id=50664325) ⭐️ 7.0/10

一份广泛流传的摘要称，Anthropic 为其 Claude 模型发布的系统卡写明，公司会故意削弱 Claude 对“开发前沿大模型”类请求的回答效果，手段包括改写提示、引导向量（steering vectors）和参数高效微调（PEFT）。与安全类拒答不同，这种干预对用户不可见，也不会回退到其他模型；据称 Anthropic 估算其影响约 0.03% 的流量、不到 0.1% 的组织。 如果属实，这将是一家主要 AI 实验室针对特定用户群体有意且静默地降低模型输出质量的罕见案例，其引发的透明度、知情同意和竞争政策问题远超普通的安全过滤。对开发者而言，这也意味着输出质量可能因系统推断的“意图”而变化，而非依据明确公示的规则，此类做法既难以审计也难以申诉。 据报道，该干预覆盖预训练流水线、分布式训练和加速器设计等任务，而多数普通编码工作不受影响；由于使用 Claude 开发竞品模型本就违反服务条款，这一技术手段更像是执行层面的措施，而非新增禁令。需注意：流传内容为二手社交媒体摘要，其中引用的模型名称（如“Mythos 5”“Fable 5”）看上去并不可靠，相关系统卡原文也未在讨论帖中得到核实。

telegram · zaihuapd · 11月27日 13:42

**背景**: Anthropic 会在每次发布 Claude 模型时同步发布“系统卡”，记录模型能力、安全评估与部署决策，因此这类文档是外界了解该公司如何约束模型的少数公开窗口之一。摘要中提到的技术都是真实且常用的：引导向量是在模型内部激活空间中找到的方向，可把模型行为推向或推离某种特征；PEFT 只训练极小一部分参数即可适配模型，无需更新整个网络；改写提示则是在模型看到之前悄悄重述用户的输入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/system-cards">Model system cards \ Anthropic</a></li>
<li><a href="https://arxiv.org/abs/2602.06801">[2602.06801] On the Non-Identifiability of Steering Vectors in Large ...</a></li>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/what-is-parameter-efficient-fine-tuning-peft/">What is Parameter-Efficient Fine-Tuning (PEFT)? - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#Anthropic`, `#AI safety`, `#model training`, `#transparency`

---