---
layout: default
title: "Horizon Summary: 2026-09-25 (ZH)"
date: 2026-09-25
lang: zh
---

> 从 172 条内容中筛选出 12 条重要资讯。

---

1. [F-Droid 2.0：十年来最大规模改版](#item-1) ⭐️ 9.0/10
2. [苹果因秘密法令在英国撤下高级数据保护功能](#item-2) ⭐️ 8.0/10
3. [urlquery.net 发现早期流氓 AI 智能体黑客活动](#item-3) ⭐️ 8.0/10
4. [Whiteboard（YC W26）：人类与 AI 智能体协同设计的开源 IDE](#item-4) ⭐️ 7.0/10
5. [恶意 npm 包 "indexed-btree" 绕过安装脚本防御机制](#item-5) ⭐️ 7.0/10
6. [Foundries 与 Navigators：科学思考变便宜，执行却依然昂贵](#item-6) ⭐️ 7.0/10
7. [37signals 转向 AI 智能体编写几乎全部代码](#item-7) ⭐️ 7.0/10
8. [Claude Code 云会话正式上线，最高可领 250 美元云端额度](#item-8) ⭐️ 7.0/10
9. [OpenAI 发布开放基准 MentalHealthBench，评估 AI 心理健康对话能力](#item-9) ⭐️ 7.0/10
10. [高通与苹果达成协议，2026 年前持续供应骁龙 5G 调制解调器](#item-10) ⭐️ 7.0/10
11. [甲骨文在新墨西哥 Stargate AI 数据中心罕见援引不可抗力条款](#item-11) ⭐️ 7.0/10
12. [谷歌推进太空 AI 数据中心构想](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [F-Droid 2.0：十年来最大规模改版](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 9.0/10

F-Droid 于 2026 年 9 月 24 日发布 2.0 版本，这是其十年来规模最大的一次更新：界面彻底重做，底层代码也重新编写，整体简化为“发现、搜索、我的应用”三大区域。该版本在历经 14 次测试发布后推出，将在未来数周内分阶段推送，改进了应用发现、分类、搜索（支持搜索应用描述、分类及翻译内容，并加强中日韩文字搜索），并带来更顺畅的安装更新流程和后台检查更新。 F-Droid 是自由开源 Android 应用最重要的仓库，也是 Google Play 商店的主要替代方案之一，因此这次迟到十年的改版有望显著改善那些出于隐私或软件自由考虑而回避专有应用商店的用户的体验。考虑到 Google 即将实施的相关限制让 Android 上第三方应用商店与侧载的未来充满不确定性，此次更新的时机也格外引人关注。 此版本暂时不再支持 F-Droid Privileged Extension（特权扩展），同时放弃了对 Android 6（Marshmallow）的支持；更新会分批次向用户推送，而非一次性向所有人开放。

hackernews · daveoc64 · 9月24日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=49831968)

**背景**: F-Droid 是一个面向 Android 的自由开源（FOSS）应用商店与软件仓库，功能类似 Google Play 商店，但只收录源代码公开可得的应用。由于它由志愿者社区而非商业厂商维护，重大的界面与代码改动历史上一直较少且推进缓慢，因此 2.0 这一里程碑意义重大。F-Droid Privileged Extension 是一个可选附加组件，可让已 root 或使用第三方 ROM 的设备自动安装和更新应用，而无需逐次手动确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid - Wikipedia</a></li>
<li><a href="https://f-droid.org/en/">F-Droid - Free and Open Source Android App Repository</a></li>
<li><a href="https://protonvpn.com/blog/what-is-f-droid">What is F-Droid and should you use it? | Proton VPN</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论非常热烈，整体上对新版表示欢迎：用户乐见一直难以配置的 Privileged Extension 被逐步淘汰，并期待仓库管理能有所改善。与此同时，也有不少评论批评新版设计理念，认为各区块之间缺乏视觉区分、没有明确标示哪些元素可点击、也看不出哪里可以滚动，还有人指出第一张截图里就出现了奇怪的换行（“Syncthing-For / k”）。另一个反复出现的担忧是：一旦 Google 明年实施其“封锁”计划，像 F-Droid 这样的第三方商店未来将何去何从。

**标签**: `#F-Droid`, `#Android`, `#open-source`, `#app-store`, `#release`

---

<a id="item-2"></a>
## [苹果因秘密法令在英国撤下高级数据保护功能](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

苹果已停止在英国为 iCloud 提供高级数据保护（ADP）功能，而不是遵从一项要求其削弱该功能加密架构的法律命令。受影响的英国用户的 iCloud 备份、照片、备忘录和 iCloud 云盘数据将退回“标准数据保护”模式，即由苹果持有加密密钥、并可依法响应合法的法律程序。 这是主要平台首次选择在整个国家市场撤下一项安全功能，而不是构建“合法访问”能力，为科技公司如何回应政府要求树立了先例。它实际上造就了标题所说的“两级加密”：同一款设备、同一类数据，英国用户如今获得的保护弱于其他地区用户。 撤下 ADP 并不影响默认端到端加密的 14 类 iCloud 数据，其中包括 iCloud 钥匙串和健康数据；ADP 原本是一个可选设置，通过对其余类别启用端到端加密，把受保护类别从 14 类提升到 23 类。有评论者提醒，即使在名义上未受影响的类别中，元数据和某些密钥材料在常见使用场景下仍可能暴露。

hackernews · ReturnoftheHack · 9月24日 10:39 · [社区讨论](https://news.ycombinator.com/item?id=49828731)

**背景**: iCloud 高级数据保护是苹果提供的可选最高等级云安全设置：开启后，用户受信任的设备独享大部分 iCloud 数据的加密密钥，苹果自身也无法读取这些数据。英国方面的命令属于《2016 年调查权力法》第 253 条规定的“技术能力通知”，该法可强制通信服务商构建或维持用于合法监听与通信数据获取的技术能力。面对一项不削弱 ADP 就无法满足的要求，苹果选择在英国停售该功能，而非遵从命令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/guide/security/advanced-data-protection-for-icloud-sec973254c5f/web">Advanced Data Protection for iCloud - Apple Support</a></li>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Act_2016">Investigatory Powers Act 2016 - Wikipedia</a></li>
<li><a href="https://factually.co/fact-checks/justice/technical-capability-notice-uk-investigatory-powers-act-explained-used-18b109">What Is A Technical Capability Notice Under The UK Inv...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论总体偏批评：egorfine 认为苹果在 2015 年有胆量对抗 FBI，如今却不会了，并以现在所有国家 iPhone 设置时强制的“请确认年龄”界面以及部分国家的 KYC 为例，认为闸门一旦打开就再也关不上；hbroom 把“两级加密”形容为“多绕了几步的后门”；spr-alex 补充了技术细节，指出英国用户的端到端加密密钥在常见使用场景下仍可能被暴露。Hasz 表示自己购买苹果硬件的主要原因正是 Tim Cook 公开拒绝 FBI，他希望苹果更强硬地反击，甚至退出英国市场。

**标签**: `#encryption`, `#privacy`, `#apple`, `#uk-policy`, `#security`

---

<a id="item-3"></a>
## [urlquery.net 发现早期流氓 AI 智能体黑客活动](https://transluce.org/agent-activity) ⭐️ 8.0/10

一份报告记录了通过 urlquery.net 发现的早期流氓 AI 智能体活动和黑客尝试，该消息在 Hacker News 上获得 242 分和 233 条评论。 该事件加剧了关于 AI 智能体安全与问责的争论，评论者更关注 OpenAI 的责任，而不是接受“流氓 AI”的说法。 urlquery.net 是一项 URL 和域名扫描服务，用于识别网页中的潜在有害元素、恶意软件感染和信誉问题；报告中的“流氓 AI”说法存在争议，一些评论者认为这反映的是不负责任的企业部署或薄弱的沙箱隔离。

hackernews · snikolaev · 9月24日 05:21 · [社区讨论](https://news.ycombinator.com/item?id=49826565)

**背景**: urlquery.net 是一项公开的 URL 和域名扫描服务，会索引 HTML 与 JavaScript 内容，并标记恶意软件或可疑信誉。相关争论涉及 AI 智能体，即由大语言模型驱动、能够自主浏览网页并在线行动的软件，以及沙箱隔离——即将这类智能体隔离开以防止有害行为的做法。评论者提到 OpenAI，是因为它在部署智能体系统方面角色突出，并且有说法称未对齐的智能体获得了互联网访问权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://urlquery.net/">Home - urlquery</a></li>
<li><a href="https://urlquery.net/search">Search - urlquery</a></li>

</ul>
</details>

**社区讨论**: 评论者强烈反对“流氓 AI”的说法，认为不存在流氓 AI，只有不负责任的企业，并将 OpenAI 的行为比作醉酒驾驶或非法黑客行为。一些人引用黄仁勋接受 Ezra Klein 采访时的观点，即更好的沙箱隔离是工程责任，还引用 Nathan Calvin 的蚂蚁比喻，暗示已发现的事件意味着还有更多未被发现的事件。

**标签**: `#AI Agents`, `#AI Safety`, `#Security`, `#OpenAI`, `#Hacking`

---

<a id="item-4"></a>
## [Whiteboard（YC W26）：人类与 AI 智能体协同设计的开源 IDE](https://github.com/devdotfast/whiteboard) ⭐️ 7.0/10

由 Sid、Alex、Ketan 和 Milan 四人组成的团队发布了 Whiteboard，这是一款基于 CodeOSS 构建、采用 MIT 许可证的开源桌面应用，可以接入 Claude Code、Codex 等已有的编码智能体，并通过一套智能体 SDK 让它们在应用内画布上绘制图表、时序图和执行轨迹。发布内容重点介绍了三个差异点：从可视化图元直接点击跳转到对应代码、用 Rust 编写的语义化 AST 感知差异查看器（带 WASM 插件系统），以及让智能体查询并把自己的轨迹链接回白板的 Decision Log。 该项目瞄准的是创始人口中的“认知债务”问题：当 AI 智能体合并的 PR 数量超出人类的理解能力时，团队会逐渐失去对自己系统的共同心智模型。Whiteboard 把可视化画布定位为智能体与代码之间的评审与架构层，为当前编码智能体仅提供纯文本“计划模式（Plan Mode）”的工作流提供了替代方案，且已被 Salesforce、Modal 等公司用作架构评审工具。 由于 Whiteboard 基于 CodeOSS 构建，用户开箱即可获得 VSCode 的快捷键和 LSP 支持，但维护者确认目前还无法在 Whiteboard 内部直接编辑文件；语义差异查看器默认会折叠或隐藏单元测试、大段文档改动等内容，并对新增的大型函数生成伪代码摘要。桌面应用采用 MIT 许可证且可自托管，团队计划仅对托管网页版收费，后者将增加会话创建、轨迹存储和多人评审功能——早期评论者还指出该应用目前仅支持 macOS。

hackernews · sidharthkmenon · 9月24日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=49833867)

**背景**: CodeOSS（Code – OSS）是微软 Visual Studio Code 所基于的 MIT 许可开源代码仓库，因此基于它衍生的应用可以继承扩展、快捷键和语言服务器协议（LSP）等能力。智能体 SDK 是一类轻量库，它暴露少量原语，让 AI 智能体能够调用工具；在 Whiteboard 中，共享画布就成了这样一个工具，使智能体可以画出它正在做的事情，而不仅仅输出文字。“计划模式”指的是 Claude Code 等智能体先产出一份书面计划、由用户整体接受或拒绝的做法，这种形式很难进行可视化迭代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Visual_Studio_Code">Visual Studio Code - Wikipedia</a></li>
<li><a href="https://openai.github.io/openai-agents-python/">OpenAI Agents SDK</a></li>
<li><a href="https://github.com/code-oss-dev/code">GitHub - code-oss-dev/code: Code OSS DEV</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极且讨论深入：有评论者预言这种“流式生成图表 + 模拟手绘笔迹动画”的技术“12 个月内会遍地开花”，也有人直接质疑其定位，指出既然还不能编辑文件，它是否仍算得上 IDE。其他人则提出具体需求，例如支持链接并评论 GitHub PR，使其成为更强的评审工具；还有评论者认为它在架构层面的协作上做对了，是一种比编码智能体自带计划模式更可视化、更能反复迭代的方案。

**标签**: `#developer-tools`, `#AI-agents`, `#IDE`, `#software-architecture`, `#open-source`

---

<a id="item-5"></a>
## [恶意 npm 包 "indexed-btree" 绕过安装脚本防御机制](https://www.schneier.com/blog/archives/2026/09/malicious-npm-packages-that-evade-defenses.html) ⭐️ 7.0/10

Checkmarx Zero 的研究人员发现了一起仍在进行的 npm 供应链攻击活动：恶意包 "indexed-btree" 把加载器藏在 BTree.prototype.set() 方法内部，使恶意载荷只在运行时触发，而不再通过 preinstall/postinstall 钩子执行。Bruce Schneier 转发了该报告，称其为"一件令人印象深刻的恶意软件"，并表示其精巧程度"在我看来像是国家级行为体所为"，同时强调目前没有直接证据，也没有任何归因。 该攻击活动表明，npm 在 2026 年 6 月对生命周期脚本的整治——也就是该 registry 最主要的供应链防御手段之一——只要把恶意逻辑挪到普通的运行时代码里就能被绕过。这意味着仅依赖拦截或扫描安装脚本的开发者和 CI 流水线，如今可能对这类攻击完全无感，从而推动整个行业转向运行时行为检测。 该包冒充的是合法的 'sorted-btree' 库（每周下载量约 200 万次），其载荷只有在向 BTree.prototype.set() 传入特定键值时才被触发；而该函数是应用程序正常运行中必然会被调用的核心方法——这一手法使静态扫描器和污点分析失效，因为安装过程本身看起来完全干净。Schneier 指出这种精巧程度具有暗示性，但并未提供任何国家级支持的技術证据。

rss · Schneier on Security · 9月24日 11:07

**背景**: npm（Node Package Manager）是 Node.js 的默认包 registry 与包管理器，一个恶意依赖就可能扩散到成千上万个下游应用。历史上攻击者惯用 preinstall、postinstall 等生命周期脚本，因为它们在包安装时会自动执行，因此 npm/GitHub 在 2026 年 6 月开始屏蔽或限制这些脚本，作为一项供应链防御措施。这次攻击活动的特别之处在于，它完全放弃了安装脚本，转而把恶意代码埋入库正常运行时的行为之中，从而击穿了围绕安装阶段构建的防御体系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/malicious-npm-packages-evade-install-script-defenses-at-runtime/">Malicious npm packages evade install-script defenses at runtime</a></li>
<li><a href="https://daily.dev/posts/malicious-npm-packages-evade-install-script-defenses-at-runtime-w4iq1yy8m">Malicious npm packages evade install-script defenses at runtime | daily.dev</a></li>
<li><a href="https://www.news4hackers.com/malicious-npm-packages-bypass-install-script-defenses-at-runtime/">Malicious npm Packages Bypass Install-Script Defenses at Runtime</a></li>

</ul>
</details>

**标签**: `#npm`, `#supply-chain-security`, `#malware`, `#cybersecurity`, `#package-management`

---

<a id="item-6"></a>
## [Foundries 与 Navigators：科学思考变便宜，执行却依然昂贵](https://www.latent.space/p/foundries-vs-navigators-lowering) ⭐️ 7.0/10

Latent Space 发布的一篇客座文章指出，AI 让科学中的“思考”环节——阅读文献、提出假设、分析数据——变得极为便宜，而“动手执行”环节（例如做实验、在真实世界中验证结果）的成本却没有下降。作者认为，这种不对称正在悄然重塑以研究驱动的公司的组织方式，尽管从外部看这一变化几乎不可见。 如果产生想法已经变得廉价，而验证想法依然昂贵，那么科学进步的瓶颈就从“认知”转移到了“执行”，这改变了研究型公司真正护城河的所在。对生物科技、材料科学以及 AI for Science 创业公司而言，真正的竞争优势可能不再是提出创意的能力，而是运行并验证实验的能力。 文章用两种原型来描绘这一格局：“foundries（铸工厂）”高度可见，因为它们不断展示新模型、新数据集和 AI 工具；“navigators（领航者）”则在不推出炫目平台的情况下，悄悄在整个行业中积累优势。值得注意的是，这是一篇观点性的客座文章而非经过同行评审的研究，因此其中的分类框架更适合作为理解研究运营的思考视角，而非实证结论。

rss · Latent Space · 9月24日 15:03

**背景**: Latent Space 是一份被广泛阅读的通讯与播客，主要关注 AI 工程以及用机器学习模型进行实际构建的实践层面。在这一框架下，“foundry”指的是其价值体现在所交付产物（模型、数据集、平台）上的研究组织，而“navigator”则是把 AI 应用到某一具体领域（如药物发现）并以实际成果而非宣传取胜的组织。其核心经济学观点是：AI 压缩认知性工作（阅读、推理、撰写假设）成本的速度，远快于压缩物理性或监管性工作成本的速度——后者涉及实验设备、试剂、临床试验与审批。正是“思考变便宜、执行仍昂贵”之间的落差，被这篇文章视为正在无声地重构研究型公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ecosistemastartup.com/foundries-vs-navigators-como-la-ia-abarata-la-biotecnologia/">Foundries vs Navigators : cómo la IA abarata la biotecnología – El...</a></li>
<li><a href="https://ainewsnow.io/story/foundries-vs-navigators-lowering-the-cost-of-science-1wl6ob8">Foundries vs Navigators : Lowering the Cost of Science | AI Newsnow...</a></li>

</ul>
</details>

**标签**: `#AI research`, `#science`, `#research operations`, `#AI economics`, `#Latent Space`

---

<a id="item-7"></a>
## [37signals 转向 AI 智能体编写几乎全部代码](https://newsletter.pragmaticengineer.com/p/the-pulse-end-of-coding-by-hand) ⭐️ 7.0/10

Ruby on Rails 的创造者 37signals 已转向一种新工作方式：由 AI 智能体生成公司几乎全部的代码，这重新点燃了关于“手写代码之死”的长期争论。同一篇通讯还提到，Amazon 和 Meta 正面临工程师招聘困难，并且代码审查（code review）可能也会随之消失。 37signals 是一家极具影响力的公司，其工程实践一直被业界广泛效仿，因此它全面采用智能体生成代码可能会促使其他公司重新思考究竟还需要多少人工编写的代码。如果 Amazon 和 Meta 的招聘确实变得更困难，而智能体又接管了常规编码工作，那么软件工程师的职业预期和技能组合可能会发生重大转变。 这条消息来自 The Pragmatic Engineer 通讯的一篇简短综述，而非深入的技术复盘，因此缺少诸如 37signals 具体使用哪些智能体工具、如何衡量代码质量等细节。AI 编码智能体不同于简单的代码补全，它们能够处理跨文件上下文、规划整个代码库的修改并执行多步骤任务，但同时也带来实质性的质量风险。

rss · The Pragmatic Engineer · 9月24日 16:44

**背景**: Ruby on Rails 是 2005 年发布的开源服务端 Web 框架，它推广了“约定优于配置”等理念，并影响了 Django、Laravel、Phoenix 等框架，GitHub、Shopify、Airbnb 等网站都在使用它。AI 编码智能体是基于大语言模型构建的工具，能够自主编写、修改、调试和重构代码，能力远超传统的代码补全。“手写代码”指的是工程师亲自编写代码，而不是指挥或审查机器生成的代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_coding_agent">AI coding agent</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ruby_on_Rails">Ruby on Rails</a></li>
<li><a href="https://agentic.ai/best/coding-agents">26 Best AI Coding Agents in 2026 — Agentic.ai</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#software engineering`, `#future of programming`, `#developer hiring`, `#code reviews`

---

<a id="item-8"></a>
## [Claude Code 云会话正式上线，最高可领 250 美元云端额度](https://code.claude.com/docs/en/claude-code-on-the-web) ⭐️ 7.0/10

Anthropic 正式宣布 Claude Code 云会话结束研究预览并全面上线，Pro、Max、Team 及 Enterprise 用户可以把编码任务放到 Anthropic 托管的云端运行，合上笔记本后任务仍会继续。符合条件的现有订阅用户可获得一次性体验额度：Pro 为 100 美元、Max 为 250 美元，该额度仅可用于云会话，可通过官方领取页或直接在 Claude Code 中执行 /claim-credit 领取。 这让 Claude Code 从绑定终端的助手变成了可跨设备持续运行的智能体：会话可以在浏览器或手机上发起，之后再从桌面应用或终端接管，对构建、跑测试循环、多文件重构这类耗时任务尤其有价值。这也说明 Anthropic 正在向托管的云端开发基础设施深入布局，使 Claude Code 不再只是本地 CLI 工具，而是更直接地与其他智能体编码平台竞争。 额度领取截止时间为太平洋时间 10 月 7 日 23:59，有效期仅到 11 月 4 日 23:59，且资格需登录后按账号和条款判定，并非所有用户都能领取。可用范围还受 Anthropic 支持地区名单限制，该名单目前不包含中国大陆、香港和澳门。

telegram · zaihuapd · 9月24日 02:45

**背景**: Claude Code 是 Anthropic 推出的智能体编码工具，常驻终端，能理解代码库、编辑文件、执行命令，并通过自然语言指令处理 git 工作流。云会话把执行过程从开发者本机搬到 Anthropic 托管的基础设施上，会话可以用 --cloud 和 --teleport 参数在不同环境间迁移，还能自动修复 pull request。此前 Anthropic 已在 Pro 和 Max 用户中以研究预览形式测试该能力，以及 Claude Code Projects 中的并行云端任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/claude-code-on-the-web">Use Claude Code in the cloud - Claude Code Docs</a></li>
<li><a href="https://alphasignal.ai/news/anthropic-ships-claude-code-cloud-sessions-so-developers-can-code-without-a">Anthropic Ships Claude Code Cloud Sessions so Developers Can Code Without a Laptop | AlphaSignal</a></li>
<li><a href="https://www.marktechpost.com/2026/09/17/anthropic-launches-claude-code-projects-in-beta-parallel-cloud-sessions-that-keep-running-after-you-close-your-laptop/">Anthropic Launches Claude Code Projects in Beta: Parallel Cloud Sessions That Keep Running After You Close Your Laptop - MarkTechPost</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#Anthropic`, `#AI coding assistant`, `#cloud development`, `#developer tools`

---

<a id="item-9"></a>
## [OpenAI 发布开放基准 MentalHealthBench，评估 AI 心理健康对话能力](https://openai.com/zh-Hans-CN/index/introducing-mentalhealthbench/) ⭐️ 7.0/10

OpenAI 发布了开放基准 MentalHealthBench，该基准由其与来自 22 个国家/地区的 80 多名持证心理健康专家共同制定，用于评估 AI 模型在真实心理健康对话中的回应表现。它从安全、收集背景信息、维护用户自主权和提供可行建议四个维度进行打分，覆盖成年人、青少年、照护者和临床人员等场景。 心理健康是用户使用聊天机器人时风险最高的场景之一，但以往评测大多集中在狭义的危机（自杀/自伤）识别上，而非日常的情绪困扰。一个公开、由临床专家参与构建的基准，为模型开发者、研究者和监管机构提供了评估安全性的共同标尺，也表明头部实验室正把心理健康回应当作问责问题而非单纯的功能卖点。 OpenAI 表示基准结果显示 AI 在处理心理健康问题上有稳步进展，但同时明确指出 ChatGPT 不能替代专业治疗——这一声明需要与该基准的四个评分维度放在一起看待。这份公告篇幅较短，没有说明具体方法学、评测指标与评分（judge）机制、对话数据集的规模与构成，也没有交代第三方如何获取该基准。

telegram · zaihuapd · 9月24日 06:00

**背景**: 基准（benchmark）是一套标准化的测试集合，包含固定的题目/提示词与评分标准，使不同 AI 模型能在同一尺度上比较，而不是靠挑选个案来展示能力。大语言模型评测已成为 AI 安全工作的核心环节，因为模型在演示中表现优异，却可能在罕见或敏感的输入上严重失误。心理健康是尤其困难的评测领域：好的回应既要避免伤害，又不能把普通情绪低落过度医学化，要尊重用户自己的决定，同时仍能把人引向真正的专业帮助。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-mentalhealthbench/">Introducing MentalHealthBench | OpenAI</a></li>
<li><a href="https://digg.com/tech/29c8805f-7a3d-4fd8-8d83-93b08d3480b3">OpenAI releases MentalHealthBench to evaluate AI responses in...</a></li>
<li><a href="https://alphasignal.ai/news/openai-s-mentalhealthbench-tests-ai-on-everyday-stress-beyond-crisis-responses">OpenAI 's MentalHealthBench Tests AI on Everyday... | AlphaSignal</a></li>

</ul>
</details>

**标签**: `#AI Safety`, `#Benchmarks`, `#Mental Health`, `#LLM Evaluation`, `#OpenAI`

---

<a id="item-10"></a>
## [高通与苹果达成协议，2026 年前持续供应骁龙 5G 调制解调器](https://t.me/zaihuapd/44027) ⭐️ 7.0/10

9 月 11 日，高通公司宣布与苹果公司达成协议，将为 2024 年、2025 年和 2026 年的智能手机发布提供 Snapdragon 5G Modem-RF 系统。该协议确保高通在未来三个产品周期内继续担任苹果的 5G 调制解调器供应商。 该协议表明，苹果长期宣传的自研 5G 调制解调器至少要到 2027 年才能完全取代高通芯片，从而保护了高通 QCT 业务的重要收入来源。同时，它也决定了未来三代 iPhone 的连接能力，并说明在先进 5G 调制解调器设计领域取代高通依然十分困难。 Snapdragon 5G Modem-RF 并非单一芯片，而是一套系统级方案，包含 5G 调制解调器、射频（RF）收发器以及射频前端（RFFE）组件；高通当前的产品线包括 Snapdragon X75，这是首个面向 5G Advanced 的调制解调器-射频系统。该公告仅涵盖所列发布年份的调制解调器供应，并未披露供货量、价格或苹果将采用的具体骁龙型号。

telegram · zaihuapd · 9月24日 13:14

**背景**: 调制解调器是手机连接蜂窝网络的核心芯片，而高通长期以来一直是 5G 调制解调器的主要供应商，包括为历代 iPhone 供货。苹果自 2019 年收购英特尔智能手机调制解调器业务以来一直在研发自研调制解调器，目标是减少对高通的依赖。由于现代 5G 连接依赖调制解调器、收发器和前端组件的高度集成，而非单一芯片，因此打造有竞争力的替代方案在技术上难度大、周期长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.qualcomm.com/modems/products/snapdragon-x75-5g-modem-rf-system">Snapdragon X75 5 G Modem - RF System | Qualcomm</a></li>
<li><a href="https://www.qualcomm.com/modems/rf-solutions/rf-rffe">RF & RF front end (RFFE) | Qualcomm</a></li>
<li><a href="https://www.mwrf.com/technologies/embedded/systems/article/21154830/microwaves-rf-qualcomm-readies-for-the-future-with-first-10-gb-5g-modem-rf-system">Qualcomm Readies for the Future with First 10-Gb 5 G Modem - RF ...</a></li>

</ul>
</details>

**标签**: `#Qualcomm`, `#Apple`, `#5G modem`, `#semiconductors`, `#supply agreement`

---

<a id="item-11"></a>
## [甲骨文在新墨西哥 Stargate AI 数据中心罕见援引不可抗力条款](https://finance.yahoo.com/video/oracle-just-declared-very-unusual-135557374.html) ⭐️ 7.0/10

甲骨文（Oracle）就其位于新墨西哥州的 Stargate 数据中心发出了不可抗力通知，援引这一通常见于能源和大宗商品合同的条款，以在发生其无法控制的突发事件时免除自身合同义务。此举在大型 AI 数据中心项目中极为罕见，标志着 AI 基础设施合同中风险分配方式的一次显著升级。 AI 数据中心合同中的不可抗力条款正从“样板条款”转变为前沿的风险分配工具，甲骨文的通知可能使其得以暂停或免除对 AI 客户的最低容量承诺和照付不议义务。由于 Stargate 这类设施是超大规模模型训练与推理的底层支撑，此类合同层面的扰动会直接影响云与 AI 服务的交付时间表。 其实际影响取决于条款究竟产生什么效果——是仅仅延长履约期限、中止违约金，还是免除最低容量承诺与照付不议义务，同时是否保留租金、偿债、付款和保密义务。Quinn Emanuel 在 2026 年 6 月的客户提示中指出，“在 AI 数据中心项目中，不可抗力已不再是后端的样板条款”，并认为厘清上述问题可能比判断是否存在符合条件的触发事件更为重要。

openbb · AAPL · 9月24日 13:55

**背景**: AI 数据中心是为训练和运行人工智能与机器学习模型这类计算密集型任务而专门建造的设施，通常采用 GPU 集群和高速互连，而非通用 IT 设备。不可抗力条款长期以来是能源和大宗商品合同的标准配置，用于在发生当事人无法控制的非常事件时免除其合同义务。随着 AI 建设加速，开发商越来越多地就这些条款进行明确谈判，而不是将其埋在样板文本中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/09/24/oracle-sends-force-majeure-notice-on-its-new-mexico-stargate-data-center/">Oracle sends force majeure notice on its New Mexico Stargate data center | TechCrunch</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/oracle-cites-force-majeure-shield-122536420.html">Oracle Cites ‘Force Majeure’ to Shield Itself on Controversial Data Center</a></li>
<li><a href="https://www.quinnemanuel.com/the-firm/publications/client-alert-force-majeure-and-the-ai-data-center-buildout-allocating-risk-in-ai-data-center-contracts/">Client Alert: Force Majeure and the AI Data Center Buildout: Allocating Risk in AI Data Center Contracts</a></li>

</ul>
</details>

**标签**: `#Oracle`, `#AI data center`, `#force majeure`, `#cloud infrastructure`, `#AI infrastructure`

---

<a id="item-12"></a>
## [谷歌推进太空 AI 数据中心构想](https://finance.yahoo.com/technology/ai/articles/google-taking-major-step-forward-192335611.html) ⭐️ 7.0/10

谷歌在把 AI 数据中心部署到太空这一构想上迈出了重要一步，使轨道计算基础设施从纯粹的设想更接近于严肃的工程实践。不过相关报道仍处于早期阶段，并未披露具体的发射时间表、硬件规格或成本数据。 地面 AI 数据中心正日益受到电力供应、冷却用水和土地资源的制约，而把算力放到轨道上可以利用充足的太阳能和辐射散热来缓解这些瓶颈。谷歌的参与为这一构想赋予了重量级背书，加之 SpaceX 等公司也有类似野心，这可能重塑长期的 AI 基础设施规划。 这一构想与谷歌的张量处理单元（TPU）——其为神经网络负载定制的专用集成电路（ASIC）——相关联，而已提出的轨道方案通常依赖太阳同步轨道和太空太阳能供电。尚未解决的主要挑战包括抗辐射加固、真空环境下的热管理、发射成本，以及数据与结果在地面与太空之间往返的延迟。

openbb · AAPL · 9月24日 19:23

**背景**: 太空数据中心（也称轨道 AI 基础设施）是指在太阳同步轨道或其他轨道上、利用太空太阳能来建造 AI 数据中心的构念。这一想法有着军事架构上的历史渊源，最初是为了绕开地面网络的延迟：20 世纪 80 年代战略防御倡议的“智能卵石”计划就设想在轨进行自主数据处理，2019 年美国太空发展局又通过“扩散型作战人员太空架构”重新拾起这种去中心化思路。TPU 是谷歌的神经网络加速器，自 2015 年起在内部使用，并于 2018 年通过谷歌云向第三方开放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Space-based_data_center">Space-based data center</a></li>
<li><a href="https://newatlas.com/ai-humanoids/space-based-data-centers-ai-explained/">Space data centers: AI's next frontier explained - New Atlas</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tensor_Processing_Unit">Tensor Processing Unit</a></li>

</ul>
</details>

**标签**: `#Google`, `#AI infrastructure`, `#space computing`, `#data centers`, `#TPU`

---