---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 69 条内容中筛选出 10 条重要资讯。

---

1. [OpenAI 主张困惑度（即压缩率）是智能的稳健代理指标](#item-1) ⭐️ 8.0/10
2. [社区进度图追踪备受争议的黎曼猜想证明的 Lean 形式化工作](#item-2) ⭐️ 8.0/10
3. [Tim O'Reilly 称硅谷已从价值创造转向价值攫取](#item-3) ⭐️ 8.0/10
4. [美商务部拟定稿新规，封堵中国 AI 公司远程使用先进芯片的漏洞](#item-4) ⭐️ 8.0/10
5. [Jeff Geerling 加入 NTP Pool，却没有用他的 Stratum 1 树莓派](#item-5) ⭐️ 7.0/10
6. [Raschka：预训练仍未出现停滞](#item-6) ⭐️ 7.0/10
7. [群联发布航天级 SSD，488 TB 存储将随 StarVault-001 入轨](#item-7) ⭐️ 7.0/10
8. [谷歌搭建名为 Mirror Dimension 的模拟互联网以测试 Chrome AI 代理](#item-8) ⭐️ 7.0/10
9. [Windows Server 2028 默认移除 WoW64，32 位应用需手动加装](#item-9) ⭐️ 7.0/10
10. [特斯拉开始推送 FSD v15，带来类 GTA 的「Reality View」可视化界面](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 主张困惑度（即压缩率）是智能的稳健代理指标](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI 发表了一篇题为《Perplexity and Intelligence》的文章，主张语言模型的困惑度（perplexity，即模型在留出文本上平均负对数似然的指数形式，本质上衡量模型对原始数据的压缩能力）是一个简单却出乎意料稳健的智能代理指标。该文在 Hacker News 上引发大规模讨论（约 513 分、354 条评论），既有对该指标定义的澄清，也有对其在强化学习训练模型上是否依然成立的争论。 如果单一且廉价的预训练指标能像各种定制基准一样反映模型能力，就可能简化业界比较模型的方式，减少对日益繁杂、层出不穷的评测套件的依赖。这一主张尤其具有争议性，因为近期进展主要来自以强化学习训练的推理模型，人们本来预期预训练损失在这类模型上会变得不那么重要。 困惑度的正式定义是每个 token 平均负对数似然的指数：当模型对每个正确 token 都给出概率 1 时，其值最小为 1；而对完全随机的预测器，其值会升至词表大小。文章的论据建立在跨模型代际的经验趋势上，而非形式化证明，因此它是一种强相关的论证，并不保证仅凭困惑度就能决定下游的推理能力。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**背景**: 困惑度是语言模型最常用的内在指标之一，可追溯到经典的 n-gram 语言建模，如今也是大模型预训练阶段的标准评估手段。它与“压缩”这一概念密切相关：能准确预测下一个 token 的模型原则上可以更紧凑地编码原始数据流，这也是部分研究者把智能本身理解为对感知数据高效压缩的原因。神经缩放定律（neural scaling laws）描述了损失如何随参数、数据和算力的增长而可预测地下降，为把损失当作能力信号提供了经验基础。与此同时，现代后训练——RLHF 以及 o1 等推理模型背后的强化学习方法——优化的是行为而非下一 token 似然，这正是困惑度与智能之间关系是否持续存在争议的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Neural_scaling_law">Neural scaling law</a></li>
<li><a href="https://agentica.wiki/articles/neural-scaling-laws">Neural Scaling Laws | Agentica</a></li>

</ul>
</details>

**社区讨论**: 评论者首先补上了文章缺失的一环，明确写出困惑度的形式化定义，并指出其取值范围从 1 到词表大小。多人表示惊讶：在转向强化学习与推理模型之后，交叉熵损失依然如此具有预测力；同时也乐见在基准日益繁杂之际出现一个简单指标。一位评论者提到自己 2008 年的论文就提出过“预测即压缩”的相同论点，另一位则指出微软的 Mustafa Suleyman 已在 OpenAI 的留出评测集上报告 MAI-2 Base 的对数困惑度为 0.819，暗示该指标可能成为各实验室共享的标尺。

**标签**: `#llm-evaluation`, `#perplexity`, `#compression`, `#scaling-laws`, `#openai`

---

<a id="item-2"></a>
## [社区进度图追踪备受争议的黎曼猜想证明的 Lean 形式化工作](https://claude.ai/artifact/CtQyX8qfYAF822bgHJHHE3) ⭐️ 8.0/10

一份由社区维护的进度图已发布，用于追踪对 Alessandro Masullo 声称证明黎曼猜想的稿件进行 Lean 形式化的进展。该仓库在 Hacker News 上引发讨论（173 分、147 条评论），其中包含一份列出数百个问题的勘误表，并正在向志愿者征集闲置的 AI 智能体 token 算力。 这一事件处于 AI 辅助数学、机器可检验的形式化验证与同行评议的交汇点，提出了“Lean 进度条能否替代数学上的正确性验证”这一问题。它也说明，一个针对著名未解问题的所谓证明，可以在公开场合被多快地传播、审视与争论。 一位参与贡献的数学家强调，勘误表中的数百条问题有的轻微、有的并不轻微，目前判断核心思路是否存在致命漏洞还为时过早。评论者还提醒，形式化进度条只衡量已编码的比例，并不代表证明正确，因为只要有一个漏洞就可能让整个论证崩塌。

hackernews · Qision · 11月22日 23:12 · [社区讨论](https://news.ycombinator.com/item?id=50605045)

**背景**: Lean 是一个开源证明助手兼函数式编程语言，最初由微软研究院于 2013 年起开发，现由非营利组织 Lean Focused Research Organization 支持；它让数学家把定理与证明写成代码，由一个小型内核机械地检查每一步。数学的形式化验证就是把论文中的证明翻译到这类系统中，但只有当形式化陈述与原命题完全一致时，才能保证正确性。Masullo 的稿件是一份对黎曼猜想的证明，而黎曼猜想是数学中最古老、最著名的未解难题之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://chierhu.medium.com/lean-for-science-how-formal-proofs-can-change-mathematics-ai-and-scientific-computing-cc383c9ce020">Lean for Science: How Formal Proofs Can Change Mathematics , AI...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏向怀疑：评论者指出 Ravi Vakil 现在表示自己从未审阅过 Masullo 的文件，Brian Conrad 对《科学美国人》称该稿件需要“重大修订”，而 Masullo 除这份所谓的证明外没有其他发表记录。一位参与贡献的数学家则反对过度解读勘误表，同时为项目招募算力；还有人感叹，智能体式 AI 在加速形式化的同时，可能让人工数学家被边缘化。

**标签**: `#lean`, `#formal-verification`, `#mathematics`, `#riemann-hypothesis`, `#ai-assisted-proofs`

---

<a id="item-3"></a>
## [Tim O'Reilly 称硅谷已从价值创造转向价值攫取](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) ⭐️ 8.0/10

Tim O'Reilly 在 O'Reilly Radar 发表新文章，认为硅谷已经从创造真正的价值滑向仅仅攫取价值，并提出用“机制设计”（也被称为“反向博弈论”）来重新设计市场规则，使其以人类福祉而非股东价值为优化目标。他用谷歌前首席经济学家 Hal Varian 的一句话来说明这种转变：谷歌搜索结果页面中只有约 6% 带有广告，其余 94% 都是无偿提供的富足供给。 这篇文章把人们对大型科技公司商业模式的常见抱怨重新表述为一个“设计问题”：如果市场是人造的系统，那么其中编码的激励机制就可以被有意识地改写，这对监管者、创业者以及所有受广告驱动或参与度驱动产品影响的人都意义重大。文章发表之际，AI 投入与变现压力正迫使大型科技公司以前所未有的力度压榨其核心产品的商业价值。 O'Reilly 的核心主张埋在一篇长文的结尾处：机制设计要问的不是“我们正在玩的游戏规则是什么”，而是“我们本该玩什么游戏”，而他的答案是“人类福祉的游戏”。这篇文章属于评论与论证，而非技术发布，因此它提供的是一种分析框架，而不是可量化的方案或实施细节。

hackernews · greenyouse · 11月22日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50602947)

**背景**: 机制设计是经济学与博弈论的一个分支，研究如何构造规则（即“机制”或“制度”），使得在设计师并不掌握参与者真实偏好或私有信息的情况下，仍能按某种预设标准产生良好结果。由于它从期望的结果出发、反向寻找能实现该结果的博弈，因此常被称为“反向博弈论”；Leonid Hurwicz、Eric Maskin 和 Roger Myerson 因奠定该理论的基础而获得 2007 年诺贝尔经济学奖。这一方法支撑着现实中的互联网系统，包括谷歌和 Facebook 的广告拍卖以及域间路由。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanism_design">Mechanism design - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reverse_game_theory">Reverse game theory</a></li>

</ul>
</details>

**社区讨论**: 讨论相当热烈（480 分、277 条评论），整体态度偏向认同：多位评论者同意 O'Reilly 的观点，但认为关于“以人类福祉为优化目标”的核心论点被埋得太靠后。也有人补充背景，指出早期谷歌无偿提供的富足供给正是许多人当年对科技业感到乐观的原因；还有评论者把当前的攫取式格局归因于零利率时代，认为它让企业膨胀到畸形规模，如今又在 AI 的推动下蚕食自身的核心业务。

**标签**: `#tech-industry`, `#silicon-valley`, `#mechanism-design`, `#capitalism`, `#economics-of-software`

---

<a id="item-4"></a>
## [美商务部拟定稿新规，封堵中国 AI 公司远程使用先进芯片的漏洞](https://t.me/zaihuapd/45289) ⭐️ 8.0/10

据报道，美国商务部正在敲定一项规则，最早可能于本月公布，旨在阻止中国 AI 公司通过境外数据中心远程使用先进 AI 芯片。该管制将把现有的半导体出口限制扩大到马来西亚、新加坡、泰国等七个国家，以封堵远程访问和芯片走私漏洞；商务部正与其他政府机构磋商后定稿。 此举将堵上中国 AI 开发者获取算力的最后几个主要迂回通道之一，可能重塑全球 AI 算力的租赁与部署格局。它不仅影响中国 AI 实验室，也会波及东南亚的云服务商和数据中心运营商，并标志着美国出口管制向第三国的进一步延伸。 据报道，该规则在现有受限名单之外新增七个国家，同时针对先进芯片的远程访问和实体芯片走私；白宫此前已要求国会立法，要求商务部制定这一规则。英伟达曾游说反对封堵远程访问缺口，称美国 AI 基础设施必须要在全球取胜。

telegram · zaihuapd · 11月22日 04:34

**背景**: 美国出口管制此前已限制向中国销售最先进的 AI 加速器，例如英伟达的高端 GPU。部分中国企业转而通过在第三国数据中心租用算力、再经由互联网远程使用的方式绕开限制，而非直接进口硬件。新加坡和马来西亚已成为亚洲重要的数据中心枢纽，因而成为这类迂回路径的关键节点。新规则试图不仅管制芯片的实体出口，还管住谁可以远程使用这些芯片。

**标签**: `#AI chips`, `#export controls`, `#US-China tech`, `#semiconductors`, `#data centers`

---

<a id="item-5"></a>
## [Jeff Geerling 加入 NTP Pool，却没有用他的 Stratum 1 树莓派](https://www.jeffgeerling.com/blog/2026/i-joined-the-ntp-pool/) ⭐️ 7.0/10

Jeff Geerling 发布了一篇博文，讲述他如何注册成为公共 NTP Pool 的志愿授时服务器，并解释了为什么他没有把自己家庭实验室里的树莓派 Stratum 1 设备投入该项目使用。文章梳理了向 NTP Pool 贡献服务器（而不只是从中获取时间）时所涉及的一系列实际决策。 由于客户端需求持续增长，NTP Pool 长期处于服务器紧缺状态，因此每新增一个志愿节点都能减轻现有服务器的压力，并提升全球时间同步的可靠性。知名家庭实验室作者所写的详细文章很可能会促使更多爱好者参与贡献，同时也推动社区更认真地思考究竟什么样的硬件才真正适合授时。 加入 NTP Pool 需要固定静态 IP 地址，并且时间必须来自另一台 NTP 服务器的准确校时；候选服务器会被监控客户端持续轮询打分，分数决定该节点是否会出现在 DNS 分发中。由于网卡和 GPIO 中断抖动，树莓派通常被认为授时性能一般，但可以通过自带网络接口的定制 HAT 扩展板以及晶振替换改造在一定程度上缓解。

hackernews · fortran77 · 11月22日 15:35 · [社区讨论](https://news.ycombinator.com/item?id=50600622)

**背景**: NTP Pool 是一个由志愿者运营的网络化计算机集合，通过 pool.ntp.org 域名、轮询 DNS 与地理定位，把使用网络时间协议（NTP）的全球客户端分散到各台服务器上获取准确时间。Stratum 1 服务器指的是直接以 GPS 等硬件参考时钟配合 PPS（每秒脉冲）信号获取时间的服务器，而不是通过网络从另一台 NTP 服务器取时——这正是许多家庭实验室爱好者围绕树莓派搭建的方案。由于该池完全依赖他人捐赠带宽和硬件，随着客户端数量增长，它始终需要更多服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NTP_pool">NTP pool</a></li>
<li><a href="https://www.ntppool.org/en/">pool.ntp.org: the internet cluster of ntp servers</a></li>
<li><a href="https://linuxjunkies.org/guides/raspberry-pi-time-server-ntp">Build a Stratum-1 NTP Server on a Pi · Linux Junkies</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同树莓派并非授时的理想基础，并提出了替代方案：基于 FPGA 的授时服务器、支持 PCIe PTM 或 TGPIO 的 x86 机器，以及一位读者在 GitHub 上开源的不到 50 美元的 ESP32-P4 加 u-blox M8T 方案。其他人则比较了 NTPSec（现已成为 Debian 默认）与 chrony 等软件选择；一位长期用户还质疑 NTP Pool 的质量，回忆起曾遇到无响应的服务器，以及给出的时间偏差达数天甚至数月的节点。

**标签**: `#NTP`, `#timekeeping`, `#homelab`, `#Raspberry Pi`, `#networking`

---

<a id="item-6"></a>
## [Raschka：预训练仍未出现停滞](https://sebastianraschka.com/blog/2026/pretraining-is-still-not-plateauing.html) ⭐️ 7.0/10

Sebastian Raschka 发布博客文章，梳理了 OpenAI 公布的“在留出代码数据上的下一词元预测”测量结果，追踪该指标从 GPT-4 到 GPT-4.5 以及后续基础模型的变化。他的结论是：数据显示性能仍在持续提升，预训练并未出现停滞。 预训练收益是否正在趋于平缓，是当前人工智能领域最关键的问题之一：一旦确认停滞，产业重心就会转向推理阶段算力、后训练和合成数据，而非单纯扩大训练规模。如果留出代码上的损失在各代模型之间持续下降，那么继续大规模投入预训练的合理性就会得到强化。 该分析依据的是留出代码上的下一词元预测损失，这是一个干净的自监督指标，不像下游评测那样容易受到基准数据污染或提示词格式的影响。比较对象是基础模型而非指令微调版本，因此衡量的是预训练本身的进展，而不是后训练或对齐带来的提升。

rss · Sebastian Raschka · 11月22日 22:07

**背景**: 神经缩放定律描述的是模型性能如何随着参数、数据和算力的增长而可预测地提升，这一经验规律由 Kaplan 等人（2020）推广，并由 Hoffmann 等人（2022）提出的模型规模与数据规模之间的“计算最优”权衡（即 Chinchilla 结论）进一步细化。下一词元预测损失衡量的是模型在从未见过的文本上给正确下一个词元分配概率的能力，因此留出数据上的损失越低，就越直接地说明模型学到了更通用的结构。基础模型是尚未经过指令微调或 RLHF 的原始预训练检查点，研究者正是用它把预训练进展与后训练效果剥离开来观察。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Neural_scaling_law">Neural scaling law - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2411.04434">Scaling Laws for Pre-training Agents and World Models</a></li>
<li><a href="https://www.together.ai/blog/how-to-fine-tune-llms">How to fine- tune an LLM : a developer's guide</a></li>

</ul>
</details>

**标签**: `#pretraining`, `#scaling-laws`, `#LLMs`, `#evaluation`, `#OpenAI`

---

<a id="item-7"></a>
## [群联发布航天级 SSD，488 TB 存储将随 StarVault-001 入轨](https://videocardz.com/newz/phison-announces-488tb-of-ssd-storage-for-space-data-centers-pricing-expected-to-be-astronomical) ⭐️ 7.0/10

群联（Phison）发布了面向航天器、卫星和在轨数据中心的 Pascari Space SSD 系列，并确认 Lonestar Data Holdings 的轨道数据中心 StarVault-001 将搭载 488 TB 该系列硬盘，计划于 2027 年上半年发射。该系列分为 Flight Critical、Main Storage 与 Orbital Data Center 三类，单盘最高容量 128 TB，群联表示产品已上市。 这是首批具有明确订单规模的、专为轨道环境设计的存储硬件承诺之一，意味着“太空数据中心”正从概念演示走向商业部署。它对存储行业和航天产业都有意义：抗辐射要求、严格的功耗限制以及无法现场维修，使得轨道存储在工程上与地面数据中心截然不同。 StarVault-001 上安装的 488 TB 在扣除冗余和系统开销后，可用容量约为 370 TB；群联称部分型号通过 pSLC 模式可将写入寿命提升至多 60 倍，但代价是原始容量降低。单盘最高容量为 128 TB，官方未公布定价，媒体预计价格将极其高昂。

telegram · zaihuapd · 11月22日 10:31

**背景**: 轨道数据中心是一个新兴品类，把服务器与存储部署到太空中，其动因包括数据主权、物理安全以及新型的数据驻留模式；Lonestar Data Holdings 正是销售此类“离地存储”的公司，其 StarVault 服务依托低地球轨道基础设施运行。Pascari 是群联的企业级 SSD 品牌，此前以高容量 Gen5 数据中心硬盘为人所知。pSLC（伪 SLC）是一种固件技术，让 TLC 或 MLC 闪存每个单元只存 1 bit，从而表现得像 SLC，以牺牲容量换取高得多的写入寿命和更好的性能——在无法更换硬盘的太空环境中，这是很有价值的取舍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.delkin.com/blog/understanding-pslc/">Understanding PseudoSLC (pSLC) | Delkin Devices</a></li>
<li><a href="https://www.tweaktown.com/news/107945/over-1-petabyte-of-phison-pascari-ssds-are-headed-to-the-international-space-station-in-2027/index.html">Over 1 Petabyte of Phison Pascari SSDs are headed to the...</a></li>
<li><a href="https://www.phisonenterprise.com/">PASCARI by Phison : Redefining Enterprise Data Storage</a></li>

</ul>
</details>

**标签**: `#SSD storage`, `#space technology`, `#orbital data centers`, `#hardware`, `#Phison`

---

<a id="item-8"></a>
## [谷歌搭建名为 Mirror Dimension 的模拟互联网以测试 Chrome AI 代理](https://www.landian.news/archives/128701.html) ⭐️ 7.0/10

据报道，谷歌为 Chrome 的 AI 代理搭建了一个名为 Mirror Dimension 的模拟互联网，在隔离环境中测试它打开网站、搜索浏览、登录、加购和完成任务等操作。该沙盒包含数千个模拟网站，每名工程师在各自隔离的环境中测试，每天运行超过 1000 个测试案例，重点防御恶意网页发起的提示词注入等攻击。 能够点击、输入和登录的浏览器 AI 代理在极大提升实用性的同时也扩大了网络攻击面，而可控制的仿真互联网让谷歌能够在不危及真实用户和真实网站的前提下训练和验证代理。在谷歌、OpenAI 等公司竞相推出代理式浏览功能之际，这些代理抵御恶意网页内容的严格程度，可能影响用户信任以及整个浏览器代理生态所遵循的安全标准。 据报道，该环境对每名工程师的测试进行单独隔离，并每天运行超过 1000 个测试案例，说明这是一套高度自动化、持续运行的评估流程，而非一次性的手工检查。对提示词注入的重视尤为值得注意，因为间接提示词注入——即隐藏在网页内容中的恶意指令——是具备浏览能力的大语言模型的一个已知薄弱环节。

telegram · zaihuapd · 11月23日 01:30

**背景**: AI 浏览代理是配备了浏览器控制工具的大语言模型，可以代替用户读取页面、点击链接和填写表单。提示词注入是一类攻击方式，网页或其他输入中隐藏的文本会被模型当作指令执行，从而可能诱使代理泄露数据或执行非预期操作。由于具备浏览权限的代理必须区分可信的开发者指令与不可信的网页内容，在安全沙盒中用对抗性网页对其进行测试已成为开发流程中的标准环节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://modeles.com/news/google-built-a-giant-mirror-dimension-internet-to-test-its-chrome-ai-agents-fde7b4">Google Built a Giant ‘ Mirror Dimension ’ Internet to... — MODELES</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Chrome`, `#prompt injection`, `#browser security`, `#AI testing`

---

<a id="item-9"></a>
## [Windows Server 2028 默认移除 WoW64，32 位应用需手动加装](https://www.windowslatest.com/2026/11/23/32-bit-apps-days-are-numbered-as-microsoft-strips-support-bit-by-bit-starting-with-windows-server-2028-but-windows-11-is-safe-for-now/) ⭐️ 7.0/10

微软在 Ignite 2026 上宣布，Windows Server 2028 将默认不再内置 WoW64 兼容子系统，因此开箱即无法运行 32 位应用程序。该系统计划于 2027 年秋季与 Windows 11 27H2 一同发布，需要 32 位兼容性的管理员可以通过“按需功能”（FoD）把 WoW64 加装回来，在 Server Core 上一般使用 PowerShell 或 DISM 完成。 WoW64 是让大量老旧 32 位 x86 软件能在现代 64 位 Windows 上继续运行的隐藏兼容层，把它改为可选意味着 IT 团队必须提前盘点服务器负载，并为升级后可能失效的遗留应用做迁移规划。这也表明微软有意最终在整个 Windows 产品线中淘汰 32 位兼容能力，尽管 Windows 11 客户端用户目前尚不受影响。 微软将这一改动定位为安全措施，用于缩小攻击面并阻止 32 位恶意软件，但它属于“默认不启用”而非彻底删除：WoW64 的按需功能包仍可从 Windows Update 或离线源安装。Server Core 环境没有图形界面，因此必须使用 PowerShell 或 DISM 而非“可选功能”向导来添加该功能，同时微软尚未公布在 Windows 11 中移除 WoW64 的计划。

telegram · zaihuapd · 11月23日 03:03

**背景**: WoW64（Windows 32-bit on Windows 64-bit）是负责转换 32 位 x86 应用调用的子系统，使这些程序能在 64 位 Windows 上运行，这也是许多遗留业务工具、安装程序和驱动至今仍可用的原因。按需功能（FoD）是指语言资源、.NET Framework 3.5 等未包含在默认映像中的可选 Windows 组件，可以之后从 Windows Update 或本地功能包源添加。Server Core 是不含桌面体验的最小化 Windows Server 安装选项，主要通过 PowerShell、DISM 和远程管理工具进行运维。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities?view=windows-11">按需功能 | Microsoft Learn</a></li>
<li><a href="https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/features-on-demand-language-fod?view=windows-11">语言和区域按需功能 (FOD) | Microsoft Learn</a></li>

</ul>
</details>

**标签**: `#Windows Server`, `#WoW64`, `#32-bit compatibility`, `#Microsoft`, `#legacy software`

---

<a id="item-10"></a>
## [特斯拉开始推送 FSD v15，带来类 GTA 的「Reality View」可视化界面](https://t.me/zaihuapd/45307) ⭐️ 7.0/10

特斯拉已在海外开始推送 FSD v15，官方称此次更新对端到端驾驶网络的各个部分都做了升级，安全关键场景的处理能力提升至 25 倍。本次更新还带来了全新的「Tesla Reality View」可视化界面，可在车机中控屏上叠加摄像头画面与 FSD 的行驶规划，并支持全屏、地图、分屏与安静模式。 FSD 是特斯拉的旗舰软件产品，也是其重要的营收押注，因此一个宣称安全性提升一个数量级的新版本，会同时牵动监管机构与已经在使用监督版 FSD 的数十万车主。炫目的 Reality View 还把驾驶界面重新围绕神经网络的规划意图来组织，这可能影响驾驶员建立信任并监督自动驾驶系统的方式。 除可视化外，v15 还新增了叠加在画面上的导航转弯提示、更轻柔并逐渐减弱的转向灯提示音，并优化了车辆碾过坑洼与路面碎片时的表现，以及学校周边和恶劣天气下的速度控制。特斯拉表示将在 12 月的 2026 年假日更新中全面推送，而「25 倍安全提升」目前只是公司自述，尚未获得第三方独立验证。

telegram · zaihuapd · 11月23日 03:33

**背景**: FSD（Full Self-Driving，完全自动驾驶能力）是特斯拉的高阶驾驶辅助软件包，目前以「监督版」形式销售，仍要求驾驶员保持注意力并随时接管。近几个版本依赖端到端神经网络，把摄像头输入直接映射为驾驶动作，而非依赖手写规则。Reality View 是一种实时生成的第三人称「跟随镜头」式渲染画面，常被比作《侠盗猎车手》（GTA），它把此前分散的多路可视化信号整合为单一视图，直观展示模型打算如何行驶。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.autoinsightreview.com/2026/11/22/tesla-fsd-v15-rollout-reality-view/">Tesla FSD v15 Begins Rolling Out With GTA-Style Reality View</a></li>
<li><a href="https://gizmodo.com/its-like-gta-musk-touts-video-game-like-update-to-tesla-fsd-2000843584">Tesla Adds GTA-Like Update to FSD</a></li>
<li><a href="https://www.zerohedge.com/technology/tesla-rolls-out-gta-style-reality-view-full-self-driving">Tesla Rolls Out "GTA-Style" Reality View For Full... | ZeroHedge</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous driving`, `#software update`, `#vehicle UI`

---