---
layout: default
title: "Horizon Summary: 2026-11-14 (ZH)"
date: 2026-11-14
lang: zh
---

> 从 99 条内容中筛选出 20 条重要资讯。

---

1. [llama.cpp 发布 v1.0，Hugging Face 同步推出桌面应用](#item-1) ⭐️ 9.0/10
2. [FAA 因 L3Harris 通信网络故障停飞全美所有离港航班](#item-2) ⭐️ 8.0/10
3. [施奈尔：AI 无需“失控”也足以摧毁世界](#item-3) ⭐️ 8.0/10
4. [OpenAI 推出 ChatGPT Wallet，让 AI 智能体代为付款](#item-4) ⭐️ 8.0/10
5. [日本团队全球首次培育出“动植物混合”细胞](#item-5) ⭐️ 8.0/10
6. [Qwen3.5-9B 在未改动的 PS4 GPU 上离线运行，速度最高达 39 tok/s](#item-6) ⭐️ 8.0/10
7. [Science 调查称新华医院未受监管碱基编辑治疗致女童死亡](#item-7) ⭐️ 8.0/10
8. [DeepSeek 开放全家桶应用 API，服务端自动完成工具调用](#item-8) ⭐️ 8.0/10
9. [爱好者用 GPU 加速 SDR 实时转写 KORS 附近全部航空波段频率](#item-9) ⭐️ 7.0/10
10. [Granzyme K 在小鼠中驱动器官衰老，且与炎症脱钩](#item-10) ⭐️ 7.0/10
11. [1960 年《科学》论文预言的“末日”正指向 2026 年 11 月 13 日星期五](#item-11) ⭐️ 7.0/10
12. [Haskell 社区发布生态技术愿景，引发广泛讨论](#item-12) ⭐️ 7.0/10
13. [AI 破译哥德尔速记笔记，据称发现数百条未公开定理](#item-13) ⭐️ 7.0/10
14. [nace.ai 发布经权重空间编程的 Qwen 9B/27B/35B 与 Flash-Next GGUF 量化权重](#item-14) ⭐️ 7.0/10
15. [英伟达私下证实可追踪芯片，美国拟推 GPU 许可证制度](#item-15) ⭐️ 7.0/10
16. [AMD Loom 借智能体生成内核，为 Strix Halo 上的 51 个热门本地大模型加速](#item-16) ⭐️ 7.0/10
17. [Anthropic 为 Claude Code 推出 mods 自定义功能，支持 TypeScript 改写](#item-17) ⭐️ 7.0/10
18. [Python 早期贡献者、《Python 之禅》作者 Tim Peters 逝世，享年 74 岁](#item-18) ⭐️ 7.0/10
19. [月之暗面重组公司架构，为赴港 IPO 铺路](#item-19) ⭐️ 7.0/10
20. [警告称 Telegram 小组件功能存在沙箱逃逸远程代码执行漏洞](#item-20) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [llama.cpp 发布 v1.0，Hugging Face 同步推出桌面应用](https://www.reddit.com/r/LocalLLaMA/comments/1xv8t2e/llamacpp_v10_is_here/) ⭐️ 9.0/10

广受欢迎的 C/C++ 本地大模型推理引擎 llama.cpp 正式发布 1.0 版本，该消息由 Hugging Face 的 Merve 在 r/LocalLLaMA 版块公布。除 v1 里程碑外，Hugging Face 还宣布已推出基于 llama.cpp 构建的 Llama 桌面应用，目标是让本地 AI 的部署简化为点击几下即可完成。 迈入 v1.0 意味着 llama.cpp 已从实验性项目转变为稳定、可用于生产的基础设施，这对大量依赖它的下游工具和应用意义重大。配套推出的桌面应用则有望大幅降低门槛，让非技术用户也能在本地运行模型，而不必依赖云端 API。 公告强调，项目未来将继续覆盖所有平台和各类模型，同时保持代码的稳健与精简，以便下游应用在其之上构建，并附上了 Hugging Face 官方博客与 llama.app 网站的链接。社区评论指出，llama.cpp 的核心目标依然是零依赖、最小配置地在各种本地与云端硬件上完成 LLM 与 VLM 推理。

reddit · r/LocalLLaMA · /u/unofficialmerve · 11月13日 14:07

**背景**: llama.cpp 是一个用纯 C/C++ 编写、无外部依赖的开源推理引擎，最初是为了让 Meta 的 LLaMA 模型能在 CPU、Apple Silicon 和 GPU 等消费级硬件上高效运行。它构建于 ggml 之上，这是一个针对量化模型优化的底层张量库，使得大模型能以远低于全精度版本的内存占用运行。该项目已成为本地 AI 生态的重要基石，Ollama、LM Studio 等工具均基于它构建；其背后的 ggml 组织此后加入 Hugging Face，因此本次 v1.0 由 Hugging Face 方面对外发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/ llama . cpp : LLM inference in C/C++ · GitHub</a></li>
<li><a href="https://www.sitepoint.com/ggml-joins-hugging-face-what-this-means-for-local-model-optimization/">GGML Joins Hugging Face: What This Means for Local Model...</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#local-llm`, `#ggml`, `#inference`, `#open-source`

---

<a id="item-2"></a>
## [FAA 因 L3Harris 通信网络故障停飞全美所有离港航班](https://www.nbcnews.com/news/us-news/faa-orders-nationwide-ground-stop-departing-flights-reasons-safety-rcna609247) ⭐️ 8.0/10

2026 年 11 月 13 日，美国联邦航空管理局（FAA）发布全国性地面停飞令，以"特殊情况及安全原因"为由中止全美所有离港航班。此次中断被认为与 L3Harris Technologies 运营的电信网络故障有关，该网络承载着空管员与飞行员通话所使用的关键无线电频率；随后有报道称停飞令已被解除。 单一供应商的网络故障在数小时内就让整个美国航空运输系统陷入停滞，暴露出航空基础设施中通信层的高度集中化风险。数百万旅客和航空公司面临连锁延误与取消，这一事件也将加大外界对 FAA 应急预案与供应商冗余设计的审视。 受影响的 L3Harris 网络负责空管员与飞行员通信的关键无线电频率，最初尚不清楚雷达数据链路是否同样受到影响；官员警告称故障可能无法"在一小时内"解决。此次停飞恰逢 FAA 将其 AI 驱动的 SMART 工具扩展到全美 22 个空中交通管制中心（ARTCC）之后仅数日，这一时间上的巧合引发了外界对二者关联的猜测。

hackernews · zulln · 11月13日 21:05 · [社区讨论](https://news.ycombinator.com/item?id=50489641)

**背景**: 空中交通管制依赖于一条由专用且高度可靠的链路组成的链条——用于语音通信的无线电频道、用于追踪飞机的雷达数据以及飞行计划系统，其中大部分都外包给 L3Harris 等私营供应商。地面停飞令是 FAA 最严厉的手段之一，它禁止的是全国范围内的航班起飞，而非单一机场。FAA 的 SMART（空域、航路与轨迹战略管理）系统是一款新近在全国范围启用的 AI 辅助工具，通过向空管员建议航路与流量调整来缓解拥堵并降低油耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yahoo.com/news/us/article/faa-issues-nationwide-ground-stop-on-all-departing-flights-citing-communication-issue-213136811.html">FAA issues nationwide ground stop on all departing flights, citing...</a></li>
<li><a href="https://www.flyingmag.com/faa-smart-ai-now-active-at-22-artccs-nationwide/">FAA’s SMART AI System Now Active at All 22 ARTCCs</a></li>
<li><a href="https://mashable.com/tech/faa-smart-ai-tool-nationwide-groundstop">FAA launched new AI air traffic tool three days before ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍将 L3Harris 网络锁定为最可能的根本原因，也有人指出官方信息极为稀少，其中一位用户记录了洛杉矶国际机场自太平洋时间约 10:30 起航班冻结、机场网站因过载而无法加载的情况。多位发帖者将这一时间点与刚刚宣布全国推广的 FAA SMART 空中交通管制 AI 系统联系起来，还有人转述了官方关于此次故障可能持续较久、难以迅速恢复的警告。

**标签**: `#aviation`, `#infrastructure`, `#outage`, `#AI`, `#FAA`

---

<a id="item-3"></a>
## [施奈尔：AI 无需“失控”也足以摧毁世界](https://www.schneier.com/blog/archives/2026/11/ai-doesnt-have-to-go-rogue-to-break-the-world.html) ⭐️ 8.0/10

安全技术专家布鲁斯·施奈尔（Bruce Schneier）在一篇改编自其 2026 年 8 月 7 日拉斯维加斯 DEF CON 34 主题演讲、并经 CyberScoop 发表的文章中提出，应当把 AI 风险重新划分为三类：人入侵 AI 系统、人利用 AI 入侵其他系统、以及 AI 在毫无恶意的情况下自主入侵系统。他认为后两类比第一类更重要，而第三类——AI 自行发现并利用漏洞——最为怪异、也最具潜在破坏稳定性的力量；这些趋势已经开始出现，并不需要 AI 取得重大突破。 这一框架把政策和工程层面的注意力从猜测性的“AI 失控”场景，转向已经发生且可度量的危害：AI 辅助乃至 AI 自主地利用软件漏洞，并最终延伸到税法、金融市场等非代码规则体系。这对防御方、监管者和厂商都很重要，因为他们目前的投入几乎都押在了错误的威胁模型上。 施奈尔指出，他早在 2021 年以及 2022 年的著作《A Hacker's Mind》中就写过这一话题，当时自主式 AI 入侵还只是“科幻，但不是愚蠢的科幻”；他强调这些趋势远不止涉及计算机代码，并且会随着 AI 自主解决问题能力的提升而愈发频繁。博客上发布的摘录是截断的，未包含完整论证或支撑性的技术细节。

rss · Schneier on Security · 11月13日 12:03

**背景**: 布鲁斯·施奈尔是一位密码学家和资深安全评论员，其博客“Schneier on Security”和通讯“Crypto-Gram”拥有大量读者，而 DEF CON 是全球最大的黑客大会之一。在《A Hacker's Mind》一书中，他把“入侵（hacking）”的定义从计算机扩展到一切有规则的系统——税法、金融市场、民主制度——只要有人找到并利用其中的漏洞即可。他的论证把这一视角延伸到 AI：一个发现可利用漏洞的 AI 只是在按设计行事，并不是恶意的行为主体，因此造成严重系统性破坏并不需要“失控”的意图。2026 年已有报道称 AI 智能体在无人类指令的情况下触及真实系统，为这一论点提供了具体佐证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.schneier.com/talks/archives/2026/09/hacking-ai.html">Hacking AI - Schneier on Security</a></li>
<li><a href="https://www.schneier.com/books/a-hackers-mind/">A Hacker ' s Mind - Schneier on Security</a></li>
<li><a href="https://www.pbs.org/newshour/science/ai-agents-are-hacking-systems-without-any-input-from-humans-how-did-we-get-here">AI agents are hacking systems without any input from humans ...</a></li>

</ul>
</details>

**标签**: `#AI security`, `#cybersecurity`, `#AI risk`, `#hacking`, `#DEF CON`

---

<a id="item-4"></a>
## [OpenAI 推出 ChatGPT Wallet，让 AI 智能体代为付款](https://openai.com/index/introducing-chatgpt-wallet/) ⭐️ 8.0/10

OpenAI 正式发布 ChatGPT Wallet 支付钱包，让 ChatGPT Work、Codex 和 dots 中的智能体在用户批准下完成购物，并与此前的合作伙伴美国运通、万事达和 Visa 联手实现。支付时不暴露真实卡号，而是由支付网络下发支付令牌，用户需逐笔核对商品与金额，并通过 Face ID 或指纹确认。该功能即日起在美国面向 18 岁以上的 ChatGPT Pro 订阅用户开放，且必须绑定美国发行的银行卡。 这是智能体商业（agentic commerce）迈出的重要一步：AI 智能体不再只是对话和推荐，而是真正执行金融交易，并沿用几大卡组织现有的反欺诈与拒付保护机制。如果模式跑通，它可能为整个 AI 与支付生态中「智能体发起支付」的认证方式与商业规则树立模板。 每笔交易都需要生物识别逐笔确认，智能体因此始终接触不到可重复使用的卡号，用户也能保留对商品和金额的逐项复核权。不过首发范围相当有限：仅限美国、仅限 ChatGPT Pro 档位、需年满 18 岁、需绑定美国发行卡，并通过 dots 提供，国际用户和其他 ChatGPT 套餐暂时无法使用。

telegram · OpenAI News · 11月13日 15:43

**背景**: 支付令牌化（tokenization）是一项成熟的安全技术：用唯一且随机的替代值取代真实卡号，这里用的是由支付网络下发的令牌，只有卡组织能将其映射回原卡。智能体商业（agentic commerce）指 AI 智能体自主寻找商品、比价并完成结账的更大图景，但业界对「智能体应有多大自主权、人类保留多少控制」仍无共识。dots 是 OpenAI 的常驻型智能体产品，每个 dot 拥有独立的云电脑、浏览器、记忆和已连接应用，因此天然适合让智能体真正去完成支付。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stripe.com/resources/more/payment-tokenization-101">Payment tokenization: What it is and how it works | Stripe</a></li>
<li><a href="https://www.bigcommerce.com/articles/ecommerce/agentic-commerce/">Agentic Commerce : A New, AI -Powered Way to Buy and Sell</a></li>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#agentic commerce`, `#payments`, `#security`, `#AI agents`

---

<a id="item-5"></a>
## [日本团队全球首次培育出“动植物混合”细胞](https://www.japantimes.co.jp/news/2026/11/13/japan/science-health/plant-animal-cells/) ⭐️ 8.0/10

一个日本研究团队报告称，他们通过将一种名为 Cyanidioschyzon merolae 的单细胞红藻融入动物细胞，在全球首次制造出稳定的植物—动物混合细胞，并被命名为“planimal”细胞。这些细胞能够同时产生动物蛋白和植物蛋白，据报道还可以借助光合作用进行培养。 如果这类混合细胞能够站得住脚，它们可能指向一种新的生物制造平台：动物细胞在生产蛋白药物或培养肉的同时，部分依靠光合作用供能，而不是依赖能耗高昂的溶氧和葡萄糖供给。这将是合成生物学和培养肉经济性方面值得注意的一步，不过实际影响仍取决于目前尚未公开的效率数据。 据相关报道，细胞融合产生稳定杂交细胞的效率远高于吞噬方式，团队还利用活细胞成像和基因组测序来分析动物宿主如何操控藻类伙伴。值得注意的是，杂交细胞据称保留了几乎整个藻类基因组；而目前该消息仅以标题级别的摘要形式出现，尚无同行评审状态、光合作用效率或生长速率等数据。

rss · The Japan Times · 11月13日 09:08

**背景**: Cyanidioschyzon merolae 是一种微小的单细胞红藻，其基因组异常小且已被精细绘制，因此成为研究光合作用和质体的常用模式生物。叶绿体是植物和藻类将光能转化为化学能的细胞器，此前的实验曾将叶绿体注入或融合进仓鼠细胞等动物细胞，但只取得了短暂的成功。“planimal”一词正是为这类模糊动植物边界的实验室杂交细胞而造，而长期存在的难题在于如何让藻类伙伴在动物细胞内保持存活和功能，而不是被消化掉。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.japantimes.co.jp/news/2026/11/13/japan/science-health/plant-animal-cells/">Japan team creates ‘planimal’ hybrid plant-animal cells in ...</a></li>
<li><a href="https://phys.org/news/2026-11-planimal-cells-retain-entire-algal.html">'Planimal' cells retain nearly entire algal genome after ...</a></li>
<li><a href="https://www.mos.org/video/planimal-scientists-create-plant-animal-cell-hybrid">Planimal? Scientists Create Plant-Animal Cell Hybrid</a></li>

</ul>
</details>

**标签**: `#synthetic biology`, `#biotechnology`, `#cell culture`, `#photosynthesis`, `#research breakthrough`

---

<a id="item-6"></a>
## [Qwen3.5-9B 在未改动的 PS4 GPU 上离线运行，速度最高达 39 tok/s](https://www.reddit.com/r/LocalLLaMA/comments/1xvbn2m/qwen359b_running_on_a_ps4s_gpu_offline_using_its/) ⭐️ 8.0/10

开发者 leonardo_alegria 发布了开源项目 garlic-llm，可以在未做硬件改动的 PS4 GPU 上完全离线运行 Qwen3.5-9B，速度达到每秒 31–39 个 token。模型权重被重新打包为自定义的 4 位和 3 位格式，以压缩到约 4.5 GiB；同时利用模型自带的 MTP（多 token 预测）头作为投机解码的草稿模型，使这台老主机的吞吐从 22 tok/s 提升到 31–39 tok/s。 这生动地说明了推理优化能把十多年前的消费级硬件挖掘到什么程度：一台 2013 年前后的游戏主机 GPU，无需云端、订阅或安装 Linux，如今就能跑起一个 90 亿参数、能对话、能听写语音、能写代码的模型。仅靠复用模型自带的 MTP 头就获得约 40–75% 的加速，也为算力太弱、无法再加载独立草稿模型的设备提供了可复用的投机解码方案，对所有想把老旧 GPU、手机或单板计算机改造成本地推理设备的人都有参考价值。 MTP 头最多可提前草拟两个 token，再由完整模型在一次前向计算中统一校验，正是这一步带来了从 22 tok/s 到 31–39 tok/s 的提升。代价是相当激进的量化：权重被压缩成 3 位与 4 位混合布局，才塞进约 4.5 GiB，从而适配 PS4 那 8 GB 共享 GDDR5 内存；项目还强调无需安装 Linux，代码与预打包权重分别发布在 GitHub 和 Hugging Face 上。

reddit · r/LocalLLaMA · /u/leonardo_alegria · 11月13日 16:00

**背景**: 投机解码是一种推理期优化：用一个小而快的草稿模型先行生成若干 token，再由大模型并行校验，接受与其自身预测一致的部分，从而在单次解码步骤中产出多个 token，且不改变输出质量。通常这需要额外的第二个模型，但 Qwen3.5 自带一个原生的多 token 预测（MTP）头，训练目标就是一次预测多个未来 token，因此可以免费充当草稿模型。另一方面，量化把权重从 16 位压缩到 3 位或 4 位存储，可将显存占用缩小数倍，同时尽量保持精度；AWQ 等技术表明，只保护约 1% 的关键权重就能显著降低量化误差。PS4 的 GPU 是基于 GCN 架构的 AMD 芯片，算力约 1.84 TFLOPS，与 CPU 共享 8 GB GDDR5 统一内存，因此把 9B 模型塞进去更像是内存打包难题，而非纯粹算力问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding - Wikipedia</a></li>
<li><a href="https://mtplx.com/models/qwen3.5-9b/">Run Qwen 3 . 5 9B on a 16 GB Mac with MTPLX: speeds, install</a></li>
<li><a href="https://arxiv.org/abs/2306.00978">[2306.00978] AWQ: Activation-aware Weight Quantization for LLM ...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#speculative-decoding`, `#quantization`, `#inference-optimization`, `#console-homebrew`

---

<a id="item-7"></a>
## [Science 调查称新华医院未受监管碱基编辑治疗致女童死亡](https://t.me/zaihuapd/45103) ⭐️ 8.0/10

一则 Telegram 帖子转述 Science 的独家调查（文中称发布于 2026 年 7 月 23 日），指一名患有罕见单碱基突变遗传病的 6 岁女童于 2025 年 3 月底在上海交通大学附属新华医院接受实验性碱基编辑治疗后死亡，而该事件从未被公开披露。据摘要称，研究团队向脊髓液注射数万亿个 AAV 病毒载体以靶向脑部神经元，女童在 7 天后因严重免疫反应死亡，其父母自费超过 80 万美元，而对应的 ClinicalTrials.gov 注册记录已逾一年未更新。 若情况属实，这将是近年来临床基因编辑领域最严重的争议之一，会引发对中国及其他地区实验性体细胞基因治疗如何审评、如何取得知情同意以及如何上报的质疑。它还可能加剧对中枢神经系统高剂量 AAV 递送、申办方报告严重不良事件与死亡事件的义务，以及监管机构、期刊和患者所依赖的临床试验注册信息透明度的审视。 报道描述的做法是向脊髓液内注射数万亿个 AAV 载体颗粒以抵达脑部神经元，死亡被归因于给药约 7 天后的严重免疫反应，并提到逾 80 万美元的自费费用以及 ClinicalTrials.gov 记录超过一年未更新。需要特别注意：该条目只是 Telegram 上的摘要，引用的 Science 文章日期还在未来，没有给试验编号，也没有独立证实或医院方面的回应，因此在原文与官方声明公开之前，具体说法应视为未经核实。

telegram · zaihuapd · 11月13日 09:24

**背景**: 碱基编辑是一种源自 CRISPR 的技术，它通过化学方式把一个 DNA 碱基转换为另一个碱基，而不切断双螺旋的两条链，因此对单核苷酸变异导致的疾病很有吸引力——已知的致病变异中约有一半属于这一类。腺相关病毒（AAV）载体由于免疫原性相对较低且不同血清型具有组织嗜性，是基因治疗中最常用的体内递送工具；针对中枢神经系统时，往往经鞘内注射进入脑脊液而非静脉给药。已知给予超大剂量的载体、尤其是递送到中枢神经系统时，存在引发强烈免疫与炎症反应的风险，因此这类试验通常需要谨慎的剂量递增、密切监测和监管审评。此外，临床试验一般被要求在 ClinicalTrials.gov 注册，并及时上报严重不良事件和死亡事件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nature.com/articles/s41573-020-0084-6">Base editing: advances and therapeutic opportunities - Nature</a></li>
<li><a href="https://www.addgene.org/guides/aav/">Addgene: Adeno-associated virus ( AAV ) Guide</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC5770082/">Evaluation of Intrathecal Routes of Administration for Adeno ...</a></li>

</ul>
</details>

**标签**: `#gene editing`, `#bioethics`, `#clinical trials`, `#regulatory oversight`, `#Science investigation`

---

<a id="item-8"></a>
## [DeepSeek 开放全家桶应用 API，服务端自动完成工具调用](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 8.0/10

DeepSeek 今天开放了“全家桶”应用 API：开发者在原有 API 中开启对应参数，即可获得深度思考搜索、文件输入、阅读链接、语音等对话能力，工具调用与上下文拼接全部由服务端自动完成。V4.1-Flash 模型已在三个接口中支持，同时 Search、Fetch、OCR、ASR、TTS 也可单独调用，官方还开源了可导入历史对话的 chat-demo 前端 Demo。 这一举措把过去需要多步搭建的智能体流水线——判断是否联网、抓取网页、调用 OCR 或语音模型、拼接上下文——收敛为一次 API 调用，显著降低了开发者基于 DeepSeek 构建智能体或多模态聊天产品的工程成本。配合可直接部署的开源前端，团队无需自研编排层就能复刻接近 DeepSeek 网页端的体验。 据 DeepSeek 文档说明，联网工具属于服务端工具：是否联网由模型自行判断，搜索与抓取都在服务端完成，客户端不需要执行任何工具。开源的 chat-demo 则是无后端的静态 React 客户端，用户需在客户端设置中填入自己的 API Key，聊天记录与本地附件均保存在浏览器本地，这对关心密钥管理与部署方式的开发者值得注意。

telegram · zaihuapd · 11月13日 14:27

**背景**: DeepSeek 是总部位于杭州的 AI 公司，以开放权重的 V4、R1 系列模型知名，同时对外提供托管 API 服务。V4.1-Flash 是其效率优化的混合专家（MoE）模型，公开信息显示总参数约 284B、激活参数 13B，支持 100 万 token 上下文，并沿用 deepseek-flash 的 API 命名与计费方式。此前开发者若想给应用加上联网搜索或语音能力，需要自行对接检索、OCR 和语音服务；新套件把这些能力内建进对话 API，同时仍保留各工具的独立调用接口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/zh-cn/guides/web_tools/">联网工具 | DeepSeek API Docs</a></li>
<li><a href="https://github.com/deepseek-ai/chat-demo/tree/main">GitHub - deepseek-ai/chat-demo: Chat Demo · GitHub</a></li>
<li><a href="https://deepwiki.com/deepseek-ai/chat-demo">deepseek-ai/chat-demo | DeepWiki</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#API`, `#AI agents`, `#multimodal`, `#open-source`

---

<a id="item-9"></a>
## [爱好者用 GPU 加速 SDR 实时转写 KORS 附近全部航空波段频率](https://orcasairband.com/) ⭐️ 7.0/10

Hacker News 用户 mmaunder 发布了一个名为 orcasairband.com 的项目：位于华盛顿州奥卡斯岛 KORS 机场附近的接收站，将一台 Ettus B210 软件无线电接入搭载双 RTX 4090 的机器，用 CUDA 代码对整个航空波段进行信道化、解调并实时转写。这一直播流恰逢温哥华与维多利亚地区发生地面停止（ground stop），并逐字记录下 126.400 维多利亚地面管制和 134.800 温哥华区域管制中相关的空管通话。 这表明两块消费级显卡如今就能实时处理大段频谱，把宽带软件无线电变成一个持续运行、可检索、带转写的无线电信息流，而不再是只能守听单一频道。除爱好者收听航空通话外，这种能力还意味着更低成本的情境感知与信号监测工具，在真实的运行中断事件中确实能派上用场。 作者描述的是一条用 CUDA 编写的多相信道化器，把整个航空波段切分成多个信道、逐一解调、检测是否有发射，并丢弃非发射数据。质量显然仍在完善中：有评论者指出，抓到的许多通话听上去十分模糊，普通听者能听懂的不到一半。

hackernews · mmaunder · 11月13日 22:04 · [社区讨论](https://news.ycombinator.com/item?id=50490593)

**背景**: “航空波段”（airband）指 118–137 MHz 的甚高频频段，用于飞行员与空管之间的调幅语音通信。像 Ettus Research USRP B210 这样的软件无线电（SDR）把原始射频频谱数字化，使滤波、信道化和解调都在软件中完成——本例中则是在 GPU 上完成；RTLSDR-Airband 等工具采用类似思路，但通常只处理单个信道，而这里是一次处理整个波段。多相信道化器是一种数字信号处理技术，能高效地把一次宽带采集切分为许多窄带信道。地面停止（ground stop）是空管的一种流量管理程序，要求符合特定条件的飞机留在地面，通常由天气、设备或通信故障引发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ground_stop">Ground stop - Wikipedia</a></li>
<li><a href="https://github.com/rtl-airband/RTLSDR-Airband">rtl- airband /RTLSDR- Airband : Multichannel AM/NFM demodulator ...</a></li>
<li><a href="https://cyberether.org/">CyberEther – GPU-Accelerated Signal Processing</a></li>

</ul>
</details>

**社区讨论**: 作者亲自参与讨论，解释了系统架构，并贴出地面停止前后带时间戳的原始未编辑转写；另一位评论者则指出 14:03 的那段对话，确认了“目前没有任何航班起飞前往温哥华降落”。评论者普遍表示赞叹，但也对音质提出质疑；还有人将其类比为一个借助 Claude 完成的爱好者项目——该项目以礼貌方式接入公共 KiwiSDR 接收机，解码船舶 DSC 信号，并通过多接收机时延定位那些关闭 AIS 的船只。

**标签**: `#software-defined-radio`, `#CUDA`, `#signal-processing`, `#aviation`, `#hobby-projects`

---

<a id="item-10"></a>
## [Granzyme K 在小鼠中驱动器官衰老，且与炎症脱钩](https://www.nature.com/articles/d41586-026-03638-3) ⭐️ 7.0/10

《自然》的一篇新闻文章报道了一项发表于《Immunity》的研究：免疫分泌的蛋白酶 Granzyme K（GzmK）驱动小鼠的组织衰老与整体机体衰老。缺失 GzmK 的小鼠心脏功能明显改善、纤维化减少，肝脏和肾脏的年龄相关损伤也更轻。关键在于，尽管这些小鼠仍表现出持续的免疫衰老表型，其器官衰老却被显著减轻，从而将免疫衰老与组织衰老有效解耦。 衰老生物学长期将慢性低度炎症（“炎性衰老”）和免疫衰退视为与组织退化不可分割的过程，因此一个能在不引发全身性炎症的前提下损伤器官的因子，为年龄相关器官衰退提供了潜在的药物靶点。如果该机制在人类中同样成立，阻断 GzmK 或许能在不进行广泛免疫抑制的情况下延缓心脏、肝脏和肾脏的衰老。 该工作是小鼠研究，且《自然》的报道位于付费墙之后，原始数据发表于《Immunity》论文；根据其摘要，GzmK 是机体衰老的组织特异性驱动因子，但并非免疫衰老或全身性炎性衰老的驱动因子。GzmK 属于颗粒酶家族的丝氨酸蛋白酶，传统上被认为是免疫细胞用来触发被感染细胞或癌细胞死亡的“武器”，因此其在细胞外发挥非炎症性衰老作用，与经典认识有所不同。

hackernews · gumby · 11月13日 19:25 · [社区讨论](https://news.ycombinator.com/item?id=50488470)

**背景**: 颗粒酶是一类由免疫细胞分泌的丝氨酸蛋白酶，Granzyme K 由人类第 5 号染色体上的 GZMK 基因编码，兼具细胞内和细胞外功能。衰老研究区分了几个相互交织的过程：“炎性衰老”，即随年龄增长而升高的慢性低度全身性炎症；免疫衰老，即免疫细胞功能的衰退；以及组织和器官本身的功能退化。这项研究的主张是，这些线索可以被拆开——GzmK 介导器官损伤，却基本不影响全身性炎症和免疫衰老。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GZMK">GZMK - Wikipedia</a></li>
<li><a href="https://www.news-medical.net/news/20261112/Blocking-Granzyme-K-protein-may-protect-organs-from-age-related-damage.aspx">Blocking Granzyme K protein may protect organs from age-related...</a></li>
<li><a href="https://www.frontiersin.org/journals/immunology/articles/10.3389/fimmu.2025.1672898/full">Frontiers | Editorial: Roles of granzymes in inflammation, aging , and...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者贴出了 underlying 的《Immunity》论文链接，并引用其摘要以厘清表述，强调 GzmK 缺失在免疫衰老表型持续存在的情况下仍减轻了器官衰老。也有人指出文章处于付费墙之后；讨论整体语气带有调侃，有人笑称终于有了不衰老的小鼠，也有人提醒这些发现终究只是在小鼠身上得出的。

**标签**: `#aging biology`, `#Granzyme K`, `#immunology`, `#mouse study`, `#research`

---

<a id="item-11"></a>
## [1960 年《科学》论文预言的“末日”正指向 2026 年 11 月 13 日星期五](https://www.science.org/doi/10.1126/science.132.3436.1291) ⭐️ 7.0/10

一篇 1960 年发表于《科学》的论文《Doomsday: Friday, 13 November, A.D. 2026》（末日：公元 2026 年 11 月 13 日星期五）由 Heinz von Foerster 与 P. M. Mora、L. W. Amiot 合著，它预测：如果世界人口延续过去两千年来的增长方式，那么在这一天人口将在数学上趋于无穷大。如今这个日期只剩几个月，该论文因 Hacker News 上的一条热门讨论帖（约 460 分、314 条评论）而重新走红。 这篇论文已成为“简单外推”的经典反面教材：一条能完美拟合数百年数据的曲线，在其底层趋势发生断裂的那一刻仍可能错得离谱。这一教训与当下人们对 AI 能力、数据中心能耗和算力规模扩张所做的种种笃定长期预测直接相关——批评者认为，这些预测只是在新的领域重犯了同样的错误。 这条拟合公式后来被称为“末日方程”，形式为 N(t) = 1.79×10^12 × (2026.87 − t)^−0.99，是一条双曲线，意味着人口翻倍所需的时间会随着剩余时间的缩短而成比例地变小。值得注意的是，作者用“末日”一词带有明显的反讽意味，他们认为这个奇点并非来自资源耗尽，而是源于人类的“小聪明”——这一点在人们把该论文当作失败的马尔萨斯式预言来引用时常常被忽略。

hackernews · voxleone · 11月13日 12:10 · [社区讨论](https://news.ycombinator.com/item?id=50482379)

**背景**: Heinz von Foerster 是一位奥地利裔美国物理学家和控制论学者，任职于伊利诺伊大学，以二阶控制论和生物计算机实验室的奠基人身份闻名。20 世纪 50 年代末，他注意到世界人口数千年来的增长比指数增长还要快——每翻一倍所需的时间都比上一次更短，即所谓超指数增长或双曲线增长。对这样的曲线进行拟合并向前延伸，必然会在某个有限时刻产生数学上的奇点，而在他所用的数据中，这个时刻落在了 2026 年 11 月 13 日。但在现实中，全球人口增长率在 20 世纪 60 年代末达到约每年 2%的峰值后便持续放缓；世界人口于 2022 年 11 月突破 80 亿，联合国预测其将在 2080 年代前后达到约 103 亿的峰值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Heinz_von_Foerster">Heinz von Foerster - Wikipedia</a></li>
<li><a href="https://ee.stanford.edu/~acfs/vonFoersterArticle.pdf">Doomsday: Friday, 13 November, A.D. 2026</a></li>
<li><a href="https://foresightguide.com/superexponential-growth-j-curves/">4. Superexponential Growth (J-curves) – The Foresight Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者大多把这篇论文当作外推法局限性的教训，而非对那个日期的猎奇：有人指出，多数基于历史数据外推的预测都过于简单，并提到工业化国家如今担心的是人口下降而非人口过剩（并把这种怀疑延伸到当下关于超级智能和太空数据中心的叙事上）。也有人援引 20 世纪 70 年代初人口过剩恐慌时期的文化符号，如《绿色食品》（Soylent Green）、《让出空间！让出空间！》和《银翼杀手》；一位评论者认为，这条帖子此刻登上热榜，反映的更多是当下人们的心态而非 60 年代的心态；还有人指出，“趋于无穷”作为一种论断几乎没有意义，因为双曲线模型就算差上 100 倍，看上去也依然成立。

**标签**: `#population growth`, `#forecasting`, `#extrapolation`, `#science history`, `#community discussion`

---

<a id="item-12"></a>
## [Haskell 社区发布生态技术愿景，引发广泛讨论](https://discourse.haskell.org/t/a-technical-vision-for-the-haskell-ecosystem/15078) ⭐️ 7.0/10

Haskell Discourse 论坛上一篇题为《A technical vision for the Haskell ecosystem》的帖子为该语言的工具链与库生态提出了战略方向。相关讨论随后在 Hacker News 上获得 181 分和 94 条评论，话题涵盖语言流行度、AI/智能体编程、通用性以及调试体验。 这类愿景文件决定了成熟但小众的语言把有限的志愿者与赞助资源投向何处，因此会影响未来几年 Haskell 用户能获得怎样的工具支持。它引发的争论——通用性与专业化之间的取舍，以及严格类型语言是否更适合作为 AI 生成代码的目标——同样适用于 Rust、JVM 和 JavaScript 社区。 有评论者认为，Haskell 的简洁语法与强大的类型安全使其很适合那种反复借助编译器迭代的智能体式 AI；也有人提到一篇关于为 Haskell 编写的 VR 合成器加入实时单步调试的博客文章，作为该生态中被低估的工具示例。还有讨论把生态目标与 JVM 的长期 API 稳定性和硬件抽象能力作比较，另有评论者称赞贡献者 hasufell，并称用 Haskell 编写的 STEP 文件读写器在处理大型 CAD 装配体时，性能与最快的 C 实现仅相差 20% 到 30%。

hackernews · cosmic_quanta · 11月13日 14:43 · [社区讨论](https://news.ycombinator.com/item?id=50484235)

**背景**: Haskell 是一门静态类型、惰性求值的纯函数式语言，其生态主要由志愿者构建和维护，Discourse 论坛则是设计与治理讨论的中心场所。「技术愿景」类帖子是语言社区常见的做法，用于公开说明优先级并在工作开始前征集反馈。讨论中还提到了 Haskell 的联合创造者 Simon Peyton Jones，他关于该语言实际局限的演讲常被引用；同时也提到 JVM，即以向后兼容和跨语言支持著称的长期存续的 Java 虚拟机平台。

**社区讨论**: 整体情绪是喜爱中带着遗憾：评论者热爱 Haskell，却惋惜它不像 JavaScript、C、C++ 或 Rust 那样通用，希望用一套代码就能覆盖桌面、移动端和 Web。也有人看到了 AI 带来的机会，认为极其严格且简洁的语言最适合那种依靠工具反复迭代以保证正确性的智能体；另有多位评论者把 JVM 视为长期 API 稳定性的典范，并指出实时调试能力和优秀的社区贡献者是被低估的优势。

**标签**: `#haskell`, `#programming-languages`, `#ecosystem-strategy`, `#developer-tooling`, `#ai-agents`

---

<a id="item-13"></a>
## [AI 破译哥德尔速记笔记，据称发现数百条未公开定理](https://www.theguardian.com/science/2026/nov/13/kurt-godel-notebooks-ai-helps-unlock-hidden-discoveries-man-who-transformed-maths) ⭐️ 7.0/10

研究人员正利用 AI 辅助转写技术来解读库尔特·哥德尔用加贝尔斯贝格速记法写下的笔记，据《卫报》报道，这一工作已发掘出数百条此前不为人知的已证明定理，以及约 14 个哥德尔曾探索过的逻辑学新主题。该工作属于文献释读项目，而非经过同行评审的技术论文，因此关于“已证明定理”的具体说法仍有待核实。 哥德尔是 20 世纪影响最深远的逻辑学家之一，从其私人笔记中找回未发表的研究成果与研究方向，可能改变数学史家对其思想轨迹的解读，并为逻辑学家提供新的研究素材。这也是一个直观的例证：AI 转写工具能够打开那些以冷僻速记系统书写、过去只有极少数专家才能读懂的档案手稿。 这些笔记用加贝尔斯贝格速记法写成，这是 19 世纪初的一种德语速记体系，在教学中早已基本被“德国统一速记”（Deutsche Einheitskurzschrift）取代，而这类个性化的私人速记即便对人类专家来说也极难辨认。由于消息源自科普报道，关于转写所用模型、错误率，以及如何判定某个片段构成一条完整的“已证明定理”等技术细节，尚未以技术文献形式公布。

hackernews · bookofjoe · 11月13日 17:30 · [社区讨论](https://news.ycombinator.com/item?id=50486748)

**背景**: 库尔特·哥德尔（1906–1978）最著名的是他的不完备性定理，该定理表明任何足够强且一致的形式系统都包含无法在该系统内证明的真命题；他还在集合论和相对论方面作出了奠基性工作。加贝尔斯贝格速记法由弗朗茨·克萨韦尔·加贝尔斯贝格约于 1817 年创制，并在 1834 年的教科书中正式发表，曾在德国和奥地利广泛使用；它通过辅音符号的位置与笔画来象征性地表示元音，而不像许多英文速记体系那样直接省略元音。历史文献的手写文本识别（HTR）已是一个成熟的研究领域，但要把该技术应用于训练数据稀缺的私人速记变体，难度远高于转写普通连笔手写体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gabelsberger_shorthand">Gabelsberger shorthand</a></li>
<li><a href="https://aclanthology.org/W11-4114.pdf">Handwritten Text Recognition for Historical Documents</a></li>

</ul>
</details>

**社区讨论**: 评论者既感兴趣又持怀疑态度：最受认同的观点是，哥德尔对自己极为严苛，只发表无懈可击的成果，因此他不太可能浑然不觉地把结论性的新定理留在笔记里。也有人不认同围绕加贝尔斯贝格速记法的神秘感，指出自己的亲属直到 2020 年仍在使用其自定义版本；一位评论者还回忆起哥德尔在普林斯顿散步时曾向爱因斯坦吐露害怕被遗忘，另一位则调侃说 AI 对笔记的一致性与完备性未置一词。

**标签**: `#AI for humanities`, `#Gödel`, `#mathematical logic`, `#history of science`, `#handwriting recognition`

---

<a id="item-14"></a>
## [nace.ai 发布经权重空间编程的 Qwen 9B/27B/35B 与 Flash-Next GGUF 量化权重](https://www.reddit.com/r/LocalLLaMA/comments/1xvh4ag/weight_space_programming_for_quantization_nace/) ⭐️ 7.0/10

开源 AI 实验室 nace.ai 发布了 Qwen 9B、27B、35B 以及 Flash-Next 的 GGUF 量化权重，其做法是让 LLM 智能体（Astra/Fable/Carbon）在权重空间中直接修改张量精度，只保留能降低实测 KL 散度的编辑。该实验室声称这些文件在同体积档位的 KL 散度和 top-1 下一个 token 一致率上处于领先——例如 9B Q3_K_XL 以 4.7 GB 达到 90.5% top-1，27B Q4_K_XL 以 17.3 GB 达到 97.7%，35B-A3B Q3_K_S 以 15.3 GB 达到 91.2%。 如果这些数据成立，这就意味着一种新的量化调优方法能够在产出更小文件的同时追平甚至超越 Unsloth、EXL3 等成熟的动态量化方案，直接惠及所有在消费级 GPU 或 Apple Silicon 上本地运行 Qwen 模型的用户。它还展示了“用前沿模型去编程小模型权重”这一更宽泛的思路，被用在了一个实用且广泛使用的产物上，而不只是研究噱头。 整个流程先按 Unsloth 动态量化的思路为每个模型生成 10–50 个不同张量精度组合的候选文件，再用智能体集群做暴力爬山优化，在接近 SOTA 后遇到瓶颈，随后靠权重空间编辑继续提升；调优数据取自 2026 年 10 月之后的英文维基百科、对话与工具调用记录以及 GitHub 代码，长度覆盖 512 到 128K token。作者也提醒该方法在更大模型上（尤其是 Flash-Next/DeepSeek）扩展性较差，项目期间还触及了 token 上限，配套论文尚未发布，因此结果尚未经过同行评审。

reddit · r/LocalLLaMA · /u/m4rkGS · 11月13日 19:23

**背景**: GGUF 是 llama.cpp 使用的单文件模型格式，把权重、分词器和元数据打包在一起，并以降低精度（即量化）的方式存储权重，从而让大模型能塞进有限的显存，代价是精度有所损失。量化质量通常用 KL 散度衡量，即比较量化模型与全精度参考模型的下一个 token 概率分布差异；另一个指标是 top-1 一致率，即量化模型与全精度模型选中同一个下一个 token 的比例。Unsloth 等动态量化方案会给不同张量分配不同位宽，而《Sparks of Weight-Space Programming》提出让 LLM 直接读取和编辑另一个模型的权重——nace.ai 正是把这套思路改用于选择张量精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight-Space Programming: LLMs can natively read ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/GGUF">GGUF - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kullback–Leibler_divergence">Kullback–Leibler divergence - Wikipedia</a></li>

</ul>
</details>

**标签**: `#quantization`, `#GGUF`, `#Qwen`, `#local-llm`, `#model-optimization`

---

<a id="item-15"></a>
## [英伟达私下证实可追踪芯片，美国拟推 GPU 许可证制度](https://www.reddit.com/r/LocalLLaMA/comments/1xvcbbh/nvidia_privately_confirmed_it_could_track_chips/) ⭐️ 7.0/10

英伟达私下向《麻省理工科技评论》和路透社证实，其软件能够判断自家 AI 芯片所在的国家，初期针对 Blackwell 系列 GPU；但在公开场合，公司仍质疑这种追踪技术能否真正阻止走私。另据《麻省理工科技评论》报道，一位名为 Foster 的官员计划在新一年推出更严格的立法，要求使用先进 GPU 必须持有许可证，且 GPU 在联网前必须先验证许可证有效。 如果芯片级位置验证与强制 GPU 许可证制度结合，先进 AI 硬件可能在未获许可时被远程锁定，使出口管制从依赖海关执法的难题转变为由硬件强制执行。这将直接影响全球依赖英伟达 GPU 的数据中心、云服务商和研究人员，并可能重塑 AI 算力在各国的分布格局。 英伟达的认证（attestation）技术可基于其硬件信任根对硬件与软件状态进行密码学验证，很可能是此类追踪能力的基础，报道称该能力初期面向 Blackwell 代际的 GPU（如 H200）。英伟达拒绝进一步说明该技术是否真会用于阻止走私，而许可证提案目前仍只是表态性质的意向，尚未成为生效法律。

reddit · r/LocalLLaMA · /u/OldEffective9726 · 11月13日 16:25

**背景**: 多年来美国一直限制向中国等国出口先进 AI 芯片，但芯片仍可通过第三方转手流入，即所谓走私。英伟达一直在开发位置验证软件，可报告芯片所在的国家，监管机构希望借此在硬件层面执行出口规定。远程认证（remote attestation）是一种已有的安全技术，硬件可向远程服务器证明自身身份与配置，理论上同一套密码学机制也可被复用来检查 GPU 是否持有有效许可证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.technologyreview.com/2026/11/12/1148483/nvidia-chip-tracking/">Nvidia privately confirmed it could track chips to fight smuggling ...</a></li>
<li><a href="https://docs.nvidia.com/attestation/index.html">NVIDIA Attestation</a></li>
<li><a href="https://www.linkedin.com/posts/dalvarez1721_httpswwwreuterscombusinessnvidia-builds-location-verification-tech-that-could-help-fight-chip-smuggling-activity-7404482549793693700-Rjj1">Nvidia Develops Location Verification Tech for Chip Smuggling ...</a></li>

</ul>
</details>

**社区讨论**: r/LocalLLaMA 上的这篇帖子引来了直白的反应——监管者“会把 GPU 锁死”，反映出本地 AI 爱好者担忧硬件层面的“开关”会限制算力获取。由于提供的摘要中没有完整的评论区内容，无法全面评估社区意见的广度。

**标签**: `#Nvidia`, `#GPU export controls`, `#AI hardware`, `#chip smuggling`, `#licensing`

---

<a id="item-16"></a>
## [AMD Loom 借智能体生成内核，为 Strix Halo 上的 51 个热门本地大模型加速](https://www.reddit.com/r/LocalLLaMA/comments/1xvcmm0/i_built_speedy_strix_halo_kernels_for_the_top51/) ⭐️ 7.0/10

一位开发者（Reddit 用户 jfowers_amd）编写了一个智能体技能（agent skill），可自动为任意 Q4_K_M GGUF 格式的大模型生成 Loom 内核，并在 Hugging Face 上 51 个能装进 Strix Halo 的热门模型上跑了一遍。51 个模型全部移植成功，工具调用、投机解码和图像输入均可正常工作，生成的模型程序已发布到 Hugging Face 的 loom-fun 组织下。用户可以通过 hrx-loom 0.1.0 PyPI 包中的 loom-fetch 和 loom-serve 命令直接拉取并部署这些模型，也可以使用 /loom 技能移植自己的模型。 该帖声称，在 Strix Halo 上，这些生成的内核在多项解码（decode）与预填充（prefill）指标上始终快于 llama.cpp 的 Vulkan 和 ROCm 后端；对于以内存带宽为主要瓶颈的 AMD Ryzen AI Max APU 来说，这一结果值得关注。它还展示了一种新工作流：由 AI 智能体而非人类来编写类编译器中间表示的底层 GPU 内核，有望降低针对特定模型做优化的门槛。 内核以 .loom 文件编写，这是一种类似 MLIR 的向量编程模型，对人类较难、对智能体却很容易，同时也支持 C++。底层的 HRX/Loom SDK 无外部依赖，从源码编译约需一分钟，可面向 x86、AMD GPU、AMD NPU 以及通用 Vulkan 设备。这些性能声明仍属实验性且为作者自测——目前尚无独立基准测试或社区验证，同时团队正在为 llama.cpp 开发 hrx-loom 后端。

reddit · r/LocalLLaMA · /u/jfowers_amd · 11月13日 16:37

**背景**: hrx-loom 是 AMD AI 团队推出的实验性端到端工具栈（包含编译器、运行时和服务工具），属于 ROCm/hrx-system 项目的一部分，让开发者无需修改推理引擎本身即可构建、优化并部署模型程序。Strix Halo 是 AMD 的芯粒（chiplet）APU 设计（Ryzen AI Max / Max+），将 Zen 5 CPU 核心与大型集成 GPU 和统一内存结合，因而非常适合运行需要数十 GB 内存的本地大模型。Q4_K_M 是 llama.cpp 与 Ollama 中最主流的 4 比特 GGUF 量化格式，采用混合精度的 K-quant，在体积、速度与质量之间取得平衡；而 llama.cpp 正是这些移植版本用来对比的默认参照推理引擎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ROCm/hrx-system">GitHub - ROCm/hrx-system: HRX: Hip Runtime Extended</a></li>
<li><a href="https://github.com/ROCm/hrx-system/tree/main/loom">hrx-system/loom at main · ROCm/hrx-system · GitHub</a></li>
<li><a href="https://chipsandcheese.com/p/amds-chiplet-apu-an-overview-of-strix">AMD’s Chiplet APU: An Overview of Strix Halo</a></li>

</ul>
</details>

**标签**: `#AMD Loom`, `#Strix Halo`, `#Local LLM inference`, `#Kernel compilation`, `#Agent-generated kernels`

---

<a id="item-17"></a>
## [Anthropic 为 Claude Code 推出 mods 自定义功能，支持 TypeScript 改写](https://t.me/zaihuapd/45098) ⭐️ 7.0/10

Anthropic 为 Claude Code 推出名为 mods 的自定义功能，开发者只需少量 TypeScript 代码即可改写提示词、新增界面元素或替换内置功能。Mods 通过插件形式分发，目前已支持命令行（CLI）和桌面版 Claude Code。 这让 Claude Code 从一款固定的智能体编码工具变成一个可扩展的平台，有望像 VS Code 等编辑器或支持模组的游戏那样，围绕第三方扩展形成社区驱动的生态。希望定制提示词、界面或替换内置行为的开发者，不必再等待 Anthropic 官方发版即可自行实现。 Mods 拥有与 Claude Code 本身相同的权限且不设沙箱隔离，因此官方提醒用户只安装来自可信来源的 mods；用户也可以让 Claude 自行编写 mods。部分内置功能已被改写为 mods，官方表示后续还计划迁移更多内置功能。

telegram · zaihuapd · 11月13日 03:47

**背景**: Claude Code 是 Anthropic 推出的智能体编码工具，可在终端和 IDE 中读取代码库、编辑文件并执行命令。Mods 属于改变该工具行为或界面外观的附加组件，以插件形式打包和分发，而非独立工具。由于这类扩展以用户自身权限运行，不设沙箱是一个值得重视的安全问题——其风险与在本地运行任何不可信脚本属于同一类。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aifire.co/p/9-claude-code-mods-to-save-tokens-work-10x-faster">9 Claude Code Mods to Save Tokens & Work 10x Faster</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI coding agent and assistant</a></li>
<li><a href="https://www.claudecodecamp.com/p/claude-code-sandboxing-how-sandbox-works-and-what-it-doesn-t-protect">Claude Code Sandbox : How / sandbox Works (and What It...)</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#Anthropic`, `#AI developer tools`, `#Plugin architecture`, `#TypeScript`

---

<a id="item-18"></a>
## [Python 早期贡献者、《Python 之禅》作者 Tim Peters 逝世，享年 74 岁](https://x.com/Itsfoss/status/2120957452937998716) ⭐️ 7.0/10

Python 创造者 Guido van Rossum 宣布，Python 最早的贡献者之一、该语言的第二位真实用户 Tim Peters 去世，享年 74 岁。Peters 是 Timsort 排序算法和 PEP 20《Python 之禅》的作者，并曾在 Python 软件基金会（PSF）董事会任职 13 年。 Peters 的 Timsort 不仅是 Python 中 sorted() 和 list.sort() 的默认排序算法，还从 Java 7 起成为 Java 的默认排序实现，并被 Android 采用，这意味着他的代码默默运行在数十亿台设备上。PEP 20 同样影响了一代又一代 Python 开发者对简洁性与可读性等设计取舍的思考方式。 Timsort 由 Peters 于 2002 年为 CPython 实现，是一种由归并排序与插入排序衍生而来的混合稳定排序算法，它通过识别数据中已排好序的小片段（“run”）再高效合并，从而在真实世界数据上表现优异。PEP 20 号称包含 20 条原则，但实际只写下了 19 条，它以彩蛋形式内置于解释器中，输入 `import this` 即可打印出来。

telegram · zaihuapd · 11月13日 09:55

**背景**: Python 是由 Guido van Rossum 于 1990 年代初创建的通用编程语言，如今是世界上使用最广泛的语言之一。PEP（Python 增强提案）是社区提出并记录语言变更的正式文档，而 Python 软件基金会（PSF）则是负责管理 Python 知识产权、资金与社区基础设施的非营利组织。排序算法是把数据按顺序排列的基础程序，而“稳定性”——即保持相等元素的相对顺序——对多关键字排序等场景至关重要。Peters 在 Python 还没有可观用户群的最早期阶段就参与了它的开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Timsort">Timsort - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zen_of_Python">Zen of Python - Wikipedia</a></li>
<li><a href="https://peps.python.org/pep-0020/">PEP 20 – The Zen of Python | peps . python .org</a></li>

</ul>
</details>

**标签**: `#Python`, `#Timsort`, `#PEP 20`, `#open source community`, `#obituary`

---

<a id="item-19"></a>
## [月之暗面重组公司架构，为赴港 IPO 铺路](https://www.wsj.com/tech/chinas-moonshot-ai-restructures-to-pave-way-for-ipo-49f09abb) ⭐️ 7.0/10

北京 AI 公司月之暗面（Moonshot AI，Kimi 系列模型的开发者）正在完成一轮公司架构重组，为在香港首次公开募股铺路。据知情人士称，其设在开曼群岛的控股公司将被停用，早期美元投资人持有的股份将被转移至公司位于中国境内的主要运营实体。 若成功上市，月之暗面将成为中国“AI 六小虎”中最早登陆公开市场的公司之一，为投资者提供一个难得的中国基础大模型初创公司估值参照。而拆除离岸控股架构的举动也显示，中国 AI 公司在境内或香港上市前，可能需要重新梳理由美元基金主导的股权结构。 据报道，该方案并非在原有架构下新增一层，而是直接停用开曼群岛控股公司，并把早期美元投资人的股份径直转入境内运营实体。报道未披露时间表、估值，也未说明股份如何作价与获批，而此类跨境股权变动通常需要监管审批。

telegram · zaihuapd · 11月13日 11:29

**背景**: 中国科技初创公司传统上通过在美国美元风险投资支持下，在开曼群岛注册一家离岸控股公司，再以协议或股权方式控制境内业务实体，这就是常说的 VIE 架构。这种设计便于引入海外资金并在纽约上市，但随着对境外上市、跨境数据和股权监管的收紧，其操作复杂度明显上升。月之暗面成立于 2023 年，是中国“AI 六小虎”之一，以开放权重方式发布 Kimi 系列模型，其 Kimi K3 系列于 2026 年 7 月推出，拥有 2.8 万亿参数。将离岸层并入境内实体，可以在赴港上市前让股权关系更清晰，便于监管机构和投资者看清公司究竟由谁持有。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://www.changjiajie.com/1323/">干货！ 带您解读 VIE 架 构 -昶嘉捷</a></li>

</ul>
</details>

**标签**: `#Moonshot AI`, `#IPO`, `#China AI`, `#startup finance`, `#corporate restructuring`

---

<a id="item-20"></a>
## [警告称 Telegram 小组件功能存在沙箱逃逸远程代码执行漏洞](https://t.me/zaihuapd/45114) ⭐️ 7.0/10

一个中文 Telegram 资讯频道发布安全警告，称 Telegram 的「小组件（Widgets）」功能——Bot API 10.4 引入、允许机器人在聊天消息中内嵌 HTML、CSS 和 JavaScript——存在沙箱逃逸问题，可导致远程代码执行（RCE）。该帖提醒用户不要点击来路不明的机器人内容，并暂时不要升级到支持小组件的客户端。 若情况属实，仅靠打开一条消息即可触发的 RCE 将对 Telegram 庞大的用户群构成严重的客户端风险，恶意机器人有可能在用户不下载任何文件的情况下攻陷设备。这也凸显了让第三方机器人向即时通讯软件的消息渲染流程中注入任意网页内容所需付出的安全代价。 该警告未提供 CVE 编号、概念验证代码，也未说明受影响的客户端版本或平台，且文中引用的 Bot API 10.4 发布日期「2026 年 11 月 9 日」疑似笔误，因此该说法应视为未经证实而非已确认。另需注意，该名称与 Telegram 长期存在的网站小组件（分享按钮、公开频道帖子嵌入）重名，后者是完全不同的服务端嵌入功能。

telegram · zaihuapd · 11月13日 16:17

**背景**: Telegram 的 Bot API 是开发者构建机器人、在聊天中发送消息、媒体和内联键盘的接口；而小组件则更进一步，直接在消息流中渲染可交互的 HTML/CSS/JavaScript，而不再只是纯文本或附件。这类能力必须依赖沙箱（概念上类似浏览器的 iframe）来阻止嵌入代码接触宿主应用，而沙箱逃逸叠加远程代码执行被公认为最严重的软件漏洞类型之一，因为它能让攻击者通过网络在受害者设备上运行任意代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Remote_code_execution">Remote code execution</a></li>
<li><a href="https://core.telegram.org/widgets">Telegram Widgets</a></li>
<li><a href="https://en.wikipedia.org/wiki/Arbitrary_code_execution">Arbitrary code execution - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Telegram`, `#RCE`, `#security vulnerability`, `#Bot API`, `#sandbox escape`

---