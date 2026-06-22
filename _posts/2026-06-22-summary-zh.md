---
layout: default
title: "Horizon Summary: 2026-06-22 (ZH)"
date: 2026-06-22
lang: zh
---

> 从 124 条内容中筛选出 19 条重要资讯。

---

1. [Apertus：面向主权 AI 的开放基础模型](#item-1) ⭐️ 8.0/10
2. [宁可重复，不要错误的抽象](#item-2) ⭐️ 8.0/10
3. [如何在 Python 中编写 Lisp 解释器（2010 年）](#item-3) ⭐️ 8.0/10
4. [几何代数批评引发丰富讨论](#item-4) ⭐️ 8.0/10
5. [开发者对 CORS 的普遍误解曝光](#item-5) ⭐️ 8.0/10
6. [三星向员工部署 ChatGPT Enterprise 和 Codex](#item-6) ⭐️ 8.0/10
7. [Polymarket 付费制作虚假交易视频](#item-7) ⭐️ 8.0/10
8. [Alphabet CEO：AI 取代广告成为最大增长引擎](#item-8) ⭐️ 8.0/10
9. [技术工作可能因欺诈性账单而存在](#item-9) ⭐️ 7.0/10
10. [Anthropic 要求 Claude 身份验证](#item-10) ⭐️ 7.0/10
11. [可销售软件的最小可行单元探讨](#item-11) ⭐️ 7.0/10
12. [具身智能初创公司被敦促聚焦大脑与世界模型](#item-12) ⭐️ 7.0/10
13. [sqlite-utils 4.0rc1：新增迁移与嵌套事务](#item-13) ⭐️ 7.0/10
14. [Cloudflare 推出临时账户用于短暂部署](#item-14) ⭐️ 7.0/10
15. [无限 VPN 隧道规避 IP 封锁](#item-15) ⭐️ 7.0/10
16. [超声波浓缩咖啡能耗降低 75%](#item-16) ⭐️ 7.0/10
17. [AI 不能或不应为你做的事](#item-17) ⭐️ 7.0/10
18. [苹果准 CEO：AI 增强产品，而非主导](#item-18) ⭐️ 7.0/10
19. [AI 投资热潮警示市场过热](#item-19) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Apertus：面向主权 AI 的开放基础模型](https://apertvs.ai/) ⭐️ 8.0/10

由瑞士联邦理工学院洛桑分校、苏黎世联邦理工学院和瑞士国家超级计算中心共同开发的 Apertus——一套完全开放的大语言模型套件——已正式发布，旨在解决开放模型中的数据合规性和多语言表征问题。 Apertus 通过提供完全透明、可复现的基础模型，帮助各国实现 AI 主权，减少对美国和中国专有 AI 技术的依赖。 Apertus 以完全开放的许可发布了所有组件——训练数据、代码、权重、方法和对齐原则，并旨在支持多种语言并符合数据法规要求。

hackernews · T-A · 6月21日 21:29 · [社区讨论](https://news.ycombinator.com/item?id=48622778)

**背景**: 主权 AI 指国家利用自身基础设施、数据和劳动力生产人工智能的能力。目前大多数大语言模型仅开放权重，即用户可以微调但无法复现训练过程。Apertus 是最大的完全开放模型之一，使任何实体都能基于其完整流水线进行构建。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apertus_(LLM)">Apertus (LLM) - Wikipedia</a></li>
<li><a href="https://apertvs.ai/">Fully Open Foundation Model for Sovereign AI</a></li>
<li><a href="https://arxiv.org/abs/2509.14233">[2509.14233] Apertus: Democratizing Open and Compliant LLMs ... Apertus: Democratizing Open and Compliant LLMs for Global ... Apertus: a fully open, transparent, multilingual language model About Apertus - APERTVS.ai Apertus released A fully open, transparent and mul- tilingual ...</a></li>
<li><a href="https://blogs.nvidia.com/blog/what-is-sovereign-ai/">What Is Sovereign AI? | NVIDIA Blog</a></li>

</ul>
</details>

**社区讨论**: 社区评论提到了其他完全开放的 LLM，如 OLMo 3.1 和 K2 Think V2，并质疑 Apertus 与之相比如何。一些人对该项目的速度和竞争力表示怀疑，而另一些人则讨论像 Cohere 这样专注于主权 AI 的公司的价值主张。

**标签**: `#open-source AI`, `#foundation models`, `#sovereign AI`, `#LLM`, `#AI governance`

---

<a id="item-2"></a>
## [宁可重复，不要错误的抽象](https://sandimetz.com/blog/2016/1/20/the-wrong-abstraction) ⭐️ 8.0/10

该文章认为，过早或不正确的抽象比代码重复更有害，主张等到模式出现三次后再进行抽象的原则。 这挑战了优先抽象而非重复的常见软件工程教条，影响了开发者重构和代码维护的方式。 该文章来自 2016 年，至今仍在开发者社区中被广泛引用。Sandi Metz 强调，消除重复比修复错误的抽象更容易。

hackernews · rafaepta · 6月21日 16:08 · [社区讨论](https://news.ycombinator.com/item?id=48620090)

**背景**: 抽象是软件工程中的核心概念，将通用代码泛化到共享函数或类中。虽然减少重复通常是可取的，但过早创建抽象可能导致代码僵硬且难以修改。该文章倡导在抽象之前遵循'三次法则'。

**社区讨论**: 评论者普遍赞同文章的观点，指出过度设计比重复更糟糕。有些人讨论函数式编程可以减少重复问题，而另一些人则强调单一事实来源的重要性。

**标签**: `#software engineering`, `#refactoring`, `#abstraction`, `#best practices`, `#code quality`

---

<a id="item-3"></a>
## [如何在 Python 中编写 Lisp 解释器（2010 年）](https://norvig.com/lispy.html) ⭐️ 8.0/10

Peter Norvig 于 2010 年发布的经典教程《如何在 Python 中编写 Lisp 解释器》再次在 Hacker News 上被分享，凸显其作为在 Python 中构建 Lisp 解释器的入门资源的持久价值。 该教程仍然是编写解释器最易上手的入门材料之一，帮助无数程序员理解语言实现的基础知识。其影响力持续体现在社区项目如 Rust 移植版和衍生实现中。 该教程在大约 100 行 Python 代码中实现了一个简单的类 Scheme Lisp 解释器。第二部分增加了更多功能，可在 norvig.com/lispy2.html 找到。

hackernews · tosh · 6月21日 15:36 · [社区讨论](https://news.ycombinator.com/item?id=48619831)

**背景**: Lisp 是最古老的高级编程语言之一，以其完全括号化的前缀记法和代码即数据的理念而闻名。解释器直接执行源代码而不需要事先编译。本教程使用 Python 演示这些概念，使其对广泛受众友好。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lisp_(programming_language)">Lisp (programming language)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Interpreter_(computer_science)">Interpreter (computer science)</a></li>

</ul>
</details>

**社区讨论**: Hacker News 社区对这一经典资源表示赞赏，有用户指出这是学习编写编程语言的最佳起点，与《Crafting Interpreters》并列。其他用户分享了相关项目，如 Rust 版本和极简 Lisp 实现 Ribbit。

**标签**: `#Lisp`, `#Python`, `#interpreter`, `#tutorial`, `#programming languages`

---

<a id="item-4"></a>
## [几何代数批评引发丰富讨论](https://alexkritchevsky.com/2024/02/28/geometric-algebra.html) ⭐️ 8.0/10

Alex Kritchevsky 在 2024 年发表的一篇博客文章批判性地审视了几何代数，质疑其在数学严谨性和工程与物理中的实际效用，引发了实质性的社区讨论。 这场辩论突显了理论数学框架与应用工程需求之间的持续张力，影响各学科如何采纳新的数学工具，并可能波及计算机图形学、机器人学和物理教育等领域。 该文章批评几何代数吸引了边缘研究者且缺乏严谨基础，而评论者反驳说几何代数在工程问题中提供了实用的易用性。讨论还强调了几何代数忽略量纲分析，这对计算物理至关重要。

hackernews · Hbruz0 · 6月21日 11:06 · [社区讨论](https://news.ycombinator.com/item?id=48617782)

**背景**: 几何代数（也称为 Clifford 代数）是一种数学框架，将向量代数扩展为以多向量表示几何对象（如直线、平面和体积）。它由物理学家 David Hestenes 在 20 世纪 60 年代重新推广用于物理学，但因缺乏严谨性和过度推崇而受到批评。该框架用于计算机图形学、机器人学和某些物理学领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Geometric_algebra">Geometric algebra</a></li>
<li><a href="https://bivector.net/">BiVector.net: Geometric Algebra Resources</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧：一些人赞扬文章表达了长期对几何代数缺乏量纲和边缘吸引力的疑虑，而另一些人则为其作为实用工具辩护，将其社区比作 Rust 编程语言的热心倡导者。少数人指出，几何代数的教学价值超过了理论纯粹性。

**标签**: `#geometric algebra`, `#mathematics`, `#academic debate`, `#engineering applications`, `#community discussion`

---

<a id="item-5"></a>
## [开发者对 CORS 的普遍误解曝光](https://fosterelli.co/developers-dont-understand-cors) ⭐️ 8.0/10

这篇文章及其 251 条评论的讨论揭示，许多开发者从根本上误解了 CORS，将其浏览器强制执行的限制与服务器端安全控制混淆。 这种持续存在的误解可能导致 Web 应用程序出现安全漏洞，因为开发者可能错误地将 CORS 视为安全边界。这也突显了开发者在威胁模型理解方面普遍存在的差距。 诸如 Access-Control-Allow-Origin 之类的 CORS 头部仅指示浏览器允许跨源请求，并不能阻止其他来源向服务器发送请求。正如评论中指出的，无论 CORS 设置如何，任何网站的 JavaScript 仍然可以访问 localhost。

hackernews · toilet · 6月21日 01:35 · [社区讨论](https://news.ycombinator.com/item?id=48614844)

**背景**: CORS（跨源资源共享）是一种基于 HTTP 头部的机制，依赖浏览器强制执行同源策略。它允许服务器指定哪些来源被允许读取跨源请求的响应。然而，CORS 并非服务器端访问控制；它仅解除浏览器对合法跨源交互的限制。许多开发者错误地认为 CORS 能保护服务器免受未授权请求，这是不正确的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://codeigniter4.github.io/CodeIgniter4/libraries/cors.html">Cross - Origin Resource Sharing ( CORS ) — CodeIgniter...</a></li>
<li><a href="https://www.linkedin.com/pulse/understanding-cors-cross-origin-resource-sharing-foe-sahil-bhanvadiya-vzaff?tl=en">Understanding CORS ( Cross - Origin Resource Sharing )...</a></li>

</ul>
</details>

**社区讨论**: 评论区争议颇多，部分读者认为文章本身曲解了 CORS。例如，用户 muvlon 指出，设置 Access-Control-Allow-Origin 并不能限制哪些网站能与 localhost 通信。其他人证实 CORS 被广泛误解，即使是经验丰富的开发者也难以掌握。总体而言，讨论强化了文章的观点，即 CORS 的困惑普遍存在。

**标签**: `#CORS`, `#web security`, `#development`, `#HTTP`, `#misconceptions`

---

<a id="item-6"></a>
## [三星向员工部署 ChatGPT Enterprise 和 Codex](https://openai.com/index/samsung-electronics-chatgpt-codex-deployment) ⭐️ 8.0/10

三星电子正在向全球员工部署 ChatGPT Enterprise 和 Codex，这成为 OpenAI 最大的企业 AI 部署之一。 此举标志着全球科技巨头在企业级生成式 AI 采用上的重大举措，可能促使其他大型企业加速自身的 AI 集成。 ChatGPT Enterprise 提供企业级安全、隐私和集中管理控制，而 Codex 是用于软件工程任务（如编写代码和修复错误）的 AI 编程代理。

rss · OpenAI News · 6月21日 23:00

**背景**: ChatGPT Enterprise 是面向组织的托管 ChatGPT 计划，于 2023 年 8 月推出，具有增强的安全和合规功能。Codex 于 2025 年 4 月以 Codex CLI 形式发布，是一个 AI 代理，通过自然语言指令生成代码来帮助程序员。三星的部署在其全球运营中同时使用这两种工具，代表着对 OpenAI 技术的显著企业级采用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Codex_(AI_agent)">Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://help.openai.com/en/articles/8265053-what-is-chatgpt-enterprise">What is ChatGPT Enterprise? | OpenAI Help Center</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(language_model)">OpenAI Codex (language model) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Samsung`, `#ChatGPT Enterprise`, `#Codex`, `#enterprise AI`, `#OpenAI`

---

<a id="item-7"></a>
## [Polymarket 付费制作虚假交易视频](https://www.wsj.com/business/media/polymarket-social-media-bets-prediction-market-441cdeb5) ⭐️ 8.0/10

《华尔街日报》揭露 Polymarket 雇佣数十名创作者在模拟网站上制作虚假交易视频，隐瞒付费合作关系以吸引流量。 这一事件揭露了加密货币预测市场中的欺骗性营销行为，违反了美国广告法，并损害了平台的可信度。 在分析的 1105 个视频中，70%显示了 190 万美元的虚假下注；其中 118 个视频声称赢得近 90 万美元，而实际会亏损超过 16.6 万美元。

telegram · zaihuapd · 6月21日 06:31

**背景**: 预测市场允许用户使用加密货币对事件结果下注。Polymarket 是领先的平台，2022 年因未注册交易被美国禁止。美国联邦贸易委员会(FTC)指南要求付费代言必须明确披露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prediction_market">Prediction market</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polymarket">Polymarket</a></li>
<li><a href="https://www.ftc.gov/business-guidance/resources/ftcs-endorsement-guides-what-people-are-asking">FTC 's Endorsement Guides : What People Are Asking | Federal ...</a></li>

</ul>
</details>

**标签**: `#Polymarket`, `#预测市场`, `#加密货币`, `#虚假广告`, `#行业丑闻`

---

<a id="item-8"></a>
## [Alphabet CEO：AI 取代广告成为最大增长引擎](https://finance.yahoo.com/technology/ai/articles/forget-ads-alphabet-ceo-says-113029880.html) ⭐️ 8.0/10

Alphabet CEO Sundar Pichai 宣布，人工智能 (AI) 已取代广告成为公司最大的增长动力。 这一战略转变表明，AI 现在比传统的广告业务更能推动 Alphabet 的未来，影响投资者预期和行业竞争。 该声明未公布具体数字；它反映了长期愿景，即 Google Cloud 和 Gemini 等 AI 产品将成为主要收入来源。

openbb · AAPL · 6月21日 11:30

**标签**: `#AI`, `#Alphabet`, `#business strategy`, `#growth driver`

---

<a id="item-9"></a>
## [技术工作可能因欺诈性账单而存在](https://david.newgas.net/did-my-old-job-only-exist-because-of-fraud/) ⭐️ 7.0/10

作者反思了自己之前的技术工作，质疑该工作是否仅仅由于欺诈性账单操作（如虚报工时、通过外包公司重新雇用合同工）而存在。 这篇文章揭示了科技行业中系统性的欺诈和浪费，可能影响工程师和公司的工作保障、项目成本以及道德标准。 社区评论描述了英国银行中的合同工回收、政府项目上的虚假工时编辑，以及与 WorldCom 欺诈案的关联，表明各行业都存在账单滥用模式。

hackernews · advisedwang · 6月21日 21:40 · [社区讨论](https://news.ycombinator.com/item?id=48622867)

**背景**: 在许多大型组织中，合同工通过外包公司引入，这些公司会收取加价。经理可能虚报工时或重复雇用合同工以用完预算，这在政府合同中尤其可能构成欺诈。本文基于个人经历探讨了这些做法。

**社区讨论**: 评论者分享了类似经历，从合同工回收再到政府项目中的虚假工时编辑。有人开导作者不必自责，认为实际工作确实完成了。还有人将这种现象与更广泛的公司欺诈（如 WorldCom 丑闻）联系起来。

**标签**: `#workplace fraud`, `#tech industry`, `#outsourcing`, `#corporate waste`, `#contractor billing`

---

<a id="item-10"></a>
## [Anthropic 要求 Claude 身份验证](https://support.claude.com/en/articles/14328960-identity-verification-on-claude) ⭐️ 7.0/10

Anthropic 现在要求用户通过政府颁发的身份证件进行身份验证才能访问 Claude，这一政策自四月份起已在支持文章中说明。 这一政策变化影响用户隐私和 Claude 的国际访问，可能将用户推向竞争性 AI 服务，并引发关于监控和企业实践的讨论。 Anthropic 表示他们不会使用身份数据进行模型训练，但其验证合作伙伴 Persona 可能会使用这些数据来提高防欺诈能力。未通过验证的用户可能在没有明确事先警告的情况下被永久锁定在顶级模型之外。

hackernews · bathory · 6月21日 12:44 · [社区讨论](https://news.ycombinator.com/item?id=48618455)

**背景**: 身份验证是服务要求提供官方身份证明以确认用户身份的过程。越来越多的 AI 公司（如 OpenAI）使用它来遵守法规并防止滥用。该政策自四月份起已存在，但最近才引起关注。

**社区讨论**: 社区评论表达了对隐私、国际限制以及政策时机的担忧，有些用户指出该帮助页面自四月份就已存在。用户强调 Persona 可能会使用提交的数据训练其模型，并且失败会导致永久锁定，这与 OpenAI 的做法类似。

**标签**: `#Claude`, `#identity-verification`, `#AI-safety`, `#privacy`, `#policy`

---

<a id="item-11"></a>
## [可销售软件的最小可行单元探讨](https://brandur.org/minimum-viable-unit) ⭐️ 7.0/10

文章提出了“可销售软件的最小可行单元”概念，即低于该阈值时，使用 LLM 内部重建比购买第三方产品更便宜。文章认为，LLM 和内部包通过降低构建成本，正在重塑经典的“构建 vs 购买”决策。 这一分析意义重大，因为它帮助软件公司和开发者在 AI 辅助开发成本低廉的时代理解何时构建而非购买。这可能会将经济激励从购买许多小工具转向内部构建，影响小型实用工具的软件市场。 文章定义了可销售软件的“可行区间”，低于该区间时，评估和购买第三方工具的努力超过了使用 LLM 内部构建的努力。文章指出，持续订阅成本进一步将平衡转向构建，尤其是对于解决狭窄、定义明确问题的包。

hackernews · brandur · 6月21日 16:41 · [社区讨论](https://news.ycombinator.com/item?id=48620342)

**背景**: “构建 vs 购买”是软件工程中的一个经典决策：是内部开发功能或产品，还是购买现有解决方案。最小可行产品（MVP）概念侧重于交付价值的最小版本。LLM（如 GPT-4）可以快速生成代码，大幅减少构建内部包（组织内共享但不对外销售的代码模块）所需的努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.brandur.org/minimum-viable-unit">The Minimum Viable Unit of Saleable Software — brandur.org</a></li>
<li><a href="https://news.ycombinator.com/item?id=48620342">The Minimum Viable Unit of Saleable Software | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Minimum_viable_product">Minimum viable product - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，虽然 LLM 使初始构建更容易，但打磨和维护软件的努力仍然很大，往往超出预期。一位评论者观察到，LLM 自身安装了许多第三方包，挑战了它们完全取代外部依赖的观念。另一位强调，更容易的内部构建也引来了竞争，缩小了可行区间。

**标签**: `#software engineering`, `#economics`, `#LLMs`, `#build vs buy`, `#side projects`

---

<a id="item-12"></a>
## [具身智能初创公司被敦促聚焦大脑与世界模型](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247898574&idx=1&sn=6ede0b426e915786f55b39231903cd4a) ⭐️ 7.0/10

近日有分析建议机器人初创公司，必须研发具身大脑和世界模型才能在竞争激烈的市场中成功。 这突显了具身人工智能的关键趋势，强调仅有硬件是不够的，智能软件才是关键。没有这些能力的初创公司可能难以脱颖而出。 原始内容来自微信公众号文章（mp.weixin.qq.com），评分为 7.0/10，表明分析有见地，但缺乏具体的技术突破。

rss · 量子位 · 6月21日 06:00

**背景**: 具身智能指的是与物理世界交互的 AI 系统，例如机器人。‘世界模型’是外部现实的内部表征，帮助预测结果，而‘具身大脑’指处理感官数据和控制行动的认知架构。近期对中国脑机接口和具身智能初创公司的投资显示出该领域日益增长的兴趣。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/World_model">World model</a></li>
<li><a href="https://grokipedia.com/page/Chinese_brain-computer_interface_and_embodied_intelligence_startups">Chinese brain-computer interface and embodied intelligence startups</a></li>

</ul>
</details>

**标签**: `#embodied intelligence`, `#robotics`, `#AI models`, `#world models`, `#startup`

---

<a id="item-13"></a>
## [sqlite-utils 4.0rc1：新增迁移与嵌套事务](https://simonwillison.net/2026/Jun/21/sqlite-utils-40rc1/#atom-everything) ⭐️ 7.0/10

sqlite-utils 4.0rc1 引入了对数据库迁移和基于保存点的嵌套事务的内置支持，这是迈向 v4 稳定版本的重要一步。 此版本显著提升了 sqlite-utils 在管理模式变更和复杂事务工作流方面的能力，使其更适合生产环境使用。 迁移系统是对 sqlite-migrate 包的移植，通过基于装饰器的 API 支持仅向前迁移。嵌套事务功能利用 SQLite 保存点，允许在更大事务内部分回滚。

rss · Simon Willison · 6月21日 23:35

**背景**: sqlite-utils 是一个用于操作 SQLite 数据库的 Python 库和命令行工具，提供比标准 sqlite3 模块更高级的操作。SQLite 本身并不原生支持嵌套事务，但可以通过保存点来模拟。之前的 sqlite-utils v3 和 alpha 版本缺少这些功能，需要依赖 sqlite-migrate 等外部包。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sqlite-utils.datasette.io/">sqlite - utils</a></li>
<li><a href="https://pypi.org/project/sqlite-utils/">sqlite - utils · PyPI</a></li>
<li><a href="https://sqlite.org/lang_transaction.html">Transaction - SQLite java - SQLiteDatabase nested transaction and workaround ... Code sample How to Handle Nested Transactions in SQLite - Sling Academy How to use transactions — sqlite7 documentation Understanding Nested Transactions in SQLite and Effective ... Transactions - Microsoft.Data.Sqlite | Microsoft Learn</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#python`, `#database`, `#migrations`, `#transactions`

---

<a id="item-14"></a>
## [Cloudflare 推出临时账户用于短暂部署](https://simonwillison.net/2026/Jun/21/temporary-cloudflare-accounts/#atom-everything) ⭐️ 7.0/10

Cloudflare 现在允许用户无需创建账户，使用命令 'npx wrangler deploy --temporary' 部署 Workers 项目，持续 60 分钟。 此功能降低了快速原型设计和测试的门槛，使开发者和 AI 代理都能受益，实现即时、可丢弃的部署。 临时部署会生成一个认领链接，用户可在 60 分钟内获取永久所有权。该功能通过支持 --temporary 标志的 Wrangler CLI 版本访问。

rss · Simon Willison · 6月21日 22:01

**背景**: Cloudflare Workers 是一个在边缘网络上运行代码的无服务器计算平台。Wrangler 是管理 Workers 项目的官方命令行工具。临时账户提供了一种无需注册即可快速测试代码的方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cloudflare.com/products/workers/">Cloudflare Workers - Global Serverless Functions Platform</a></li>
<li><a href="https://developers.cloudflare.com/workers/wrangler/">Wrangler · Cloudflare Workers docs</a></li>

</ul>
</details>

**标签**: `#cloudflare`, `#workers`, `#serverless`, `#deployment`, `#ai agents`

---

<a id="item-15"></a>
## [无限 VPN 隧道规避 IP 封锁](https://www.reddit.com/r/netsec/comments/1ubvd13/scanning_malicious_websites_with_infinite_number/) ⭐️ 7.0/10

该文描述了一种利用无限数量的 VPN 隧道扫描恶意网站的技术，通过轮换 IP 地址来规避封锁。 该方法使得安全研究人员能够持续扫描恶意网站而不会被基于 IP 的限制所阻挡，对威胁情报和安全研究至关重要。 该方法涉及同时运行多个 VPN 连接，并在每次请求时轮换出口 IP，从而有效防止速率限制和黑名单封禁。

reddit · r/netsec · /u/moonlightelite · 6月21日 17:07

**背景**: VPN 隧道在设备和 VPN 服务器之间创建一条安全加密的连接，隐藏用户的真实 IP。网站通常实施基于 IP 的速率限制或封锁以防止扫描或爬取等滥用行为；轮换 IP 有助于绕过这些限制。通过使用多个 VPN 隧道，扫描器可以生成几乎无限的源 IP 池。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://discounttimu.substack.com/p/scanning-malicious-websites-with">Scanning malicious websites with 'infinite' number of VPN ...</a></li>
<li><a href="https://www.venn.com/learn/vpn-tunneling/">VPN Tunneling: Protocols, Security Risks & Alternatives</a></li>
<li><a href="https://www.expressvpn.com/blog/ip-rotation/">What Is IP Rotation & Why You Need It | ExpressVPN</a></li>

</ul>
</details>

**标签**: `#network security`, `#VPN`, `#scanning`, `#web security`, `#malicious websites`

---

<a id="item-16"></a>
## [超声波浓缩咖啡能耗降低 75%](https://www.wired.com/story/scientists-brew-espresso-with-ultrasonic-waves/) ⭐️ 7.0/10

新南威尔士大学的研究人员开发了一种超声波浓缩咖啡冲泡方法，利用高频声波在室温下萃取咖啡，其口感与传统方法相当，但能耗仅为后者的 24%。 这项创新可能彻底改变咖啡冲泡方式，大幅降低能耗，催生能制作多种咖啡的新型设备，并为加热萃取提供可持续的替代方案。 该系统使用 100 瓦的超声波反应器，约 3 分钟即可制作出浓度与浓缩咖啡相当的咖啡。100 名受试者的感官测试显示，其在香气、风味和整体接受度上与传统浓缩咖啡无显著差异。

telegram · zaihuapd · 6月21日 01:34

**背景**: 传统浓缩咖啡依赖高温高压水从咖啡粉中萃取可溶物。超声波空化效应通过微小气泡破裂产生强烈剪切力，无需加热即可机械萃取这些物质。这与冷萃不同，冷萃需要长时间浸泡（12-24 小时），且所得饮品浓度较低。新方法结合了机械作用和短冲泡时间，提供了独特的折中方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0260877426002311">Ultrasound enables espresso-strength coffee brewing in 2–3 ...</a></li>
<li><a href="https://www.zmescience.com/science/news-science/espresso-ultrasound/">Scientists Brewed Espresso at Room Temperature Using Ultrasound ...</a></li>

</ul>
</details>

**标签**: `#coffee`, `#ultrasound`, `#energy efficiency`, `#food science`, `#innovation`

---

<a id="item-17"></a>
## [AI 不能或不应为你做的事](https://www.wsj.com/tech/ai/when-ai-more-harm-than-good-519a83e7?siteid=yhoof2&yptr=yahoo) ⭐️ 7.0/10

《华尔街日报》最近的一篇文章探讨了人工智能无效或因道德或实际原因应避免的任务。 这一分析对从业者和决策者至关重要，因为它强调了认识 AI 局限性和应用负责任的 AI 原则以避免有害结果的重要性。 该文章可能提供了具体例子，如高风险决策、需要人类细微差别的创造性任务，以及 AI 偏见或缺乏可解释性带来风险的情况。

openbb · AAPL · 6月21日 15:00

**背景**: AI 对齐是确保 AI 系统追求预期目标的挑战，而可解释 AI（XAI）旨在使 AI 决策透明且可理解。这些领域解决了现代机器学习的“黑箱”问题，即即使设计者也无法完全解释输出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Explainable_AI">Explainable AI</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-alignment">What Is AI Alignment? | IBM</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#AI limitations`, `#responsible AI`, `#decision-making`

---

<a id="item-18"></a>
## [苹果准 CEO：AI 增强产品，而非主导](https://finance.yahoo.com/technology/ai/articles/apple-incoming-ceo-draws-line-123055617.html) ⭐️ 7.0/10

苹果即将上任的首席执行官表示，AI 工具应服务于产品开发，而非主导产品方向，强调产品优先策略。 这表明苹果继续致力于以用户为中心的设计，并谨慎整合 AI，可能影响更广泛的行业趋势。 CEO 明确反对由 AI 驱动产品决策，优先考虑人工监督和产品愿景而非自主 AI 功能。

openbb · AAPL · 6月21日 12:30

**标签**: `#AI`, `#Apple`, `#product strategy`, `#technology leadership`

---

<a id="item-19"></a>
## [AI 投资热潮警示市场过热](https://www.wsj.com/finance/stocks/all-the-money-flooding-into-ai-is-a-giant-warning-sign-6e08e3ea?siteid=yhoof2&yptr=yahoo) ⭐️ 7.0/10

《华尔街日报》一篇文章警告称，大量资金涌入人工智能可能表明市场过热，存在泡沫风险。 这很重要，因为过热投资可能导致资源错配和随后的市场调整，影响投资者、初创企业及整个科技行业。 文章未提供具体数据，但强调 AI 融资快速增加，并将其与历史上的科技泡沫进行比较。它警告当前估值可能不可持续。

openbb · AAPL · 6月21日 09:30

**背景**: 近年来，在生成式 AI 和大语言模型突破的推动下，AI 初创企业吸引了创纪录的风险投资。历史上，这种投资激增往往先于市场调整，如互联网泡沫时期。《华尔街日报》的这篇文章加剧了分析师对 AI 长期盈利能力的谨慎态度。

**标签**: `#AI`, `#investment`, `#industry trends`, `#warning`

---