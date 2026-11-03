---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 107 条内容中筛选出 21 条重要资讯。

---

1. [vLLM v0.33.0rc3 发布：升级 PyTorch 2.14、仅提供 CUDA 13.0 构建，并新增大量模型支持](#item-1) ⭐️ 8.0/10
2. [Subvocal：射频智能眼镜将无声口型解码为文字](#item-2) ⭐️ 8.0/10
3. [陶哲轩探讨 AI 时代的“无我数学”](#item-3) ⭐️ 8.0/10
4. [Ubuntu LTS 内核近三周仍未修复严重 0day 远程代码执行漏洞](#item-4) ⭐️ 8.0/10
5. [施奈尔：AI 一个月发现全部历史 3%的关键软件漏洞](#item-5) ⭐️ 8.0/10
6. [ChatGPT 分享链接漏洞：一次点击即可接管账号](#item-6) ⭐️ 8.0/10
7. [树莓派 5 正式发布：4GB 版 60 美元、8GB 版 80 美元，搭载 2.4GHz Cortex-A76](#item-7) ⭐️ 8.0/10
8. [Linux 内核 IPv4 TCP 高危释放后使用漏洞（CVE-2026-98432），务必尽快更新内核](#item-8) ⭐️ 8.0/10
9. [SGLang v0.5.23 发布：扩展模型支持并显著加速 MoE 解码](#item-9) ⭐️ 7.0/10
10. [博客宣称 Astra 可读写 Qwen 权重以提升数学能力](#item-10) ⭐️ 7.0/10
11. [随笔呼吁读者为自己珍爱的网站做备份](#item-11) ⭐️ 7.0/10
12. [Cloudflare 将 DNS 区域构建延迟减半，内存占用降低 85%](#item-12) ⭐️ 7.0/10
13. [Legora 首席技术官谈如何打造“看不见”的法律 AI](#item-13) ⭐️ 7.0/10
14. [谷歌联合业界捣毁 130 万台 Android 电视盒代理僵尸网络](#item-14) ⭐️ 7.0/10
15. [OpenAI 推出 LifeVal 基准，评估 AI 日常任务能力](#item-15) ⭐️ 7.0/10
16. [朝鲜相关创纪录黑客事件后，币安净流出达 47 亿美元](#item-16) ⭐️ 7.0/10
17. [百度网盘摇一摇广告改用磁力计判方向，绕过运动权限限制](#item-17) ⭐️ 7.0/10
18. [WIRED 调查发现 400 多个 AI 应用暗藏色情深伪功能](#item-18) ⭐️ 7.0/10
19. [瑞典 ICA 门店遭网络攻击，冷柜被远程调至 50°C](#item-19) ⭐️ 7.0/10
20. [Anthropic 据报公开提交纳斯达克 IPO 申请，股票代码 ANT](#item-20) ⭐️ 7.0/10
21. [阿布扎比与 OpenAI 签署四项协议，启动「机器可读政府」试点](#item-21) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.33.0rc3 发布：升级 PyTorch 2.14、仅提供 CUDA 13.0 构建，并新增大量模型支持](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 8.0/10

vLLM 发布候选版本 v0.33.0rc3，包含来自 389 位贡献者的 927 个提交，将引擎升级至 PyTorch 2.14.0（配套 torchvision 0.29.0 与 Triton 3.8.0），不再发布 CUDA 12.9 构建而只提供 CUDA 13.0 的 wheel 与镜像，并使 CUDA wheel 与 libtorch 实现 ABI 稳定。该版本还新增大量模型支持，包括 Reflection Beam-1.0（501B MoE、23B 激活参数）及其 DFlash2 草稿模型、Yandex AliceAI-Foundation-80B-A3B、Recursive Flint、Step-5 Preview、Nemotron Parse 3.5 和 MiniCPM-OCR 1.0，并带来投机解码、ROCm 与服务 API 的多项改进。 vLLM 是部署最广泛的开源大模型推理与服务引擎之一，因此一次改变 CUDA 基线版本与 PyTorch 版本的发布，会直接影响所有大规模自建推理服务的团队，尤其是那些在部署流水线中锁定 CUDA 12.9 或特定 PyTorch 构建的用户。ABI 稳定的 libtorch wheel 以及新增的 AWS EFA 镜像，也降低了 vLLM 在不同 Python 与硬件环境下分发的门槛。 这是一个候选发布版本，并包含破坏性变更：Medusa 与 MLP speculator 被移除，旧的 Ray compiled-graph 执行器被删除，`--mamba-cache-mode` 被弃用，生成暂停期间收到的请求现在返回 HTTP 503，且 NIXL 连接器要求 NIXL 1.5 或更新版本。性能优化高度依赖具体硬件，例如 GB300 上针对 Kimi-K3 的可选低延迟解码（TP8/TP16 下 1.5–2 倍）、MI300X/MI325X 上的 MonoKernel 解码、ROCm 10.0 成为默认版本而 7.2 仍以 `-rocm72` 发布，以及在原有 `vllm/vllm-openai` 之外新增 `vllm/vllm` 镜像别名。

github · khluu · 11月2日 10:10

**背景**: vLLM 是一个面向大语言模型的高吞吐、显存高效的推理与服务引擎，最初由加州大学伯克利分校 Sky Computing Lab 开发，如今由来自学术界和产业界数千名贡献者共同维护。它常被用于在兼容 OpenAI 的 HTTP API 之后提供模型服务，因此每次发布都会同时包含新模型架构支持、内核级性能优化与 API 层面的变化。PyTorch（其 C++ 运行时库称为 libtorch）是 vLLM 所依赖的深度学习框架，而 CUDA 是英伟达的 GPU 计算平台，因此升级 PyTorch 与 CUDA 版本会改变用户所需的 GPU 驱动、Python 版本与预编译二进制。所谓 ABI 稳定的 libtorch wheel，意味着 vLLM 可以基于 libtorch 的稳定二进制接口只构建一次，而不必为每种 PyTorch 或 Python 组合重新编译。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/">vLLM</a></li>
<li><a href="https://github.com/vllm-project/vllm">GitHub - vllm -project/ vllm : A high-throughput and...</a></li>
<li><a href="https://en.wikipedia.org/wiki/VLLM">Transformer (deep learning) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#PyTorch`, `#CUDA`, `#release`

---

<a id="item-2"></a>
## [Subvocal：射频智能眼镜将无声口型解码为文字](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

The Subvocal Company（YC F26）的 Aarush 和 Arnav 发布了一款智能眼镜：眼镜向佩戴者面部发射低功率无线电波，并用基于这些信号扰动训练的基础模型，把无声口型实时解码为文字，速度接近正常说话。他们表示系统还可以针对"内部言语"调优——闭着嘴默念、嘴唇完全不动；此前在斯坦福 TreeHacks 黑客松上用 EMG 电极做的原型已被放弃。 如果这一演示在受控环境之外依然成立，无声语音输入就能让听写功能真正用于图书馆、开放办公室和公共场所——这些场合大声说话既不合适也不可能；同时对有言语或运动障碍的人群，它提供了一种免手动的文字输入方式。这也意味着在构建实用无声语音接口的竞争中，射频感知成为 EMG、耳机声学与深度相机方案之外的有力竞争者。 团队在黑客松原型之后放弃了 EMG，原因是出汗导致信号漂移、电气干扰、电极位置难以复现，以及最根本的一点——没人愿意把电极贴在脸上；改用射频是因为无线电波能穿过面部，并被舌头、嘴唇和软腭的动作调制。他们提到剩下的两个最大难题是跨用户泛化（每个人的面部解剖结构对射频场的扰动各不相同）以及传感链路本身，需要极低噪声的前端，并让天线场与发音器官最大限度重叠。目前尚未公布独立的准确率基准或延迟数据，推理究竟在眼镜端运行还是依赖配对的手机/应用也仍不明确。

hackernews · aarushyadav · 11月2日 17:16

**背景**: 无声语音识别（SSR）的目标是在不产生可听声音的前提下解码语音，通常通过读取肌肉电活动（EMG）、口型几何（深度相机）或射频反射来实现，从而绕开普通自动语音识别在环境噪声、隐私和可及性上的局限。MIT 媒体实验室的 AlterEgo 让"EMG 头戴设备"这一路线广为人知，也正是 Subvocal 两位创始人最初想复现的项目。"默读/无声言语"（subvocalization）指不发声地在心里把词说出来；公司强调其系统读取的是有意识的闭口发音动作，而不是默读时无意识的舌头微动。这里的射频感知使用类似蓝牙的低功率无线电波，其场分布会被口腔内的发音器官扰动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/29855428/">Development of sEMG sensors and algorithms for silent speech ...</a></li>
<li><a href="https://chaof94.github.io/Papers/EarSSR.pdf">EarSSR: Silent Speech Recognition via Earphones</a></li>
<li><a href="https://www.youtube.com/watch?v=JvD0TcBd4Hc">Watch Your Mouth: Silent Speech Recognition with Depth Sensing</a></li>

</ul>
</details>

**社区讨论**: HN 讨论整体非常热情，至少有一位评论者当场预订，同时提出了具体诉求：保留可调节的金属鼻托、提供适合非标准头型的大尺寸镜框，以及做一个可以夹在现有近视眼镜上的模块，而不是必须换整副眼镜。另一些人追问工程与隐私问题：繁重的信号处理是在眼镜端完成还是通过应用完成、能否离线工作，以及射频数据是否可能被用来推断性唤起之类的内在状态——这与早年反对把此类传感装进手机的隐私担忧一脉相承。也有评论者指出一个明显优势：无声输入在庭院劳作、操作机械等嘈杂环境中应当照样可用，而这正是麦克风失灵的场景。

**标签**: `#HCI`, `#smart glasses`, `#silent speech recognition`, `#accessibility`, `#privacy`, `#RF sensing`, `#wearable computing`

---

<a id="item-3"></a>
## [陶哲轩探讨 AI 时代的“无我数学”](https://terrytao.wordpress.com/2026/11/02/egoless-mathematics-in-the-ai-era/) ⭐️ 8.0/10

陶哲轩（Terry Tao）在其博客发表题为《AI 时代的无我数学》的文章，探讨随着 AI 系统在数学发现中承担更大角色，数学研究文化可能如何变化。文章引发了关于数学家是否应把个人身份与荣誉同工作分离的广泛讨论。 作为全球最知名的数学家之一，陶哲轩的论述可能影响数学界如何讨论 AI 对荣誉归属、研究动机和职业道路的冲击。这场讨论对数学家、AI 研究者、期刊编辑和资助机构都具有意义，因为他们正面对越来越多机器辅助发现的转变。 这篇文章是哲学与文化层面的随笔，而非技术成果，并在 Hacker News 上引发了约 89 条评论。评论者聚焦于自我作为雄心驱动与“无我”投入解题之间的张力，也谈到研究职业的经济压力。

hackernews · smilelamp · 11月2日 18:54 · [社区讨论](https://news.ycombinator.com/item?id=50341736)

**背景**: 陶哲轩是菲尔兹奖得主、高产研究者和长期博客作者，其科普与解释性文章在数学界广受阅读。“无我数学”一词呼应了更早的“无我编程”理念，即程序员把自我价值与代码分开，以便接受批评并共同改进。在 AI 时代，大语言模型等工具越来越多地用于提出猜想、辅助证明和形式化数学，这也带来了作者身份、荣誉归属以及人类数学家应重视什么等问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.flyingcoloursmaths.co.uk/the-egoless-mathematician/">The Egoless Mathematician | Flying Colours Maths</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧：一些人认为自我与人类动机和经济现实不可分割，另一些人则欢迎陶哲轩的重新框定，认为这是适应 AI 的健康方式。还有几个人担心“无我”或只重真理的框架会贬低数学家的职业与人性，其中一人称这种隐含的“人不重要”观点令人警惕。

**标签**: `#mathematics`, `#AI`, `#research culture`, `#philosophy`, `#Terry Tao`

---

<a id="item-4"></a>
## [Ubuntu LTS 内核近三周仍未修复严重 0day 远程代码执行漏洞](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

Ubuntu LTS 内核至今仍受一个严重 Linux 内核 0day 远程代码执行漏洞影响，该漏洞编号为 CVE-2026-98432，自披露以来已接近三周，Ubuntu 既未发布已修复的内核软件包，也未给出官方缓解指引。这一空窗期迫使用户自行寻找临时规避方案，也引发了外界对 Ubuntu 保持沉默的批评——相比之下 RHEL 等发行版已经发布了安全公告说明。 一个可远程利用的内核漏洞在数周内得不到修补，意味着所有未采取缓解措施的 Ubuntu LTS 服务器、云实例和桌面系统都处于暴露状态，而 LTS 版本恰恰是企业在生产环境中长期运行的版本。此事还引发了对 Ubuntu 安全响应透明度的质疑，因为用户无法判断修复是即将到来还是已经停滞。 社区成员指出，可以在数据包进入内核处理之前，用 raw 表的 PREROUTING 链配合 u32 匹配规则丢弃漏洞利用所依赖的流量，例如 `sudo iptables -t raw -I PREROUTING -p tcp -m u32 ! --u32 "0>>24&0x0F=5" -j DROP`。RHEL 已针对该问题发布缓解公告，但自己也声明该规避方法只能降低暴露面、无法完全阻止漏洞被利用，且未解释具体原因。

hackernews · majorchord · 11月2日 18:39 · [社区讨论](https://news.ycombinator.com/item?id=50341462)

**背景**: 0day 指在公开时厂商尚无修复方案的漏洞；远程代码执行（RCE）则意味着攻击者无需本地权限，就能通过网络在目标机器上运行自己的代码，属于危害最严重的一类缺陷。CVE-2026-98432 是分配给该漏洞的通用漏洞披露编号，即让厂商、扫描器和安全公告能够指向同一问题的标准公共标识。由于漏洞位于 Linux 内核本身，所有基于该内核的发行版（包括 Ubuntu 的长期支持版本）都必须各自发布打好补丁的内核构建；在此之前，管理员只能依靠 iptables 或 nftables 等包过滤工具在防火墙层拦截相关流量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Iptables">iptables - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/linux-unix/iptables-command-in-linux-with-examples/">iptables command in Linux - GeeksforGeeks</a></li>
<li><a href="https://linux.die.net/man/8/iptables">iptables (8) - Linux man page</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Ubuntu 既未发布补丁、也未提供缓解说明感到不满，多人公开质疑：一个看起来并不复杂的内核修复为何拖了近三周，并指出 RHEL 至少发布了安全公告。有评论者提出用 raw 表 u32 的 PREROUTING 丢弃规则作为实用应急方案；另一位把担忧扩大到运行 Linux 内核却从不推送安全更新的消费级路由器；还有人认为大模型正在把国家级水平的漏洞利用工具交到脚本小子手中，因此已知漏洞远不如接下来那二十个未知漏洞值得关注。

**标签**: `#security`, `#linux`, `#ubuntu`, `#kernel-vulnerability`, `#cve`

---

<a id="item-5"></a>
## [施奈尔：AI 一个月发现全部历史 3%的关键软件漏洞](https://www.schneier.com/blog/archives/2026/11/ai-vulnerability-finding-2.html) ⭐️ 8.0/10

Bruce Schneier 在博客中重点引用了 Nick Dobos 在 X 上的一项说法：AI 漏洞发现工具在仅仅一个月内就找出了有记录以来全部关键软件安全漏洞的 3%。该说法预测今年还可能再发现约 10 万个漏洞，使历史漏洞总数增加约 26%，Schneier 对此回应称：“是的，这是一个新世界。” 如果这一说法成立，它将意味着网络安全经济学发生重大转变：AI 发现软件缺陷的速度可能远远超过厂商和维护者进行分类、修补和披露的速度。这将对漏洞数据库、披露流程以及专有和开源生态中的软件供应链安全带来新的压力。 3% 这一数字是未经独立验证的社交媒体说法，没有说明方法、数据集或“关键”漏洞的定义，因此可能包含重复项、误报或 AI 辅助报告，而非完全自主发现。实际应用已经可见：Google 表示在 Chrome 的漏洞管理流程中使用了大型语言模型，并称 AI 帮助其在两个版本中修复了 1,072 个安全漏洞。

rss · Schneier on Security · 11月2日 12:02

**背景**: 大型语言模型可以分析源代码、补丁和漏洞报告，识别与安全缺陷相关的模式，补充已经使用数十年的静态应用安全测试（SAST）工具。漏洞数量通常指国家漏洞数据库（NVD）和 CVE 系统等数据库中记录的条目，因此关于“全部已记录”漏洞占比的说法很大程度上取决于记录范围和重复项处理方式。这条新闻反映出人们越来越关注利用 AI 不仅发现漏洞，还用于复现报告、评定严重程度和生成候选补丁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/google/google-says-ai-helped-chrome-fix-1-072-security-bugs-in-two-releases/">Google says AI helped Chrome fix 1,072 security bugs in two releases</a></li>
<li><a href="https://kb.cert.org/">CERT Vulnerability Notes Database</a></li>

</ul>
</details>

**标签**: `#AI security`, `#vulnerability discovery`, `#software security`, `#cybersecurity`, `#LLMs`

---

<a id="item-6"></a>
## [ChatGPT 分享链接漏洞：一次点击即可接管账号](https://www.parameter.ai/labs/we-found-a-gap-at-openai) ⭐️ 8.0/10

Parameter 研究团队发现 ChatGPT 分享链接功能存在漏洞，攻击者可在已登录用户的会话中执行代码，读取私密对话并将其外传至外部服务器。OpenAI 已于 10 月 26 日修复该问题，将其定级为 P1（最高严重级别），并向该团队支付了 5000 美元赏金。 该漏洞只要求受害者打开一条恶意分享链接，无需安装应用、无需提供凭证、也没有钓鱼表单，从而把针对全球使用最广泛的 AI 产品之一的账号接管门槛降低到一次点击。它也说明，旨在让 ChatGPT 内容公开传播的“分享对话”功能，正在围绕私密聊天数据扩大攻击面。 该漏洞串联了分享链接预览功能与图表组件之间的消息处理缺陷，因此仅渲染一个精心构造的共享对话，就足以在受害者的会话上下文中执行攻击者代码。OpenAI 将其定级为 P1 并奖励 5000 美元；修复后，此前构造的分享链接应不再能执行代码，但用户仍应把来源不明的分享链接视为不可信输入。

telegram · zaihuapd · 11月2日 10:24

**背景**: ChatGPT 允许用户把一段对话发布为公开的分享链接，其他人无需登录或安装任何东西即可在浏览器中打开；渲染这类页面会涉及预览生成以及图表等富组件。当这些组件之间传递消息的方式存在缺陷时，被注入的内容就可能突破共享页面的沙箱，触达浏览者的已登录会话。在典型的漏洞披露或漏洞赏金体系中，“P1”是最高严重级别，用于影响极其严重的问题；OpenAI 通过 Bugcrowd 运营其赏金计划，奖金从数百美元到数万美元不等。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/chatgpt/">Introducing ChatGPT - OpenAI</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#security vulnerability`, `#account takeover`, `#OpenAI`, `#data exfiltration`

---

<a id="item-7"></a>
## [树莓派 5 正式发布：4GB 版 60 美元、8GB 版 80 美元，搭载 2.4GHz Cortex-A76](https://t.me/zaihuapd/44854) ⭐️ 8.0/10

树莓派 5 正式发布，4GB 型号售价 60 美元、8GB 型号售价 80 美元（均不含当地税费），相比上一代 35 至 75 美元的价格区间有所上移。新板搭载 2.4GHz 四核 64 位 Arm Cortex-A76 CPU、支持 OpenGL ES 3.1 与 Vulkan 1.2 的全新 VideoCore VII GPU、双路 4K60p HDMI 输出、4K60p HEVC 解码器、双频 802.11ac Wi-Fi、蓝牙 5.0/低功耗蓝牙，以及两个可同时以 5Gbps 运行的 USB 3.0 接口和运行在 SDR104 模式下的高速 microSD 卡接口。 树莓派是业余爱好者、教育市场、工业控制器与边缘计算部署中事实上的标准单板计算机，其 CPU 与 I/O 的世代级升级会影响到规模极其庞大的用户群与产品线。从 Cortex-A72 升级到 Cortex-A76，再加上重新设计的 I/O 子系统，带来约 2 至 3 倍的 CPU 性能提升，使树莓派 5 能够胜任过去需要迷你主机或 x86 板卡才能完成的本地推理、媒体转码、多路摄像头采集等负载。 除标题规格外，新板还通过 FPC 排线引出单通道 PCIe 2.0 接口（可连接 NVMe 固态硬盘），采用全新的 RP1 南桥芯片负责 USB 与以太网，并首次加入板载实时时钟与独立电源按键；此外需要 5V/5A（27W）的 USB-C 电源才能发挥全部性能。60 美元与 80 美元的报价不含当地税费与运费，而高速 microSD 支持也取决于所用 UHS-I 存储卡能否真正协商到 SDR104 模式。

telegram · zaihuapd · 11月2日 12:00

**背景**: 树莓派是一块信用卡大小、价格低廉、运行 Linux 的单板计算机，广泛应用于教育、原型开发与嵌入式产品中，历代产品通常保持相同的基本板型而升级 SoC。Cortex-A76 是 Arm 在 2018 年推出的全新微架构，面向 7nm 级工艺设计，每时钟性能较树莓派 4 所用的 Cortex-A72 有大幅提升，因此树莓派 5 的 CPU 升级被视为该平台历史上最大的一次跨越。VideoCore VII 是对应的新一代博通图形核心，而 SDR104 则是 SD 卡 UHS-I 标准中速度最快的模式，可把 microSD 吞吐量提升到约 100MB/s，接近此前水平的两倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidauthority.com/cortex-a76-deep-dive-870896/">Arm Cortex - A 76 CPU microarchitecture deep dive</a></li>
<li><a href="https://web.archive.org/web/20180601043138/https://www.anandtech.com/show/12785/arm-cortex-a76-cpu-unveiled-7nm-powerhouse">Arm 's Cortex - A 76 CPU Unveiled: Taking Aim at the Top for 7nm</a></li>

</ul>
</details>

**标签**: `#Raspberry Pi`, `#single-board computers`, `#hardware release`, `#embedded systems`, `#Arm Cortex-A76`

---

<a id="item-8"></a>
## [Linux 内核 IPv4 TCP 高危释放后使用漏洞（CVE-2026-98432），务必尽快更新内核](https://t.me/zaihuapd/44866) ⭐️ 8.0/10

近期流传的安全提醒指出，Linux 内核在建立 IPv4 TCP 连接的代码路径中存在释放后使用（use-after-free）漏洞，编号为 CVE-2026-98432，攻击者可完全从网络侧触发，既不需要认证也不需要用户交互。该提醒还提到，针对 MPTCP 监听端口的远程代码执行（RCE）利用示例已被公开，目前上游内核已修复，Red Hat 等发行版也已发布修补后的内核。 该漏洞 CVSS 评分高达 9.8，且可经网络远程、无需认证触发，这意味着几乎所有未修补、暴露在公网的 Linux 服务器都处于风险之中，无论是云主机还是本地设备。影响面被进一步放大的原因是：自 Go 1.24 起，Linux 上的监听套接字默认启用 MPTCP，因此大量用 Go 编写的服务在运维人员毫无感知的情况下就默认处于暴露状态。 该缺陷位于处理入站 IPv4 TCP 连接建立时请求套接字选项（inet_opt/ireq_opt）的代码中，表现为释放后使用，可导致远程拒绝服务，在存在 MPTCP 监听的情况下甚至有报告称可实现远程 root。需要特别注意的是，单纯关闭多路径 TCP 并不能修复该漏洞，而且各发行版的补丁进度并不一致——Red Hat 已于 11 月 1 日为 RHEL 8、9、10 发布修复内核，而部分发行版在报道时仍无补丁或仅有测试版本。

telegram · zaihuapd · 11月3日 02:37

**背景**: 释放后使用（use-after-free）是一种内存安全缺陷：程序在释放某块内存后仍继续使用它，如果攻击者能够控制这块被释放的内存被重新分配给什么内容，往往就能劫持程序执行流。本次漏洞位于 Linux 内核的 TCP 协议栈中，而这段代码要处理每一个入站的 TCP 连接，因此任何能发送网络数据包的人都能触达它。MPTCP（多路径 TCP）是 TCP 的扩展，允许一条 TCP 连接同时使用多条网络路径，以提升冗余性与带宽聚合能力；它自 Linux 5.6 起进入内核主线，而 Go 运行时从 1.24 版本开始在 Linux 上默认为监听套接字启用该特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://atlasum.net/blog/cve-2026-98432-linux-ipv4-tcp-uaf">Linux 's October 2026 TCP Use-After-Free: CVE - 2026 - 98432 — Atlas</a></li>
<li><a href="https://almalinux.org/blog/2026-10-30-cve-2026-98432/">CVE - 2026 - 98432 : Patched kernels available in testing | AlmaLinux OS</a></li>
<li><a href="https://www.mptcp.dev/">MPTCP | Multipath TCP for Linux</a></li>

</ul>
</details>

**标签**: `#security`, `#linux-kernel`, `#vulnerability`, `#cve`, `#networking`

---

<a id="item-9"></a>
## [SGLang v0.5.23 发布：扩展模型支持并显著加速 MoE 解码](https://github.com/sgl-project/sglang/releases/tag/v0.5.23) ⭐️ 7.0/10

SGLang 发布 v0.5.23，这是一个由 257 位贡献者提交的 1007 个 PR 构成的大型版本更新，新增对 Muse Spark Open、Beam-1.0、MiniMax-M3.1-Flash、MiniCPM-V 4.7、FLUX.3 Image Klein、MOSS-Image 等多款 LLM、VLM 与扩散模型的推理支持。该版本还引入了面向 NVIDIA 与 AMD GPU 的可选低延迟 megakernel/monokernel 插件、可在单张消费级显卡上运行超出显存 MoE 模型的 Paged Experts、面向量化 MoE 模型的 LoRA 引擎，以及名为 SGLang-TorchTPU 的 PyTorch 原生 TPU7x 后端。 SGLang 是广泛使用的高吞吐推理服务框架，因此这些改动直接影响生产环境中的模型部署：该版本称 DeepSeek-V4.1 在 GB300 上预填充吞吐提升最高 1.5 倍、32K 至 64K 长提示词下首 token 延迟降低约 28%，MoE 模型在 H200 上首个 token 生成速度提升 30% 至 58%。新增扩散模型支持与 TPU 后端，说明该框架正从以 NVIDIA 为中心的自回归 LLM 服务，扩展到多模态与多硬件平台部署。 这些亮点性能特性大多是可选开启而非默认启用，包括 NVIDIA megakernel 与 AMD monokernel 插件（据称在 GB300 上单用户解码最高提速 44%，在 MI350X 上针对 DeepSeek-V4.1-Flash 提速 75%）以及 Paged Experts（宣称比 CPU offload 快最多 30 倍）。安装时需通过 `uv pip install --prerelease=allow sglang==0.5.23` 允许预发布版本，官方还提供了面向 CUDA 13、AMD MI35x/MI30x、Intel GPU、Intel CPU 和 Google TPU7x 的预构建 Docker 镜像。

github · Fridge003 · 11月2日 22:14

**背景**: SGLang 是一个面向大模型高吞吐服务的开源框架，作为非营利开源项目托管，已被用于大规模生产部署，每天在超过 40 万块 GPU 上生成数万亿 token。它主要支持 Hugging Face 格式（safetensors、FP16/BF16）的模型，并提供前缀缓存、投机解码和分页注意力等优化。VLM 是能够同时理解文本与图像的多模态模型，而扩散模型以并行方式而非逐 token 方式生成图像等输出，因此在面向 LLM 的框架中原生支持扩散模型是一次值得关注的扩展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.sglang.io/">Welcome to SGLang - SGLang Documentation</a></li>
<li><a href="https://grokipedia.com/page/SGLang">SGLang</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model_(VLM)">Vision-language model (VLM)</a></li>

</ul>
</details>

**标签**: `#SGLang`, `#LLM inference`, `#model serving`, `#release`, `#diffusion models`

---

<a id="item-10"></a>
## [博客宣称 Astra 可读写 Qwen 权重以提升数学能力](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 7.0/10

一篇题为《Weight-Space Programming》的博客宣称，一个名为 Astra 的通用大语言模型可以在不借助优化器或任何外部工具的情况下，直接查看并手工修改一个小型 Qwen 模型的权重，从而显著提升其数学能力，有评论者提到提升幅度约为 5 倍。该博文还声称 Astra 仅凭权重就能判断小型网络是被什么任务训练出来的。 如果这一说法成立，就意味着大模型能够原生地推理神经网络参数，而不只是处理文本，这将是迈向「模型直接调试并改进其他模型」的重要一步。它对自动化模型改进、可解释性研究以及递归自我改进（RSI）研究都有明显意义，因此 Hacker News 上的讨论帖获得了超过 2000 分和近 700 条评论。 该演示仅限于小型 Qwen 模型和单一任务（数学），而且至少有一位从事权重空间学习研究的评论者认为，博客及其传播夸大了新颖性——编辑和生成权重的能力早已存在，并已在更大模型上实现。也有人反驳说，即便这项能力并非全新，看到一个「下一个词预测器」手工调权重来改善泛化表现依然令人惊叹。

hackernews · dbreunig · 11月2日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=50341174)

**背景**: 权重空间学习是一个新兴研究方向，它通过参数空间而非仅输入输出来研究神经网络；相关工作还包括「模型编辑」，即通过精准改动少量参数来改变模型的特定知识。Qwen 是阿里云发布的大语言模型系列，其中包含面向数学的专门版本。对这类演示的常见质疑是：看似「涌现」的能力可能只是训练数据的反映——例如早期 GPT 模型因为预训练语料中含大量国际象棋棋谱，而在国际象棋上表现异常出色。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50341174">Astra can read and write weights to improve Qwen | Hacker News</a></li>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪在震惊与怀疑之间分化。包括一位权重空间研究者的怀疑派呼吁大家先去读论文，认为结果被炒作而非史无前例；另一部分人则把它视为大模型快速理解复杂系统的又一例证，这类系统人类往往要花数月乃至数年才能掌握；还有第三种观点猜测，Astra 是刻意用神经网络权重数据训练的，是通往递归自我改进的一次尝试。

**标签**: `#LLM interpretability`, `#weight-space learning`, `#model editing`, `#Qwen`, `#AI research`

---

<a id="item-11"></a>
## [随笔呼吁读者为自己珍爱的网站做备份](https://blog.mistys-internet.website/post/2026/10/29/if-you-love-a-website-back-it-up/) ⭐️ 7.0/10

博客 mistys-internet.website 上的一篇题为《如果你爱一个网站，就把它备份下来》的短文主张，读者应当亲自归档自己看重的网站，而不是指望它们一直在线；这篇文章在 Hacker News 上引发了大规模讨论（约 438 分、100 条评论），话题集中在链接失效（link rot）与网页保存工具上。评论者们在帖中给出了 SingleFile、ArchiveWeb 扩展等具体推荐，也分享了论坛关停、链接返回 404 的亲历故事。 这场讨论凸显了开放网络已变得多么脆弱：当域名过期或网站改版时，人们所依赖的内容可能就此消失，而 Wayback Machine 也并非把所有内容都抓取下来。一些评论者把归档视为一种防御手段，用以应对未来由集中式云端大模型来代理、甚至悄然改写人们所能检索到的信息的局面。 被推荐的工具从 SingleFile 到 ArchiveWeb 不等：前者把页面连同媒体资源保存成一个自包含的 HTML 文件，适合快速的一次性抓取；后者允许用户在抓取时挑选具体页面和页面元素；此外还有可自托管的 ArchiveBox，适合长期持续收集。评论者还指出了工具链上的缺口——尤其是缺少对多次抓取结果做差异对比、以及方便地浏览 WARC/WACZ 文件的工具——并有一位提醒说归档行为应在你所在司法辖区内合法。

hackernews · ingve · 11月2日 13:25 · [社区讨论](https://news.ycombinator.com/item?id=50336518)

**背景**: 链接失效（link rot）是指超链接随着时间推移不再指向原始页面、文件或服务器，从而产生 404 错误和永久性数据丢失，这一现象已有大量记录。最主要的公共应对手段是互联网档案馆（Internet Archive）的 Wayback Machine：这是一个非营利数字图书馆，于 2001 年 10 月向公众开放，保存网页的历史快照，让用户能查看网站过去的样子。由于任何爬虫都无法抓全所有内容，于是出现了 ArchiveBox 这类可自托管工具（可把页面保存为 HTML、PDF、PNG、WARC、SQLite 等格式）以及各种浏览器抓取扩展，让个人自行保存页面，通常采用 WARC/WACZ 归档容器格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://web.archive.org/">Wayback Machine</a></li>
<li><a href="https://github.com/ArchiveBox/ArchiveBox">GitHub - ArchiveBox / ArchiveBox : Open source self-hosted web...</a></li>
<li><a href="https://archivebox.io/">ArchiveBox</a></li>

</ul>
</details>

**社区讨论**: 整体情绪高度支持，评论者描述了自己书签缓慢“腐坏”的过程，并指出对于他们需要的页面，Archive.org 上往往什么也没有。反复出现的主题是 AI 的局限与风险：一位评论者警告说，云端大模型可能在五年内取代开放互联网成为主要信息来源，并带来集中化控制与改写历史的能力；另一位则讲述自己请 Claude 从零散的存档中重建一个已消失的论坛，结果发现 AI 无法恢复真正已经丢失的数据。还有人呼吁更好的归档工具——对多次抓取做差异对比、深入浏览 WARC/WACZ 内容——说明需求不止于“保存下来”。

**标签**: `#digital-preservation`, `#web-archiving`, `#link-rot`, `#open-web`, `#community-discussion`

---

<a id="item-12"></a>
## [Cloudflare 将 DNS 区域构建延迟减半，内存占用降低 85%](https://blog.cloudflare.com/dns-targeted-zone-builds/) ⭐️ 7.0/10

Cloudflare 发布了一篇技术深度文章，介绍了其如何重新设计 DNS 的“定向区域构建”（targeted zone build）系统：区域构建延迟大约缩短了一半，峰值内存占用下降 85%（从约 79 GiB 降至 12 GiB）。完整区域重建量减少了约 40%，如今约 92.95% 的构建不再需要重建整个区域。 DNS 区域构建处于关键路径上：从客户修改一条记录，到该变更在全球生效，都要经过它。因此把构建延迟减半、内存占用降低 85%，能直接提升解析记录的生效速度，并提高基础设施的部署密度，惠及所有 Cloudflare DNS 客户。与此同时，在内存价格持续高企的背景下，这也是整个行业推动软件内存效率提升的一个具体案例。 这些收益源自从“整区重建”转向更具针对性的增量式区域构建，而这通常也意味着区域数据在内部采用了更接近关系型或结构化的表示方式。值得关注的权衡是正确性：增量构建路径往往会引入隐蔽的边界情况缺陷，这类问题只有在长期生产运行中才会暴露出来。

hackernews · wondersky · 11月2日 14:47 · [社区讨论](https://news.ycombinator.com/item?id=50337558)

**背景**: DNS 区域（zone）是存放某个域名或一组域名全部记录（A、AAAA、CNAME、MX、TXT 等）的容器；像 Cloudflare 这样的权威 DNS 服务商必须把这些记录编译成服务器可以直接应答查询的形式。过去，只要有任何改动就要重建整个区域，对于超大型区域或被众多客户共享的区域来说代价很高。“定向区域构建”（targeted zone build）指的是只重建区域中受影响的部分，从而不必重新处理未变更的数据、也不必为其重新分配内存。

<details><summary>参考链接</summary>
<ul>
<li><a href="/url?opi=89978449&q=CAESlAEB6zswFertidkCtHp9Q4TPSb-Bw4pqZBOixERul23K1vUS6Xkb8H0g69ws49FyQwu_RhOsXETyBRWcF9AWDUan5S496yhGeSxJLGx-1P_7e-ctKaybelHDMqEEKvqjX5J3Jue6u0QG10Myyu6BNqGhx5fDBOUmkya_bbemlYZgTU0rJmM5HtVEEncolOtxAlgBVTbl&sa=U&uoh=3&ved=2ahUKEwj-saTC9OqXAxW_AHkGHYBYNfkQFnoECA0QAg&usg=AOvVaw3IoP2BSGUtoaEEbPBHrcoX">How we halved DNS build delay and cut memory use by 85% | daily.dev</a></li>
<li><a href="/url?opi=89978449&q=CAESaAHrOzAVivfXBv544JvLwl2sJHcKXnn66OMU5J5AJBaILpg8a6SWEK6ih1irtV6JXvYpghq-f-FSNX6q2x7i8IEU2KNV7B33_HgwMtldxgoTwTNNOAIGZ9gz1CyUNKdfZE-gYqOlKHYr&sa=U&uoh=3&ved=2ahUKEwj-saTC9OqXAxW_AHkGHYBYNfkQFnoECAYQAg&usg=AOvVaw2U0awGzFqDvGOYy-U4zkC3">We halved DNS build delay and cut memory use by 85% | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者称赞 Cloudflare 的技术博客一贯质量很高；其中一个讨论串把这项工作与一个更宏观的问题联系起来：内存紧缺是否会推动业界开发更省内存的软件，以及这类研发在未来一到两年内的投入产出比如何。主要的质疑集中在规模上：有评论者怀疑，以 Cloudflare 的体量而言，每秒约 700 次变更是不是太低了；还有人好奇，放弃整区重建后，长期来看会引入哪些隐蔽的缺陷。

**标签**: `#DNS`, `#Cloudflare`, `#performance-optimization`, `#memory-efficiency`, `#infrastructure`

---

<a id="item-13"></a>
## [Legora 首席技术官谈如何打造“看不见”的法律 AI](https://latent.space/p/building-ai-for-lawyers-jacob-lauritzen-cto-of-legora/) ⭐️ 7.0/10

在 Latent Space 的一期访谈中，Legora 首席技术官 Jacob Lauritzen 解释了这家法律 AI 初创公司如何在“读不到任何一条 agent 执行轨迹”的情况下构建和评估其智能体——因为这些数据属于律所的客户。他还谈到了涉及数百万单元格的大规模表格审查，以及 AI 对律所“按小时计费”商业模式造成的日益增大的压力。 Legora 是增长最快的垂直 AI 公司之一，它针对“工作过程在法律上不可见”的智能体所提出的评估方案，可为医疗、金融等其他受保密约束的行业提供范本。关于按小时计费的讨论还表明，AI 的采用不仅改变专业服务公司的工具，也可能重塑其经济模式。 核心限制是结构性的而非技术性的：由于客户数据不能被记录或检视，传统的基于轨迹的调试和离线评估流水线都无法使用，团队只能寻找间接方法来测试智能体行为。产品还需要处理规模达百万单元格的表格审查，这一负载远超常见的对话式 LLM 用法；同时这些说法来自单一厂商的访谈，并未附公开的基准测试数据。

rss · Latent Space · 11月2日 23:01

**背景**: Latent Space 是一档聚焦“生产环境中的 AI 系统究竟如何搭建”的 AI 工程播客与通讯。“垂直 AI”指面向某一特定行业（此处为法律）打造的产品，相对于通用的横向工具，厂商认为这种专注能带来更深的护城河和更强的客户黏性。“轨迹（trace）”是智能体中间步骤的记录日志（提示词、工具调用、检索到的文档、输出），工程师通常依赖它来定位失败原因并构建评估。律所目前仍主要以小时计费，因此能够压缩检索和文件审阅时间的工具，会直接侵蚀支撑这些律所收入的商业模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://inhouseconnect.org/resource-center/news/horizontal-vs-vertical-legal-ai-which-one-holds-you-back/">Horizontal vs. Vertical Legal AI : Which One Holds... - In-House Connect</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://plenaura.com/blog/vertical-ai-niche-beats-general-purpose">Vertical AI : Why Niche Beats General Purpose in 2026 | Plenaura</a></li>

</ul>
</details>

**标签**: `#legal-tech`, `#LLM-evals`, `#AI-applications`, `#vertical-AI`, `#business-models`

---

<a id="item-14"></a>
## [谷歌联合业界捣毁 130 万台 Android 电视盒代理僵尸网络](https://krebsonsecurity.com/2026/11/tech-firms-dismantle-botnet-that-turned-1-3m-tv-boxes-into-proxies/) ⭐️ 7.0/10

谷歌表示已与多家行业合作伙伴联手，捣毁了一个由超过 130 万台 Android 电视盒子组成的僵尸网络；这些设备出厂时即带有恶意固件。该恶意软件会偷偷把用户的网络连接租给陌生人，并从事广告欺诈。参与此次行动的研究人员称，这次打击很可能切断了该僵尸网络对另外 1000 多万台受控系统的访问，其中包括基于 Android 的医疗设备和点歌机。 住宅代理僵尸网络让犯罪分子借助普通消费者的 IP 地址洗白恶意流量，使欺诈、撞库和扫描活动更难被溯源和封堵，因此摧毁其控制基础设施等于瘫痪一整项犯罪服务，而非仅仅阻止一次行动。此案还凸显了廉价物联网硬件的供应链安全问题：恶意软件在用户开机之前就已被植入，而受影响范围远不止电视盒子，还波及医疗设备等其他嵌入式设备。 由于恶意软件是在工厂被写入固件、而非通过漏洞利用投递，用户无法简单地将其卸载；130 万台这一数字反映的是运营者能够实际掌控的设备，而通过同一套控制基础设施还可能触达另外 1000 多万台设备。安全研究者已在通过灰色渠道销售的数百乃至上千款通用 Android 电视盒型号中，记录到 BADBOX 2.0、Kimwolf 等类似的固件预装恶意软件家族。

rss · Krebs on Security · 11月3日 02:24

**背景**: 僵尸网络（botnet）是由恶意软件感染、可被攻击者远程操控的大量联网设备组成的网络；在本案中，恶意代码在设备售出之前就已预装在硬件里。住宅代理（residential proxy）服务会把他人流量伪装成来自普通家庭宽带的真实用户 IP，因而对广告欺诈、账号撞库攻击和绕过基于 IP 的封禁极具价值。通过灰色渠道销售的廉价“全负载”Android 电视盒通常预装盗版流媒体应用和高度定制的固件，这让分发者得以在设备到达买家手中之前轻易植入持久化恶意软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://packet.guru/blog/tv-box-trojan-horse">Kimwolf Botnet: Is Your Cheap Android TV Box a Trojan... | packet.guru</a></li>
<li><a href="https://troypoint.com/fully-loaded-android-boxes/">Fully Loaded Android Boxes - Why You Should Avoid Them</a></li>

</ul>
</details>

**标签**: `#botnet`, `#IoT security`, `#Android`, `#cybercrime`, `#ad fraud`

---

<a id="item-15"></a>
## [OpenAI 推出 LifeVal 基准，评估 AI 日常任务能力](https://openai.com/index/lifeval) ⭐️ 7.0/10

OpenAI 推出了 LifeVal 基准，用于衡量 AI 模型在寻找托儿服务、管理财务和处理政府文书等日常任务中帮助人们完成工作的能力。 LifeVal 将评估重点转向实际生活中的辅助能力，而非学术考试或编程竞赛，这可能更真实地反映 AI 助手在日常生活中的实用性，并影响开发者和用户比较模型的方式。 该公告篇幅简短，未提供任务设计、评分方法或模型结果等详细技术信息，因此目前更像是一个方向性的基准提议，而非完整记录的评估套件。

rss · OpenAI News · 11月2日 09:00

**背景**: AI 基准是用于比较模型能力的标准化测试，近年来越来越多的基准开始关注智能体、长周期或真实世界任务，而非孤立的知识问答。LifeVal 属于这一更广泛的趋势，旨在评估模型能否做出决策、采取行动并处理人们真正希望获得帮助的日常责任。这类基准之所以重要，是因为学术考试的高分并不一定意味着模型能提供有用的日常协助。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/lifeval/">LifeVal | OpenAI</a></li>
<li><a href="https://www.crypto-headlines.com/articles/1293608-openai-unveils-lifeval-benchmark-for-everyday-ai-tasks">OpenAI unveils LifeVal benchmark for everyday AI... | Crypto-Headlines</a></li>
<li><a href="https://bitcoinnewsinvest.com/openai-unveils-lifeval-benchmark-for-everyday-ai-tasks/">OpenAI unveils LifeVal benchmark for everyday... - BitcoinNewsInvest</a></li>

</ul>
</details>

**标签**: `#AI evaluation`, `#benchmark`, `#OpenAI`, `#LLM`, `#everyday tasks`

---

<a id="item-16"></a>
## [朝鲜相关创纪录黑客事件后，币安净流出达 47 亿美元](https://www.japantimes.co.jp/business/2026/11/02/binance-outflows-north-korea-hack/) ⭐️ 7.0/10

据币安（Binance）一位发言人称，在发生一起被归咎于朝鲜、规模创纪录的黑客事件之后，截至伦敦时间周一上午，该交易所的净提现额已达到 47 亿美元。这一数字反映了事件发生后用户将资产撤离平台所造成的资金外流。 如此规模的提现说明，在发生重大安全漏洞之后，一家大型交易所可能多快地遭遇流动性与信任冲击，这也使中心化加密货币平台的安全实践再次受到审视。此外，一起与朝鲜相关、规模创纪录的黑客事件，其影响超出加密市场本身，因为历史上被盗资金曾被指与相关国家的资金筹措有关。 这一外流数字是以美元计价的净提现额，统计时间截至伦敦时间周一上午，并由币安发言人予以确认。现有报道尚未说明具体受影响的钱包或区块链网络、被盗资金的确切规模，以及平台是否已暂停提现。

rss · The Japan Times · 11月2日 11:57

**背景**: 币安是全球最大的加密货币交易所之一，这类中心化交易所通过热钱包和冷钱包持有客户存款，历来是攻击者的重点目标。与朝鲜相关的黑客组织（如 Lazarus）长期针对加密平台和 DeFi 协议发动攻击，被盗资产往往通过混币器和跨链桥进行洗钱。链上分析师通常把交易所的大额净流出视为存款人焦虑的信号，因为当用户担心平台的偿付能力或安全性时，往往会将代币转移出平台。

**标签**: `#cryptocurrency`, `#cybersecurity`, `#Binance`, `#North Korea`, `#financial markets`

---

<a id="item-17"></a>
## [百度网盘摇一摇广告改用磁力计判方向，绕过运动权限限制](https://t.me/zaihuapd/44850) ⭐️ 7.0/10

一名开发者借助 AI 辅助分析百度网盘 iOS 版（10 月 22 日发布的 13.36.0 版本）的广告跳转逻辑，发现框架内存在一个名为 NoShake 的「没有运动」变体，完全绕开了 CoreMotion。该变体改用 Core Location 的 CLHeading 接口读取磁力计数据来判断手机是否被晃动，因此用户即使禁用了陀螺仪和加速度计权限，仍然会被摇一摇跳转广告；报告还提到在特定参数下等待约 1 秒会自动执行一次广告点击。 这是一起具体的权限绕过与暗黑模式案例：用户以为关闭运动权限就等于拒绝了摇一摇广告，但应用仍能通过另一条传感器通道判断晃动。它揭示出 iOS 上的传感器权限分散在不同框架之中，也为应用审计和隐私社区提供了一套可复用的排查思路，用来识别这类规避行为。 这一发现的关键在于 Core Location 这条通道：CLHeading 会提供由磁力计计算出的方向更新，而应用只要已获得定位权限，就能在没有「运动与健身」权限（该权限管控 CoreMotion 的加速度计与陀螺仪）的情况下拿到这些数据。分析是在 13.36.0 的二进制文件上借助 AI 完成的，报告指出在特定参数下约 1 秒后会自动触发广告点击，这比单纯跳转落地页更进一步。

telegram · zaihuapd · 11月2日 09:27

**背景**: 在 iOS 上，运动传感器通常通过苹果的 CoreMotion 框架访问，需要用户授予「运动与健身」权限；广受诟病的「摇一摇跳转广告」正是依赖该框架读取加速度计数据实现的。Core Location 则是另一个负责定位与指南针方向的框架，其方向数据来自设备磁力计，通过感知地球磁场和手机倾斜状态来判断朝向。由于 Core Location 受定位权限而非运动权限管控，一个已获得定位权限的应用无需申请运动权限也能推断设备是否在移动——这正是本次发现所利用的缺口。

**标签**: `#privacy`, `#iOS`, `#reverse-engineering`, `#mobile-ads`, `#dark-patterns`

---

<a id="item-18"></a>
## [WIRED 调查发现 400 多个 AI 应用暗藏色情深伪功能](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 7.0/10

WIRED 于 11 月 2 日发布的调查揭露了一个由 400 多个相互关联的应用与网站组成的网络：它们伪装成宠物画像、语言学习等普通 AI 工具，却在特定条件下加载色情深伪界面，允许用户上传他人照片生成露骨图像或视频。在 WIRED 提供线索后，苹果下架了 19 款应用；谷歌在此前已移除 9 月仍在 Google Play 上架、累计下载超 35 万次（不少标注为适合所有年龄）的 27 款应用中的大部分；Meta 则阻止了 209 款相关应用投放广告。 这一事件表明，主流应用商店与广告网络很容易被用来分发未经同意的色情深伪内容，使原本小众的滥用行为变成面向普通用户的大众化产品。它同时给苹果、谷歌和 Meta 施加压力：平台不仅要审查应用安装包本身，还要监管其审核流程未能完全覆盖的远端网页内容与广告投放链路。 研究人员通过共享代码、域名注册信息和广告追踪标识将这些应用关联起来；WIRED 依据中文代码、托管信息与域名线索，将该网络与中文开发者及一家香港注册公司联系起来，但报道强调这一关联属于媒体与研究人员的调查判断，运营方未回应置评请求。苹果表示，开发者在通过审核后替换了远端网页内容，这种手法使应用的获批版本与实际呈现给用户的内容不一致。

telegram · zaihuapd · 11月2日 12:45

**背景**: 深度伪造（deepfake）指利用 AI 生成或编辑的图像、视频与音频，让人物呈现出从未发生过的事情；而色情深伪——即针对真实人物、通常在未经同意情况下合成的露骨影像——是这项技术最普遍也最具危害性的用途之一。移动应用商店依赖对提交应用的审核流程，因此那些主要从远端服务器拉取内容的应用可以先通过审核、之后再展示不同内容。广告网络则构成另一条分发渠道，因为广告追踪标识也能揭示看似互不相关的众多应用其实由同一运营方掌控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Deepfake">Deepfake - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Deepfake_pornography">Deepfake pornography - Wikipedia</a></li>

</ul>
</details>

**标签**: `#deepfakes`, `#AI safety`, `#app store moderation`, `#privacy`, `#investigative reporting`

---

<a id="item-19"></a>
## [瑞典 ICA 门店遭网络攻击，冷柜被远程调至 50°C](https://x.com/InsiderGeo/status/2117164877701595165) ⭐️ 7.0/10

瑞典连锁超市 ICA 表示，多家门店在夜间遭到网络攻击，冷藏柜和冷冻柜被远程设定为 50°C，斯约博（Sjobo）和托梅利拉（Tomelilla）等地的门店受到影响。相关门店上午暂停营业，预计当地时间 9 点左右重新开放，ICA 已就此事向顾客致歉。 这是一起典型的针对运营技术（OT）的网络物理攻击：攻击者没有窃取数据，却通过纯数字手段直接导致食品变质、门店停业，说明楼宇自动化和制冷控制器已成为一线攻击目标。该事件发生在法国和美国出现类似攻击仅数周之后，表明这更像是针对零售业暴露在外的冷链与物联网控制器的一轮系统性攻击，而非孤立恶作剧。 报道未说明攻击者如何获得访问权限，但 50°C 的设定值暗示被滥用的是可远程访问的制冷或楼宇管理控制器，而非 ICA 的核心企业网络遭到入侵。除食品损耗外，此类篡改还可能造成压缩机损坏、除霜循环引发火灾以及食品安全合规问题；门店仅在上午短暂停业，说明恢复工作主要依靠现场人工重新配置。

telegram · zaihuapd · 11月2日 13:52

**背景**: 现代超市通过联网的楼宇管理和制冷控制器来运行冷柜机组、暖通空调和照明系统，其中许多设备可以直接从互联网访问，以便承包商远程维护。这类设备属于运营技术（OT），即工业与物理过程控制系统；它们过去通常与互联网隔离，如今却越来越多地接入 IT 网络。这种融合让攻击者能够从一台暴露的控制器直达现实世界的后果，而 OT 系统在打补丁和监控方面远难于普通办公 IT。近期类似攻击已针对法国数百家超市的制冷控制器，温度被推高到约 50°C，据报道部分设备还发生了起火。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.securitymagazine.com/articles/102356-ot-cybersecurity-is-maturing-but-visibility-is-still-a-challenge">OT Cybersecurity Is Maturing, But Visibility Is Still... | Security Magazine</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#IoT`, `#OT-security`, `#cyberattack`, `#retail`

---

<a id="item-20"></a>
## [Anthropic 据报公开提交纳斯达克 IPO 申请，股票代码 ANT](https://t.me/zaihuapd/44858) ⭐️ 7.0/10

10 月 26 日，一个 Telegram 科技频道报道称，Anthropic 已公开提交纳斯达克 IPO 申请，股票代码为「ANT」，计划于 11 月中旬挂牌，由摩根士丹利和高盛牵头承销。该帖引用招股书草稿称，公司上半年营收达 163 亿美元，而去年同期仅为 11 亿美元；净亏损为 807 亿美元，其中约 720 亿美元来自可转债等融资工具。 如果消息得到证实，Anthropic 在纳斯达克上市将成为迄今为止规模最大、最受关注的 AI 行业 IPO 之一，使公开市场投资者首次能够直接持有这家领先的前沿模型开发商。这也将为 OpenAI 等竞争对手及其他资金充裕的 AI 实验室树立估值与信息披露的参照基准。 该报道强调，807 亿美元的净亏损主要是非经营性项目，其中约 720 亿美元来自可转债等融资工具，这意味着实际经营性亏损要小得多。但这一说法仅有单一信源，来自 Telegram 频道而非链接到美国证监会的申报文件，且营收在一年内从 11 亿美元跃升至 163 亿美元实属罕见，因此在 S-1 文件公开前，相关数字应被视为未经证实。

telegram · zaihuapd · 11月2日 15:12

**背景**: Anthropic 是开发 Claude 系列模型的 AI 安全公司，注册为公益公司（PBC），并获得包括谷歌在内的多家战略投资者支持，据报英伟达和微软也参与投资。在美国上市，公司必须向美国证监会提交注册说明书（通常为 S-1 表格），其中包含经审计的财务数据，之后股票才能在纳斯达克等交易所挂牌；所谓「公开提交」意味着该文件对所有人可见，而此前的保密草稿则不会公开。可转债和可转换优先股是上市前常见的融资工具，相关会计规则可能要求公司在这些工具转换或重新计量时计入大额非现金费用，因此财报上的净亏损往往比基于现金的经营业绩看起来糟糕得多。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO`, `#AI industry`, `#funding`, `#unverified news`

---

<a id="item-21"></a>
## [阿布扎比与 OpenAI 签署四项协议，启动「机器可读政府」试点](https://thenextweb.com/news/openai-abu-dhabi-deals-machine-readable-government-mubadala) ⭐️ 7.0/10

阿布扎比于周一与 OpenAI 签署了四项协议，其中「机器可读政府」计划把政策法规转换为 AI 可读格式，以协助官员核查许可与证书申请，目前已在食品进口场景开展试点。与此同时，穆巴达拉与 OpenAI 及 G42 旗下 Inception42 合作开展投资分析；Inception42 另签五年协议，向阿联酋政府、企业和学校提供模型；ADNOC 则成为首家使用 OpenAI Frontier 平台的能源公司。 这是迄今为止 OpenAI 技术在公共部门最具体的落地之一，其意义不止于聊天助手，而是把监管规则本身编码为机器可读形式，这种做法很可能被其他政府研究并效仿。与此同时，在各大 AI 厂商激烈争夺国家级合同之际，此举也加深了 OpenAI 与 G42、穆巴达拉、ADNOC 等海湾主权 AI 力量的绑定。 在许可审查试点中，官员明确保留最终决定权，且初期范围刻意收窄至食品进口，之后再考虑扩大。Inception42 的五年协议覆盖政府、企业与学校，而 ADNOC 采用的 OpenAI Frontier 是 2026 年初推出的企业级 AI 智能体构建与管理平台，ADNOC 也因此成为该平台的首家能源行业客户。

telegram · zaihuapd · 11月2日 15:55

**背景**: 「机器可读政府」是指把法律、政策与法规从 PDF、自然语言文本等人类可读的形式，转换为结构化、机器可处理的格式，使软件与 AI 模型能够查询并推理其中的规则。这正是 AI 辅助许可预审的前提：系统可以自动将申请材料与相关规则比对，再由人工审核人员作出决定，美国能源部等机构也在试验类似做法。OpenAI Frontier 是 OpenAI 于 2026 年 2 月发布的企业级平台，用于构建、部署和管理与记录系统集成的 AI 智能体。Inception42 是 G42 位于阿布扎比的 AI 业务部门，其另与微软合作，可在 Microsoft 365 应用中运行数据不出境的主权 AI 智能体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.agbi.com/ai/2026/07/inception42-targets-q3-for-uae-agentic-ai-rollout/">Inception 42 targets UAE agentic AI rollout in third quarter | AGBI</a></li>
<li><a href="https://tbreak.com/microsoft-inception42-bring-uae-sovereign-ai-agents-microsoft/">Microsoft, Inception 42 Put UAE Sovereign AI Agents in Copilot</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Abu Dhabi`, `#AI governance`, `#public sector AI`, `#technology partnerships`

---