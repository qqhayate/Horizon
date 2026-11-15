---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 86 条内容中筛选出 12 条重要资讯。

---

1. [SpaceX 用机械臂捕获星舰上级，Flight 15 圆满收官](#item-1) ⭐️ 9.0/10
2. [Lovable 生成的应用因 RLS 配置不足泄露护照信息与逾 20 万条私信](#item-2) ⭐️ 8.0/10
3. [报道称英伟达通过循环融资维持 GPU 高价](#item-3) ⭐️ 7.0/10
4. [PyPI 推出全新项目页面，突出安全与来源溯源信号](#item-4) ⭐️ 7.0/10
5. [Show HN：用约 200 行纯 JAX 代码复现 DeepSeek V3 架构](#item-5) ⭐️ 7.0/10
6. [Google Project Zero 将漏洞披露期限逐步缩短至 60 天乃至 30 天](#item-6) ⭐️ 7.0/10
7. [CBC 调查后，LinkedIn 与 Monster 下架逾千条虚假招聘信息](#item-7) ⭐️ 7.0/10
8. [EFF 指出：科技公司再次重新定义隐私，以将 AI 数据采集正常化](#item-8) ⭐️ 7.0/10
9. [意大利因未经同意读取相册对 Meta 罚款 8.05 亿欧元](#item-9) ⭐️ 7.0/10
10. [SpaceX 下月将首次尝试同时回收星舰飞船与超级重型助推器](#item-10) ⭐️ 7.0/10
11. [Cloudflare 开源 Kitesurf：为 AI 代理打造的无状态浏览器](#item-11) ⭐️ 7.0/10
12. [星舰入轨但助推器爆炸，双塔捕回收落空](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [SpaceX 用机械臂捕获星舰上级，Flight 15 圆满收官](https://www.spacex.com/launches/starship-flight-15) ⭐️ 9.0/10

在星舰 Flight 15 任务收官阶段，SpaceX 位于得克萨斯州星舰基地的发射塔用巨大的“筷子”机械臂在空中接住了从太空返回的星舰上级（Ship 42）。而超重型助推器（Super Heavy）的回收捕获在飞行早期被中止，因此本次任务只完成了单次捕获，而非外界期待的“双捕获”。 回收上级是复用难题中更困难的一半，因为星舰必须扛住再入大气层的高温并且仍可再次使用；成功捕获意味着这枚全球最大火箭的两级都已在发射塔完成回收。如果星舰能够被快速捕获、检修并再次飞行，入轨载荷成本有望大幅下降，这将支撑 SpaceX 的星链扩张、NASA 的月球着陆器项目以及马斯克的火星计划。 助推器捕获失败的原因是超重型助推器的制导、导航与控制（GNC）系统出现故障，因此本次只回收了星舰上级；SpaceX 表示已基本查明故障原因。接下来的关键节点是实现真正的“双捕获”，然后让已被捕获过的星舰再次飞行并再次被捕获，而星舰的隔热瓦被认为是目前最大的未知因素。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**背景**: 星舰是 SpaceX 研制的完全可复用两级超重型运载火箭，由超重型一级和星舰上级组成，两级都设计为由位于得州星舰基地、绰号“Mechazilla”的发射塔用“筷子”机械臂在空中直接夹住回收。相比用着陆腿降落，直接捕获可省去着陆硬件的重量，并让飞行器直接回到发射台以便快速检查和复飞。SpaceX 早在 2024 年 10 月的 Flight 5 中首次成功捕获超重型助推器，但上级此前一直只能在海上溅落。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.zerohedge.com/technology/watch-live-spacex-targets-historic-starship-booster-double-chopsticks-catch">Elon Musk's 'Mechazilla' Catches Starship Rocket In... | ZeroHedg...</a></li>
<li><a href="https://www.space.com/space-exploration/launches-spacecraft/spacex-chopsticks-catch-starship-upper-stage-flight-14">'Now everything changes': SpaceX catches Starship upper stage ...</a></li>
<li><a href="https://www.space.com/spacex-starship-flight-5-launch-super-heavy-booster-catch-success-video">SpaceX catches giant Starship booster with 'Chopsticks' on ...</a></li>

</ul>
</details>

**社区讨论**: 评论区几乎是一边倒的兴奋，许多人称这是新时代的开端，并把星舰形容为“做对了的航天飞机”：没有固体助推器、轨道器叠在箭体上方而非侧挂，从而规避了挑战者号与哥伦比亚号事故的失效模式，而且采用流水线式制造。讨论中提出的主要技术疑虑是隔热瓦能否扛住再入，以及最终入轨质量比会是多少；有评论者指出，即便性能有所牺牲，完全可复用的飞行器仍优于猎鹰 9 这类部分复用（按成本计约 60% 可复用）的方案。

**标签**: `#SpaceX`, `#Starship`, `#reusable rockets`, `#spaceflight`, `#aerospace engineering`

---

<a id="item-2"></a>
## [Lovable 生成的应用因 RLS 配置不足泄露护照信息与逾 20 万条私信](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

发布于 crissyfield.de 的一份安全研究报告指出，使用 AI 应用构建平台 Lovable 生成的多款 Web 应用暴露出敏感用户数据——包括护照信息和超过 20 万条私信——原因是这些应用背后的 Supabase 数据库缺少足够的行级安全（RLS）策略。作者表示，攻击者无需高深黑客技术，仅通过查看浏览器中的网络请求就能访问这些数据。 该事件凸显了快速扩张的“vibe coding”生态中的系统性风险：AI 构建工具能在几分钟内产出可用应用，但其底层的安全默认配置（尤其是数据库访问控制）往往形同虚设，而这类应用数量庞大、易于探测，使用者又无法判断风险高低。由于 Lovable 的安全负责人亲自参与讨论，舆论焦点已从指责单个用户转向平台在安全默认值上应承担的责任。 根本原因是 Supabase/Postgres 数据表上的行级安全策略不足，使未认证或低权限客户端能够读取本不该可见的数据行。Lovable 表示会在每次发布前自动扫描应用，并提供免费的深度 SAST 扫描，同时支持一键“修复”、后台自动修复以及在发现问题时阻止发布；但评论者指出，Supabase 针对老项目的宽松默认设置在 10 月 30 日的修复之后据称仍然存在。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**背景**: Lovable 是一款 AI 应用构建工具，可将一段文字提示直接变成可运行的 Web 应用，通常会接入 Supabase 作为后端，用于身份认证和 Postgres 数据库。行级安全（RLS）是 PostgreSQL 内置的授权机制，用于限定某个用户能查询或修改哪些数据行，而 Supabase 正是依靠 RLS 策略加上表级授权来保护通过其自动生成 API 暴露的数据。若未启用 RLS 或策略写得过于宽松，前端中公开的 API key 就足以让任何人读取其他用户的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supabase.com/docs/guides/database/postgres/row-level-security">Row Level Security | Supabase Docs</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>

</ul>
</details>

**社区讨论**: 这条获得 279 条评论的讨论整体对研究者表示支持，但在责任归属上存在分歧：一些评论者认为 Supabase 为降低上手门槛而长期采用宽松默认设置，应负很大责任；另一些人则认为 Lovable 这类平台必须采用默认拒绝的数据库、最小权限 API 和自动化认证测试。也有人指出，数据泄露早在 AI 出现之前就存在，但 AI 生成的应用具有易被利用、数量极多、使用者对风险毫不知情等特点。

**标签**: `#security`, `#Supabase`, `#AI-generated apps`, `#data breach`, `#row-level security`

---

<a id="item-3"></a>
## [报道称英伟达通过循环融资维持 GPU 高价](https://www.techspot.com/news/114558-nvidia-deliberately-kept-gpu-prices-high-through-circular.html) ⭐️ 7.0/10

TechSpot 的一篇文章（在 Hacker News 上引发长篇讨论）指称，英伟达有意通过循环融资交易——即向 AI 初创公司和“新云”（neocloud）提供商投资或提供信贷，而这些公司随后用这笔钱购买英伟达 GPU——来维持 GPU 价格高企，并让竞争对手更难获得供货。该文被定位为对英伟达交易行为的分析评论，而非经过核实的调查结论，英伟达也未确认这一说法。 英伟达的 GPU 几乎是所有前沿 AI 训练与推理的瓶颈资源，因此任何抬高芯片价格或限制竞争对手供货的策略，都会直接影响整个 AI 行业的成本结构。这些指控还与既有的针对英伟达市场支配地位的的反垄断审查相呼应，并卷入“当前 AI 基建狂潮究竟是真实的算力短缺，还是融资驱动的泡沫”这一争论。 评论者举出了具体的价格证据：96GB 的 RTX 6000 Blackwell 原始建议零售价约为 8000 美元，但在所谓的“稀缺”之下实际售价已高达约 16000 美元。持怀疑态度的反方观点则认为，多数需求侧数据——包括高企的 GPU 租赁价格以及各大云厂商和推理服务商的公开表态——都表明算力确实供不应求，因此这些交易的目的可能是把竞争对手挡在供应链之外，而非人为制造需求。

hackernews · madihaa · 11月14日 22:26 · [社区讨论](https://news.ycombinator.com/item?id=50501631)

**背景**: “循环融资”是互联网泡沫时代“供应商融资”的现代翻版，指芯片厂商或云服务商向客户提供资金、担保或采购承诺，客户再用这些资源购买其硬件和服务，从而使供应商计入的收入部分源自自己的资金。英伟达此前大举投资领先的 AI 初创公司以及“新云”（出租 GPU 算力的新兴服务商），这被拿来与 1990 年代末的电信泡沫相比较。英伟达的 GPU 在 AI 数据中心占据主导地位，而自 2024 年以来的多篇报道称美国反垄断监管机构正在审视这种主导地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_build-out_financing">AI build-out financing - Wikipedia</a></li>
<li><a href="https://www.bloomberg.com/graphics/2026-ai-circular-deals/">AI Circular Deals: How Microsoft, OpenAI and Nvidia Keep ...</a></li>
<li><a href="https://www.nytimes.com/2024/08/06/technology/nvidia-antitrust-scrutiny.html">Nvidia Scrambles for a Response to Antitrust Scrutiny - The New...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论呈两极分化：一些评论者认为循环融资不过是正常的刺激需求手段，并无不妥；另一些人则主张英伟达主要是借此锁定供货，使谷歌、亚马逊和 AMD 拿不到芯片，并让新云继续使用英伟达芯片而非 TPU 或 Trainium。多位读者指出，租赁价格和云厂商的数据表明算力短缺确实存在；还有人贴出了前一天关于同一指控的大型重复讨论帖。

**标签**: `#Nvidia`, `#GPU pricing`, `#AI infrastructure`, `#antitrust`, `#circular financing`

---

<a id="item-4"></a>
## [PyPI 推出全新项目页面，突出安全与来源溯源信号](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 7.0/10

PyPI 已完成项目页面的重新设计并正式上线，新页面将安全与来源溯源（provenance）信息放在显眼位置：例如 datasette 这类项目的文件页会显示溯源证明，而 dlt 等未采用的项目则不会显示。该消息于 2026 年 11 月 6 日发布在 PyPI 官方博客上，意味着这些信号从隐藏在元数据中变成了默认浏览体验的一部分。 Python 开发者日常往往就是根据项目页面来挑选依赖，把溯源和安全信号放到最显眼的位置，等于给每个安装者提供了一个低成本的方式，去确认构件是在哪里、由谁构建的。这把供应链透明度从少数安全专家的实践推向了主流的打包体验，也会对维护者形成可见的压力，促使他们采用可信发布（Trusted Publishing）。 页面上展示的信号来自基于 OIDC 的可信发布与溯源证明，而不是对包是否恶意的判断，因此它有助于发现那些原本正常、但 PyPI 凭据被盗用的项目，却无法识别本身就是恶意的包。此外，可信发布目前仍不支持可复用的 GitHub Actions 工作流（warehouse 仓库 issue #11096），这限制了那些围绕可复用工作流组织 CI 的维护者采用该机制。

hackernews · rbanffy · 11月14日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50497892)

**背景**: PyPI 是 Python 默认的包索引，而“可信发布”是 PyPI 的术语，指利用 OpenID Connect（OIDC）在 GitHub Actions 等 CI 服务与 PyPI 之间交换短时效的身份令牌，从而不再需要长期有效的 API 令牌。溯源证明（provenance attestation）是一种机器可读的签名记录，用来描述构件的来源与构建过程；更广泛的 Sigstore 项目提供了无密钥签名模式——由 Fulcio 签发短时效证书并配合 Rekor 透明日志——使得这类记录无需管理长期密钥即可落地。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.pypi.org/trusted-publishers/">Publishing to PyPI with a Trusted Publisher</a></li>
<li><a href="https://www.sigstore.dev/">Sigstore</a></li>
<li><a href="https://safeguard.sh/resources/blog/what-is-software-provenance-explained">What Is Software Provenance ? Origin and Build History Explained</a></li>

</ul>
</details>

**社区讨论**: 评论者总体欢迎这种透明度提升，但也提出了不少异议：有人认为这套信任模型本质上是中心化的，依赖“大云厂商”并助长锁定效应；有人强调溯源只能发现原本正常的项目被劫持上传的情况，而无法识别恶意包；还有人希望无密钥的 Sigstore 式签名能更普及，并呼吁可信发布尽快支持可复用工作流。

**标签**: `#PyPI`, `#software supply chain security`, `#provenance`, `#Sigstore`, `#Python packaging`

---

<a id="item-5"></a>
## [Show HN：用约 200 行纯 JAX 代码复现 DeepSeek V3 架构](https://github.com/Vaibhaav-Tiwari/deepseek-v3-jax) ⭐️ 7.0/10

一位开发者发布了 GitHub 项目 deepseek-v3-jax，用约 200 行纯 JAX 代码从零复现了 DeepSeek V3 的模型架构，并以 Show HN 帖子的形式分享出来。该项目定位为极简、易读的参考实现，而非生产级推理框架。 DeepSeek V3 是一个拥有 6710 亿参数的混合专家（MoE）模型，官方实现代码体量庞大且复杂，而这个精简易读的版本降低了工程师理解现代大模型推理原理的门槛。Hacker News 的讨论还显示它不仅可读而且可用：有评论者通过 ROCm 在 AMD 显卡上成功端到端跑通，使其成为少见的非 CUDA 实验起点。 由于目标是教学用途，这约 200 行代码主要覆盖模型结构与前向传播逻辑，而非完整推理服务栈，因此在权重加载、KV 缓存管理和性能调优等方面会有简化。在硬件方面，用户反馈 AMD 显卡需要设置 HSA_OVERRIDE_GFX_VERSION=11.0.0 等环境变量，才能让 JAX 的 ROCm 插件识别消费级 GPU。

hackernews · VaibhaavTiwari · 11月14日 15:04 · [社区讨论](https://news.ycombinator.com/item?id=50497589)

**背景**: DeepSeek V3 是中国公司深度求索（DeepSeek）推出的开源大语言模型，采用总参数达 6710 亿的混合专家（MoE）架构，并结合多 token 预测等技术；每个 token 只激活其中一小部分专家，这是它能够被实际部署服务的关键。JAX 是谷歌推出的面向加速器的 Python 数值计算库，把自动微分与 XLA 编译器结合在一起。ROCm 则是 AMD 面向 GPU 加速计算的开源软件栈，相当于英伟达 CUDA 的对应物，在 ROCm 上运行 JAX 需要走专门的插件而非默认的 CUDA 路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/en/news/deepseek-v3/">Introducing DeepSeek-V3</a></li>
<li><a href="https://en.wikipedia.org/wiki/Google_JAX">Google JAX - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/ROCm">ROCm - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论氛围非常积极且偏重学习：评论者认为从第一性原理重建模型具有独特价值，并表示这个项目促使他们重新拾起 JAX，或打算自己动手复刻以便学习。一个实用的亮点来自某位用户，他一直在 Fedora 上折腾 ROCm 本地深度学习环境，表示这是首个能在其 RX 7600 XT 16GB 上端到端跑通的项目，但前提是设置好两个必需的环境变量。也有人询问：对于熟悉 Java/Python、但不了解推理内部机制的开发者来说，有没有好的学习路线图。

**标签**: `#JAX`, `#DeepSeek`, `#LLM inference`, `#Show HN`, `#ROCm`

---

<a id="item-6"></a>
## [Google Project Zero 将漏洞披露期限逐步缩短至 60 天乃至 30 天](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 7.0/10

Google 的 Project Zero 团队在博客中宣布，其披露政策即日起改为“Full 90”，即在通知厂商后 90 天公开漏洞；随后于 2027 年 2 月 2 日改为“Full 60”，最终于 2028 年 1 月 3 日改为“Full 30”。这取代了该团队长期执行的 90+30 期限，此前厂商实际上最多拥有约 120 天才会被公开披露。 Project Zero 设定的期限历来是整个行业协同漏洞披露事实上的节奏标尺，把窗口压缩到 30 天将迫使厂商和开源项目大幅加快补丁发布速度，否则未修复的漏洞就会被公开。这种压力对资源有限的维护者和发行版厂商冲击最大，因为他们往往单单测试和回溯移植补丁就需要数周时间。 关键的技术变化是取消了 Project Zero 于 2021 年增设的额外 30 天宽限期，因此披露时间现在严格按初次报告起的日历天数计算，而不再顺延到与计划的补丁发布日期对齐。错过期限的厂商将面临完整技术细节被公开而用户仍处于未修复状态，因为该团队给出的理由是：只有截止日期才能创造出单纯提交漏洞报告所不具备的紧迫感。

hackernews · hacb · 11月14日 11:13 · [社区讨论](https://news.ycombinator.com/item?id=50496051)

**背景**: Project Zero 是 Google 于 2014 年成立的安全研究团队，专门寻找零日漏洞——即攻击者可在补丁存在之前利用的缺陷——范围不仅限于 Google 自家产品，还包括被广泛使用的第三方软件。该团队在 2015 年推广了 90 天披露期限，用以推动厂商及时修复补丁，并在漏洞已被在野利用时保护用户。协同漏洞披露（CVD）则是更广泛的做法：先私下向厂商报告缺陷、商定修复时间表，随后公开细节，以便防御方和用户评估自身风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://projectzero.google/vulnerability-disclosure-policy.html">Vulnerability Disclosure Policy - Project Zero</a></li>
<li><a href="https://en.wikipedia.org/wiki/Project_Zero">Project Zero - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coordinated_vulnerability_disclosure">Coordinated vulnerability disclosure</a></li>

</ul>
</details>

**社区讨论**: 评论者对如此短的窗口是否现实持怀疑态度，有人指出考虑到发行版打补丁的周期之长，“Ubuntu 需要的时间会比这多得多”。也有人主张更快行动，认为有漏洞赏金收益的研究者没有理由拖延，立即公开才是唯一能迫使厂商修复漏洞的手段；还有一条讨论则跑偏到猜测 AI 厂商会借漏洞研究推动自家工具的采用。

**标签**: `#cybersecurity`, `#vulnerability disclosure`, `#Project Zero`, `#Google`, `#security policy`

---

<a id="item-7"></a>
## [CBC 调查后，LinkedIn 与 Monster 下架逾千条虚假招聘信息](https://www.cbc.ca/news/canada/linkedin-monster-take-down-over-1-000-fake-job-postings-after-cbc-investigation-9.7415379) ⭐️ 7.0/10

在 CBC（加拿大广播公司）展开调查之后，LinkedIn 与 Monster 两家招聘平台下架了超过 1000 条虚假招聘信息。此次大规模清理较为罕见地公开暴露了主流招聘网站处置虚假岗位的过程，而这些信息是由记者发现、而非平台自身检测系统识别的。 招聘诈骗是危害最大的网络欺诈形式之一，因为它瞄准的是处于经济压力下的求职者，并可能导致身份信息被盗或被卷入洗钱链条。上千条虚假岗位能在两家最大的招聘网站上存续、直到新闻机构介入才被清除，这让人质疑用户应对平台审核抱有多少信任，也让人担忧还有多少诈骗信息未被发现。 诈骗者正越来越多地借助 AI 工具批量生成看似可信的职位描述和公司主页，而最危险的虚假信息往往与真实岗位混杂在正规招聘平台上，若不仔细核查几乎难以分辨。常见的危险信号包括：该职位未出现在企业官网的招聘页面上、招聘方没有可验证的个人资料，以及在流程早期就索要敏感个人信息或银行资料。

hackernews · gnabgib · 11月14日 18:56 · [社区讨论](https://news.ycombinator.com/item?id=50499723)

**背景**: LinkedIn、Monster、Indeed 等招聘平台依靠自动化检测、人工审核以及用户举报相结合的方式来识别虚假招聘信息，这一领域通常被称为“信任与安全”（trust and safety）。虚假岗位的目的通常是收集个人信息、以押金或设备费名义骗取求职者钱财，或诱骗不知情者充当洗钱“钱骡”。美国联邦贸易委员会（FTC）引用的估算显示，美国每年因招聘诈骗造成的损失高达数亿美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.indeed.com/help/employers/articles/fraudulent-job-policy">Fraudulent Job Policy - Indeed</a></li>
<li><a href="https://www.totaldefense.com/security-blog/job-board-safety-guide-how-to-avoid-employment-scams-on-fake-recruiting-sites/">Job board safety guide: how to avoid employment scams on fake ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Trust_and_safety">Trust and safety - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论普遍持怀疑态度，认为诈骗在网络经济中所占比例远高于平台所承认的，有人引用路透社报道称 Meta 约 10%的收入来自推广诈骗和违禁产品的广告。多位用户分享了亲身经历：一人回忆当年按 Craigslist 上的招聘信息去面试，结果发现一群人被锁在门外排队等候；另一人则说自己接管了一个无人管理的日内交易 subreddit，清理掉广告和机器人后竟一条正常帖子都不剩。还有人感叹，如今找工作几乎被迫使用社交网络。

**标签**: `#trust-and-safety`, `#fraud`, `#platform-moderation`, `#job-listings`, `#online-scams`

---

<a id="item-8"></a>
## [EFF 指出：科技公司再次重新定义隐私，以将 AI 数据采集正常化](https://www.eff.org/deeplinks/2026/11/tech-companies-are-trying-shift-entire-concept-privacy-again) ⭐️ 7.0/10

电子前沿基金会（EFF）发表了一篇评论文章，认为科技公司正在再次试图改变“隐私”一词的含义，以便将无处不在的、由 AI 驱动的数据采集正常化。文章把这种重新定义与现实中的做法联系起来，例如始终在线的 AI 会议记录工具和转写功能；该文在 Hacker News 上引发了大规模讨论（471 分、175 条评论）。 “隐私”如何被定义，决定了哪些法律、产品默认设置和职场政策会被视为可接受；因此，把隐私从“对数据采集的限制”重新解释为“用户可控”，会在不知不觉中让持续录音变得正当。受影响最大的是那些无法选择不被录音的员工，以及依赖转写等辅助技术的残障人士。 这篇文章属于倡导性评论，而非技术披露，因此它提供的是一种对叙事框架的批判，而不是新的研究或产品细节。其核心论点是：把数据采集包装成用户“同意”的功能，会掩盖平台与被录音者之间的权力不对等。

hackernews · gslin · 11月14日 12:45 · [社区讨论](https://news.ycombinator.com/item?id=50496602)

**背景**: 电子前沿基金会（EFF）成立于 1990 年，是一家通过诉讼、政策分析和草根行动来捍卫数字世界公民自由的非营利组织，隐私是其核心议题之一。围绕隐私的争论往往取决于相互竞争的定义：一种把隐私理解为对“哪些数据可以被采集”的限制，另一种则把隐私理解为数据被采集后用户所拥有的控制权和同意权。辅助技术——即帮助残障人士完成日常任务的设备和软件，例如为聋人和听障用户提供的实时转写——正处于这一张力的中心，因为赋能无障碍访问的同一项能力，也可能被用于监控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eff.org/issues/privacy">Privacy | Electronic Frontier Foundation</a></li>
<li><a href="https://www.eff.org/about">About EFF | Electronic Frontier Foundation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Assistive_technology">Assistive technology - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为这一趋势令人担忧，但在应对方式上存在分歧：一个突出疑问是，员工能否在不冒失业风险的情况下，现实地要求同事在会议中关闭 AI 记录工具，因为“选择退出”似乎与“保住工作”无法兼得。有人援引《世界人权宣言》第十二条关于免受“任意干涉”隐私的保护，认为公司无权获取这类数据；但也有反向观点指出，禁售实时转写眼镜会伤害聋人和听障用户，而采用本地运行、不导出数据的模型则是一条折中路径。

**标签**: `#privacy`, `#surveillance`, `#AI`, `#policy`, `#EFF`

---

<a id="item-9"></a>
## [意大利因未经同意读取相册对 Meta 罚款 8.05 亿欧元](https://www.reddit.com/r/worldnews/comments/1xwc80v/italy_has_fined_social_media_giant_meta_805m_for/) ⭐️ 7.0/10

意大利数据保护局（Garante Privacy）对 Meta 开出 8.05 亿欧元罚单，认定 Facebook 安卓应用在未获得用户具体同意的情况下，读取了约 2000 万意大利用户的照片、视频及其元数据。监管机构要求 Meta 在 60 天内将该 2023 年上线的相册推荐功能改为默认关闭，并单独、明确地征得用户同意，否则不得对未有效授权的用户启用该功能。 这是欧盟数据保护监管机构迄今开出的最大罚单之一，表明各国监管机构愿意就后台数据采集的同意方式对大型平台处以天价罚款。这可能促使 Meta 及其他应用开发者在欧盟范围内，对设备本地媒体访问采用默认关闭、颗粒度更细的同意流程。 此案的核心在于安卓的媒体权限——它允许应用广泛读取设备照片库；意大利监管机构既反对该功能默认开启，也认为向用户展示的授权提示过于笼统。Meta 有 60 天时间调整配置，同时仍可对该决定提出上诉，这笔罚款属于国家层面的裁决，其最终金额与执行仍可能面临争议。

reddit · r/worldnews · /u/Raj_Valiant3011 · 11月14日 20:18

**背景**: 意大利个人数据保护局（GPDP，通称 Garante Privacy）是意大利的独立数据保护机构，成立于 1996 年，负责执行隐私法律，包括欧盟《通用数据保护条例》（GDPR）。GDPR 要求处理个人数据必须具备合法依据，且同意必须自由给出、具体、知情且明确，因此笼统打包的授权弹窗可能被判定为不合格。在技术层面，安卓一直在收紧媒体访问权限：Android 13（API 33）引入了细分的 READ_MEDIA_IMAGES 和 READ_MEDIA_VIDEO 权限以替代宽泛的存储访问权限，Android 14 又增加了“部分照片访问”选项，允许用户只向应用开放特定图片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cwn83gxemk35o">Italy fines Meta €805m over accessing users' photos</a></li>
<li><a href="https://www.garanteprivacy.it/web/garante-privacy-en">Home - Garante privacy en</a></li>
<li><a href="https://developer.android.com/about/versions/14/changes/partial-photo-video-access">Grant partial access to photos and videos | Android Developers</a></li>

</ul>
</details>

**标签**: `#privacy`, `#GDPR`, `#Meta`, `#data-protection`, `#regulation`

---

<a id="item-10"></a>
## [SpaceX 下月将首次尝试同时回收星舰飞船与超级重型助推器](https://t.me/zaihuapd/45117) ⭐️ 7.0/10

马斯克在财报电话会上宣布，SpaceX 将于下月首次尝试在同一飞行任务中同时回收星舰飞船与超级重型助推器。他表示，若成功，这将是人类首次完整回收轨道运载工具。 若成功，星舰将成为人类首个完全可复用的轨道发射系统，有望大幅降低每公斤入轨成本并提高发射频次，对星链卫星部署和 NASA 阿尔忒弥斯登月着陆器等任务影响重大。这次尝试也检验了 SpaceX 快速迭代试飞的策略能否在现实时间表内实现完全复用。 马斯克坦言首次尝试并不保证成功，但称下一次飞行的成功概率会更高。这一宣布紧随上个月的发射：当时一台发动机提前关机，任务被缩短至约三小时，助推器与飞船均未能回收。

telegram · zaihuapd · 11月14日 03:03

**背景**: 星舰是两级完全可复用的发射系统：超级重型助推器作为一级，设计为返回后被发射塔的机械臂（常被称为“筷子”）在空中夹住；星舰飞船作为二级，则依靠隔热瓦保护再入大气层并完成动力着陆。历史上从未有轨道火箭实现完全复用——航天飞机只是部分复用，且每次飞行后都需要大量翻修。因此，在一次飞行中同时回收两级，是迈向像飞机一样日常化复用的关键一步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Super_Heavy">SpaceX Super Heavy - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reusable_launch_vehicle">Reusable launch vehicle - Wikipedia</a></li>
<li><a href="https://interestingengineering.com/space/spacex-starship-15th-flight-booster-catch-skipped">SpaceX Starship 15’s Super Heavy booster skips tower catch ...</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#reusable rockets`, `#spaceflight`, `#Elon Musk`

---

<a id="item-11"></a>
## [Cloudflare 开源 Kitesurf：为 AI 代理打造的无状态浏览器](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 7.0/10

Cloudflare 以 Apache 2.0 协议开源了 Kitesurf，将其定位为专为 AI 代理设计的实验性无状态浏览器引擎。Kitesurf 不需要启动 Chromium 容器，而是完全运行在 Cloudflare Workers 之上，能够解析 HTML、应用 CSS 并执行 JavaScript，代码已发布在 GitHub 上，可供本地运行或自行部署实例。 让 AI 代理浏览网页通常要依赖无头 Chromium，而它 CPU 和内存开销大，面对突发、并行的负载很难弹性扩展。Cloudflare 通过在自身全球网络上提供可按需扩展的轻量浏览器运行时，把自己定位为新兴“代理化网络”的基础设施，并给代理开发者提供了容器化浏览器集群之外的另一种选择。 Kitesurf 是无状态、临时的，每个会话完全隔离且不保留持久化的浏览器状态，适合大批量的抓取与自动化任务。Cloudflare 还说明它可以与 Browser Run 配合完成截图与自动化，并支持通过 CDP 在 Chrome DevTools 中检查页面；不过它仍被标记为实验性项目，目前也没有公开的第三方基准数据来验证其 CPU 与内存占用的说法。

telegram · zaihuapd · 11月14日 09:33

**背景**: Chromium 等无头浏览器为自动化工具和 AI 代理提供了完整的渲染引擎，但每个实例都背负着整个浏览器进程的开销，大规模部署时成本高、启动也慢。Cloudflare Workers 是一个无服务器平台，在数百个城市以轻量级 V8 isolate 运行代码，启动速度远快于容器或虚拟机上的 Node 进程，内存占用也小得多。Kitesurf 实际上是把浏览器重新构想为运行在 isolate 中的引擎，用更小的资源占用取代完整的 Chromium 功能集，以适配代理真正需要的网页提取与交互任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf-open-source">Kitesurf is now open source | Cloudflare Blog</a></li>
<li><a href="https://developers.cloudflare.com/browser-run/kitesurf/">Kitesurf · Cloudflare Browser Run docs</a></li>
<li><a href="https://kitesurf.dev/">Kitesurf - stateless browser running entirely on Workers</a></li>

</ul>
</details>

**标签**: `#ai-agents`, `#cloudflare-workers`, `#open-source`, `#serverless`, `#web-scraping`

---

<a id="item-12"></a>
## [星舰入轨但助推器爆炸，双塔捕回收落空](https://t.me/zaihuapd/45129) ⭐️ 7.0/10

SpaceX 于当地时间 11 月 13 日从得州发射星舰第 15 次试飞，飞船成功入轨并部署全部 26 颗 Starlink V3 卫星；但超重型助推器返场中止，在墨西哥湾受控溅落后爆炸，原定的双塔捕回收未能实现。 如果飞船在次日成功被发射塔机械臂捕获，将成为人类首次回收轨道级飞船上面级，是迈向快速完全复用和降低单位载荷成本的关键一步；而助推器回收失败也说明超重型助推器的复用仍是高难度工程问题。 助推器中止返场的原因尚未公布；飞船预计在轨约 22 小时、绕地球约 14 圈，随后返回 Starbase 尝试塔捕。26 颗 Starlink V3 卫星中有 3 颗携带摄像头，用于检查飞船隔热瓦。

telegram · zaihuapd · 11月14日 23:49

**背景**: 星舰是 SpaceX 的两级完全可复用发射系统：超重型助推器负责把星舰上面级送入高空，两级都设计为由发射塔机械臂捕获，而不是依靠着陆腿或海上溅落。Starlink V3 是 SpaceX 的新一代宽带卫星，体积和容量均大于早期版本，需要由星舰发射部署。星舰腹部覆盖数千块陶瓷隔热瓦，用于在再入大气层时抵御气动加热。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithome.com/1/026/467.htm">有望改写人类火箭复用史：SpaceX 星 舰 明日第 15...</a></li>
<li><a href="https://starlink.com/updates/starlink-version-3-satellites">Starlink Version 3 Satellites</a></li>
<li><a href="https://c.m.163.com/news/a/L31VOQN30511ABC3.html">星 舰 隔 热 瓦 又‘烧出条纹’，专家：这条技术路线走不通</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#航天工程`, `#火箭回收`, `#Starlink`

---