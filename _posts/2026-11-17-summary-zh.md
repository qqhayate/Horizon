---
layout: default
title: "Horizon Summary: 2026-11-17 (ZH)"
date: 2026-11-17
lang: zh
---

> 从 98 条内容中筛选出 17 条重要资讯。

---

1. [vLLM v0.34.0 发布：默认启用可扩展 KV 缓存、移除 Model Runner V1、Blackwell 显著提速](#item-1) ⭐️ 8.0/10
2. [卡内基梅隆大学推出 CS Learn，在 YouTube 免费发布计算机课程讲座](#item-2) ⭐️ 8.0/10
3. [Optimizely 遭入侵，通过其 CDN 向 Zoom、GitLab 等大站投递恶意脚本](#item-3) ⭐️ 8.0/10
4. [BurntSushi 发布 Rust 新日期时间库 Jiff 1.0](#item-4) ⭐️ 8.0/10
5. [阿里、腾讯、月之暗面在新模型中收紧攻击性网络能力](#item-5) ⭐️ 8.0/10
6. [报告称 Windows 11 会收集开发者所用编程代理与开发工具的遥测数据](#item-6) ⭐️ 7.0/10
7. [摩根大通技术故障引发多家美国银行网上银行服务中断](#item-7) ⭐️ 7.0/10
8. [Linebender 深入解析超椭圆圆角矩形 Squircles 的数学与设计](#item-8) ⭐️ 7.0/10
9. [博主探索用原生 Three.js 打造 3A 级光照渲染管线](#item-9) ⭐️ 7.0/10
10. [Harmonic 的 Aristotle 形式化验证工具扩展支持 Rust](#item-10) ⭐️ 7.0/10
11. [Black Forest Labs 创始人谈视觉智能与 AGI](#item-11) ⭐️ 7.0/10
12. [萨提亚·纳德拉谈 AI 让代码变便宜之后的软件工程](#item-12) ⭐️ 7.0/10
13. [OpenAI 将计算机使用智能体引入医疗团队](#item-13) ⭐️ 7.0/10
14. [Maxwell-V1.0-Flash：35B 总参数 MoE 模型，支持 256K 上下文与学习式块稀疏注意力](#item-14) ⭐️ 7.0/10
15. [Hugging Face 将语言模型推理路由切换至 OpenRouter](#item-15) ⭐️ 7.0/10
16. [美商务部将定稿新规，封堵经东南亚远程使用 AI 芯片的漏洞](#item-16) ⭐️ 7.0/10
17. [丘成桐牵头成立数学与 AI 实验室联盟](#item-17) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.34.0 发布：默认启用可扩展 KV 缓存、移除 Model Runner V1、Blackwell 显著提速](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM 发布 v0.34.0 版本，由 412 位贡献者（其中 120 位新贡献者）提交的 1,061 个 commit 构成，新增 10 个模型，包括 Mistral Large 4（总参数 1T、激活 52B）和 NVIDIA Nemotron-3.5-Transcribe。该版本将可扩展 KV 缓存容量计算设为默认行为，移除 Model Runner V1 使 Model Runner V2 成为唯一的 GPU 执行器，默认块大小从 16 提升到 64，并在 GB200 上实现最高 1.95 倍解码加速、在 AMD MI355X 上实现 1.6 倍吞吐提升。 vLLM 是使用最广泛的开源大模型推理与 serving 引擎之一，因此其默认行为的改动会直接传导到整个生态的生产部署中。自动化的 KV 缓存容量计算让多数模型无需调优即可获得更大的缓存和高并发下更高的吞吐，而移除 Model Runner V1 等破坏性变更则迫使运维方在升级前必须审查现有配置。 可扩展 KV 缓存不再基于估算值，而是依据 CUDA 图捕获与预热后实际空闲的显存来分配，在 H200 上使 MiniMax-M3 的缓存容量从 433k 提升到 672k token，但在并发 128 时某些模型的单 token 解码延迟（TPOT）可能增加 6%–18%；可通过 --gpu-memory-utilization 0.9 或 --no-enable-extensible-kv-cache 关闭。其他升级注意事项包括：不再提供 ROCm 7.2 构建产物、要求 huggingface_hub >= 2.0.0，以及移除 QuTLASS/fp_quant、Marlin W4A8 和 Keye-VL 支持。

github · khluu · 11月16日 23:22

**背景**: vLLM 是一个用于大模型推理服务的开源引擎，其核心创新是 PagedAttention——它把 KV 缓存（每个请求的键值张量，用于避免对整段 prompt 重复计算注意力）像虚拟内存分页那样存放在不连续的块中。块大小决定每个缓存块能容纳多少 token，因此默认值从 16 提到 64 是以更粗的粒度换取更低的簿记开销。“Model Runner”是真正在 GPU 上执行模型前向计算的组件；V2 是模块化、GPU 原生的重写版本，避免了每步都要经过 Python 调度的开销，本次发布通过删除 V1 完成了迁移。在 GB200（NVIDIA Blackwell）和 MI355X（AMD CDNA 4，288GB HBM3E）上报告的加速来自厂商专用 kernel，包括 FP8/NVFP4 路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/configuration/optimization/">Optimization and Tuning - vLLM</a></li>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V 2 : A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://openrelay.inc/gpus/mi355x">AMD Instinct MI 355 X Price: $6.30/hr per GPU | OpenRelay</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#model-serving`, `#release-notes`, `#gpu-performance`

---

<a id="item-2"></a>
## [卡内基梅隆大学推出 CS Learn，在 YouTube 免费发布计算机课程讲座](https://www.cs.cmu.edu/learn/) ⭐️ 8.0/10

卡内基梅隆大学 Griffin 计算机科学学院推出了 CS Learn（cs.cmu.edu/learn），在 YouTube 上免费发布 CMU 当前计算机科学课程的完整学期讲座视频，发布周内每天上线一门新课，明年 1 月还将推出更多课程。该项目由 CMU 讲师 Phillip Compeau 负责，部分学生开发了用于自动化大量制作流程的工具。 顶尖计算机科学项目免费放出当前课程的完整学期讲座，而不是预告片或 MOOC 式的重制版本，这大幅拓宽了自学者、其他高校学生和从业者获取高质量计算机教育的机会。在开放课程内容自 MIT 最初发布以来大多停留在讲义与笔记层面的生态中，此举也会给其他顶尖院系带来跟进压力。 这些视频是 CMU 现行课程目录中的真实课堂录像，而非专门制作的在线课程，涵盖计算机图形学（15-462/662）和 Tianqi Chen 的 ML Systems 等主题，评论中还提到 15-259 概率与计算课程即将上线。目前尚不清楚作业、课后习题和考试是否会随视频一起发布，这也是它与完全开放的课程之间的主要差距。

hackernews · pcompeau · 11月16日 20:43 · [社区讨论](https://news.ycombinator.com/item?id=50522980)

**背景**: 开放课程（OpenCourseWare，OCW）指大学将讲座笔记、视频、作业等课程材料免费发布在互联网上。这一运动始于 20 世纪 90 年代末，并在 2001 年 MIT 宣布其 OpenCourseWare 计划后获得全球关注，最终几乎公开了全部课程的材料。传统 OCW 项目往往缺少完整课堂录像，而 YouTube 后来成为录制讲座的重要分发渠道。CMU 的课程编号（计算机科学课程以 15-开头）是学生称呼课程时使用的内部代码，例如 15-122 命令式计算原理或 15-251 理论计算机科学伟大思想。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenCourseWare">OpenCourseWare</a></li>
<li><a href="https://ocw.mit.edu/about/">About Us | MIT OpenCourseWare | Free Online Course Materials</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪非常积极，项目负责人 Phillip Compeau 亲自到场解释由学生构建的自动化工具，评论者则请求发布 15-122、15-150、15-251、15-451 等核心课程，并询问是否会一并公开作业。校友特别提到 Tianqi Chen 的 ML Systems 和 15-259 概率与计算是亮点，还有一条高赞评论认为，只有把基础学扎实，AI 才会成为你的强力工具，否则就会取代你。

**标签**: `#computer-science-education`, `#open-courseware`, `#online-learning`, `#YouTube`, `#ML-systems`

---

<a id="item-3"></a>
## [Optimizely 遭入侵，通过其 CDN 向 Zoom、GitLab 等大站投递恶意脚本](https://blog.report-uri.com/worlds-largest-brands-infected-with-malware-via-optimizely/) ⭐️ 8.0/10

被广泛使用的实验与数字体验平台 Optimizely 遭到入侵，其 CDN 向包括 Zoom、GitLab 在内的多个大型网站的访问者投递了恶意 JavaScript，恶意代码同样出现在 Optimizely 自家的 www.optimizely.com 与 login.optimizely.com 页面上。该事件由 report-uri.com 披露，其分析强调这并非 CDN 缓存投毒——边缘节点只是原样返回了被写入 Optimizely 存储的内容，说明攻击者取得了对大量互不相关的客户项目的写权限。 这是一次典型的 Web 软件供应链攻击：由于成千上万个网站都嵌入了 Optimizely 脚本，单一供应商被攻破就让攻击者的触角瞬间覆盖所有这些网站的访问者，其中还包括 Zoom、GitLab 这类安全敏感站点。它也进一步激化了长期存在的争论——由市场部门驱动的第三方 JavaScript 实际上是一条缺乏问责与审计、却直通生产环境页面的代码执行通道。 据该分析称，Optimizely 的 CDN 并未在传输环节被投毒或劫持，恶意载荷是被写入了 CDN 所提供服务的客户项目数据中，这意味着要么是 Optimizely 自身系统被攻破，要么是具备跨客户访问权限的凭据被盗——文中表示这个问题只有 Optimizely 才能解释。由于 Optimizely 脚本是在运行时从供应商域名动态加载的，网站很难用子资源完整性（SRI）或严格的内容安全策略（CSP）白名单把它固定住，因此客户端并没有任何校验能发现脚本被篡改。

hackernews · kristjansson · 11月16日 23:00 · [社区讨论](https://news.ycombinator.com/item?id=50524767)

**背景**: Optimizely 是一个用于 A/B 测试与数字体验优化的平台（如今也包含 CMS 与电商能力的“DXP”）：客户在页面中粘贴一小段 JavaScript 片段，该片段在运行时从 Optimizely 的 CDN 加载更多代码，从而让市场人员无需发版就能改动页面内容。以这种方式加载的脚本拥有宿主页面的全部权限，这正是第三方标签成为 Magecart 式（窃取凭据与支付数据）攻击经典入口的原因。此前的多起事件——例如攻击者滥用托管在 CDN 上的脚本，以及利用被盗的 CDN 凭据把正规插件变成恶意软件投放工具——都说明这是一个反复出现的模式，而非孤立事件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://firstlinesoftware.com/blog/what-is-optimizely/">What is Optimizely and Why Do You Need It? - First Line Software</a></li>
<li><a href="https://pulse.cafiyn.com/signals/story/third-party-script-tag-risk">Third Party Script Risk : Auditing Your Embeds · Cafiyn Pulse</a></li>
<li><a href="https://getshieldsecurity.com/blog/shieldnotes-113/">WordPress Plugin Vulnerabilities & the Hidden OptinMonster CDN ...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上对现状持批评态度：不少人把如今每篇文章都加载数 MB JavaScript 的局面前追溯到 Google Tag Manager 最初的设想——让市场部门无需工程团队介入即可添加标签；也有人认为根本问题是完全没有问责机制，称 Optimizely 本应具备分批发布、冷却期与自动化安全检查，而像 CNN、BBC 这样的大站根本没有理由直接嵌入供应商代码。也有人提出技术性反问：大型新闻网站真的会在同一来源下处理加密货币或支付数据吗，还是说同时还存在浏览器安全漏洞；另有评论推荐 NoScript 之类的防御工具来降低暴露面。

**标签**: `#security`, `#supply-chain`, `#javascript`, `#web-security`, `#optimizely`

---

<a id="item-4"></a>
## [BurntSushi 发布 Rust 新日期时间库 Jiff 1.0](https://burntsushi.net/jiff/) ⭐️ 8.0/10

知名 Rust 开发者 Andrew Gallant（BurntSushi）发布了 Rust 日期时间库 Jiff 的 1.0 版本，该库主打难以误用且性能合理的高层日期时间原语。1.0 里程碑意味着 API 趋于稳定，发布文档还明确说明了在什么场景下 Jiff 并不是合适的选择。 日期时间处理是编程中最容易出错的领域之一，而 Rust 生态长期依赖 API 存在已知缺陷的 chrono，因此一个由受人尊敬的维护者打造、设计更佳的替代方案有可能改变 Rust 项目处理时区与日历运算的方式。1.0 版本也为下游 crate 提供了一个可放心采用的稳定目标。 Jiff 集成了时区数据库（Time Zone Database），支持考虑夏令时的算术运算、带时区日期时间的格式化与解析，并提供可选的 Serde 支持；有评论者还询问了 TAI、UT1 等其他时间尺度的处理方式，文档中至少有所提及。作者坦诚地界定了库的适用范围，指出它并非适用于所有场景——包括既要求微秒级又要求百万年级精度的极端天文时间尺度。

hackernews · burntsushi · 11月16日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=50519744)

**背景**: Rust 中最广泛使用的日期时间 crate 历来是 chrono，它功能丰富，但长期因 API 容易让人在时区和夏令时上写出微妙错误而受到批评。Jiff 的作者 BurntSushi 也是 ripgrep、regex 和 csv 等广泛使用的 Rust 工具的开发者，该库旨在提供一种“顺利落入成功之坑”（pit of success）的设计，让最直观的写法同时也是正确的写法。日期时间库必须同时处理民用时间（受时区支配的日历与钟表时间）与绝对时间（单调的时刻），这正是 Jiff 采用分离类型设计的原因所在。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.rs/jiff/latest/jiff/">jiff - Rust</a></li>
<li><a href="https://www.websitehunt.co/websites/jiff-rust-datetime-library">Jiff : Rust datetime library - Website Hunt</a></li>
<li><a href="https://github.com/BurntSushi/rust-csv">GitHub - BurntSushi / rust -csv: A CSV parser for Rust , with Serde...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪非常正面：评论者称赞 Jiff 与 BurntSushi 的其他库一样优秀，并希望更广泛的生态能逐步用它取代 chrono。一位前 chrono 维护者回顾说，试图改进 chrono 的 API 总是遭遇阻力，心力交瘁最终让他离开；也有人赞赏 Jiff 坦诚划定适用范围，认为知道“不实现什么”才是关键能力。一位从事小行星轨道模拟的用户则提出了关于支持 UT1、TAI 等特殊时间尺度的技术疑问。

**标签**: `#Rust`, `#datetime`, `#libraries`, `#Jiff`, `#timezones`

---

<a id="item-5"></a>
## [阿里、腾讯、月之暗面在新模型中收紧攻击性网络能力](https://www.bloomberg.com/news/articles/2026-11-16/china-s-top-ai-firms-limit-cyber-capabilities-in-latest-models) ⭐️ 8.0/10

阿里巴巴、腾讯、月之暗面等中国头部 AI 公司在新一代模型中削弱了进攻性网络能力，同时提升了防御性表现。值得注意的是，阿里最新旗舰 Qwen 未开放权重，用户无法再下载并自行定制完整版本。 这对开放模型生态是一个重要转折，因为阿里的 Qwen 系列一直是全球应用最广泛的开源权重模型之一，也是开发者常用的微调基座。此举还表明中国主要实验室正主动让模型发布与出口管制草案保持一致，这可能会重塑中国 AI 能力在全球的流通方式。 据报道，腾讯在本月发布 Hy4 模型之前已削减了与网络攻击相关的功能；商务部上月公布的草案拟禁止出口可攻击关键基础设施或政府网络的 AI 工具。这些限制之所以重要，是因为当模型权重公开后，下游微调往往可以消除发布时所做的安全对齐。

telegram · zaihuapd · 11月17日 02:20

**背景**: Qwen 是阿里云打造的大语言模型系列，过去通常在 Hugging Face、GitHub 等平台开放发布，开发者可以自行下载、运行和微调。月之暗面（Moonshot AI）是推出 Kimi 助手的中国创业公司，以超长上下文模型著称。“开放权重”意味着训练好的参数可被公开下载，这会让模型能力广泛扩散，但也使安全限制难以真正执行。中国监管机构一直在起草针对 AI 系统的出口管制，促使各实验室限制公开版本中所包含的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>
<li><a href="https://www.tencent.com/tencent-releases-and-open-sources-tencent-hy4-preview/">Tencent Releases and Open-Sources Tencent Hy 4 preview - Tencent</a></li>
<li><a href="https://huggingface.co/tencent/Hy4-preview">tencent / Hy 4 -preview · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#export controls`, `#open weights`, `#cybersecurity`, `#China AI`

---

<a id="item-6"></a>
## [报告称 Windows 11 会收集开发者所用编程代理与开发工具的遥测数据](https://xusheng.dev/posts/windows-coding-agent-telemetry/) ⭐️ 7.0/10

xusheng.dev 上的一篇博客文章称，Windows 11 会收集开发者使用哪些编程代理（coding agent）和开发工具的遥测数据。该贴子在 Hacker News 上获得 383 个赞和 239 条评论，读者围绕“究竟收集了什么”以及“披露是否足够清晰”展开争论。 开发者的电脑上存放着源代码、凭据和内部工具，因此记录一个人运行了哪些 AI 编程代理和编辑器的遥测数据，比一般的使用统计更为敏感。这一事件也助推了更广泛的趋势：当开发者不信任 Windows 默认配置时，会更多考虑 Linux 或 macOS 等替代方案。 讨论指出，这类数据收集并非 Windows 独有：Intel、AMD 和 NVIDIA 的显卡驱动在用户未主动退出时会记录可执行文件名称和路径，浏览器配置也可能保留大量历史记录。评论者还提到，Windows 目前缺乏成熟的 AI 代理沙箱——微软的 MXC 沙箱直到 10 月 7 日才推出，且 Claude Code 尚未支持，导致许多代理只能在无沙箱环境或 WSL 中运行。

hackernews · cwaffles · 11月16日 22:58 · [社区讨论](https://news.ycombinator.com/item?id=50524736)

**背景**: Windows 遥测是微软为评估功能使用情况和安排工程优先级而收集的诊断与使用数据，注重隐私的用户常通过本地账户和第三方精简工具将其关闭。AI 编程代理并非简单的代码补全插件，而是一个会自动读取文件、编写代码、执行 shell 命令和发起网络请求的自治进程，因此通常需要在微虚拟机、gVisor 或容器等隔离沙箱中运行，而不是直接跑在宿主机上。WSL（Windows Subsystem for Linux）已成为在 Windows 上运行这类代理的常见变通方案，因为系统本身缺少原生隔离。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://northflank.com/blog/how-to-sandbox-ai-agents">How to sandbox AI agents in 2026: MicroVMs, gVisor... — Northflank</a></li>
<li><a href="https://discuss.privacyguides.net/t/best-tool-to-disable-telemetry-on-win11/18516">Best tool to disable telemetry on Win 11 - Questions - Privacy Guides...</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪褒贬不一但颇具实质：一些评论者认为显卡驱动和 Chrome 也在收集类似数据，单独指责 Windows 并不公平；另一些人则表示这正是他们打算迁移到 Linux 的原因，并指出如今大多数单机游戏在 Linux 上运行良好。一个值得注意的反方观点是，非侵入式的遥测或许是微软判断该优先开发哪些功能（尤其是代理沙箱）所必需的。

**标签**: `#privacy`, `#telemetry`, `#windows-11`, `#ai-coding-agents`, `#developer-tools`

---

<a id="item-7"></a>
## [摩根大通技术故障引发多家美国银行网上银行服务中断](https://apnews.com/article/bank-outage-chase-wells-fargo-truist-50fee2693c22f597fa6ca51a97ef2cda) ⭐️ 7.0/10

摩根大通（JPMorgan Chase）发生技术故障，导致网上银行服务出现延迟和中断，受影响范围不仅包括大通银行自身，也波及富国银行（Wells Fargo）、Truist 等其他美国主要银行。据反映，故障期间用户遇到银行卡支付失败、分行电话无人接听以及网上银行和手机银行无法使用等问题。 这起事件表明，一家机构技术栈中的单一故障就可能向外扩散并波及多家银行的服务，使客户在一个高度无现金化的经济环境中无法查看余额、转账或支付。它也加剧了外界对高度集中的云服务和共享基础设施可靠性的担忧——在那种架构下，一个单点故障会同时传导到众多依赖它的服务上。 摩根大通尚未公开确认根本原因，关于受影响客户数量及具体涉及哪些系统的细节仍然有限。有评论者指出，此次症状与以往事件相似，例如 Revolut 那次被追溯到谷歌云（Google Cloud）故障、约 12 小时后恢复的服务中断，因此本次故障更可能出在数据库或云端，而不是仍运行在大型机上的核心账务系统。

hackernews · samk3nny · 11月16日 18:31 · [社区讨论](https://news.ycombinator.com/item?id=50521045)

**背景**: 现代网上银行和手机银行依托于一个分层技术栈：面向客户的应用与 API、数据库，以及越来越多从少数几家超大规模云厂商租用的公有云基础设施。而在背后，许多大型银行仍然在几十年前诞生的大型机系统上处理账户和账务（常见的是 IBM z/OS 上的 COBOL、CICS、IMS 和 DB2），这些系统改造缓慢但极其可靠。由于头部云厂商掌控着全球基础设施的很大份额，共享组件一旦出错，故障往往会在多家机构之间级联扩散，而不会局限于某一家银行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.academia.edu/144565752/When_Clouds_Fail_Understanding_Critical_Service_Dependencies">(PDF) When Clouds Fail: Understanding Critical Service Dependencies</a></li>
<li><a href="https://www.linkedin.com/pulse/mainframe-modernization-banking-from-reliable-backbone-andreas-volz-gvfbe">Mainframe Modernization in Banking : From Reliable Backbone to...</a></li>
<li><a href="https://www.americantv.com/what-you-need-to-know-about-the-aws-outage.php">What you need to know about the AWS Outage of 10-25-2025</a></li>

</ul>
</details>

**社区讨论**: 评论者将此次事件与欧洲 Revolut 的服务中断相类比——后者被归因于谷歌云故障并在约 12 小时内修复，因此推测本次也很可能是类似的数据库或云端故障。不少人认为，在整个科技行业中，质量保障（QA）往往是最先被削减的预算项，而它的价值只有在其缺席时才被察觉；也有人指出，核心银行业务流程很可能仍运行在非常老旧但可靠的大型机上。反复出现的一个主题是公众认知：非技术用户会把这次中断与 Microsoft 365 故障、FAA 停飞事件笼统地看作同一个系统性脆弱问题，评论者认为这种担忧很难被轻易打消。

**标签**: `#banking outage`, `#system reliability`, `#cloud infrastructure`, `#QA`, `#legacy systems`

---

<a id="item-8"></a>
## [Linebender 深入解析超椭圆圆角矩形 Squircles 的数学与设计](https://linebender.org/wiki/curves/squircle/) ⭐️ 7.0/10

Linebender 发布了一篇关于 squircle（超椭圆圆角矩形）的深度 wiki 文章，系统梳理了这类用于 UI 和图形设计的形状的数学性质与设计影响。 相比传统圆角矩形，squircle 能带来更平滑的转角过渡，因此这篇分析对从事图标、界面形状和基于曲线的渲染的设计师与图形工程师具有参考价值。 文章将 squircle 视为类超椭圆形状，并将其与样条曲线和光滑曲线技术联系起来；讨论参与者还提到了 clothoid（欧拉螺线）以及三维类似物 sphube 等相关概念。

hackernews · raphlinus · 11月16日 07:55 · [社区讨论](https://news.ycombinator.com/item?id=50515151)

**背景**: Squircle 是“square”和“circle”的合成词；在设计与图形学中，它通常指由超椭圆（Lamé 曲线）导出的圆角矩形，常见的是指数为 4 的四次曲线情形。与把直边和圆弧简单拼接的圆角矩形不同，基于超椭圆的 squircle 具有不同的、连续变化的曲率分布。自 iOS 7 起 Apple 采用类似 squircle 的应用图标后，这种形状在用户界面中变得广为人知。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Squircle">Squircle - Wikipedia</a></li>
<li><a href="https://squircle.js.org/blog/what-is-a-squircle">What is a Squircle ? - Squircle .js</a></li>
<li><a href="https://mathworld.wolfram.com/Squircle.html">Squircle -- from Wolfram MathWorld</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体积极：评论者分享了 Zune 第二代方向键等真实案例，链接到样条曲线/超椭圆创作工具，并提到 sphube、clothoid 等相关概念。不少人指出，导数连续的曲线对物理交互和顺滑运动很重要，也有人单纯赞赏这篇文章是实用的设计灵感来源。

**标签**: `#squircles`, `#geometry`, `#computer-graphics`, `#UI-design`, `#curves`

---

<a id="item-9"></a>
## [博主探索用原生 Three.js 打造 3A 级光照渲染管线](https://ben3d.ca/blog/building-the-aaa-lighting-pipeline-in-threejs) ⭐️ 7.0/10

一位开发者在 ben3d.ca 上发表了一篇详细的技术深度文章，讲解如何用原生 Three.js 逼近 3A 游戏引擎级别的光照与反射质量，完整梳理了一条光照/反射管线的搭建过程，而不是依赖引擎现成功能。这篇文章在 Hacker News 上引发关注，但讨论焦点并不在技术本身，而是围绕文章是否为 AI 生成、以及为何没有附带可交互的浏览器演示展开。 对于希望缩小浏览器 3D 渲染与传统桌面游戏引擎视觉差距的 Web 图形开发者来说，这篇文章提供了有价值的参考，因为 Three.js 是 WebGL 网页 3D 领域使用最广泛的库之一。它同时折射出技术写作与图形开发的一种更广泛转变：LLM 辅助的内容与代码生成越来越多地融入工作流，也因此受到社区的公开质疑。 这篇文章是对光照与反射设置的文字讲解，而非可运行的演示，多位评论者认为这正是缺失的“回报”环节。讨论还指出，3A 大作的观感远不止渲染管线——美术方向、贴图制作与画面戏剧化处理同样关键；也有批评者认为，LLM 可以直接编写定制 WebGL 代码，无需迁就 Three.js 的架构决策。

hackernews · bhouston · 11月16日 21:07 · [社区讨论](https://news.ycombinator.com/item?id=50523291)

**背景**: Three.js 是一个开源 JavaScript 库，主要用于简化浏览器中的动画 3D 图形开发，其底层封装了 WebGL——这是一个让网页无需插件即可获得 GPU 加速 2D 与 3D 渲染能力的 JavaScript API。二者都建立在渲染管线之上，即把 3D 场景转换为屏幕上像素的一系列步骤；在 Unreal、Unity 等原生引擎中，这类管线已针对实时光照、屏幕空间反射等效果做了大量优化。要在浏览器库中复现这些效果，开发者必须手动拼装着色器、渲染目标与后处理通道，而这些在商业引擎中本是开箱即用的——这正是该博文所探讨的问题领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://threejs.org/">Three . js – JavaScript 3D Library</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebGL">WebGL</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rendering_pipeline">Rendering pipeline</a></li>

</ul>
</details>

**社区讨论**: 社区情绪褒贬不一，但整体偏向认可：有读者表示学到了东西，或认为内容与自己用 Three.js 做的副业项目相关；也有人批评文章由 AI 生成，并对缺少浏览器内可交互示例感到遗憾。一个值得注意的反驳意见认为，LLM 完全可以绕开 Three.js 直接编写针对具体项目的 WebGL 代码；还有评论强调，3A 品质不仅取决于图形管线，同样依赖美术部门的贴图制作与画面戏剧化处理。

**标签**: `#Three.js`, `#WebGL`, `#computer graphics`, `#rendering pipeline`, `#game engines`

---

<a id="item-10"></a>
## [Harmonic 的 Aristotle 形式化验证工具扩展支持 Rust](https://www.harmonic.fun/news/aristotle-rust-verification/) ⭐️ 7.0/10

Harmonic 宣布其 Aristotle 验证智能体现已支持 Rust，并声称可以形式化地证明程序不存在未定义行为——包括 unsafe 代码块内部——且代码完全符合其规格说明。此前 Aristotle 主要面向数学证明以及基于 Lean 4 证明助手的硬件验证任务。 unsafe Rust 中的未定义行为已经引发过真实的安全事件，因此一个能够以机械方式排除此类问题的工具，对内存安全的系统级编程意义重大。如果这一声明站得住脚，还将推动 AI 驱动的形式化验证从细分领域的数学与芯片设计，走向普通软件工程——而绝大多数开发者从未写过证明。 该公告并未说明其遵循的是哪一版 Rust 规范草案，而这一点很关键，因为 Rust 至今仍没有一个完整、正式批准的未定义行为定义。其声明同时涵盖“不存在未定义行为”和“完全符合用户提供的规格”，而规格本身据称是由 LLM 辅助生成，以在自然语言意图与形式化性质之间搭桥。

hackernews · maufl · 11月16日 17:34 · [社区讨论](https://news.ycombinator.com/item?id=50520270)

**背景**: 形式化验证指用数学证明而非测试来表明程序在所有可能输入下都满足某份规格说明。Rust 的安全保证由编译器强制执行，但 unsafe 代码块允许程序员做编译器无法检查的事情，从而把避免未定义行为的责任转移给开发者。Harmonic 是一家利用 Lean 4 证明助手构建可生成机器可检验证明的 AI 智能体的初创公司，于 2025 年完成了 1 亿美元融资。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.harmonic.fun/aristotle/">Aristotle : AI that formally verifies your code | Harmonic</a></li>
<li><a href="https://lab.cs.tsinghua.edu.cn/rust/std-cn/doc/reference/behavior-considered-undefined.html">Behavior considered undefined - The Rust Reference</a></li>
<li><a href="https://aiuntethered.com/news/harmonic-aristotle-formal-mathematician-agent/">Harmonic Launches Aristotle : A Free Mathematician... | AiUntethered</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者既感兴趣又持怀疑态度：多人质疑在 Rust 规范及其未定义行为定义尚未完成的情况下，如何对整个语言做验证，并认为这一领域还需一到五年才能成熟。也有人追问规格究竟如何产生——是由人类编写，还是由 LLM 从自然语言意图生成；有评论指出还没有其他系统真正尝试排除 unsafe 块内的未定义行为，另有评论则欢迎业界回归“以证明写程序”的传统。

**标签**: `#formal-verification`, `#rust`, `#undefined-behavior`, `#program-proofs`, `#LLM-assisted-specs`

---

<a id="item-11"></a>
## [Black Forest Labs 创始人谈视觉智能与 AGI](https://latent.space/p/bfl/) ⭐️ 7.0/10

Latent Space 发布了对 Black Forest Labs 的 Andreas Blattmann 和 Dustin Podell 的采访，讨论如何构建视觉智能，以及从像素、运动和声音中学习 AGI。 Black Forest Labs 是 Latent Diffusion、Stable Diffusion 和 FLUX 背后的团队，因此其创始人对视觉智能和多模态 AGI 的看法，为生成式 AI 的下一步走向提供了战略信号。 该条目将这场对话概括为探讨从像素、运动和声音中学习 AGI，但提供的摘要并未披露具体的模型版本、基准测试结果或发布日期。

rss · Latent Space · 11月16日 21:38

**背景**: Black Forest Labs 是一家由前 Stability AI 员工创立的前沿 AI 实验室，开发了 FLUX 文本生成图像模型系列，并将其使命描述为构建视觉智能的基础设施。AGI 指的是在大多数认知任务上达到或超越人类水平的假想人工智能，而多模态学习则涉及在图像、视频和音频等多种模态的组合数据上训练模型。这次采访将这些概念联系起来，探讨通用智能是否能够从丰富的感官数据中学习产生，而不仅仅依赖文本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flux_(text-to-image_model)">Flux (text-to-image model) - Wikipedia</a></li>
<li><a href="https://bfl.ai/about">About | Black Forest Labs</a></li>
<li><a href="https://www.linkedin.com/company/bflai">Black Forest Labs | LinkedIn</a></li>

</ul>
</details>

**标签**: `#generative AI`, `#computer vision`, `#Black Forest Labs`, `#AGI`, `#multimodal learning`

---

<a id="item-12"></a>
## [萨提亚·纳德拉谈 AI 让代码变便宜之后的软件工程](https://newsletter.pragmaticengineer.com/p/software-engineering-after-code-becomes) ⭐️ 7.0/10

在 Pragmatic Engineer 通讯发布的一篇访谈中，微软 CEO 萨提亚·纳德拉分享了他的观点：AI 驱动的低成本代码生成将如何重塑软件工程实践、代码验证方式以及工程师的职业路径。整场讨论围绕一个前提展开——当写代码不再是工作中昂贵且稀缺的环节时，这门学科会发生什么变化。 纳德拉掌管着最大的 AI 开发者工具供应商之一，因此他对工程精力应转向何处的判断，可能影响企业如何制定审查与信任机器生成代码的标准。对工程师个人而言，这释放出一个信号：围绕验证、系统设计与判断力的能力，可能比单纯的代码产出更重要。 目前可获取的内容仅有一句话的摘要，因此所审阅的材料中并未披露具体产品、版本或数据指标。从主题上看，这场对话聚焦于代码验证——即当生成代码变得廉价后，稀缺且昂贵的环节转变为确认生成的代码是否真正正确、是否可以安全上线。

rss · The Pragmatic Engineer · 11月16日 13:33

**背景**: 基于大语言模型的编码助手大幅降低了生成样板代码、测试乃至完整功能的成本，这就带来了一个问题：人类的工程精力应当集中在哪些环节。Pragmatic Engineer 是由 Gergely Orosz 撰写的广受关注的软件工程通讯，以面向实践者的行业趋势与工程职业分析著称。纳德拉的言论处于一场更广泛的行业争论之中：AI 究竟是在增强工程师，还是在重构整个职业。

**标签**: `#AI`, `#software-engineering`, `#career`, `#code-verification`, `#industry-trends`

---

<a id="item-13"></a>
## [OpenAI 将计算机使用智能体引入医疗团队](https://openai.com/index/advancing-computer-use-for-healthcare-teams) ⭐️ 7.0/10

OpenAI 宣布，面向医疗的计算机使用智能体现已在 ChatGPT for Healthcare、ChatGPT for Clinicians 和 OpenAI API 中可用。该公司还发布了面向医疗机构、临床医生和开发者的入门指南。 医疗工作流常常涉及缺乏标准 API 的遗留软件和网页门户，因此能够操作图形界面的智能体有望自动完成重复性行政工作。但临床使用要求严格的人工监督、隐私保护和可靠性，因为错误可能带来严重后果。 OpenAI 引导医疗机构、临床医生和开发者使用 ChatGPT for Healthcare、ChatGPT for Clinicians 和 OpenAI API，其在 GitHub 上的 openai-cua-sample-app 则展示了使用 Responses API 构建计算机使用模式的示例。现有摘要未包含基准测试结果或详细的安全评估，因此真实世界表现和风险控制仍不明确。

rss · OpenAI News · 11月16日 06:00

**背景**: 计算机使用智能体是一类通过图形界面操作软件的 AI 系统：它们读取屏幕截图、移动鼠标、点击按钮并输入文字，而不只是依赖 API 或代码集成。这使它们可能适用于遗留系统或仅有图形界面的系统，但也意味着故障可能发生在界面操作层面。OpenAI 的医疗公告将这一通用的计算机使用模式扩展到了医疗专用产品和开发者工具中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/advancing-computer-use-for-healthcare-teams/">Advancing computer - use agents for healthcare teams | OpenAI</a></li>
<li><a href="https://openai.com/index/more-ways-to-move-care-forward-with-chatgpt-for-healthcare/">More ways to move care forward with ChatGPT for Healthcare | OpenAI</a></li>
<li><a href="https://github.com/openai/openai-cua-sample-app">GitHub - openai / openai -cua-sample-app: Learn how to use CUA...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#healthcare`, `#computer-use`, `#OpenAI`, `#automation`

---

<a id="item-14"></a>
## [Maxwell-V1.0-Flash：35B 总参数 MoE 模型，支持 256K 上下文与学习式块稀疏注意力](https://www.reddit.com/r/LocalLLaMA/comments/1xyamk6/maxwellmodelmaxwellv1flash_hugging_face/) ⭐️ 7.0/10

Maxwell 团队在 Hugging Face 上发布了 Maxwell-V1.0-Flash，这是一个混合专家（MoE）语言模型，总参数 35B、每 token 仅激活 3B 参数（均不含嵌入层），支持最长 256K token 的上下文。该模型引入了带学习式块索引器的 Maxwell 块稀疏注意力（MBSA）、流形约束超连接（manifold-constrained hyper-connections）以及细粒度 MoE 主干，预训练使用约 26T token。 长上下文推理的开销通常主要由注意力机制主导，而该设计将每个 KV 组的主注意力限制在 4,096 token、同时保留完整 KV 缓存，有望让 256K token 的推理在仅激活 3B 参数的预算下变得可行。如果其宣称的 6.7 倍内核加速能够成立，这对追求低成本长上下文部署的本地与自托管 LLM 社区具有直接意义。 每个 KV 组保留 8 个固定的前缀块、8 个本地块（每块 128 token），以及最多 16 个由学习式索引器选出的远端块；块稀疏注意力是在 128K 中训练阶段、索引器已针对稠密全历史注意力完成预热之后才启用的。模型还对大多数隐藏权重矩阵使用 Muon 优化器，配备面向泰语、老挝语、缅甸语、高棉语和掸语等低资源东南亚语言优化的脚本感知多语言分词器，并采用两阶段 SFT 加多教师在线策略蒸馏的训练流程。

reddit · r/LocalLLaMA · /u/pmttyji · 11月17日 04:04

**背景**: 混合专家（MoE）模型用许多更小的专家网络替代单个稠密前馈网络，每个 token 只被路由到其中少数几个专家，因此总参数量可以很大，而单 token 计算量保持较小——DBRX 就是这类设计，总参数 132B 但每 token 仅激活 36B。稀疏注意力针对的是另一个瓶颈：模型不再对全部历史 token 做注意力，而是用轻量级学习式索引器挑选少量相关的 KV 块，只在这些块上执行精确注意力，MiniMax 稀疏注意力与 DeepSeek 的原生稀疏注意力（NSA）也采用了类似思路。超连接（hyper-connections）通过维护多条残差流并用学习到的混合方式进行推广化残差连接，而流形约束版本则把这种混合限制在结构化流形上，以在极深网络中保持稳定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://andlukyane.com/blog/paper-review-minimax-sparse-attention">MiniMax Sparse Attention : Per-Group Block Selection for Cheap...</a></li>
<li><a href="https://www.databricks.com/blog/accelerated-dbrx-inference-mosaic-ai-model-serving">Accelerated DBRX Inference on Databricks Model ... | Databricks Blog</a></li>
<li><a href="https://prathamp.com/blog/manifold-constrained-hyper-connections/">Manifold - Constrained Hyper - Connections ... | Pratham Patel</a></li>

</ul>
</details>

**标签**: `#mixture-of-experts`, `#long-context`, `#sparse-attention`, `#LLM-architecture`, `#local-llm`

---

<a id="item-15"></a>
## [Hugging Face 将语言模型推理路由切换至 OpenRouter](https://www.reddit.com/r/LocalLLaMA/comments/1xy9o6j/hugging_face_switched_its_language_model/) ⭐️ 7.0/10

Hugging Face 于 2026 年 11 月 16 日宣布，通过 Inference Providers 发出的语言模型请求不再走自家路由器，而是改由 OpenRouter 处理：OpenRouter 会依据实时价格、速度和可靠性为每次调用挑选供应商，失败时自动重试到另一家供应商。原有的 Hugging Face token 仍然有效，且官方称不额外加价；用户依然可以通过模型 ID 后缀（如 :fastest、:cheapest 或具体供应商名称）指定路由策略。 Hugging Face 是开放模型生态的核心枢纽，把语言模型推理路由交给第三方网关是一次颇具分量的架构与竞争格局转变，会影响到所有依赖 Inference Providers 的开发者。这也凸显了开放权重模型在 OpenRouter 上的主导地位：其 token 占比从 2025 年 10 月的 26.8% 升至 2026 年 9 月底的 71.7%，而平均成本仅为闭源模型的四分之一左右。 自动故障转移可以说是最有价值的部分，因为长时间任务往往就是被单个供应商的一次故障毁掉。但这同时是一处破坏性变更：自定义的供应商 API key 不再适用于语言模型请求，相关费用改由 Hugging Face 账户结算；而图像、视频和音频生成仍走 Hugging Face 原有的 Inference Providers 通道，不经过 OpenRouter。

reddit · r/LocalLLaMA · /u/jomic01 · 11月17日 03:16

**背景**: Hugging Face Inference Providers 让开发者用一个 Hugging Face token 就能调用 Cerebras、Groq、Together、Fireworks、DeepInfra 等合作方托管的模型，由 Hugging Face 的代理层统一处理认证与计费。OpenRouter 则是一个托管网关，用一套兼容 OpenAI 的 API 对接数十家供应商的数百个模型，并依据实测的价格、吞吐、延迟和可靠性对它们排序。把模型请求路由到当前最便宜或最快的可用供应商，并在某家宕机时自动回退，正是这类服务在裸推理之外提供的核心价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/docs/inference-providers/index">Inference Providers · Hugging Face</a></li>
<li><a href="https://openrouter.ai/docs/guides/routing/provider-selection">Provider Routing - Smart Multi- Provider Request Management</a></li>
<li><a href="https://sentiogate.app/vs/openrouter-vs-hugging-face">OpenRouter vs Hugging Face Inference (2026) | SentioGate</a></li>

</ul>
</details>

**标签**: `#llm-inference`, `#hugging-face`, `#openrouter`, `#model-routing`, `#open-weight-models`

---

<a id="item-16"></a>
## [美商务部将定稿新规，封堵经东南亚远程使用 AI 芯片的漏洞](https://t.me/zaihuapd/45161) ⭐️ 7.0/10

美国商务部正在敲定一项规则，最早可能于本月公布，将阻止中国 AI 公司通过位于中国境外的数据中心远程使用先进 AI 芯片。该规则把现有的半导体出口限制扩展到马来西亚、新加坡、泰国等七个国家，以封堵远程访问和芯片走私的漏洞，商务部正与其他政府机构磋商后定稿。 这封堵了美国出口管制体系中最明显的剩余绕道之一，意味着中国 AI 实验室不能再简单地通过在第三国租用算力、用受限硬件训练前沿模型。此举将重塑全球 AI 基础设施与云算力布局，并迫使东南亚及其他地区的 datacenter 运营商和云服务商审查其客户的最终使用方。 据报道，该规则将要求新加坡、马来西亚、泰国、印度尼西亚和巴西等国的数据中心运营商，在向总部位于中国、俄罗斯、伊朗等高风险国家的企业提供大规模算力时须获得美国许可证。据称英伟达曾游说反对封堵这一远程访问缺口，理由是美国的 AI 基础设施需要在全球取胜；白宫此前也已要求国会立法，以便商务部制定该规则。

telegram · zaihuapd · 11月16日 14:44

**背景**: 美国出口管制禁止中国实体直接购买英伟达 H100、B200 等先进 AI 加速卡，这类芯片通常按总处理性能和内存带宽阈值来界定。一个被广泛指出的漏洞是：中国企业可以在新加坡或马来西亚的数据中心租用算力，远程使用受限芯片，而芯片本身从未进入中国境内。拜登政府的“AI 扩散”框架曾试图管理这种全球算力访问，但遭到批评并正被现政府重新修订，此次规则就是这一进程的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-16/us-moves-to-limit-remote-access-to-advanced-ai-chips">US Moves to Curb China’s Remote Access to Nvidia’s AI Chips</a></li>
<li><a href="https://www.nytimes.com/2026/11/16/us/politics/trump-china-ai-chip-loophole.html">Trump Administration Moves to Close A . I . Chip Loophole Ahead of...</a></li>
<li><a href="https://www.scmp.com/news/asia/southeast-asia/article/3317232/worried-about-china-us-takes-aim-malaysia-thailand-new-ai-chip-crackdown">Worried about China, US takes aim at Malaysia , Thailand in new AI ...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#Nvidia`, `#geopolitics`, `#Southeast Asia`

---

<a id="item-17"></a>
## [丘成桐牵头成立数学与 AI 实验室联盟](https://t.me/zaihuapd/45172) ⭐️ 7.0/10

10 月 11 日，菲尔兹奖得主、清华大学讲席教授丘成桐在清华大学牵头成立丘成桐数学与人工智能实验室联盟，汇集超过 1000 名科学家，旨在自主研发中国数学专用大模型。 该联盟标志着中国在“AI for Science”方向上的重要机构化布局，意在建设专门的数学 AI 基础设施，有望加速定理证明、数学发现以及量子计算、生命科学等交叉领域的研究。 联盟将重点研发数学专用模型、建设 AI 辅助数学研究基础设施，并计划拓展至量子计算、生命科学、金融经济等交叉领域；丘成桐称 AI 对数学的冲击“像海啸来了”，应主动冲浪而非回避。此次公布未披露模型参数、技术路线图或时间表。

telegram · zaihuapd · 11月17日 04:00

**背景**: 菲尔兹奖被广泛视为数学领域的最高荣誉，清华大学则是中国顶尖研究型大学之一。数学专用大模型通常基于数学语料和基准进行训练或微调，例如阿里巴巴的 Qwen2-Math 和 Qwen2.5-Math 系列；AI 辅助数学研究则越来越多地涉及定理证明、猜想探索以及人机协作验证流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen2-Math-1.5B-Instruct">Qwen/Qwen2- Math -1.5B-Instruct · Hugging Face</a></li>
<li><a href="https://github.com/QwenLM/Qwen2.5-Math">QwenLM/Qwen2.5-Math: A series of math - specific large language ...</a></li>
<li><a href="https://arxiv.org/pdf/2604.11504">Lectures on AI for Mathematics</a></li>

</ul>
</details>

**标签**: `#AI for Mathematics`, `#Large Language Models`, `#Research Alliance`, `#China`, `#AI for Science`

---