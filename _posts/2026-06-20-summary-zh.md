---
layout: default
title: "Horizon Summary: 2026-06-20 (ZH)"
date: 2026-06-20
lang: zh
---

> 从 140 条内容中筛选出 26 条重要资讯。

---

1. [Project Valhalla 登陆 JDK 28，引入值类型](#item-1) ⭐️ 9.0/10
2. [Squidbleed：所有版本 Squid 代理存在 Heartbleed 式内存泄漏](#item-2) ⭐️ 9.0/10
3. [ATProto 没有实例，不同于 Mastodon](#item-3) ⭐️ 8.0/10
4. [EFF 认为法院记录应当免费](#item-4) ⭐️ 8.0/10
5. [美国政府将 Anthropic 的 Fable AI 归类为武器](#item-5) ⭐️ 8.0/10
6. [GLM-5.2 通过社区评价测试，开源模型崭露头角](#item-6) ⭐️ 8.0/10
7. [nginx HTTP/3 QPACK 编码器中的释放后重用漏洞 (CVE-2026-42530)](#item-7) ⭐️ 8.0/10
8. [OpenBSD MPLS 内核栈泄漏漏洞(CVE-2026-56099)](#item-8) ⭐️ 8.0/10
9. [智谱创始人称模型或可在 2027 年第一季度前达到 Mythos 级别](#item-9) ⭐️ 8.0/10
10. [多品牌婴儿纸尿裤检出有毒甲酰胺](#item-10) ⭐️ 8.0/10
11. [ProPublica 揭露 SpaceX 在 IPO 前向中国投资者出售股份](#item-11) ⭐️ 8.0/10
12. [科技巨头在 AI 上的支出将两倍于美国国防预算](#item-12) ⭐️ 8.0/10
13. [AWS Graviton5 正式发布，为智能体 AI 提升 25%性能](#item-13) ⭐️ 8.0/10
14. [谷歌 Gemini 联合负责人 Noam Shazeer 加入 OpenAI](#item-14) ⭐️ 8.0/10
15. [ASML 因对华 EUV 出口面临美国新审查](#item-15) ⭐️ 8.0/10
16. [《毁灭战士》与《德军总部》作曲家鲍比·普林斯去世](#item-16) ⭐️ 7.0/10
17. [Google Workspace 可通过管理员设置阻止 Firefox](#item-17) ⭐️ 7.0/10
18. [两党新法案遏制政府施压在线平台删帖](#item-18) ⭐️ 7.0/10
19. [中国就分布式数字身份互通互认规则征求意见](#item-19) ⭐️ 7.0/10
20. [Google 宣布 Android 侧载未验证应用需等待 24 小时](#item-20) ⭐️ 7.0/10
21. [印度为防作弊封锁 Telegram，VPN 使用量激增 150%](#item-21) ⭐️ 7.0/10
22. [苹果同意在巴西开放第三方应用商店](#item-22) ⭐️ 7.0/10
23. [英国总检察长因假消息担忧弃用 X](#item-23) ⭐️ 7.0/10
24. [北航教授被前博士生指控论文造假](#item-24) ⭐️ 7.0/10
25. [谷歌发布新 AI 芯片战略挑战英伟达](#item-25) ⭐️ 7.0/10
26. [智谱股价因 AI 政治风险飙升 33%](#item-26) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Project Valhalla 登陆 JDK 28，引入值类型](https://www.jvm-weekly.com/p/project-valhalla-explained-how-a) ⭐️ 9.0/10

经过十年开发，Project Valhalla 在 JDK 28 中实现了值类型和堆扁平化，使 JVM 能够无需对象头或指针间接地内联存储值对象。 这一演进大幅提升了 Java 应用的内存效率和缓存局部性，减少了垃圾回收压力，使数据密集型工作负载的性能接近手写 C 代码。 堆扁平化将值对象编码为紧凑的位向量直接存储在字段或数组单元中，但仅适用于不超过 64 位的表示；更大的值仍使用间接引用。空安全争论仍在继续，因为值类型强制非空语义。

hackernews · philonoist · 6月19日 06:35 · [社区讨论](https://news.ycombinator.com/item?id=48595511)

**背景**: 传统 Java 对象因对象头和指针间接引用而产生开销，损害小型数据类型的性能。值类型通过允许对象直接存储在栈上或内联于数组中，消除了这种开销，类似于基本类型但具有完整对象语义。由 Brian Goetz 领导的 Project Valhalla 自 2014 年起一直在探索此特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Project_Valhalla_(Java_language)">Project Valhalla (Java language)</a></li>
<li><a href="https://www.jvm-weekly.com/p/project-valhalla-explained-how-a">Project Valhalla, Explained: How a Decade of... - JVM Weekly vol. 180</a></li>
<li><a href="https://inside.java/2025/10/31/jvmls-jep-401/">Value Classes Heap Flattening - What to expect from JEP 401...</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：有人赞赏十年努力和性能优势，也有人批评复杂性，认为空安全模型过于复杂。辩护者指出，自 JDK 8 以来 Java 已显著发展，Valhalla 是向前迈出的重要一步。

**标签**: `#Java`, `#JVM`, `#Project Valhalla`, `#value types`, `#performance`

---

<a id="item-2"></a>
## [Squidbleed：所有版本 Squid 代理存在 Heartbleed 式内存泄漏](https://www.reddit.com/r/netsec/comments/1u9y7yw/squidbleed_cve202647729_heartbleedstyle/) ⭐️ 9.0/10

一个名为 Squidbleed 的新漏洞（CVE-2026-47729）暴露了所有版本 Squid 代理在默认配置下的 Heartbleed 式内存泄漏。 该漏洞至关重要，因为 Squid 代理部署广泛，且其默认配置使数百万安装易受内存内容泄漏的影响，让人想起破坏性的 Heartbleed 漏洞。 该漏洞影响所有版本的 Squid 代理，而不仅仅是旧版本，且无需特殊配置即可利用；它允许攻击者读取内部内存，可能暴露凭证、令牌或其他秘密。

reddit · r/netsec · /u/qwerty0x41 · 6月19日 10:21

**背景**: Heartbleed 是 2014 年 OpenSSL 中的一个漏洞，允许攻击者读取服务器和客户端的内存，导致广泛的凭证窃取。Squid 代理是一个流行的开源缓存 HTTP 代理，全球组织用它来提升网络性能和安全性。Squidbleed 漏洞遵循类似模式，利用内存泄漏从代理的进程内存中提取数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Heartbleed">Heartbleed - Wikipedia</a></li>
<li><a href="https://www.cvedetails.com/vulnerability-list/vendor_id-9950/product_id-17766/Squid-cache-Squid.html">Squid-cache Squid : Security vulnerabilities, CVEs</a></li>
<li><a href="https://megamansec.github.io/Squid-Security-Audit/">Squid Caching Proxy Security Audit: 55 vulnerabilities and 35 0days | Squid-Security-Audit</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#squid proxy`, `#memory leak`, `#CVE`

---

<a id="item-3"></a>
## [ATProto 没有实例，不同于 Mastodon](https://overreacted.io/there-are-no-instances-in-atproto/) ⭐️ 8.0/10

Dan Abramov 发表了一篇博客文章，澄清 ATProto——Bluesky 背后的协议——没有像 Mastodon 那样的“实例”，并用 RSS 类比来解释其模块化架构。 这一澄清消除了 Mastodon 用户中常见的误解，帮助开发者理解 ATProto 独特的去中心化设计，将数据托管、中继和应用视图分离为独立服务。 在 ATProto 中，用户数据存储在个人数据服务器（PDS）中，中继（Relay）聚合数据以供索引，应用视图（AppView）呈现社交信息流；这与 ActivityPub 的整体式实例模型形成对比。

hackernews · danabramov · 6月19日 15:10 · [社区讨论](https://news.ycombinator.com/item?id=48599515)

**背景**: ATProto 是由 Bluesky 开发的去中心化社交协议。与 ActivityPub（Mastodon 所用）不同，后者每个服务器都是一个自包含的实例，ATProto 将职责分离为三种不同的服务：PDS、中继和应用视图。这种模块化旨在提升可扩展性和用户可迁移性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Atproto">Atproto</a></li>
<li><a href="https://en.wikipedia.org/wiki/AT_Protocol">AT Protocol - Wikipedia</a></li>
<li><a href="https://github.com/bluesky-social/atproto">GitHub - bluesky-social/atproto: Social networking technology created by Bluesky · GitHub</a></li>

</ul>
</details>

**社区讨论**: 一些评论者认为，实际上 Bluesky（公司）运行了大部分服务，使得系统事实上是中心化的。其他人欣赏架构上的清晰性，但指出中继（Relay）运行成本高昂，不像 RSS 那样有很多独立的阅读器。

**标签**: `#ATProto`, `#Bluesky`, `#decentralized social`, `#protocol`, `#ActivityPub`

---

<a id="item-4"></a>
## [EFF 认为法院记录应当免费](https://www.eff.org/deeplinks/2026/06/court-records-should-be-free) ⭐️ 8.0/10

电子前沿基金会（EFF）发表文章，主张公众应能免费获取法院记录，批评联邦 PACER 系统的高昂费用以及更贵的州法院系统。 此事重要，因为获取法院记录对法律透明和公共正义至关重要；高昂费用为个人（尤其是自诉人）设置了障碍，并阻碍了公众获取法律信息的自由。 PACER 每页收费 0.10 美元，每份文件上限 3 美元，季度使用费低于 30 美元可免除；但像爱达荷州这样的州系统每页收费高达 10 美元，加剧了访问问题。

hackernews · hn_acker · 6月19日 17:34 · [社区讨论](https://news.ycombinator.com/item?id=48600946)

**背景**: PACER（公共访问法院电子记录）是访问美国联邦法院电子文件的系统。尽管规定上公开，但其按页付费模式被批评为营利性障碍。RECAP 和 CourtListener 等工具通过众包已购文件提供部分免费访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PACER_(law)">PACER (law) - Wikipedia</a></li>
<li><a href="https://pacer.uscourts.gov/">Public Access to Court Electronic Records | PACER: Federal Court Records</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了个人经历，如在爱达荷州法院每页收费 10 美元，并赞扬了 RECAP 等工具共享已购文档。有人指出财务成本是故意的访问障碍，而另一些人预测免费访问可能只对经批准的合作伙伴开放，而非普通公众。

**标签**: `#open access`, `#PACER`, `#legal tech`, `#EFF`, `#public records`

---

<a id="item-5"></a>
## [美国政府将 Anthropic 的 Fable AI 归类为武器](https://www.schneier.com/blog/archives/2026/06/anthropics-fable-and-the-state-of-ai.html) ⭐️ 8.0/10

2026 年 6 月 9 日，Anthropic 发布了其 Fable 生成式 AI 模型，但三天后美国政府将其归类为危险武器，并利用出口管制权力禁止外国人访问，导致 Anthropic 关闭了全球所有用户的访问权限。 这一事件凸显了 AI 能力与政府监管之间日益紧张的关系，表明出口管制等生硬手段可能适得其反，甚至限制国内用户的访问。它还引发了对通过国界控制先进 AI 模型可行性的质疑。 在政府命令下达后，Anthropic 无法区分美国用户和外国用户，因此全球关闭了访问权限。专家认为政府的行动可能无济于事，因为真正的问题是 AI 能力的整体增长趋势，而非某个特定模型。

rss · Schneier on Security · 6月19日 11:03

**背景**: 像 Anthropic 的 Fable 这样的生成式 AI 模型通过大量数据训练，能够生成类似人类的文本和代码。美国政府将此类模型归类为“武器”，使其受到严格的出口管制——这一管制原本针对武器。此举反映了对先进 AI 落入敌手的担忧，但批评者认为这不可行且损害创新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/commentisfree/2026/jun/16/anthropic-fable-ai">The Anthropic ‘Fable’ saga proves: we have opened the AI Pandora’s box. What now? | Nathan E Sanders and Bruce Schneier</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#regulation`, `#export controls`, `#policy`, `#Anthropic`

---

<a id="item-6"></a>
## [GLM-5.2 通过社区评价测试，开源模型崭露头角](https://www.latent.space/p/ainews-glm-gpt-glm-52-passes-vibe) ⭐️ 8.0/10

Z.AI 推出的开源语言模型 GLM-5.2 通过了社区的“印象测试”，在实际应用中表现优异。同时，Z.AI 预测将于 12 月发布“Open Fable”。 这一里程碑表明，开源模型已能与 GPT 等专有前沿模型竞争，可能使先进 AI 的获取更民主化，并加速开源大语言模型在企业与科研中的应用。 GLM-5.2 在 Terminal-Bench 2.1 上取得 81.0 分（GLM-5.1 为 62.0），在 SWE-bench Pro 上取得 62.1 分（GLM-5.1 为 58.4）。它采用 MIT 开源许可，无地域限制，并改进了 MTP 层用于推测解码，使接受长度提升最多 20%。

rss · Latent Space · 6月19日 05:53

**背景**: GLM（通用语言模型）是 Z.AI 开发的一系列开源大语言模型，旨在与专有模型竞争。“印象测试”指社区对模型可用性和输出质量进行的非正式评估。历史上开源模型落后于专有模型，但近期进展正在缩小差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ollama.com/library/glm-5.2">GLM - 5 . 2 is Z.ai’s flagship model for the era of long-horizon tasks.</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/ GLM - 5 . 2 · Hugging Face</a></li>
<li><a href="https://llm-stats.com/models/glm-5.2">GLM - 5 . 2 Benchmarks, Pricing & Context Window</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#open-source`, `#GLM`, `#frontier models`

---

<a id="item-7"></a>
## [nginx HTTP/3 QPACK 编码器中的释放后重用漏洞 (CVE-2026-42530)](https://www.reddit.com/r/netsec/comments/1uab0j6/useafterfree_in_the_qpack_encoder_of_nginx_http3/) ⭐️ 8.0/10

nginx HTTP/3 的 QPACK 编码器中发现了一个释放后重用漏洞，已分配编号 CVE-2026-42530。 由于 nginx 是广泛使用的 Web 服务器，且 HTTP/3 的采用正在增长，此类漏洞可能导致任意代码执行，影响服务器安全。 QPACK 是 HTTP/3 的头部压缩协议，类似于 HTTP/2 的 HPACK。该释放后重用漏洞出现在编码器组件中。

reddit · r/netsec · /u/everping · 6月19日 19:15

**背景**: HTTP/3 使用 QUIC 传输协议和 QPACK 进行头部压缩，以减少队头阻塞。释放后重用是一种内存安全问题，程序在释放内存后仍访问该内存，可能允许攻击者执行任意代码。nginx 的 HTTP/3 实现引入了此漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datatracker.ietf.org/doc/html/rfc9204">RFC 9204 - QPACK : Field Compression for HTTP / 3 | IETF Datatracker</a></li>
<li><a href="https://encyclopedia.kaspersky.com/glossary/use-after-free/">What is Use-After-Free? | Kaspersky IT Encyclopedia</a></li>
<li><a href="https://http.dev/3">HTTP / 3 explained</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#nginx`, `#HTTP/3`, `#CVE`

---

<a id="item-8"></a>
## [OpenBSD MPLS 内核栈泄漏漏洞(CVE-2026-56099)](https://www.reddit.com/r/netsec/comments/1ua20fg/openbsd_mpls_kernel_stack_leaks_remotely/) ⭐️ 8.0/10

精心构造的 MPLS 包可触发 mpls_do_error 函数中的越界读取，通过 ICMP/MPLS 错误响应远程泄露 4 字节内核栈内存。该漏洞编号 CVE-2026-56099，已于 2026 年 6 月 18 日在 OpenBSD-current 中修复。 该漏洞严重，因为允许远程、可重复地从启用 MPLS 的 OpenBSD 系统泄漏内核内存，可能暴露敏感内核数据。尽管每次只泄漏 4 字节，但远程且无需认证的特点使其成为严重的信息泄露风险。 越界读取发生在处理精心构造的 MPLS 包时的 mpls_do_error 函数中，读取相邻内核栈内存的 4 字节。泄露的数据在 ICMP/MPLS 错误响应中返回。该漏洞需要目标系统启用 MPLS。

reddit · r/netsec · /u/Emergency_Stable_923 · 6月19日 13:27

**背景**: MPLS（多协议标签交换）是一种网络技术，使用短路径标签代替长网络地址来路由流量，常用于广域网以实现高效转发和服务质量。越界读取是指程序在读取数据时超出已分配缓冲区边界，可能访问相邻内存。在 C/C++代码中，此类漏洞常因缺少边界检查而出现，常被利用于信息泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/which-tunneling-technology-most-appropriate-choice-5g-monowar-hossain">SR- MPLS : The most appropriate tunneling technology for 5G Transport...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Out-of-bounds_read">Out-of-bounds read</a></li>

</ul>
</details>

**标签**: `#security`, `#openbsd`, `#vulnerability`, `#mpls`, `#kernel`

---

<a id="item-9"></a>
## [智谱创始人称模型或可在 2027 年第一季度前达到 Mythos 级别](https://x.com/jietang/status/2067580270078030088) ⭐️ 8.0/10

智谱 AI 创始人唐杰回应了埃隆·马斯克的评论，声称他们的大语言模型可能比马斯克预测的 2027 年第一季度更早达到 Anthropic 的“Mythos”级别。 这一互动突显了中美之间日益激烈的人工智能竞赛，具体的时间线比较会影响行业预期和投资方向。 用户评估智谱的 GLM-5.2 大约相当于 Claude Opus 4.7-4.8 水平，并预计中国模型可能在 2026 年底达到 Mythos 级别；马斯克回复“Probably Q1”（解读为 2027 年第一季度），而唐杰则反驳说会更快。

telegram · zaihuapd · 6月19日 02:24

**背景**: Claude Mythos 是 Anthropic 开发的用于发现软件漏洞的专业大语言模型，被认为比其 Opus 系列能力更强。智谱 AI 是中国领先的人工智能公司，其 GLM-5.2 模型拥有 100 万 token 的上下文窗口，并已开源。Opus 和 Mythos 层级之间的比较为衡量各 AI 实验室的进展提供了基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/mythos">Claude Mythos \ Anthropic</a></li>
<li><a href="https://models.dev/models/zhipuai/glm-5.2/">GLM-5.2</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos">Claude Mythos - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社交媒体上的讨论聚焦于时间线预测，一些用户同意马斯克的谨慎估计，而另一些用户则支持唐杰的乐观态度，认为中国 AI 进展迅速。同时，关于用户运行评估将 GLM-5.2 与 Claude Opus 进行比较的可靠性也存在争议。

**标签**: `#AI`, `#LLM`, `#China`, `#ZhiPu`, `#model comparison`

---

<a id="item-10"></a>
## [多品牌婴儿纸尿裤检出有毒甲酰胺](https://t.me/zaihuapd/42051) ⭐️ 8.0/10

经济参考报委托的检测报告显示，好奇、碧芭宝贝、Babycare 等品牌婴幼儿纸尿裤中检出生殖毒性物质甲酰胺。部分婴幼儿血液和尿液中亦检出该物质，一名记者穿戴某品牌纸尿裤一夜后血液浓度飙升近一倍。 这一暴露对婴幼儿构成严重健康风险，因为甲酰胺可通过皮肤吸收并在体内蓄积，可能损害生殖系统、肝脏和肾脏。该发现凸显了监管空白——中国纸尿裤国家标准目前未对甲酰胺设限，尽管该物质已在化妆品中禁用。 甲酰胺在欧盟法规中被归类为 1B 类生殖毒性物质，动物实验显示其会降低生育率和幼崽存活率。现行婴儿纸尿裤国标 GB/T 28004.1-2021 未包含甲酰胺检测项目，业内呼吁尽快修订标准。

telegram · zaihuapd · 6月19日 06:05

**背景**: 甲酰胺是一种有机溶剂，广泛用于工业生产如聚合物材料和合成纤维制造。它在纸尿裤生产过程中可能残留在材料中，并通过长期皮肤接触被吸收。虽然中国已在化妆品中禁用甲酰胺，但纸尿裤标准缺乏此类限制，形成了监管不一致，危及婴幼儿健康。专家指出，低剂量长期接触对孕妇和婴幼儿风险尤为突出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.sina.com.cn/c/2026-06-18/doc-inicuyvt6526008.shtml">多个品牌纸尿裤检出毒性物质甲酰胺，“长期蓄积或影响生殖系统和肝肾功能”|经济参考报|婴幼儿|检测|血液|风险_新浪新闻</a></li>
<li><a href="https://www.bjnews.com.cn/detail/1781760045169406.html">多款婴儿 纸 尿 裤 检出 甲 酰 胺 ？ “好奇”等品牌回应， 国 标 尚无 限 值 — 新京报</a></li>
<li><a href="https://www.zhihu.com/question/2050890464476263871">多品牌婴幼儿纸尿裤被检出有毒物质「甲酰胺」，什么是甲酰胺？会对婴幼儿健康有哪些危害？ - 知乎</a></li>

</ul>
</details>

**社区讨论**: 知乎上的评论表达了愤怒和担忧，质疑为何知名品牌中会出现有毒物质。部分用户呼吁加强监管和独立检测。少数品牌代表如 Babycare 声称其送检纸尿裤未检出甲酰胺，引发了关于检测方法和责任归属的讨论。

**标签**: `#health`, `#safety`, `#consumer products`, `#regulation`, `#toxicology`

---

<a id="item-11"></a>
## [ProPublica 揭露 SpaceX 在 IPO 前向中国投资者出售股份](https://www.propublica.org/article/spacex-elon-musk-ipo-foreign-investors-china) ⭐️ 8.0/10

ProPublica 的调查显示，SpaceX 在 2018 年至 2021 年间通过中间商 Tomales Bay Capital 向至少十几位地址位于中国大陆、香港或俄罗斯的投资者出售股份，这与该公司后来在 IPO 中禁止中国和香港投资者的规定相矛盾。 这一披露引发了严重的国家安全和监管合规担忧，因为 SpaceX 是美国敏感军事项目的主要承包商，而这些早期外国投资可能绕过了该公司自己声明的政策。 投资金额从 80 万美元到 4000 万美元不等，投资者包括与中国军工承包商有联系的商界人士以及卡塔尔王室关联实体；股份是通过美国中间商 Tomales Bay Capital 购买的，该中间商承诺提供季度更新和接触 SpaceX 首席财务官的机会。

telegram · zaihuapd · 6月19日 12:00

**背景**: Tomales Bay Capital 是一家全球投资公司，采用集中投资策略投资创新企业。ProPublica 是一家非营利性调查新闻组织，以揭露权力滥用而闻名。SpaceX 由埃隆·马斯克创立，是一家私营航天公司，已成为美国国家安全发射的关键政府承包商。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ProPublica">ProPublica</a></li>
<li><a href="https://www.linkedin.com/company/tomales-bay-capital">Tomales Bay Capital | LinkedIn</a></li>
<li><a href="https://raizer.app/investor/tomales-bay-capital">Tomales Bay Capital – VC Investor Profile & Insights</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#National Security`, `#Foreign Investment`, `#IPO`, `#Compliance`

---

<a id="item-12"></a>
## [科技巨头在 AI 上的支出将两倍于美国国防预算](https://finance.yahoo.com/technology/ai/articles/google-spacex-microsoft-amazon-spend-171902335.html) ⭐️ 8.0/10

包括谷歌、SpaceX、微软和亚马逊在内的主要科技公司预计将在人工智能上投入相当于整个美国国防预算两倍的资金，标志着前所未有的投资水平。 这一巨额资金投入凸显了人工智能的战略重要性，可能加速 AI 发展，并重塑行业格局和全球竞争态势。 与美国国防预算的对比凸显了规模之大——国防预算通常每年约 8000 亿美元，意味着科技公司在 AI 上的支出可能超过 1.6 万亿美元。

openbb · AAPL · 6月19日 17:19

**背景**: 人工智能已成为主要科技公司的关键焦点，推动了对硬件、研究和人才的投资。这种支出水平反映了人们相信 AI 将成为跨所有行业的变革性技术。

**标签**: `#AI investment`, `#big tech`, `#spending`, `#industry trend`

---

<a id="item-13"></a>
## [AWS Graviton5 正式发布，为智能体 AI 提升 25%性能](https://tech.yahoo.com/computing/articles/amazon-amzn-aws-graviton5-generally-235911296.html) ⭐️ 8.0/10

AWS 宣布其 Graviton5 处理器正式可用，与上一代相比，为智能体 AI 工作负载提供高达 25% 的性能提升。 此次发布提升了 AI 驱动云工作负载的性价比，尤其是需要自主决策和适应能力的智能体 AI。这巩固了 AWS 在云 AI 基础设施市场的竞争地位。 Graviton5 处理器基于 64 位 Arm 架构，并集成到 Amazon EC2 实例中。性能提升通过针对 AI 推理和数据处理的架构优化实现。

openbb · AAPL · 6月19日 23:59

**背景**: AWS Graviton 是 AWS 自研的基于 Arm 架构的处理器系列，专为云计算设计，提供高效率和成本节约。智能体 AI 指能够自主行动以实现目标的 AI 系统，与传统的被动响应式 AI 模型形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AWS_Graviton">AWS Graviton - Wikipedia</a></li>
<li><a href="https://aws.amazon.com/ec2/graviton/">ARM Processor - Performance Processor - AWS EC2 Graviton - AWS</a></li>
<li><a href="https://aws.amazon.com/what-is/agentic-ai/">What is Agentic AI? - Agentic AI Explained - AWS</a></li>

</ul>
</details>

**标签**: `#AWS`, `#Graviton5`, `#AI`, `#cloud computing`, `#semiconductors`

---

<a id="item-14"></a>
## [谷歌 Gemini 联合负责人 Noam Shazeer 加入 OpenAI](https://tech.yahoo.com/ai/gemini/articles/google-gemini-co-lead-noam-223113611.html) ⭐️ 8.0/10

谷歌 Gemini AI 模型的联合负责人 Noam Shazeer 已离开谷歌加入 OpenAI。OpenAI 首席执行官 Sam Altman 称此举是 '十年磨一剑'。 OpenAI 此次重大人才引进可能加速其 AI 开发，并加剧与谷歌的竞争。这也预示着 AI 领导层和战略方向的潜在变化。 Shazeer 共同领导了 Gemini 项目，这是谷歌的旗舰多模态 AI 模型，在多项基准测试中已超越 GPT-4。他的离开可能影响谷歌的 AI 工作和产品路线图。

openbb · AAPL · 6月19日 22:31

**背景**: Gemini 是谷歌的一套先进 AI 模型，基于张量处理单元（TPU）训练，包括 Ultra、Pro 和 Nano 等版本。Gemini Ultra 是首个在 MMLU 测试中超越人类专家的模型，得分达 90%。该模型名称参考了 DeepMind 与 Google Brain 的合并以及 NASA 的 Gemini 项目。这一背景凸显了 Shazeer 领导如此具有竞争力的 AI 模型的重要性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gemini_(language_model)">Gemini (language model) - Wikipedia</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models">Models | Gemini API | Google AI for Developers</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#OpenAI`, `#talent movement`, `#industry news`

---

<a id="item-15"></a>
## [ASML 因对华 EUV 出口面临美国新审查](https://finance.yahoo.com/technology/articles/asml-faces-fresh-china-export-175704126.html) ⭐️ 8.0/10

美国商务部长卢特尼克表示怀疑一台顶级 EUV 光刻机可能非法流入中国，但 ASML 坚决否认，并强调从未向中国出口过任何 EUV 整机。 这一争端加剧了美欧在半导体出口管制上的紧张关系，可能影响美国国会推动更严格的对华设备限制法案，进而影响全球芯片供应链和技术竞争。 ASML 已散发文件自证清白，指出全球运行的 314 台 EUV 设备均不在中国，且从未向中国出口过任何 EUV 专用组件。

openbb · AAPL · 6月19日 17:57

**背景**: 极紫外（EUV）光刻技术是用于制造 5 纳米和 3 纳米等先进节点半导体芯片的前沿技术。ASML 是全球唯一的 EUV 系统供应商，因此这些设备对先进芯片生产至关重要。这些系统受到严格的出口管制，以防止中国获得领先的芯片制造能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography">Extreme ultraviolet lithography - Wikipedia</a></li>
<li><a href="https://www.asml.com/en/products/euv-lithography-systems">EUV lithography systems – Products | ASML</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#export controls`, `#geopolitics`, `#technology`, `#ASML`

---

<a id="item-16"></a>
## [《毁灭战士》与《德军总部》作曲家鲍比·普林斯去世](https://www.legacy.com/legacy/robert-bobby-prince-lll) ⭐️ 7.0/10

传奇作曲家鲍比·普林斯（Bobby Prince）去世，他曾为《毁灭战士》《德军总部 3D》和《毁灭公爵 3D》创作标志性配乐。讣告确认了他的离世，社区正在哀悼。 普林斯的音乐定义了史上最具影响力的电子游戏的氛围，他的作品帮助塑造了第一人称射击类游戏的声音。他的去世标志着一代先驱的陨落，其配乐至今仍被数百万人所珍爱。 值得一提的是，就在上个月，美国国会图书馆将《毁灭战士》原声带列入国家录音登记册，认可其文化意义。普林斯为《毁灭战士》创作的音乐，尤其是《At Doom's Gate》等曲目，几十年来一直备受赞誉。

hackernews · pgrote · 6月19日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=48602352)

**背景**: 鲍比·普林斯是 1990 年代初 PC 游戏界的关键人物，曾为 id Software 和 3D Realms 创作音乐。他的配乐融合重金属和工业音乐元素，借助 MIDI 技术，在有限的硬件上创作出令人难忘的主题。他参与制作的游戏，包括《毁灭战士》和《德军总部 3D》，被视为第一人称射击游戏的奠基之作。

**社区讨论**: 社区表达了深切感激并分享美好回忆，许多人提到《At Doom's Gate》等曲目令人难忘。评论者指出，普林斯的音乐对《毁灭战士》和《德军总部 3D》的沉浸式氛围至关重要。

**标签**: `#video games`, `#composer`, `#obituary`, `#Doom`, `#Wolfenstein 3D`

---

<a id="item-17"></a>
## [Google Workspace 可通过管理员设置阻止 Firefox](https://tales.fromprod.com/2026/169/google-workspace-threatening-to-block-firefox.html) ⭐️ 7.0/10

有报道称，Google Workspace 的上下文感知访问功能可以阻止 Firefox 浏览器访问，但这是企业管理员可配置的选项，并非 Google 的全局政策。 这澄清了一个常见误解，并凸显了企业环境中管理员设置的重要性。它影响到那些可能无意或有意限制浏览器选择的组织中的 Firefox 用户。 该阻止是通过上下文感知访问功能实现的，该功能仅适用于 Google Workspace 企业版。它允许管理员根据设备安全状态和用户身份等属性创建精细的访问控制策略。

hackernews · birdculture · 6月19日 16:30 · [社区讨论](https://news.ycombinator.com/item?id=48600345)

**背景**: 上下文感知访问是 Google Workspace 中的一项安全功能，允许管理员根据用户身份、位置、设备安全性和 IP 地址等上下文属性执行访问策略。它通常用于限制来自非受管或不可信设备的访问。该功能默认未启用，需要管理员显式配置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://knowledge.workspace.google.com/admin/security/about-context-aware-access">About Context-Aware Access | Security & data protection | Google Workspace Help</a></li>
<li><a href="https://knowledge.workspace.google.com/admin/security/protect-your-business-with-context-aware-access">Protect your business with Context-Aware Access | Security & data protection | Google Workspace Help</a></li>
<li><a href="https://docs.cloud.google.com/access-context-manager/docs/securing-console-and-apis">Set up Context-Aware Access | Access Context Manager | Google Cloud Documentation</a></li>

</ul>
</details>

**社区讨论**: 评论者迅速指出，该阻止是管理员可配置的功能，而非 Google 的全局禁令。博客作者确认他们使用的是 Workspace Business Plus（没有上下文感知访问），表明该警报可能具有误导性。总体情绪认为这个问题被夸大了，应该向企业 IT 部门反映。

**标签**: `#firefox`, `#google-workspace`, `#browser-compatibility`, `#enterprise-policy`

---

<a id="item-18"></a>
## [两党新法案遏制政府施压在线平台删帖](https://www.eff.org/deeplinks/2026/06/new-bill-takes-aim-government-pressure-silence-lawful-online-speech) ⭐️ 7.0/10

参议员罗恩·怀登和特德·克鲁兹提出一项两党法案 JAWBONE，禁止政府机构施压在线平台删除合法言论，电子前哨基金会（EFF）表示支持。 该法案应对了政府过度干预内容审核的担忧，可能保护在线自由表达免受非正式审查。法案获得两党支持，增加了推进的可能性。 法案缩写 JAWBONE 代表'反对官僚机构武器化干预网络表达的正义法案'。它明确针对幕后施压行为，而非合法的法院命令或监管行动。

hackernews · hn_acker · 6月19日 17:34 · [社区讨论](https://news.ycombinator.com/item?id=48600950)

**背景**: 政府机构有时会非正式联系社交媒体平台，要求删除其认为有问题但并未违法的内容。批评者认为这绕过了第一修正案保护。EFF（电子前哨基金会）是一家著名的数字权利组织，长期以来反对这种做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Electronic_Frontier_Foundation">Electronic Frontier Foundation - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对法案缩写及两党共同发起表示赞赏，有人指出克鲁兹参议员支持可能有利于 ICEBlock（用于举报移民执法活动的应用）的法案颇具讽刺意味。也有人对类似过去倡议未能完全保护言论自由表示怀疑。

**标签**: `#online speech`, `#government pressure`, `#EFF`, `#bipartisan bill`, `#free speech`

---

<a id="item-19"></a>
## [中国就分布式数字身份互通互认规则征求意见](https://www.cac.gov.cn/2026-06/18/c_1783525605384124.htm) ⭐️ 7.0/10

2026 年 6 月 18 日，中国国家互联网信息办公室发布了《促进分布式数字身份互通互认应用规定（征求意见稿）》，向社会公开征求意见，旨在推动基于区块链技术的分布式数字身份的互通互认。 该规定可能为中国多个领域（包括金融、交通、海关和数字人民币）建立统一的数字身份框架，有望加速自我主权身份的采用，减少对集中式身份提供商的依赖。 征求意见稿将分布式数字身份定义为由标识符、密钥、可验证凭证和可验证声明组成，并提议在国家区块链网络之上建设‘身份链’，以实现跨平台身份互通。

telegram · zaihuapd · 6月19日 01:39

**背景**: 分布式数字身份允许用户拥有并管理自己的身份信息，无需依赖中央机构，通常使用区块链技术确保安全性和防篡改。可验证凭证（VC）是遵循 W3C 标准的数字凭证，通过加密签名实现即时验证。中国一直在建设国家区块链基础设施——区块链服务网络（BSN），该网络可作为拟议身份链的底层平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blockchain-based_Service_Network">Blockchain-based Service Network - Wikipedia</a></li>
<li><a href="https://spectrum.ieee.org/china-launches-national-blockchain-network-100-cities">China Launches National Blockchain Network in 100 Cities - IEEE Spectrum</a></li>
<li><a href="https://en.wikipedia.org/wiki/Verifiable_credentials">Verifiable credentials</a></li>

</ul>
</details>

**标签**: `#blockchain`, `#digital identity`, `#regulation`, `#China`, `#distributed ledger`

---

<a id="item-20"></a>
## [Google 宣布 Android 侧载未验证应用需等待 24 小时](https://t.me/zaihuapd/42054) ⭐️ 7.0/10

Google 推出了新的 Android 侧载高摩擦流程，要求用户在安装未经过验证的开发者应用前等待 24 小时，期间需开启开发者模式并验证身份。 这一变化大幅提高了侧载的门槛，旨在减少通过欺骗用户安装恶意软件进行诈骗的风险，影响所有侧载应用的用户及在 Google Play 外分发的开发者。 该流程在初始步骤后包含一次性的 24 小时间隔期，用户可以选择将权限设置为 7 天或长期有效。Google 在 2024 年 8 月首次宣布了开发者验证要求。

telegram · zaihuapd · 6月19日 07:59

**背景**: Android 侧载指从 Google Play 商店以外的来源安装应用，通常通过下载 APK 文件进行。Google Play Protect 会扫描应用是否存在有害行为，但新流程增加了摩擦以阻止社会工程攻击。Google 一直在面临平衡安全性与开放性的压力，尤其是在受监管的市场如欧盟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sideloading">Sideloading - Wikipedia</a></li>
<li><a href="https://support.google.com/googleplay/answer/2812853?hl=en">Use Google Play Protect to help keep your apps safe & your data private - Google Play Help</a></li>
<li><a href="https://f-droid.org/en/2025/10/28/sideloading.html">What We Talk About When We Talk About Sideloading | F-Droid - Free and Open Source Android App Repository</a></li>

</ul>
</details>

**标签**: `#Android`, `#security`, `#sideloading`, `#Google`, `#mobile`

---

<a id="item-21"></a>
## [印度为防作弊封锁 Telegram，VPN 使用量激增 150%](https://t.me/zaihuapd/42058) ⭐️ 7.0/10

印度政府为防止医学入学重考（NEET-UG）中出现作弊，自 6 月 16 日至 22 日临时封锁通讯平台 Telegram，导致印度 VPN 注册量飙升 150%，Proton VPN 报告称。 这一事件表明，审查措施可能意外推动 VPN 的使用，并突显了 BGP 劫持策略的附带损害——该策略还导致阿联酋等其他国家用户无法使用 Telegram。 印度电信运营商被指控通过 BGP 路由劫持强行阻断 Telegram 流量，意外影响了印度以外的用户。该封锁是临时性的，仅持续了六天。

telegram · zaihuapd · 6月19日 10:30

**背景**: BGP（边界网关协议）是指导互联网流量的路由协议。BGP 劫持指某个网络宣告其不拥有的 IP 前缀，从而转移流量。印度此前曾使用此类技术强制执行网络封锁。NEET-UG 考试竞争激烈，引发了通过通讯应用作弊的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/BGP_hijacking">BGP hijacking - Wikipedia</a></li>
<li><a href="https://www.cloudflare.com/learning/security/glossary/bgp-hijacking/">What Is BGP Hijacking?</a></li>
<li><a href="https://www.thousandeyes.com/learning/glossary/bgp-route-hijacking">What is BGP Hijacking? Internet & IP Route Hijacking</a></li>

</ul>
</details>

**标签**: `#internet censorship`, `#VPN`, `#India`, `#Telegram`, `#cybersecurity`

---

<a id="item-22"></a>
## [苹果同意在巴西开放第三方应用商店](https://t.me/zaihuapd/42059) ⭐️ 7.0/10

苹果与巴西反垄断监管机构达成和解，同意在 105 天内允许巴西 iPhone 用户安装第三方应用商店并使用外部支付系统。 这一重大决定挑战了苹果长期以来对 iOS 应用分发和支付的控制，可能为其他国家树立先例，进一步削弱 App Store 的封闭生态。 根据这份为期三年的协议，苹果仍可对通过外部支付链接进行的交易收取佣金，但支付系统将与 App Store 解耦。

telegram · zaihuapd · 6月19日 11:15

**背景**: 苹果的 App Store 因其封闭生态系统而受到批评，所有 iOS 应用下载和应用内购买都必须通过苹果平台，佣金高达 30%。类似的监管行动已在欧盟根据《数字市场法案》发生，迫使苹果允许在欧盟成员国使用替代应用商店和侧载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://9to5mac.com/2025/12/23/apple-settles-brazilian-antitrust-case-with-app-store-policy-overhaul/">Apple settles Brazilian antitrust case with App Store policy overhaul - 9to5Mac</a></li>
<li><a href="https://support.apple.com/en-us/118110">About alternative app distribution - Apple Support</a></li>

</ul>
</details>

**标签**: `#Apple`, `#antitrust`, `#regulation`, `#app store`, `#Brazil`

---

<a id="item-23"></a>
## [英国总检察长因假消息担忧弃用 X](https://www.theguardian.com/technology/2026/jun/18/uk-attorney-general-tells-staff-stop-using-x-disinformation-concerns) ⭐️ 7.0/10

英国总检察长理查德·赫默已要求其办公室停止在 X（原推特）上发帖，理由是担心假消息和仇恨言论，成为首个弃用该平台的英国政府机构。 这标志着机构对社交媒体平台信任的重大转变，可能会影响其他政府部门重新考虑在 X 上的存在，同时英国正面临日益增长的监管压力。 该决定是在 2026 年 6 月初南安普敦和贝尔法斯特发生暴力事件后做出的，同时英国政府计划禁止 16 岁以下青少年使用社交媒体，并修订《在线安全法》，要求平台在危机期间更快删除煽动性内容。

telegram · zaihuapd · 6月19日 15:30

**背景**: 英国《2023 年在线安全法》要求在线平台承担注意义务，处理非法和有害内容，罚款最高可达 1800 万英镑或年营业额的 10%。政府目前正在考虑修订，以加强危机应对机制，尤其是在近期与 X 上的假消息相关的骚乱之后。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UK_Online_Safety_Act">UK Online Safety Act</a></li>
<li><a href="https://www.gov.uk/government/publications/online-safety-act-explainer/online-safety-act-explainer">Online Safety Act: explainer - GOV.UK</a></li>

</ul>
</details>

**标签**: `#social media`, `#disinformation`, `#UK government`, `#platform regulation`, `#X/Twitter`

---

<a id="item-24"></a>
## [北航教授被前博士生指控论文造假](https://www.zaobao.com.sg/news/china/story20260619-9231002) ⭐️ 7.0/10

前北航博士生耿江涛公开指控该校两名教授常凌乾和王军在多篇论文中造假，其中一篇发表在《自然》期刊，大量网民涌入官网查阅，导致网站一度瘫痪。 此案凸显了中国学术界科研不端行为的长期问题，并显示出公众对问责制日益增长的需求，网民涌入导致官网瘫痪即为明证。这可能会促使对论文工厂和顶尖大学数据诚信的进一步调查。 耿江涛于 2025 年从北航博士退学成为科普博主，他特别指出常凌乾在《自然》上的论文实验数据“完美到诡异”，并声称王军的两篇论文数据前后矛盾。自今年 4 月以来，耿江涛已举报其他大学的五名学者，这五人均已被处理。

telegram · zaihuapd · 6月19日 16:02

**背景**: 学术诚信在中国一直是一个有争议的问题，不时出现数据造假和剽窃的丑闻。北京航空航天大学是一所隶属于工业和信息化部的重点大学。像耿江涛这样的举报者经常利用社交媒体引发对涉嫌不端行为的关注，有时会促成官方调查。

**标签**: `#academic integrity`, `#research misconduct`, `#whistleblower`, `#Chinese academia`, `#paper retraction`

---

<a id="item-25"></a>
## [谷歌发布新 AI 芯片战略挑战英伟达](https://finance.yahoo.com/technology/ai/articles/google-takes-nvidia-bold-ai-174825604.html) ⭐️ 7.0/10

谷歌宣布了一项新的 AI 芯片战略，旨在利用其定制的张量处理单元（TPU）直接与英伟达在 AI 硬件市场竞争。 此举表明谷歌有意减少对英伟达主导 GPU 的依赖，可能重塑 AI 硬件格局，降低成本和促进创新。 该战略据报道涉及扩大使用谷歌定制的 TPU，这些 TPU 专为机器学习工作负载设计，已在内部使用多年。

openbb · AAPL · 6月19日 17:48

**背景**: 谷歌的张量处理单元（TPU）是谷歌专门为神经网络机器学习开发的定制专用集成电路（ASIC）。与英伟达的通用 GPU 不同，TPU 针对谷歌的机器学习框架 TensorFlow 进行了优化。这一战略转变可能导致谷歌提供更多垂直整合的 AI 解决方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Google_Tensor">Google Tensor - Wikipedia</a></li>
<li><a href="https://www.youtube.com/watch?v=3-U1FieCKTM">Touching the Elephant: technical evolution of Google ’s Tensor ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#hardware`, `#Google`, `#Nvidia`, `#chips`

---

<a id="item-26"></a>
## [智谱股价因 AI 政治风险飙升 33%](https://finance.yahoo.com/technology/ai/articles/ai-politics-risk-emerges-zhipu-180947049.html) ⭐️ 7.0/10

中国人工智能公司智谱的股价在 AI 政治风险担忧加剧的背景下飙升 33%。此次大幅上涨反映了市场对围绕 AI 发展的地缘政治紧张局势的反应。 这一事件凸显了人工智能技术与地缘政治日益交织，影响投资者情绪和市场估值。它强调了政治风险如何推动人工智能领域的股票波动。 中国知名人工智能公司智谱因新兴的 AI 政治风险触发，股价单日上涨 33%。虽然未提及具体政治事件，但这一波动表明市场对监管和地缘政治新闻的高度敏感。

openbb · AAPL · 6月19日 18:09

**背景**: 智谱是一家以开发大型语言模型而闻名的中国领先人工智能公司。'AI 政治风险'指政府政策、贸易限制或国家安全关切对人工智能公司的潜在影响。全球人工智能竞赛加剧了地缘政治摩擦，尤其是中美之间，导致人工智能股票波动加剧。

**标签**: `#AI`, `#geopolitics`, `#stock market`, `#Zhipu`, `#risk`

---