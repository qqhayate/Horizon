---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 70 条内容中筛选出 9 条重要资讯。

---

1. [PHP 紧急修复两项评分 9.2 的未授权远程代码执行漏洞](#item-1) ⭐️ 8.0/10
2. [苹果将于周三发布首款触屏 MacBook Pro](#item-2) ⭐️ 8.0/10
3. [十年前的老模型 Inception v3 经微调后在皮肤癌诊断上超越前沿大模型](#item-3) ⭐️ 7.0/10
4. [OpenAI 与 Anthropic 数月内将大模型 API 价格最高下调 80%](#item-4) ⭐️ 7.0/10
5. [俄勒冈警方为一名警员的记录报价 250 万美元与 44,816 小时](#item-5) ⭐️ 7.0/10
6. [菲尔兹奖得主博尔谢兹称 AI 让批改数学作业失去意义](#item-6) ⭐️ 7.0/10
7. [改装 RTX 3080 20GB 解锁 ReBAR 与 P2P，vLLM 预填充提速 70%–115%](#item-7) ⭐️ 7.0/10
8. [特斯拉自研 AI 地图将随 FSD v15 首发推送](#item-8) ⭐️ 7.0/10
9. [GEEKCON 上海站无人机攻防赛题引厂商报警，赛事一度暂停](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [PHP 紧急修复两项评分 9.2 的未授权远程代码执行漏洞](https://t.me/zaihuapd/44678) ⭐️ 8.0/10

PHP 团队发布了紧急安全更新，推出 PHP 8.5.12、8.4.27、8.3.36 和 8.2.35 版本，修复两个可让攻击者在无需登录的情况下远程执行代码的漏洞，两项漏洞的 CVSS 4.0 评分均为 9.2 分。官方敦促 PHP 8.2 至 8.5 的用户立即升级。 PHP 支撑着互联网上大量网站和应用，因此一个无需认证的远程代码执行漏洞几乎会波及所有使用受影响分支的站点，从小型博客到大型平台都可能中招。这些漏洞在所有常见的 PHP 请求处理方式下都可被触发，因此打补丁是紧迫的运维任务，而非例行维护。 该公告涵盖所有处理网页请求的部署方式，包括 PHP-FPM、Apache 的 mod_php、php-cgi、FrankenPHP 和 LiteSpeed；其中 mod_php 风险最高，因为已有验证表明攻击可在网站自身的业务代码运行之前就被触发。这意味着即使应用代码本身没有缺陷，存在漏洞的 Web 服务器仍可能被攻陷。

telegram · zaihuapd · 10月25日 02:42

**背景**: PHP 是一种服务端脚本语言，由称为 SAPI（服务器应用编程接口）的运行层来执行，不同 SAPI 会把它嵌入不同的 Web 服务器中：PHP-FPM 是一种 FastCGI 进程管理器，通常与 Nginx 搭配使用；mod_php 将解释器直接嵌入 Apache；php-cgi 是较老的 CGI 实现；FrankenPHP 是构建在 Caddy Web 服务器之上的新型应用服务器；LiteSpeed Web Server 则是兼容 Apache 的专有商业服务器。由于这些组件位于应用程序之前，其自身的缺陷可能被任意传入的 HTTP 请求触发。CVSS 4.0 评分超过 9.0 即属于“严重”级别，9.2 分说明利用难度低且危害极大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.php.net/manual/en/install.fpm.php">PHP: FastCGI Process Manager (FPM) - Manual</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP: the modern PHP app server</a></li>
<li><a href="https://www.litespeedtech.com/products/litespeed-web-server">LiteSpeed Web Server - Apache Alternative - LiteSpeed Technologies</a></li>

</ul>
</details>

**标签**: `#php`, `#security`, `#vulnerability`, `#rce`, `#patching`

---

<a id="item-2"></a>
## [苹果将于周三发布首款触屏 MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 8.0/10

苹果将于本周三发布首款触屏 MacBook Pro，这是 Mac 产品线首次同时引入触摸输入和 OLED 屏幕，并加入灵动岛设计。新品包含 14 英寸和 16 英寸两个版本，起售价将高于现款的 2499 美元。 这是苹果一次重大的战略转向：多年来苹果高管一直以人体工学理由公开否定笔记本触屏，如今改变立场将重新定义整个高端笔记本品类的预期。这也反映出苹果姿态的转变——不再一味固执己见、要求行业跟随自己，而是更愿意反思和调整，而营收与营销很可能是主要驱动力。 触控将作为键盘和触控板的补充而非替代性输入方式，OLED 面板与灵动岛则沿用了 iPhone 上的成熟方案。14 英寸和 16 英寸机型的售价将高于目前 2499 美元的起售价，消费者需为此支付溢价。

telegram · zaihuapd · 10月25日 14:25

**背景**: OLED（有机发光二极管）屏幕由每个像素自行发光，无需背光，因此能实现更深的黑色、更高的对比度和更薄的机身——苹果已在 iPhone 和 Apple Watch 上使用该技术，但此前从未用于 Mac。灵动岛是苹果 2022 年随 iPhone 14 Pro 推出的药丸形摄像头开孔区域，同时可作为实时活动和系统提示的交互式界面。在此之前，苹果高管一直主张触摸竖直的笔记本屏幕会导致手臂疲劳，并称 macOS 是为鼠标和触控板这类间接输入而设计的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OLED">OLED - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Dynamic_Island">Dynamic Island</a></li>
<li><a href="https://grokipedia.com/page/Dynamic_Island">Dynamic Island</a></li>

</ul>
</details>

**标签**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#OLED`, `#hardware`

---

<a id="item-3"></a>
## [十年前的老模型 Inception v3 经微调后在皮肤癌诊断上超越前沿大模型](https://lynchlab.net/llm-skin-cancer) ⭐️ 7.0/10

一位博主使用单块 H100 GPU，在来自 ISIC 档案库的 68,011 张皮肤镜与临床图像上对约 2015 年问世的卷积网络架构 Inception v3 进行微调，随后在 200 个留出的皮肤病变样本上与前沿大语言模型进行对比。这十年前的专用小网络在皮肤癌判别上据称优于通用大模型，该文章在 Hacker News 上获得了 413 个赞和约 200 条评论。 这一实验为当下的大模型热潮提供了一个具体的反例：在黑色素瘤筛查这类狭窄但高风险的任務上，一个低成本训练的小型专用分类器就能胜过参数规模巨大的通用模型。它提示，许多医疗和工业 AI 应用的务实路径是利用大模型去孵化专用模型，而不是直接把大模型当作最终产品部署。 该模型以在普通照片上预训练的 Inception v3 权重为起点，并对全部层进行了微调；关键在于，200 个测试病变的影像以及同一患者的其他照片都已从训练集和验证集移除，也未用于挑选模型或设定阈值。不过评论者仍指出测试集规模过小，属于“刷榜”（benchmaxxing），并认为针对基准优化的模型通常会在自己的基准上胜过通用模型。

hackernews · sungam · 10月25日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50233779)

**背景**: Inception v3 是谷歌于 2015 年底发布的卷积神经网络架构，它通过并行使用不同尺寸的卷积核来高效提取图像特征，因此成为迁移学习中常用的骨干网络。ISIC 档案库是由国际皮肤影像协作组织（ISIC）维护的大型公开皮肤病变皮肤镜图像集，被广泛用于训练和评估自动化黑色素瘤检测系统。卷积神经网络（CNN）通过堆叠可学习的滤波器来处理图像，这种面向视觉任务的方式与前缀大语言模型所基于的 token 化 Transformer 架构本质不同，通常在样本效率上更高。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/machine-learning/understanding-googlenet-model-cnn-architecture/">Understanding GoogLeNet Model - CNN Architecture - GeeksforGeeks</a></li>
<li><a href="https://api.isic-archive.com/doi/melanoma-and-nevus-dermoscopy-images-with-confirmed-histopathological-diagnosis/">Melanoma and Nevus Dermoscopy Images with Confirmed...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的普遍反应是“这不明摆着吗”：评论者认为，任何规模化应用都应由专用分类器承担，其精度会高于通用大模型，而大模型的主要价值在于把构建这类专用模型的成本压到近乎为零。还有人指出其中的讽刺意味——几年前人们曾用医疗应用来为大模型的外部性辩护；而持怀疑态度的评论者则称该结果属于针对基准的优化，并把它比作计算器在乘法上完胜大模型。

**标签**: `#machine-learning`, `#medical-ai`, `#computer-vision`, `#llm`, `#model-specialization`

---

<a id="item-4"></a>
## [OpenAI 与 Anthropic 数月内将大模型 API 价格最高下调 80%](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 7.0/10

2026 年 10 月发布于 minimaxir.com 的一篇分析文章指出，OpenAI 与 Anthropic 在短短数月内将自家大语言模型 API 的价格最高下调了 80%。文章认为，如此大幅度的降价是正面竞争、推理成本优化、开放权重模型带来的压力以及为重大商业节点做战略布局等多重因素共同作用的结果。 更便宜的 token 直接降低了开发者和创业公司基于这些 API 构建产品的门槛，同时也压缩了所有无法跟进这一价格水平的厂商的利润空间。降价还把竞争优势从单纯的模型质量转向服务经济性，这意味着最终胜出的可能不是榜单分数最高的公司，而是推理栈优化最彻底的公司。 这些降价与其说是让利，不如说是工程能力的体现：在 2026 年，朴素部署的模型与经过量化、连续批处理、KV 缓存管理、提示缓存和请求路由等优化的推理栈之间，在相同硬件上的吞吐量——也就是单 token 成本——差距约为 10 倍。不过文章的观点存在争议，因为公开评论指出两家实验室在研发与算力扩张上仍在亏损数十亿美元，因此降价既可能是效率提升的结果，也可能是竞争压力下的无奈之举。

hackernews · minimaxir · 10月25日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50236102)

**背景**: 大语言模型通常通过 API 按每百万输入和输出 token 计价出售，这一价格必须覆盖 GPU 时间、电力以及数据中心的开销。由于模型服务成本高昂，厂商会在推理优化上大量投入——例如量化（用更低精度运行权重）、将大量请求合批处理、缓存重复的提示前缀等技术——以提升单块 GPU 的吞吐量。与此同时，来自 DeepSeek、Qwen、GLM、Kimi 等中国实验室的开放权重模型（即训练好的参数以许可证形式公开，这与完全开源的 AI 不同）为客户提供了可自行部署或廉价托管的替代方案，从而给闭源厂商的定价设置了天花板。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ailearningguides.com/llm-inference-optimization-2026-serving-batching-kv-cache/">LLM Inference Optimization 2026: Serving, Batching, KV Cache</a></li>
<li><a href="https://atlan.com/know/ai-agent/llm-cost-optimization-strategies/">LLM Cost Optimization Strategies: Complete Tactics List [2026]</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍对两家公司的叙事持怀疑态度：有人认为 OpenAI 和 Anthropic 亏损数十亿美元并非因为研发投入，而是因为大模型本身还不是一门可持续的生意， favorable 的媒体报道与 IPO 布局只是掩盖了这一点。也有人把降价归因于竞争，称自己在遭遇美国 API 的拒答和“网络安全”拦截后转用 Kimi 与 GLM，发现成本低得多；还有评论者认为推动监管的部分动机就是把中国的开放模型挡在门外。另有一条更技术性的讨论拆解了 DeepSeek 宣称的 Flash V4 每 GPU 每小时约 38 美元收入，暗示规模更大的实验室仍有降价空间。

**标签**: `#LLM pricing`, `#AI economics`, `#OpenAI`, `#Anthropic`, `#AI competition`

---

<a id="item-5"></a>
## [俄勒冈警方为一名警员的记录报价 250 万美元与 44,816 小时](https://theintercept.com/2026/10/01/oregon-police-misconduct-public-records-cost-fee/) ⭐️ 7.0/10

据 The Intercept 报道,俄勒冈州尤金市警察局告知一家当地新闻媒体,要处理一项针对单名警员的公共记录申请,至少需要 44,816 小时的员工工时,费用约为 2,484,599.04 美元。这一估算相当于约 21 年的工作量,实际上等于把一项常规的透明性申请标价到新闻机构无法承受的地步。 高昂到无法承担的报价,是在不正式拒绝申请的前提下让公共记录法失效的最有效手段之一,而这起事件为透明度倡导者提供了一个具体且有数字支撑的案例。如果这种做法被认可,任何机构只要开出一张无法支付的账单,就能把不当行为记录挡在公众监督之外。 这一报价针对的仅是一名警员,却需要 44,816 小时工时,相当于一名全职员工二十多年的工作量。俄勒冈州的公共记录法允许机构收取员工工时费用,也允许申请人向州总检察长申请复核,但真正引人关注的是这份估算的规模,而非收费机制本身的存在。

hackernews · tdeck · 10月25日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=50234232)

**背景**: 美国《信息自由法》(FOIA) 于 1966 年通过,仅适用于联邦机构;向市警察局等州及地方机构提出的申请,则受俄勒冈州公共记录法等各州法规约束。联邦与州法律通常都允许机构收回检索、审阅和删减文件的成本,多数还规定可为公共利益(如新闻报道)减免费用,但申请人往往需要自行争取。因此在实际操作中,机构可以通过给出高额估算来拖延或阻止信息公开,这种做法长期受到记者和透明度组织的批评。

**社区讨论**: Hacker News 的评论者几乎一致认为 250 万美元的报价荒谬至极,有人指出 44,816 小时相当于约 21 年的员工工时。其他人则描述了另一种阻挠手段——某学区每月只挤出少量记录分批交付——并作出国际对比:英国要求在 30 天内答复申请,而德国政客(如延斯·施潘)正推动立法允许这类高得离谱的收费。还有评论者回忆起 2015 年美国国防部对一项 FOIA 申请给出的 1500 万小时、6.6 亿美元的估算。

**标签**: `#government-transparency`, `#FOIA`, `#public-records`, `#civil-liberties`, `#policy`

---

<a id="item-6"></a>
## [菲尔兹奖得主博尔谢兹称 AI 让批改数学作业失去意义](https://www.dailycal.org/news/campus/academics/ai-use-leads-uc-berkeley-math-professor-to-see-no-point-in-grading-homework/article_bdf1eae2-c08b-491f-b9f1-81a7cea177de.html) ⭐️ 7.0/10

加州大学伯克利分校数学家、1998 年菲尔兹奖得主理查德·博尔谢兹公开表示，既然 AI 工具可以随时解出常规作业题，继续批改作业已经“没有意义”。据校媒《Daily Californian》报道，他的这番言论在 Hacker News 上引发了一场多达 279 条评论的激烈讨论，话题聚焦于考核方式与学术诚信。 这一观点出自世界最知名的数学家之一，因而使“LLM 时代课后作业不再能可靠衡量学习效果”这一正在教师群体中蔓延的情绪获得了格外的分量。如果各院系依此逻辑行事，可能会加快整个 STEM 高等教育转向课堂内考核或口试式评估的步伐。 博尔谢兹本人很可能多年未亲自批改作业，因为拥有科研经费的终身教授通常把批改工作交给研究生助教——评论者指出这正是其中的讽刺之处。讨论还涉及作业的真正价值究竟在于反馈过程还是分数本身。

hackernews · romanhn · 10月25日 16:28 · [社区讨论](https://news.ycombinator.com/item?id=50233304)

**背景**: 理查德·博尔谢兹因证明“魔群月光”猜想（该猜想把模函数与魔群表示联系起来）于 1998 年获得菲尔兹奖，他还以在 YouTube 上发布大量数学讲座视频而闻名。ChatGPT、Claude 等大语言模型如今能够逐步解出许多教材级别的数学题，这令人担忧学生提交的作业不再反映其自身的理解。各高校已推出从荣誉守则到口试答辩、课堂闭卷考试等一系列应对政策。

**社区讨论**: Hacker News 上的讨论整体上对取消评分持怀疑态度：多位评论者认为，即便是抄袭或互相合作，也迫使学生接触学习材料，而 AI 彻底消除了这种“强制机制”。也有人讽刺地指出博尔谢兹本就把批改工作交给助教，还有人借用《魔鬼经济学》式的思路建议：教师在课堂上随机点名让学生口头讲解解题过程，以抽查其真实理解。

**标签**: `#AI in education`, `#academic integrity`, `#LLMs`, `#pedagogy`, `#higher education`

---

<a id="item-7"></a>
## [改装 RTX 3080 20GB 解锁 ReBAR 与 P2P，vLLM 预填充提速 70%–115%](https://www.reddit.com/r/LocalLLaMA/comments/1xf9kmd/rtx_3080_20gb_got_rebar_and_p2p_unlock_70_prompt/) ⭐️ 7.0/10

一位社区改装者在改装版 20GB RTX 3080 上解锁了 PCIe 点对点（P2P）DMA 和 Resizable BAR，并在双 GPU Threadripper 1920X 系统的 vLLM 0.32.0 张量并行推理中进行了基准测试。相比原始配置，GPU 解锁+ReBAR+P2P 组合将提示处理吞吐量提升了 71%–115%，仅 P2P 相对 GPU 解锁也有最高约 70%的增益。 这一点很重要，因为张量并行 LLM 服务高度依赖 GPU 间通信，而更快的预填充会直接改善廉价多 GPU 平台上的长上下文和智能体工作负载。它表明改装消费级显卡可以在本地推理中缩小与更昂贵数据中心硬件的一部分差距。 加速在 8K 提示时最大（相对原始配置提升 115%），到约 262K token 时缩小至 71%；而 token 生成的令牌间延迟基本落在噪声范围内，P2P 没有带来一致收益。测试使用两个 PCIe 3.0 x16 插槽、每 GPU 240W 功耗上限、FP8 KV 缓存、分块预填充和 FlashInfer 注意力后端。

reddit · r/LocalLLaMA · /u/No-Refrigerator-1672 · 10月25日 18:16

**背景**: Resizable BAR 允许 CPU 访问 GPU 的完整帧缓冲，而不是仅能访问一个很小的 256MB 窗口，从而可能提升内存传输效率；NVIDIA 在 2021 年为 RTX 30 系列显卡加入了对该功能的支持。P2P DMA 允许 GPU 通过 PCIe 直接交换数据，而无需经过主机内存中转，这一功能在消费级 GeForce 显卡上通常被禁用。vLLM 的张量并行会将模型权重拆分到多块 GPU 上，并需要频繁的 all-reduce 通信，因此互连效率会强烈影响提示处理性能。RTX 3080 20GB 并非官方零售型号，而是通过硬件改装将显存翻倍而来，因此这些解锁对硬件爱好者尤其有意义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/geforce/news/geforce-rtx-30-series-resizable-bar-support/">GeForce RTX 30 Series Performance Accelerates With Resizable ...</a></li>
<li><a href="https://docs.vllm.ai/en/latest/serving/parallelism_scaling/">Parallelism and Scaling - vLLM</a></li>
<li><a href="https://medium.com/gpu-kernel-hacking-for-engineers/part-2-inter-gpu-communication-with-pcie-nvlink-and-bars-19c20d367f44">Part 2: Inter- GPU Communication with PCIe, NVLink, and... | Medium</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#gpu-hardware`, `#vllm`, `#tensor-parallelism`, `#inference-performance`

---

<a id="item-8"></a>
## [特斯拉自研 AI 地图将随 FSD v15 首发推送](https://www.digitaltoday.co.kr/en/view/118497/tesla-to-build-in-house-maps-and-navigation-to-address-fsd-limits) ⭐️ 7.0/10

在特斯拉 2026 年第三季度财报电话会上，特斯拉 AI 副总裁 Ashok Elluswamy 宣布公司正在构建自研的 AI 地图与导航架构，并将随 FSD v15 首次推送。该系统最初将用于行程的出发与到达阶段，随后在数月内逐步扩展到导航与泊车环节。 这是一次值得注意的战略转向：特斯拉此前长期主张自动驾驶不应依赖地图，而自研地图栈说明纯视觉 FSD 仍存在外部地图（或完全无图）无法弥补的缺口。如果落地顺利，它有望修复外界广泛反映的 FSD 在限速识别、泊车和路线选择方面的短板，惠及约 174 万名 FSD 订阅用户，同时降低对第三方地图供应商的依赖。 该系统基于特斯拉自有车队采集的道路数据构建，主打改善限速识别、泊车与路线选择，并支持语音指令和个性化路线偏好。不过此次仅为战略层面公布——除将随 FSD v15 推送外，未披露技术架构细节、精度目标或明确的落地时间表，且首个版本只覆盖行程的出发与到达阶段，而非完整的门到门导航。

telegram · zaihuapd · 10月25日 10:57

**背景**: 特斯拉的 Full Self-Driving（FSD）是一套以摄像头和神经网络为主、不依赖预先构建的高精地图的辅助驾驶系统，特斯拉一直主张这种路线比 Waymo 等竞争对手依赖高精地图的 Robotaxi 方案更具可扩展性。地图之所以重要，主要在于感知能力较弱的环节——例如某段道路的准确限速值，或停车场入口应走哪条车道——因为这些信息依赖静态知识，而非摄像头当下的所见。特斯拉做地图的优势在于车队规模：在路上行驶的车辆可持续采集摄像头与道路数据，这与 Uber 等公司把车辆视作传感器网络的做法类似。此次是特斯拉首次承诺自建 AI 地图层，背景是股东对 FSD 在导航、泊车和限速方面表现的批评。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.digitaltoday.co.kr/en/view/118497/tesla-to-build-in-house-maps-and-navigation-to-address-fsd-limits">Tesla to build in-house maps and navigation system to address ...</a></li>
<li><a href="https://www.notateslaapp.com/news/4868/tesla-is-building-its-own-ai-maps-starting-with-fsd-v15">Tesla Is Building Its Own AI -Based Maps , Will Begin... - Not a Tesla App</a></li>
<li><a href="https://tech-insider.org/tesla-own-maps-fsd-v15-elluswamy-2026/">Tesla Builds Own FSD Maps, Starting With v15 [2026]</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous driving`, `#AI maps`, `#navigation`

---

<a id="item-9"></a>
## [GEEKCON 上海站无人机攻防赛题引厂商报警，赛事一度暂停](https://tech.ifeng.com/c/8xSZe56UAz6) ⭐️ 7.0/10

10 月 24 日晚闭幕的 GEEKCON 上海站上，据称一项无人机攻防赛题导致某头部无人机厂商报警，相关人员被带走，赛事一度暂停。该赛题要求选手突破 GPS 禁飞限制，并夺取无人机的完整控制权。 这一事件让白帽研究与厂商协同披露之间的边界再次成为焦点，也使外界质疑赛事主办方与研究者能否安全地演示真实的无人机漏洞。它可能影响国内未来安全竞赛对硬件与物联网赛题的设计方式，以及厂商和执法部门对公开演示漏洞的应对方式。 该报道篇幅简短，既未点名涉事厂商，也未确认被带走人员的后续法律结果，因此报警的具体性质仍不清楚。GEEKCON 每年 10 月 24 日举办，官方赛题中本就设有无人机与机器人安全赛道，并长期获得华为、腾讯安全和蚂蚁集团等大厂赞助。

telegram · zaihuapd · 10月25日 13:29

**背景**: GPS 地理围栏是消费级无人机固件层面的功能，会在机场、敏感区域等指定禁飞区内阻止起飞或飞行；绕过这一限制与 GPS 欺骗、Wi-Fi 劫持、固件利用一样，都是业界熟知的研究课题。GEEKCON（前身为 2014 年由 DARKNAVY 创办的 GeekPwn）这类安全赛事通过现场演示漏洞来证明问题真实存在，但公开演示可用的绕过手段，可能与无线电干扰、航空安全及非授权访问相关法规相冲突。厂商通常更倾向协同披露，即研究者私下上报漏洞，待修复后再公开细节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geekcon.top/2025/">GEEKCON· New GeekPwn</a></li>
<li><a href="https://geekcon.top/doc/GEEKCON-2025-Call-for-Participation.pdf">GEEKCON 2025 Call for Participation</a></li>
<li><a href="https://journals.stmjournals.com/ijd/article=2025/view=227626/">A Study On Drone Hacking: Vulnerabilities And Mitigation ...</a></li>

</ul>
</details>

**标签**: `#security research`, `#drone security`, `#responsible disclosure`, `#GEEKCON`, `#legal boundaries`

---