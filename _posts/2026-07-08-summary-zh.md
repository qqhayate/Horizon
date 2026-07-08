---
layout: default
title: "Horizon Summary: 2026-07-08 (ZH)"
date: 2026-07-08
lang: zh
---

> 从 178 条内容中筛选出 32 条重要资讯。

---

1. [Januscape：潜伏 16 年的 KVM 漏洞可让虚拟机逃逸至宿主机](#item-1) ⭐️ 10.0/10
2. [欧盟议会二读推进聊天控制法](#item-2) ⭐️ 9.0/10
3. [AI 推理成本下降 50 倍，迎来智能体数据系统时代](#item-3) ⭐️ 9.0/10
4. [Anthropic 发布 Claude Sonnet 5，代理能力大幅提升](#item-4) ⭐️ 9.0/10
5. [DeepSeek 自研 AI 芯片，减少对英伟达华为依赖](#item-5) ⭐️ 9.0/10
6. [Kokoro：CPU 友好的高质量文本转语音模型](#item-6) ⭐️ 8.0/10
7. [欧盟聊天控制提案强制扫描加密消息](#item-7) ⭐️ 8.0/10
8. [微软裁掉 id Software 的 idTech 团队](#item-8) ⭐️ 8.0/10
9. [sqlite-utils 4.0 新增数据库模式迁移功能](#item-9) ⭐️ 8.0/10
10. [为扎克伯格写脚本：Meta 财报电话会议的战略指导](#item-10) ⭐️ 8.0/10
11. [中国开源 AI 模型威胁美国主导地位](#item-11) ⭐️ 8.0/10
12. [KDDI 网络攻击导致 1200 万邮箱和 700 万密码泄露](#item-12) ⭐️ 8.0/10
13. [谷歌新增“保存媒体”设置，用户上传内容用于 AI 训练](#item-13) ⭐️ 8.0/10
14. [中国计划五年投入 2 万亿元建设全国算力网络](#item-14) ⭐️ 8.0/10
15. [中国拟对顶尖 AI 模型实施出口管制](#item-15) ⭐️ 8.0/10
16. [Claude Fable 5 重新上线引发安全与访问争议](#item-16) ⭐️ 8.0/10
17. [英伟达 AI 系统因电路板问题推迟至 2028 年](#item-17) ⭐️ 8.0/10
18. [StreetComplete：让 OpenStreetMap 编辑变得简单有趣](#item-18) ⭐️ 7.0/10
19. [欧盟强制所有新车安装驾驶员监控摄像头](#item-19) ⭐️ 7.0/10
20. [PgDog：解决状态泄漏的新 Postgres 连接池](#item-20) ⭐️ 7.0/10
21. [高薪难留技术移民 德国面临人才流失](#item-21) ⭐️ 7.0/10
22. [98%的成功率：在关键场景中远远不够](#item-22) ⭐️ 7.0/10
23. [MemGUI-Agent：为长程 GUI 任务引入记忆机制](#item-23) ⭐️ 7.0/10
24. [谷歌起诉利用 Gemini AI 进行钓鱼诈骗的中国骗子](#item-24) ⭐️ 7.0/10
25. [2026 年科技就业市场：AI 浪潮与招聘错位](#item-25) ⭐️ 7.0/10
26. [Windows 11 漏洞吞噬高达 513 GB 存储](#item-26) ⭐️ 7.0/10
27. [new-api 修复计费漏洞，防止负数扣费](#item-27) ⭐️ 7.0/10
28. [英伟达 Blackwell 晶圆美国制造，封装仍需送台](#item-28) ⭐️ 7.0/10
29. [中国网络文学平台从拥抱 AI 转向严打 AI 生成内容](#item-29) ⭐️ 7.0/10
30. [加州纽约立法要求 3D 打印机安装枪支检测软件](#item-30) ⭐️ 7.0/10
31. [内存芯片危机加剧，SEMI 向华盛顿发出警告](#item-31) ⭐️ 7.0/10
32. [SpaceXAI 计划本周三与 Cursor 联合发布新 AI 模型](#item-32) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Januscape：潜伏 16 年的 KVM 漏洞可让虚拟机逃逸至宿主机](https://github.com/V4bel/Januscape) ⭐️ 10.0/10

研究人员公开了 Januscape（CVE-2026-53359）漏洞，这是首个同时影响 Intel 和 AMD 平台的 KVM/x86 虚拟机逃逸漏洞，并发布了概念验证代码。 该漏洞破坏了多租户 KVM 宿主机中的隔离边界，对公有云和所有虚拟化环境构成严重威胁。16 年的潜伏期凸显了 hypervisor 安全中的系统性风险。 该漏洞是 shadow MMU 模拟中的 use-after-free 缺陷，客户机无需特定硬件触发即可破坏宿主机内核的 shadow page 表。它影响 2010 年至 2026 年 6 月的 Linux 内核，PoC 可导致宿主机内核 panic。

telegram · zaihuapd · 7月7日 10:14

**背景**: KVM（基于内核的虚拟机）在没有或禁用硬件辅助虚拟化（如 AMD 的 NPT 或 Intel 的 EPT）时，使用 shadow page table 进行内存虚拟化。shadow MMU 负责同步客户机页表与宿主机物理地址。Use-after-free 是指内存被释放后仍然被引用，导致数据损坏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/16-year-old-linux-kvm-flaw-lets-guest.html">16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on Intel and AMD x86 Systems</a></li>
<li><a href="https://docs.kernel.org/virt/kvm/x86/mmu.html">The x86 kvm shadow mmu — The Linux Kernel documentation</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#KVM`, `#VM escape`, `#CVE`

---

<a id="item-2"></a>
## [欧盟议会二读推进聊天控制法](https://www.heise.de/en/news/Showdown-in-Strasbourg-The-unexpected-return-of-Chat-Control-1-0-11356680.html) ⭐️ 9.0/10

欧盟议会通过程序性操作，在二读中推进了有争议的聊天控制监控法，并计划于周四进行最终投票。 该法律威胁到整个欧盟的加密和数字隐私权，而程序性策略引发了对民主侵蚀和压制反对声音的担忧。 在二读中，修正或否决需要绝对多数（361 票），而批准只需出席议员的简单多数，这在夏季休会前为支持者提供了战术优势。

hackernews · miroljub · 7月7日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=48819008)

**背景**: 聊天控制官方名称为《儿童性虐待条例》（CSAR），是一项欧盟提案，要求消息平台扫描用户内容以查找儿童性虐待材料，从而实质上破坏端到端加密。尽管遭到隐私倡导者和技术专家的广泛反对，该提案仍被反复推动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://stateofsurveillance.org/articles/government/eu-chat-control-surveillance-architecture-2026/">EU Chat Control and CSAR: The 2026 Picture - State of ...</a></li>
<li><a href="https://edri.org/our-work/chat-control-what-is-actually-going-on/">Chat Control: What is actually going on? - European Digital ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对程序性策略表示失望，有人指出反复重提不受欢迎的法律会损害民主。另一人引用让-克洛德·容克的言论，称法律被逐步推进直至无法回头。

**标签**: `#EU Policy`, `#Surveillance`, `#Encryption`, `#Privacy`, `#Legislation`

---

<a id="item-3"></a>
## [AI 推理成本下降 50 倍，迎来智能体数据系统时代](http://bair.berkeley.edu/blog/2026/07/07/intelligence-is-free-now-what/) ⭐️ 9.0/10

GPT-4 级别推理成本从 2023 年初的每百万 token 约 30 美元降至不到 1 美元，部分供应商甚至低于 0.10 美元，中位数每年下降 50 倍。BAIR 博客文章认为，这种近乎免费的智能趋势要求数据系统实现范式转变，以支持作为用户、管理者和构建者的 AI 智能体。 这种戏剧性的成本降低使得大规模部署 AI 智能体进行知识工作在经济上可行，迫使数据系统重新设计以处理智能体工作负载。这一转变可能重新定义数据系统的架构方式，从服务于人类查询转向协调自主智能体群。 该博客指出了三个核心挑战：为智能体设计数据系统（将智能体作为主要用户）、由智能体组成的数据系统（管理长期运行任务的状态和协调）以及由智能体构建的数据系统（让智能体从头合成定制数据系统）。作者来自 UC Berkeley 的 EPIC 数据实验室，并指出即使前沿模型每一代都在大幅降价。

rss · BAIR Blog · 7月7日 09:00

**背景**: AI 推理成本按 token 计量，一个 token 大约对应 0.75 个单词。由于模型蒸馏、硬件改进和供应商竞争，价格急剧下降。AI 智能体是可以追求目标、使用工具并自主行动的软件系统，随着推理成本趋近于零，它们预计将成为数据系统的主要工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://benchlm.ai/llm-pricing-trends">LLM API Pricing History — How AI Model Costs Have Changed ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent</a></li>

</ul>
</details>

**标签**: `#AI costs`, `#inference pricing`, `#agents`, `#data systems`, `#BAIR`

---

<a id="item-4"></a>
## [Anthropic 发布 Claude Sonnet 5，代理能力大幅提升](https://t.me/zaihuapd/42404) ⭐️ 9.0/10

Anthropic 发布了 Claude Sonnet 5，这是迄今为止最强大的 Sonnet 系列模型，具备增强的代理能力，包括规划、使用浏览器和终端等工具并自主执行任务。它在推理、编码和知识工作方面优于 Sonnet 4.6，性能接近 Opus 水平但价格更低。 此次发布标志着在让先进 AI 代理能力更易获取且更经济方面迈出了重要一步，因为 Sonnet 5 以中端价格提供了接近旗舰的性能。这可能加速 AI 代理在编程、自动化和知识工作等领域的行业采用。 Claude Sonnet 5 即日起在所有套餐（Free、Pro、Max、Team、Enterprise）中可用，并成为 Free 和 Pro 层级的默认模型。定价为每百万输入 token 2 美元，输出 token 价格未公布，限时优惠至 2026 年 8 月 31 日。

telegram · zaihuapd · 7月7日 09:02

**背景**: Claude 是 Anthropic 开发的一系列大型语言模型，以克劳德·香农命名。Sonnet 层级是中端选项，在能力与成本之间取得平衡，而 Opus 是顶级旗舰。'代理能力'指模型自主规划、使用外部工具（如网页浏览器或命令行界面）以及执行多步骤任务的能力。Sonnet 5 引入了实时网络安全防护，以防止在代理场景中被滥用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-sonnet-5">Introducing Claude Sonnet 5 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/whats-new-sonnet-5">What's new in Claude Sonnet 5 - Claude Platform Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Sonnet">Claude Sonnet</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#model release`, `#agent capabilities`

---

<a id="item-5"></a>
## [DeepSeek 自研 AI 芯片，减少对英伟达华为依赖](https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/) ⭐️ 9.0/10

中国 AI 公司 DeepSeek 正在自研 AI 芯片，专注于推理环节，以减少对英伟达和华为芯片的依赖。该项目始于约一年前，目前仍处于早期阶段。 此举可能重塑 AI 硬件供应链，加剧中美科技竞争，因为 DeepSeek 试图绕过先进芯片的出口限制。这也标志着 AI 公司向垂直整合芯片设计的趋势。 该芯片仅用于推理（运行已训练模型生成答案），而非训练。DeepSeek 已开始接触芯片设计、代工和存储公司，并近几个月私下招募芯片设计工程师。

telegram · zaihuapd · 7月7日 11:08

**背景**: AI 芯片是专门用于加速机器学习任务的硬件。推理是将训练好的模型应用于新数据以产生输出的阶段，而训练是从数据中学习的过程。美国的出口管制限制了中国公司获取英伟达 H100 等先进芯片，促使中国企业寻求华为昇腾等替代品或自研芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/629035506">人工智能中训练和推理的区别和联系 - 知乎</a></li>

</ul>
</details>

**标签**: `#AI chip`, `#DeepSeek`, `#US-China tech rivalry`, `#inference`, `#hardware`

---

<a id="item-6"></a>
## [Kokoro：CPU 友好的高质量文本转语音模型](https://ariya.io/2026/03/local-cpu-friendly-high-quality-tts-text-to-speech-with-kokoro/) ⭐️ 8.0/10

Kokoro 是一个拥有 8200 万参数的开源权重文本转语音模型，能在 CPU 上高效生成高质量语音，无需 GPU 即可实现本地 TTS。 它让没有专用 GPU 的用户也能使用高质量 TTS，支持保护隐私的离线应用，并降低了开发者及无障碍工具对硬件的门槛。 尽管参数仅 8200 万，Kokoro 却能媲美更大模型的质量，支持多语言、语音混合以及手动 IPA 发音指南以提高准确性。

hackernews · speckx · 7月7日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=48821576)

**背景**: 传统的高质量文本转语音模型通常因体积庞大而需要强大的 GPU，限制了本地部署。Kokoro 是一种轻量级开源权重替代方案，在 CPU 上实现相近质量，减少硬件依赖，支持私密离线使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/hexgrad/kokoro">GitHub - hexgrad/kokoro: https://hf.co/hexgrad/Kokoro-82M</a></li>
<li><a href="https://github.com/nazdridoy/kokoro-tts">GitHub - nazdridoy/kokoro-tts: A CLI text-to-speech tool ...</a></li>
<li><a href="https://kokorottsai.com/">Kokoro TTS: Advanced AI Text-to-Speech Model with 82M parameters</a></li>

</ul>
</details>

**社区讨论**: 用户对 Kokoro 的评价积极，尤其赞赏其 CPU 效率和手动 IPA 支持。部分用户指出其对单字或同形异义词的处理有局限，也有用户分享了 Linux 下的替代方案如 voiceio。

**标签**: `#TTS`, `#text-to-speech`, `#machine-learning`, `#open-source`, `#CPU-friendly`

---

<a id="item-7"></a>
## [欧盟聊天控制提案强制扫描加密消息](https://fightchatcontrol.eu/chat-control-overview) ⭐️ 8.0/10

欧盟的“聊天控制”提案（1.0 和 2.0 版本）将要求消息服务提供商扫描加密通信以查找儿童性虐待材料（CSAM）。1.0 版本允许自愿扫描，而 2.0 版本强制扫描，可能破坏端到端加密。 该立法对数字隐私和加密构成重大威胁，因为它将允许大规模监控私人消息。它影响所有欧盟公民，并可能影响全球加密政策。 聊天控制 1.0 提供了 ePrivacy 指令的临时豁免以允许自愿扫描，但已于 2024 年到期；然而，Google、Meta 和 Microsoft 等主要提供商继续扫描。聊天控制 2.0 旨在强制扫描，包括在消息加密前的客户端扫描。

hackernews · gasull · 7月7日 14:23 · [社区讨论](https://news.ycombinator.com/item?id=48818311)

**背景**: 端到端加密确保只有发送者和接收者可以读取消息，但客户端扫描会在加密前在设备上扫描内容。欧盟认为这对于打击儿童性虐待材料是必要的，但批评者警告这破坏了隐私，并可能被用于监控。这些提案在技术专家和隐私倡导者中引发了广泛辩论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://www.patrick-breyer.de/en/posts/chat-control/">Chat Control: The EU's CSAM scanner proposal</a></li>
<li><a href="https://www.internetsociety.org/resources/doc/2020/fact-sheet-client-side-scanning/">Fact Sheet: Client-Side Scanning - Internet Society</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍反对这些提案，强调了隐私和民主问题。一些人指出，虽然每个人都想制止虐待儿童，但广泛的监控是过度行为，可能被滥用。其他人指出，客户端扫描会破坏端到端加密的信任模型。

**标签**: `#privacy`, `#encryption`, `#surveillance`, `#EU legislation`, `#CSAM`

---

<a id="item-8"></a>
## [微软裁掉 id Software 的 idTech 团队](https://gamefromscratch.com/microsoft-fire-idtech-team-at-id-software/) ⭐️ 8.0/10

微软裁掉了 id Software 整个 idTech 引擎团队，该团队负责开发《毁灭战士》和《雷神之锤》等游戏。此举可能意味着未来将转向使用 Unreal Engine 5。 这一决定可能导致游戏引擎在 Unreal 下趋于同质化，减少行业的技术多样性和创新。同时也引发了对微软削弱所收购工作室独特技术战略的担忧。 据报道，裁员包括了整个 idTech 团队，该团队负责开发 id Software 游戏所使用的专有引擎。微软和 id Software 尚未提供官方确认。

hackernews · bauc · 7月7日 15:33 · [社区讨论](https://news.ycombinator.com/item?id=48819244)

**背景**: idTech 是 id Software 开发的专有游戏引擎系列，以驱动《毁灭战士》和《雷神之锤》等标志性游戏而闻名。该引擎经历了包括 id Tech 5、6 和 7 在内的多个版本。微软于 2021 年收购了 id Software 的母公司 ZeniMax Media。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Id_Tech">id Tech - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Id_tech_5_engine">Id tech 5 engine</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍批评此举，许多人认为裁掉引擎团队是短视行为，将引擎垄断权拱手让给 Epic Games。一些评论者指出缺乏确凿证据，但仍对同质化和技术文化流失表示担忧。

**标签**: `#Microsoft`, `#id Software`, `#game engines`, `#corporate strategy`, `#layoffs`

---

<a id="item-9"></a>
## [sqlite-utils 4.0 新增数据库模式迁移功能](https://simonwillison.net/2026/Jul/7/sqlite-utils-4/#atom-everything) ⭐️ 8.0/10

sqlite-utils 4.0 于 2026 年 7 月 7 日发布，新增了通过 Python 迁移文件实现的数据库模式迁移功能、通过新的 db.atomic() 方法实现的嵌套事务，以及对复合外键的支持。 此次重大更新填补了流行 SQLite 工具的关键空白，实现了版本控制的模式变更和更安全的事务操作，使使用 SQLite 构建数据驱动应用的开发者受益。 迁移系统利用 table.transform() 方法，该方法实现了 SQLite 推荐的创建临时表、复制数据并重命名的模式。嵌套事务通过一个上下文管理器支持，允许在现有事务内使用原子块。

rss · Simon Willison · 7月7日 19:32

**背景**: sqlite-utils 是由 Simon Willison 创建的 Python 库和命令行工具，用于操作 SQLite 数据库。它提供从 JSON/CSV 导入数据、运行 SQL 查询以及转换表等功能。在 v4.0 之前，该工具缺少对模式迁移和嵌套事务的内置支持，需要手动处理数据库演化。复合外键允许多列外键引用，增强了关系完整性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/sqlite-utils">GitHub - simonw/sqlite-utils: Python CLI utility and library ...</a></li>
<li><a href="https://pypi.org/project/sqlite-utils/">sqlite-utils · PyPI</a></li>
<li><a href="https://sqlite-utils.datasette.io/">sqlite-utils</a></li>

</ul>
</details>

**标签**: `#sqlite-utils`, `#database migrations`, `#SQLite`, `#schema management`, `#open source`

---

<a id="item-10"></a>
## [为扎克伯格写脚本：Meta 财报电话会议的战略指导](https://stratechery.com/2026/a-script-for-mark-zuckerberg/) ⭐️ 8.0/10

Ben Thompson 发表了一篇建议脚本，供马克·扎克伯格在 Meta 下一次财报电话会议上使用，提供了战略定位建议。 这一分析可能影响 Meta 向投资者传达其战略的方式，从而可能影响市场看法和股价表现。 该脚本针对 Meta 当前面临的挑战量身定制，包括 AI 投资和元宇宙愿景，同时维持投资者信心。

rss · Stratechery · 7月7日 10:00

**背景**: Ben Thompson 是知名的科技分析师，撰写专注于科技战略的博客 Stratechery。他的观点在硅谷常具有影响力。财报电话会议是公司每季度讨论财务结果和未来展望的活动，精心准备的脚本可以塑造投资者情绪。

**标签**: `#Meta`, `#earnings call`, `#Mark Zuckerberg`, `#strategy`, `#Stratechery`

---

<a id="item-11"></a>
## [中国开源 AI 模型威胁美国主导地位](https://www.japantimes.co.jp/commentary/2026/07/07/world/china-shock-shakes-silicon-valley/) ⭐️ 8.0/10

据近期评论，以 DeepSeek-V3 为代表的中国开源大语言模型如今被广泛视为对美国 AI 产业的重大生存威胁。 这一转变可能重塑全球 AI 竞争格局，因为来自中国的开源模型以低成本提供高性能，可能削弱 OpenAI 和 Google 等美国公司的竞争优势。 截至 2025 年中，中国在全球约 3755 个公开发布的大语言模型中占了 1509 个，远超其他国家，像 DeepSeek-V3（671B 参数）这样的模型在基准测试上达到了最先进水平。

rss · The Japan Times · 7月7日 06:57

**背景**: 开源 AI 模型以宽松许可证发布，允许任何人自由使用、修改和部署。中国在 AI 领域投入巨大，目前在开源大语言模型数量上领先，挑战了以美国为中心的专有 AI 生态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://intuitionlabs.ai/articles/chinese-open-source-llms-2025">An Overview of Chinese Open-Source LLMs (Sept 2025)</a></li>

</ul>
</details>

**标签**: `#AI`, `#open-source`, `#China`, `#Silicon Valley`, `#competition`

---

<a id="item-12"></a>
## [KDDI 网络攻击导致 1200 万邮箱和 700 万密码泄露](https://www.japantimes.co.jp/business/2026/07/07/companies/kddi-passwords-number/) ⭐️ 8.0/10

日本大型电信公司 KDDI 遭受网络攻击，导致 1200 万个电子邮件地址和 700 万个密码泄露。受影响的用户需要在未来几天内更改密码。 此次泄露影响了数百万 KDDI 用户，可能导致身份盗窃和其他网络犯罪。这凸显了在大型电信网络中，强大密码安全性和快速事件响应的持续关键重要性。 泄露的数据包括电子邮件地址和密码，密码可能经过哈希处理，但仍需立即更改。KDDI 已敦促用户及时更改密码并采取额外的安全措施。

rss · The Japan Times · 7月7日 03:23

**背景**: KDDI 是日本最大的电信运营商之一，为数百万人提供移动、固定电话和互联网服务。如此规模的数据泄露如果用户重复使用密码，通常会导致其他服务账户也被入侵，因此更改密码至关重要。

**标签**: `#cybersecurity`, `#data breach`, `#KDDI`, `#password security`, `#privacy`

---

<a id="item-13"></a>
## [谷歌新增“保存媒体”设置，用户上传内容用于 AI 训练](https://techcrunch.com/2026/07/06/if-you-use-google-youre-training-its-ai-heres-how-to-opt-out/) ⭐️ 8.0/10

谷歌在搜索服务历史记录中新增了“保存媒体”设置，用户通过 Google Lens、Search Live、语音搜索等产品上传的媒体文件可能被保存并用于改进谷歌的 AI 模型。用户可以在账户设置中关闭该设置以选择退出。 这一变化扩大了谷歌可用于 AI 训练的数据范围，引发了数十亿用户的重大隐私担忧。同时，它为用户提供了明确的退出机制，但默认是开启状态，意味着大多数用户将在不知情的情况下贡献其数据。 该设置适用于来自 Google Lens、Search Live、语音搜索和翻译口语练习的上传内容，包括图片、文件、音频和视频。在“搜索服务历史记录”中关闭“保存媒体”可阻止后续存储，但不会删除之前已保存的数据。

telegram · zaihuapd · 7月7日 04:00

**背景**: Google Lens 允许用户通过拍摄的照片进行搜索，Search Live 支持与搜索引擎进行实时语音对话。语音搜索和翻译口语练习同样依赖音频录制。这些功能因其便捷的免提搜索而广受欢迎，但用户可能未意识到其上传的媒体可能被重新用于 AI 训练。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/07/06/if-you-use-google-youre-training-its-ai-heres-how-to-opt-out/">If you use Google, you're training its AI. Here's how to opt out. | TechCrunch</a></li>
<li><a href="https://www.engadget.com/2208978/google-now-uses-your-uploaded-search-media-to-train-ai/">Google Now Uses Your Uploaded Search Media To Train AI - Engadget</a></li>
<li><a href="https://support.google.com/websearch/answer/16329036?hl=en&co=GENIE.Platform=Android">Have a real-time conversation with Live in Search</a></li>

</ul>
</details>

**标签**: `#Google`, `#Privacy`, `#AI Training`, `#Settings`, `#User Data`

---

<a id="item-14"></a>
## [中国计划五年投入 2 万亿元建设全国算力网络](https://t.me/zaihuapd/42399) ⭐️ 8.0/10

中国宣布计划未来五年投入约 2 万亿元（2950 亿美元）建设全国互联数据中心网络，优先采用华为等本土供应商的 AI 芯片，要求国产占比至少八成。 这项大规模基础设施投资旨在减少中国对英伟达、AMD 等外国芯片制造商的依赖，同时通过统一网络使计算资源更易获取，加速各行业的 AI 应用开发。 该计划是北京'六网'基础设施计划的关键一环，中国电信、中国联通等国有电信运营商已推出 token 套餐，将算力像移动数据一样打包销售。

telegram · zaihuapd · 7月7日 04:45

**背景**: 中国的'六网'基础设施计划包括水网、电网、通信网、算力网、物流网和地下管网，旨在构建现代化基础设施体系。算力网络旨在将分散的区域算力资源整合为统一的全国网络，使企业和公共部门更易获得高性能计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gov.cn/lianbo/202605/content_7070126.htm">统筹建设、动态推进“六张网” - 中国政府网</a></li>
<li><a href="https://news.qq.com/rain/a/20260518A05V3X00">Token套餐全面上线!三大运营商悉数入局，算力进入“按Token收费”时代_...</a></li>

</ul>
</details>

**标签**: `#算力网络`, `#AI芯片`, `#基础设施`, `#中国科技`

---

<a id="item-15"></a>
## [中国拟对顶尖 AI 模型实施出口管制](https://www.reuters.com/world/beijing-is-looking-curbing-overseas-access-chinas-top-ai-models-sources-say-2026-07-07/) ⭐️ 8.0/10

中国商务部召集阿里巴巴、字节跳动和智谱 AI 等企业开会，讨论限制最先进的国产 AI 模型（包括尚未发布的模型）向海外提供访问。 这一政策转向可能通过限制外国实体获取中国 AI 模型来显著影响全球 AI 发展和竞争，并可能加速技术脱钩。 限制范围仍在商讨中，可能仅适用于未来发布的新模型。AI 核心技术的泄露或窃取可能被定为危害国家安全罪。

telegram · zaihuapd · 7月7日 11:42

**背景**: 美国已对 AI 模型权重实施出口管制，例如 ECCN 4E091 要求对向中国实体转移某些先进 AI 模型申请许可证。中国的举措类似，旨在防止技术泄露并保持 AI 领域的竞争优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hankunlaw.com/portal/article/index/cid/8/id/15704.html">AI管制前沿 — 美国出口管制政策观察</a></li>

</ul>
</details>

**标签**: `#AI`, `#regulation`, `#China`, `#export control`, `#policy`

---

<a id="item-16"></a>
## [Claude Fable 5 重新上线引发安全与访问争议](https://t.me/zaihuapd/42415) ⭐️ 8.0/10

Anthropic 于 2026 年 7 月 1 日在美国解除出口管制后重新部署了 Claude Fable 5，但用户反馈体验下降，访问配额减少且安全误判频发。 这一事件凸显了前沿 AI 模型中安全性与可用性之间的张力，直接影响依赖 Claude 进行编程和研究工作的开发者。 到 7 月 7 日之前，Pro 和 Max 订阅者仅能用每周 50% 的额度调用 Fable 5；之后该模型将不再包含在订阅中，改为按量付费。模型的安全分类器会自动将包含“漏洞”、“hook”、“C/C++”或“Rust”等关键词的查询降级到较旧的 Opus 4.8 模型。

telegram · zaihuapd · 7月7日 18:01

**背景**: Claude Fable 5 是 Anthropic 的旗舰大语言模型，以高级推理和编程能力著称。为了平衡安全与性能，Anthropic 采用了激进的安全分类器，将敏感查询路由到能力较弱的模型。此次重新部署之前，出口管制限制了其可用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/redeploying-fable-5">Redeploying Claude Fable 5 \ Anthropic</a></li>
<li><a href="https://www.mindstudio.ai/blog/claude-fable-5-safety-guardrails-what-gets-blocked">Claude Fable 5 Safety Guardrails: What Gets Blocked, What ...</a></li>

</ul>
</details>

**社区讨论**: 在 Telegram 上，开发者表达了强烈不满，称频繁的安全误判扰乱了编程工作流，并批评访问配额减少是“挂羊头卖狗肉”的做法。

**标签**: `#AI`, `#Safety`, `#Claude`, `#Subscription`, `#Model Access`

---

<a id="item-17"></a>
## [英伟达 AI 系统因电路板问题推迟至 2028 年](https://finance.yahoo.com/technology/ai/articles/circuit-board-problem-just-delayed-211831216.html) ⭐️ 8.0/10

据研究公司 SemiAnalysis 报道，英伟达下一代 AI 机架系统（名为 Kyber）因印刷电路板问题被推迟超过 12 个月至 2028 年。这一延迟导致芯片股立即下跌。 这一延迟影响了整个 AI 硬件路线图，因为英伟达的 Rubin Ultra 芯片本应推动下一波 AI 计算。它还影响了供应链时间表和投资者信心，股市反应即为明证。 Kyber 机架级架构设计用于容纳英伟达 2027 年的 Rubin Ultra 芯片，但 PCB 问题将生产推迟到 2028 年。问题源于高电流 AI 芯片的电源传输挑战，跨 PCB 传输电源成为限制因素。

openbb · AAPL · 7月7日 21:18

**背景**: 英伟达的 AI 系统依赖于复杂的机架级架构，集成多个高功耗芯片。随着 AI 芯片功耗达到数百瓦，通过印刷电路板供电成为关键设计挑战。行业正在转向 800 VDC 配电以解决这些问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/06/nvidia-kyber-rack-system-delays-manufacturing-taiwan-rubin-chips-.html">Nvidia's next-gen AI rack system delayed to 2028 on ... - CNBC</a></li>
<li><a href="https://semiengineering.com/power-delivery-challenges-for-ai-chips/">Power Delivery Challenges For AI Chips</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI hardware`, `#semiconductor`, `#stock market`, `#delay`

---

<a id="item-18"></a>
## [StreetComplete：让 OpenStreetMap 编辑变得简单有趣](https://streetcomplete.app/) ⭐️ 7.0/10

StreetComplete 是一款 Android 应用，将 OpenStreetMap 贡献转化为简单的、游戏化的小任务，用户通过回答诸如“这里的营业时间是什么？”之类的问题来补充缺失的地图数据。 它显著降低了新手参与 OpenStreetMap 的门槛，提高了数据完整性和社区参与度，从而帮助保持地图对所有人的准确性和最新性。 该应用在地图上显示任务标记，每个任务可通过在现场回答一个简单问题来完成；答案直接上传到 OSM 数据库。v59.0 版本将渲染器从 Tangram-ES 迁移到了 MapLibre。

hackernews · kls0e · 7月7日 12:38 · [社区讨论](https://news.ycombinator.com/item?id=48816883)

**背景**: OpenStreetMap（OSM）是一个协作项目，旨在创建免费、可编辑的世界地图，但传统贡献方式需要了解复杂的标签方案。StreetComplete 通过根据位置上下文提出特定的选择题或文本问题来简化这一过程，使任何人都无需 OSM 专业知识即可参与贡献。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/StreetComplete">StreetComplete</a></li>
<li><a href="https://streetcomplete.app/">StreetComplete</a></li>
<li><a href="https://wiki.openstreetmap.org/wiki/StreetComplete">StreetComplete - OpenStreetMap Wiki GitHub - streetcomplete/StreetComplete: Easy to use ... StreetComplete - Apps on Google Play StreetComplete - Wikipedia Releases · streetcomplete/StreetComplete - GitHub StreetComplete | F-Droid - Free and Open Source Android App ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍非常积极，用户称该应用“非常有趣”且“对初学者友好”。一些用户指出了局限性，例如无法添加新的道路或人行道，另有一位用户对谷歌可能使用 OSM 数据而未有回馈表示担忧。

**标签**: `#OpenStreetMap`, `#gamification`, `#mapping`, `#open data`, `#crowdsourcing`

---

<a id="item-19"></a>
## [欧盟强制所有新车安装驾驶员监控摄像头](https://allaboutcookies.org/eu-mandatory-distracted-driver-system) ⭐️ 7.0/10

欧盟颁布了一项法规，要求在其境内销售的所有新车都必须配备驾驶员监控摄像头系统。该规定作为更广泛车辆安全标准的一部分，自 2026 年起对新车型生效，2028 年起对所有新车生效。 该法规是汽车安全领域的重要一步，有望减少因驾驶员分心和困倦引发的事故。但同时也引发了隐私担忧，并可能因摄像头持续监测驾驶员行为而影响用户体验。 该系统使用红外摄像头跟踪头部位置、视线方向和眨眼模式，以检测分心或困倦。预计将与高级驾驶辅助系统（ADAS）集成，并在无响应时触发警告甚至减速车辆。

hackernews · nickslaughter02 · 7月7日 20:50 · [社区讨论](https://news.ycombinator.com/item?id=48823557)

**背景**: 驾驶员监控系统（DMS）自 2006 年便在高端车型中使用，但欧盟法规使其成为所有细分市场的标配。Euro NCAP 2026 年协议大幅提高了驾驶员参与度的权重，促使制造商采用更先进的 DMS。该法规旨在通过确保驾驶员警觉性来支持向自动驾驶的过渡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Driver_monitoring_system">Driver monitoring system</a></li>
<li><a href="https://www.euroncap.com/safe-driving/">Euro NCAP | Safe Driving | Protocols & technical bulletins</a></li>
<li><a href="https://smarteye.se/blog/driver-monitoring-euro-ncap-2026/">Driver Monitoring 2.0: How Euro NCAP is Raising the Bar in ...</a></li>

</ul>
</details>

**社区讨论**: 评论反映了复杂的反应：一些用户认为新车技术烦人且侵犯隐私，而另一些用户则承认潜在的安全益处。有用户提到其福特 Blue Cruise 系统能准确检测分心而无误报，表明该技术可能是有效的。关于用户体验问题和政府过度干预的担忧也很突出。

**标签**: `#automotive`, `#privacy`, `#EU regulation`, `#driver monitoring`, `#safety`

---

<a id="item-20"></a>
## [PgDog：解决状态泄漏的新 Postgres 连接池](https://pgdog.dev/blog/why-yet-another-connection-pooler) ⭐️ 7.0/10

状态泄漏是连接池中一个关键但常被忽视的问题；PgDog 修复了这个问题，并高效处理 NOTIFY，这对实时应用很重要。其选择 AGPL 许可证可能影响行业趋势，推动更强的开源保护。 PgDog 用 Rust 编写，声称与现有 Postgres 客户端兼容，并引入了一种新颖的方法来隔离每个客户端的会话状态。它通过批量处理通知来优化 NOTIFY，避免每连接开销。

hackernews · levkk · 7月7日 15:36 · [社区讨论](https://news.ycombinator.com/item?id=48819308)

**背景**: 像 PgBouncer 这样的连接池会在多个客户端之间重用数据库连接，这可能导致状态泄漏（例如临时表、会话变量）从一个客户端无意中传递给另一个。NOTIFY/LISTEN 机制广泛用于实时更新，但标准连接池通常会降低其性能，因为每个通知会发送到每个池连接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech-champion.com/database/postgresql/postgresql-temp-tables-and-connection-pooling-navigating-performance-pitfalls/">PostgreSQL Temp Tables and Connection Pooling: Navigating ...</a></li>
<li><a href="https://dev.to/geekyfox90/postgresql-connection-pooling-with-pgbouncer-a-complete-guide-2fam">PostgreSQL Connection Pooling with PgBouncer: A Complete Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者赞扬使用 AGPL 而非 BSL，称其“很棒”。还有人询问状态泄漏的严重性、查询缓存、模式切换支持，以及 NOTIFY 修复是否会牺牲事务语义——这些问题显示了技术上的参与度。

**标签**: `#PostgreSQL`, `#connection pooling`, `#open-source`, `#database`, `#AGPL`

---

<a id="item-21"></a>
## [高薪难留技术移民 德国面临人才流失](https://www.dw.com/en/germany-migrants-skilled-workers-integration-labor-market-bureaucracy-language-housing/a-77853162) ⭐️ 7.0/10

德国之声最新分析揭示了高薪技术移民仍选择离开德国的悖论，指出官僚障碍、文化隔离和有限的晋升空间是主要原因。 这很重要，因为德国经济严重依赖技术移民，如果不能留住这些人才，将加剧劳动力短缺并削弱科技及其他行业的竞争力。 文章及大量评论显示，缓慢的官僚体系、住房危机、语言障碍以及难以结交本地朋友等问题阻碍了长期定居。许多技术移民感到，无论收入或国籍如何，他们始终被视为局外人。

hackernews · theanonymousone · 7月7日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=48815982)

**背景**: 德国长期致力于吸引技术移民以填补工程技术、IT 和医疗行业的劳动力缺口。然而，复杂的签证系统、文化保守以及日常生活中的英语普及率低等融合挑战，一直是移民研究中的常见议题。

**社区讨论**: 社区评论分享了与文章发现一致的个人经历。评论者强调不被接纳的感受——有人比较了德国归化与美国归化，指出美国的朋友会参加仪式。其他人则指出了基础设施恶化以及在国际公司之外职业发展受限的问题。

**标签**: `#immigration`, `#Germany`, `#tech workers`, `#bureaucracy`, `#culture`

---

<a id="item-22"></a>
## [98%的成功率：在关键场景中远远不够](https://whynothugo.nl/journal/2026/07/03/98-isnt-very-much/) ⭐️ 7.0/10

文章指出，在需要接近完美的场景中（如软件可靠性或清洁任务），98%的成功率通常不够，因为即使很小的失败率也可能导致严重后果。 这一观点挑战了软件质量和工程设计中的自满情绪，强调失败率必须根据具体情况评估，尤其是在涉及大规模用户或安全关键系统时。 文章举例说明，2%的失败率意味着每 50 次尝试就有 1 次失败，这在手术、购票或代码部署中可能是不可接受的，并且百分比度量在极端情况下可能具有误导性。

hackernews · speckx · 7月7日 12:45 · [社区讨论](https://news.ycombinator.com/item?id=48816959)

**背景**: 在高可用性系统中，'五个九'（99.999%）可用性是常见目标，允许每年仅约 5 分钟的停机时间。类似地，六西格玛质量标准旨在每百万机会中只有 3.4 个缺陷，即 99.99966%的成功率。这些基准强调了上下文如何决定 98%是否足够。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_availability">High availability - Wikipedia</a></li>
<li><a href="https://www.techtarget.com/searchnetworking/feature/The-Holy-Grail-of-five-nines-reliability">Five-nines availability: What it really means | TechTarget</a></li>
<li><a href="https://en.wikipedia.org/wiki/Six_Sigma">Six Sigma - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍同意 98%取决于上下文：有人指出，对于扫针或高价值交易，需要接近完美；而其他人则认为客户接受度和业务目标更重要。还有人建议使用几率表示法（例如“1/50”）比百分比更清晰。

**标签**: `#software quality`, `#statistics`, `#engineering`, `#design trade-offs`

---

<a id="item-23"></a>
## [MemGUI-Agent：为长程 GUI 任务引入记忆机制](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247902040&idx=3&sn=68b945acd4b331099f80f29c018551b8) ⭐️ 7.0/10

快手与浙江大学联合提出了 MemGUI-Agent，这是一个端到端的手机 GUI 代理，其核心创新是 ConAct（上下文即动作）接口，将上下文管理作为模型动作输出的一部分。 这解决了现有 GUI 代理在长程任务中因提示爆炸和中间事实丢失而表现不佳的关键限制，有望为复杂多步工作流实现更可靠的移动自动化。 MemGUI-Agent 基于多模态大语言模型（MLLM），通过在每一步动作中主动管理上下文来实现端到端的长程任务执行，详情见 arXiv 论文（2606.19926）并在 GitHub 上开源。

rss · 量子位 · 7月7日 04:30

**背景**: 当前基于 MLLM 的 GUI 代理通常采用 ReAct 风格的提示，将之前的观察和动作全部拼接进提示，导致提示爆炸和关键跨应用事实在长序列中被稀释。MemGUI-Agent 的 ConAct 机制将上下文管理作为模型输出的组成部分，使代理能在每一步决定保留和遗忘哪些信息，从而保持提示简洁并保存关键信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://memgui-agent.github.io/">MemGUI-Agent</a></li>
<li><a href="https://arxiv.org/abs/2606.19926">MemGUI-Agent: An End-to-End Long-Horizon Mobile GUI Agent ...</a></li>
<li><a href="https://github.com/kwai/MemGUI-Agent/tree/main">GitHub - kwai/MemGUI-Agent: Official code for "MemGUI-Agent ...</a></li>

</ul>
</details>

**标签**: `#GUI Agent`, `#Memory`, `#Long-term Tasks`, `#AI`, `#Mobile Automation`

---

<a id="item-24"></a>
## [谷歌起诉利用 Gemini AI 进行钓鱼诈骗的中国骗子](https://www.schneier.com/blog/archives/2026/07/google-is-suing-chinese-scammers-who-are-using-gemini.html) ⭐️ 7.0/10

谷歌对名为 Outsider Enterprise 的中国网络犯罪团伙提起诉讼，该团伙利用谷歌的 Gemini AI 通过 Telegram 自动化钓鱼诈骗，提供近 300 种诈骗模板的钓鱼即服务。 此案凸显了先进 AI 工具在网络犯罪中的实际滥用，并表明科技公司开始采取法律行动打击 AI 驱动的诈骗，为未来执法树立先例。 诉讼指控 Outsider Enterprise 利用 Gemini 创建模仿谷歌、YouTube 及纽约 E-ZPass 等政府机构的网站，并通过 Telegram 频道向非技术犯罪分子提供钓鱼工具包。

rss · Schneier on Security · 7月7日 10:43

**背景**: 钓鱼即服务是一种网络犯罪商业模式，犯罪分子向他人出售现成的钓鱼工具包和基础设施，降低了发动攻击的门槛。谷歌 Gemini 是一种多模态 AI 模型，可生成包括虚假网站在内的内容，可能被诈骗者滥用。这起诉讼是谷歌打击 AI 滥用更广泛努力的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Phishing_as_a_service">Phishing as a service</a></li>
<li><a href="https://www.huntress.com/cybersecurity-101/topic/phishing-as-a-service">What is Phishing-as-a-Service | Cybercrime Democratized ...</a></li>

</ul>
</details>

**社区讨论**: 新闻作者对诉讼的有效性表示怀疑，但支持这一努力，反映了常见的观点：尽管法律行动是向前的一步，但可能难以震慑国际网络犯罪分子。

**标签**: `#security`, `#AI misuse`, `#phishing`, `#Google Gemini`, `#legal`

---

<a id="item-25"></a>
## [2026 年科技就业市场：AI 浪潮与招聘错位](https://newsletter.pragmaticengineer.com/p/tech-jobs-market-in-2026-part-3-hiring) ⭐️ 7.0/10

根据 50 多位招聘经理和求职者的洞见，2026 年科技就业市场的特点严重错位：AI 相关岗位火爆，而其他职位（尤其是工程领导岗）面临招聘困难。 该分析揭示了影响科技从业者职业规划和企业人才战略的关键趋势，凸显了 AI 技能提升的紧迫性以及招聘经验丰富的工程领导者的挑战。 报告指出市场是‘AI 相关职位最热门’但‘对工程领导来说艰难’，表明需求两极分化。分析基于多个来源的定性数据而非量化指标。

rss · The Pragmatic Engineer · 7月7日 17:25

**背景**: 自 2022 年以来，科技就业市场波动不断，先是裁员潮，随后 AI 招聘激增。本报告是分析 2026 年就业形势系列的一部分，聚焦特定职位的供需脱节。

**标签**: `#tech-jobs`, `#hiring`, `#AI`, `#market-trends`

---

<a id="item-26"></a>
## [Windows 11 漏洞吞噬高达 513 GB 存储](https://www.windowslatest.com/2026/07/06/microsoft-admits-a-windows-11-bug-is-eating-up-to-500gb-of-storage-verify-if-you-are-affected/) ⭐️ 7.0/10

Windows 11 的 Capability Access Manager 出现一个漏洞，导致 CapabilityAccessManager.db-wal 文件异常膨胀，最多占用 513 GB 磁盘空间。微软已在 2026 年 6 月可选更新 KB5095093 中修复，并计划纳入 7 月补丁。 该漏洞会填满系统盘，可能导致性能问题甚至阻止更新，严重影响用户。这凸显了微软及时修复隐私权限记录等核心操作系统组件的重要性。 该漏洞影响 Capability Access Manager 数据库的预写日志 (WAL) 文件，该文件记录应用对摄像头、麦克风和位置的权限使用情况。微软的修复改进了 WAL 文件的大小管理；用户也可以手动停止 camsvc 服务并删除 WAL 文件作为临时解决方法。

telegram · zaihuapd · 7月7日 06:34

**背景**: Capability Access Manager (camsvc) 是一项 Windows 服务，记录哪些应用访问了隐私敏感资源。它使用 SQLite 数据库并采用预写日志 (WAL) 进行崩溃恢复：更改先写入 WAL 文件，再合并到主数据库。在此漏洞中，WAL 文件未能合并，导致其持续增大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/answers/questions/5815087/capabilityaccessmanager-is-devouring-my-hard-drive">CapabilityAccessManager is devouring my hard drive ...</a></li>
<li><a href="https://techcommunity.microsoft.com/discussions/windows11/fix-for-capabilityaccessmanager-db-wal-growing-huge-in-windows-11/4524594">Fix for CapabilityAccessManager.db-wal Growing Huge in ...</a></li>
<li><a href="https://www.wintips.org/how-to-fix-capabilityaccessmanager-db-wal-taking-up-huge-disk-space-on-windows-11/">How to Fix CapabilityAccessManager.db-wal Taking up Huge Disk ...</a></li>

</ul>
</details>

**标签**: `#Windows 11`, `#bug`, `#storage`, `#Microsoft`, `#Capability Access Manager`

---

<a id="item-27"></a>
## [new-api 修复计费漏洞，防止负数扣费](https://github.com/QuantumNous/new-api/commit/d0bd8aa) ⭐️ 7.0/10

QuantumNous/new-api 项目的两个提交修复了计费系统中的整数溢出漏洞，该漏洞可通过超大参数触发负数扣费，使攻击者无需付款即可获得额度。 该安全修复防止了计费系统被滥用及潜在的经济损失，保护了服务提供者和用户免受余额操纵的影响。 修复方法包括对用户可控参数增加上限校验，并引入饱和转换逻辑，防止 quota 计算结果在转为整数时发生回绕。此外，还对其他入口补充了边界检查，以预防类似攻击。

telegram · zaihuapd · 7月7日 07:26

**背景**: 整数溢出是指算术运算的结果超出整数类型可表示的范围，可能导致结果回绕为负数。在计费系统中，这会导致扣费计算错误。饱和转换将超出范围的值钳制到最近的表示范围内，从而防止回绕。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cwe.mitre.org/data/definitions/190.html">CWE - CWE-190: Integer Overflow or Wraparound (4.20)</a></li>
<li><a href="https://registry.khronos.org/OpenCL/specs/unified/refpages/man/html/convert_T.html">convert_T (3) - Khronos Group</a></li>

</ul>
</details>

**标签**: `#security`, `#bug-fix`, `#integer-overflow`, `#billing`

---

<a id="item-28"></a>
## [英伟达 Blackwell 晶圆美国制造，封装仍需送台](https://www.tomshardware.com/tech-industry/nvidia-and-intel-tout-chips-built-in-america-but-every-arizona-made-blackwell-die-is-still-packaged-in-taiwan) ⭐️ 7.0/10

台积电亚利桑那州 Fab 21 已开始使用定制的 4NP 制程量产英伟达 Blackwell 晶圆，同时英特尔 Fab 52 也已启动 18A 制程生产，但这些晶圆仍需运往台湾进行 CoWoS-L 先进封装。 这凸显出即使美国逻辑制造产能提升，尖端 AI 芯片仍依赖台湾的先进封装，给英伟达及整个 AI 行业带来供应链风险。 Blackwell 晶圆需运输约 7000 英里至台湾进行切割、堆叠和 CoWoS-L 封装；美国目前缺少高带宽内存（HBM）量产设施和先进封装能力，完整的本土供应链预计最早要到 2028-2029 年才能形成。

telegram · zaihuapd · 7月7日 09:47

**背景**: CoWoS-L 是台积电的晶圆级封装技术，采用基于 RDL 的转接板与局部硅互联桥，适用于 Blackwell 等大型 HPC 芯片。TSMC 4NP 是 N4P 节点的增强版，专为英伟达数据中心 GPU 定制。英特尔 18A 制程采用 RibbonFET 晶体管和 PowerVia 背面供电，是重要的工艺节点升级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/cowos.htm">CoWoS® - Taiwan Semiconductor Manufacturing Company Limited</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#Nvidia`, `#supply chain`, `#advanced packaging`, `#TSMC`

---

<a id="item-29"></a>
## [中国网络文学平台从拥抱 AI 转向严打 AI 生成内容](https://restofworld.org/2026/china-ai-web-novels/) ⭐️ 7.0/10

晋江、起点、番茄小说等中国主要网络文学平台正逆转此前对 AI 写作工具的拥抱态度，因质量问题和读者反弹而严格限制或禁止 AI 生成内容。 这一政策转变凸显了 AI 内容审核在现实中的挑战及其对创意产业的影响，表明不加控制的 AI 使用会损害内容质量和读者信任。 晋江仅允许将 AI 用于资料搜集和校对，而番茄小说则限制每个账号每日发布字数，并在 6 月份拒绝了超过 10.4 万份包含 AI 写作的“低质量”投稿。

telegram · zaihuapd · 7月7日 13:27

**背景**: 中国网络文学平台是数字出版生态系统，作者连载故事，读者按章节付费。许多平台曾推出 AI 辅助写作工具以提高效率，但广泛使用导致内容模式化且残留 AI 提示词，激怒了读者。反弹迫使平台收紧规则以保护内容质量和作者声誉。

**标签**: `#AI-generated content`, `#web novels`, `#China`, `#content moderation`, `#AI ethics`

---

<a id="item-30"></a>
## [加州纽约立法要求 3D 打印机安装枪支检测软件](https://www.theverge.com/tech/960802/3d-printed-gun-laws-ghost-guns) ⭐️ 7.0/10

纽约州已签署法律，加州正在推进 AB 2047 法案，要求州内销售的 3D 打印机必须内置能够扫描并拦截枪支蓝图的软件。 这些法律可能为通过监管 3D 打印技术防止无法追踪的‘幽灵枪’树立先例，但也引发了对隐私、开源创新以及过度监管可能限制 3D 打印机合法用途的严重担忧。 纽约州的法律还涵盖 CNC 机床；加州法案在众议院通过，拟自 2029 年 3 月起禁止销售未经认证的打印机，违规罚款最高达 2.5 万美元。批评者指出，法案未明确拦截技术标准，可能误判水管、玩具等物品。

telegram · zaihuapd · 7月7日 14:02

**背景**: ‘幽灵枪’是指没有序列号、无法追踪的家制枪支。3D 打印机和 CNC 机床可用于制造这类枪支的塑料或金属部件；目前已有利用 AI 和 CAD 文件分析的软件解决方案，用于检测并拦截枪支蓝图。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ghost_gun">Ghost gun</a></li>
<li><a href="https://3dprint.com/314218/daring-am-software-advances-aim-to-curb-illegal-3d-printing-of-firearms/">Daring AM: Software Advances Aim to Curb Illegal 3D Printing ...</a></li>

</ul>
</details>

**标签**: `#3D printing`, `#gun control`, `#legislation`, `#privacy`, `#open source`

---

<a id="item-31"></a>
## [内存芯片危机加剧，SEMI 向华盛顿发出警告](https://finance.yahoo.com/technology/articles/memory-chip-crunch-deepens-semi-175944791.html) ⭐️ 7.0/10

代表半导体供应链的全球行业协会 SEMI 向华盛顿发出警告，称内存芯片短缺正在加剧，可能扰乱技术供应链。 这一警告突显了内存芯片短缺的严重性，可能导致全球电子产品制造商、数据中心和消费者的成本上升和交付延迟。 SEMI 的警告强调，尽管之前已努力增加产量，但从智能手机到服务器所需的内存芯片仍然严重短缺。

openbb · AAPL · 7月7日 17:59

**背景**: SEMI（国际半导体设备与材料协会）是一个代表半导体和电子产品供应链公司的行业协会。内存芯片，包括 DRAM 和 NAND 闪存，是现代电子产品中的重要组件。当需求超过供应时，就会发生短缺，通常是由于产能限制或地缘政治因素。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Semiconductor_equipment_and_materials_international">Semiconductor equipment and materials international</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#memory chips`, `#supply chain`, `#tech industry`

---

<a id="item-32"></a>
## [SpaceXAI 计划本周三与 Cursor 联合发布新 AI 模型](https://finance.yahoo.com/technology/ai/articles/spacexai-plans-launch-model-cursor-210200389.html) ⭐️ 7.0/10

据 The Information 报道，SpaceXAI 计划最早于本周三与 Cursor 合作发布一款新 AI 模型。该模型预计将与 Cursor 的 AI 编码环境集成。 此次合作可能增强 AI 驱动的代码生成和软件开发能力，将 SpaceXAI 的大规模模型与 Cursor 的专业开发者工具相结合。这标志着 AI 基础模型与实用编码助手之间日益融合的趋势。 发布日期仍为暂定，可能变动；尚未披露具体模型名称或能力。Cursor 是 Anysphere 开发的 AI 编码代理，估值达 293 亿美元。

openbb · AAPL · 7月7日 21:02

**背景**: SpaceXAI 前身为 xAI，是 SpaceX 的子公司，专注于 AI 研究，以 Grok 聊天机器人和 Colossus 超级计算机闻名。Cursor 是一个 AI 驱动的编码环境，帮助开发人员使用自然语言编写代码。此次合作旨在将先进的 AI 能力直接引入开发者工作流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceXAI">SpaceXAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cursor_(company)">Cursor (company) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI`, `#SpaceXAI`, `#Cursor`, `#AI model`, `#news`

---