---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 63 条内容中筛选出 11 条重要资讯。

---

1. [Nolan Lawson 追问：开发者为何不愿「使用平台」原生 API](#item-1) ⭐️ 8.0/10
2. [SK 电信就大规模信息泄露致歉，为全体用户免费更换 USIM 卡](#item-2) ⭐️ 8.0/10
3. [Google 发布 VeriHarness：面向长程任务的自验证框架](#item-3) ⭐️ 8.0/10
4. [Strata 在单张 RTX 4090 上运行 125B Qwen3.8-Flash-Next](#item-4) ⭐️ 7.0/10
5. [RemoveMacAI 脚本可从 macOS 27 中移除 Apple Intelligence 以回收磁盘空间](#item-5) ⭐️ 7.0/10
6. [脱敏失败曝光谷歌数据中心用水与用电数据](#item-6) ⭐️ 7.0/10
7. [从单张 RTX 3090 到 20 台 DGX Spark：一位玩家的本地推理扩容史](#item-7) ⭐️ 7.0/10
8. [爱好者用廉价退役矿机 FPGA 卡跑通 Qwen3.5 9B/27B INT4 推理](#item-8) ⭐️ 7.0/10
9. [双 DGX Spark 上 GLM 5.3 Flash 新配方解码提速 50%–90%](#item-9) ⭐️ 7.0/10
10. [开发者仅用 865 亿 token 从零训练出 3.87B MoE 模型](#item-10) ⭐️ 7.0/10
11. [天津大学发布 3 克无创脑机一体化系统](#item-11) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Nolan Lawson 追问：开发者为何不愿「使用平台」原生 API](https://nolanlawson.com/2026/10/03/why-dont-more-developers-use-the-platform/) ⭐️ 8.0/10

Nolan Lawson 发表了题为《Why don't more developers "use the platform"?》的博客文章，探讨原生 Web 平台 API（如 Web Components）与 React 等 JavaScript 框架之间长期存在的张力。文章指出，把框架流行简单归结为「更好玩」的说法，忽视了原生平台 API 本身可能既繁琐又不可靠的事实；该文引发了热烈讨论，获得 278 分和 288 条评论。 这场争论之所以重要，是因为它牵涉到几乎所有前端开发者日常的工具选择，也影响浏览器厂商如何权衡标准工作与框架生态开箱即用的能力。如果原生 API 被认为难用，标准倡导者就会在与框架的竞争中处于下风，从而影响开放 Web 平台的长期健康，以及实际上线应用的无障碍性与性能。 评论者强烈质疑「浏览器原生实现更快更好」这一前提，并以 HTML 的 <datalist> 元素为例：它在大多数浏览器中的实现糟糕到几乎不可用。也有人指出，Web Components 若没有 Lit 之类的封装库就几乎无人直接使用，说明原生的自定义元素与 Shadow DOM API 单独使用时相当别扭。

hackernews · vinhnx · 10月4日 04:10 · [社区讨论](https://news.ycombinator.com/item?id=49950554)

**背景**: Web Components 是一套 Web 平台标准，包括自定义元素（custom elements）、Shadow DOM 和 HTML 模板，允许开发者直接在浏览器中定义可复用、样式与结构封装的 HTML 元素。而「使用平台」（use the platform）是 Web 标准、性能与无障碍倡导者长期以来的口号，呼吁开发者优先使用浏览器内建能力，而非框架抽象。React 等框架之所以占据主导，部分原因是它们在原生组件模型成熟之前就提供了统一、一致的组件开发方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nolanlawson.com/2026/10/03/why-dont-more-developers-use-the-platform/">Why don’t more developers “ use the platform ”? | Read the Tea Leaves</a></li>
<li><a href="https://en.wikipedia.org/wiki/Web_Components">Web Components</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/Web_components">Web Components - Web APIs | MDN - MDN Web Docs</a></li>

</ul>
</details>

**社区讨论**: 整体情绪对文章的论述持怀疑态度：多位评论者认为 Web Components 本身就是一套设计糟糕、难以上手的 API，而 React 则是设计相对良好、也并不臃肿的库。另一些人坚称「浏览器原生更快更好」这一前提很少成立，并以几乎不可用的 <datalist> 元素为证；还有一位从通用编程视角出发的评论者指出，Web 开发反常地缺乏其他领域那种小而可组合的抽象。

**标签**: `#web development`, `#web components`, `#javascript frameworks`, `#platform APIs`, `#browser standards`

---

<a id="item-2"></a>
## [SK 电信就大规模信息泄露致歉，为全体用户免费更换 USIM 卡](https://t.me/zaihuapd/44206) ⭐️ 8.0/10

韩国最大电信运营商 SK Telecom（SKT）确认其内部系统遭黑客攻击，核心 HSS 服务器被攻破，超过 2500 万用户的 IMEI、序列号、ICCID、PIN2/PUK2、eID、加密 K 值和私钥等敏感数据被泄露。SKT CEO 已公开致歉，并宣布为所有希望更换的 SKT 用户（含其网络下的 MVNO 用户，部分设备除外）免费更换 USIM 卡，并报销近期已付费更换的用户。 这是迄今披露的规模最大的电信安全事件之一，波及韩国约一半人口，并泄露了支撑 SIM 卡身份认证的密码学材料，可能带来 SIM 卡克隆、身份盗用和账户接管等风险。这也迫使全球运营商重新审视用户密钥的存储方式，以及在核心网被攻破后快速轮换 SIM 凭证的能力。 泄露数据包括长期认证密钥（K 值）、私钥、eID 以及 PIN2/PUK2 码，这些材料存放在 HSS 中，与泄露的密码不同，用户无法自行更改，正常情况下应受 SIM 卡安全芯片保护。免费更换 USIM 卡（部分设备除外）实质上是一种凭证轮换措施，因为换发新卡会生成全新的密钥；据称该攻击在最初发生一段时间后才被公开披露。

telegram · zaihuapd · 10月4日 09:02

**背景**: HSS（Home Subscriber Server，归属用户服务器）是 LTE/5G 核心网中的主用户数据库，存储每个用户的 IMSI、认证密钥和签约信息，网络通过查询它来验证 SIM 卡并跟踪用户位置。每张 SIM/USIM 卡由 ICCID 序列号唯一标识，并内置一个密钥（K/Ki），运营商侧也保存有对应副本；网络正是通过两者匹配来完成对卡的认证。因此一旦卡与运营商侧的密钥同时泄露，攻击者就有可能冒充用户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/learning/telecom-network-evolution-2g-to-6g-technologies-architecture-and-key-concepts/4g-home-subscriber-server-hss">4G home subscriber server ( HSS ) - Telecom Network Evolution...</a></li>
<li><a href="https://telnyx.com/resources/iccid-number">ICCID number: how to find, decode, and use it</a></li>
<li><a href="https://reverseengineering.stackexchange.com/questions/15011/how-does-a-sim-card-work">firmware - How does a SIM card work? - Reverse Engineering Stack...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#data-breach`, `#telecom`, `#SK Telecom`, `#privacy`

---

<a id="item-3"></a>
## [Google 发布 VeriHarness：面向长程任务的自验证框架](https://arxiv.org/abs/2610.00972v1) ⭐️ 8.0/10

Google 研究团队发布了 VeriHarness——一个验证框架：给定一个任务和同一智能体独立生成的 N 条 rollout，它用生成这些 rollout 的同一个模型对照任务环境进行核查，并产出一个经过修订或重建的最终结果。该工作在 5 个长程任务基准、2 个模型上取得最高选择分；在证据驱动修订后，相较单次生成平均提升 Gemini 3.5 Flash 6.2 分、Claude Opus 4.8 6.4 分，同时公开了约 2.6 万条 rollouts。 长程任务是当前大模型智能体最容易失败的环节，而 VeriHarness 把“验证”做成可扩展、可自我改进的一层能力，无需另训一个专用验证模型，因此有望显著提升智能体的可靠性。由于它复用同一模型并公开了 rollout 数据，该方法对构建或评测多步智能体系统的开发者都具有直接参考价值。 该框架区分两类主张：对分歧主张核查环境证据，对共识主张则主动发起挑战，据此选择、修订或重建最终结果，并为每一处改动保留证据记录。论文还指出验证能力可以从失败反馈中自我改进，说明这一验证循环本身具备可扩展性。

telegram · zaihuapd · 10月4日 13:32

**背景**: 长程任务指的是需要大量相互依赖步骤、往往持续数小时才能完成的智能体任务，而非单轮推理，前沿大模型往往随着任务变长而性能下降。这里的 rollout 指智能体在同一任务上独立采样出的一条执行轨迹，因此生成 N 条 rollout 就为验证框架提供了多个可比较的候选结果。VeriHarness 遵循“自验证”思路，即让产出候选结果的模型自己去判断并修复结果，本质上是为每个任务投入更多推理期算力，而不是依赖一个独立的批评模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/google-research/veriharness">GitHub - google-research/veriharness</a></li>
<li><a href="https://arxiv.org/abs/2610.00972">[2610.00972] VeriHarness: Scaling Agentic Verification for ...</a></li>
<li><a href="https://github.com/acensia/long-horizon-papers">GitHub - acensia/long-horizon-papers: 2026 papers on long ...</a></li>

</ul>
</details>

**标签**: `#LLM verification`, `#long-horizon tasks`, `#AI agents`, `#Google Research`, `#benchmark`

---

<a id="item-4"></a>
## [Strata 在单张 RTX 4090 上运行 125B Qwen3.8-Flash-Next](https://github.com/Niko1221/Strata) ⭐️ 7.0/10

一个名为 Strata（v0.1.38）的开源推理引擎声称，通过将模型分散到 GPU、CPU、内存和 SSD 上，可以在单张 RTX 4090 上以约 100+ token/秒的速度运行 125B 参数的 Qwen3.8-Flash-Next 模型。社区用户报告在 4090 上达到约 124 token/秒，而该项目所谓「比 llama.cpp 快 6 倍」的核心宣传，在其他评测中被认为在同等条件下更接近 2 倍。 在消费级硬件上高速运行 125B 级模型降低了本地 LLM 部署的门槛，这对注重隐私、离线或预算受限的工作流来说意义重大。不过相互矛盾的基准测试结果表明，激进的 4-bit 以下量化可能以显著牺牲输出质量为代价换取速度，因此这些亮眼数字值得审慎对待。 Qwen3.8-Flash-Next 总参数量为 125B，但每个 token 仅激活 6B 参数，另有 51B 的 N-gram 嵌入和 4B 的 MTP；其隐藏维度为 2560。一位独立测试者发现，Strata 的视觉输出中位误差为 154.8 像素，而同一 GGUF 与视觉适配器在 llama.cpp 上仅为 46.5 像素，这引发了对 Strata 所依赖的低比特量化导致质量下降的担忧。

hackernews · snehesht · 10月4日 12:51 · [社区讨论](https://news.ycombinator.com/item?id=49953495)

**背景**: 大语言模型的参数量通常在数百亿甚至上千亿级别，远超 RTX 4090 这类消费级 GPU 的显存容量。量化技术通过以更低精度（如 4-bit 或更低）存储权重来缩小模型以便装进有限内存，而混合专家（MoE）与卸载（offloading）等技术则把未激活的部分分散到 CPU、内存和 SSD。Strata 更应被理解为专为 Qwen3.8-Flash-Next 定制的运行时，而非通用推理引擎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-Flash-Next">Qwen / Qwen 3 . 8 - Flash - Next · Hugging Face</a></li>
<li><a href="https://www.linuxcompatible.org/story/strata-v0138-runs-a-125billionmodel-llm-on-any-gaming-pc/">Strata v0.1.38 Runs a 125-Billion-Model LLM on Any Gaming PC</a></li>
<li><a href="https://www.youtube.com/watch?v=m0VHx73SAG0">The New Way to Run 125 B Models 6× Faster Than... - YouTube</a></li>

</ul>
</details>

**社区讨论**: 社区情绪谨慎乐观但存疑：用户确认吞吐量很强（4090 上 124 token/秒），但多人质疑 4-bit 以下量化是否会造成明显的质量损失。一位评论者的 50 张图像视觉测试显示，Strata 的误差约为运行相同权重的 llama.cpp 的三倍；也有人指出在 RTX Pro 6000（约每小时 1 美元）上用 4-bit 量化已能满足困难的编程任务质量，还有人认为铺天盖地的 Strata 链接属于过度炒作。

**标签**: `#llm-inference`, `#quantization`, `#consumer-gpu`, `#local-llm`, `#qwen`

---

<a id="item-5"></a>
## [RemoveMacAI 脚本可从 macOS 27 中移除 Apple Intelligence 以回收磁盘空间](https://github.com/omlahore/RemoveMacAI) ⭐️ 7.0/10

GitHub 上的 RemoveMacAI 项目提供了一款脚本，用于从 macOS 27（“Golden Gate”）中删除 Apple Intelligence 相关组件，让用户回收这些本地 AI 模型与资源所占用的磁盘空间。该工具被发布到 Hacker News 后引发热议，帖子获得约 360 分、222 条评论。 这凸显了苹果大力推广设备端 AI 与用户希望掌控存储、系统资源和隐私之间的矛盾，尤其是在 macOS 27 高度依赖 Apple Intelligence 和 Siri 的背景下。这样一款第三方移除脚本受到欢迎，说明用户对苹果尚未提供的官方“退出”选项存在真实需求。 macOS 上的 Apple Intelligence 仅支持 Apple 芯片（M1 及以上）的 Mac，因此可回收的空间只适用于这些机型；与其它“去臃肿”脚本一样，用户应预期在系统更新后需要重新运行，并且它可能影响依赖被删除模型的某些功能。讨论中还提到，这些本地模型体积相对较小且不依赖云端运行，因此部分用户认为它们是优点而非臃肿。

hackernews · privacyisntdead · 10月4日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=49957116)

**背景**: Apple Intelligence 是苹果于 2024 年 6 月 10 日 WWDC 上发布的一套 AI 功能，作为 iOS 18、iPadOS 18 和 macOS Sequoia 的内置特性提供；它对支持的设备免费，包含写作工具、图像生成、通知摘要、照片修图以及与 ChatGPT 的集成。macOS 27 代号“Golden Gate”，是 macOS 的第 23 个主要版本，于 2026 年 6 月 8 日的 WWDC 2026 上发布、2026 年 9 月 14 日正式推出；它是首个仅支持 Apple 芯片 Mac 的 macOS 版本，也是最后一个保留完整 Rosetta 2 功能的版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://en.wikipedia.org/wiki/MacOS_27">MacOS 27</a></li>

</ul>
</details>

**社区讨论**: 评论者把这一情况比作 Windows 上长期需要的“去臃肿”脚本，有人称其相当于 O&O ShutUp10 那个级别，并质疑苹果的产品策略。也有人抱怨 iOS 连一个简单的 AI 开关都没有，而微软和 Firefox 已转向提供全局 AI 开关；一位用户则为苹果辩护，认为这些本地推理模型体积小、不依赖云端，足以应付基本任务；还有人回顾 15 年前动辄数 GB 的打印机驱动，好奇苹果究竟如何权衡磁盘占用成本与用户不满。

**标签**: `#macOS`, `#privacy`, `#Apple Intelligence`, `#bloatware-removal`, `#AI-opt-out`

---

<a id="item-6"></a>
## [脱敏失败曝光谷歌数据中心用水与用电数据](https://www.1011now.com/2026/09/30/more-questions-than-answers-about-lincolns-google-data-center-water-electricity-usage/) ⭐️ 7.0/10

一份本应经过脱敏处理的文件泄露了谷歌位于内布拉斯加州林肯市数据中心的水电消耗数据，其中林肯数据中心的用水量据报道约为 1300 万加仑。这些数字之所以公开，是因为脱敏操作不当，底层文字仍可被还原读取。 数据中心的用水与用电量正是 AI 基础设施扩张争议的核心，但这类数据通常被保密的水电协议覆盖，因此这次泄露让当地居民和监管者获得了平时无法看到的真实数字。它也进一步推动了关于 AI 基础设施环境成本是否被如实披露的更广泛争论。 此次泄露源于典型的 PDF 脱敏失败：用黑框或与背景同色的文字在视觉上遮盖信息，却没有真正删除内容，导致数据仍可被提取。评论者还提醒，这类报道常常把数据中心获批或签约可抽取的最大水量与其日常实际消耗混为一谈，并指出林肯数据中心约 1300 万加仑的用水量，相比另一座被提及超过 5 亿加仑的数据中心要小得多。

hackernews · sensanaty · 10月4日 19:37 · [社区讨论](https://news.ycombinator.com/item?id=49957068)

**背景**: 数据中心用水主要用于蒸发冷却，用电则同时用于计算设备和冷却等配套开销；业界用“水利用效率”（WUE）和“电能利用效率”（PUE）等指标来衡量，两者均由行业联盟 The Green Grid 提出，数值越低代表效率越高。由于与市政部门签订的水电合同往往以保密方式谈判，公众通常只能依靠企业自愿披露或泄露信息来了解真实消耗。PDF 脱敏失败是一个长期存在且反复出现的问题，记者们多次从遮盖层并未真正生效的文件中提取出敏感信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Water_usage_effectiveness">Water usage effectiveness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Power_usage_effectiveness">Power usage effectiveness - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Improper_PDF_Redaction">Improper PDF Redaction — Grokipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多对报道的框架提出质疑：有人指出 1300 万加仑在具体语境下根本算不上有意义的用水量，并称赞作者花时间做了量化换算。另有人主张，用水和用电只是真正诉求之上的“抽象层”，因为一旦聚焦于此，就容易被人用“实际消耗相对较小”的数据反驳——真正该争论的是我们到底要不要 AI 和数据中心。有行业经验的人补充了细节：一位评论者描述了谷歌数据中心附近居民提出的离谱指控以及员工无法反驳的处境，还有一位提醒人们常把许可水量误当作实际日消耗量。

**标签**: `#data-centers`, `#ai-environmental-impact`, `#google`, `#water-usage`, `#energy-consumption`

---

<a id="item-7"></a>
## [从单张 RTX 3090 到 20 台 DGX Spark：一位玩家的本地推理扩容史](https://www.reddit.com/r/LocalLLaMA/comments/1wxgm0h/from_1x3090_to_20_dgx_sparks_my_house_fuses_were/) ⭐️ 7.0/10

LocalLLaMA 用户 u/ciprianveg 记录了自己多年来家庭 LLM 推理设备的升级历程：最初用单张 RTX 3090 跑 LLaMA 33B/65B，后来搭起基于 100 Gbit 网络的 16x3090 集群，最终转向多组 8x ASUS GB10（DGX Spark 级别）集群，并与住在五分钟路程外的兄弟共享算力。据其自述，他已在 NVIDIA 论坛发布了首个 8x Spark 上的 MiMo 2.5 Pro 与 Kimi 2.6 可用方案，以及首个 16x Spark 上的 Kimi K3 方案，并即将再添四台 Spark，预计 10 月 2 日到货。 这是一份少见的端到端实践报告，说明开源权重的前沿级模型推理如今在家庭环境中已具备可行性，同时也表明随着集群扩大，瓶颈会从显存转移到供电容量、散热、网络与软件调优上。它还展示了在日常专业编程工作中替代商业 API 订阅的一种具体路径，而这正是本地 AI 与 homelab 社区的核心主张。 16x3090 方案采用基于 P620 的节点并通过 100 Gbit 网络互联，但功耗约 6 kW，一旦与电烤箱同时运行就会烧断家中保险丝，且 397B 级模型在该平台上也仅有 50-60 t/s；相比之下，4x GB10 仅用约 400 W 就能让 397B 跑到 30 t/s，被形容为稳定得惊人且几乎无声。改用 8x Spark 后，397B 还能从 INT4 切换到 FP8 运行并提升约 20% 速度；经过多轮迭代，Kimi K3（2.8T）据称从 100k 上下文下不可用的 7 t/s 提升到 300k 上下文下可用的 20 t/s。

reddit · r/LocalLLaMA · /u/ciprianveg · 10月4日 14:09

**背景**: DGX Spark 是 NVIDIA 基于 GB10 Grace Blackwell 平台打造的紧凑型个人 AI 计算机，将 Arm CPU、Blackwell GPU 与统一内存组合在一起；文中提到的 ASUS GB10 属于同一类设备。官方仅认证两台设备直连互连，超过两台的规模就需要用户自建高速网络多节点集群，而这正是作者自称填补的空缺——他发布了可用的配置方案。文中涉及的模型多为混合专家（MoE）架构，每个 token 只激活一小部分参数，这种稀疏性使 671B 甚至 2.8T 的模型能在有限硬件上运行，但把专家卸载到系统内存后速度会明显下降；也正因为如此，随着上下文变长，prefill（处理提示词）与 decode（逐 token 生成）的表现会有很大差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/NVIDIA_DGX_Spark">NVIDIA DGX Spark</a></li>
<li><a href="https://www.nvidia.com/en-us/products/workstations/dgx-spark/">Personal AI Supercomputer Powered by Blackwell | NVIDIA DGX Spark</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>

</ul>
</details>

**标签**: `#LocalLLaMA`, `#LLM inference`, `#homelab`, `#GPU clustering`, `#AI hardware`

---

<a id="item-8"></a>
## [爱好者用廉价退役矿机 FPGA 卡跑通 Qwen3.5 9B/27B INT4 推理](https://www.reddit.com/r/LocalLLaMA/comments/1wxken1/qwen35_arch_implementation_in_fpga_fabric_for/) ⭐️ 7.0/10

一位爱好者发布了以 MIT 许可开源的 VHDL 推理引擎（llm.vhdl），在两块二手 SQRL FK33 矿机 FPGA 卡（每块约 280 美元、配备 8GB HBM2、带宽约 400GB/s）上跑通了 Qwen3.5 级别的 9B INT4 推理。在 75MHz 的 FPGA 时钟下，双卡流水线可达到约 6 tok/s 的 prefill 和会话初期约 3.2 tok/s 的生成速度（2-3k 上下文时约 2.4 tok/s），输出结果与 llama.cpp 逐层比对验证。 它说明被淘汰的加密货币矿机 FPGA 板卡可以成为真正廉价的本地推理加速方案，而在当前 GPU 显存价格主导本地 LLM 成本结构的背景下，这一点尤其有吸引力。帖子还给出了 ASIC 外推：在 2GHz 时钟的现代工艺节点上，27B 模型在短上下文下约可达 294 tok/s，功耗仅 125-340W，暗示相比通用 GPU 仍有大量性能空间。 实际跑通的只有 9B INT4；所有 27B 的数据（单块 Jungle Cat 在 75MHz 下约 2 tok/s prefill、1.1 tok/s 生成，四颗 die 在 200MHz 下可扩展到约 25 tok/s）都是基于 9B 实测的逐算子性能画像推算出来的。作者指出，更高时钟需要更多 RTL 优化和更高的核心电压；Jungle Cat Lite 板卡在不做 PCB 改造的情况下无法快速加载权重，且缺少 GTY 通道的时钟生成（只需补焊少量元件即可解决）；此外两块 die 最多只能支撑约 45k 上下文，因为 27B 的 KV cache 无法与 14.5GB 权重共存。

reddit · r/LocalLLaMA · /u/I_am_purrfect · 10月4日 16:51

**背景**: FPGA（现场可编程门阵列）是一种出厂后仍可重新配置逻辑的芯片，作为神经网络推理载体灵活但传统上较慢；SQRL FK33 是采用 Xilinx Virtex UltraScale+ VU33P 的板卡，配备 8GB HBM2 高带宽显存，原本用于加密货币挖矿，如今以几百美元的价格在 eBay 上甩卖。Qwen3.5 是阿里巴巴的原生多模态模型系列，采用 3:1 的混合注意力结构——每三个 Gated DeltaNet（线性注意力）层搭配一个完整的 Gated Attention 层，以控制长上下文和视觉 token 的开销。INT4 量化把模型权重存为 4 位整数而非 16 位浮点数，可将显存占用压缩约 4 倍（代价是一定精度损失），这正是让 9B-27B 模型塞进几 GB 的 FPGA 板载显存的前提。llama.cpp 则是作者用来做对照验证的常用 C/C++ 推理引擎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/docs/transformers/model_doc/qwen3_5">Qwen3.5 · Hugging Face</a></li>
<li><a href="https://apxml.com/courses/quantized-llm-deployment/chapter-1-advanced-llm-quantization-fundamentals/low-bit-quantization-techniques">Low-Bit LLM Quantization ( INT 4 , NF4, FP4)</a></li>
<li><a href="https://github.com/d953i/SQRL_FK33">GitHub - d953i/SQRL_FK33: SQRL FK33 board files, example ...</a></li>

</ul>
</details>

**标签**: `#FPGA`, `#LLM inference`, `#quantization`, `#hardware acceleration`, `#local-llama`

---

<a id="item-9"></a>
## [双 DGX Spark 上 GLM 5.3 Flash 新配方解码提速 50%–90%](https://www.reddit.com/r/LocalLLaMA/comments/1wxrozq/for_dual_dgx_spark_users_glm_53_flash_got_a_50/) ⭐️ 7.0/10

一位双 DGX Spark 用户报告称，最新发布的推理"配方"让 GLM 5.3 Flash 的解码速度提升 50%–90%，使其解码速度超过 DeepSeek v4.0 Flash，智能水平也高于无法在双 DGX Spark 上运行的 DeepSeek v4.1 Flash。其基准测试总均值从 61.5 提升到 66.0（+7%），其中聊天场景 +13%、批量 SQL INSERT +10%、代码 +9%、工具调用 +7%。 对于在 NVIDIA 小型 DGX Spark 工作站上跑本地智能体工作负载的用户来说，解码吞吐和多智能体扩展性是最大的瓶颈；50%–90% 的解码提升意味着 320B 级别的 MoE 模型可以在两台小型设备上长时间稳定运行。这也让本地推理的竞争天平重新向 GLM 倾斜——此前 GLM 版本在速度上输给 DeepSeek v4.0 Flash，还存在被不少人抱怨的重复输出缺陷。 提升并不全面：prefill 下降 10%–21%（1.5K 上下文从 1738 降到 1376 tps，128K 从 1758 降到 1578），KV 池缩小约 72%（从 1,988,929 降至 560,362 token，每 rank 固定占用 6 GiB），字节稳定性探针从 8/8 降到 6/8，每步接受 token 数从 6 个中的 3.26（54%）变为 8 个中的 3.55（44%）。在并发 4 下持续 40 分钟的压测中完成 503 次请求，0 错误、0 软空、乱码门限全清。

reddit · r/LocalLLaMA · /u/swiebertjee · 10月4日 21:53

**背景**: DGX Spark 是 NVIDIA 推出的紧凑型桌面 AI 计算机，2025 年以 NUC 形态发布，号称"全球最小的 AI 超级计算机"，面向本地运行 CUDA 加速模型。NVFP4 是 NVIDIA 为 Blackwell Tensor Core 设计的 4 比特浮点格式，用于降低显存占用并提升低精度推理吞吐。GLM 是智谱（Z.ai）的开源权重模型系列，GLM-5.3-Flash 是该系列首个原生多模态模型，总参数约 320B、激活参数约 18B。文中的"decode"指逐 token 生成速度，"prefill"指提示词处理速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DGX_Spark">DGX Spark</a></li>
<li><a href="https://en.wikipedia.org/wiki/GLM_5.3_Flash">GLM 5.3 Flash</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>

</ul>
</details>

**标签**: `#Local LLM inference`, `#DGX Spark`, `#GLM`, `#DeepSeek`, `#Benchmarking`

---

<a id="item-10"></a>
## [开发者仅用 865 亿 token 从零训练出 3.87B MoE 模型](https://www.reddit.com/r/LocalLLaMA/comments/1wxiy8y/i_trained_a_387b_moe_145b_active_from_scratch_on/) ⭐️ 7.0/10

一位 Reddit 用户（u/Prestigious-Taste-63）发布了 Apex-2 模型：这是一个纯解码器（decoder-only）的混合专家（MoE）模型，总参数量 3.87B、每 token 激活 1.45B，完全从零训练、未使用任何外部基座权重，预训练消耗 865 亿 token，随后又进行了约 25 亿 token 的 SFT。该模型及其基准测试结果已发布在 Hugging Face 上，在贪心解码下取得的成绩包括 HumanEval 43.9、MBPP 56.3、GSM8K 32.4 和 MMLU 28.6。 它提供了一个罕见的公开数据点：token 预算极小的小型 MoE 模型在代码任务上依然具备竞争力——其基座模型的 HumanEval+ 据称追平了使用约 18 万亿 token（约为其 200 倍数据量）训练的 Qwen2.5-1.5B。这对希望在有限硬件预算下训练或微调高效小模型的个人研究者和本地 LLM 社区来说是一个积极信号。 在架构上，Apex-2 共有 32 层、d_model 为 2048，采用 GQA（16 个 query 头、4 个 KV 头），每一层都是 16 专家、top-4 路由的 MoE（没有稠密层），上下文长度为 4096，并使用 Qwen3 分词器（15.1 万词表）；模型可通过 transformers/vLLM 中的 Qwen3MoeForCausalLM 映射加载。作者表示，在 22 万对做了长度归一化的数据上做 DPO 会让回答显著变长，并损害代码、数学和 IFEval 表现，因此弃用了 DPO 检查点；他也坦承了若干局限：以英文为主、知识薄弱导致频繁幻觉、LiveCodeBench 中高难度题目得分近乎为零，以及仅支持 4k 上下文。

reddit · r/LocalLLaMA · /u/Prestigious-Taste-63 · 10月4日 15:50

**背景**: 混合专家（MoE）模型把每一层的前馈计算拆分成多个“专家”子网络，每个 token 只被路由到其中少数几个，因此总参数量可以很大，而每个 token 实际消耗的算力（即“激活参数”）保持较小。Grouped Query Attention（GQA）是一种注意力变体，让多个 query 头共享同一个 key/value 头，从而缩小 KV 缓存与显存开销。DiLoCo 是一种分布式训练算法，能大幅降低工作节点之间的通信量，使训练可以跨多台机器乃至多个数据中心展开；本案例中作者借此从单块 NVIDIA GH200 Grace Hopper 超级芯片扩展到两块。整个训练流程还包括在精选数据上的监督微调（SFT），以及 DPO——一种用“优选/劣选”答案对来对齐模型输出的偏好优化方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cyrilzakka.github.io/llm-playbook/nested/gqa.html">Grouped - Query Attention ( GQA ) - The Large Language Model...</a></li>
<li><a href="https://en.wikipedia.org/wiki/NVIDIA_H100_GPU">NVIDIA H100 GPU</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Mixture-of-Experts`, `#from-scratch-training`, `#LocalLLaMA`, `#model-release`

---

<a id="item-11"></a>
## [天津大学发布 3 克无创脑机一体化系统](https://news.tju.edu.cn/info/1005/615029.htm) ⭐️ 7.0/10

天津大学脑机交互与人机共融海河实验室发布“神工·须弥·脑立方”无创脑机一体化系统，重 3 克、体积 2 立方厘米，被称为迄今全球体积最小、重量最轻的无创脑机接口系统。该系统把脑电电极、电路、电池和无线传输全部集成在极小空间内，可隐于发丝间佩戴。 无创脑机接口长期受制于笨重的头戴设备和导电凝胶电极，把采集、处理与无线传输完整压缩进 3 克、可隐于发丝的形态，有望让该技术从实验室演示走向日常使用。官方提及的医疗、消费、教育科研及特种作业安全管理等场景横跨临床与大众市场，这正是脑机接口小型化的商业价值所在。 该消息来自天津大学新闻网的简要通稿，并未给出通道数、信噪比、采样率、采用干电极还是湿电极、续航时间以及无线传输协议等任何技术参数。文中也没有引用经过同行评审的验证或第三方独立测试结果，因此“全球最小最轻”的说法目前仅基于校方自身表述。

telegram · zaihuapd · 10月4日 03:24

**背景**: 脑机接口大致分为两条技术路线：侵入式需通过手术将电极植入大脑皮层，可直接获取高精度神经信号，但存在手术风险与长期稳定性问题；非侵入式通过头皮电极采集脑电（EEG）信号，安全便捷、便于推广，但信号分辨率相对较低。脑电采集高度依赖电极方案：凝胶电极（湿电极）信号质量最好，但需要专业准备、不适合长时间佩戴；干电极则以部分信号质量为代价换取便捷性与可穿戴性。因此，把无创系统做到可隐于发丝的尺寸，本质上是在不牺牲信号质量的前提下，把电极、模拟前端电路、电源和无线传输高度集成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/2056409788087645686">脑电电极怎么选？凝胶电极、水电极与干电极的区别、优缺点解析</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/699343201">侵入式、半侵入式、非侵入式脑机接口，具体应该怎么选 - 知乎</a></li>
<li><a href="https://www.xhby.net/content/s695cce5be4b05fbb22fdf755.html">奋进“十五五”“强富美高”新图景｜ 无 创 脑 机 接 口 ，推开未来世界的“三道门”</a></li>

</ul>
</details>

**标签**: `#brain-computer-interface`, `#BCI`, `#wearable-devices`, `#neurotechnology`, `#hardware`

---