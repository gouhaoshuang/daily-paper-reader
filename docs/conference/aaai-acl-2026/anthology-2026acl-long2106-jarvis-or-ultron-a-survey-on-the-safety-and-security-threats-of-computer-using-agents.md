---
title: JARVIS or Ultron? A Survey on the Safety and Security Threats of Computer-Using Agents
title_zh: JARVIS还是奥创？计算机使用智能体的安全与安保威胁综述
authors: "Ada Chen, Yongjiang Wu, Junyuan Zhang, Jingyu Xiao, Shu Yang, Jen-tse Huang, Kun Wang, Wenxuan Wang, Shuai Wang"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.2106.pdf"
tags: ["query:mobile-agent"]
score: 7.0
evidence: 系统梳理计算机使用智能体（包括移动端）面临的安全威胁，对应移动智能体部署中的挑战
tldr: 计算机使用智能体能够自主操作桌面应用、网页和移动应用，但也引入了新的安全与安保风险。本综述系统化地梳理了由LLM推理漏洞、多组件集成复杂性和多模态输入带来的威胁，并对攻击面进行分类。综述提供了对该领域安全问题的全面认知，为移动端等计算机使用智能体的安全部署和后续研究奠定基础。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2106/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1655, \"height\": 2364, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2106/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1643, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2106/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1640, \"height\": 502, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2106/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1641, \"height\": 670, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2106/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1648, \"height\": 429, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2106/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1645, \"height\": 1760, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2106/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1644, \"height\": 2197, \"label\": \"Table\"}]"
motivation: 计算机使用智能体操作移动应用等带来新的安全与安保风险，缺少系统梳理。
method: 采用系统化方法，从推理漏洞、软件集成和多模态输入三个维度分析威胁。
result: 给出威胁分类和防护研究现状，明确关键脆弱环节。
conclusion: 为包括移动端在内的计算机使用智能体安全部署提供了参考框架。
---

## Abstract
Recently, AI-driven interactions with computing devices have advanced from basic prototype tools to sophisticated, LLM-based systems that emulate human-like operations in graphical user interfaces. We are now witnessing the emergence of Computer-Using Agents (CUAs), capable of autonomously performing tasks such as navigating desktop applications, web pages, and mobile apps. However, as these agents grow in capability, they also introduce novel safety and security risks. Vulnerabilities in LLM-driven reasoning, with the added complexity of integrating multiple software components and multimodal inputs, further complicate the security landscape. In this paper, we present a systematization of knowledge on the safety and security threats of CUAs. We conduct a comprehensive literature review and distill our findings along four research objectives: (i) define the CUA that suits safety analysis; (ii) categorize current safety threats among CUAs; (iii) propose a comprehensive taxonomy of existing defensive strategies; (iv) summarize prevailing benchmarks, datasets, and evaluation metrics used to assess the safety and performance of CUAs. Building on these insights, our work provides future researchers with a structured foundation for exploring unexplored vulnerabilities and offers practitioners actionable guidance in designing and deploying secure Computer-Using Agents.

---

## 论文详细总结（自动生成）

# 《JARVIS还是奥创？计算机使用智能体的安全与安保威胁综述》详细总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究对象**：Computer-Using Agents（CUAs，计算机使用智能体）——一类基于 LLM 的系统，能够通过多模态感知（截图、HTML、UI 树）、高级推理和工具调用能力，像人类用户一样操作图形用户界面（GUI），包括桌面应用、网页和移动应用。
- **现实进展**：系统如 AppAgent、SeeAct、PC-Agent，以及 OpenAI 的 o3、o4-mini 等，展示了 CUA 自主完成订购商品、预约、填写表单等端到端任务的能力。
- **核心问题**：CUA 能力越强，其引入的新型安全与安保风险也越大。与传统 LLM 相比，CUA 的安全问题因三个因素而更加复杂：
  - LLM 推理本身的内在漏洞；
  - 多软件组件集成带来的攻击面扩大；
  - 多模态输入（图像、文本、结构数据）带来的新的攻击向量。
- **研究空白**：已有综述或聚焦于 CUA 的能力构建（如 OS agents、GUI agents 相关综述），或泛泛讨论通用 LLM/智能体的安全，缺少一个专门针对 CUA 独特安全挑战的、威胁-防御-评估三位一体的系统化梳理。
- **本文目标**：通过四个研究目标提供系统化知识：① 定义适合安全分析的 CUA；② 归类 CUA 面临的安全威胁；③ 提出防御策略分类法；④ 总结评估基准与指标。

## 2. 方法论：核心思想、技术细节与流程

### 2.1 系统性文献综述方法（核心思想）

- 从 2022 年起对 CUA 安全与安保相关文献进行全面检索：
  - **数据库选择**：arXiv、Semantic Scholar、Google Scholar、OpenReview；
  - **关键词检索**：筛出 700+ 篇潜在相关论文；
  - **筛选过滤**：人工逐篇审查，剔除重复或与 CUA 安全威胁/防御不直接相关的论文，最终保留 **124 篇** 进行深度分析。

