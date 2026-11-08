---
layout: default
title: "Horizon Summary: 2026-11-08 (ZH)"
date: 2026-11-08
lang: zh
---

> 从 74 条内容中筛选出 15 条重要资讯。

---

1. [GitHub 新架构 Rubicon 实现每秒 7200 次推送](#item-1) ⭐️ 9.0/10
2. [MaxxBench 通过扰动任务描述来压力测试 DeepSWE 分数](#item-2) ⭐️ 8.0/10
3. [每台 Mac 上都藏着构建个人知识图谱的未公开守护进程](#item-3) ⭐️ 8.0/10
4. [Asahi Linux 7.3 进展报告：Fedora Asahi Remix 同日发布与许可证隐忧](#item-4) ⭐️ 8.0/10
5. [苹果披露人形机器人系统 HALO，用两个千问模型](#item-5) ⭐️ 8.0/10
6. [微软研究院 AI Frontiers 团队的终结](#item-6) ⭐️ 7.0/10
7. [爱好者在一根 10 美元的 OpenStick ARM 棒上跑起自托管服务栈](#item-7) ⭐️ 7.0/10
8. [《卫报》曝苹果 iOS 键盘存在“灰名单”，部分词句不予联想](#item-8) ⭐️ 7.0/10
9. [Claude Code 本地设置文件在 1,122 个公开 GitHub 仓库中泄露了 1,379 个密钥](#item-9) ⭐️ 7.0/10
10. [Coldframe：伪装成丹佛斯与 Dixell 冷柜控制器的 Python 蜜罐](#item-10) ⭐️ 7.0/10
11. [《极品飞车：地下狂飙 2》借助 WebGPU 在浏览器中运行，并支持联机对战](#item-11) ⭐️ 7.0/10
12. [VISTA 让具身智能体自写代码修复自身，成功率升至 95%](#item-12) ⭐️ 7.0/10
13. [苹果据报联手阿里训练中国专属大模型，并已向网信办备案](#item-13) ⭐️ 7.0/10
14. [Claude Code 被指在联网请求中泄露用户登录邮箱](#item-14) ⭐️ 7.0/10
15. [中国叫停软银 54 亿美元收购 ABB 机器人业务](#item-15) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [GitHub 新架构 Rubicon 实现每秒 7200 次推送](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 9.0/10

GitHub 公布了代号为 Rubicon 的全新 Git 存储架构，专门面向大量 AI 智能体在同一仓库上高并发操作的场景。内部测试中该架构支持 5000 个智能体同时协作、每秒处理 7200 次推送，并保持较低的读取延迟，目前已进入有限私有预览阶段。 这是对全球最关键开发者平台之一存储核心的重新设计，面向的是一类几年前几乎不存在的工作负载：大量自主智能体同时读写同一个仓库。如果它能在预览之外顺利扩展，可能会改变 CI 系统、单体大仓库以及基于智能体的编程工具在 GitHub 之上的构建方式。 Git 对象被存入 Azure Blob Storage，而引用状态与 pack 清单则放在一个名为 Ref-CAS（Reference Compare-and-Swap，引用比较并交换）的独立复制日志服务中，它采用“先校验再替换”的语义，防止并发写入者悄悄覆盖彼此的分支顶端。虚拟副本负责处理读写请求，后台节点负责压缩 packfile；推广将从当前的有限私有预览阶段逐步扩大。

telegram · zaihuapd · 11月7日 14:12

**背景**: Git 把文件内容存储为内容寻址对象，并定期打包成 packfile，通过相似版本之间的增量压缩来节省空间；分支指针（引用，ref）则是很小且可变的值，读取成本低，但在高并发争用下更新很麻烦。过去这种争用并不明显，因为人类推送代码的速度有限，单个仓库很少同时出现成千上万个写入者。Rubicon 把变化缓慢的对象数据与频繁更新的引用拆分开，使两者可以独立扩展，并用“比较并交换”（compare-and-swap，与 Git 自身 update-ref 校验旧值的思路一致）来保证跨副本的引用更新保持一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/">Inside GitHub’s new Git storage architecture - The GitHub Blog</a></li>
<li><a href="https://www.moreread.net/articles/2026/11/p20261107-021/en.html">GitHub Rubicon: separating stored data from reference updates</a></li>
<li><a href="https://git-scm.com/book/en/v2/Git-Internals-Packfiles">Git - Packfiles</a></li>

</ul>
</details>

**标签**: `#GitHub`, `#distributed-systems`, `#storage-architecture`, `#AI-agents`, `#cloud-infrastructure`

---

<a id="item-2"></a>
## [MaxxBench 通过扰动任务描述来压力测试 DeepSWE 分数](https://maxxbench.unlap.ai/research/why-maxxbench/) ⭐️ 8.0/10

MaxxBench 发布了一篇方法论批评文章，追问高分 DeepSWE 成绩究竟是否代表真实编码能力，其做法是对原始任务描述进行扰动，并测量各模型分数的变化幅度。结果显示基准结果整体上相当脆弱，其中规模最小的模型——尤其是名称带 “-flash” 后缀的模型——分数崩塌最为严重。 DeepSWE 是当前用于给编码模型排名的主要长程软件工程智能体基准之一，因此“微小描述改动就会显著改变排名”这一证据直接影响团队该如何解读排行榜和选型。该研究主张，在报告任何单一基准分数时，都应把基于扰动的敏感性测试作为常规配套手段。 该批评本质上是一种一阶敏感性分析：改变任务的某一个参数并观察分数变化，而不是重新跑一套全新基准。社区评论者还指出 DeepSWE 本身存在若干具体 bug，并提醒至少有一个模型家族的命名（GLM-5.3 与 GLM-5.3-flash）其实属于不同血统，因此“小模型崩塌更严重”这一规律并不能简单套用到所有模型对上。

hackernews · antiuniverse · 11月7日 17:19 · [社区讨论](https://news.ycombinator.com/item?id=50406222)

**背景**: DeepSWE 由 Datacurve 打造，是一个面向智能体式编码的长程软件工程基准：模型需要完成多步骤任务，而非解答短小自足的题目，且题目全部从零撰写，以免被预训练阶段见过的代码污染。由于这类基准构建成本高昂，业界常常把单个 pass@1 数字当作稳定的能力度量。而大语言模型评测文献中的鲁棒性研究恰恰表明，提示词措辞、格式或任务框定的细微变化都可能明显影响输出质量——这正是 MaxxBench 试图为 DeepSWE 量化的敏感性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50406222">MaxxBench – "Nice DeepSWE score. But is it true?" | Hacker News</a></li>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE</a></li>
<li><a href="https://arxiv.org/html/2601.06341">Evaluating Robustness of Large Language Models in Enterprise ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认可这是一种检验分数能否泛化的清晰模板，但对部分解读提出异议：有人认为真正的问题在于实验室构建的 RL 环境过于粗糙、把类似基准的任务过度简化，而非直接在基准上训练；也有人指出许多较弱模型并非答错，而是以其他方式失败。多位评论者表示，发现 DeepSWE 内部存在 bug 加深了他们对 LLM 基准的普遍怀疑，其中一位把“不要使用 max 模式”视为最实用的结论。

**标签**: `#LLM benchmarks`, `#evaluation methodology`, `#AI/ML`, `#benchmark robustness`, `#software engineering agents`

---

<a id="item-3"></a>
## [每台 Mac 上都藏着构建个人知识图谱的未公开守护进程](https://8rank.ai/game/apple-intelligence-personal-knowledge-graph) ⭐️ 8.0/10

一位署名 infwhispers 的研究者发布调查，指出自 2022 年起出厂的每一台 Mac 都运行着一对未公开的守护进程，其用途是构建一张图谱，描述用户本人、其联系人、这些人彼此之间的关系、用户与他们的沟通方式，以及用户去了哪里、和谁一起。该文章发布在 8rank.ai 上，详述了这些守护进程所收集的内容，作者随后还发表了一篇关于 Apple Intelligence 知识图谱的后续研究。 这一发现的重要性在于：它说明支撑设备端 AI 助手的数据基础设施早已部署在操作系统层面，而用户往往并不知道它的存在；即使对于一家以隐私为核心卖点的公司，这也引发了关于知情同意与透明度的质疑。它同样影响到那些以为本地机器只保存自己主动放入照片、通讯录或信息中的内容的 Mac 用户。 据文章所述，这些守护进程是被动地推断关系与位置，而非依赖用户显式填写的家庭关系；作者指出，类似的图谱构建正是 Siri 在你说“给 James 发消息”时能区分“哪个 James”这类功能的基础。数据看起来是在本地组装完成的，但由于缺乏文档，用户没有直接的办法去查看、审计或关闭这张图谱。

hackernews · infwhispers · 11月7日 09:46 · [社区讨论](https://news.ycombinator.com/item?id=50403097)

**背景**: 个人知识图谱是一张结构化地图，描述一个人所关注的实体（人物、地点、机构、对话）以及它们之间的关系；与用户手工搭建的个人知识库不同，它通常由软件自动生成并被软件消费。在 macOS 上，守护进程（daemon）是开机即启动、长期运行的后台进程，默默承担同步 iCloud 数据、校验证书、投递推送通知等任务，因此普通用户几乎感知不到它们的存在。Apple Intelligence 中 Siri 的情境化回应等能力，恰恰依赖这类本地语义索引来解析“我的老板”“妈妈”等指代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Personal_knowledge_base">Personal knowledge base - Wikipedia</a></li>
<li><a href="https://developer.apple.com/library/archive/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/Introduction.html">About Daemons and Services - Apple Developer</a></li>
<li><a href="https://www.netmute.com/blog/macos-network-processes-explained">macOS Background Processes Explained (2026 Guide) | NetMute</a></li>

</ul>
</details>

**社区讨论**: 评论者意见明显分化：一些人觉得这项技术在技术上很有意思，但也表达了疲惫感，并担忧持续记录会侵蚀“对话本是转瞬即逝”的社会默契；另一些人则认为这张图谱只是无害的上下文，用来支持“告诉老板我明天不来了”这类自然表达。有人引用乔布斯 2010 年的说法——隐私意味着用大白话反复告诉用户他们同意了什​​么——以此与未公开的守护进程作对比；研究者本人也加入了讨论并回答提问。

**标签**: `#privacy`, `#Apple`, `#macOS`, `#personal-knowledge-graph`, `#AI`

---

<a id="item-4"></a>
## [Asahi Linux 7.3 进展报告：Fedora Asahi Remix 同日发布与许可证隐忧](https://asahilinux.org/2026/11/progress-report-7-3/) ⭐️ 8.0/10

Asahi Linux 发布了 7.3 进展报告，其中一大亮点是 Fedora Asahi Remix 与上游 Fedora Linux 45 实现同日发布（Fedora Linux 45 于 11 月 3 日发布），这是该项目首次做到同步发版。报告还披露，项目方发现有多个试图利用其宽松许可证来劫持其成果的行为，目的直指取代该项目并对 Apple Silicon 上的 Linux 进行激进商业化，同时项目仍在持续推进硬件支持工作。 同日发布意味着 Asahi 用户不必再等数周甚至数月才能用上新版基础系统，这标志着该移植项目已从实验性尝试成熟为 Fedora 的常态化下游发行版。许可证争议则关系到整个生态：Asahi 以宽松许可证发布的驱动可能被专有或闭源产品吸收，使第三方得以从志愿者的劳动中攫取价值却不回馈社区。 Asahi 过去一直将代码以“上游许可证（如 GPL）+ 宽松许可证（如 MIT）”的双许可证方式发布，以便最大限度地向上游合并，而这恰恰是报告中指出的被利用的漏洞所在。讨论区中另一个社区项目 Gravity Linux 声称已支持 Vulkan 1.4、M4 全部可用、M5 大部分可用，并在挂起到内存（suspend-to-RAM）方面取得进展——目前尚无任何 Asahi 版本支持该功能。

hackernews · ackyshake · 11月7日 05:20 · [社区讨论](https://news.ycombinator.com/item?id=50401867)

**背景**: Asahi Linux 是一个由志愿者驱动的项目，通过逆向工程苹果的片上系统（SoC），把 Linux 内核及相关软件移植到 Apple Silicon Mac 上——苹果并未公开这些芯片的文档。其旗舰发行版 Fedora Asahi Remix 是与 Fedora 项目多年合作的成果，为在 M 系列 Mac 上运行 Linux 提供了打磨完善的终端用户体验。苹果允许在 Apple Silicon Mac 上启动自定义的未签名内核，正是这一特性使整个工作无需越狱即可实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Asahi_Linux">Asahi Linux</a></li>
<li><a href="https://asahilinux.org/fedora/">Fedora Asahi Remix</a></li>
<li><a href="https://asahilinux.org/about/">About - Asahi Linux Installing Linux on Apple Silicon Macs (M1/M2/M3) Running Linux on Apple Silicon Macs in 2026: Is It Finally a ... Unleashing the Power of Apple Silicon Linux - linuxvox.com Linux Apple Silicon Guide: Install on M1, M2, M3 Macs</a></li>

</ul>
</details>

**社区讨论**: 评论区整体气氛热烈：一位长期资助者称 Fedora 同日发布“读起来太棒了”；另一位用户则表示，缺少 USB-C 外接显示器支持仍是阻碍其安装 Asahi 的唯一原因，并对项目优先支持更新款 CPU 感到意外。也有人追问许可证警告是否指向 Omarchy 项目，并惊讶 Asahi 当初竟采用 MIT 而非 GPL；此外还有竞争项目（Gravity Linux）在帖中宣传自己在 M4/M5 与休眠方面的支持。

**标签**: `#Linux`, `#Apple Silicon`, `#Asahi Linux`, `#open source`, `#hardware support`

---

<a id="item-5"></a>
## [苹果披露人形机器人系统 HALO，用两个千问模型](https://weibo.com/1642634100/RqjjGllvw) ⭐️ 8.0/10

苹果研究团队 11 月 4 日在 arXiv 提交论文，披露了人形机器人自主控制系统 HALO（Perceptive Humanoid Motion from Simulation），并在宇树 G1 上完成验证。该系统分为三层：上层用千问 Qwen3.6-35B-A3B 编排任务，中层用 Qwen3.5-2B 生成动作，底层是经强化学习训练的动作跟踪器；团队同时公开了数据生成、模型训练与部署代码。 这项工作显示一家大型消费科技公司正押注“大模型分层规划 + 强化学习底层控制”的技术栈，让完全在仿真中训练的人形机器人能在陌生的真实房间里执行语言指令任务，这是迈向通用具身智能的重要一步。完整代码流程的公开，也为高校和初创机器人团队提供了一个可复现的基线，且基于低成本量产平台而非定制硬件。 HALO 以语言指令和第一视角相机图像为输入，输出全身动作，据报道在评估中任务成功率约为 91%；它采用两个相对较小的千问模型（35B-A3B 的 MoE 模型与 2B 模型），使高层推理足够轻量，可与实时控制并行运行。主要局限在于验证仅限单台宇树 G1 平台和科研环境，跨硬件的鲁棒性与长时序任务尚未得到检验。

telegram · zaihuapd · 11月7日 13:35

**背景**: 仿真到现实迁移（sim-to-real）指在物理仿真器中训练控制策略再部署到真实机器人上，通常借助对摩擦、阻尼和传感器噪声的域随机化等技术来弥合“现实鸿沟”。人形机器人因自由度多、平衡约束强而难以控制；宇树 G1 身高约 1.27 米、重约 35 公斤，拥有 23 个自由度（装配灵巧手后可扩展到 43 个），是广泛使用的低成本科研平台。苹果的方案把问题分层拆解：大语言模型负责推理“做什么”，较小的模型把计划转成动作目标，强化学习跟踪器则在执行时维持机器人平衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/apple-aiml-research/ml-halo">GitHub - apple-aiml-research/ml-halo: HALO: Perceptive ...</a></li>
<li><a href="https://ai.42how.com/en/article/ee6a8f15-db79-4091-9a86-3bc31de6c02f">Apple Integrates Humanoid Perception Into Simulation for Zero ...</a></li>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G1_Humanoid Robot Functions ... - Unitree G1</a></li>

</ul>
</details>

**标签**: `#humanoid robotics`, `#sim-to-real`, `#Qwen`, `#LLM robotics`, `#Apple research`

---

<a id="item-6"></a>
## [微软研究院 AI Frontiers 团队的终结](https://hunch.net/?p=13764006) ⭐️ 7.0/10

随着 John Langford 的离职，微软研究院关闭了其 AI Frontiers 团队，这引发了人们的讨论：业界正日益将重心收窄于 Transformer 的规模化，而牺牲了探索性研究。

hackernews · srean · 11月7日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50406563)

**标签**: `#AI research`, `#Microsoft Research`, `#industry trends`, `#research funding`, `#LLM scaling`

---

<a id="item-7"></a>
## [爱好者在一根 10 美元的 OpenStick ARM 棒上跑起自托管服务栈](https://blog.bosscher.ch/posts/openstick/) ⭐️ 7.0/10

一位 homelab 博主发布了详细文章，介绍他在一根 10 美元的 OpenStick 上搭建的 Linux 环境以及实际运行的自托管服务。OpenStick 是一款基于高通 MSM8916 的 4G LTE USB 上网卡，被改装成运行 Debian Linux 的迷你服务器；文章涵盖了硬件背景、系统准备过程，以及他为适配该设备有限的内存和 CPU 而挑选的具体软件栈。 这篇实践记录说明，如今入门级自托管的硬件成本几乎等同于一顿外卖，从而降低了普通用户尝试 homelab 的门槛。在内存价格居高不下、爱好者寻求更便宜实验途径的背景下，它也呼应了业界转向轻量、资源高效软件的整体趋势。 该设备的资源极为有限，性能大致相当于树莓派 Zero 2 级别的 ARM 芯片，内存仅约 512MB，因此作者强调挑选轻量级软件比硬件参数本身更重要。需要注意的地方包括：需要给这类回收的上网卡硬件刷入 Debian，并仔细甄选能塞进内存预算的服务。

hackernews · LaurensBER · 11月7日 18:12 · [社区讨论](https://news.ycombinator.com/item?id=50406670)

**背景**: OpenStick 指的是一系列基于高通 MSM8916 的廉价 4G LTE USB 上网卡（如 UZ801、UFI003、UFI001B/C 等型号），社区已经摸索出为它们刷入 Debian Linux 的方法，从而把一块“用完即弃”的上网卡变成通用 ARM 计算机。Homelab 指个人搭建的服务器环境，用来自托管 RSS 阅读器、笔记应用或文件存储等服务，而不依赖云厂商。这类服务栈通常需要比这些棒子更多的资源，因此整件事的核心在于软件层面的极简主义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.bosscher.ch/posts/openstick/">What I run on my $10 USD OpenStick homelab | Bosscher</a></li>
<li><a href="https://openstick.org/">OpenStick (Open Stick) — 1-Click Debian Linux for MSM8916 4G ...</a></li>
<li><a href="https://agihunt.info/en/p/1a1b748664637022b2fd69c2239">What I run on my OpenStick: a full Linux… · AGI Hunt</a></li>

</ul>
</details>

**社区讨论**: 评论区气氛热烈：有人建议做成带 PoE 的以太网棒形态，这样只要把节点插进交换机就能组成集群；还有人分享了自己为受限硬件而 fork 的轻量版 miniflux——picoflux，同时称赞了文中选用的订阅阅读器界面。也有人询问在哪里能买到这款硬件，一位资深 homelab 玩家则表示，只要对运行的软件足够挑剔，512MB 内存依然够用。

**标签**: `#homelab`, `#self-hosting`, `#single-board-computers`, `#arm`, `#raspberry-pi`

---

<a id="item-8"></a>
## [《卫报》曝苹果 iOS 键盘存在“灰名单”，部分词句不予联想](https://www.theguardian.com/technology/2026/nov/06/struggling-to-spell-male-chauvinist-pig-apple-grey-list-means-your-iphone-wont-help-you) ⭐️ 7.0/10

2026 年 11 月 6 日，《卫报》报道称苹果 iOS 键盘内置了一份未公开的多语言“灰名单”，包含数万个不会被预测输入推荐、且滑动输入通常也无法生成的词句——据称其中包括“dictator Trump”“sleepy Joe”等政治性短语，以及“male chauvinist pig”之类的辱骂语。逐字母手动输入仍然有效，因此名单上的内容实际上并未被禁止输入。该报道在 Hacker News 上引发了 362 分、243 条评论的热议。 键盘是智能手机上最高频的触碰界面之一，一份不可见的筛选名单因此会悄然影响数亿 iPhone 用户被“引导”去写什么。这件事对整个行业也提出了更普遍的治理问题：平台厂商是否应该在系统层面做出不公开的、带有编辑判断色彩的语言取舍，以及 Gboard 等 Android 竞品键盘是否也在做同样的事。 据报这份名单是多语言的、内置于系统层面，并且匹配的是精确的词序列而非单个字符，因此它只影响联想推荐和滑动输入的解码，而不影响输入本身；不同语言和不同条目的覆盖情况并不一致，滑动输入会规避名单上的“大部分”而非全部短语。苹果并未公开该名单，也未给出详细的公开解释，其官方文档中的键盘设置里也没有查看或修改该名单的选项。

hackernews · user_7832 · 11月7日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50406111)

**背景**: 现代智能手机键盘并不只是记录按键——它运行着语言模型来预测下一个词，并把滑动输入那条潦草的手指轨迹解码成可能的单词。由于这些候选词由模型生成而非用户亲手输入，厂商就可以通过压制特定输出来引导结果，这比直接禁止输入更便宜、也更不显眼。“灰名单”介于普通词典与硬性黑名单之间：这些词仍然可以打出来，但键盘永远不会主动把它推给你。自从有研究揭示 iOS 似乎不愿意自动补全某些短语之后，围绕这类过滤机制的争论就不断升温。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://braindetox.kr/en/posts/apple_iphone_spelling_gray_list.html">iPhone grey list: what Apple’s keyboard won’t autocomplete</a></li>
<li><a href="https://nypost.com/2026/11/06/business/apples-secret-list-of-banned-autocomplete-phrases-include-dictator-trump-sleepy-joe/">Apple’s secret list of banned autocomplete phrases include ...</a></li>
<li><a href="https://swipeblocked.com/">Swipeblocked: the phrases your iPhone won't suggest</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论呈两极分化。批评者认为，即便这些词仍可打出，悄悄不予推荐也是一种“软性胁迫”和不需问责的编辑控制，有人还追问这样的设计决策在会议室里是怎样被拍板的。支持者则反驳说，当你的手指在屏幕上乱划时，键盘给出一个“最佳猜测”并不构成审查；也有不少人指出这大概并非苹果独有——Gboard 被广泛怀疑也在做类似的事——另一些人则借机吐槽 iOS 键盘的整体质量和滑动输入准确度依然落后于竞争对手。

**标签**: `#apple`, `#ios`, `#predictive-text`, `#censorship`, `#ux-design`

---

<a id="item-9"></a>
## [Claude Code 本地设置文件在 1,122 个公开 GitHub 仓库中泄露了 1,379 个密钥](https://apiiro.com/blog/coding-agents-leaking-secrets-github-dont-ask-again) ⭐️ 7.0/10

安全公司 Apiiro 的一项分析发现，有 1,122 个公开 GitHub 仓库提交了 Claude Code 的 .claude/settings.local.json 文件副本，这些文件中包含约 1,379 个密钥——即开发者此前批准过的 shell 命令里直接内嵌的密码、API key 和 token。该发现在 Hacker News 上引发广泛讨论，并获得了 Claude Code 团队的官方回应。 这一泄露把一个日常的便利功能变成了密钥外泄渠道，说明 AI 编码代理可能悄悄把凭据从开发者的 shell 操作中复制到版本控制系统里。随着越来越多团队采用拥有广泛权限的终端代理，这类本地代理状态被意外公开的问题将从个人失误演变为系统性风险。 关键限定在于，问题并非由点击“Don't Ask Again”本身引起：Claude Code 在自动创建 .claude/settings.local.json 时会将其加入 gitignore，因此受影响的文件都是被手动创建并提交到公开仓库的。Claude Code 团队成员 Boris Cherny 承认，Claude Code 过去并未做密钥清理（secret scrubbing），并表示团队正在研究防范措施。

hackernews · shmulc · 11月7日 20:45 · [社区讨论](https://news.ycombinator.com/item?id=50407882)

**背景**: Claude Code 在执行 shell 命令前通常会请用户批准；选择“Yes, and don't ask again”后，它会把一条允许规则写入项目内的 .claude/settings.local.json，使同一命令不再需要审批。这是官方文档中说明的设计行为，但如果被批准的命令中直接含有凭据——例如 URL 中带有 API token 的 curl 请求——该密钥就会以明文形式保存在这个文件里。一旦把该文件提交到公开仓库，凭据也就随之公开，这实际上是“密钥被误提交进源码管理”这一老问题的新变种。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/piekwerk/claude-codes-dont-ask-again-file-held-1379-secrets-in-1122-public-repos-what-4mg5">Claude Code's don't-ask-again file held 1,379 secrets in ...</a></li>
<li><a href="https://code.claude.com/docs/en/settings">Settings files and precedence - Claude Code Docs</a></li>
<li><a href="https://code.claude.com/docs/en/security">Security - Claude Code Docs</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为标题具有误导性，有人指出只有当开发者把含有内嵌密钥的已批准命令的本地 Claude 设置提交上去时，风险才会真正发生。Claude Code 团队的 Boris 确认该文件本应只保留在本地并会被自动加入 gitignore；其他用户则分享了缓解方案，例如为每个任务在隔离网络中启动临时虚拟机并配合 --dangerously-skip-permissions，再通过 API 代理限制其对外部服务的访问，或者把凭据存放在 1Password 中、仅在通过指纹验证调用 op CLI 时才授权访问。还有评论者批评该文章内容反复、像是未经编辑的 AI 生成文本。

**标签**: `#security`, `#AI coding agents`, `#secrets management`, `#Claude Code`, `#developer tooling`

---

<a id="item-10"></a>
## [Coldframe：伪装成丹佛斯与 Dixell 冷柜控制器的 Python 蜜罐](https://github.com/hedgerow-dev/coldframe) ⭐️ 7.0/10

一位开发者发布了 Coldframe，这是一个仅用单个 Python 文件（只依赖标准库）实现的蜜罐，能够高度还原丹佛斯 AK-SM 800A 与 Dixell XWEB 超市制冷控制器的 Web 界面和指纹特征，目前在 Shodan 上会被识别为真实设备而非蜜罐。两个实例已上线运行一天，目前只吸引到通用扫描器和 Shodan 自家爬虫 refrigerator.census.shodan.io 的访问。 暴露在互联网上的制冷与食品零售控制设备已成为真实的攻击目标，因此一个足以以假乱真、成本低廉的诱饵能让防御方观察到针对 OT 设备的真实攻击行为，而不只是停留在推测层面。它也把“谁来负责保护那些根本没有安全人员的超市设备”这一争论推到了台前。 为了让伪装更逼真，作者参照 Shodan 上的真实设备记录复刻了响应头顺序、页面标题、证书字段和 TLS 版本：丹佛斯角色按真实 AK-SM 800A 的顺序发送 nginx 响应头，Dixell 角色则不发送 Server 头，并把页面填充到恰好 8,202 字节。该蜜罐能识别 CVE-2025-41450（丹佛斯“每日代码”登录绕过），记录攻击者提交的当日代码是否正确，还会标记针对另外三个丹佛斯 CVE 及 XWEB 漏洞的尝试，并允许用默认口令登录到一个带除霜按钮的虚假门店仪表盘，从而观察攻击者的下一步动作。

hackernews · hedgerow-dev · 11月7日 17:27 · [社区讨论](https://news.ycombinator.com/item?id=50406292)

**背景**: 丹佛斯 AK-SM 800A 系列是用于监管制冷与食品零售设备的系统管理器，和许多楼宇及工业控制器一样，部分设备可以直接从互联网访问，并被专门搜索暴露设备的搜索引擎 Shodan 收录。CVE-2025-41450 是丹佛斯控制器中的一个身份认证绕过漏洞，根源在于“每日代码”的生成算法可被预测，攻击者无需凭据即可获得管理员权限，并远程强制制冷机组持续进入除霜循环。蜜罐是用于吸引并研究攻击者的诱饵系统，而 OT/ICS 蜜罐则用于收集针对工业和楼宇设备的攻击情报。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nvd.nist.gov/vuln/detail/cve-2025-41450">NVD-CVE-2025-41450</a></li>
<li><a href="https://github.com/GabrieleDattile/CVE-2025-41450-Fromagegate">GitHub - GabrieleDattile/CVE-2025-41450-Fromagegate ...</a></li>
<li><a href="https://www.cisco.com/site/us/en/learn/topics/security/what-is-ot-security.html">OT security: protect ICS and infrastructure [Explained] - Cisco</a></li>

</ul>
</details>

**社区讨论**: 有评论者对依赖 Shodan 指纹来保证真实度表示怀疑，指出网上许多暴露设备本身就是蜜罐或早已被入侵，并建议直接买一台存在漏洞的真实设备来研究。讨论还提到有报道称血库制冷设备遭到攻击，并集中在一个更宏观的观点上：超市根本没有安全团队，因此打补丁、VPN 和强口令等防护应当由厂商或安装方默认提供。也有评论者质疑大规模入侵是否真的发生过，认为可能只是大量机组恰好在同一时间收到了软件更新。

**标签**: `#honeypots`, `#OT/ICS security`, `#industrial control systems`, `#Shodan`, `#Python`

---

<a id="item-11"></a>
## [《极品飞车：地下狂飙 2》借助 WebGPU 在浏览器中运行，并支持联机对战](https://nfsu2.xyz/) ⭐️ 7.0/10

一个托管在 nfsu2.xyz 的爱好者项目让玩家可以完全在浏览器中运行 2004 年的街头竞速游戏《极品飞车：地下狂飙 2》，底层由 WebGPU 驱动，并且支持可用的在线多人联机。该演示在 Hacker News 首页获得 826 分和 227 条评论，有用户表示它甚至在手机上也能流畅运行。 这有力证明了 WebGPU 目前的能力已足以在一个浏览器标签页中运行完整的商业 3D PC 游戏并支持联网对战，模糊了原生游戏与网页游戏之间的界限。同时它也让人们关注“废弃软件”（abandonware）与游戏保存所处的法律灰色地带，因为该项目依赖的是早已停止销售的受版权保护的内容。 Linux 用户反馈，该网站需要在 Chromium 中启用不安全的 WebGPU 特性（例如使用 chromium --enable-unsafe-webgpu 之类的启动参数）才能运行；评论者还指出，如今任何零售版游戏在现代 PC 上几乎都无法直接游玩，需要依赖爱好者补丁。该网站的法律地位存疑，有评论者反对其为受版权保护的内容募捐，因此在其走红之后，被下架的可能性不小。

hackernews · fluxusars · 11月7日 09:36 · [社区讨论](https://news.ycombinator.com/item?id=50403052)

**背景**: WebGPU 是由 W3C 标准化的 JavaScript API，通过 Vulkan、Metal 或 Direct3D 12 为 Web 应用提供高效、底层的 GPU 访问能力，旨在取代 WebGL；浏览器支持方面，Chrome 和 Edge 于 2023 年 5 月率先支持，Firefox 141 于 2025 年 7 月跟进，Safari 26 于 2025 年 9 月支持，到 2025 年 11 月已覆盖所有主流浏览器。所谓“废弃软件”（abandonware）指创作者已不再销售或提供支持的软件（通常是游戏），但其版权实际上并未被放弃——分发这类软件在法律上仍属盗版，尽管一些游戏史研究者认为这是保存游戏历史的必要手段。因此，要在浏览器中运行这类游戏，往往需要重新实现或重新打包原始引擎，这也使此类项目长期处于法律灰色地带。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU</a></li>
<li><a href="https://en.wikipedia.org/wiki/Abandonware">Abandonware</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论充满了怀旧情绪——玩家们回忆当年局域网联机的时光、Snoop Dogg 演唱的《Riders on the Storm》配乐，以及数百辆车同时原地烧胎、互相鸣笛的混乱场面——同时也对它能真的跑起来感到惊讶。多位评论者担心项目的合法性和被 DMCA 下架的风险，有人反对为受版权保护的内容募捐，也有人认为这些被弃置的游戏理应得到保存。此外，大家还分享了诸如 Linux 下开启 Chromium 不安全 WebGPU 标志等实用技巧。

**标签**: `#emulation`, `#WebGPU`, `#game-preservation`, `#browser-gaming`, `#abandonware`

---

<a id="item-12"></a>
## [VISTA 让具身智能体自写代码修复自身，成功率升至 95%](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247940414&idx=3&sn=6a208ab7dffbe83bfda1e6dd1c91550d) ⭐️ 7.0/10

据一篇中文技术报道，VISTA 框架让具身智能体通过主动探索环境并生成代码来实现自我修复和能力迭代。报道称，在不更新模型权重的情况下，任务成功率从 17.5% 提升到了 95%。 如果报道结果成立，VISTA 为已部署机器人提供了一条无需昂贵重训或更新权重就能适应环境、从故障中恢复的实用路径。对于数据采集、微调和重新部署都很慢或成本很高的长期运行具身智能系统，这一点尤其重要。 根据摘要，性能提升来自代码层面的自我修改，而不是基于梯度的学习。不过，现有内容没有披露基准测试、任务集合、生成代码的验证方式或安全约束，因此可复现性和鲁棒性仍是未解问题。

rss · 量子位 · 11月7日 04:30

**背景**: 具身智能指的是通过机器人等物理实体感知和行动的人工智能系统，而不只是处理虚拟数据。模型权重是训练过程中通常会更新的学习参数；“不更新权重”意味着智能体借助生成代码、记忆或工具等外部产物来提升能力，而不是重新训练。代码生成智能体旨在自动产出或修复可执行程序，在机器人场景中，这可能让系统在遇到故障时修改自身的控制逻辑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://juejin.cn/post/7486670839923359796">什么是 具 身 智 能 ？ 具 身 智 能 （Embodied Intelligence...</a></li>
<li><a href="https://post.smzdm.com/p/ad723v6n/">AI...</a></li>
<li><a href="https://blog.csdn.net/weixin_42601702/article/details/170031005">[项目篇23] 用TaoToken统一通道为OpenCode机器人接入代码生成与自动修...</a></li>

</ul>
</details>

**标签**: `#具身智能`, `#自进化智能体`, `#代码生成`, `#机器人自修复`, `#VISTA`

---

<a id="item-13"></a>
## [苹果据报联手阿里训练中国专属大模型，并已向网信办备案](https://t.me/zaihuapd/44977) ⭐️ 7.0/10

知情人士称，苹果已专门针对中国市场训练了一款大语言模型，并获得阿里巴巴的支持，一改此前依赖第三方模型的策略。Apple 智能预计将在未来数月随 iOS 更新在中国上线，而中国网信办已于上个月对其生成式人工智能服务完成备案。 如果获批落地，苹果将成为首个获北京批准在华提供自有 AI 模型的外国公司，而在中国市场，绝大多数海外 AI 服务目前都无法使用。相比租用本土合作伙伴的模型，自研模型能让苹果更好地掌控数亿台 iPhone 上的中文 AI 体验，也可能为外国企业进入中国受监管的 AI 市场树立先例。 该消息来自路透社，依据的是匿名知情人士的说法，苹果与阿里巴巴均未公开确认该模型的存在、参数规模或阿里参与的具体范围。Apple 智能于 2024 年 10 月随 iOS 18.1 首次上线，在境外部分请求会调用 OpenAI 的 ChatGPT，而这一能力显然不会出现在中国版本中。

telegram · zaihuapd · 11月7日 03:06

**背景**: 根据 2023 年 8 月生效的《生成式人工智能服务管理暂行办法》，任何面向中国公众提供的生成式人工智能服务都必须通过安全评估并向网信办完成备案；截至 2024 年末约有 302 款服务完成备案，到今年 3 月这一数字已增至约 346 款。正因为这一备案要求，ChatGPT、Gemini 等服务无法在中国大陆直接提供，苹果也不能简单地把全球版的 Apple 智能功能原样搬到中国。此前有报道称苹果曾与中国本土 AI 厂商洽谈由其为该功能提供本地支持，而这次的消息显示苹果改为自研模型，同时保留阿里巴巴作为合作伙伴。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://files.chinaaet.com/files/2025/01/14/20250114140515-66797.pdf">files.chinaaet.com/files/2025/01/14/20250114140515-66797.pdf</a></li>
<li><a href="https://boilingwater.cn/en/article/1912063788787535873/1">滚水科技- 【今日资讯】 AI ... | 滚水科技-最值得 信 任的数字化合作伙伴</a></li>

</ul>
</details>

**标签**: `#Apple`, `#LLM`, `#China AI regulation`, `#Alibaba`, `#AI industry news`

---

<a id="item-14"></a>
## [Claude Code 被指在联网请求中泄露用户登录邮箱](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 7.0/10

有开发者投诉称，Claude Code 会把用户的账号登录邮箱填入对外发出的网页请求中，收件方包括 Wikipedia、美国证券交易委员会（SEC）等站点，导致用户每天收到大量诈骗与垃圾邮件。Anthropic 工程师确认了根因，表示 2.1.317 版已加入拦截，并承诺在下一个版本中彻底把登录邮箱从模型上下文中移除。 Claude Code 是使用广泛的 AI 编程代理工具，账号标识被意外发送给任意第三方站点，对其用户群构成实实在在的隐私与安全风险。该事件也揭示了所有 AI 代理的通病：一旦数据被放进模型上下文，就可能随对外网络请求一起流出，而这种泄露既难以审计又容易被忽视。 该问题早在 2026 年 7 月就有人报告，而 2.1.317 版的修复只是基于模式匹配的拦截，开发者称用一段简单的 Python 脚本即可绕过，因此在后续版本真正把邮箱从上下文中移除之前，用户仍处于暴露状态。Anthropic 当初把登录邮箱放进模型上下文的原因，是为了避免模型在生成内容时胡乱编造作者名。

telegram · zaihuapd · 11月7日 08:09

**背景**: Claude Code 是 Anthropic 推出的命令行 AI 编程代理，可以代替用户读取文件、执行命令和抓取网页。为了让输出保持一致，该工具会把一些账号元数据（此处即登录邮箱）保留在模型上下文中，模型因此能看到它，并可能在生成的文本里复述出来。当代理执行联网搜索或对外 HTTP 请求时，这些生成文本连同其中泄露的标识信息会被发送到第三方服务器。正因如此，上下文治理与对外请求过滤正成为 AI 代理工具的核心安全问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.w3cschool.cn/article/23992735.html">TRAE... | w3cschool笔记</a></li>
<li><a href="https://topstip.com/browserstack-leaking-user-emails-not-so-simple/">BrowserStack 竟然在 泄 露 用户 邮 箱 ？ 这 事 可 能 没那么简单</a></li>

</ul>
</details>

**标签**: `#claude-code`, `#privacy`, `#security`, `#ai-agents`, `#anthropic`

---

<a id="item-15"></a>
## [中国叫停软银 54 亿美元收购 ABB 机器人业务](https://t.me/zaihuapd/44988) ⭐️ 7.0/10

中国外国投资安全审查机构已通知禁止软银集团以约 53.75 亿美元收购 ABB 机器人部门的交易在中国实施，ABB 于 11 月 5 日确认已收到该通知。这一决定使软银通过收购 ABB 分拆出的机器人控股公司来布局人工智能与机器人产业的计划受阻。 中国约占 ABB 机器人业务 30%的份额，因此北京行使否决权足以实质性地终止而非仅仅推迟一项全球性分拆交易，这表明中国监管机构如今对全球战略科技并购拥有事实上的否决权。此举也显示，继此前阻止 Meta 收购中国 AI 智能体公司 Manus 之后，中国对涉及工业数据、供应链和机器人/人工智能核心技术的交易审查正在趋严。 该交易于 2025 年 10 月 8 日公布，原计划由 ABB 将机器人部门分拆进入一家新设控股公司，软银以 53.75 亿美元的企业价值收购其全部股份，从而取代 ABB 此前将该部门独立上市的方案。中方给出的关切是，ABB 机器人业务相关的工业数据、供应链信息与核心技术可能被转移至海外并用于训练人工智能模型。

telegram · zaihuapd · 11月7日 11:24

**背景**: 中国的外国投资安全审查（FISR）制度建立在《外商投资法》以及 2021 年 1 月生效的《外商投资安全审查办法》之上，国家发展改革委牵头的工作机制有权审查涉及国家安全的交易，并可予以禁止或要求解除相关安排。由于该权限既覆盖外资收购境内资产，也覆盖目标公司在中国拥有重要业务的交易，因此中国的禁令可以让一笔完全在两家非中国公司之间构建的交易陷入停滞。日本综合性企业集团软银正围绕人工智能与机器人重新布局，而瑞士 ABB 与发那科、库卡、安川并列为全球工业机器人“四大家族”之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://group.softbank/en/news/press/20261106">Update on Acquisition of ABB Ltd’s Robotics Business</a></li>
<li><a href="https://www.abb.com/global/en/news/129685/abb-to-divest-robotics-division-to-softbank-group">ABB to divest Robotics division to SoftBank Group</a></li>
<li><a href="https://mmlcgroup.com/china-national-security-reviews/">An Analysis of China’s Foreign Investment Security Review ...</a></li>

</ul>
</details>

**标签**: `#tech-geopolitics`, `#mergers-and-acquisitions`, `#robotics`, `#foreign-investment-review`, `#AI`

---