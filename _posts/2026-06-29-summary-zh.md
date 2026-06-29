---
layout: default
title: "Horizon Summary: 2026-06-29 (ZH)"
date: 2026-06-29
lang: zh
---

> 从 135 条内容中筛选出 22 条重要资讯。

---

1. [央视曝光手机厂商测评作弊系统](#item-1) ⭐️ 9.0/10
2. [GLM 5.2 在网络安全测试中超越 Claude](#item-2) ⭐️ 8.0/10
3. [Claude Code 为 MRI 提供 AI 第二诊疗意见](#item-3) ⭐️ 8.0/10
4. [《儿童在线安全法案》要求年龄验证](#item-4) ⭐️ 8.0/10
5. [中国在网络安全领域迎头赶上 Anthropic，重塑 AI 竞赛](#item-5) ⭐️ 8.0/10
6. [DFlash 支持已合并到 llama.cpp](#item-6) ⭐️ 8.0/10
7. [Ornith-35B GGUF 原生 MTP 推测解码基准测试](#item-7) ⭐️ 8.0/10
8. [DeepSpec：DeepSeek 开源投机解码代码库](#item-8) ⭐️ 8.0/10
9. [纯 C 语言实现的 Qwen 3 CPU 推理引擎](#item-9) ⭐️ 8.0/10
10. [谷歌限制 Meta 使用 Gemini，因 AI 算力不足](#item-10) ⭐️ 8.0/10
11. [苹果 WWDC 2026 AI 战略重置](#item-11) ⭐️ 8.0/10
12. [英国 AI 初创公司 Wayve 挑战特斯拉和 Waymo](#item-12) ⭐️ 8.0/10
13. [1960-2026 内存价格：历史趋势与波动](#item-13) ⭐️ 7.0/10
14. [布朗大学教授谴责考试中大规模 AI 作弊](#item-14) ⭐️ 7.0/10
15. [Tokenmaxxing 争议转向复合正确性](#item-15) ⭐️ 7.0/10
16. [OpenAI Codex 安全争议：是否采用选择性文件访问](#item-16) ⭐️ 7.0/10
17. [消失的波兰字母 S：键盘快捷键与变音符号的冲突](#item-17) ⭐️ 7.0/10
18. [惠普与 OpenAI 达成 Frontier 战略合作](#item-18) ⭐️ 7.0/10
19. [基于本地模型与 RAG 的 NPC 引擎](#item-19) ⭐️ 7.0/10
20. [800M 参数模型通过因果扩散实现图像动画化](#item-20) ⭐️ 7.0/10
21. [Telegram 在 Android 12.9 Beta 中测试社区功能](#item-21) ⭐️ 7.0/10
22. [诺基亚与英伟达合作构建 6G AI-RAN](#item-22) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [央视曝光手机厂商测评作弊系统](https://weibo.com/2656274875/5314693197725859) ⭐️ 9.0/10

央视调查发现，手机厂商向测评博主提供特供媒体机，固件内嵌识别程序可在检测到博主身份时自动开启高性能模式，并配合云端远程配置作弊，营造出超出实际性能的假象。 这种系统性作弊损害了手机测评的公信力，误导消费者，使其难以做出明智的购买决策。同时也给监管机构和科技记者发现并揭露此类隐蔽操纵行为带来了巨大挑战。 作弊体系分为三层：硬件筛选、固件识别和云端配置调整。识别到博主测评时，设备可自动提升 CPU 性能、提高屏幕亮度，并仅加载应用界面而非完整应用，以营造流畅假象。

telegram · zaihuapd · 6月28日 01:37

**背景**: 手机跑分测试是用于衡量智能手机性能的标准化测试，帮助消费者比较不同设备。近年来，多个品牌被指控优化手机以检测跑分应用并在测试中运行最高性能，这种做法被称为'跑分作弊'。央视报道揭露了针对具体测评博主的更复杂方案，而不仅仅是针对跑分应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=9SkaucNNYvQ">Smartphone Benchmark Cheating Explained: New "Boost ... - YouTube</a></li>
<li><a href="https://www.phonearena.com/news/benchmark-gate-are-smartphone-manufacturers-secretly-cheating_id179574">Benchmark gate: Are smartphone manufacturers secretly cheating?</a></li>

</ul>
</details>

**标签**: `#phone reviews`, `#benchmark cheating`, `#consumer rights`, `#tech ethics`, `#investigative reporting`

---

<a id="item-2"></a>
## [GLM 5.2 在网络安全测试中超越 Claude](https://semgrep.dev/blog/2026/we-have-mythos-at-home-glm-52-beats-claude-in-our-cyber-benchmarks/) ⭐️ 8.0/10

来自 Z.AI 的开源 753B 参数模型 GLM 5.2 在网络安全基准测试中被报告超越 Claude，在 Semgrep 的测试中以每个漏洞 0.17 美元的成本发现漏洞，击败了 Claude Code 的 32%成功率。 这表明开源模型在网络安全等专业领域正在缩小与专有前沿模型的差距，可能为漏洞检测等任务提供成本效益更高的替代方案。 GLM 5.2 采用 MIT 许可证发布，支持 100 万 token 的上下文长度，在 Terminal-Bench 2.1 上达到 81.0 分，仅略低于 Claude Opus 4.8 的 85.0 分。但其 753B 参数要求本地推理需大量硬件资源。

hackernews · jms703 · 6月28日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=48709670)

**背景**: 类似 CyberBench 的 LLM 基准测试评估模型在网络安全任务上的性能。GLM 是由 Z.AI 开发的开源模型系列，GLM 5.2 是其最新旗舰模型，专注于编码和长周期任务。Claude 是 Anthropic 的专有模型系列。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openlm.ai/glm-5.2/">GLM-5.2 - openlm.ai</a></li>
<li><a href="https://z.ai/blog/glm-5.2">GLM-5.2: Built for Long-Horizon Tasks - z.ai</a></li>

</ul>
</details>

**社区讨论**: 评论者指出 GLM 5.2 性能强劲且通过能源计价成本低廉，有用户仅花费 18 美元就使用了 3.74 亿 token。但也有质疑基准对比的，指出 Claude Code 是代理工具而非纯 LLM。

**标签**: `#AI`, `#LLM`, `#benchmarks`, `#GLM-5.2`, `#open-source`

---

<a id="item-3"></a>
## [Claude Code 为 MRI 提供 AI 第二诊疗意见](https://antoine.fi/mri-analysis-using-claude-code-opus) ⭐️ 8.0/10

一位用户使用 Anthropic 开发的 AI 编程代理 Claude Code 分析自己的 MRI 图像，作为第二诊疗意见，展示了大型语言模型在医学影像解读中的潜力和局限性。 这一实验凸显了 AI 用于个人健康分析的日益普及，但也强调了在高风险医疗决策中数据不完整和过度依赖 AI 等风险。 该分析使用了 Claude Code 的视觉能力，但用户缺少完整的 3D MRI 数据集，放射科医生指出这对准确评估至关重要。用户还基于超声结果对先前的冲击波治疗建议提出了质疑。

hackernews · engmarketer · 6月28日 16:35 · [社区讨论](https://news.ycombinator.com/item?id=48708941)

**背景**: Claude Code 是 Anthropic 开发的 AI 代理，能通过自然语言读取代码、编辑文件和运行命令。它基于 Claude 模型构建，该模型具备视觉能力，可以处理 MRI 扫描等图像。大型语言模型越来越多地应用于医学影像分析，用于报告生成和疾病分类等任务，但其在直接患者诊断中的应用仍处于实验阶段且需谨慎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://www.mdpi.com/2306-5354/12/8/818">Large Language Models in Medical Image Analysis: A ... - MDPI</a></li>

</ul>
</details>

**社区讨论**: 来自放射科医生的评论强调，没有完整的 3D 数据集，AI 分析是有限的，并指出超声检测钙化不可靠。其他用户讨论了 AI 与人类专家的可信度，一些人赞赏可以无时间压力地无限提问，而另一些人则担忧误诊风险，并引用了如结核病误诊等例子。

**标签**: `#AI in healthcare`, `#LLM applications`, `#medical imaging`, `#trust in AI`, `#Claude Code`

---

<a id="item-4"></a>
## [《儿童在线安全法案》要求年龄验证](https://www.eff.org/deeplinks/2026/06/kids-act-would-require-age-checks-get-online) ⭐️ 8.0/10

电子前哨基金会（EFF）发布了对《儿童在线安全法案》的分析，该法案要求在线平台对所有用户实施年龄验证。 这项立法引发了严重的隐私和言论自由担忧，因为年龄验证可能导致数据收集和匿名言论的潜在审查。 该法案将“受覆盖平台”定义为使用个人信息进行广告、营销或内容推荐的平台，这可能排除了许多网站，如 Hacker News 或个人博客。

hackernews · bilsbie · 6月28日 11:56 · [社区讨论](https://news.ycombinator.com/item?id=48706560)

**背景**: 年龄验证法律日益被提出以保护未成年人上网安全，但它们通常要求用户提交政府颁发的身份证件或生物特征数据。批评者认为这破坏了匿名性，并可能创建易受攻击的集中式数据库。

**社区讨论**: 评论者质疑该法案的覆盖范围，有人指出 Hacker News 很可能不属于受覆盖平台。另一人指出研究显示社交媒体与心理健康关联的证据很少，暗示该法案可能基于有问题的前提。

**标签**: `#internet regulation`, `#privacy`, `#child safety`, `#age verification`, `#EFF`

---

<a id="item-5"></a>
## [中国在网络安全领域迎头赶上 Anthropic，重塑 AI 竞赛](https://www.reddit.com/r/LocalLLaMA/comments/1ui3tck/china_has_matched_anthropic_in_cybersecurity/) ⭐️ 8.0/10

有说法称中国在网络安全能力上已与 Anthropic 持平，可能重新定义全球 AI 竞赛格局。 这一进展标志着 AI 领域的重大地缘政治转变，网络安全是 AI 能力的关键维度；中国迎头赶上可能改变竞争平衡，并加速全球 AI 安全讨论。 该说法源自 r/LocalLLaMA 上一个高评分帖子，但帖子本身未提供具体证据或技术细节。Anthropic 已通过 Project Glasswing 和 Claude Mythos2 Preview 等项目展示了先进网络安全能力。

reddit · r/LocalLLaMA · /u/pscoutou · 6月28日 17:51

**背景**: Anthropic 的 Claude 模型展现出涌现的网络安全能力，例如在夺旗挑战中发现和利用软件漏洞。中国一直在大力投资 AI，包括网络安全应用。关于匹敌的说法表明中国的 AI 模型可能已达到类似复杂程度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/glasswing">Project Glasswing: Securing critical software for the AI era \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/research/building-ai-cyber-defenders">Building AI for cyber defenders \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#cybersecurity`, `#China`, `#Anthropic`, `#AI race`

---

<a id="item-6"></a>
## [DFlash 支持已合并到 llama.cpp](https://www.reddit.com/r/LocalLLaMA/comments/1uhx862/dflash_support_merged_into_llamacpp/) ⭐️ 8.0/10

DFlash——一种用于投机解码的块扩散模型——已被合并到 llama.cpp 中，通过并行块草稿实现了更快的本地 LLM 推理。 此集成显著提升了 llama.cpp 用户的推理速度，尤其是在 NVIDIA Blackwell GPU 上，有望降低延迟并提高本地 LLM 部署的吞吐量。 DFlash 使用块扩散草稿模型并行生成整个 token 块，由目标 LLM 验证。Blackwell GPU 上的基准测试显示，对于 gpt-oss-120b 等模型，吞吐量提升高达 15 倍。

reddit · r/LocalLLaMA · /u/sammcj · 6月28日 13:24

**背景**: 投机解码通过使用快速草稿模型生成多个候选 token，然后由目标模型并行验证，从而加速 LLM 推理。DFlash 通过同时草稿 token 块进一步提升了效率。llama.cpp 是一个广泛使用的 C++ 库，用于在消费级硬件上运行 LLM。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/boost-inference-performance-up-to-15x-on-nvidia-blackwell-using-dflash-speculative-decoding/">Boost Inference Performance up to 15x on NVIDIA Blackwell Using DFlash ...</a></li>
<li><a href="https://arxiv.org/abs/2602.06036">DFlash: Block Diffusion for Flash Speculative Decoding</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#DFlash`, `#local LLMs`, `#inference optimization`

---

<a id="item-7"></a>
## [Ornith-35B GGUF 原生 MTP 推测解码基准测试](https://www.reddit.com/r/LocalLLaMA/comments/1ui4yn6/ornith1035b_gguf_update_native_mtp/) ⭐️ 8.0/10

Ornith-1.0-35B GGUF 模型现在在 IQ4_XS 量化版本上集成了原生 MTP 推测解码草稿头，在单个 GPU 上通过 llama.cpp 实现了单流解码速度 1.3-1.35 倍的提升（从 172.6 tok/s 到 233.8 tok/s）。 这展示了多令牌预测（MTP）推测解码被实际集成到广泛使用的本地 LLM 格式中，在大多数情况下无需牺牲输出质量即可实现更快的推理。该方法可被其他模型量化者复制，有望提升本地 AI 应用的实时性能。 下一个令牌分布对 32/32 序列保持字节级一致（KLD 0.0），但长确定性生成中令牌匹配率为 93.4%，并非逐位精确。MTP 嫁接版本（IQ4_XS 主体加 Q6 头部）占用约 19.6 GB，与 Q4_K_M 相比在大小、速度和保真度之间提供了有利的权衡。

reddit · r/LocalLLaMA · /u/Blahblahblakha · 6月28日 18:35

**背景**: 推测解码通过使用小型草稿模型预测多个令牌，再由目标模型并行验证，从而加速 LLM 推理。多令牌预测（MTP）是其中一种变体，目标模型自身包含对未来令牌的预测头，无需单独的草稿模型即可自我推测。GGUF 是一种量化模型格式，以牺牲部分精度为代价减少内存占用；常见级别从 Q2 到 Q8，其中 K_M 变体提供了混合精度优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency in AI Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://www.shepbryan.com/blog/what-is-gguf">What is GGUF? A Beginner's Guide — Trencadís</a></li>

</ul>
</details>

**标签**: `#MTP`, `#speculative decoding`, `#GGUF`, `#llama.cpp`, `#quantization`

---

<a id="item-8"></a>
## [DeepSpec：DeepSeek 开源投机解码代码库](https://www.reddit.com/r/LocalLLaMA/comments/1uhyhl3/deepspec_a_deepseekai_collection/) ⭐️ 8.0/10

投机解码是加速大语言模型推理的关键技术，DeepSpec 提供了完整且可复现的开源实现，使研究人员和从业者能够训练自己的草稿模型，有望将推理延迟降低 2-3 倍甚至更多。 该仓库包括数据准备工具、多种草稿模型架构（DSpark、DFlash、Eagle3）、训练代码、评估脚本，以及针对 Qwen3-4B/8B/14B 和 Gemma-4-12B-it 的预训练检查点。所有检查点均在非思考模式下使用 open-perfectblend 数据训练，用户被建议针对特定领域或思考模式使用情况进行微调。

reddit · r/LocalLLaMA · /u/pmttyji · 6月28日 14:18

**背景**: 投机解码是一种推理时优化技术：小型草稿模型生成多个候选 token，大型目标模型在单次前向传递中验证它们，在保持输出分布不变的同时降低延迟。DeepSpec 实现了三种前沿草稿算法：Eagle3 使用外推草稿头，DFlash 使用块扩散，DSpark 是另一种变体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding</a></li>
<li><a href="https://arxiv.org/abs/2503.01840">[2503.01840] EAGLE-3: Scaling up Inference Acceleration of ... llm-draftmodels-eagle3/README.md at main - GitHub Images EAGLE-3: Scaling up Inference Acceleration of Large Language ... thoughtworks/MiniMax-M2.5-Eagle3 · Hugging Face Eagle3 - Speculators Docs Ex0bit/Qwen3.6-27B-PRISM-EAGLE3 · Hugging Face</a></li>
<li><a href="https://www.baseten.co/blog/dflash-faster-llm-inference/">DFlash : 3x faster LLM inference</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#LLM inference`, `#open-source`, `#DeepSeek`, `#efficiency`

---

<a id="item-9"></a>
## [纯 C 语言实现的 Qwen 3 CPU 推理引擎](https://www.reddit.com/r/LocalLLaMA/comments/1uht9rf/a_barebones_cpuonly_inference_engine_for_qwen_3/) ⭐️ 8.0/10

一位开发者从头用纯 C 语言编写了一个极简的 CPU 推理引擎，支持 Qwen 3 模型（4B 及以下），仅依赖 libc、libm、cJSON 和可选的 OpenMP。 该项目表明，无需依赖高层框架也能深入理解 Transformer 推理过程，并为 LLM 社区提供了一个极具可读性的学习代码库。 该引擎直接从 Hugging Face 的 safetensors 格式加载权重，实时进行 4 位仿射量化，实现了 KV 缓存，并内置聊天界面，但在 i5-1240P 笔记本上每秒仅能生成约 1 个 token。

reddit · r/LocalLLaMA · /u/jakint0sh · 6月28日 09:58

**背景**: Qwen 3 是阿里巴巴开发的一系列大型语言模型，覆盖从 0.6B 到更大的参数规模。Safetensors 是一种安全、快速存储模型权重的文件格式，旨在替代不安全的 pickle 格式。4 位仿射量化将模型精度降至 4 位以降低内存占用并加速推理，通过仿射变换将浮点值映射为整数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3-0.6B">Qwen / Qwen 3 -0.6B · Hugging Face</a></li>
<li><a href="https://github.com/safetensors/safetensors">GitHub - safetensors/safetensors: Simple, safe way to store and ...</a></li>
<li><a href="https://arxiv.org/abs/2403.12544">[2403.12544] AffineQuant: Affine Transformation Quantization ... 4-bit quantization · Hugging Face Model Quantization: Concepts, Methods, and Why It Matters TwinQuant: Learnable Subspace Decomposition for 4-Bit LLM ... 4-bit Quantization Guide 2025 | ShadeCoder Quantization concepts · Hugging Face Mastering QLoRa : A Deep Dive into 4-Bit Quantization and ...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#CPU`, `#Qwen 3`, `#C`, `#open-source`

---

<a id="item-10"></a>
## [谷歌限制 Meta 使用 Gemini，因 AI 算力不足](https://www.ft.com/content/c5d52f72-71ef-40bc-bad3-61afdba8b378) ⭐️ 8.0/10

谷歌已告知 Meta，无法提供 Meta 计划购买的全部 Gemini AI 算力容量，自 2026 年 3 月以来，Meta 的一些内部 AI 项目被延迟。 这凸显了 AI 行业关键的基础设施瓶颈，Meta 等大公司的算力需求超出了 Google 等云提供商的供应能力，可能重塑竞争格局，促使公司加速自研模型。 限制措施仍然有效，Meta 已鼓励员工更高效地使用 AI tokens，同时加速开发其自研的 Muse Spark 模型（2026 年 4 月发布）。

telegram · zaihuapd · 6月28日 07:38

**背景**: AI tokens 是大型语言模型处理文本的基本单位，管理 token 使用是控制算力成本的关键。Google 正在扩充算力，包括与 SpaceX 签署每月 9.2 亿美元的协议，CEO Sundar Pichai 承认近期算力受限。Meta 自身无云业务，正大力投资数据中心（计划到 2028 年在美国投资 6000 亿美元）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/ai-tokens-explained/">What Are AI Tokens ? The Language and Currency... | NVIDIA Blog</a></li>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-msl/">Introducing Muse Spark: Scaling Towards Personal Superintelligence</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Google`, `#Meta`, `#Gemini`, `#AI Infrastructure`, `#Compute Capacity`

---

<a id="item-11"></a>
## [苹果 WWDC 2026 AI 战略重置](https://finance.yahoo.com/technology/ai/articles/apple-ai-overhaul-seen-driving-211812667.html) ⭐️ 8.0/10

预计苹果在 WWDC 2026 上将宣布对其 AI 策略进行重大积极调整，回应此前的批评，并指引新方向。 此次调整可能重塑苹果在 AI 赛道的地位，影响竞争格局和投资者信心，并可能带动行业产品发展方向。 预计该公告将包含克服先前 AI 策略不足的具体措施，但具体细节仍待大会揭晓。

openbb · AAPL · 6月28日 21:18

**背景**: 苹果的 AI 策略因落后于谷歌和微软等竞争对手而受到批评。WWDC（全球开发者大会）是苹果每年发布重大软件和硬件更新的活动。策略重置意味着苹果在生态系统内整合 AI 的方式将发生根本性转变。

**标签**: `#Apple`, `#AI`, `#WWDC`, `#Strategy`

---

<a id="item-12"></a>
## [英国 AI 初创公司 Wayve 挑战特斯拉和 Waymo](https://www.wsj.com/business/autos/wayve-self-driving-technology-2e917ebd?siteid=yhoof2&yptr=yahoo) ⭐️ 8.0/10

一家名为 Wayve 的新 AI 初创公司凭借端到端深度学习和纯摄像头传感器，成为自动驾驶领域特斯拉和 Waymo 的竞争对手。 Wayve 摒弃昂贵的传感器套件而采用纯摄像头系统，可能降低自动驾驶技术的成本，从而加速其普及。 Wayve 使用改装电动车队收集数据并训练其 AI 模型，专注于可泛化的驾驶行为而非基于规则的系统。

openbb · AAPL · 6月28日 09:30

**背景**: 自动驾驶传统上依赖激光雷达、雷达和摄像头等多种传感器，并基于大量规则编程。特斯拉和 Waymo 代表两种主流范式：特斯拉采用纯视觉方案，而 Waymo 依赖激光雷达和高精地图。Wayve 的端到端学习方法类似特斯拉，但更强调从人类驾驶中学习，提供了潜在的第三条路径。

**标签**: `#autonomous driving`, `#AI`, `#startup`, `#Tesla`, `#Waymo`

---

<a id="item-13"></a>
## [1960-2026 内存价格：历史趋势与波动](https://dam.stanford.edu/memory-prices.html) ⭐️ 7.0/10

这些长期价格数据为理解硬件成本趋势、摩尔定律的终结以及人工智能等新技术对内存可负担性的影响提供了重要背景。 该图表显示，截至 2024 年，每 GB 内存价格已回滚至大约 2010 年的水平，且曲线在 2010 年代随着摩尔定律的终结而趋于平缓。

hackernews · vga1 · 6月28日 18:32 · [社区讨论](https://news.ycombinator.com/item?id=48710092)

**背景**: 由于技术进步和规模经济，内存价格历史上呈指数级下降，这一趋势由摩尔定律体现。但近年来，加密货币挖矿和人工智能需求导致了价格波动，部分逆转了长期以来的下降趋势。

**社区讨论**: 社区评论指出，价格未根据通货膨胀进行调整，这会使早期的数据点显著提高。用户还讨论了加密货币和人工智能在近期波动中的作用，并观察到 DDR5 的价格大约相当于 2010 年 DDR3 的水平。

**标签**: `#memory prices`, `#hardware`, `#history`, `#economics`

---

<a id="item-14"></a>
## [布朗大学教授谴责考试中大规模 AI 作弊](https://english.elpais.com/education/2026-06-28/ai-fraud-at-brown-university-academic-integrity-is-at-risk.html) ⭐️ 7.0/10

2026 年 6 月，布朗大学一位教授公开谴责考试中广泛存在的 AI 辅助作弊现象，引发了关于如何调整学术评估以适应 AI 时代的讨论。 这一事件凸显了 AI 对学术诚信日益严峻的挑战，迫使大学重新设计考试形式，并反思在 AI 能轻松完成作业的时代，分数的意义何在。 该教授的研究方向是博弈论，他指出学生普遍使用 AI 使得传统检测方法失效。社区讨论中建议采取现场手写考试和一对一面试等应对措施。

hackernews · geox · 6月28日 16:41 · [社区讨论](https://news.ycombinator.com/item?id=48708991)

**背景**: 大型语言模型（如 GPT-4）能够生成文章并解决复杂问题，成为在开卷考试和作业中作弊的强大工具。现有的 AI 检测工具（如 Turnitin 的 AI 检测器）准确性有限，且可以被规避。这促使教育工作者探索替代评估方法，包括监考下的手写考试和口头面试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://discovery.ucl.ac.uk/id/eprint/10208163/9/Leaton_AI-Based+Digital+Cheating+At+University,+and+the+Case+for+New+Ethical+Pedagogies_VoR.pdf">AI-Based Digital Cheating At University, and the Case for New Ethical...</a></li>
<li><a href="https://answers.atlassian.syr.edu/wiki/spaces/blackboard01/pages/154371659/AI+Tools+and+How+Students+Use+Them+for+Academic+Dishonesty">AI Tools and How Students Use Them for Academic Dishonesty ...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了多种观点：有人主张恢复现场手写考试，有人建议拥抱 AI 并重新设计评估以聚焦高阶技能。一位评论者分享了调整课程的经验，还有一位教授质疑了评分的意义。

**标签**: `#AI ethics`, `#academic integrity`, `#education technology`, `#AI fraud`, `#assessment design`

---

<a id="item-15"></a>
## [Tokenmaxxing 争议转向复合正确性](https://12gramsofcarbon.com/p/agentics-tech-things-tokenmaxxing) ⭐️ 7.0/10

最近的一场争论认为，被称为“tokenmaxxing”（最大化 token 消耗）的 AI 效率策略正被一种新的“复合正确性”范式所取代，即花费更多 token 会带来更好的结果。 这一转变反映了对如何在工作流中有效利用 AI 的理解不断演变，从基于数量的指标转向关注质量的方法，可能重塑开发者和公司衡量 AI 生产力的方式。 “复合正确性”的概念表明，在代码生成或安全分析等任务中增加 token 支出会带来更好的结果，但批评者认为这种关系并不确定，且取决于具体情境。

hackernews · theahura · 6月28日 16:24 · [社区讨论](https://news.ycombinator.com/item?id=48708795)

**背景**: Tokenmaxxing 指的是将最大化 AI token 使用量作为生产力和采用率的指标的做法，通常出现在早期实验阶段。复合正确性是一种新兴理念，AI 系统通过迭代的 token 消耗来改进，从每次交互中学习以产生更准确的输出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://builtin.com/articles/ai-tokenmaxxing">What Is Tokenmaxxing ? The AI Workplace Trend Explained. | Built In</a></li>
<li><a href="https://www.ibm.com/think/insights/tokenmaxxing-dead-long-live-valuemaxxing">Tokenmaxxing is dead, long live valuemaxxing | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了不同观点：一些人认为 tokenmaxxing 是推动 AI 采用的临时过渡策略，而另一些人则对“复合正确性”表示怀疑，认为 token 支出与质量之间的关系并不简单。一位用户指出，tokenmaxxing 始终只是一种短期推动手段，而非永久性指标。

**标签**: `#AI`, `#token usage`, `#LLM`, `#efficiency`, `#community discussion`

---

<a id="item-16"></a>
## [OpenAI Codex 安全争议：是否采用选择性文件访问](https://github.com/openai/codex/issues/2847) ⭐️ 7.0/10

OpenAI Codex 的 GitHub issue (#2847) 仍未关闭，讨论是否应实现选择性文件访问机制，以防止用户机器上的敏感数据意外泄露。 这场争论凸显了 AI 编码助手中的关键安全矛盾：在便利性与数据保护之间取得平衡。其结果可能影响其他 AI 工具处理文件访问和用户隐私的方式。 社区成员指出，现有操作系统级控制（chmod、容器）已能限制文件访问，而由于 LLM 的行为不可预测，选择性列表可能提供虚假的安全感。一些人认为问题应在沙箱层面解决，而非在 Codex 内部。

hackernews · pikseladam · 6月28日 12:27 · [社区讨论](https://news.ycombinator.com/item?id=48706714)

**背景**: 代码泄露是指从系统中未经授权传输源代码或敏感数据。像 OpenAI Codex 这样的 AI 编码助手可以访问本地文件以生成代码，引发了敏感文件（例如包含 API 密钥的 .env）可能被意外上传到远程服务器的担忧。选择性机制要求用户明确授予文件访问权限，与当前默认允许（opt-out）的方式形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fortinet.com/resources/cyberglossary/data-exfiltration">What is Data Exfiltration and How Can You Prevent It? | Fortinet</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人主张选择性访问（nikhilsimha）并分享自定义沙箱方案；另一些人认为现有操作系统工具已足够（TheDong, petcat），并警告黑名单方法不完整。Skybrian 呼吁通过 ssh-agent 等代理消除 .env 文件，而 mbid 开源了远程 devcontainer 方案（rumpelpod）以隔离代理。

**标签**: `#AI safety`, `#security`, `#coding assistants`, `#OpenAI Codex`

---

<a id="item-17"></a>
## [消失的波兰字母 S：键盘快捷键与变音符号的冲突](https://aresluna.org/the-curious-case-of-the-disappearing-polish-s/) ⭐️ 7.0/10

一篇 2015 年的文章解释了为什么波兰语变音符号（如'ś'）会被浏览器键盘快捷键拦截，导致其消失或触发意外操作。问题在于浏览器对组合键的处理与输入这些字符所用的输入法存在冲突。 这突出了一个长期存在的本地化和 Web 开发难题，影响了波兰语使用者以及其他使用变音符号的语言用户。理解这一点有助于开发者构建更包容的 Web 应用，以尊重多样化的输入方式。 文章指出，在 Windows 上使用右 Alt 键组合输入变音符号时会出现问题，所提供的解决方法只能部分修复。此外，社区评论指出，其他变音符号如'Ć'会触发 Windows 上的 Copilot，而 Unicode 规范化也揭示了处理波兰字母的复杂性，例如'ł'无法分解。

hackernews · colinprince · 6月28日 12:44 · [社区讨论](https://news.ycombinator.com/item?id=48706814)

**背景**: Unicode 规范化是将等效的字符序列转换为标准形式的过程。例如，字母'ñ'可以表示为单个码点（U+00F1），也可以表示为基本字母'n'加组合波浪号（U+006E + U+0303）。这对于文本处理、搜索和分词很重要，例如在 SQLite 的全文搜索中，去除变音符号对于某些波兰字母（如'ł'）会失败。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unicode_normalization">Unicode normalization</a></li>

</ul>
</details>

**社区讨论**: 评论者补充了文化背景，指出波兰使用拉丁字母使其与西欧更为接近。技术评论讨论了浏览器 API 的不足以及波兰字母在 Unicode 规范化中的复杂性，例如'ł'在 NFC 规范化中无法分解。

**标签**: `#unicode`, `#keyboard shortcuts`, `#Polish language`, `#web development`, `#localization`

---

<a id="item-18"></a>
## [惠普与 OpenAI 达成 Frontier 战略合作](https://openai.com/index/hp-frontier-partnership) ⭐️ 7.0/10

惠普公司宣布与 OpenAI 达成 Frontier 战略合作，将在客户体验、软件开发和企业运营中全面部署 AI。 此次合作标志着前沿 AI 模型在企业级应用中的普及加速，可能推动惠普数字化转型，同时拓展 OpenAI 在企业市场的覆盖。 惠普加入 OpenAI 的 Frontier 计划，该计划提供前沿模型和专属工程支持；合作覆盖惠普多个业务部门。

rss · OpenAI News · 6月28日 17:00

**背景**: OpenAI 的 Frontier 计划是一项战略举措，旨在与大型企业和咨询公司（如 Capgemini、Accenture）合作，大规模部署最先进的 AI 模型。前沿模型指的是像 GPT-4 这样最先进的大语言模型，具有成本高、能力广泛的特点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Frontier_model">Frontier model</a></li>
<li><a href="https://www.linkedin.com/posts/tinholt_capgemini-and-openai-today-announced-a-strategic-activity-7431837038951346176-7V5j">Capgemini and OpenAI today announced a strategic partnership ...</a></li>
<li><a href="https://aibusinessweekly.net/p/openai-frontier-alliances-accenture-bcg-capgemini-mckinsey-enterprise-ai">OpenAI Frontier Alliances: Big 4 Consulting Partnership</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#HP`, `#AI Partnerships`, `#Enterprise AI`, `#Frontier Model`

---

<a id="item-19"></a>
## [基于本地模型与 RAG 的 NPC 引擎](https://www.reddit.com/r/LocalLLaMA/comments/1uibt9o/npc_engine_using_local_models/) ⭐️ 7.0/10

该开发者构建了一个游戏无关的 NPC 引擎，使用 NVIDIA Parakeet 0.6 进行语音转文字、Gemma 4 26B A4B 作为语言模型、Qwen3-TTS 进行文字转语音，并借助 RAG 保持提示简洁，从而实现快速响应。 该项目展示了将本地模型用于 RPG 实时 NPC 对话的实用案例，有可能减少对云 API 的依赖并支持离线游戏。它可能激励更多轻量级、保护隐私的游戏 AI 开发。 该引擎通过 RAG 仅根据玩家消息注入数百个可能动作中的相关项，避免提示过长。使用较小的本地模型实现了超快的响应速度和不错的输出质量。

reddit · r/LocalLLaMA · /u/goodive123 · 6月28日 23:13

**背景**: NPC 引擎负责游戏中非玩家角色的对话和行动。RAG（检索增强生成）从数据库中检索相关信息来增强语言模型的提示。本地模型在用户自己的机器上运行，提供隐私保护和离线能力。SillyTavern 是一个流行的本地界面，用于与 LLM 和 TTS 模型交互。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/KritBlade/MVU_Game_Maker">GitHub - KritBlade/MVU_Game_Maker: Turn any SillyTavern RPG character card into MVU based. · GitHub</a></li>
<li><a href="https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2">nvidia / parakeet -tdt-0.6b-v2 · Hugging Face</a></li>
<li><a href="https://huggingface.co/spaces/Qwen/Qwen3-TTS">Qwen 3 - TTS Demo - a Hugging Face Space by Qwen</a></li>

</ul>
</details>

**标签**: `#local models`, `#RAG`, `#game development`, `#NPC engine`, `#AI`

---

<a id="item-20"></a>
## [800M 参数模型通过因果扩散实现图像动画化](https://www.reddit.com/r/LocalLLaMA/comments/1uicq8x/locally_running_mode_turns_an_image_into_a_cute/) ⭐️ 7.0/10

一个 800M 参数模型利用因果扩散和键值缓存，将静态图像转化为可在消费级 GPU 上运行的动画、可控制角色。相比之前版本，稳定性有所提升，但仍存在一致性问题。 这实现了从单张图像到本地硬件上的实时角色动画，使 AI 爱好者和游戏开发者无需依赖云端即可创建可交互角色。它展示了扩散模型与类 Transformer 缓存结合用于高效视频生成的进步。 该模型处理 12 个潜在帧（通过 VAE 对应 80-120 个像素帧），并使用滑动窗口限制 KV 缓存在训练上下文长度内。500M 版本在 RTX 5090 上可达到 60 fps 以上，而 800M 版本速度更慢但能力更强。

reddit · r/LocalLLaMA · /u/lucidml_lover · 6月28日 23:55

**背景**: 因果扩散将去噪步骤调整为顺序生成帧，每帧的潜在表示被添加到存储过去帧作为上下文的 KV 缓存中。KV 缓存借鉴自大型语言模型，使扩散模型能够维持时间连贯性而无需重新处理所有历史帧。该方法受扩散因果模型以及最近关于扩散 LLM 的 KV 缓存自适应工作的启发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/patrickrchao/DiffusionBasedCausalModels">GitHub - patrickrchao/DiffusionBasedCausalModels · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2510.14973">[2510.14973] Attention Is All You Need for KV Cache in Diffusion LLMs</a></li>

</ul>
</details>

**标签**: `#diffusion models`, `#local AI`, `#animation`, `#machine learning`, `#image generation`

---

<a id="item-21"></a>
## [Telegram 在 Android 12.9 Beta 中测试社区功能](https://t.me/zaihuapd/42224) ⭐️ 7.0/10

Telegram 在 Android 12.9 Beta 版中引入了社区功能，允许用户将多个围绕同一主题的群组聚合为一个社区。目前该功能仅限于测试服务器，且仅支持群组，不支持频道。 该功能显著增强了 Telegram 的群组管理能力，使用户更容易组织和浏览相关对话。这可能会提升 Telegram 对大规模社区建设的吸引力，与 Discord 等平台竞争。 社区管理员可以开启“显示为一个对话”，将社区内聊天合并为单一入口，并可以设置仅受邀成员可见的隐藏对话。该功能目前处于测试阶段，仅在测试服务器上可用，频道支持预计稍后推出。

telegram · zaihuapd · 6月28日 09:43

**背景**: Telegram 是一款注重隐私和大型群组功能的流行即时通讯平台。这项新的社区功能在其现有群组功能基础上构建，旨在为主题讨论提供更有组织的结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www1.ru/en/news/2026/06/27/telegram-testiruet-novuiu-funkciiu-soobshhestva.html">Telegram is testing a new "Communities" feature - ru</a></li>
<li><a href="https://telegram.org/beta">Telegram Messenger</a></li>

</ul>
</details>

**标签**: `#Telegram`, `#beta`, `#community`, `#groups`, `#features`

---

<a id="item-22"></a>
## [诺基亚与英伟达合作构建 6G AI-RAN](https://finance.yahoo.com/technology/ai/articles/nokia-hlse-nokia-partners-nvidia-220600162.html) ⭐️ 7.0/10

诺基亚宣布与英伟达合作，为 6G 电信开发人工智能驱动的无线接入网络（AI-RAN）。 此次合作将诺基亚的电信基础设施专长与英伟达的 AI 计算领导力相结合，可能加速 6G 标准化进程，并实现智能高效的网络。 合作将聚焦于 AI-RAN（AI 与 RAN）架构，即在网络边缘共享 AI 和 RAN 功能的计算资源，这与行业讨论的描述一致。

openbb · AAPL · 6月28日 22:06

**背景**: 6G 是 5G 的规划后继，预计将提供更高的数据速率、更低的延迟，并支持 AI 原生网络。AI-RAN（人工智能无线接入网络）将 AI 集成到 RAN 运营中，要么使用 AI 优化无线电功能（AI-for-RAN），要么在 AI 与 RAN 任务之间共享计算资源（AI-with-RAN）。此次合作旨在为未来的 6G 部署开发后一种方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/6G">6 G - Wikipedia</a></li>
<li><a href="https://www.6gflagship.com/news/ai-ran-momentum-builds-and-it-might-be-time-to-pay-attention/">AI - RAN momentum builds and it might be time to pay attention</a></li>
<li><a href="https://www.linkedin.com/learning/ai-in-ran-radio-access-network-transforming-mobile-networks/the-building-blocks-of-ai-ran">The building blocks of AI - RAN - AI in RAN ( Radio Access Network )...</a></li>

</ul>
</details>

**标签**: `#6G`, `#AI`, `#Nokia`, `#Nvidia`, `#Telecom`

---