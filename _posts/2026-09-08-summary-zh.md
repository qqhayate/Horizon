---
layout: default
title: "Horizon Summary: 2026-09-08 (ZH)"
date: 2026-09-08
lang: zh
---

> 从 148 条内容中筛选出 12 条重要资讯。

---

1. [华为时隔六年携麒麟 9050 Pro 回归，首用逻辑折叠技术](#item-1) ⭐️ 9.0/10
2. [Qwen3.8-27B 任务感知量化以 15%体积达到 BF16 推理性能的 99%](#item-2) ⭐️ 8.0/10
3. [最高法发布 AI 纠纷司法解释，明确换脸、算法杀熟等责任](#item-3) ⭐️ 8.0/10
4. [谷歌 AI 将凝结尾迹增温在实测中降低 40%](#item-4) ⭐️ 8.0/10
5. [互动地图展示洛杉矶 1880 至 2026 年建筑建造年代](#item-5) ⭐️ 7.0/10
6. [加州理工首届研究级数学黑客松引发 AI 争论](#item-6) ⭐️ 7.0/10
7. [bzip3 热议：生态系统短板与基准测试误导](#item-7) ⭐️ 7.0/10
8. [滥用爬虫在 git.kernel.org 上消耗的 CPU 超过合法用户](#item-8) ⭐️ 7.0/10
9. [OpenAI 首席科学家呼吁构建对齐 AI 防御体系，警告勿鲁莽竞赛](#item-9) ⭐️ 7.0/10
10. [MiniCPM5-2B 发布，登顶 4B 以下开源模型排行榜](#item-10) ⭐️ 7.0/10
11. [开发者用 DeepSeek-V4-Flash-Vision-Exp 两天内构建游戏世界](#item-11) ⭐️ 7.0/10
12. [exllamav3 CPU 卸载推理在双 RTX 3080 上运行 Qwen3.8-Flash-Next，超越 llama.cpp](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [华为时隔六年携麒麟 9050 Pro 回归，首用逻辑折叠技术](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 9.0/10

9 月 7 日，华为在广州发布三折叠手机 Mate XT 2，搭载最新的麒麟 9050 Pro 芯片；这是继 Mate40 全球发布会之后，华为时隔六年首次在旗舰发布会推出全新麒麟芯片，也是首款采用逻辑折叠技术的高性能芯片。逻辑折叠让片内逻辑单元分层排布，并通过垂直互联通道（像加装“电梯”）缩短信号路径、降低时延。 时隔六年再次发布旗舰级新芯片，表明华为在制造条件受限的情况下仍能延续高端芯片设计创新。逻辑折叠把性能提升路径从单纯依赖尺寸微缩转向三维堆叠与先进封装，可能影响高端手机市场格局，并改变半导体行业的技术竞争逻辑。 逻辑折叠相当于把平层走线改为“立体大楼”：原本长距离横向互连缩短，信号直达、损耗降低，但也会带来散热、供电和设计复杂度等三维集成挑战；该技术契合华为 2026 年 5 月提出的“韬(τ)定律”，预计 2031 年基于该路线的高端芯片晶体管密度可达 1.4nm 制程同等水平。

telegram · zaihuapd · 9月7日 08:20

**背景**: 麒麟是华为旗舰智能手机的应用处理器家族；上一次在旗舰全球发布会上推出全新麒麟芯片还要追溯到 Mate40 时代，距今约六年。随后多年的外部限制，使华为获取先进制程代工和高端光刻设备受到制约。逻辑折叠属于三维集成电路（3D IC）与先进封装范畴，思路是把逻辑单元分层堆叠并用垂直互连代替平面长走线，相当于从单层平房改为立体互通大楼。与之配套的“韬定律”把这套思路概括为“以时间缩微替代几何缩微”，意在绕开受限于 EUV 光刻的传统微缩路径，继续提升芯片性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/逻辑折叠技术/67870423">逻辑折叠技术_百度百科</a></li>
<li><a href="https://semi.ofweek.com/2026-06/ART-202530-8420-30689144.html">华为 “ 韬定律 ” 与逻辑折叠技术，正在重构半导体的底层投资逻辑 - OF...</a></li>
<li><a href="https://www.guancha.cn/economy/2026_05_25_818264.shtml">华为 何庭波：今年麒麟芯片首次实施逻辑折叠技术，性能将大幅提升</a></li>

</ul>
</details>

**标签**: `#芯片`, `#华为`, `#半导体`, `#硬件`

---

<a id="item-2"></a>
## [Qwen3.8-27B 任务感知量化以 15%体积达到 BF16 推理性能的 99%](https://www.reddit.com/r/LocalLLaMA/comments/1wa5dp9/my_qwen3827b_taskaware_quant_reaches_99_of_bf16/) ⭐️ 8.0/10

作者发布了名为 TAK（Task Aware Knapsack）的任务感知量化流程，并将其应用于 Qwen3.8-27B。该 TAK 量化在推理基准上得到 82.81%，约为 BF16 成绩 83.59%的 99%，而体积约为 BF16 的 15%。 这一结果证明，任务感知的精度分配可以在不进行微调或剪枝的情况下，在极高压缩比下保留大部分推理能力。它可能让更强的模型在本地硬件上运行，并为 Unsloth 等通用静态量化方法提供了有基准数据支撑的替代方案。 TAK 先从任务特定语料库构建 imatrix，找到模型彻底崩溃前的最小体积，再在字节预算内对张量进行升级或降级分配。测试覆盖了 dense、QAT 和 MoE 架构；编码不是当前的目标领域，作者正在调查用户反馈的重复循环问题。

reddit · r/LocalLLaMA · /u/devildip · 9月7日 21:42

**背景**: 量化通过以较低数值精度存储权重来缩小模型体积，以少量精度损失换取内存节省；BF16 是常被视为高保真基线的 16 位浮点格式。极低位方案如 IQ2_S 可能导致能力急剧下降，而量化感知训练（QAT）通过微调让模型更能容忍压缩。TAK 则改用任务特定的校准数据来决定哪些张量应保留更高精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bfloat16_floating-point_format">bfloat16 floating-point format - Wikipedia</a></li>
<li><a href="https://unsloth.ai/docs/basics/dynamic-3.0-ggufs">Unsloth Dynamic 3.0 GGUFs | Unsloth Documentation</a></li>
<li><a href="https://pytorch.org/blog/quantization-aware-training/">Quantization - Aware Training for Large Language Models with...</a></li>

</ul>
</details>

**社区讨论**: 一些用户尝试用这个专注于推理的量化版本进行编码，遇到了重复循环问题。作者回应称编码不属于该模型的预期领域，并计划复现和描述这个失败案例。

**标签**: `#quantization`, `#efficient-LLMs`, `#reasoning`, `#Qwen`, `#local-LLM`

---

<a id="item-3"></a>
## [最高法发布 AI 纠纷司法解释，明确换脸、算法杀熟等责任](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

9 月 7 日，最高人民法院发布共 5 部分 24 条的人工智能纠纷案件司法解释。解释明确，未经同意用 AI 制作可识别的人脸、声音可能构成人格权侵权；算法价格歧视、AI 冒充他人代言诱导消费等行为需依法担责，并可支持惩罚性赔偿。 这是重要的监管里程碑，因为最高法院正在为人工智能相关纠纷设定具有约束力的法律标准，直接影响 AI 产品和平台的设计与部署方式。中国的开发者和企业今后在深度伪造、算法定价和 AI 冒充他人等方面将面对更清晰的责任规则。 该司法解释共 5 部分 24 条，涉及 AI 换脸、算法杀熟、AI 冒充代言、自动驾驶和知识产权等问题。解释还依法规制利用 AI 实施‘开盒’‘人肉搜索’等侵害自然人隐私权的行为，并明确 AI 冒充他人代言诱导消费的，可支持惩罚性赔偿请求。

telegram · zaihuapd · 9月7日 09:32

**背景**: 在中国的法律体系中，最高人民法院发布的司法解释为下级法院适用法律处理特定类型案件提供具有约束力的指引。‘大数据杀熟’指的是平台利用算法对老客户或忠实客户收取高于新客户的价格。‘开盒’是网络用语，指在网上公开他人隐私信息以进行骚扰的‘人肉搜索’式网络暴力行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/人肉搜索">人肉搜索 - 维基百科，自由的百科全书</a></li>
<li><a href="https://baike.baidu.com/item/开盒/58943997">开盒（网络热词）_百度百科</a></li>
<li><a href="https://news.bjd.com.cn/2025/03/15/11097249.shtml">“懂你”的 算 法 里，藏着 什 么 算 计？_ 京报网</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#deepfakes`, `#algorithm`, `#China`, `#legal liability`

---

<a id="item-4"></a>
## [谷歌 AI 将凝结尾迹增温在实测中降低 40%](https://finance.yahoo.com/technology/ai/articles/googles-ai-slashes-contrail-warming-215343560.html) ⭐️ 8.0/10

谷歌基于人工智能的凝结尾迹规避系统在一次真实航班测试中将尾迹增温降低了 40%。该测试验证了基于机器学习的航线规划可实际减少航空业在二氧化碳之外的气候影响。 由于凝结尾迹卷云是航空业对气候影响的最大因素之一，即使只调整少量航班也能带来显著的降温效益。这一结果支持在常规航班计划中使用 AI 预测，以减少航空业整体的环境足迹。 凝结尾迹规避是指预测会在空中形成持久凝结尾迹的区域，并调整飞行高度以避开；谷歌的测试主要针对尾迹增温最强的航班。搜索结果中引用的其他可行性试验在燃油消耗增加约 2%的情况下，使卫星可见凝结尾迹减少 64%，说明这种方法即使在额外油耗下仍能带来净气候收益。

openbb · AAPL · 9月7日 21:53

**背景**: 凝结尾迹是飞机排出的湿热废气在高空与寒冷空气相遇时形成的线状冰云。它们会困住地表向外散发的热量，从而加剧气候变暖，尤其当它们持续存在并扩展成卷云状云层时。以凝结尾迹卷云为主的航空业非二氧化碳增温效应，与二氧化碳影响相当。基于卫星数据训练的 AI 模型可以预测凝结尾迹可能在何处形成，从而支持通过调整航线来避免产生尾迹。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://scienceinsights.org/what-is-a-contrail-formation-types-and-climate-effects/">What Is a Contrail? Formation, Types, and Climate Effects</a></li>
<li><a href="https://www.iata.org/contentassets/726b8a2559ad48fe9decb6f2534549a6/aviation-contrails-climate-impact-report.pdf">Aviation contrails and their climate effect</a></li>
<li><a href="https://www.nature.com/articles/s44172-024-00329-7">Feasibility test of per-flight contrail avoidance in commercial aviation | Communications Engineering</a></li>

</ul>
</details>

**标签**: `#AI`, `#Climate Change`, `#Machine Learning`, `#Aviation`, `#Google`

---

<a id="item-5"></a>
## [互动地图展示洛杉矶 1880 至 2026 年建筑建造年代](https://lax-skyline.parcelscope.net/) ⭐️ 7.0/10

位于 lax-skyline.parcelscope.net 的交互式地图展示了洛杉矶各地建筑的建造年份，覆盖 1880 年至 2026 年。该可视化基于洛杉矶县税务评估官的地块记录，并通过 GIS 流程渲染呈现。 这幅地图让一个半世纪的城市开发历程一目了然，帮助居民、规划者和政策制定者观察密度、楼龄与社区变迁的模式。它也凸显了数据局限性——特别是仅展示现存建筑这一事实——如何影响人们对洛杉矶区划历史及当前住房可负担性危机的理解。 关键局限在于，这幅地图只显示至今仍存的建筑，因此类似 Palms 这样老建筑后来被逐栋替换的社区，在早期年代会显得几乎是空白，尽管它们在 19 世纪 90 年代曾有繁华的市中心。底层数据来自洛杉矶县税务评估官门户网站，有评论指出该图本质上就是这个数据集按建造日期进行可视化。

hackernews · rustywasm · 9月7日 18:52 · [社区讨论](https://news.ycombinator.com/item?id=49601655)

**背景**: 地理信息系统（GIS）用于对与地理位置关联的数据进行存储、管理和可视化；在这个项目中，它将地块级产权记录与交互式地图瓦片结合起来。Downzoning（降密度区划）是指降低某地块允许开发密度或强度的区划变更，例如把多户住宅用地改为单户住宅用地，从而可能限制住房供给。另有评论者提到，洛杉矶曾拥有美国最大的公共交通网络之一，但其中大部分后来被拆除以建设道路。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Geographic_information_system_(GIS)">Geographic information system (GIS)</a></li>
<li><a href="https://zoning.buildingclub.info/glossary/downzoning">What is Downzoning? Zoning Definition | Zoning Guide by ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍称赞这幅地图，但强调它反映的是现存建筑的年代，而非城市建筑历史的完整总量，因此像 Palms 这类被大规模重建的社区看起来远比其原始密度稀疏。一些评论者将地图呈现的格局与 1980 年代洛杉矶大规模降低密度区划联系起来，认为这人为限制了住房供给，使房东和房主受益，而损害了新来居民的利益。还有人补充历史背景，如该市曾拥有庞大的轨道交通网络；也有评论者认为地图只统计留存至今的建筑，因此有一定误导性。

**标签**: `#data visualization`, `#urban planning`, `#Los Angeles`, `#GIS`, `#housing`

---

<a id="item-6"></a>
## [加州理工首届研究级数学黑客松引发 AI 争论](https://mathathonchallenge.com/index.html) ⭐️ 7.0/10

加州理工学院的本科生宣布了 Mathathon 活动，称其为有史以来第一个专门面向研究级数学的黑客松。该活动强调负责任地使用 AI，并将把所有赞助资金用于支付评委和参与者的报酬。 该活动检验在 LLM 辅助发现的时代，短促而高强度的黑客松形式能否为数学研究带来有价值的贡献。其对'负责任地使用 AI'的强调，也切合当前关于 AI 生成的数学成果是否值得信任和认可的争论。 据组织者在 AMA 中的说明，团队由加州理工本科生组成，不代表加州理工或任何赞助商，组织者也不领取报酬。FAQ 页面详细说明了他们对负责任使用 AI 的承诺。

hackernews · astroanax · 9月7日 09:26 · [社区讨论](https://news.ycombinator.com/item?id=49596055)

**背景**: 黑客松传统上是限时的团队协作活动，侧重于快速构建原型或软件；而研究级数学通常需要长期、严谨的推理。此次 Mathathon 试图将两者结合，聚焦开放数学问题并引入 AI 工具，反映了利用 LLM 进行数学发现的更广泛趋势。这一公告既引发了热情，也引发了怀疑——人们不确定这种形式是否真的适合 LLM 数学研究实际的推进方式。

**社区讨论**: 评论中，一位组织者进行了 AMA，澄清团队的独立性以及资金用于支付评委和参与者；一位加州理工新近毕业生则将此次活动与该校正因 CS 系被认为薄弱、学生需要获得 AI 认可的动机联系起来。另一位评论者认为，花费 40 小时等待 LLM 输出与经典黑客松的吸引力完全相悖，也不符合目前 LLM 数学进展的实际产生方式。

**标签**: `#Mathematics`, `#AI`, `#Hackathon`, `#Caltech`, `#LLM`

---

<a id="item-7"></a>
## [bzip3 热议：生态系统短板与基准测试误导](https://github.com/iczelia/bzip3) ⭐️ 7.0/10

Hacker News 上一场讨论（372 分、106 条评论）深入探讨了开源压缩工具 bzip3，它基于 Burrows-Wheeler transform（BWT），被定位为 bzip2 的继任者。社区分析了现实使用中的权衡，指出常见数据工具对它的支持不足，并认为 bzip3 公布的基准测试有误导性，因为 zstd 的窗口大小被保留为默认值而未作匹配。 这一讨论很重要，因为 bzip3 的压缩率优于 bzip2 且解压更快，有助于降低归档存储成本。但它的软件生态支持有限，用户必须在原始压缩率与实际兼容性之间权衡；而不公平的基准测试也可能让用户做出糟糕的工具选择。 批评者指出，bzip3 以 512MB 的块大小参与基准测试，而 zstd 使用默认窗口（约 8MB），导致 zstd 无法有效利用重复文件之间的冗余。bzip3 结合了基于后缀数组的快速 BWT、order-0 context mixing 熵编码器，以及 LZ77/PPM 风格的 RLE 阶段；在早前讨论时，它也未列入 Matt Mahoney 的大型文本压缩基准。

hackernews · tosh · 9月7日 13:35 · [社区讨论](https://news.ycombinator.com/item?id=49598291)

**背景**: Burrows-Wheeler transform（BWT）会把字符串重排成相似字符聚集的形式，使 move-to-front 和游程编码更有效；bzip2 就把它作为核心预处理步骤。bzip3 是一个开源“精神继承者”，保留 BWT，并加入现代编码阶段以提高压缩率和解压速度。实际使用中，透明压缩支持往往起决定作用：DuckDB 能透明读取 gzip，也有 bzip2 扩展，但不支持 lzma 或 bzip3，因此有评论者为了兼容性最终选用 gzip 处理 JSONL 归档。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Burrows-Wheeler_Transform">Burrows-Wheeler Transform</a></li>
<li><a href="https://github.com/iczelia/bzip3">GitHub - iczelia/bzip3: A better and stronger spiritual ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Bzip2">bzip2 - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者参与度高但普遍持怀疑态度。有人分享说 lzma 压缩效果更好，却因生态支持而选择 gzip；另一些人认为基准测试“不诚实”甚至“精心挑选”，因为 zstd 窗口大小未匹配，并补充说含长重复的语料对 BWT 类压缩器最有利。他们建议用更大窗口测试 zstd、参考 bzip3 自身发布归档的压缩效果，并检查工作流中为其他压缩器选择的选项。

**标签**: `#compression`, `#bzip3`, `#benchmarking`, `#data-engineering`, `#open-source`

---

<a id="item-8"></a>
## [滥用爬虫在 git.kernel.org 上消耗的 CPU 超过合法用户](https://simonwillison.net/2026/Sep/7/creepy-crawlies/) ⭐️ 7.0/10

Konstantin Ryabitsev 发布了一篇题为 “Creepy crawlies” 的博文，报告称 git.kernel.org 花费在给恶意爬虫渲染 HTML 上的 CPU 周期，已经超过包括 git 克隆在内的所有其他合法访问。在任何时刻，该站点 5 个地理分布节点上有 14 个 CPU 核心正专门用于为这些爬虫把 git 提交渲染成 HTML。 这篇博文揭示了滥用爬虫（通常用于 AI 训练的机器人）给大型开源基础设施带来的隐性运营成本。对于 Datasette 这类有大量可抓取网页的服务，维护者在规划容量与防护措施时，必须把这类被浪费的计算资源考虑进去。 Ryabitsev 将这种流量描述为遍布 5 个地理分布节点的、持续存在的恶意爬虫“背景辐射”。与高效的 git clone 操作不同，每次请求 HTML 提交页面都需要服务器端渲染，这使得爬虫的每次请求成本要高得多。

rss · Simon Willison · 9月7日 23:08

**背景**: git.kernel.org 是 Linux 内核的官方 Git 仓库托管站点，也是最繁忙的开源基础设施站点之一。Git 通常通过命令行协议使用，而像 cgit 这类用 C 编写的高速 Git Web 前端，则让人们可以在浏览器中浏览提交历史和源代码。按需渲染内容丰富的 HTML 提交页面，比提供 git 协议数据要消耗多得多的 CPU。“滥用爬虫”是指大量抓取页面的自动化程序，它们常常无视 robots.txt，其请求对运维者来说就像持续存在的低可见度“背景辐射”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://git.zx2c4.com/cgit/about/">cgit - A hyperfast web frontend for git repositories written ...</a></li>

</ul>
</details>

**标签**: `#crawling`, `#git`, `#linux kernel`, `#web scraping`, `#operations`

---

<a id="item-9"></a>
## [OpenAI 首席科学家呼吁构建对齐 AI 防御体系，警告勿鲁莽竞赛](https://simonwillison.net/2026/Sep/7/jakub-pachocki/) ⭐️ 7.0/10

OpenAI 首席科学家 Jakub Pachocki 在题为"An Alien Mind"的文章中表示，继续快速训练更聪明模型的最有力理由，是构建防御系统以应对其他 AI 带来的危险。他主张需要强大且对齐的 AI 用于防御，同时强调这种紧迫性不能成为鲁莽竞赛的借口。 这一表态意义重大，因为一位顶尖 AI 安全人物公开将更快开发强大的对齐模型视为必要的防御手段，可能影响当前的 AI 监管与国际竞争政策辩论。这或许能让担心 AI 军备竞赛失控的人稍感安心，但也引发了关于如何平衡速度与安全性的疑问。 这段引文出自 OpenAI 文章中一个题为"Scalable Defense"（可扩展防御）的小节，Pachocki 将保护基础设施和实时防范恶意智能体列为核心防御任务。该声明承认预期中广泛 AI 进展带来的不确定性，并明确反对不计代价向前冲刺的观念。

rss · Simon Willison · 9月7日 22:26

**背景**: AI 对齐是 AI 安全的一个子领域，旨在让 AI 系统可靠地追求设计者期望的目标和价值观；未对齐的系统可能会以有害的方式行事。一些研究人员和公司高管认为，若不能妥善对齐，高度强大的未来 AI 可能危及文明，因此“用于防御的对齐 AI”被视为关键。关于是否应加速前进的争论，正是 AI 风险、监管与全球竞争力等更广泛讨论的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#OpenAI`, `#artificial intelligence`, `#AI alignment`, `#ethics`

---

<a id="item-10"></a>
## [MiniCPM5-2B 发布，登顶 4B 以下开源模型排行榜](https://www.reddit.com/r/LocalLLaMA/comments/1w9skjz/minicpm52b_release_day/) ⭐️ 7.0/10

OpenBMB 发布了 MiniCPM5-2B，这是一个 2.52B 参数的稠密小模型，在 Artificial Analysis Intelligence Index v4.2 上得分为 15，是 4B 及以下参数开源权重模型中的最高分。该模型已可在 Hugging Face 和 GitHub 上获取。 该发布表明小型开源模型也能提供领先的智能水平，使强大的大语言模型性能更容易用于本地、端侧和成本敏感场景。它强化了开源权重生态中追求高效模型设计的趋势。 该模型拥有 131k token 的上下文窗口，知识截止日期为 2025 年 12 月，并以 Apache 2.0 许可证发布。它面向本地助手、编程代理、工具调用工作流和推理场景设计，在 34 项基准测试中平均得分为 53.9。

reddit · r/LocalLLaMA · /u/Equivalent-Grass-527 · 9月7日 13:43

**背景**: Artificial Analysis Intelligence Index 是一个综合基准，通过多项评测来衡量推理、编程、知识和指令跟随等能力。MiniCPM 是 OpenBMB 推出的开源紧凑型模型系列，目标在于高效部署。在 4B 以下开源权重模型中取得最高分，表明小型与大型开源模型之间的差距正在缩小。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/openbmb/MiniCPM5-2B">openbmb/MiniCPM5-2B · Hugging Face</a></li>
<li><a href="https://artificialanalysis.ai/models/minicpm5-2b">MiniCPM5-2B - Intelligence, Performance & Price Analysis ...</a></li>
<li><a href="https://www.marktechpost.com/2026/09/07/openbmb-releases-minicpm5-2b-a-2-52b-dense-model-averaging-53-9-across-34-benchmarks-and-built-to-run-on-device/">OpenBMB Releases MiniCPM5-2B: A 2.52B Dense Model Averaging ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#open-weights`, `#model-release`, `#efficiency`, `#benchmark`

---

<a id="item-11"></a>
## [开发者用 DeepSeek-V4-Flash-Vision-Exp 两天内构建游戏世界](https://www.reddit.com/r/LocalLLaMA/comments/1wa06k3/deepseekv4flashvisionexp_is_amazing_at_creating/) ⭐️ 7.0/10

Reddit 上的一位开发者表示，DeepSeek-V4-Flash-Vision-Exp 能在约两天的测试与小改进中生成、调试并试玩一个完整的游戏世界。该模型借助视觉能力“查看”游戏截图，修正贴图、修复故障、编写动画脚本，并端到端测试 UI 与游戏机制。 这一演示凸显了一个实际转变：具备视觉能力的大语言模型现在可以打通代码与画面质量之间的闭环，充当自己的质检员和试玩员。这说明 AI 工具可能极大加速独立游戏开发者的创意原型制作，并降低打造精美互动世界的门槛。 DeepSeek-V4-Flash-Vision-Exp 是 DeepSeek-V4 系列首个实验性多模态模型；它是一个稀疏混合专家模型，总参数 284B，其中激活参数为 13B。该项目也建立在先前 Qwen3.8-Flash-Next 的工作之上——该模型一次性地生成了一个 Cat-Hunt 游戏演示；开发者后来还针对笔记本上的卡顿加入了性能优化。

reddit · r/LocalLLaMA · /u/sloptimizer · 9月7日 18:27

**背景**: 视觉语言模型（VLM）是一种多模态 AI 系统，接收图像和文本输入并生成文本输出，因此可以描述图片、读取截图中的文字、分析图表或用户界面。传统的纯文本大语言模型无法直观验证自己生成的内容，所以编码助手通常依赖人工检查输出。通过在 DeepSeek-V4-Flash 中加入视觉能力，模型能够截取它正在构建的游戏的真实截图，并迭代调整美术资源、动画和用户体验，直至画面看起来合理。这种开放式反馈回路对许多本地大模型爱好者来说是全新的；他们一直在探索小型及混合专家模型在多模态生产工作流中能走多远。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp">deepseek-ai/DeepSeek-V4-Flash-Vision-Exp · Hugging Face</a></li>
<li><a href="https://api-docs.deepseek.com/guides/vision/">Vision | DeepSeek API Docs</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-vision-exp">DeepSeek V4 Flash Vision Exp - API Pricing & Providers | OpenRouter</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#vision language model`, `#game development`, `#AI-assisted coding`, `#local LLM`

---

<a id="item-12"></a>
## [exllamav3 CPU 卸载推理在双 RTX 3080 上运行 Qwen3.8-Flash-Next，超越 llama.cpp](https://www.reddit.com/r/LocalLLaMA/comments/1wa1jkb/exllamav3_comfortably_beats_llamacpp_running/) ⭐️ 7.0/10

一位 Reddit 用户在双 RTX 3080（20GB）、128GB DDR4 内存和 Xeon 6148 上，用 Qwen3.8-Flash-Next 对比了 exllamav3 的 CPU 卸载推理与 llama.cpp。结果 exllamav3 解码约 25 tokens/s、预填充约 870 tokens/s，而 llama.cpp 解码约 13 tokens/s、预填充约 270 tokens/s。 这是首批公开对比结果之一，显示 exllamav3 的 CPU 卸载模式在消费级多 GPU 配置上胜过 llama.cpp，可能会影响在内存受限硬件上运行 Qwen3.8-Flash-Next 等 MoE 模型时的引擎选择。该优势因模型和配置而异，用户在切换前应自行对两个引擎进行基准测试。 这次 exllamav3 运行使用 Qwen 的 4.05-bit EXL3 量化，未启用多 token 预测（MTP），在 160k 上下文内解码稳定在约 25 tokens/s（峰值 32 tokens/s），并自评质量优于 Unsloth 的 Q4_K_XL GGUF。但在同一配置下，GLM 5.3 Flash 的 3.05-bit EXL3 量化解码速度约为 llama.cpp 的 1/2；解码速度还需数千 token 预热，用户怀疑 CPU 的 AVX2 性能是目前瓶颈。

reddit · r/LocalLLaMA · /u/Lowkey_LokiSN · 9月7日 19:16

**背景**: llama.cpp 和 exllamav3 等本地 LLM 推理引擎主要依赖消费级 GPU，而显存限制了可运行的模型大小。CPU 卸载（也称异构推理）会把部分模型权重放入系统内存，从而在较低速度下运行更大的模型。GGUF 与 EXL2/EXL3 是不同大小-质量权衡的量化/存储方案；EXL3 是 exllamav3 面向 NVIDIA GPU 推出的较新的优化格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/turboderp-org/exllamav3">GitHub - turboderp-org/exllamav3: An optimized quantization ...</a></li>
<li><a href="https://github.com/QwenLM/Qwen3.8-Flash-Next">GitHub - QwenLM/ Qwen 3 . 8 - Flash - Next : Qwen 3 . 8 - Flash - Next is the...</a></li>
<li><a href="https://www.hardware-corner.net/quantization-local-llms-formats/">Quantization for Local LLMs: How It Works and Which Formats Fit Your Setup</a></li>

</ul>
</details>

**标签**: `#exllamav3`, `#llama.cpp`, `#CPU offloading`, `#inference performance`, `#LocalLLaMA`

---