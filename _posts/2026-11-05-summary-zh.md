---
layout: default
title: "Horizon Summary: 2026-11-05 (ZH)"
date: 2026-11-05
lang: zh
---

> 从 95 条内容中筛选出 19 条重要资讯。

---

1. [Firecracker 快照恢复漏洞致虚拟机逃逸至宿主机（CVE-2026-122192）](#item-1) ⭐️ 9.0/10
2. [OpenAI 流水线发现 948 个 Linux 内核提权至 root 的漏洞利用](#item-2) ⭐️ 8.0/10
3. [月之暗面开源 Kimi K3.1 Pro 权重，定位三万亿参数级开放模型](#item-3) ⭐️ 8.0/10
4. [Go 1.27 正式发布稳定的 encoding/json/v2 与 jsontext 包](#item-4) ⭐️ 8.0/10
5. [Anthropic 发布 FlashProve，让大模型推理结果可被密码学证明](#item-5) ⭐️ 8.0/10
6. [经过十年逆向工程，DOS《银河飞将》实现合作多人模式](#item-6) ⭐️ 8.0/10
7. [数据中心在地方投票中落败，AI 基础设施建设前景蒙上阴影](#item-7) ⭐️ 8.0/10
8. [腾讯以约 70 亿美元向甲骨文租用 10 万枚先进 AI 芯片](#item-8) ⭐️ 8.0/10
9. [OpenAI 发布 ChatGPT Images 2.0：引入推理、联网搜索并大幅改善文字渲染](#item-9) ⭐️ 8.0/10
10. [蓝牙 HDT 随 Core 7.0 落地，LE 峰值速率提升至 7.5 Mbps](#item-10) ⭐️ 8.0/10
11. [博客称白宫网段出现住宅代理出口节点](#item-11) ⭐️ 7.0/10
12. [AI 驱动的漏洞挖掘迫使企业偿还 40 年技术债](#item-12) ⭐️ 7.0/10
13. [Ripple-65B Preview 宣称成为美国开源权重大模型智能体编程 SOTA](#item-13) ⭐️ 7.0/10
14. [腾讯发布 Hy4 开放权重模型，并开源科学伴生模型](#item-14) ⭐️ 7.0/10
15. [AMD 预计第四季度营收将史上首次超越英特尔](#item-15) ⭐️ 7.0/10
16. [研究者披露医疗服务软件中 40 多个漏洞，影响逾 1 亿患者](#item-16) ⭐️ 7.0/10
17. [支付宝联合多方发布中国首个智能体商业信任协议 ACT](#item-17) ⭐️ 7.0/10
18. [华为告知昇腾 960DT 客户自行采购三星、SK 海力士 HBM](#item-18) ⭐️ 7.0/10
19. [苹果将检查 iCloud 公共链接中的有害内容](#item-19) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Firecracker 快照恢复漏洞致虚拟机逃逸至宿主机（CVE-2026-122192）](https://www.reddit.com/r/netsec/comments/1xo0yov/escaping_aws_firecracker_from_guest_userspace_vmm/) ⭐️ 9.0/10

Coinspect 研究团队披露了 CVE-2026-122192：在使用 File 内存后端并带有 balloon 或 virtio-mem 设备的情况下恢复 microVM 快照时，KVM 可能仍引用过期的宿主机虚拟地址范围，恶意 guest 因此可读写 Firecracker VMM 进程内存，实现受控的宿主机代码执行。受影响版本为 Firecracker 0.23.0 至 1.16.1，已在 1.16.2 和 1.17.0+ 中修复。 Firecracker 是 AWS Lambda、Fargate 以及众多多租户无服务器和容器平台所依赖的 microVM 技术，guest 到 host 的逃逸直接突破了这些服务运行不可信代码所依赖的核心隔离边界。自建 Firecracker 且使用快照恢复的部署需要尽快修补，云服务用户则应确认提供商已采取缓解措施。 该漏洞利用需要特定配置：使用 File 内存后端恢复快照，并同时启用 balloon 或 virtio-mem 设备，根源是一次失败的内存重映射操作，而非 KVM 的通用缺陷。AWS 公告和明确的修复版本提供了清晰的修复路径，研究文章则详细介绍了相关内存管理行为和从 guest 用户态到受控宿主机代码执行的完整利用链。

reddit · r/netsec · /u/coinspect · 11月4日 21:47

**背景**: Firecracker 是构建在 Linux KVM 之上的开源 VMM，以极简设备模型运行轻量级 microVM，专为安全的多租户无服务器工作负载设计。每个 microVM 运行在宿主机上的一个 Firecracker 进程中，KVM 负责 CPU 虚拟化和内存映射，将 guest 物理地址转换为宿主机虚拟地址。Firecracker 支持快照与恢复以实现 microVM 快速启动，内存后端决定了 guest 内存的承载与恢复方式。一旦 KVM 对 guest 内存的视图与 VMM 实际使用的内存发生错位，guest 的内存访问就可能变成对宿主机 VMM 进程内存的访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://firecracker-microvm.github.io/">GitHub Pages - Firecracker</a></li>
<li><a href="https://deepwiki.com/firecracker-microvm/firecracker/5.3-memory-backends">Memory Backends | firecracker -microvm/ firecracker | DeepWiki</a></li>
<li><a href="https://github.com/firecracker-microvm/firecracker/blob/main/docs/snapshotting/snapshot-support.md">firecracker /docs/ snapshotting / snapshot -support.md at main...</a></li>

</ul>
</details>

**标签**: `#security`, `#virtualization`, `#firecracker`, `#cve`, `#exploit-research`

---

<a id="item-2"></a>
## [OpenAI 流水线发现 948 个 Linux 内核提权至 root 的漏洞利用](https://openai.com/index/a-thousand-fewer-paths-to-root/) ⭐️ 8.0/10

OpenAI 研究人员披露了一条自主漏洞研究流水线：在 2026 年 10 月对 Linux 内核的一次扫描中，该流水线动态复现了 1,724 个漏洞，并产出 948 个可用的本地提权（LPE）利用程序，使普通用户能够拿到 root 权限，此外还生成了 291 个信息泄露的 PoC。本次运行的总 API 成本约为 121 万美元，平均每个成功的 LPE 利用程序约 1,279 美元。 这表明由大模型驱动的智能体已经能够以远超人类研究团队的规模批量产出经过验证、可利用的内核漏洞，使内核安全的瓶颈从“发现漏洞”转移到“打补丁与分类处置”。由于 Linux 支撑着云主机、Kubernetes 节点、CI/CD 执行环境与容器平台，共享内核中一个未修补的本地提权漏洞就可能让被攻陷的容器演变为对整个宿主机的接管。 该流水线并不只是标记可疑代码：它会动态复现每个漏洞并生成候选补丁，不过文中并未声称每个报告的问题都是独立的新 CVE，也未声称所有补丁都被上游接受。这些利用程序均为本地提权，意味着攻击者必须已经在目标上获得代码执行能力；而每个利用程序约 1,279 美元的成本，说明此类扫描目前的定价更适合资金充裕的机构而非个人研究者。

hackernews · OpenAI News · 11月4日 23:33 · [社区讨论](https://news.ycombinator.com/item?id=50372929)

**背景**: 本地提权（LPE）漏洞指的是：攻击者已经在机器上取得低权限立足点（例如容器内的 shell，或被攻陷的 Web 应用账号）后，进一步获取宿主机内核的 root 权限。Linux 内核自己的威胁模型文档明确列出大量假设，说明内核保护哪些边界、不保护哪些边界，这种模糊性长期是安全争论的焦点。AI 辅助的内核漏洞挖掘正快速兴起：2026 年的多起披露（如 CVE-2026-53264 和 CVE-2026-64300）都出自 AI 驱动的研究，大幅压缩了从发现漏洞到公开利用的时间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.kernel.org/process/threat-model.html">The Linux Kernel threat model</a></li>
<li><a href="https://linuxsecurity.com/features/linux-privilege-escalation-patterns">Understanding Linux Privilege Escalation Patterns and ...</a></li>
<li><a href="https://cybersecuritynews.com/ai-assisted-linux-kernel-zero-day/">AI-Assisted Research Uncovers Linux Kernel Zero-Day Enabling ...</a></li>

</ul>
</details>

**社区讨论**: 评论者的态度在惊叹与不安之间：有人追问内核是如何走到拥有上千条提权路径这一步的，问题出在复杂度、安全模型还是语言实现；也有人表示本地提权一直被视为“必然可行”，但 948 个案例仍令人震惊。有团队成员现身答疑并招聘；还有人追问，既然潜藏着如此多漏洞，互联网、电网等关键基础设施为何仍在运转，并指出分层防御、攻击者需先取得立足点等缓解因素。

**标签**: `#security`, `#linux-kernel`, `#vulnerability-research`, `#privilege-escalation`, `#ai-for-security`

---

<a id="item-3"></a>
## [月之暗面开源 Kimi K3.1 Pro 权重，定位三万亿参数级开放模型](https://huggingface.co/moonshotai/Kimi-K3.1-Pro) ⭐️ 8.0/10

月之暗面在 Hugging Face 上公开了 Kimi K3.1 Pro 的模型权重，这是 K3.1 系列的首款模型，官方称其为目前最强的三万亿参数级开放权重模型。该模型以 Kimi K3 为基础进行大规模联合强化学习后训练，覆盖数百个下游领域，支持 100 万 token 上下文窗口，并同步推出速度约为标准版 2 至 3 倍的 Highspeed 版本。 如此规模的准前沿开放权重模型，为自托管用户和推理服务商在编程与智能体任务上提供了可替代闭源 API 的选择，而多家第三方托管方在数小时内陆续上线，说明价格与吞吐竞争已经开始。这也让它与 DeepSeek、Qwen 等最新开源前沿模型之间的对比竞争更加激烈。 该模型支持 100 万 token 上下文，重点面向编程、三维创作、金融研究、事实准确性和智能体任务；官方给出的 Terminal-Bench 4.0 得分为 65.7%，高于其引用的 GPT-6 Astra 的 58.2%，并接近 Claude 的水平。在本地运行完整权重对个人用户而言几乎不可行，有评论者估算需要 8 块 B300 级别的节点，因此多数用户会通过托管端点来使用它。

hackernews · abrarthought · 11月4日 15:30 · [社区讨论](https://news.ycombinator.com/item?id=50366999)

**背景**: 所谓开放权重，是指训练好的参数可以被下载，任何人都能自行托管、微调，或通过第三方推理服务商调用，这与只能经由厂商 API 访问的闭源模型不同。对于如此大规模的模型，自托管需要多 GPU 的服务器级集群，于是 OpenRouter、Together、Modal、Fireworks 等推理服务商形成一个细分行业，托管权重并在吞吐与价格上展开竞争。月之暗面、DeepSeek 以及阿里 Qwen 等中国实验室的开放权重发布，已成为大模型生态中的常见现象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3.1-Pro">moonshotai/Kimi-K3.1-Pro - Hugging Face</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-1-pro-quickstart">Kimi K3.1 Pro - Kimi API Platform</a></li>
<li><a href="https://blogs.novita.ai/inference-api-providers-for-open-source-models/">Top Inference API Providers for Open -Source Models in 2026 - Novita</a></li>

</ul>
</details>

**社区讨论**: 评论普遍认为该模型很强，但尚未达到真正的前沿水平：有人称它并没有明显超越 DeepSeek V4.1 Flash，还有人批评其“榜单刷分”；不过也有测试者持不同意见，表示自己的评测并未发现刷分现象，并认为它在多数场景下表现出色。最集中的现实抱怨是硬件成本，多位用户提到 OpenRouter 等第三方托管方，并指出在相同价格下 Together 的吞吐量大约是月之暗面自家端点的两倍。

**标签**: `#LLM`, `#open-weights`, `#AI/ML`, `#model-release`, `#inference`

---

<a id="item-4"></a>
## [Go 1.27 正式发布稳定的 encoding/json/v2 与 jsontext 包](https://go.dev/blog/jsonv2) ⭐️ 8.0/10

经过数年的实验与打磨，Go 团队宣布 encoding/json/v2 以及更底层的 encoding/json/jsontext 包已在 Go 1.27 中稳定并正式可用。此次发布同时更新了博客文章，说明原 encoding/json 的不足，并提供了从 v1 安全迁移到 v2 的正式迁移指南。 encoding/json 是 Go 生态中被引入次数最多的包之一，因此对它的重新设计几乎会影响每一个涉及数据序列化的 Go 服务、命令行工具和库。新 API 旨在解决长期以来在性能、正确性和可配置性方面的抱怨，而整个生态需要在接下来的发布周期中决定是否迁移、以及迁移得多快。 这次重构将职责拆成两层：jsontext 负责 JSON 文本的词法级 token 与字节处理，json/v2 则实现 JSON 与 Go 值之间的语义映射。迁移明确是可选的——迁移指南强调你并不一定需要迁移——但 v2 在 nil 切片编码、字段名大小写敏感匹配、UTF-8 严格性以及重复键处理等方面改变了行为，因此依赖 v1 特殊行为的代码必须经过审查。

hackernews · olexsmir · 11月4日 17:52 · [社区讨论](https://news.ycombinator.com/item?id=50369106)

**背景**: JSON（JavaScript Object Notation）是服务之间交换数据以及编写配置文件时事实上的文本格式，而 Go 的 encoding/json 包自语言早期起就是在 JSON 与 Go 结构体之间转换的标准方式。原始包更注重简洁与安全而非速度，随着时间推移，用户开始要求诸如流式 token API、可定制的字段命名与省略规则以及更好的性能，而这些只有第三方库能零散提供。Go 团队最初把 v2 设计作为实验、放在构建标志之后发布，在收集社区反馈后才敲定最终的稳定 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://go.dev/blog/jsonv2">A new Go API for JSON - The Go Programming Language</a></li>
<li><a href="https://go.dev/doc/jsonv2-migration">encoding/json/v2 Migration Guide - The Go Programming Language</a></li>
<li><a href="https://github.com/golang/go/discussions/63397">encoding/json/v2 · golang go · Discussion #63397</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎这次重构：一位生产环境用户称赞 jsontext 能在保持极佳速度的同时给出针对每类错误的精确报错，另一位则抱怨移除 MarshalIndent 之类的辅助函数让常见任务和迁移变得不必要地麻烦。讨论中反复出现的观点是 JSON 看似简单实则复杂——否则每种语言早就把它解决了——此外还有人对基于 schema 特化的 SIMD 风格解析器很感兴趣，一位资深开发者则指出如今 Go 代码越来越多是由大模型而非手写完成的。

**标签**: `#Go`, `#JSON`, `#API design`, `#standard library`, `#programming languages`

---

<a id="item-5"></a>
## [Anthropic 发布 FlashProve，让大模型推理结果可被密码学证明](https://www.anthropic.com/research/provable-inference) ⭐️ 8.0/10

Anthropic 公布了在“可证明推理”方向上的进展，发布了一个名为 FlashProve 的研究原型：它基于 zkSNARK，能够生成密码学证明，证实某段回复确实由指定的模型生成，并在一个 400B 参数的开源混合专家模型（Llama 4 Maverick）上做了演示。公司将其定位为研究里程碑而非即将上线的产品功能，该帖子也在 Hacker News 上引发了关于成本、信任假设与署名归属的大量讨论。 目前 API 客户无法验证响应请求的模型是否真的是宣称的那套权重——服务商可能悄悄换成更便宜或量化过的模型，甚至把流量路由到别处。可证明推理让这一承诺变成客户可以用数学方式检验的东西，这对受监管行业、模型归属声明以及建立在商用大模型 API 之上的审计与合规流程都具有重要意义。 据报该原型的 GPU 开销约为普通推理的 72 倍（社区成员提到某些配置下达到 90–100 倍）；客户端需要下载约 6.5 MB 的承诺值，该承诺值大约可支撑 1600 万次请求，之后服务商必须重新承诺；每个请求附带一个证明，校验一个证明在 24 线程上约需 17 秒（单线程 21 秒）。目前没有部署计划，而且该证明只能证明“哪套权重被执行了”，并不能证明输出内容正确、安全或未被后处理修改。

hackernews · ltononro · 11月4日 17:17 · [社区讨论](https://news.ycombinator.com/item?id=50368626)

**背景**: zkSNARK 是一种密码学证明：它能在不让验证方重算整个计算、也不泄露私有输入（在这里是模型权重，某些设计下还包括提示词）的前提下，证明某个计算被正确执行。把它用在 LLM 上非常困难，因为 Transformer 推理对应的电路规模极其庞大（数十亿次乘法），历史上开销高出几个数量级而难以实用。像 Meta 的 Llama 4 Maverick 这样的混合专家（MoE）模型每个 token 只激活一部分参数，这也是为什么 400B 规模的模型会成为此类演示的可行目标之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/provable-inference">Progress on provable inference for large language models</a></li>
<li><a href="https://shattered.io/anthropic-flashprove-provable-inference-72x-overhead-2026/">Anthropic FlashProve: Provable Inference at 72x [2026]</a></li>
<li><a href="https://blockchain.news/news/anthropic-provable-inference-flashprove-llama-4-maverick">Anthropic reports progress on provable inference for large ...</a></li>

</ul>
</details>

**社区讨论**: 讨论氛围是“有兴趣但存疑”。一位评论者（neuwirth）公开质疑署名，称该工作建立在他早前的 VerInf 研究之上，连选用 400B Maverick 模型这一决定也来自他的工作却几乎没有致谢；另一些人认为 72 倍开销是错误的取舍，指出对开源权重模型来说，直接确定性地重跑一遍计算即可，而让四家彼此独立的推理服务商运行同一个非批处理提示词，可以得到成本低得多的概率性保证。评论者还提到其现实价值——能够发现服务商悄悄把请求路由到别的模型——但同时也质疑：若不开放权重，信任问题恐怕永远无法彻底解决。

**标签**: `#provable inference`, `#LLM verification`, `#cryptography`, `#AI trust`, `#zero-knowledge proofs`

---

<a id="item-6"></a>
## [经过十年逆向工程，DOS《银河飞将》实现合作多人模式](https://fireflyk64.github.io/wcmulti/) ⭐️ 8.0/10

经过十多年的内存探测，作者和他的兄弟通过定位 64KB 数据段中的游戏状态变量、向游戏函数注入调用并在网络上同步状态，为原版 DOS《银河飞将》实现了合作多人模式，使两人可以一起执行剧情任务。 这表明深度逆向工程可以在没有源代码的情况下为经典游戏添加现代多人功能，延长 1990 年代作品的生命周期，并为游戏保存和遗留代码研究提供可借鉴的技术路径。 该项目依靠走走停停、转向和通信等实验来测绘内存并注入调用，作者最喜欢的发现是摄像机状态位于实体结构中。评论区还有人询问为什么语音流量走数据通道而不是 RTC 流，这凸显了该模组中的网络设计取舍。

hackernews · daniel_rh · 11月4日 18:51 · [社区讨论](https://news.ycombinator.com/item?id=50369895)

**背景**: 《银河飞将》（Wing Commander）是 1990 年推出的 DOS 太空战斗模拟游戏，玩家在 TCS Tiger's Claw 号母舰上执行各种任务。那个年代的 DOS 游戏运行在实模式下，内存采用分段管理，修改者常通过观察内存中数值的变化来逆向分析程序。这个项目正是利用这类技术定位游戏状态、修补函数调用，并在网络上同步两名玩家的游戏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.moddb.com/games/wing-commander">Wing Commander DOS game - ModDB</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞这篇详细的技术写作，并分享了对此前《银河飞将》以及 8 位机时代通过磁盘/内存修改作弊的怀旧回忆。有人提出技术问题：为什么语音流量走数据通道而不是 RTC 流；作者则说明项目始于 2015 年发现游戏状态可以放入 64KB 数据段。

**标签**: `#reverse-engineering`, `#retro-gaming`, `#DOS`, `#memory-hacking`, `#networking`

---

<a id="item-7"></a>
## [数据中心在地方投票中落败，AI 基础设施建设前景蒙上阴影](https://stratechery.com/2026/ai-on-the-ballot/) ⭐️ 8.0/10

在题为《AI on the Ballot》的 Stratechery 文章中，Ben Thompson 指出，数据中心项目被纳入地方选举投票，并以“重大方式”落败。他由此提出一个战略性问题：如果美国民众对建设这类基础设施的反对是长期性的而非一时挫折，这对 AI 产业意味着什么。 AI 能力依赖于大规模实体建设——园区、电力与输电线路——因此，如果地方阻力成为一种持久的政治约束而非短暂的“邻避”阶段，就可能拖慢 AI 发展节奏，并把竞争优势转向那些能够搞定选址与能源的企业或地区。这一框架对整个科技生态都很重要，因为审批与土地使用政治可能变得和芯片供应一样具有决定性。 公开可见的摘要非常简短，只有一句话说明数据中心被列入投票并大幅落败，外加一个关于“永久性反对”的设问；完整论证位于 Stratechery 的付费墙之后。值得注意的是，该分析把选址政治——而非算力、模型或资本——视为 AI 进展潜在的硬性约束。

rss · Stratechery · 11月4日 11:00

**背景**: Stratechery 是 Ben Thompson 的付费订阅通讯，也是被广泛阅读的科技战略分析来源之一，以其“聚合理论”和平台商业框架而具有影响力。数据中心是云计算与 AI 训练、推理的物理骨架，消耗大量电力与水，并需要大片土地，因此经常成为地方区划争议的焦点。“NIMBY”（“不要建在我家后院”）指居民对周边开发项目的反对，近年来因电网负荷、噪音和税收优惠等担忧，越来越多地被用于数据中心项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stratechery.com/">Stratechery by Ben Thompson – On the business, strategy, and...</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#tech policy`, `#NIMBY`, `#Stratechery`

---

<a id="item-8"></a>
## [腾讯以约 70 亿美元向甲骨文租用 10 万枚先进 AI 芯片](https://t.me/zaihuapd/44912) ⭐️ 8.0/10

腾讯与甲骨文签订了一份价值约 70 亿美元、为期五年的租约，租用约 10 万枚其在中国境内无法合法购买的先进 AI 芯片，这是腾讯迄今规模最大的海外租赁交易。相关算力将部署在东南亚多个数据中心，用于加速腾讯的 AI 模型与智能体（Agent）工具开发，其中约 30%的款项需要预付。 这笔交易表明，中国 AI 巨头正越来越多地通过海外租用算力来绕过美国出口管制，而不是直接采购芯片，实际上把云租赁变成了硬件进口的替代方案。如此规模的租约还说明，中国的前沿级 AI 训练可能已开始依赖境外数据中心，这将对算力成本、数据主权以及美国后续规则制定产生影响。 这一安排恰恰利用了美国规则的漏洞：中国企业被禁止购买英伟达 H100、H200、B200 等先进芯片，但允许在海外云数据中心租用。约 30%的预付款意味着在任何算力交付前就需投入大量现金，而把芯片物理上留在中国境外则可避免违反出口管制。

telegram · zaihuapd · 11月4日 11:01

**背景**: 自 2022 年以来，美国政府持续收紧对先进 AI 加速卡的出口管制，使中国企业无法获得英伟达顶级的 Hopper 与 Blackwell 世代 GPU，而这些芯片正是大模型训练的主力。英伟达的 H100、H200（Hopper 架构）与 B200（Blackwell）主要在显存容量、带宽和算力吞吐上有差异，每一代的单芯片性能都大幅提升。由于中国企业仍可通过海外云服务商远程使用这些 GPU，把硬件放在东南亚数据中心并通过网络访问，已成为获取前沿算力的重要渠道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://t.me/OneMillion_AI/5683">动察Beating AI News – Telegram</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/1984367989412344349">一文读懂英伟达四大旗舰显卡差异：H100/H200/B200/B300</a></li>
<li><a href="https://introl.com/blog/h100-vs-h200-vs-b200-choosing-the-right-nvidia-gpus-for-your-ai-workload">H100 vs H200 vs B200: NVIDIA GPU Comparison | Introl Blog</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#export controls`, `#Tencent`, `#Oracle`, `#chip shortage`

---

<a id="item-9"></a>
## [OpenAI 发布 ChatGPT Images 2.0：引入推理、联网搜索并大幅改善文字渲染](https://t.me/zaihuapd/44923) ⭐️ 8.0/10

OpenAI 发布了基于 GPT Image 2 的图像生成模型 ChatGPT Images 2.0，首次在架构中引入原生“思考能力”，使其能够在生成前对提示词进行逻辑推理并联网搜索。该模型可依据单一提示词一次性生成最多 8 张视觉一致的连续图像，覆盖漫画、UI 元素与营销素材等复杂构图，最高支持 2K 分辨率，同时显著改善了 AI 绘图长期存在的拼写难题，尤其是中文、日文、韩文等非拉丁语系的文字渲染。 这是 OpenAI 首个内置推理能力的图像模型，意味着图像生成正从“一次性出图”转向类似智能体的工作流：模型先规划、先查资料，再动手绘制。非拉丁文字准确性的跃升，对中日韩等市场的设计师、营销人员和创作者影响最大——过去由于模型常常把本地文字画错，他们不得不依赖后期修图。 据报道，多图一致性是在单一提示词内一次性产出最多 8 张画面，并可输出适合设计与营销使用的 2K 图像。该消息来自 Telegram 频道摘要，因此确切的模型命名、API 可用性与定价细节尚未在摘要中得到确认，建议以 OpenAI 官方文档为准。

telegram · zaihuapd · 11月4日 23:42

**背景**: GPT Image、Imagen、Flux 等现代图像生成模型通常是一次性从文本提示直接出图，这使得多步骤版式和小字号文字极易出错。推理模型则不同，它会在给出结果前先生成中间“思考”内容，而 OpenAI 现在把这一范式搬到了图像上，让模型可以先规划构图，甚至先联网查清需要描绘的事实。中文、日文、韩文等非拉丁文字的渲染尤其困难，因为这些书写系统包含数千个字符，需要字形级别的精确，而不仅是“看起来像”的笔画。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.buildfastwithai.com/chatgpt-images-2-0-gpt-image-2-2026">ChatGPT Images 2.0: Full Developer Breakdown (2026)</a></li>
<li><a href="https://www.engadget.com/ai/chatgpt-images-20-is-better-at-rendering-non-latin-text-190000153.html">ChatGPT Images 2.0 is better at rendering non-Latin text</a></li>
<li><a href="https://kolbo.ai/blog/multilingual-text-in-ai-images">Non-Latin Text in AI Images: Which Models Actually Work ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#image-generation`, `#multimodal-AI`, `#text-rendering`, `#product-release`

---

<a id="item-10"></a>
## [蓝牙 HDT 随 Core 7.0 落地，LE 峰值速率提升至 7.5 Mbps](https://www.bluetooth.com/press/bluetooth-high-data-throughput-opens-a-new-chapter-in-wireless-performance/) ⭐️ 8.0/10

11 月 4 日，蓝牙技术联盟（SIG）宣布正式采纳 Bluetooth HDT（High Data Throughput，高数据吞吐量）特性，将蓝牙低功耗（LE）的最高支持比特率从 2 Mbps 提升至 7.5 Mbps，接近原来的四倍，同时改善了容量、能效与可靠性。HDT 是近期通过的蓝牙 Core 7.0 规范中的可选特性，其首个标准化应用场景为支持无损与高解析度播放的高端无线音频，相关产品预计于 2027 年初上市。 峰值速率约 4 倍的提升，让蓝牙低功耗首次拥有承载无损与高解析度音频的带宽余量，而这一场景此前往往需要借助 Wi-Fi 或私有编解码方案。由于该特性属于核心规范的一部分，它可能改变真无线耳机、智能手表和智能家居设备的设计方式，以及它们与基于 Wi-Fi 的替代方案之间的竞争格局。 HDT 引入了一个新的射频层，即新的 PHY（物理层），可在同一信号中承载更多数据；它作为可选特性可与旧设备共存，从而实现向后兼容。问题在于连接的两端都需要新硬件才能使用，这也是首批支持 HDT 的产品要到 2027 年初才会出现的原因。

telegram · zaihuapd · 11月5日 01:39

**背景**: 蓝牙低功耗（LE）是蓝牙中面向低功耗场景的分支，广泛用于耳机、可穿戴设备和传感器，其此前的最高射频模式 2M PHY 将原始比特率限制在 2 Mbps，实际吞吐往往更低。PHY（物理层）是定义比特如何调制到空口上的最底层射频配置，因此增加一个更快的 PHY 正是 SIG 在不放弃现有协议栈的前提下提升速率的方式。蓝牙核心规范是所有可互操作的蓝牙设备都必须实现的母文档，每一个带编号的版本（如 Core 7.0）都会加入新的可选特性，由厂商按自己的节奏采纳。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techpowerup.com/354478/bluetooth-sig-announces-bluetooth-high-data-throughput">Bluetooth SIG Announces Bluetooth High Data Throughput</a></li>
<li><a href="https://www.howtogeek.com/bluetooth-hdt-makes-your-devices-faster-and-richer-but-it-needs-new-hardware/">Bluetooth HDT will finally give smartwatches and earbuds the ...</a></li>
<li><a href="https://www.bluetooth.com/wp-content/uploads/Files/Specification/HTML/Core_v7.0/out/en/index-en.html">Bluetooth Core Specification</a></li>

</ul>
</details>

**标签**: `#Bluetooth`, `#wireless standards`, `#HDT`, `#lossless audio`, `#connectivity`

---

<a id="item-11"></a>
## [博客称白宫网段出现住宅代理出口节点](https://layer3intel.com/blog/residential-proxies-white-house-network) ⭐️ 7.0/10

安全博客 Layer3Intel 发布分析文章称，有住宅代理出口节点似乎运行在登记于白宫名下的 IP 网段中，并指出约一半的观测活动集中在美东时间下午 5 点至午夜，凌晨几乎为零。文章认为这种时间分布更像网络中某台个人设备被植入了代理 SDK，而不是公共访客 Wi-Fi 网络。 如果属实，一台位于高价值政府网络中的被感染设备将成为值得关注的供应链与终端安全隐忧，因为住宅代理流量可能为外部人员提供进入敏感环境的立足点。此事也凸显仅凭 IP 与 ASN 数据做归因仍然非常困难，这对从事网络取证和威胁情报的人来说是一个重要议题。 文中给出的证据仅限于 IP 网段归属和流量时间分布，并未指向任何具体设备、用户或物理位置，而且该博文同时也在宣传这家公司自己的检测服务。作者本人也承认，这些数据“显示的是出口，而非背后的设备或人”，同一 IP 段也可能服务于实验室、访客网络或媒体工作区。

hackernews · Rasbora · 11月4日 20:45 · [社区讨论](https://news.ycombinator.com/item?id=50371246)

**背景**: 住宅代理网络会把客户的流量经由普通消费者的宽带线路转发出去，使流量看起来来自真实的家庭或办公 IP 地址，因此比数据中心代理更难被封堵。这类网络通常有三种搭建方式：把代理 SDK 打包进免费应用、游戏或工具中以换取共享带宽；带宽共享计划；或者通过恶意软件控制路由器与物联网设备。由于出口 IP 属于真实机构，防守方在做归因时只能把 IP 归属当作线索，而不能当作流量真实来源的证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fbi.gov/investigate/cyber/alerts/2026/evading-residential-proxy-networks-protecting-your-devices-from-becoming-a-tool-for-criminals">Evading Residential Proxy Networks: Protecting Your Devices ...</a></li>
<li><a href="https://ipgeolocation.io/blog/how-residential-proxy-detection-works">Residential Proxy Detection: How It Works & Why It's Hard</a></li>
<li><a href="https://decodo.com/blog/how-residential-proxies-work">How Residential Proxies Work: A Technical Guide to Types...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论（726 分、231 条评论）总体持怀疑态度：多位评论者指出，该文只确认了 IP 网段的归属者，有人更直言作者是在为上线仅一周的服务做宣传，并认为这些流量也可能来自安全实验室或媒体访客网络。另一些人认为更值得担忧的是此类设备自带潜在的指挥与控制通道，日后可能被派发更有害的任务，这与政界人士把手机带入 SCIF 的报道相呼应；还有评论者表示，约二十家主要住宅代理服务商中大概只有一家算是正经生意。

**标签**: `#security`, `#privacy`, `#residential-proxies`, `#network-forensics`, `#supply-chain`

---

<a id="item-12"></a>
## [AI 驱动的漏洞挖掘迫使企业偿还 40 年技术债](https://spectrum.ieee.org/ai-in-cybersecurity-php2shell-vulnerability) ⭐️ 7.0/10

IEEE Spectrum 的一篇分析文章指出，AI 驱动的安全工具正在以远超企业消化速度的节奏，在广泛部署的软件中发现遗留漏洞，实际上迫使整个行业直面积累了约四十年的技术债。文章将这一变化描述为从零散、以人力节奏进行的漏洞挖掘，转向持续的、机器规模的代码审计。 如果 AI 能够大规模审计代码，那么“总会有别人审查过”这一开源软件安全性的长期假设，将从一种信念变成可被检验的事实，从而动摇现代软件供应链信任的根基。这也意味着防御方要承担一项与功能无关的强制修复工作量——投入工程能力却无法交付任何新东西。 讨论中强调，被暴露出来的许多问题并不是靠范围极窄的“差一错误”式补丁就能解决，而是需要重构或重新设计，因此修复成本取决于架构层面的债务，而非漏洞发现的数量。这篇文章属于分析性评论，而非披露某一个具体漏洞，其核心不确定性在于：这究竟会是一次性的集中清理，还是会变成永久性的修复跑步机。

hackernews · pseudolus · 11月4日 11:52 · [社区讨论](https://news.ycombinator.com/item?id=50364336)

**背景**: 技术债是指在软件开发过程中走捷径所导致的未来成本——临时补丁、过时的依赖项、缺乏文档的设计决策，它们让后续修改更加困难，并在安全层面给生产系统留下潜在弱点。过去，发现这些弱点依赖稀缺的人工审计人员，因此大多数代码（尤其是由志愿者维护的开源项目）从未被深入审查过。AI 漏洞管理工具通过为分析增加上下文和规模，改变了这种审查的成本结构，这也是为什么几十年未修的问题会突然集中浮现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Technical_debt">Technical debt - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/technical-debt">What is technical debt? - IBM</a></li>
<li><a href="https://www.rapid7.com/fundamentals/ai-vulnerability-management-platform/">AI-Driven Vulnerability Management Platform Explained - Rapid7</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同 AI 审计会带来大量阵痛，但对它究竟算不算真正的“还债”，还是变成一台强制性的、与功能无关的修复跑步机，意见分歧明显。有人对此表示欢迎，认为它终于让“代码会被他人审查”这一开源承诺落到实处，并指出“肯定有人审计过”的想法只是一种虚假的安全感；也有人引用《哥德尔、埃舍尔、巴赫》的观点，认为任何系统在理论上都不可能做到完全安全。

**标签**: `#AI`, `#cybersecurity`, `#technical debt`, `#open source`, `#vulnerability management`

---

<a id="item-13"></a>
## [Ripple-65B Preview 宣称成为美国开源权重大模型智能体编程 SOTA](https://www.ricursive.com/ripple) ⭐️ 7.0/10

Ricursive Intelligence 发布了 Ripple-65B Preview，这是一个端到端训练的 65B 参数稠密（dense）大语言模型，公司称其在美国开源权重模型的智能体编程基准上创下新的 SOTA，并同时提供 NVFP4 量化版本和 DFlash2 投机解码草稿模型等配套产物。公司声称该模型超越了此前美国开源权重的发布成果，但公告中并未直接点名被其击败的竞品模型。 美国实验室大多将前沿模型保持闭源，因此一个在智能体编程领域可信的美国开源权重模型，对那些被限制使用 Qwen、DeepSeek 等中国开源模型的开发者和机构来说意义重大。如果这一声明站得住脚，它将在开源发布由中国实验室主导的当下，为开源权重生态补充一个在司法管辖上更安全的选择。 社区成员指出，Ripple-65B 在 Terminal Bench 2.1 上得分 80.5，而规模更大（但因采用 MoE 架构、推理成本可能更低）的 Qwen 3.8 Flash Next 约为 84.3，Qwen 3.8-27B 为 73.0。由于它是 65B 稠密模型，在消费级硬件上运行很可能不切实际；该发布还包含 NVFP4 量化版本以及用于提升推理效率的投机解码草稿模型。

hackernews · Philpax · 11月4日 18:53 · [社区讨论](https://news.ycombinator.com/item?id=50369925)

**背景**: 开源权重模型会公开训练好的参数，供他人下载并在本地运行，这与只能通过 API 访问的闭源模型形成对比。智能体编程指 AI 系统自主规划并执行多步骤软件任务（如编写、调试和测试代码），通常用 Terminal Bench 这类模拟真实命令行工作流的基准来评估。稠密模型对每个 token 都会激活全部参数，因此 65B 稠密模型在本地部署时的成本远高于同等或更大总参数量的混合专家（MoE）模型。发布 NVFP4 量化版本和投机解码草稿模型，分别是降低推理显存占用和降低延迟的常见手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/ricursive-intelligence_today-we-release-ripple-65b-preview-a-65b-activity-7523812868476305409-dRxz">Today we release Ripple-65B Preview, a 65B dense LLM we ...</a></li>
<li><a href="https://huggingface.co/ricursiveAI/Ripple-65B-Preview-DFlash2">ricursiveAI/Ripple-65B-Preview-DFlash2 · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>

</ul>
</details>

**社区讨论**: 评论者对“SOTA”这一说法持怀疑态度，认为通过不断缩小比较范围，直到它只意味着“某一规模下美国产开源模型中的最佳”，这个词已被稀释。也有人欢迎又多了一个有竞争力的开源权重模型，但质疑其实用性：相比 Qwen 的 27B 级别模型和 MoE 模型，65B 稠密模型对爱好者和本地推理而言太慢；同时批评公告没有点名其所对比的开源权重模型。

**标签**: `#LLM`, `#open-weight`, `#agentic-coding`, `#benchmarking`, `#Hacker News`

---

<a id="item-14"></a>
## [腾讯发布 Hy4 开放权重模型，并开源科学伴生模型](https://hy.tencent.ai/research/hy4) ⭐️ 7.0/10

腾讯混元 Hy 团队发布了 Hy4——一个总参数 770B、每 token 激活 49B 的混合专家（MoE）开放权重基础模型，上下文窗口超过 100 万 token，并以 Apache 2.0 许可证开放。与此同时，腾讯还开源了两个由 Hy4 与 Hyra 2.0 共同开发的科学伴生模型：用于单细胞表征的 HyCell 和用于物理场建模的 HyPDE。 来自中国大型实验室的前沿级开放权重发布，为研究人员和开发者提供了一个许可证宽松的替代方案，可对冲美国闭源模型常在条款中限制科研用途的问题。将通用大模型与可复用的科学基础模型、以及深度游戏引擎支持打包在一起，表明其目标不只是聊天模型，而是面向具体领域的开放工具链。 腾讯坦言 Hy4 与顶级闭源模型之间仍有明显差距，尤其是在研究级数学、长程编码、模型自我改进和高级视觉问答等内部基准上。在游戏开发方面，团队与腾讯互娱（IEG）的专业开发者合作整理高质量训练数据和评测，并针对虚幻引擎、Unity 和 Godot 做了大量适配，能力扩展到多人游戏玩法和资产管线。

hackernews · Philpax · 11月4日 14:11 · [社区讨论](https://news.ycombinator.com/item?id=50365780)

**背景**: 开放权重模型是指将训练所得的参数公开释出，任何人都可以下载、部署，通常还能在本地微调，这与只能通过 API 访问的闭源模型形成对比。Hy4 采用混合专家（MoE）架构，即每个 token 只激活 770B 总参数中的一部分（49B），因此推理成本远低于同等总规模的稠密模型。腾讯的 Hy（混元）系列此前包括 Hy3，为 295B 总参数、21B 激活参数的 MoE 模型，上下文长度为 25.6 万 token。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hy.tencent.ai/research/hy4">Tencent Hy</a></li>
<li><a href="https://www.eesel.ai/blog/tencent-hy4">Tencent Hunyuan Hy 4 : specs, benchmarks, and pricing... | eesel AI</a></li>
<li><a href="https://www.tencent.com/tencent-launches-hy4-joining-the-ranks-of-the-worlds-leading-open-source-ai-models/">Tencent Launches Hy4, Joining the Ranks of the World's ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者总体持欢迎态度：有人赞赏这与限制科研用途的美国实验室形成鲜明对比，认为开源科学工具是具有文明级价值的资产；也有人欣赏腾讯坦承与闭源模型仍存在差距。评论者还认为其游戏开发定位少见而有趣，一位 Plotly 工程师则称 Hy4 在成本与准确率的权衡曲线上落在 GPT-6.1 Sol 与 Terra 之间，但工作非常细致、因此速度很慢。

**标签**: `#LLM`, `#open-weight-models`, `#Tencent`, `#scientific-ML`, `#game-development`

---

<a id="item-15"></a>
## [AMD 预计第四季度营收将史上首次超越英特尔](https://www.tomshardware.com/pc-components/cpus/amd-expects-to-outsell-intel-in-q4-for-the-first-time-in-history-usd17b-guidance-would-exceed-intels-projections) ⭐️ 7.0/10

AMD 给出的第四季度营收指引约为 170 亿美元，这一数字将超过英特尔自身对第四季度的预测，成为历史上首个 AMD 营收超越英特尔的季度。公司将这一增长很大程度上归功于其 Instinct 数据中心 GPU 的强劲销售，以及服务器和客户端处理器产品线。 这一交叉点标志着曾长期在 x86 处理器市场处于劣势的 AMD 实现了惊人的逆转，也反映出 AMD 在 AI 加速器上的进展以及英特尔在制造和产品执行上的持续困境。一个更强的第二供应商对整个数据中心、服务器和消费 PC 市场的定价与竞争格局都具有重要意义。 AMD 明确将 Instinct 产品的高销量列为主要增长动力，这意味着该里程碑更多由 AI 加速器而非传统 CPU 份额的提升所推动，而 AMD Instinct 的出货规模相较英伟达的数据中心业务仍然很小。此外，这一比较基于营收而非出货量或 x86 整体份额，因此英特尔在 CPU 总出货量上可能仍遥遥领先。

hackernews · rbanffy · 11月4日 15:38 · [社区讨论](https://news.ycombinator.com/item?id=50367125)

**背景**: AMD 与英特尔在 x86 处理器领域竞争了数十年，AMD 长期扮演规模较小的挑战者角色；它在 2009 年将晶圆厂剥离为 GlobalFoundries，直到 2017 年推出 Zen 架构后才真正恢复竞争力。Instinct 是 AMD 的数据中心 GPU 品牌，于 2016 年推出以取代 FirePro S 系列，基于 CDNA 架构，用于加速 AI 训练、推理以及高性能计算负载。由于当前 AI 基础设施的支出规模已远超传统服务器 CPU 预算，加速器销售对芯片厂商季度营收的影响远大于 CPU 份额的变化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AMD_Instinct">AMD Instinct - Wikipedia</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct.html">AMD Instinct ™ GPUs</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论对英特尔普遍缺乏同情，评论者称其臃肿且自满，并以第 13、14 代 CPU 的电压问题作为转向 AMD 的理由。不少人认为这一里程碑更多说明的是英特尔的失误（包括放弃 Optane），而非 AMD 有多么出色，并指出 AMD Instinct 的销量相较英伟达微不足道，而英特尔 Arc 加速器几乎无人问津。也有人对英特尔的管理引擎和 DCI 调试功能提出隐私与安全担忧，而共同的看法是两家厂商之间更激烈的竞争对所有人都有利。

**标签**: `#AMD`, `#Intel`, `#CPUs`, `#semiconductor industry`, `#market share`

---

<a id="item-16"></a>
## [研究者披露医疗服务软件中 40 多个漏洞，影响逾 1 亿患者](https://www.reddit.com/r/netsec/comments/1xng15c/finding_40_vulnerabilities_in_healthcare_software/) ⭐️ 7.0/10

一名安全研究者以 /u/idnsec 的身份在 r/netsec 发帖，分享了一份技术报告，记录了在服务超过 1 亿名患者的医疗软件中发现的 40 多个漏洞。该帖仅提供指向完整技术报告的链接，并未在 Reddit 正文中概述这些发现。 医疗软件直接嵌入临床和计费工作流，并存储高度敏感的患者记录，因此如此规模的漏洞意味着大量患者面临广泛暴露风险。数量如此之多的漏洞也说明这类软件在构建和维护方式上存在系统性的安全问题，将迫使厂商及其医院客户尽快修复。 目前可获得的材料只有 Reddit 的投稿链接，没有厂商名称、CVE 编号、受影响版本、漏洞类型或披露时间线，因此无法核实技术细节和当前的修复状态。该条目的标签表明相关工作遵循了负责任披露流程，但漏洞是否已修复、是否仍处于禁发期或已公开，均未说明。

reddit · r/netsec · /u/idnsec · 11月4日 05:28

**背景**: 医疗软件涵盖电子健康记录（EHR/EMR）系统、患者门户、预约排程工具和计费平台，这些系统汇聚了大量受保护的健康信息，是攻击者眼中的高价值目标；在美国，此类数据受 HIPAA 法规约束。安全研究者通常遵循协同披露原则，先私下向厂商报告，有时也会通报 CERT/CC 或 CISA 等协调机构，之后再公布细节。像这样成批的漏洞通常会通过 CVE 编号或厂商公告进行跟踪，因此本文中缺少这些标识符限制了对事件的评估深度。

**标签**: `#security`, `#vulnerability-research`, `#healthcare`, `#infosec`, `#responsible-disclosure`

---

<a id="item-17"></a>
## [支付宝联合多方发布中国首个智能体商业信任协议 ACT](https://t.me/zaihuapd/44909) ⭐️ 7.0/10

1 月 16 日，支付宝联合千问 App、淘宝闪购等伙伴正式发布智能体商业信任协议（ACT Protocol），这是中国首个面向 AI 智能体商业需求设计的开放技术框架。该协议为 AI 助手与电商、生活服务平台建立“通用语言”，用户可在千问 App 等终端以对话方式完成比价、领券和支付。 智能体电商能否落地，关键在于商家和支付机构是否信任 AI 代替用户执行操作，因此由国内主导性支付平台推出的统一信任与授权层，有可能成为整个生态的事实标准。若被广泛采用，将降低各类商家被 AI 购物智能体接入的门槛，使流量和交易从 App 浏览转向对话式入口。 支付宝围绕该协议构建了四大核心基础设施标准，确保 AI 执行流程可追溯、可验证，付款环节始终由用户主导或经用户明确授权，同时降低商家接入成本。在蚂蚁集团的相关技术布局中，ACT 与负责智能体之间安全互联与授权管理的 ASL 协议配合使用，由 ACT 提供商业交易所需的信任基础。

telegram · zaihuapd · 11月4日 08:45

**背景**: AI 智能体（Agent）指不仅能回答问题、还能实际执行搜索、比价、填表、支付等操作的模型，而“智能体电商”就是由这类智能体代用户完成购物。这带来了几个难题：商家如何确认请求确实来自用户本人、智能体的行为如何被审计、出错时责任如何界定。支付宝是蚂蚁集团旗下国内主导的移动支付平台，千问 App 则是基于通义千问大模型打造的阿里 AI 助手，因此此次发布实质上是把主流支付通道与主流消费级 AI 入口连接了起来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aibase.com/news/24679">Alipay Launches ACT Protocol, Establishing China's First AI ...</a></li>
<li><a href="https://xix.ai/ainews/ant-group-drives-innovation-in-asl-protocol-to-enhance-trust-in-smart-agent-interactions.html">Ant Group Drives Innovation in ASL Protocol to Enhance Trust ... - xix. ai</a></li>
<li><a href="https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-agentic-commerce-opportunity-how-ai-agents-are-ushering-in-a-new-era-for-consumers-and-merchants">Agentic commerce : How agents are ushering in a new era | McKinsey</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#payments`, `#protocols`, `#e-commerce`, `#Alipay`

---

<a id="item-18"></a>
## [华为告知昇腾 960DT 客户自行采购三星、SK 海力士 HBM](https://thenextweb.com/news/huawei-hbm-smuggling-samsung-sk-hynix-ascend-960dt) ⭐️ 7.0/10

据 The Information 报道，华为已告知部分客户，其下一代旗舰 AI 芯片昇腾 960DT 将主要采用三星和 SK 海力士的 HBM，并因中国本土 HBM 产能不足而要求客户自行解决内存来源。报道还披露了一条走私链路：HBM 被焊在性能极弱的处理器上，按处理器编码报关运至香港，再由人携带入境内地后加热拆下。 这一消息表明，中国最重要的 AI 芯片厂商在多年追求自主可控之后，仍依赖外国的高带宽内存，这可能限制昇腾 960DT 的出货规模，并推高中国 AI 算力建设方的成本。它也说明针对先进内存的出口管制在现实中正被绕开，使政策问题演变成物流与价格问题。 成本影响十分明显：深圳一名芯片经纪人称，单颗 HBM3E 的价格已从一年前的数百美元涨到目前的约 4000 美元。经由香港转运并靠人工携带入境的方式意味着这些内存没有质保和原厂支持，而额外增加的成本与风险最终都由必须自行采购的终端客户承担。

telegram · zaihuapd · 11月4日 14:52

**背景**: 高带宽内存（HBM）是一种多层堆叠的 DRAM，被放置在 AI 加速器旁边，为 GPU 和 NPU 的训练负载提供所需带宽；没有足够的 HBM，AI 芯片无法发挥标称性能。美国的出口管制限制向中国出售先进 HBM 和 AI 加速器，这正是国产替代方案具有战略意义的原因，但本土产品目前在产能和良率上仍难以比肩三星、SK 海力士和美光。华为昇腾系列是中国替代英伟达加速器的主要选择，因此其旗舰产品上的任何内存瓶颈都会直接影响中国的 AI 算力供给。

**标签**: `#Huawei`, `#HBM`, `#AI chips`, `#export controls`, `#semiconductor supply chain`

---

<a id="item-19"></a>
## [苹果将检查 iCloud 公共链接中的有害内容](https://9to5mac.com/2026/11/04/with-ios-27-3-apple-will-start-checking-icloud-public-links-for-harmful-content/) ⭐️ 7.0/10

苹果宣布，从 iOS、iPadOS、macOS 和 visionOS 27.3 起，通过“任何拥有链接的人”方式分享的 iCloud 内容将在苹果服务器端接受有害内容检查。仅分享给指定人员的内容则不在该政策所述范围之内。 这标志着苹果的一次明显转向：这家长期把 iCloud 隐私作为核心卖点的公司，如今开始对可分享链接引入服务端内容审核。由于后果可能包括移除内容、停用账户以及移交执法部门，该政策会影响所有使用 iCloud 链接分享照片、文件或文档的用户。 苹果保留对被判定为有害的内容进行移动、拒绝、修改或删除的权利，并可能限制或停用上传此类内容的用户账户。该检查仅适用于基于链接的公开分享，而不涉及分享给指定接收人的内容，但苹果尚未公开说明检测机制如何运作，也未说明是否存在申诉流程。

telegram · zaihuapd · 11月5日 02:11

**背景**: iCloud 允许用户通过生成链接来分享照片、文件等内容，任何拿到链接的人即使没有苹果账户也能打开。过去这类链接被视为用户主动发起的分享，除常规的滥用与恶意软件防护外，几乎不进行自动化审查。苹果曾在 2021 年提出在 iCloud 照片上实施端侧 CSAM 检测，但在隐私研究者的持续批评下搁置，因此这次针对链接分享的服务端方案被视为检验苹果会走多远的一次重要试验。

**标签**: `#Apple`, `#privacy`, `#content-moderation`, `#iCloud`, `#platform-policy`

---