### 2.2 CUA 的形式化定义

- 定义 CUA 为：结合**多模态感知**（Perception）、**推理决策大脑**（Brain）、**行动执行**（Action）三组件，能够像人类一样操作 GUI 和应用的技术体系。
- 划归为四类从属概念：**OS Agent**（操作系统级）、**GUI Agent**（界面级）、**Web Agent**（网页环境）、**Device-control Agent**（设备控制）。

### 2.3 威胁分类法（核心框架）

**威胁分为两大类：**

- **内在威胁（Intrinsic Threats）**——源于智能体自身配置、训练或固有局限，细分为 8 种：
  - 感知组件（1 种）：UI 理解与接地困难（UI Understanding & Grounding Difficulties）；
  - 大脑组件（6 种）：调度错误、错位、幻觉、上下文过长、社会文化关切、响应延迟；
  - 行动组件（1 种）：API 调用错误。

- **外在威胁（Extrinsic Threats）**——由外部恶意实体发起，细分为 8 种：
  - 对抗攻击（Adversarial Attack）；
  - 提示注入攻击（Prompt Injection Attack，分直接注入和间接注入，含视觉提示注入、环境注入、任务对齐注入、细印注入、自适应注入等）；
  - 越狱攻击（Jailbreak Attack，含单智能体与多智能体协同变体）；
  - 记忆攻击（Memory Attack，分为记忆提取与记忆投毒）；
  - 后门攻击（Backdoor Attack，含输入触发、视觉触发、推理链后门、多子后门组合）；
  - 推理鸿沟攻击（Reasoning Gap Attack，跨模态信号冲突）；
  - 系统破坏攻击（System Sabotage Attack）；
  - 网页黑客攻击（Web Hacking Attack）。

**威胁刻画三维度**：威胁来源（环境/提示/模型/用户，区分主要/次要）、受影响组件（感知/大脑/行动）、威胁模型（发起者）。

### 2.4 防御分类法（核心框架）

- 归纳 **14 类防御策略**：环境约束、输入验证、防御性提示、数据清洗、对抗训练、输出监控、模型检查、交叉验证、持续学习与自适应、透明化、拓扑引导、感知算法协同、以规划为中心的架构优化、预定义法规合规。
- 每个防御方法沿三个轴刻画：目标组件、强化的智能体框架环节、所缓解的威胁编号（建立威胁-防御映射表）。

## 3. 实验设计：数据集、Benchmark 与评估体系

> 本文为综述论文，不包含原始实验，但其核心"实验"体现在系统化的基准汇总和分析框架上。

### 3.1 数据/基准场景分类

- **Web 场景**（典型代表）：
  - ST-WebAgentBench（235 个策略增强任务）、BrowserART（100 种有害浏览器行为）、CASA（1225 条用户查询 + 622 条网页观察）、SafeArena（250 安全 + 250 有害任务）、WASP（84 个任务）、VPI-Bench（306 个视觉提示注入用例）、AgentDAM（246 个任务）、PrivacyLens（493 个隐私种子）等。

- **移动场景**：
  - MobileSafetyBench（80 个任务，覆盖消息、社交媒体、金融、系统工具）、Hijacking JARVIS（58 个动态任务 + 210 张静态截图的攻击场景）。

- **通用场景**（进一步细分）：
  - **工具使用场景**：ToolEmu（36 个工具包、144 个任务）、RAS-Eval（80 个核心用例 + 3802 个攻击任务）、AgentDojo（97 个任务、629 个安全用例）、InjecAgent（330 个工具）、AgentHarm（110 个恶意行为 + 330 个增强任务）、Agent Security Bench（400 个工具/任务）、Agent-SafetyBench（2000 个用例、349 个环境）；
  - **混合/异构环境**：OpenAgentSafety（350 个多轮多用户任务）、RiOSWorld（492 个风险任务）、RedTeamCUA（864 个混合 Web-OS 对抗场景）、MLA-Trust（34 个高风险任务）、HAICOSYSTEM（132 个场景、8000+ 模拟回合）、AgentHazard（2653 个实例）；
  - **风险意识/多维安全**：R-Judge（569 条多轮交互记录）、TrustAgent（70 个样本）。

### 3.2 评估指标

- **任务完成指标**：Task Success Rate（TSR）/Benign SR/PNA、Helpfulness、TCR、TIR、TFR 等；
- **中间步骤指标**：Step Success Rate（SSR）、Total Correct Prefix；
- **安全与鲁棒性指标**：Attack Success Rate（ASR）、NRP（净韧性表现 = PNA × (1−ASR)）、Completion under Policy（CuP）/Partial CuP、F1 及衍生指标（FPR/FNR/Specificity）、Refusal Rate（RR/RtE）、Leakage Rate（LR/LRh）、Attempt Rate（AR/RGI）、文化社会规范指标（AC-R、Edu-R）、Harm/ Harmfulness Score、Toxicity Score 等。

