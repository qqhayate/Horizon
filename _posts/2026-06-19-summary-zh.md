---
layout: default
title: "Horizon Summary: 2026-06-19 (ZH)"
date: 2026-06-19
lang: zh
---

> 从 165 条内容中筛选出 30 条重要资讯。

---

1. [发现 1 万个 GitHub 仓库分发木马恶意软件](#item-1) ⭐️ 9.0/10
2. [隐私倡导者的挑战导致 Elkjop 被罚 180 万欧元](#item-2) ⭐️ 8.0/10
3. [医院和大学以更低成本重新利用药物](#item-3) ⭐️ 8.0/10
4. [你在大模型的权重里吗？网站检测 LLM 对你的识别度](#item-4) ⭐️ 8.0/10
5. [Modos 13.3 英寸彩色电子纸显示器实现 60Hz 刷新率](#item-5) ⭐️ 8.0/10
6. [SK 电信与 Anthropic 的 Mythos 争议](#item-6) ⭐️ 8.0/10
7. [Gerrymandle：每日重划选区解谜游戏](#item-7) ⭐️ 8.0/10
8. [Emacs 31 预览：日常使用的新特性](#item-8) ⭐️ 8.0/10
9. [Datasette Apps 插件：在 Datasette 中运行沙盒 HTML+JS 应用](#item-9) ⭐️ 8.0/10
10. [美国据报禁止 Anthropic 的新 Fable AI 模型](#item-10) ⭐️ 8.0/10
11. [Popa 僵尸网络与以色列上市公司关联](#item-11) ⭐️ 8.0/10
12. [AI 模型助力诊断儿童罕见遗传病](#item-12) ⭐️ 8.0/10
13. [苹果与英特尔达成初步芯片代工协议](#item-13) ⭐️ 8.0/10
14. [小米开源 AI 智能家居方案 Miloco 2.0](#item-14) ⭐️ 8.0/10
15. [谷歌测试新版 reCAPTCHA 挥手验证](#item-15) ⭐️ 8.0/10
16. [谷歌采用英伟达策略打造 AI 芯片竞争对手](#item-16) ⭐️ 8.0/10
17. [Ubiquiti 发布基于 ZFS 的企业级 NAS](#item-17) ⭐️ 7.0/10
18. [康奈尔 CS 6120：免费自导式高级编译器课程](#item-18) ⭐️ 7.0/10
19. [瑞士议会取消新建核电站禁令](#item-19) ⭐️ 7.0/10
20. [.gitignore 之外的其他 Git 忽略技巧](#item-20) ⭐️ 7.0/10
21. [W Social：欧洲数字主权还是政治秀场？](#item-21) ⭐️ 7.0/10
22. [GLM-5.2 引入 IndexShare 实现高效长上下文推理](#item-22) ⭐️ 7.0/10
23. [迈克尔·莫顿访谈：AI 时代电商的变革](#item-23) ⭐️ 7.0/10
24. [ChatGPT 定时任务新增 Scheduled 页面与监控通知](#item-24) ⭐️ 7.0/10
25. [多款婴幼儿纸尿裤检出生殖毒性物质甲酰胺](#item-25) ⭐️ 7.0/10
26. [华为将 Wi-Fi 7 专利费定为每台设备 0.5 美元](#item-26) ⭐️ 7.0/10
27. [GitHub Models 停止接纳新用户](#item-27) ⭐️ 7.0/10
28. [中国拟出台分布式数字身份互通互认规定](#item-28) ⭐️ 7.0/10
29. [亚马逊可能对外销售 AI 芯片，挑战英伟达](#item-29) ⭐️ 7.0/10
30. [苹果的现金无法主宰内存市场](#item-30) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [发现 1 万个 GitHub 仓库分发木马恶意软件](https://orchidfiles.com/github-repositories-distributing-malware/) ⭐️ 9.0/10

研究发现超过 1 万个 GitHub 仓库正在分发木马恶意软件，通过频繁提交和伪装成合法项目等手段，针对自动化依赖抓取系统进行攻击。 这一发现凸显了对软件供应链安全的重大威胁，因为自动化工具和 AI 代理可能无意中获取恶意代码，可能影响成千上万的开发者和组织。 攻击者克隆热门仓库，然后每隔几小时删除并重新推送提交以显得活跃，从而欺骗自动化系统。他们还冒充知名作者，以增加其仓库被克隆的可能性。

hackernews · theorchid · 6月18日 11:45 · [社区讨论](https://news.ycombinator.com/item?id=48583928)

**背景**: 供应链攻击针对软件开发流程中较薄弱的环节，例如第三方依赖。GitHub 冒充是指创建模仿可信开发者的虚假仓库来分发恶意软件。这些策略利用了开源生态系统中的信任和自动化，开发者依赖自动化工具来获取依赖项。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Supply_chain_attack">Supply chain attack</a></li>
<li><a href="https://www.vanderbilt.edu/valiant/2025/07/28/whos-pushing-the-code-an-exploration-of-github-impersonation/">Who’s Pushing the Code? An Exploration of GitHub Impersonation</a></li>
<li><a href="https://www.linkedin.com/posts/trustdlogo_softwaresupplychain-supplychainsecurity-appsec-activity-7436752192742739968-PLiR">GitHub Malware Distribution via Impersonated Repositories | LinkedIn</a></li>

</ul>
</details>

**社区讨论**: 社区成员报告了类似经历，有人指出攻击者针对的是自动化代理而非人类，另有人提到自己的名字被附加到虚假项目上。有评论认为频繁提交是为了在自动化工具的搜索结果中排名靠前。还有人将这类攻击的增加与 AI 代理的普及和全球重大选举联系起来。

**标签**: `#security`, `#malware`, `#GitHub`, `#supply chain`, `#open source`

---

<a id="item-2"></a>
## [隐私倡导者的挑战导致 Elkjop 被罚 180 万欧元](https://www.thatprivacyguy.com/blog/elkjop-forced-consent-fine/) ⭐️ 8.0/10

一名隐私倡导者因强制同意营销而持续投诉，导致电子零售商 Elkjop 被挪威数据保护局处以 180 万欧元罚款。 此案表明，GDPR 禁止强制同意的规定是可执行的，可能阻止其他公司将营销同意与服务访问挂钩。 Elkjop 曾要求客户同意营销作为加入其忠诚计划的先决条件，而倡导者在五年前就警告这是非法的。罚款基于在正式通知后仍持续违规。

hackernews · speckx · 6月18日 18:31 · [社区讨论](https://news.ycombinator.com/item?id=48589501)

**背景**: 根据《通用数据保护条例》（GDPR），数据处理的同意必须是自由给予、具体且知情的。强制同意发生在服务将访问权与同意非必要数据使用绑定时，这通常是非法的。

**社区讨论**: 评论者赞扬倡导者的坚持和裁决，强调挑战企业过度行为的重要性。一些人指出，倡导者起诉了最终为他赢得案件的法人实体，这颇具讽刺意味。

**标签**: `#privacy`, `#GDPR`, `#data protection`, `#consent`, `#enforcement`

---

<a id="item-3"></a>
## [医院和大学以更低成本重新利用药物](https://www.kcl.ac.uk/news/hospitals-and-universities-repurposing-drugs-at-90-lower-cost) ⭐️ 8.0/10

伦敦国王学院的一份新报告指出，医院和大学正在以比开发新药低 90%的成本成功重新利用现有药物治疗新适应症。 这挑战了传统的药品定价模式，可能使治疗更便宜、更可及，尤其是对罕见病患者而言。 关键细节包括贝伐珠单抗（Avastin）每剂 50 美元与雷珠单抗（Lucentis）每剂 1500 美元用于同一疾病的对比，以及正式重新利用面临的监管障碍。

hackernews · giuliomagnifico · 6月18日 10:33 · [社区讨论](https://news.ycombinator.com/item?id=48583386)

**背景**: 药物重新利用是指为已获批药物寻找新的治疗用途。由于已有安全性数据，这比开发新药更快更便宜。然而，没有制造商支持，超说明书使用缺乏正式批准和保险覆盖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Drug_repositioning">Drug repositioning - Wikipedia</a></li>
<li><a href="https://www.fda.gov/news-events/press-announcements/fda-advances-drug-repurposing-address-unmet-medical-needs">FDA Advances Drug Repurposing to Address Unmet Medical Needs</a></li>

</ul>
</details>

**社区讨论**: 社区讨论提供了具体例子，如 Avastin 与 Lucentis、Spravato 与氯胺酮，突出了成本差异和监管障碍。评论者普遍支持药物重新利用，但指出没有正式批准途径，超说明书使用仍然有限。

**标签**: `#healthcare`, `#drug repurposing`, `#pharmaceuticals`, `#cost reduction`

---

<a id="item-4"></a>
## [你在大模型的权重里吗？网站检测 LLM 对你的识别度](https://www.intheweights.com/) ⭐️ 8.0/10

新网站“Are You in the Weights?”并行查询多个前沿和小型语言模型，根据用户的在线足迹检查模型对用户的识别强度，并对回复进行聚类以提供识别分数。 该工具凸显了个人数据存在于大语言模型中的新兴问题，引发隐私和同意方面的担忧。它让用户探索自己的数字足迹对 AI 识别的影响，促进关于数据权利的讨论。 该网站同时查询前沿模型（如 GPT-4、Claude）和小型模型（如 Llama 3.2 1B），将回复聚类为准确、幻觉或未知等类别。结果非确定性，添加更多关于自己的关键词可提高分数。

hackernews · turtlesoup · 6月18日 20:49 · [社区讨论](https://news.ycombinator.com/item?id=48591348)

**背景**: 大型语言模型通过海量网络数据训练，包括来自论坛、社交媒体和其他公共来源的个人内容。这意味着个人的在线足迹可能嵌入模型权重中，使模型能够“识别”他们。“Are You in the Weights?”网站通过查询模型对特定名称或角色的反应并分析回复来探究这一现象。

**社区讨论**: 社区评论显示了不同的体验：一些用户报告了准确的识别（例如开源贡献者获得高分），而另一些则发现幻觉身份或完全没有识别。用户还提出了输入真实姓名的隐私担忧，并注意到结果的非确定性，分数因添加关键词而异。

**标签**: `#LLMs`, `#privacy`, `#AI recognition`, `#web presence`, `#Hacker News`

---

<a id="item-5"></a>
## [Modos 13.3 英寸彩色电子纸显示器实现 60Hz 刷新率](https://spectrum.ieee.org/modos-e-paper-monitor) ⭐️ 8.0/10

Modos，一个两人初创公司，正在开发一款名为 Modos Flow 的 13.3 英寸彩色电子纸显示器，具有 3200x2400 分辨率、300 PPI，以及 60Hz 刷新率和低于 100 毫秒的延迟。 这一突破通过提供彩色、高刷新率的电子纸显示器，使其更接近主流应用，该显示器具有类纸质感和节能特性，有望为生产力和娱乐设备提供户外可读、低功耗的解决方案。 该显示器采用 E Ink Carta 面板，专为交互式工作流程设计，支持 USB-C DisplayPort Alt-Mode 和触摸输入。

hackernews · Vinnl · 6月18日 11:41 · [社区讨论](https://news.ycombinator.com/item?id=48583897)

**背景**: 电子纸显示器（如 E Ink 的产品）以其超低功耗和类纸可读性而闻名，但传统上刷新率较慢且颜色有限。大多数电子纸显示器刷新率低于 30Hz，且为单色或有限颜色（如 4096 色）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linuxgizmos.com/modos-flow-is-a-paper-like-13-3-inch-monitor-with-60-hz-refresh-and-touch-support/">Modos Flow is a paper -like 13.3-inch monitor with 60 Hz refresh and...</a></li>
<li><a href="https://www.tomshardware.com/monitors/portable-monitors/hands-on-with-modos-tech-13-3-inch-e-paper-monitors">Hands-on with Modos Tech 13.3-inch e - paper ... | Tom's Hardware</a></li>

</ul>
</details>

**社区讨论**: 社区成员对这一进展表示兴奋，有人指出这是电子纸领域最令人兴奋的发展之一。其他人则对更高刷新率对面板寿命的影响表示好奇，并希望定价合理且能兼作电子阅读器。

**标签**: `#e-paper`, `#displays`, `#hardware`, `#startups`, `#technology`

---

<a id="item-6"></a>
## [SK 电信与 Anthropic 的 Mythos 争议](https://www.wired.com/story/sk-telecom-anthropic-mythos-export-controls/) ⭐️ 8.0/10

白宫要求 Anthropic 根据美国出口管制撤销 SK 电信对 Mythos AI 模型的访问权限，Anthropic 立即遵守，尽管 SK 电信已投资 1 亿美元。 这一事件突显了 AI 治理中的地缘政治紧张局势，并对外国公司整合美国 AI 模型时的供应商连续性提出了严重关切。它可能阻碍国际对美国 AI 实验室的投资。 Mythos 是一款旨在发现软件漏洞的强大 AI 模型，但 Anthropic 出于安全考虑未公开发布。SK 电信的访问权限在 Claude Fable 发布前被撤销，后者使用相同的基础模型并增加了安全防护。

hackernews · dstala · 6月18日 12:44 · [社区讨论](https://news.ycombinator.com/item?id=48584484)

**背景**: 美国出口管制限制向某些国家转让先进 AI 技术，SK 电信是一家投资 Anthropic 巨额的韩国电信巨头。Mythos 模型（也称 Claude Mythos）是一个用于网络安全的 LLM，因其潜在的滥用风险引发了全球警报。这一争议凸显了国际投资与国家安全政策之间的冲突。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos">Claude Mythos - Wikipedia</a></li>
<li><a href="https://www.nytimes.com/2026/04/22/technology/anthropics-mythos-ai.html">Anthropic's New A.I. Model Sets Off Global Alarms</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了不同观点：有人认为这是对‘倾向自由派’公司的政治打压，也有人警告不要投资美国公司。该事件也被视为供应商连续性问题，可能使外国公司更加谨慎。一条评论认为 Wired 的文章具有误导性，称关闭访问权限主要是由于 Fable 的越狱问题，而非 SK 电信。

**标签**: `#Anthropic`, `#export controls`, `#AI governance`, `#geopolitics`, `#SK Telecom`

---

<a id="item-7"></a>
## [Gerrymandle：每日重划选区解谜游戏](https://gerrymandle.cc/) ⭐️ 8.0/10

Gerrymandle 是一款每日解谜游戏，要求玩家重新划分选举选区，以理解不公正选区划分（gerrymandering）的概念，在 Hacker News 上获得了高度关注。 通过将复杂的政治策略“不公正选区划分”游戏化，Gerrymandle 使抽象概念变得具体且具有教育意义，适用于公民教育课堂和公众意识提升。 该游戏简化了不公正选区划分的机制——例如，若一个选区中两党票数持平，则无人获胜——优先考虑趣味性而非严格真实性，但能有效展示“集中”和“分散”策略。

hackernews · realmofthemad · 6月18日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=48585739)

**背景**: 不公正选区划分（gerrymandering）是指操纵选区边界以偏袒某一政党或群体，通常通过“集中”（将对手聚集在少数选区）和“分散”（将对手分散到多个选区）实现。该术语源于 1812 年马萨诸塞州州长埃尔布里奇·格里签署的一个形似蝾螈的选区。这种做法被广泛批评为破坏公平代表性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gerrymandering">Gerrymandering - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Packing_and_cracking">Packing and cracking</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该游戏是高中公民教育的创意工具，有人指出虽然平局设定不现实，但核心概念传达得很好。还有人引用了关于公平选区划分算法的学术论文以及类似桌游“Berrymandering”。

**标签**: `#game`, `#politics`, `#education`, `#gerrymandering`, `#puzzle`

---

<a id="item-8"></a>
## [Emacs 31 预览：日常使用的新特性](https://www.rahuljuliato.com/posts/emacs-31-around-the-corner) ⭐️ 8.0/10

Emacs 31 即将发布，带来多项新特性以改善日常编辑工作流，Rahul Juliato 在一篇详细预览中进行了介绍。 Emacs 31 是为历史最悠久、影响力最大的文本编辑器之一的重要里程碑，将影响数百万依赖其可扩展性和强大功能的开发者和写作者。 文章描述了诸如改进的 tree-sitter 支持、更好的性能以及新的自定义选项等变化，旨在使 Emacs 更加现代化和高效。

hackernews · frou_dh · 6月18日 12:10 · [社区讨论](https://news.ycombinator.com/item?id=48584135)

**背景**: Emacs 是一个高度可扩展、可定制的文本编辑器，已活跃开发数十年。其最新版本 31 延续了由活跃的开源社区驱动的渐进式改进传统。

**社区讨论**: 评论者对 Emacs 31 表示热情，许多人指出尽管有竞争编辑器，Emacs 对于严肃工作仍然不可或缺。一些人强调现在可以集成 Claude 等 LLM，使 Emacs 更加强大，而另一些人则开玩笑说他们会升级但可能忽略新功能。

**标签**: `#emacs`, `#editor`, `#software-release`, `#productivity`

---

<a id="item-9"></a>
## [Datasette Apps 插件：在 Datasette 中运行沙盒 HTML+JS 应用](https://simonwillison.net/2026/Jun/18/datasette-apps/#atom-everything) ⭐️ 8.0/10

Simon Willison 发布了 datasette-apps 插件，该插件允许在 Datasette 内部以严格受限的 iframe 沙盒方式托管自包含的 HTML+JavaScript 应用，并支持只读和写入 SQL 查询。 该插件将 Datasette 从数据发布工具扩展为自定义交互式应用平台，用户无需额外基础设施即可直接在 SQLite 数据库上构建丰富的界面。 应用在设置了 sandbox='allow-scripts allow-forms' 并注入 CSP 头部的 iframe 中运行，阻止外部 HTTP 请求，防止数据泄露。仅当配置了存储查询时才允许写入操作。

rss · Simon Willison · 6月18日 23:58

**背景**: Datasette 是一个开源的多功能工具，用于将数据探索和发布为交互式网站和 API。它使用 SQLite 数据库并提供 JSON API。该插件的灵感来自 Claude Artifacts 以及作者在“vibe-coded”HTML 工具方面的实验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datasette.io/">Datasette: An open source multi-tool for exploring and ...</a></li>
<li><a href="https://github.com/simonw/datasette">GitHub - simonw/datasette: An open source multi-tool for ... The Datasette Ecosystem Introduction to Datasette, a Frontend to Tabulated Data datasette · PyPI Datasette Reviews, Pricing & Alternatives (2026) | Toolradar Datasette - skills.network</a></li>

</ul>
</details>

**标签**: `#datasette`, `#plugin`, `#web-application`, `#sql`, `#sandbox`

---

<a id="item-10"></a>
## [美国据报禁止 Anthropic 的新 Fable AI 模型](https://newsletter.pragmaticengineer.com/p/the-pulse-big-implications-of-us) ⭐️ 8.0/10

美国政府据报道禁止了 Anthropic 的最新 AI 模型 Claude Fable 5，引发关于国家安全和 AI 监管的讨论。 此举表明政府对先进 AI 能力的审查加强，可能重塑前沿模型的部署和全球监管方式。 Claude Fable 5 在 Anthropic 官网及云服务商处标注为普遍可用，但禁令表明可能因国家安全原因受限。

rss · The Pragmatic Engineer · 6月18日 17:11

**背景**: Anthropic 是一家以 Claude 模型系列闻名的 AI 安全初创公司。Claude Fable 5 是其迄今最强大的模型，在编程和推理基准测试中表现出色。美国此前曾考虑监管强大 AI 模型以防止滥用，例如在网络安全或武器开发领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/news/claude-fable-5-mythos-5">Claude Fable 5 and Claude Mythos 5 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/introducing-claude-fable-5-and-claude-mythos-5">Introducing Claude Fable 5 and Claude Mythos 5 - Claude API Docs</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#Anthropic`, `#US policy`, `#tech industry`, `#newsletter`

---

<a id="item-11"></a>
## [Popa 僵尸网络与以色列上市公司关联](https://krebsonsecurity.com/2026/06/popa-botnet-linked-to-publicly-traded-israeli-firm/) ⭐️ 8.0/10

研究人员将已运行四年、利用数百万台安卓电视盒进行广告欺诈和数据抓取的 Popa 安卓僵尸网络，与上市公司 Alarum Technologies 旗下的住宅代理服务商 NetNut 关联起来。 此次曝光揭示了一家合法的上市公司可能从大规模僵尸网络中获利，引发了对网络安全和广告行业中住宅代理服务的监管及道德边界的严重质疑。 与专注于破坏性攻击的传统僵尸网络不同，Popa 僵尸网络与被感染设备建立持久加密通信通道，用于广告欺诈、账户接管和大规模数据抓取。

rss · Krebs on Security · 6月18日 17:37

**背景**: 僵尸网络是由攻击者控制的受感染设备网络，用于进行恶意活动。住宅代理通过真实的住宅 IP 地址路由互联网流量，使流量看似合法。Popa 僵尸网络感染安卓电视盒，将其变为 NetNut 服务的代理节点，而 NetNut 出售住宅 IP 访问权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://krebsonsecurity.com/2026/06/popa-botnet-linked-to-publicly-traded-israeli-firm/">‘Popa’ Botnet Linked to Publicly-Traded Israeli Firm</a></li>
<li><a href="https://en.wikipedia.org/wiki/Residential_proxy">Residential proxy</a></li>

</ul>
</details>

**标签**: `#botnet`, `#android`, `#cybersecurity`, `#advertising fraud`

---

<a id="item-12"></a>
## [AI 模型助力诊断儿童罕见遗传病](https://openai.com/index/diagnose-rare-childhood-diseases) ⭐️ 8.0/10

研究人员使用 OpenAI 的推理模型 o3 Deep Research 重新分析了 376 个此前未确诊的罕见儿科病例，发现了 18 个新诊断。 这展示了 AI 如何帮助解决罕见遗传病的诊断难题，为等待多年的家庭带来希望，凸显了先进 AI 推理在医疗领域的实际应用。 这项研究发表在《NEJM AI》上，由波士顿儿童医院和哈佛大学合作完成，使用的模型是 OpenAI 的推理模型 o3 Deep Research。

rss · OpenAI News · 6月18日 08:00

**背景**: 罕见遗传病因其症状多样和遗传复杂性而极难诊断。传统方法往往无法确定根本原因，导致许多病例无法确诊。像 o3 Deep Research 这样的 AI 模型可以分析大量数据，包括基因组和临床信息，提出可能被忽略的潜在诊断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/diagnose-rare-childhood-diseases/">Using AI to help physicians diagnose rare genetic diseases ... | OpenAI</a></li>
<li><a href="https://digg.com/tech/dct30el2">OpenAI and Boston Children's Hospital use o3 Deep Research to...</a></li>
<li><a href="https://aiproductivity.ai/news/openai-reasoning-model-diagnoses-rare-childhood-diseases/">OpenAI Model Diagnoses 18 Rare Childhood Diseases</a></li>

</ul>
</details>

**标签**: `#AI`, `#healthcare`, `#rare diseases`, `#diagnosis`, `#OpenAI`

---

<a id="item-13"></a>
## [苹果与英特尔达成初步芯片代工协议](https://t.me/zaihuapd/42031) ⭐️ 8.0/10

苹果与英特尔签署了一项初步协议，由英特尔代工生产部分苹果设备所需的芯片，谈判历时一年有余，并于近几个月最终敲定。 该协议标志着半导体行业的重大转变——苹果作为台积电的长期客户，在美国政府的压力下开始分散供应链。这也提振了英特尔的代工业务，使其成为台积电和三星的更强劲竞争对手。 英特尔具体将代工哪类设备（iPhone、iPad 或 Mac）的哪类芯片尚未披露。至此，英特尔的代工客户已包括苹果、英伟达和 SpaceX 三家。

telegram · zaihuapd · 6月18日 09:19

**背景**: 半导体代工厂是制造集成电路的工厂。传统上，英特尔既设计也制造自己的芯片（即整合器件制造商，IDM），但其推出了英特尔代工服务，为其他公司制造芯片，与台积电等纯代工厂竞争。美国政府一直通过激励措施和直接游说积极推动本土芯片制造。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Semiconductor_foundry">Semiconductor foundry</a></li>
<li><a href="https://en.wikipedia.org/wiki/Intel_Foundry_Services">Intel Foundry Services</a></li>
<li><a href="https://en.wikipedia.org/wiki/Foundry_model">Foundry model - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Apple`, `#Intel`, `#chip manufacturing`, `#semiconductor`, `#foundry`

---

<a id="item-14"></a>
## [小米开源 AI 智能家居方案 Miloco 2.0](https://github.com/XiaoMi/xiaomi-miloco) ⭐️ 8.0/10

小米发布了 Miloco 2.0，这是一个开源的 AI 智能家居系统，通过米家摄像头的音视频感知，内置 MiMo 大模型，实现主动控制全屋设备。 小米将 Miloco 开源，使 AI 驱动的智能家居技术民主化，让开发者能够构建主动感知的家居自动化，可能加速智能家居生态系统的创新。 Miloco 2.0 作为 OpenClaw 插件运行，需要 macOS 或 Linux（Windows 通过 WSL），4GB 内存、256GB 存储，以及小米账号和 MiMo API 密钥；它依赖云端大模型，会产生持续的 API 费用，且仅限于非商业用途。

telegram · zaihuapd · 6月18日 12:23

**背景**: MiMo 是小米的具身大语言模型，提供从 39 元/月起的 TokenPlan 定价方案。OpenClaw 是一个开源 AI 代理框架，支持多种功能的插件。Miloco 利用摄像头作为感知入口，使系统能够理解用户意图并主动控制设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/XiaoMi/xiaomi-miloco">GitHub - XiaoMi/xiaomi-miloco: Xiaomi Miloco · GitHub</a></li>
<li><a href="https://xiaomiforall.com/xiaomi-miloco-smart-homes-local-ai/">Xiaomi Miloco: Revolutionizing Smart Homes with Local AI - Xiaomi for All</a></li>
<li><a href="https://www.gizchina.com/ai/xiaomi-launches-mimo-large-model-with-tokenplan-pricing-starting-at-39-yuan">Xiaomi Launches MiMo Large Model With TokenPlan Pricing...</a></li>

</ul>
</details>

**标签**: `#smart home`, `#open source`, `#AI`, `#large language model`, `#Xiaomi`

---

<a id="item-15"></a>
## [谷歌测试新版 reCAPTCHA 挥手验证](https://www.ithome.com/0/966/252.htm) ⭐️ 8.0/10

谷歌正在测试新版 reCAPTCHA，要求用户授权摄像头并录制挥手视频进行验证。系统通过提取手部 21 个关键点坐标来区分真人和机器程序。 这标志着从传统验证码向生物特征验证的重大转变，引发了安全与隐私方面的担忧。如果广泛部署，可能会改变数百万用户在线证明身份的方式。 谷歌声称视频不与用户身份绑定，不录制音频，验证完成后自动删除。该系统旨在防范凭证填充攻击和批量注册等行为。

telegram · zaihuapd · 6月18日 16:39

**背景**: reCAPTCHA 是谷歌提供的一项免费服务，通过区分人类和自动化机器人来保护网站免受垃圾邮件和滥用。传统 reCAPTCHA 方法包括识别扭曲文本、选择图片或点击复选框。新方法采用了手部关键点检测技术，可识别手部 21 个关键点，该技术最初由谷歌的 MediaPipe 开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.google.com/edge/mediapipe/solutions/vision/hand_landmarker">Hand landmarks detection guide | Google AI Edge | Google for Developers</a></li>
<li><a href="https://en.wikipedia.org/wiki/Credential_stuffing">Credential stuffing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 根据 IT 之家文章，已有用户批评此举正在推动互联网向生物特征认证方向发展。搜索结果中未提供详细评论。

**标签**: `#reCAPTCHA`, `#biometrics`, `#security`, `#privacy`, `#Google`

---

<a id="item-16"></a>
## [谷歌采用英伟达策略打造 AI 芯片竞争对手](https://www.wsj.com/tech/ai/google-is-using-nvidias-playbook-to-build-a-rival-ai-chip-business-1eac86f9?siteid=yhoof2&yptr=yahoo) ⭐️ 8.0/10

谷歌正效仿英伟达的策略，建立自己的 AI 芯片业务，旨在与英伟达在 AI 硬件市场的主导地位竞争。 此举可能重塑 AI 芯片格局，减少对英伟达 GPU 的依赖，并可能降低 AI 工作负载的成本，使谷歌及其云客户受益。 谷歌多年来一直在开发张量处理单元（TPU），但如今它正采用英伟达的策略，围绕其硬件构建全面的软件生态系统以吸引开发者。

openbb · AAPL · 6月19日 01:09

**背景**: 英伟达的 CUDA 平台是一个专有的并行计算 API，允许开发者使用英伟达 GPU 进行通用处理，形成了强大的生态系统锁定。谷歌的 TPU 是专门为加速机器学习工作负载而设计的定制 ASIC，但缺乏类似的软件生态系统。通过采用英伟达的策略，谷歌旨在创建一个开发者友好的平台，以挑战英伟达的主导地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tensor_Processing_Unit">Tensor Processing Unit - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/NVIDIA_CUDA">NVIDIA CUDA</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#Google`, `#Nvidia`, `#competition`, `#hardware`

---

<a id="item-17"></a>
## [Ubiquiti 发布基于 ZFS 的企业级 NAS](https://blog.ui.com/article/introducing-enterprise-nas) ⭐️ 7.0/10

Ubiquiti 发布了一款企业级 NAS 设备，采用 ZFS 文件系统，配备双 25Gbps SFP28 端口和冗余电源。 此举将 ZFS 的高级数据完整性和快照功能引入 Ubiquiti 生态系统，可能提供一个无订阅费用的高性价比企业存储方案，但社区对 Ubiquiti 的软件质量和企业级准备的质疑可能阻碍其推广。 该 NAS 包含双 25GbE SFP28 端口和冗余电源，但部分社区成员质疑机械硬盘能否充分利用这些带宽。Ubiquiti 此前曾发生安全事件和软件质量问题，包括不当处理 AWS 访问密钥和误导性的加密声明。

hackernews · ksec · 6月18日 14:24 · [社区讨论](https://news.ycombinator.com/item?id=48585866)

**背景**: ZFS 是由 Sun Microsystems 最初开发的组合文件系统和卷管理器，以其数据完整性特性（如校验和、快照和复制）而闻名。它被广泛应用于 TrueNAS 等 NAS 解决方案，但商用现成的 ZFS 设备常被认为性能不足。Ubiquiti 主要以网络设备闻名，并正在扩展到存储领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ZFS">ZFS - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区对 Ubiquiti 进入 NAS 领域并使用 ZFS 感到兴奋，称赞 ZFS 的优越性和无月费模式。然而，许多人强烈担忧 Ubiquiti 的软件质量，提及过去的安全漏洞、误导性的加密声明，以及将未测试软件发布到企业环境中的不良记录。

**标签**: `#Ubiquiti`, `#NAS`, `#ZFS`, `#Enterprise`, `#Storage`

---

<a id="item-18"></a>
## [康奈尔 CS 6120：免费自导式高级编译器课程](https://www.cs.cornell.edu/courses/cs6120/2025fa/self-guided/) ⭐️ 7.0/10

康奈尔大学的 CS 6120 高级编译器课程已作为免费自导式在线资源发布，包含讲座视频、作业和项目材料。 这使得高质量的高级编译器课程对任何人开放，可能惠及自学者和没有正式计算机科学教育的专业人士。 该课程涵盖静态单赋值（SSA）形式、数据流分析和动态编译等主题，但社区评论指出关于追踪编译的部分被认为已过时。

hackernews · ibobev · 6月18日 11:04 · [社区讨论](https://news.ycombinator.com/item?id=48583606)

**背景**: 编译器构建是计算机科学中的一个基础主题，连接理论与实践。高级编译器课程通常涵盖优化技术和运行时系统。许多编译器资源要么是入门级的，要么已过时，因此这个高级自定进度课程很有价值。

**社区讨论**: 评论包括对可用性的赞扬，但也有批评：一位评论者指出追踪编译是一条死路，建议关注类型反馈和去优化。另一位质疑该课程何以为“高级”，因为许多主题是标准的。历史上的重复发布表明持续的兴趣。

**标签**: `#compilers`, `#education`, `#computer-science`, `#self-guided-course`

---

<a id="item-19"></a>
## [瑞士议会取消新建核电站禁令](https://www.bluewin.ch/en/news/switzerland/parliament-lifts-ban-on-new-nuclear-power-plants-3257535.html) ⭐️ 7.0/10

瑞士议会投票决定取消新建核电站的禁令，推翻了 2011 年福岛事故后做出的决定。 这一政策转变对瑞士的能源战略意义重大，在气候目标和能源安全背景下为核电作为无碳能源打开了大门，并可能影响其他国家重新考虑核能。 该禁令最初是在 2011 年福岛核事故后实施的，该决定在成为法律前仍可能面临瑞士全民公投。

hackernews · leonidasrup · 6月18日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=48585746)

**背景**: 2011 年福岛核事故后，瑞士决定逐步淘汰核电并禁止新建核电站，但目前该国仍有四个核反应堆，供应约三分之一的电力。此次投票反映了对核电作为低碳能源选项的态度转变。

**社区讨论**: 评论者意见不一：有人强调核电的低死亡率/太瓦时和安全性优势，也有人担忧成本、时机、对稀土开采的依赖以及全民公投的需要。讨论政治色彩浓厚，左翼政党反对核电。

**标签**: `#nuclear energy`, `#energy policy`, `#Switzerland`, `#environment`, `#politics`

---

<a id="item-20"></a>
## [.gitignore 之外的其他 Git 忽略技巧](https://nelson.cloud/.gitignore-isnt-the-only-way-to-ignore-files-in-git/) ⭐️ 7.0/10

一篇文章指出 Git 提供了除 .gitignore 之外的多种忽略机制，具体包括 .git/info/exclude、通过 core.excludesfile 设置的全局忽略文件，以及用于控制差异和归档的 .gitattributes。 了解这些替代方案有助于开发者保持项目 .gitignore 文件的整洁，避免在所有仓库中提交个人或环境特定文件，同时不影响他人的工作流程。 .git/info/exclude 文件仅作用于本地仓库且不会被提交，适合忽略个人 IDE 或操作系统文件。全局忽略通过 git config core.excludesfile 配置，适用于机器上的所有仓库。.gitattributes 可以设置 export-ignore 以从归档中排除文件，或设置 diff= 以隐藏差异。

hackernews · FergusArgyll · 6月18日 10:29 · [社区讨论](https://news.ycombinator.com/item?id=48583356)

**背景**: Git 的 .gitignore 是阻止跟踪某些文件的标准方式，但它常被误用于仅针对单个开发者环境的文件。Git 提供了不提交的本地忽略（per-repo local ignore）和针对用户的全局忽略（global ignore）。.gitattributes 则进一步扩展了对 Git 在差异比较、合并和归档操作中处理文件方式的控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.github.com/articles/ignoring-files">Ignoring files - GitHub Docs</a></li>
<li><a href="https://git-scm.com/docs/gitattributes">Git - gitattributes Documentation</a></li>
<li><a href="https://stackoverflow.com/questions/7335420/can-i-use-a-global-user-profile-scope-gitignore-file">Can I use a global (user-profile-scope) .gitignore file? Usage example</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞文章突出了鲜为人知的功能，不少人推荐使用全局忽略来避免在每个 .gitignore 中添加 IDE 文件。有人建议使用 ~/.config/git/ignore 作为全局忽略路径。另有人提到用 .gitattributes 隐藏诸如 package-lock.json 等嘈杂文件的差异，还有人分享技巧，如创建一个 attic 目录并在其中放置包含 "*" 的本地 .gitignore。

**标签**: `#Git`, `#configuration`, `#version control`, `#developer tools`

---

<a id="item-21"></a>
## [W Social：欧洲数字主权还是政治秀场？](https://blog.elenarossini.com/w-social-public-institutions-and-the-theater-of-european-digital-sovereignty/) ⭐️ 7.0/10

这篇博文批判性地审视了 2026 年 1 月推出的欧洲社交媒体平台 W Social，质疑其作为数字主权倡议的透明度和动机。 这很重要，因为它对欧洲推动数字主权的真实性提出了质疑，暗示 W Social 可能更注重政治便利，而非真正的去中心化和用户信任。 W Social 是一个营利性有限责任公司，而非非营利组织，并在世界经济论坛上亮相；欧盟高官迅速加入，而透明开放的替代方案 Eurosky 几乎没有获得媒体关注。

hackernews · nemoniac · 6月18日 12:46 · [社区讨论](https://news.ycombinator.com/item?id=48584497)

**背景**: 欧洲数字主权指的是减少对美国持有的平台（如 X 和 Meta）依赖的努力。W Social 要求身份验证，并声称基于欧洲法律和基础设施构建。批评者认为其闭源、营利结构与这些理想相矛盾，而欧盟则通过《数字服务法》等法规促进主权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wsocial.news/">W - The European social network for verified humans</a></li>
<li><a href="https://cybernews.com/tech/europe-social-media-w/">Europe is launching its own social media platform | Cybernews</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍表示怀疑，将其与 TruthSocial 相提并论，原因是其政治联系和不透明的运营。一位用户报告称，尽管有所谓的人类验证，仍能创建多个账户。其他人则指出 Eurosky 是一个被媒体忽视的透明替代方案。

**标签**: `#European digital sovereignty`, `#social media`, `#W Social`, `#decentralization`, `#public institutions`

---

<a id="item-22"></a>
## [GLM-5.2 引入 IndexShare 实现高效长上下文推理](https://sebastianraschka.com/blog/2026/glm-5-2-indexshare.html) ⭐️ 7.0/10

GLM-5.2 是 GLM-5 稀疏 MoE 模型的开源权重更新，引入了 IndexShare 方法，用于降低百万 token 动态稀疏注意力（DSA）推理成本。 这一进展显著降低了处理超长序列的计算成本，使长上下文大语言模型在代码生成、文档分析等实际应用中更加实用。 GLM-5.2 保留了 GLM-5 的稀疏 MoE 架构，并改进了其多 token 预测（MTP）层以实现推测解码，接受长度最多提升 20%。

rss · Sebastian Raschka · 6月18日 09:16

**背景**: 大语言模型常因注意力机制的二次复杂度而难以处理长上下文。稀疏注意力机制（如 DSA）通过仅关注相关 token 来减少计算。GLM-5 采用混合专家（MoE）架构，不同专家处理输入的不同部分。IndexShare 是一种通过跨 token 共享索引信息来进一步优化稀疏注意力的技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/ GLM - 5 . 2 · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/GLM-5.2">GLM-5.2</a></li>

</ul>
</details>

**标签**: `#GLM`, `#sparse attention`, `#long-context`, `#MoE`, `#efficient inference`

---

<a id="item-23"></a>
## [迈克尔·莫顿访谈：AI 时代电商的变革](https://stratechery.com/2026/an-interview-with-michael-morton-about-e-commerce-in-the-age-of-ai/) ⭐️ 7.0/10

迈克尔·莫顿探讨了 AI 如何重塑电子商务，重点关注分发模式与推荐模式的张力、生鲜配送的挑战以及自动驾驶汽车的作用。 这次访谈提供了对不断变化的电商格局的战略性见解，突显了 AI 驱动的变革可能重新定义零售业的商业模式和竞争动态。 关键话题包括不可证伪的看空论点——即无法被反驳的论点——以及在 AI 背景下分发模式（如亚马逊）与推荐模式（如联盟营销）的比较。

rss · Stratechery · 6月18日 10:00

**背景**: 分发模式涉及公司拥有库存和物流，而推荐模式则专注于将流量引导至第三方卖家。不可证伪的看空论点是指无法通过实证反驳的悲观论点，常用于投资辩论。访谈探讨了 AI 如何可能打破这些模型之间的平衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Falsifiability">Falsifiability - Wikipedia</a></li>
<li><a href="https://www.nostra.ai/blogs-collection/ecommerce-distribution-channels">What Are the Best Ecommerce Distribution Channels?</a></li>

</ul>
</details>

**标签**: `#e-commerce`, `#artificial intelligence`, `#distribution models`, `#grocery tech`, `#autonomous vehicles`

---

<a id="item-24"></a>
## [ChatGPT 定时任务新增 Scheduled 页面与监控通知](https://help.openai.com/en/articles/10291617-scheduled-tasks-in-chatgpt) ⭐️ 7.0/10

OpenAI 在 ChatGPT 侧边栏新增了 Scheduled 页面，用于集中管理一次性与重复任务，并引入了监控通知功能，可在检测到重要变化时发送提醒。 此次更新使 ChatGPT 成为更主动的助手，适用于定时提醒和自动监控，提升了 Plus、Pro、Business 和 Enterprise 用户的生产力。 该功能支持网页版和移动应用，但不支持桌面客户端和 Codex；不同套餐的活跃任务上限从 3 到 15 个不等，且不支持语音对话和 GPTs。

telegram · zaihuapd · 6月18日 04:20

**背景**: ChatGPT 的定时任务功能允许用户安排一次性或重复执行的 AI 提示。新增的 Scheduled 页面提供了集中管理功能。监控任务让 ChatGPT 定期检查变化并通知用户。Codex 是 OpenAI 的 AI 编程代理，GPTs 是自定义聊天机器人版本；定时任务功能不支持这两个平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(language_model)">OpenAI Codex (language model) - Wikipedia</a></li>
<li><a href="https://openai.com/index/introducing-gpts/">Introducing GPTs - OpenAI</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#OpenAI`, `#scheduled tasks`, `#monitoring`, `#AI assistant`

---

<a id="item-25"></a>
## [多款婴幼儿纸尿裤检出生殖毒性物质甲酰胺](https://www.sohu.com/a/1038121771_122014422) ⭐️ 7.0/10

《经济参考报》委托专业机构检测发现，好奇、碧芭宝贝、Babycare 等品牌婴幼儿纸尿裤中检出有毒物质甲酰胺。部分婴幼儿血液和尿液中也检出该物质，记者穿戴一款纸尿裤一夜后血液浓度飙升近一倍。 甲酰胺被列为生殖毒性物质，可通过皮肤吸收，对器官尚未发育完全的婴幼儿构成严重健康风险。该事件暴露出监管空白：我国纸尿裤国标暂未对甲酰胺设限，而化妆品目录中已禁用该物质。 甲酰胺在泡沫塑料制品中用作发泡剂，可使塑料更轻更柔韧，可能在纸尿裤生产过程中引入。专家指出，长期蓄积可能损害生殖系统及肝肾，呼吁尽快修订国标，补上监管空白。

telegram · zaihuapd · 6月18日 07:09

**背景**: 甲酰胺是一种工业化学品，常用作溶剂和塑料发泡剂。在纸尿裤等泡沫制品中，残留的甲酰胺可能释放并通过皮肤吸收。欧盟 REACH 法规对物品中甲酰胺的限值为 1000 mg/kg，但我国现行纸尿裤标准未将其纳入检测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.greature.cn/womendechanpin/zhudachanpin/1446.html">甲 酰 胺 _江苏巨莱生物医药有限公司</a></li>
<li><a href="https://inews.ifeng.com/53303283/news.shtml">多种儿童地垫存安全隐患：抽检35...</a></li>

</ul>
</details>

**标签**: `#consumer safety`, `#toxicology`, `#health hazard`, `#regulation`, `#infant care`

---

<a id="item-26"></a>
## [华为将 Wi-Fi 7 专利费定为每台设备 0.5 美元](https://36kr.com/newsflashes/3858656955847687) ⭐️ 7.0/10

华为宣布 Wi-Fi 7 设备的专利许可费率为每台 0.5 美元，遵循公平、合理、无歧视（FRAND）原则。这为行业内的 Wi-Fi 7 专利许可设定了基准。 这一公告意义重大，因为它为 Wi-Fi 7 的采用提供了明确性，并为其他公司可能遵循的专利许可费率树立了先例。它可能影响 Wi-Fi 7 设备的成本结构，并促进该技术的更广泛部署。 该费用适用于每台 Wi-Fi 7 设备，华为通过双边协议或专利池提供许可。截至 2024 年底，超过 12 亿部消费类电子设备已获得华为 Wi-Fi 专利的授权。

telegram · zaihuapd · 6月19日 00:09

**背景**: Wi-Fi 7 是最新一代基于 IEEE 802.11be 标准的无线网络技术，提供更高的速度、更低的延迟和更强的容量。FRAND（公平、合理、无歧视）许可是标准必要专利的常见政策，旨在确保公平访问的同时补偿专利持有人。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wi-fi_technology">Wi-fi technology</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reasonable_and_non-discriminatory_licensing">Reasonable and non-discriminatory licensing - Wikipedia</a></li>
<li><a href="https://www.u-blox.com/en/blogs/insights/wi-fi-7-next-generation-wi-fi-technology">Wi - Fi 7 : The next generation of Wi - Fi technology | u-blox</a></li>

</ul>
</details>

**标签**: `#Wi-Fi 7`, `#patent licensing`, `#Huawei`, `#intellectual property`, `#wireless technology`

---

<a id="item-27"></a>
## [GitHub Models 停止接纳新用户](https://github.blog/changelog/2026-06-16-github-models-is-no-longer-available-to-new-customers/) ⭐️ 7.0/10

GitHub 宣布自 2026 年 6 月 16 日起，GitHub Models 不再向新客户开放，这是该服务完全退役的第一步。 这一变化影响计划使用 GitHub 内置 AI 模型 playground 和 API 的组织，将新项目引向更全面的 AI 平台 Azure AI Foundry。 现有的 GitHub Models 用户仍可继续使用 Playground、API 及模型；详细的退役时间表后续将公布。

telegram · zaihuapd · 6月19日 00:54

**背景**: GitHub Models 是一个通过网页 playground 和 API 推理来原型设计和实验 AI 模型的平台，提供来自 OpenAI、Meta 等提供商的模型。Azure AI Foundry（前身为 Microsoft Foundry）是一个完全托管的平台，用于构建、部署和扩展 AI 代理，是微软战略性的 AI 开发中心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/GitHub_Models">GitHub Models</a></li>
<li><a href="https://grokipedia.com/page/Microsoft_Foundry_Agent_Service">Microsoft Foundry Agent Service</a></li>

</ul>
</details>

**标签**: `#GitHub`, `#AI Models`, `#Product Retirement`, `#Azure`

---

<a id="item-28"></a>
## [中国拟出台分布式数字身份互通互认规定](https://www.cac.gov.cn/2026-06/18/c_1783525605384124.htm) ⭐️ 7.0/10

该规定标志着中国有意建立国家级的分布式身份基础设施，有望增强用户对个人数据的控制权，并在金融、交通、海关、税务和数字人民币等领域实现无缝身份验证。 征求意见稿将分布式数字身份定义为包含标识符、密钥、可验证凭证和可验证声明的体系，并提出依托国家区块链网络建设身份链以支持跨平台互通互认。境内外个人、机构和工业设备均可自愿申请注册。

telegram · zaihuapd · 6月19日 01:39

**背景**: 分布式数字身份（DID）允许用户自主创建和管理标识符，无需依赖中央机构，利用区块链作为分布式账本。可验证凭证（VC）是经过数字签名和可验证的加密声明，能够实现保护隐私的身份验证。这种方式与传统中央集权身份系统（由单一实体控制用户数据）形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.metaguan.cn/web3/3544.html">DID 是 什 么 意思(WEB3去中心化 数 字 身 份 认证)_元宇宙观察</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/357716225">可验证凭证 – 数字身份的核心 - 知乎</a></li>
<li><a href="https://www.w3.org/zh-hans/press-releases/2025/verifiable-credentials-2-0/">W3C发布可验证凭证2.0标准：让数字凭证的表达、交换和验证更加便捷且...</a></li>

</ul>
</details>

**标签**: `#decentralized digital identity`, `#blockchain`, `#regulation`, `#China`

---

<a id="item-29"></a>
## [亚马逊可能对外销售 AI 芯片，挑战英伟达](https://finance.yahoo.com/technology/ai/articles/amazon-may-start-selling-custom-005304720.html) ⭐️ 7.0/10

据报道，亚马逊计划将其自研 AI 芯片（包括 Inferentia 和 Trainium）对外销售，不再仅限于内部使用。 此举可能挑战英伟达在 AI 芯片领域的近乎垄断地位，有望降低 AI 训练和推理的成本，并加剧市场竞争。 亚马逊的 Trainium3 性能是上一代的四倍以上，而 Inferentia 提供数百 TOPS 的推理性能。外部销售可能首先面向 AWS 合作伙伴。

openbb · AAPL · 6月19日 00:53

**背景**: 亚马逊开发了自研 AI 芯片，如用于推理的 Inferentia 和用于训练的 Trainium，目前已在 AWS 中使用以降低成本。英伟达凭借其 GPU 主导 AI 芯片市场。如果亚马逊对外销售这些芯片，可能动摇英伟达的地位，为 AI 公司提供更多选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS - aws.amazon.com</a></li>
<li><a href="https://aws.amazon.com/ai/machine-learning/inferentia/">AI Chip - Amazon Inferentia - AWS</a></li>
<li><a href="https://www.aboutamazon.com/news/aws/aws-trainium-graviton-ai-chips-explained">AWS Trainium and Graviton chips: How Amazon powers AI and ...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#Amazon`, `#Nvidia`, `#hardware`, `#market competition`

---

<a id="item-30"></a>
## [苹果的现金无法主宰内存市场](https://www.wsj.com/tech/why-apples-war-chest-cant-win-the-memory-war-cb997d02?siteid=yhoof2&yptr=yahoo) ⭐️ 7.0/10

《华尔街日报》的一篇分析指出，尽管苹果拥有巨额财务资源，但由于市场整合和供应链动态，它无法在存储芯片市场获得战略优势。 这很重要，因为苹果无法控制内存定价可能会影响其产品成本与利润率，同时也会影响到面临供应限制的 Android 制造商等竞争对手。 苹果一直在高价囤积移动 DRAM 以保障供应并阻止竞争对手，但这种策略牺牲了自身的利润率，且无法解决内存市场的周期性特点。

openbb · AAPL · 6月19日 00:00

**背景**: 存储芯片市场，尤其是 NAND 闪存和 DRAM，具有高度周期性，会出现供过于求和短缺的阶段。苹果作为主要买家，利用其购买力保障供应，但由于三星、SK 海力士和美光等供应商的整合，它无法控制市场。市场需求还受到数据中心和 AI 应用的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tradingkey.com/analysis/stocks/us-stocks/261750153-apple-dram-memory-hbm-supply-ai-chips-shortage-tradingkey">Apple Starts Buying Spree. All In on Mobile Storage DRAM at Any Cost. What Is the Reason?</a></li>
<li><a href="https://eu.36kr.com/en/p/3758859119444738">Apple Utilizes Supply Chain to Strangle Android as Consumers Rush to Buy Memory at Double the Price</a></li>
<li><a href="https://www.sourcengine.com/blog/nand-vs-dram-a-tale-of-two-markets">NAND vs DRAM: A Tale of Two Markets | Sourcengine</a></li>

</ul>
</details>

**标签**: `#Apple`, `#memory`, `#semiconductor`, `#hardware`, `#industry analysis`

---