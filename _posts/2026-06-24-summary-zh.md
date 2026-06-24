---
layout: default
title: "Horizon Summary: 2026-06-24 (ZH)"
date: 2026-06-24
lang: zh
---

> 从 158 条内容中筛选出 26 条重要资讯。

---

1. [FFmpeg 严重漏洞“PixelSmash”可远程执行代码](#item-1) ⭐️ 9.0/10
2. [所见即所得的 TikZ 编辑器，同步源码与预览](#item-2) ⭐️ 8.0/10
3. [AI 代理重塑软件开发迭代循环](#item-3) ⭐️ 8.0/10
4. [德国全国列车因 GSMR 无线通信系统中断停运](#item-4) ⭐️ 8.0/10
5. [无限 OCR：一次性长篇幅文档解析](#item-5) ⭐️ 8.0/10
6. [Anthropic 的 Fable 5 AI 模型数日内被破解](#item-6) ⭐️ 8.0/10
7. [GPT-5 帮助解开持续三年的免疫学谜团](#item-7) ⭐️ 8.0/10
8. [近半数 LG 智能电视应用检出住宅代理 SDK](#item-8) ⭐️ 8.0/10
9. [三星发布 UFS 5.0：面向端侧 AI，带宽达 10.8 GB/s](#item-9) ⭐️ 8.0/10
10. [中国“灵晟”超算登顶 TOP500，时隔八年重返第一](#item-10) ⭐️ 8.0/10
11. [甲骨文裁员，AI 重塑运营](#item-11) ⭐️ 8.0/10
12. [FUTO 为隐私键盘发布全新滑行输入模型](#item-12) ⭐️ 7.0/10
13. [Swift 包索引被苹果收购](#item-13) ⭐️ 7.0/10
14. [不要通过发送垃圾邮件来验证邮箱地址](#item-14) ⭐️ 7.0/10
15. [加州 AB 2047 法案限制 3D 打印机使用](#item-15) ⭐️ 7.0/10
16. [谷歌因非官方 Workspace CLI 解雇员工](#item-16) ⭐️ 7.0/10
17. [Datasette 1.0a35 新增创建/修改表格的 JSON API](#item-17) ⭐️ 7.0/10
18. [慢下来以提速：六个月内的工程变化](#item-18) ⭐️ 7.0/10
19. [分散蜘蛛黑客在英国法庭认罪](#item-19) ⭐️ 7.0/10
20. [OpenAI 加入 Appia 基金会共建 AI 标准](#item-20) ⭐️ 7.0/10
21. [中国内存制造商与微软的 AI 激励](#item-21) ⭐️ 7.0/10
22. [OpenAI 支持 AI 动画电影《Critterz》，预算 3000 万美元](#item-22) ⭐️ 7.0/10
23. [Valve 发布 Steam Machine：1049 美元起的小型游戏主机](#item-23) ⭐️ 7.0/10
24. [美国人形机器人依赖中国零部件](#item-24) ⭐️ 7.0/10
25. [众多中国高校撤销外语专业](#item-25) ⭐️ 7.0/10
26. [SpaceX 将于 2028 年发射欧洲火星车，NASA 提供支持](#item-26) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [FFmpeg 严重漏洞“PixelSmash”可远程执行代码](https://cybernews.com/security/critical-ffmpeg-vulnerability-enables-complete-compromise/) ⭐️ 9.0/10

FFmpeg 的 MagicYUV 解码器中被发现一个严重的堆越界写入漏洞，编号为 CVE-2026-8461（称为“PixelSmash”），CVSS 评分 8.8。FFmpeg 已发布 8.1.2 版本修复此漏洞。 FFmpeg 是众多媒体应用（如 VLC、Jellyfin 和 Kodi）使用的核心库。攻击者可通过诱使用户播放甚至预览恶意视频来利用此漏洞，导致桌面、服务器和 IoT 设备被完全控制。 该漏洞是一个堆越界写入问题，源于帧分配器和解码器在处理切片时计算色度平面高度不一致。任何使用 FFmpeg MagicYUV 解码器的应用都受影响；用户应更新到 FFmpeg 8.1.2，或在不需要时禁用该解码器。

telegram · zaihuapd · 6月23日 15:00

**背景**: FFmpeg 是领先的多媒体框架，用于音频和视频的解码、编码和处理。MagicYUV 编解码器是一种无损视频编解码器，广泛应用于高分辨率视频录制和存档。堆越界写入是指程序写入数据超出分配的内存，可能导致内存损坏并执行远程代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jfrog.com/blog/pixelsmash-critical-ffmpeg-vulnerability-turns-media-files-into-weapons/">PixelSmash - Critical FFmpeg Vulnerability Turns Media Files into Weapons</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/ffmpeg-fixes-pixelsmash-flaw-in-widely-used-video-decoder/">FFmpeg fixes PixelSmash flaw in widely used video decoder</a></li>

</ul>
</details>

**标签**: `#ffmpeg`, `#vulnerability`, `#CVE-2026-8461`, `#remote code execution`, `#cybersecurity`

---

<a id="item-2"></a>
## [所见即所得的 TikZ 编辑器，同步源码与预览](https://tikz.dev/editor/) ⭐️ 8.0/10

一个开源的所见即所得 TikZ 编辑器已发布，允许用户编辑代码并同步查看渲染输出，该编辑器主要由 Codex 编码代理构建。 该工具大幅减少了 LaTeX 用户创建图表时的繁琐试错过程，可能节省数小时的手动坐标调整和重新编译时间。 编辑器追踪对象的精确源码位置，拖拽时仅修改坐标而不改变其他代码结构；还包含从 SVG、PPTX 和 IPE 到 TikZ 的转换器。

hackernews · DominikPeters · 6月23日 14:24 · [社区讨论](https://news.ycombinator.com/item?id=48645437)

**背景**: TikZ 是一个强大的 LaTeX 包，用于使用\draw 等命令创建矢量图形，常用于学术论文。传统上，用户编写代码并反复重新编译以调整位置，缺乏视觉反馈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.overleaf.com/learn/latex/TikZ_package">TikZ package - Overleaf, Online LaTeX Editor</a></li>
<li><a href="https://www.overleaf.com/learn/latex/LaTeX_Graphics_using_TikZ:_A_Tutorial_for_Beginners_(Part_1)—Basic_Drawing">LaTeX Graphics using TikZ: A Tutorial for Beginners (Part 1)—Basic Drawing - Overleaf, Online LaTeX Editor</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了该项目的实用性和开源性质，其中一位提到巨大的 token 成本（API 价值 1.5 万美元但仅支付 500 美元订阅费）。然而，有用户批评生成的 TikZ 代码使用了绝对坐标，这在 TikZ 中往往是不必要的。

**标签**: `#tikz`, `#latex`, `#wysiwyg`, `#editor`, `#opensource`

---

<a id="item-3"></a>
## [AI 代理重塑软件开发迭代循环](https://lucumr.pocoo.org/2026/6/23/the-coming-loop/) ⭐️ 8.0/10

Armin Ronacher 探讨了 AI 代理如何改变软件开发的迭代循环，强调由于代理能快速执行任务但需要精确的事前规范，前置清晰度变得更加关键。 这种范式转变可能从根本上改变工程实践，使规范清晰度与编码技能同等重要，并推动软件成为一种通过交互而非传统编辑来演化的生命系统。 作者指出，AI 代理擅长执行定义明确的任务，但无法加速理解混乱需求所需的人类思考；多位评论者证实，他们的瓶颈在于编写良好的规范，而非实现循环本身。

hackernews · ingve · 6月23日 11:06 · [社区讨论](https://news.ycombinator.com/item?id=48643180)

**背景**: 传统软件开发涉及编码、测试和优化的迭代循环。AI 代理是使用推理和规划来实现目标的自主系统；它们能快速生成代码，但依赖清晰的指令。文章认为，迭代循环的本质正在从‘编码并修复’转向‘指定并执行’。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.index.dev/blog/ai-agents-for-software-development">10 Best AI Agents for Software Development in 2026</a></li>
<li><a href="https://cloud.google.com/discover/what-are-ai-agents">What are AI agents? Definition, examples, and types</a></li>
<li><a href="https://www.sciencedirect.com/topics/computer-science/self-adaptive-system">Self-Adaptive System - an overview | ScienceDirect Topics</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍同意作者的观点。mccoyb 强调清晰度是前提，没有代理能缩短思考时间。stillpointlab 表示自己的瓶颈在于规范编写，而 miki123211 补充说 LLM 擅长完成任务但缺乏审美，这解释了在迭代优化中人类品味的重要性。

**标签**: `#software development`, `#AI agents`, `#iteration`, `#paradigm shift`, `#engineering practices`

---

<a id="item-4"></a>
## [德国全国列车因 GSMR 无线通信系统中断停运](https://apnews.com/article/germany-trains-halted-communications-radio-problem-deutsche-bahn-e8fd970b2d889f3ae7ce03322d5c726b) ⭐️ 8.0/10

[日期未明确] 德国铁路公司因 GSMR 数字铁路无线电系统故障，被迫在全国范围内停运所有列车。社区传闻称可能是软件更新存在缺陷所致。 这一事件表明，软件故障可能导致关键基础设施瘫痪，影响数百万乘客。它凸显了铁路通信系统需要更严格的测试和可靠性保障。 GSMR 系统是模拟铁路无线电的数字化替代方案，用于司机与信号员之间的通信。社区推测，此次中断并非网络攻击，而可能是软件更新错误所致。

hackernews · sva_ · 6月23日 21:19 · [社区讨论](https://news.ycombinator.com/item?id=48651613)

**背景**: GSM-R（全球铁路移动通信系统）是铁路数字通信标准，提供安全的语音和数据服务，在欧洲广泛部署，对列车安全运行至关重要。德国铁路公司依赖 GSM-R 进行全国列车控制和通信。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GSM-R">GSM-R - Wikipedia</a></li>
<li><a href="https://www.networkrail.co.uk/industry-and-commercial/gsm-r-communicating-on-the-railway/">GSM-R: the railway’s mobile communication system - Network Rail</a></li>
<li><a href="https://www.nokia.com/industries/railways/gsm/">GSM-Railway | Nokia</a></li>

</ul>
</details>

**社区讨论**: 社区评论者表达了怀疑，一些人最初怀疑是网络攻击，但其他人指出德国铁路公司历来存在维护问题。有用户称传闻是软件更新存在缺陷所致，并分享了 Tagesschau 的链接以获取官方更新。

**标签**: `#infrastructure`, `#software failure`, `#transportation`, `#Germany`, `#bug`

---

<a id="item-5"></a>
## [无限 OCR：一次性长篇幅文档解析](https://github.com/baidu/Unlimited-OCR) ⭐️ 8.0/10

百度开源了 Unlimited OCR 模型，该模型避免了 Transformer 中 KV 缓存的线性内存增长，无需分块即可一次性解析长篇幅 PDF。 这一突破解决了长文档 OCR 的主要瓶颈——注意力机制的二次方内存成本。它大幅降低 VRAM 使用，使企业和研究人员能够单次推理处理整本书籍、法律合同或档案。 该方法是一种架构技巧，阻止模型累积 KV 缓存，论文中对此有详细描述。它基于 Deepseek-OCR 和 PaddleOCR，代码在 GitHub 上以 Unlimited-OCR 名称开源。

hackernews · ingve · 6月23日 11:35 · [社区讨论](https://news.ycombinator.com/item?id=48643426)

**背景**: 在基于 Transformer 的 OCR 模型中，KV 缓存随输入长度线性增长，长文档会导致内存溢出。传统解决方案将文档分页，但会丢失上下文。Unlimited OCR 通过选择性丢弃缓存的键和值来保持内存恒定，从而实现对任意长度输入的流式处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/baidu-unlimited-ocr-one-shot-long-horizon-parsing-2026">Baidu Unlimited-OCR: One-Shot Long-Horizon Document Parsing ...</a></li>
<li><a href="https://news.ycombinator.com/item?id=48643426">Unlimited OCR: One-Shot Long-Horizon Parsing | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了避免内存积累的巧妙架构技巧，并对致谢 Deepseek-OCR 和 PaddleOCR 表示赞赏。有用户幽默地引用《命运/停留之夜》中的“无限剑制”，另一用户则分享了自己本地的 OCR 流式处理方法。

**标签**: `#OCR`, `#memory efficiency`, `#deep learning`, `#AI architecture`, `#document parsing`

---

<a id="item-6"></a>
## [Anthropic 的 Fable 5 AI 模型数日内被破解](https://www.schneier.com/blog/archives/2026/06/anthropics-fable-5-model-jailbroken-within-days.html) ⭐️ 8.0/10

Anthropic 的 Fable 5 模型专设安全护栏以防止生成网络攻击等滥用行为，但在发布数日内即被越狱破解。 这一事件凸显了构建稳健 AI 护栏的持续挑战，即使是注重安全的主流模型也被迅速绕过，对 AI 安全与网络安全具有重要影响。 Fable 5 是 Anthropic 旗下 Mythos Preview 的安全版本；越狱方法尚未公开，但表明现有护栏可被有决心的攻击者绕过。

rss · Schneier on Security · 6月23日 11:03

**背景**: AI 越狱指编写提示词绕过大型语言模型的安全训练，常用技术如提示注入。护栏是用于过滤输入输出以防止有害行为的安全措施，但在对抗性输入面前仍不完善。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-fable-5-mythos-5">Claude Fable 5 and Claude Mythos 5 \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_jailbreaking">AI jailbreaking</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#jailbreaking`, `#Anthropic`, `#cybersecurity`

---

<a id="item-7"></a>
## [GPT-5 帮助解开持续三年的免疫学谜团](https://openai.com/index/gpt-5-immunology-mystery) ⭐️ 8.0/10

GPT-5 Pro 帮助免疫学家 Derya Unutmaz 解决了一个持续三年的关于 T 细胞行为的谜团，为免疫系统调控提供了新见解。 这一突破展示了人工智能在加速科学发现方面的强大作用，特别是在免疫学等复杂领域，对开发癌症和自身免疫性疾病治疗具有潜在意义。 GPT-5 发现的具体机制尚未公开，但这一成就凸显了 GPT-5 在分析复杂生物数据方面的先进推理和模式识别能力。

rss · OpenAI News · 6月23日 17:00

**背景**: T 细胞是一种对免疫系统至关重要的白细胞，理解其行为对于推进癌症免疫疗法和治疗自身免疫性疾病至关重要。像 GPT-5 这样的 AI 模型可以处理海量数据，识别人类可能忽略的模式，从而加速假设生成和验证。这个案例展示了大型语言模型如何超越文本，应用于解决现实世界的科学问题。

**标签**: `#AI`, `#immunology`, `#scientific discovery`, `#healthcare`, `#GPT-5`

---

<a id="item-8"></a>
## [近半数 LG 智能电视应用检出住宅代理 SDK](https://spur.us/blog/smart-tv-apps-residential-proxy-sdks) ⭐️ 8.0/10

一项针对 6038 款 LG 和三星智能电视应用的扫描发现，其中 2058 款包含住宅代理 SDK，LG 平台上近一半的应用受到影响。 这些 SDK 可将家庭电视变为供第三方使用的代理，可能泄露用户 IP 地址并导致未经同意的滥用，引发物联网设备的严重隐私担忧。 受影响的应用包括屏保、时钟和小游戏，部分在用户关闭后仍可继续运行代理功能；Amazon 和 Roku 已禁止此类 SDK，而 LG 和三星尚未采取同等限制。

telegram · zaihuapd · 6月23日 02:26

**背景**: 住宅代理是一种通过住宅 IP 地址路由流量的代理服务器，使其看起来像普通用户流量。嵌入智能电视应用的 SDK 可以在用户不知情的情况下将电视变为此类代理，允许第三方借家庭 IP 隐藏其活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Residential_proxy">Residential proxy</a></li>

</ul>
</details>

**标签**: `#security`, `#smart TV`, `#proxy`, `#privacy`, `#IoT`

---

<a id="item-9"></a>
## [三星发布 UFS 5.0：面向端侧 AI，带宽达 10.8 GB/s](https://news.samsung.com/global/samsung-unveils-industrys-fastest-ufs-5-0-solution-for-next-gen-on-device-ai-applications) ⭐️ 8.0/10

三星宣布开发出 UFS 5.0，这是业界最快的 UFS 解决方案，顺序读取速度高达 10.8 GB/s，写入速度高达 9.5 GB/s，计划于 2025 年第四季度量产。 这使性能比上一代 UFS 4.1 标准提升一倍，同时功耗效率提高超过 40%，为旗舰手机、XR 头显和 AI 可穿戴设备中的端侧 AI 应用提供更快的数据处理能力。 UFS 5.0 基于 JEDEC UFS 5.0 标准，采用 UniPro 3.0 和 M-PHY 6.0 接口，并利用优化的 PAM4 信号技术。与三星 UFS 4.1 方案相比，封装尺寸缩小了 16.7%。

telegram · zaihuapd · 6月23日 09:17

**背景**: 通用闪存存储（UFS）是用于移动设备的内置存储标准，以高速和低功耗闻名。端侧 AI 指的是在设备本地而非云端进行的人工智能处理，需要快速的数据访问。UFS 5.0 以更高的带宽和改进的随机读取速度满足了这一需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.samsung.com/global/samsung-unveils-industrys-fastest-ufs-5-0-solution-for-next-gen-on-device-ai-applications">Samsung Unveils Industry’s Fastest UFS 5.0 Solution for Next ...</a></li>
<li><a href="https://semiconductor.samsung.com/estorage/ufs/ufs-5-0/">UFS 5.0 | Universal Flash Storage | Samsung Semiconductor Global</a></li>

</ul>
</details>

**标签**: `#storage`, `#UFS 5.0`, `#Samsung`, `#on-device AI`, `#mobile`

---

<a id="item-10"></a>
## [中国“灵晟”超算登顶 TOP500，时隔八年重返第一](https://news.mydrivers.com/1/1131/1131573.htm) ⭐️ 8.0/10

2026 年 6 月 23 日公布的 TOP500 榜单中，中国“灵晟”超算以 2.198 ExaFLOPS 的 HPL 性能排名第一，成为全球首台纯 CPU 设计突破 2 ExaFLOPS 的系统。该超算基于国产灵鲲平台与 LX2 处理器。 这标志着中国超算时隔八年重回榜首，展示了国产 CPU 设计与高性能计算能力的重大进步。该成就凸显了中国在高性能计算领域追求自主可控的决心，可能改变全球超算领导格局。 “灵晟”还在 HPCG 基准测试中位居首位，并在 HPL-MxP 混合精度测试中排名第四。该系统部署于深圳国家超算中心，采用灵骐互联网络和麒麟操作系统。

telegram · zaihuapd · 6月23日 15:30

**背景**: TOP500 榜单基于高性能 Linpack（HPL）基准测试对超算进行排名，该测试衡量求解稠密线性方程组时的浮点性能。ExaFLOPS 即每秒百亿亿次浮点运算。中国此前排名第一的超算是 2016–2017 年的神威·太湖之光。“灵晟”采用纯 CPU 架构，这与近期许多依赖 GPU 加速器的顶级系统形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/HPL_(benchmark)">HPL (benchmark)</a></li>
<li><a href="https://www.hpcg-benchmark.org/">HPCG Benchmark</a></li>
<li><a href="https://www.itpro.com/infrastructure/a-chinese-supercomputer-just-secured-first-place-on-the-top500-list-for-the-first-time-since-2017-heres-everything-we-know-about-lineshine">A Chinese supercomputer just secured first place on the ...</a></li>

</ul>
</details>

**标签**: `#超算`, `#TOP500`, `#中国`, `#高性能计算`, `#国产CPU`

---

<a id="item-11"></a>
## [甲骨文裁员，AI 重塑运营](https://finance.yahoo.com/technology/ai/articles/oracle-cuts-jobs-ai-reshapes-161327932.html) ⭐️ 8.0/10

甲骨文公司正在裁员，作为由 AI 整合推动的重组计划的一部分，反映了自动化对技术劳动力日益增长的影响。 此举突显了一个重要的行业趋势：即使在甲骨文这样的大型老牌科技公司，AI 自动化也在导致岗位减少，预示着整个行业就业模式可能发生广泛变化。 具体裁员人数或受影响部门尚未披露，但据报道，此次裁员是甲骨文将资源重新聚焦于 AI 相关计划的更广泛战略的一部分。

openbb · AAPL · 6月23日 16:13

**背景**: 甲骨文是一家以数据库和云服务闻名的企业软件巨头。随着 AI 技术的发展，许多公司正在将以前由人类完成的任务自动化，导致某些领域的劳动力减少。

**标签**: `#AI`, `#job cuts`, `#Oracle`, `#automation`, `#industry trend`

---

<a id="item-12"></a>
## [FUTO 为隐私键盘发布全新滑行输入模型](https://swipe.futo.tech/) ⭐️ 7.0/10

FUTO 为其注重隐私的安卓键盘发布了一次重大更新，引入了一个全新的滑行输入模型，用户反馈其表现几乎与谷歌的 Gboard 相当。该模型利用用户贡献的数据进行训练，并完全离线运行。 此次更新显著改善了注重隐私用户的使用体验，缩小了与 Gboard 等主流键盘的差距。它证明了无需将数据发送到云端也能提供高质量的输入方法。 该滑行模型与语言无关，但目前似乎缺乏上下文单词预测功能，有时会错误地大写单词。底层库采用 GPLv3 许可，而安卓应用则使用专有的 FUTO 许可证。

hackernews · futohq · 6月23日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=48648619)

**背景**: 滑行输入（也称为手势输入）允许用户通过从一个字母滑到下一个字母来输入，无需抬手指。FUTO 键盘是一款完全离线、开源的安卓键盘，通过永不要求网络连接来优先保护用户隐私。在此次更新之前，其滑行输入的准确性被认为远不如 Gboard 等替代品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://play.google.com/store/apps/details?id=org.futo.inputmethod.latin.playstore&hl=en-US">FUTO Keyboard - Apps on Google Play FUTO Keyboard FUTO Keyboard APK for Android Download - APKPure.com Releases: futo-org/android-keyboard - GitHub FUTO Voice Input This keyboard app finally made typing on Android feel... good FUTO Keyboard APK Download - AppBrain</a></li>
<li><a href="https://keyboard.futo.org/">FUTO Keyboard</a></li>

</ul>
</details>

**社区讨论**: 社区反馈极为积极，许多用户表示新的滑行模型已足够好，可以永久从 Gboard 切换过来。但也有用户注意到一些小问题，例如撇号处理不正确（如将 'what's' 识别为 'whats'）、随机大写以及缺乏上下文单词建议。

**标签**: `#swipe typing`, `#keyboard`, `#privacy`, `#FUTO`, `#input method`

---

<a id="item-13"></a>
## [Swift 包索引被苹果收购](https://swiftpackageindex.com/blog/swift-package-index-joins-apple) ⭐️ 7.0/10

根据该索引网站的一篇博文，社区运营的 Swift 包发现站点 Swift Package Index 已被苹果收购。 此次收购将一项关键社区资源纳入苹果旗下，可能改善 Swift 包管理器的可发现性，同时也引发了关于开放性和控制的担忧。 Swift Package Index 承诺保持开源和免费，但苹果明确提到了开发者身份作为未来方向。该索引目前仅支持 GitHub 仓库。

hackernews · JDevlieghere · 6月23日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=48648779)

**背景**: Swift Package Index 是一个社区驱动的 Swift 包搜索引擎和元数据索引，补充了苹果官方的 Swift 包管理器。它旨在帮助开发者轻松找到库。苹果的收购遵循了将社区工具整合到其生态系统中的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://9to5mac.com/2026/06/23/swift-package-index-joins-apple-pledges-to-remain-open-source/">Swift Package Index joins Apple, pledges to remain open ...</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：有人为创始人感到高兴，也有人担心苹果在开源和开发者服务方面的记录，特别是对索引包的潜在监管以及关注开发者身份。

**标签**: `#Swift`, `#Apple`, `#Package Management`, `#Open Source`

---

<a id="item-14"></a>
## [不要通过发送垃圾邮件来验证邮箱地址](https://milek7.pl/mailverifyspam/) ⭐️ 7.0/10

一位用户发现，某个邮箱验证服务在用户注册新邮箱后，向其发送了未经请求的垃圾邮件，暗示验证过程本身可能产生垃圾邮件，这是一种黑暗模式。 这种做法侵犯了用户隐私和信任，可能将邮箱验证用作垃圾邮件的传播途径，凸显了在认证流程中需要采用道德的邮箱处理方式。 垃圾邮件包含 base64 编码的 HTML，里面填充了关于磁畴的无关文字，并带有一个零宽空格，其 CSS 设置了 'font-size: 0'，表明这是为了绕过过滤器而故意混淆。

hackernews · garaetjjte · 6月23日 20:23 · [社区讨论](https://news.ycombinator.com/item?id=48650837)

**背景**: 邮箱验证通常用于确认用户身份，方法是在收件箱中发送链接或验证码。然而，一些服务可能不当处理此过程，产生类似垃圾邮件的邮件，要么作为副作用，要么作为利用用户数据获利的黑暗模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dark_pattern">Dark pattern</a></li>
<li><a href="https://deceptive.design/">Deceptive Patterns — spreading awareness since 2010</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人认为垃圾邮件是巧合，指出验证邮件来自声誉良好的服务如 Customer.IO 和 Mailgun。另一些人则担心可能存在通过受感染库或滥用追踪像素泄露邮箱地址的问题。

**标签**: `#email verification`, `#spam`, `#privacy`, `#security`, `#dark patterns`

---

<a id="item-15"></a>
## [加州 AB 2047 法案限制 3D 打印机使用](https://www.the3dprintingnerd.com/ab2047) ⭐️ 7.0/10

加州议会通过了 AB 2047 法案，要求该州销售的所有 3D 打印机配备‘枪支拦截技术’，在打印前筛查设计文件，并将绕过该技术的行为定为犯罪。 该法案可能通过强制使用专有软件，极大地限制学生、教育工作者和企业使用 3D 打印，扼杀创新和教育。它代表技术监管的重大扩展，可能为其他州树立先例。 该法案将‘枪支拦截技术’定义为使用枪支蓝图检测算法评估文件的硬件或固件。它比纽约、华盛顿和科罗拉多州的类似法案更进一步，将规避行为定为犯罪。

hackernews · Buildstarted · 6月23日 22:12 · [社区讨论](https://news.ycombinator.com/item?id=48652184)

**背景**: 3D 打印机读取数字设计文件（如 STL）并逐层制造实体物品。对 3D 打印枪支的担忧促使立法尝试强制内容过滤。批评者认为这种技术无效，因为打印机无法区分意图，并且限制可能将用户锁定在专有生态系统中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eff.org/deeplinks/2026/04/dangers-californias-legislation-censor-3d-printing">The Dangers of California’s Legislation to Censor 3D Printing | Electronic Frontier Foundation</a></li>
<li><a href="https://www.tomshardware.com/3d-printing/california-assembly-passes-3d-printer-bill-that-would-criminalize-bypassing-mandated-gun-blocking-software">California Assembly passes 3D printer bill that would criminalize bypassing mandated gun-blocking software | Tom's Hardware</a></li>
<li><a href="https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260AB2047">Bill Text - AB-2047 Firearms: 3-dimensional printing blocking technology.</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，执法很可能徒劳无功，因为坚定的用户可以规避检查（例如分半打印）。一位评论者推测未来的 AI 可能推断武器意图，另一位批评该法案比欧洲更过度监管。一些人认为这是彭博社游说的结果。

**标签**: `#3D printing`, `#regulation`, `#education`, `#policy`, `#Hacker News`

---

<a id="item-16"></a>
## [谷歌因非官方 Workspace CLI 解雇员工](https://twitter.com/JPoehnelt/status/2069482265953087602) ⭐️ 7.0/10

谷歌员工 Justin Poehnelt 因创建并发布非官方的 Google Workspace 命令行工具（CLI）而被解雇，该工具发布在个人账户下，可能被误认为是谷歌官方产品。 此事件突显了员工创新与公司关于副业项目政策之间的持续紧张关系，特别是在谷歌这样的科技巨头中，可能影响开发者如何处理与雇主相关的开源贡献。 该 CLI 项目在 GitHub 上一举成名，但谷歌认为其违反了公司政策，因为它使用了公司品牌并可能混淆用户。Poehnelt 被解雇似乎是因为未遵循内部审批流程。

hackernews · justinwp · 6月23日 18:13 · [社区讨论](https://news.ycombinator.com/item?id=48649011)

**背景**: 命令行界面（CLI）是基于文本的软件交互工具，深受开发者喜爱用于自动化。许多科技公司，包括谷歌，都有严格的政策，要求员工在发布与公司业务相关或使用公司名称的项目前获得批准。

**社区讨论**: 社区意见分歧：一些人批评 Poehnelt 判断失误，发布可能被误认为官方工作的项目；另一些人则认为谷歌的官僚主义扼杀了创新，不公平地惩罚了一位有才华的员工。

**标签**: `#Google`, `#open source`, `#employment`, `#CLI`, `#controversy`

---

<a id="item-17"></a>
## [Datasette 1.0a35 新增创建/修改表格的 JSON API](https://simonwillison.net/2026/Jun/23/datasette/#atom-everything) ⭐️ 7.0/10

Datasette 1.0a35 引入了新的创建表格和修改表格界面，并通过 JSON API 支持，允许用户通过 /<database>/-/create 和 /<database>/<table>/-/alter 端点定义列、主键、约束等。 这些新界面显著增强了 datasette 对数据库模式管理的能力，使用户能够更方便地通过 Web 界面或 API 直接修改 SQLite 数据库。这标志着向更成熟、功能更完整的数据探索工具迈出了一步。 创建表格 API 支持定义列、主键、自定义列类型、NOT NULL 约束、文字默认值、表达式默认值和单列外键。修改表格 API 支持添加、重命名、重新排序和删除列，以及更改类型、默认值、约束、主键、外键和重命名表格。此外，模板上下文文档现已提供，并被视为直到 2.0 版本的稳定 API。

rss · Simon Willison · 6月23日 21:34

**背景**: Datasette 是一个基于 SQLite 的开源数据探索和发布工具。它提供 Web 界面和 JSON API 来查询和操作数据库。JSON API 允许编程访问数据，而此版本将其扩展至模式修改。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.datasette.io/en/stable/json_api.html">JSON API - Datasette documentation</a></li>

</ul>
</details>

**标签**: `#datasette`, `#data tools`, `#release`, `#database`, `#open source`

---

<a id="item-18"></a>
## [慢下来以提速：六个月内的工程变化](https://newsletter.pragmaticengineer.com/p/slow-down-to-speed-up) ⭐️ 7.0/10

这篇文章概述了过去六个月工程实践的变化，并主张采取更慢、更审慎的工作方式。 这很重要，因为它为应对快速变化和生产力悖论的工程领导者提供了可操作的见解，可能提高团队的可持续性和产出。 文章讨论了各类科技公司如何改变工作流程，并主张将减速作为一种反直觉的生产力提升手段，但未提及具体公司或指标。

rss · The Pragmatic Engineer · 6月23日 15:30

**背景**: “慢下来以提速”是软件工程中的一个概念，即通过降低节奏、注重质量和避免倦怠，可以实现更高的长期生产力。本文将这一概念置于最近的行业变化中，如 AI 工具的兴起和远程工作的调整。

**标签**: `#engineering culture`, `#tech trends`, `#management`, `#productivity`

---

<a id="item-19"></a>
## [分散蜘蛛黑客在英国法庭认罪](https://krebsonsecurity.com/2026/06/scattered-spider-hackers-plead-guilty-on-day-1-of-trial/) ⭐️ 7.0/10

两名分散蜘蛛网络犯罪团伙成员在英国审判首日认罪，承认对 2024 年伦敦交通局网络攻击负责。 此次认罪标志着执法部门对一个臭名昭著的网络犯罪集团取得重大胜利，该集团曾发动多起高调攻击，突显了网络安全领域国际合作的有效性。 原本预计为期六周的审判在第一天便因认罪而迅速结束。该团伙以社会工程和 SIM 卡交换攻击闻名。

rss · Krebs on Security · 6月23日 16:12

**背景**: 分散蜘蛛（又称 UNC3944 或 ShinyHunters）是一个主要由美国和英国青少年及年轻人组成的黑客组织，擅长通过社会工程手段绕过多因素认证。该组织曾攻击大公司和 IT 服务台。伦敦交通局负责管理大伦敦地区的公共交通网络。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Scattered_Spider">Scattered Spider - Wikipedia</a></li>
<li><a href="https://www.cybersecuritydive.com/news/what-we-know-about-the-cybercrime-group-scattered-spider/756312/">What we know about the cybercrime group Scattered Spider | Cybersecurity Dive</a></li>
<li><a href="https://www.cisa.gov/news-events/cybersecurity-advisories/aa23-320a">Scattered Spider | CISA</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#cybercrime`, `#Scattered Spider`, `#Transport for London`, `#guilty plea`

---

<a id="item-20"></a>
## [OpenAI 加入 Appia 基金会共建 AI 标准](https://openai.com/index/helping-build-shared-standards-for-advanced-ai) ⭐️ 7.0/10

OpenAI 宣布参与由 Linux 基金会发起的 Appia 基金会，共同为先进 AI 系统制定共享评估框架、安全实践和合规规范。 这一合作旨在推动 AI 安全实践的行业标准化，可能加速负责任部署并建立公众对先进 AI 系统的信任。 Appia 基金会提供开放连接层，包括测试标准、评估指南和组件分类，用于验证和审计安全可信的 AI 模型及应用。

rss · OpenAI News · 6月23日 13:00

**背景**: Appia 基金会由 Linux 基金会发起，旨在建立 AI 价值链的标准化合规规范。AI 安全评估框架是在部署前和部署中系统评估 AI 系统是否满足既定安全标准的方法体系。OpenAI 的参与标志着行业在 AI 治理方面走向合作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://appiafoundation.org/">Appia Foundation</a></li>
<li><a href="https://www.linuxfoundation.org/press/linux-foundation-launches-appia-foundation-to-establish-standardized-conformity-specifications-across-the-ai-value-chain">Linux Foundation Launches Appia Foundation to Establish ...</a></li>
<li><a href="https://aisecurityandsafety.org/en/glossary/ai-safety-evaluation-framework/">AI Safety Evaluation Framework</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#standards`, `#OpenAI`, `#governance`, `#collaboration`

---

<a id="item-21"></a>
## [中国内存制造商与微软的 AI 激励](https://stratechery.com/2026/memory-chips-and-china-microsoft-and-chinese-models/) ⭐️ 7.0/10

Ben Thompson 认为，三大内存芯片制造商可能会后悔为中国竞争对手（如 YMTC）敞开大门，而微软则有强烈动力采用中国 AI 模型，例如 DeepSeek。 这一分析凸显了半导体地缘政治与 AI 战略的交汇，将影响关键技术的全球供应链和竞争格局。 YMTC 采用专有的 Xtacking 技术生产 NAND 闪存，而 DeepSeek-V3 是一个具有 671B 总参数的混合专家模型。该分析将这些发展与公司战略和国际贸易的影响联系起来。

rss · Stratechery · 6月23日 10:00

**背景**: 长江存储（YMTC）是一家中国 NAND 闪存制造商，尽管面临美国出口限制，仍在扩大产能。DeepSeek 是一家由中国对冲基金 High-Flyer 支持的 AI 公司，以开发高效的大语言模型而闻名。该新闻讨论了中美科技紧张局势如何影响全球科技公司的机遇与风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Yangtze_Memory_Technologies">Yangtze Memory Technologies - Wikipedia</a></li>
<li><a href="https://www.reuters.com/world/china/chinese-chipmaker-ymtc-plans-new-factories-amid-heightened-us-sino-trade-2026-04-14/">Chinese chipmaker YMTC plans new factories amid heightened US ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>

</ul>
</details>

**标签**: `#memory chips`, `#China`, `#Microsoft`, `#AI models`, `#geopolitics`

---

<a id="item-22"></a>
## [OpenAI 支持 AI 动画电影《Critterz》，预算 3000 万美元](https://t.me/zaihuapd/42125) ⭐️ 7.0/10

OpenAI 正在支持制作一部名为《Critterz》的动画长片，该片主要使用 OpenAI 的生成式 AI 工具（包括即将推出的 GPT-5 模型）制作。影片预算不到 3000 万美元，制作周期仅为 9 个月，远短于传统动画电影。 该项目展示了 AI 彻底改变电影制作的潜力，能大幅降低成本和制作时间，可能使独立创作者也能制作高质量动画。同时也展示了 OpenAI 的创意工具，表明该公司正从对话式 AI 扩展到媒体制作领域。 该片改编自 2023 年创作的同名病毒式传播短片，该短片是首批使用 OpenAI 创意工具的作品之一。长片版本正在与《帕丁顿熊 3》的编剧合作开发，计划在戛纳电影节首映，并于 2026 年全球影院上映。

telegram · zaihuapd · 6月23日 03:11

**背景**: 传统动画电影通常成本超过 1 亿美元，耗时 3-5 年，需要数百名艺术家团队。由 GPT-5 等模型驱动的 AI 生成动画可以自动化故事板、角色设计和渲染等方面。《Critterz》代表了一项开创性尝试，将 AI 整合到长片制作的整个流程中，可能为行业树立新标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vice.com/en/article/openai-is-getting-into-the-movie-business-with-critterz/">OpenAI Is Getting Into the Movie Business With 'Critterz'</a></li>
<li><a href="https://deadline.com/2026/05/open-ai-produced-animated-family-film-critterz-cannes-1236879586/">Open AI-Backed Animated Film 'Critterz' Heads To Cannes Market</a></li>
<li><a href="https://nativeforeign.co/work/critterz">Critterz</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI filmmaking`, `#animation`, `#GPT-5`

---

<a id="item-23"></a>
## [Valve 发布 Steam Machine：1049 美元起的小型游戏主机](https://store.steampowered.com/hardware/steammachine) ⭐️ 7.0/10

Valve 正式发布了 Steam Machine，这是一款起售价 1049 美元、运行 SteamOS 3 的紧凑型游戏主机，官方宣称其性能是 Steam Deck 的 6 倍以上。 这标志着 Valve 在初代 Steam Machine 失败后，借助成熟的 SteamOS 3 和 Steam Deck 的成功，重新进军专用游戏主机市场。它可能为客厅游戏提供一个强大的、原生 Steam 平台的传统主机替代方案。 Steam Machine 是一款约 6 英寸大小的立方体设备，附带 Steam Controller 无线适配器，并配有可自定义显示下载进度的 LED 灯条。用户还可以在硬件上安装其他操作系统。

telegram · zaihuapd · 6月23日 04:53

**背景**: SteamOS 是 Valve 基于 Linux 开发的游戏操作系统，最初于 2013 年发布，但在 2022 年为 Steam Deck 重新打造了 SteamOS 3.0。Steam Deck 是一款广受欢迎的手持游戏 PC，而新的 Steam Machine 旨在将相同的 SteamOS 体验带到更强大的家用主机形态中。提到的 6 倍性能提升很可能是指与 Steam Deck 的 APU 相比的原始图形性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SteamOS">SteamOS</a></li>
<li><a href="https://store.steampowered.com/steamos/">SteamOS</a></li>
<li><a href="https://store.steampowered.com/news/app/1675200/view/697641379212298072">Steam Deck - SteamOS 3.8 - Steam News</a></li>

</ul>
</details>

**标签**: `#Steam`, `#gaming hardware`, `#SteamOS`, `#console`, `#Valve`

---

<a id="item-24"></a>
## [美国人形机器人依赖中国零部件](https://t.me/zaihuapd/42129) ⭐️ 7.0/10

《华尔街日报》报道称，美国人形机器人在关键机体零部件上越来越依赖中国供应链，包括电机、关节、磁体和传感器。迪士尼的“奥拉夫”机器人使用了中国宇树科技的部件，特斯拉也正与中国供应商合作推进 Optimus 的量产准备。 这种依赖暴露了美国机器人产业的战略脆弱性，并促使两党提出法案来评估竞争力和供应链风险。如果中国控制关键零部件，美国企业可能面临中国供应商的成本优势或潜在的供应中断风险。 中国在 2025 年推出了 28 款人形机器人，数量接近美国企业的 3 倍。摩根士丹利估算，中国供应链最多可将相关制造成本压低三分之二。美国国会议员已于 2025 年 2 月提出法案，拟评估机器人竞争力及供应链风险。

telegram · zaihuapd · 6月23日 07:47

**背景**: 人形机器人是模仿人体形态的机器人，需要电机（执行器）、关节、磁体和传感器等复杂组件来实现运动和感知。这些零部件的供应链高度专业化，中国在磁体和传感器的制造上投入了大量资源。宇树科技是中国一家以四足机器人和人形机器人闻名的机器人公司，为其他企业供应零部件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/宇树科技">宇树科技 - 维基百科，自由的百科全书</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/686471535">人形机器人核心零部件和行业分析 - 知乎</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/1933912453382660680">深度 | 一天吃透 “人形机器人” 产业链，核心零部件全解</a></li>

</ul>
</details>

**标签**: `#humanoid robots`, `#supply chain`, `#US-China competition`, `#robotics industry`, `#manufacturing`

---

<a id="item-25"></a>
## [众多中国高校撤销外语专业](https://t.me/zaihuapd/42130) ⭐️ 7.0/10

包括对外经济贸易大学和北京语言大学在内的多所中国高校已停止日语笔译、意大利语口译等小语种硕士招生。教育部数据显示，2018 年至 2022 年间，共有 109 所高校撤销了 28 个外语相关专业。 这一转变反映了市场需求的变化和 AI 翻译工具的兴起，可能减少语言专业毕业生的就业前景，并重塑高等教育课程。削减可能导致专业领域或文化语境中人工翻译的短缺。 最常被撤销的专业包括日语、英语和朝鲜语。例如，济南大学停招朝鲜语、德语等 9 个本科专业；沈阳航空航天大学 2024 年暂停英语等 10 个专业招生。

telegram · zaihuapd · 6月23日 08:32

**背景**: 外语专业曾是中国高校的热门专业，但随着 AI 翻译的进步和全球交流需求的变化，招生人数下降。许多高校现在将资源重新分配给 STEM 和应用学科。这一趋势反映了国际上对语言教育的重新评估。

**标签**: `#education policy`, `#foreign language`, `#higher education`, `#China`, `#AI impact`

---

<a id="item-26"></a>
## [SpaceX 将于 2028 年发射欧洲火星车，NASA 提供支持](https://t.me/zaihuapd/42133) ⭐️ 7.0/10

美国宇航局周四确认，已选定 SpaceX 的猎鹰重型火箭于 2028 年底从肯尼迪航天中心发射欧洲航天局的罗莎琳德·富兰克林火星车。 这项历经 20 多年曲折的任务终于确定了运载火箭，标志着国际火星探测合作的重要里程碑。该火星车将寻找火星地表下是否存在过去或现在的生命迹象。 猎鹰重型是一种超重型运载火箭，由三个可重复使用的猎鹰 9 号芯级组成，产生超过 500 万磅推力。NASA 作为合作的一部分，提供关键硬件，包括火星车的钻探和采样系统。

telegram · zaihuapd · 6月23日 10:47

**背景**: 罗莎琳德·富兰克林火星车原为 ExoMars 任务，是由 ESA 领导的天体生物学任务，能够钻探至地下两米分析样本。猎鹰重型是目前世界上现役最强大的火箭，已执行过多次任务，包括发射卫星和前往火星轨道的货物。该任务是 ESA、NASA 和 SpaceX 的联合努力，融合了欧洲的科学仪器与美国的发射和硬件能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Falcon_Heavy">Falcon Heavy - Wikipedia Top Stories Falcon Heavy - SpaceX SpaceX Falcon Heavy — 12+ Flights, Specs, Payload & Mission ... Images SpaceX launch vehicles - Wikipedia Falcon Heavy & Starman - YouTube Starship's Twelfth Flight Test - SpaceX Falcon Heavy Compendium - ElonX.net</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rosalind_Franklin_(rover)">Rosalind Franklin (rover) - Wikipedia</a></li>
<li><a href="https://www.esa.int/Science_Exploration/Human_and_Robotic_Exploration/Exploration/ExoMars/ExoMars_rover">ESA - ExoMars rover</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Mars exploration`, `#NASA`, `#ESA`, `#Rosalind Franklin`

---