### 3.3 评测方式

- **规则评测**：基于确定性规则（环境状态比对、轨迹匹配、关键字检测），可扩展但难以捕捉上下文细微差异；
- **LLM-as-a-judge 评测**：用 GPT-4/GPT-4o 等对行为分类、打分或风险分级，灵活但存在变异性和成本问题；
- **人工评测**：作为金标准验证自动评测，但成本高、难以规模化。

## 4. 资源与算力

- **全文未提及任何具体算力信息**——包括 GPU 型号、数量、训练时长、推理成本等。
- 原因在于：本文是**纯文献综述研究**，不涉及模型训练或微调，也不进行攻击或防御实验的实测。唯一涉及的计算资源相关讨论是对基准报告中"推理成本"（Inference Cost，如 ShieldAgent-Bench）的引用，而非本文自身的计算开销。

## 5. 实验数量与充分性

- **作为综述**：系统收集 700+ 候选文献，精读 124 篇，覆盖了 CUA 安全研究的主要攻击、防御和评估工作；
- **基准覆盖广度**：汇总了 20+ 个代表性安全基准/数据集，横跨 Web、移动、桌面/OS、混合环境及纯工具场景，场景维度较全面；
- **公平性评估**：
  - 优点：威胁与防御的分类均有明确的维度标注（来源、组件、威胁模型），并给出威胁-防御映射表，便于交叉验证与定位；
  - 不足：各基准之间的可比性有限（数据规模、任务难度、评测方式差异大），论文未对不同防御策略的有效性进行定量横向比较或元分析；
  - 偏差风险：主要依赖英语公开来源，可能遗漏非英语或闭源研究。

## 6. 主要结论与发现

- **关键洞察一：实时性与多模态压力**。CUA 在动态 GUI 环境中运行，对低延迟推理、多模态接地、设备端资源使用提出了严苛要求。
- **关键洞察二：接地与感知鸿沟是核心短板**。多数 CUA 在安全基准上表现不佳的根源是 UI 接地脆弱——误读视觉/结构线索、产生多模态幻觉，亟需更全面的训练与测试场景。
- **关键洞察三：实验场景过于受限**。现有 CUA 评估大多在高度约束的小规模设置下进行，不能反映真实世界高风险任务的广度和动态性。
- **关键洞察四：透明度缺失**。CUA 提供商缺乏可见的安全策略与系统性评估结果公开，削弱了问责机制和用户信任。
- **关键洞察五：威胁-防御映射揭示了防御研究的不均衡**。提示注入和对抗攻击获得的防御研究最多，而社会文化关切、响应延迟、推理鸿沟攻击、系统破坏等威胁的防御研究相对薄弱。
- **未来方向**：集成化防御机制、实时综合基准、透明度与问责机制、人在环路安全防护、可扩展的审计机制。

## 7. 优点（亮点）

- **首个聚焦 CUA 安全与安保的系统化综述**：区别于已有综述聚焦一般 LLM 智能体安全，本文专门针对"感知-推理-行动"紧密耦合的 CUA 场景；
- **统一覆盖 Web、移动、桌面多场景**：对 OS Agents、GUI Agents、Web Agents、Device-control Agents 提供统一的安全分析框架；
- **明确的威胁-防御映射**：每类防御策略标注了其目标威胁类别（内外威胁编号），可操作性强的结构化框架；
- **完整的研究闭环**：威胁建模（是什么）、防御机制（怎么防）、评估基准（怎么量）三位一体，为后续研究提供一站式参考；
- **细粒度的内在威胁分析**：将内在威胁定位到感知/大脑/行动具体组件并溯源至环境/提示/模型/用户，为诊断智能体故障提供精确坐标；
- **详尽的附录支撑**：对每种攻击给出具体变体（如细印注入、足入门效应攻击、跨模态注入、多子后门组合等）和代表文献，有很好的史料价值。

## 8. 不足与局限

- **领域快速演进导致的覆盖不完整**：论文自身承认，提交时可能遗漏了新兴攻击手段、防御方法或基准数据；
- **语言与来源偏倚**：主要依据英语公开学术资源，可能低估了闭源系统（如商业产品安全实践）和非英语研究社区的成果；
- **缺乏实证量化评估**：对各类威胁的有效性、严重性，以及防御策略的相对效能，没有进行实际的实验对比或元分析，仅停留在定性分类层面；
- **分类法的主观性风险**：威胁与防御之间并非一一对应，部分防御可泛化到多个威胁类别，表格中的映射关系带有作者的判断成分；
- **基准可比性问题**：各基准的数据规模、采集方式、难度和评测方式差异较大，论文未提供归一化对比或有意义的横向参考框架；
- **应用局限**：框架的实用性未在真实 CUA 系统中得到验证，对实践者的指导主要停留在"该做什么"的层面，缺乏"怎么做"的操作性细节（如具体的提示词设计、阈值设定等）。

（完）
