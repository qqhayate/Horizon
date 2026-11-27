---
layout: default
title: "Horizon Summary: 2026-11-27 (ZH)"
date: 2026-11-27
lang: zh
---

> 从 80 条内容中筛选出 9 条重要资讯。

---

1. [英伟达叫停对马来西亚、新加坡、泰国和印尼的 AI 服务器出货](#item-1) ⭐️ 8.0/10
2. [llama.cpp 的 AMD 专用分支引发本地 LLM 推理优化讨论](#item-2) ⭐️ 7.0/10
3. [勒索软件谈判公司 RansomwareHelp 首席技术官因电信欺诈被起诉](#item-3) ⭐️ 7.0/10
4. [谷歌引导 AI 智能体使用自家 Workspace MCP 服务器，但 Gmail 发信仍仅限合作伙伴](#item-4) ⭐️ 7.0/10
5. [arXiv 预印本声称在零锥上实现引力的背景无关代数量子化](#item-5) ⭐️ 7.0/10
6. [Show HN：在一个浏览器标签页内并排运行三台 Linux 虚拟机，各带独立浏览器](#item-6) ⭐️ 7.0/10
7. [Nextcloud 推出基于 ONLYOFFICE 分支 Euro-Office 的桌面办公应用](#item-7) ⭐️ 7.0/10
8. [新加坡总理表态：绝不允许新加坡成为规避美国芯片管制的通道](#item-8) ⭐️ 7.0/10
9. [阿斯麦 CEO 警告：全面断供中国只会加速其自研设备](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [英伟达叫停对马来西亚、新加坡、泰国和印尼的 AI 服务器出货](https://t.me/zaihuapd/45392) ⭐️ 8.0/10

英伟达已要求戴尔、美超微等主要制造伙伴暂停向马来西亚、新加坡、泰国和印度尼西亚发运搭载其先进处理器的 AI 服务器。据《金融时报》报道，四国买家已被告知相关订单无法出厂，目前尚不清楚这一冻结是否为临时措施。 这四个国家一直是中国 AI 公司获取英伟达最先进芯片的重要中转与远程接入枢纽，而这些芯片不能直接出口到中国大陆。因此，此次冻结直接重塑了亚洲的 AI 硬件供应链，并威胁到东南亚数十亿美元规模的数据中心建设浪潮——2025 年英伟达通过其新加坡子公司录得约 1040 亿美元收入，同比增长 72%。 此次停运源于美国商务部的新规：海外数据中心运营商和区域云服务商须在 90 天内取得美国出口许可，才能向位于中国等高风险国家的客户提供大规模算力，门槛设定为 1200 万 TPP。目前尚不清楚此次暂停属于临时性的合规审查，还是更长期的限制。

telegram · zaihuapd · 11月26日 15:14

**背景**: 美国出口管制此前已禁止英伟达最先进的 AI 加速器直接销往中国大陆。为绕开限制，中国 AI 公司转而从东南亚的数据中心租用算力，或采购在当地组装的服务器——戴尔和美超微正是把英伟达芯片组装成整机再在区域内转售的厂商。美国商务部的新规将许可要求扩展到海外数据中心运营商，从而堵上了这一“远程接入”漏洞，这也是英伟达在厘清规则适用范围期间暂缓发货的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/world/asia-pacific/nvidia-halts-chip-shipments-southeast-asia-ft-reports-2026-11-26/">Nvidia halts server shipments to four Southeast Asian ...</a></li>
<li><a href="https://aiweekly.co/alerts/nvidia-halts-ai-server-shipments-to-four-southeast-asian-nations-as-us-export">Nvidia Halts AI Server Shipments to Four Southeast Asian ...</a></li>
<li><a href="https://www.nytimes.com/2026/11/17/business/southeast-asia-china-ai-chips.html">Trump’s New A.I. Chip Rules Rattle Southeast Asia - The New York...</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#export-controls`, `#ai-hardware`, `#supply-chain`, `#geopolitics`

---

<a id="item-2"></a>
## [llama.cpp 的 AMD 专用分支引发本地 LLM 推理优化讨论](https://devnull.land/amd-specific-llama-cpp) ⭐️ 7.0/10

一位开发者在 devnull.land 的博客文章中公开了 llama.cpp 的 AMD 专用分支，目标是提升 AMD GPU 上的本地大语言模型推理性能。该文章及其在 Hacker News 上的讨论重点在于挖掘非主流 AMD 硬件的性能，尤其是 2018 年前后的 gfx906 数据中心系列显卡。 llama.cpp 实际上已成为大多数本地 LLM 工具背后的标准推理内核，因此针对 AMD 瓶颈的修复分支能直接扩大爱好者和中小团队在不购买 NVIDIA 硬件的前提下可运行的模型范围。这也说明一个不断壮大的社区正在从厂商已不再重点支持的廉价高带宽 AMD 显卡中挖掘可用的 AI 性能。 所讨论的 gfx906 显卡没有张量核心，也不原生支持 bf16，因此要获得良好吞吐量需要定制内核和精细的量化处理，而不能依赖默认代码路径。讨论者表示手工调优的 AMD 内核带来了大幅加速，同时也有观点提到无需 ROCm 的 Vulkan 后端等替代推理引擎。

hackernews · julianlam · 11月26日 17:11 · [社区讨论](https://news.ycombinator.com/item?id=50657265)

**背景**: llama.cpp 是一个开源库，由 Georgi Gerganov 于 2023 年 3 月发起，并与 GGML 张量库共同开发，可在消费级硬件上运行量化 LLM 推理，是 Ollama、LM Studio 等工具的底层核心。在 AMD GPU 上它通常通过 ROCm 运行，这是 AMD 的开放 GPU 编程软件栈，提供 HIP、OpenMP 和 OpenCL 等编程模型，成熟度总体不及 NVIDIA 的 CUDA。gfx906 指的是 AMD 2018 年推出的 Vega 20 架构数据中心显卡（如 MI50/MI60 和 Radeon VII），它们计算性能一般但配备高带宽 HBM2 显存，这对受显存带宽限制的 LLM 解码过程很有吸引力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">Llama.cpp</a></li>
<li><a href="https://en.wikipedia.org/wiki/AMD_ROCm">AMD ROCm</a></li>
<li><a href="https://rocm.blogs.amd.com/artificial-intelligence/llm-inference-optimize/README.html">Large language model inference optimizations on AMD GPUs</a></li>

</ul>
</details>

**社区讨论**: 评论者总体态度积极：有人指出拥有约 1 TB/s 带宽的 32GB gfx906 显卡只需约 200 美元，而性能相当的现代显卡要 3000 美元以上，由此催生了一个围绕 llama.cpp 优化的小型生态。其他人分享了实测结果，例如一位 Radeon R9700 用户称赞某替代引擎达到 2400 tok/s 的预填充和 150 tok/s 的解码速度，还有一位 MI100 用户借助 AI 助手将 NVIDIA 内核移植到 ROCm，获得 2 至 3 倍加速。一个反复出现的观点是，真正在 AMD 和苹果硬件上带来大幅提升的不只是 llama.cpp 本身，还有各类替代运行时和移植版本。

**标签**: `#llama.cpp`, `#AMD`, `#LLM inference`, `#GPU optimization`, `#local AI`

---

<a id="item-3"></a>
## [勒索软件谈判公司 RansomwareHelp 首席技术官因电信欺诈被起诉](https://krebsonsecurity.com/2026/11/cto-of-ransomwarehelp-indicted-for-wire-fraud/) ⭐️ 7.0/10

此案将聚光灯对准了基本不受监管的勒索软件谈判行业——处于极端压力下的受害企业依赖中间人，而这些中间人的经济激励可能与受害者利益相冲突。它同时也在检验美国欺诈法的适用范围能延伸至事件响应合同的何种程度，并可能促使企业重新审视谈判方的收费方式与其作出的承诺。 根据对起诉书的讨论，涉案金额相对整个事件而言并不大：所谓的勒索软件组织索要约 1.3 万美元，公司仅加价约 260 美元（2%），另收取 2750 美元的诊断费。核心指控似乎在于公司对资金流向以及是否真的存在威胁行为者作出了实质性虚假陈述，而非加价幅度本身。

hackernews · Bender · 11月26日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=50657645)

**背景**: 勒索软件谈判公司受受害机构聘请，负责与勒索团伙沟通、评估对方交付解密密钥的可能性，并就支付赎金提供建议。由于支付赎金可能触及制裁规定并带来声誉风险，许多此类公司公开将自己定位为不协助付款的角色。电信欺诈（美国法典第 18 编第 1343 条）是一项联邦罪名，涵盖通过跨州电子通信以欺骗手段获取钱财的图谋，这正是本案中营销宣传与客户沟通内容成为焦点的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtarget.com/cybersecurity/feature/Why-using-ransomware-negotiation-services-is-worth-a-try">Why using ransomware negotiation services is worth... | TechTarget</a></li>
<li><a href="https://www.group-ib.com/resources/knowledge-hub/ransomware-negotiation/">Ransomware Negotiation : What Enterprises Should Know</a></li>

</ul>
</details>

**社区讨论**: 评论者对这一行为是否真正构成电信欺诈看法不一：他们认为确实存在明显的实质性欺骗，但鉴于受害者确实以自己接受的价格拿回了数据，对“欺诈意图”表示怀疑。另一些人认为，欺诈的要害在于一边宣传“我们从不支付赎金”、一边却真的付了钱，并建议把合同改写为披露“紧急情况下可付款”的选项；也有少数人纯粹觉得此事荒诞可笑。

**标签**: `#cybersecurity`, `#ransomware`, `#fraud`, `#legal`, `#security-ethics`

---

<a id="item-4"></a>
## [谷歌引导 AI 智能体使用自家 Workspace MCP 服务器，但 Gmail 发信仍仅限合作伙伴](https://techstackups.com/articles/google-workspace-ai-agents-mcp/) ⭐️ 7.0/10

谷歌正引导 AI 智能体使用其自家托管的远程 Workspace MCP 服务器，这些服务器开箱即用地提供覆盖 Gmail、Drive、Docs、Sheets、Slides、Calendar、Chat 和 Tasks 的预置工具。不过，Gmail 服务器中真正“发送邮件”的能力仅向部分合作伙伴开放，而非面向所有开发者，这引发了关于该限制究竟是出于安全还是商业考量的争论。 通过自行托管 MCP 服务器，谷歌实际上成为了第三方智能体访问 Workspace 数据的把关者，把一个开放协议变成了平台控制点。如果最有价值的操作——以用户身份发信——仅对合作伙伴开放，其他智能体平台和初创公司就可能面临锁定，或被迫转向浏览器自动化、原生 SMTP/IMAP 等替代方案。 Workspace MCP 服务器基于开放的 MCP 标准构建，目前以预览形式提供，可让云端和网页端智能体直接调用预置工具。关键限制在于，读取类访问与发送类访问被区别对待：发送邮件被提升为合作伙伴计划，而 Gmail、Drive、Calendar 等数据类工具仍可普遍配置使用。

hackernews · ritzaco · 11月26日 09:44 · [社区讨论](https://news.ycombinator.com/item?id=50653477)

**背景**: MCP（Model Context Protocol，模型上下文协议）是由 Anthropic 提出的开源标准，用于把 AI 应用连接到数据源、工具和工作流等外部系统，以统一协议取代零散的一次性集成。Google Workspace 的 MCP 服务器把这一标准应用到 Gmail、Drive、Docs、Calendar 等产品上，使 AI 智能体能够代表用户执行操作。谷歌表示智能体必须经由这些服务器才能安全地与 Workspace 交互，但批评者指出，MCP 本身已内置“elicitation（征询）”原语，允许服务器暂停工具调用并在执行前请求用户确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.google.com/workspace/guides/configure-mcp-servers">Configure the Google Workspace MCP servers | Google for...</a></li>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )?</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍持怀疑态度：有人指出 MCP 内置的 elicitation 机制本身就能实现人工确认，因此仅限合作伙伴的做法更像是商业决策而非安全措施。还有人认为用户会直接用浏览器自动化，或通过 NeoMutt 等客户端走原生 SMTP/IMAP 绕过限制；也有人将此与雇主把 API 转向按用量计费、以便对数据提取收费的趋势联系起来。

**标签**: `#MCP`, `#Google Workspace`, `#AI Agents`, `#Platform Lock-in`, `#API Access`

---

<a id="item-5"></a>
## [arXiv 预印本声称在零锥上实现引力的背景无关代数量子化](https://arxiv.org/abs/2611.34924) ⭐️ 7.0/10

一篇新的 arXiv 预印本（2611.34924）提出在四维洛伦兹时空上对真空广义相对论做背景无关的量子化：从一阶引力出发，在体区域相交的零锥上求解引力约束，得到有限牛顿常数 G_N 下的约化相空间。作者随后把该约化相空间的正则泊松括号提升为对易关系，并利用约化作用量的形变来定义可观测量代数，还给出高斯波函数、因果菱形的希尔伯特空间以及通向黑洞熵的离散面积谱。 如果这一构造站得住脚，它将是罕见的、在有限 G_N 下完成的非微扰且背景无关的引力量子化方案，并且还能给出黑洞熵——这正是量子引力研究者追求了数十年的结果。由于它是一篇尚未经过同行评审、又触及著名难题的预印本，其关注度已远远超出专业圈子（数百点热度、数十条评论）。 评论者指出，该论文似乎得到的是 Type I 型 von Neumann 代数，而在包含引力时通常预期应为 Type II 型；他们还质疑洛伦兹路径积分是如何被严格构造的，以及在相交零锥上量子化如何与背景无关性相容。摘要中也没有给出任何新的、可实验检验的预言，而这正是不少读者所追问的。

hackernews · hecmmm · 11月26日 05:37 · [社区讨论](https://news.ycombinator.com/item?id=50651863)

**背景**: 量子化引力就是把广义相对论中的度规变成量子对象，而其核心难点在于该理论是背景无关的——没有一个固定的时空舞台来定义场，因此标准量子场论工具不能直接套用。代数方法则用可观测量代数及其在希尔伯特空间上的表示来刻画理论；von Neumann 代数的“型”（I、II、III）编码了诸如是否存在合理的熵或迹这样的结构性质，而 Type II 型代数近年正是黑洞熵与量子场论中引力熵研究进展的关键。零锥方法（或称特征初值方法，与光前量子化相关）用类光曲面叶化时空并处理特征初值问题，从而使约束简化，数据定义在类光超曲面而非类空切片上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2611.34924v1">An algebraic quantization of gravity from the null cone</a></li>
<li><a href="https://arxiv.org/pdf/2308.03663">A Background - Independent Algebra in Quantum</a></li>
<li><a href="https://en.wikipedia.org/wiki/Light_front_quantization">Light front quantization - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论持怀疑态度且颇具技术含量：评论者质疑 Type I 型代数、洛伦兹路径积分的严格性以及背景无关性主张的自洽性，也有人追问该论文是否给出任何可检验的预言。多位参与者引用了 r/physics 版主的说明，指出围绕该文的争论大多是关于 AI 而非量子引力，并认为明智的做法是等待该领域研究者的评审。

**标签**: `#quantum gravity`, `#theoretical physics`, `#arxiv preprint`, `#algebraic QFT`, `#peer review`

---

<a id="item-6"></a>
## [Show HN：在一个浏览器标签页内并排运行三台 Linux 虚拟机，各带独立浏览器](https://michidk.github.io/sidebyside/) ⭐️ 7.0/10

一个发布在 michidk.github.io/sidebyside 的 Show HN 演示，在单个浏览器标签页内并排运行三台独立的 Linux 虚拟机，每台虚拟机各自运行一个浏览器实例。据评论者推测，该演示建立在此前几天登上 Hacker News 的 trynix 与 unkernel 项目之上。 它体现了标签页内虚拟化已经走到哪一步：不再只是一个模拟的 Linux 终端，而是可以在完全客户端、无服务器参与的情况下启动多台相互隔离的机器和完整的浏览器实例。这种“每个应用一个浏览器、每个浏览器跑在独立 unikernel 上”的隔离模型，与沙箱、一次性环境和基于浏览器的安全研究直接相关。 有评论者指出该页面并未启用跨源隔离（cross-origin isolation），这通常会限制对 SharedArrayBuffer 和多线程 WebAssembly 能力的访问；另一位评论者则发现演示会下载一个 ONNX Runtime 包，其原因并未说明。作为一个演示而非正式发布，它没有提供文档、基准测试或性能说明。

hackernews · michidk · 11月26日 15:00 · [社区讨论](https://news.ycombinator.com/item?id=50656036)

**背景**: 在浏览器标签页里跑 Linux 之所以变得可行，要归功于在运行时把 x86 机器码翻译成 WebAssembly 的引擎，例如 WebVM 使用的 CheerpX 和 LinuxOnTab 使用的 v86 模拟器，它们可以在客户端启动未经修改的 Linux 二进制文件，甚至启动带 Alpine 用户态的真实内核。Unikernel 走的是另一条路：不提供通用操作系统，而是把每个应用与一个最小化、专用化的内核一起编译，使实例体积小、启动快、隔离强——kernel.sh 项目正是用这种方式让每个应用实例都在基于 Unikraft 的 unikernel 上运行自己的 Chromium。把这两种思路结合起来，一个标签页就能承载多个相互独立的“浏览器盒子”。浏览器通常要求启用跨源隔离（COOP/COEP 响应头）后才会授予页面 SharedArrayBuffer 和线程等强大能力，这也是讨论中出现该话题的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://themenonlab.blog/blog/webvm-linux-browser-cheerpx-wasm">WebVM: Full Linux in Your Browser via WebAssembly</a></li>
<li><a href="https://linuxontab.com/">LinuxOnTab — Real Linux in your browser . No install, no server, no...</a></li>
<li><a href="https://www.kernel.sh/docs/info/unikernels">Browsers on Unikernels - Kernel</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的反应既热情又偏技术：评论者称赞了这个演示，并推测它基于近期的 trynix 与 unkernel 工作，还有开发者分享了一个把浏览器标签页当作容器的相关项目 tabc 并征求反馈。另一些人提出了具体的技术疑问，指出页面未启用跨源隔离，并追问为何要下载 ONNX Runtime 包。

**标签**: `#Linux virtualization`, `#WebAssembly`, `#browsers`, `#unikernels`, `#Show HN`

---

<a id="item-7"></a>
## [Nextcloud 推出基于 ONLYOFFICE 分支 Euro-Office 的桌面办公应用](https://nextcloud.com/blog/euro-office-comes-to-your-desktop-with-the-nextcloud-office-desktop-app/) ⭐️ 7.0/10

Nextcloud 发布了 Nextcloud Office 桌面应用，把 ONLYOFFICE 的 Euro-Office 分支（该分支于 2026 年 3 月首次亮相，定位为面向欧洲的 Microsoft 365 替代方案）从浏览器和移动端延伸到了桌面端。该应用让 Nextcloud 用户可以在 Windows、macOS 和 Linux 上原生编辑文档、表格和演示文稿。 原生桌面客户端让自托管的 Nextcloud 更有资格成为 Microsoft 365 和 Google Workspace 的日常替代品，因为许多用户仍然需要可离线使用、功能完整的编辑器，而不是浏览器标签页。这也让仍属年轻的 Euro-Office 分支借助广泛部署的开源协作平台获得了第一个重要的分发渠道。 社区观察者指出，该应用似乎是使用 Chromium Embedded Framework 封装 C++ 内核的壳层；同时 Euro-Office 的 DocumentServer 变更日志似乎缺少 ONLYOFFICE 于 2026 年 10 月 12 日发布的 10.0.0 版本中所列的 46 项安全相关修复中的许多项。用户还反映现有基于浏览器的 Nextcloud Office 存在不少粗糙之处，尤其是在编辑 .xlsx 文件和渲染 PDF 时。

hackernews · e12e · 11月26日 11:50 · [社区讨论](https://news.ycombinator.com/item?id=50654289)

**背景**: ONLYOFFICE 是一套开源办公套件与协作平台，提供文档、表格、演示文稿和 PDF 编辑器，既可自托管部署，也有桌面版本。Euro-Office 是 2026 年 3 月宣布的 ONLYOFFICE 分支，定位为“欧洲制造”的开源自由软件版 Microsoft 365 替代方案；它一诞生就引发了关于其许可证和治理可信度的争论。Nextcloud 是一个开源、可自托管的协作平台，此前主要通过集成 ONLYOFFICE DocumentServer 的网页方式来提供办公编辑功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.omgubuntu.co.uk/2026/11/euro-office-desktop-apps-nextcloud">Euro-Office, the ONLYOFFICE fork, now has a desktop app</a></li>
<li><a href="https://itsfoss.com/news/onlyoffice-forked/">ONLYOFFICE Gets Forked as "Made in Europe", Sparks Licensing ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Euro-Office">Euro-Office - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一：一些用户称赞其表格体验在外观和手感上都非常出色，并乐见终于能摆脱 OpenOffice；另一些人则提醒这是一个由官僚化的企业联盟运营的争议性分支。最尖锐的担忧集中在安全上——评论者指出 Euro-Office 的变更日志似乎遗漏了 ONLYOFFICE 10.0.0 中已有的修复；同时还有人抱怨现有在线版 Nextcloud Office 在处理 .xlsx 编辑和 PDF 渲染方面依然很糟糕。

**标签**: `#Nextcloud`, `#ONLYOFFICE`, `#open-source office`, `#desktop apps`, `#security`

---

<a id="item-8"></a>
## [新加坡总理表态：绝不允许新加坡成为规避美国芯片管制的通道](https://t.me/zaihuapd/45381) ⭐️ 7.0/10

新加坡总理黄循财表示，不允许新加坡被当作企业规避美国芯片出口管制的通道，并确认当局正在调查 Megaspeed 采购英伟达芯片的交易。此番表态的前一天，美国商务部已将 Megaspeed 及另外 6 家东南亚企业列入贸易黑名单，其中包括其在马来西亚、泰国的关联实体，以及阿里巴巴的新加坡子公司 Apex Enterprise Solutions。 这一公开承诺表明，作为 AI 硬件重要转运枢纽的东南亚正被牢牢纳入美国半导体出口管制的执法范围，区域内分销商、云服务商和数据中心运营商面临的合规风险随之上升。这也给依赖第三国实体获取受限英伟达加速器的中资关联企业带来压力，可能重塑亚洲 AI 算力资源的获取方式。 《联邦公报》称这些企业存在向未获授权用户转移先进计算产品的「重大风险」，名单涵盖 Megaspeed 在马来西亚和泰国的关联实体，以及阿里巴巴新加坡子公司 Apex Enterprise Solutions。黄循财强调新加坡不会为绕开管制提供路径，但他与美方文件均未披露受调查芯片的数量或最终流向。

telegram · zaihuapd · 11月26日 07:38

**背景**: 美国「实体清单」是一份贸易黑名单，出口商在向清单上的实体运送美国原产技术前必须申请许可，而此类许可通常会被拒绝；它已成为限制中国获取英伟达 GPU 等先进 AI 加速器的主要工具。由于对华直接出货受到严格限制，执法重点逐渐转向新加坡、马来西亚、泰国等中转枢纽和中间商，芯片可能在这些地方被改道转运。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mha.gov.sg/media-room/newsroom/singapore-investigations-into-alice-huang-huang-le-and-megaspeed-international-pte-ltd/">Singapore’s Investigations into Alice Huang (Huang Le) and ...</a></li>
<li><a href="https://www.bbc.com/news/articles/cmn504nq5033o">US government confirms investigation into tech firm Megaspeed</a></li>
<li><a href="https://www.reuters.com/world/china/how-china-got-access-nvidias-ai-chips-despite-rules-stop-them-2026-11-25/">How China got access to Nvidia's AI chips despite rules to ...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#Singapore`, `#Nvidia`, `#semiconductor supply chain`

---

<a id="item-9"></a>
## [阿斯麦 CEO 警告：全面断供中国只会加速其自研设备](https://t.me/zaihuapd/45391) ⭐️ 7.0/10

阿斯麦 CEO 富凯（Christophe Fouquet）在 Semafor 的《Future Proof》节目中表示，出口管制应当只保护最先进的技术，而不能把中国完全排除在外，否则会促使中国在自研设备上“加倍甚至三倍投入”。他还表示，阿斯麦卖给中国的设备落后最先进制程十多年，而正是维持这道代差，才让中国继续依赖西方设备。 这番表态来自芯片供应链中最关键的“卡脖子”供应商，直接挑战了美国主导的收紧管制背后的逻辑，把政策选择重新定义为“管理技术代差”而非彻底脱钩。如果这一论点在盟国政府中获得认同，未来针对 DUV 设备及维护服务的限制节奏和范围可能改变，从而影响中国芯片制造商及其设备供应商。 富凯指出，阿斯麦近 30 年来在中国光刻机市场的份额接近 100%，他认为这让中国接受了对其技术的依赖；美国正在推动的 MATCH 法案拟把管制范围从 EUV 扩大到浸没式 DUV 和维护服务，荷兰政府和阿斯麦均表示反对。另有报道称中国已造出 EUV 原型机，并在探索稳态微聚束（SSMB）、激光诱导放电等离子体（LDP）等替代光源路线，但距离量产成熟仍有很大差距。

telegram · zaihuapd · 11月26日 14:56

**背景**: 光刻是把电路图案印到硅片上的关键工序，所用光源的波长决定了能刻出的最小特征尺寸。DUV（深紫外）设备是成熟制程和中端制程的主力机型，而最先进的 5 纳米及以下逻辑芯片则需要 EUV（极紫外，13.5 纳米），目前全球只有阿斯麦一家公司销售量产型 EUV 系统。由于这条供应链极难复制，光刻设备出口管制已成为美中科技博弈的核心杠杆，而 MATCH 法案正是试图把管制进一步下沉到较老的 DUV 设备及维护服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EUV_lithography">EUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://informedclearly.com/en/geopolitics/60865/semiconductor-export-controls-match-act-2026">Semiconductor Export Controls 2026: MATCH Act and Japan</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#export-controls`, `#ASML`, `#China-tech`, `#geopolitics`

---