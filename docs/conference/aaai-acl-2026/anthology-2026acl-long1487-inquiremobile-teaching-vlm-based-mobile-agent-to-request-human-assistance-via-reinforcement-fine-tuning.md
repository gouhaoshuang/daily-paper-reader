---
title: "InquireMobile: Teaching VLM-based Mobile Agent to Request Human Assistance via Reinforcement Fine-Tuning"
title_zh: InquireMobile：通过强化微调教会基于VLM的移动智能体请求人类帮助
authors: "Qihang Ai, Pi Bu, Yue Cao, Yingyao Wang, Jihao Gu, Jingxuan Xing, Zekun Zhu, Wei Jiang, Zhicheng Zheng, Jun Song, Yuning Jiang"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.1487.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 通过主动询问人类来评估和训练移动智能体的安全交互能力
tldr: 针对移动视觉语言智能体在自主执行时理解或推理不足可能带来安全风险的问题，提出InquireBench基准，覆盖5大类22子类以评估智能体安全交互与主动询问能力。在此基础上，采用强化微调训练VLM移动智能体在必要时主动请求人类确认。实验表明现有智能体在该基准上近乎零分，而所提方法能有效提升其安全求助行为。该工作为移动智能体的安全部署与负责任任务执行提供了评测基准与训练范式。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1487/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1617, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1487/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1619, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1487/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 634, \"height\": 629, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1487/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1638, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1487/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 705, \"height\": 437, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1487/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1615, \"height\": 717, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1545, \"height\": 591, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1656, \"height\": 1034, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 799, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 796, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 799, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1566, \"height\": 982, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1283, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1487/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1627, \"height\": 522, \"label\": \"Table\"}]"
motivation: 移动智能体完全自主执行存在安全隐患，应学会在能力不足时主动求助。
method: 构建InquireBench基准并提出基于强化微调的交互训练方法，使智能体学会主动请求人类确认。
result: 大多数现有VLM智能体在基准上近乎零分，所提方法显著提升安全交互能力。
conclusion: 主动询问机制与基准可提高移动智能体在真实环境中的安全性和可信度。
---

## Abstract
Recent advances in Vision-Language Models (VLMs) have enabled mobile agents to perceive and interact with real-world mobile environments based on human instructions. However, the current fully autonomous paradigm poses potential safety risks when model understanding or reasoning capabilities are insufficient. To address this challenge, we first introduce InquireBench , a comprehensive benchmark specifically designed to evaluate mobile agents’ capabilities in safe interaction and proactive inquiry with users, encompassing 5 categories and 22 sub-categories, where most existing VLM-based agents demonstrate near-zero performance. In this paper, we aim to develop an interactive system that actively seeks human confirmation at critical decision points. To achieve this, we propose InquireMobile , a novel model inspired by reinforcement learning, featuring a two-stage training strategy and an interactive pre-action reasoning mechanism. Finally, our model achieves an 46.8% improvement in inquiry success rate and the best overall success rate among existing baselines on InquireBench. The project page is available at https://bit-aqh.github.io/InquireMobile/homepage/ .

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究背景**：近年来，视觉语言模型（VLM）的发展使移动智能体（mobile agent）能够根据人类指令自主感知和操作真实手机环境。然而，现有移动智能体普遍采用**完全自主执行范式**，默认对模型自身的理解与推理能力抱有“绝对信任”。
- **核心问题**：当模型能力不足以应对复杂、模糊或高风险的场景时，完全自主执行可能带来严重安全风险，例如：
  - 错误理解支付界面指令，导致意外金融交易；
  - 误删文件、误操作敏感个人信息；
  - 在需要登录、授权、确认等关键节点缺少人机交互反馈。
- **核心主张**：稳健的移动智能体不应仅与环境交互，还必须建立**主动与用户交互的反馈机制**——即在关键决策点（低置信度、潜在风险、意图不明）主动向用户确认或澄清，将“人类在环”（human-in-the-loop）引入智能体系统，从而提升安全性、透明度和可信度。
- **整体含义**：该论文首次系统性地关注“智能体主动求助”这一被忽视的能力维度，并提出完整的评测基准与训练方法，为移动智能体的安全部署提供了新范式。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 2.1 核心思想

论文提出 **InquireMobile**，一种基于强化微调（Reinforcement Fine-Tuning）的 VLM 移动智能体模型，核心思想是**教会智能体在关键决策点主动请求人类帮助**，采用两阶段训练策略：
1. **冷启动阶段（Stage 1）**：监督微调（SFT），获得稳健的输出格式和基础 GUI 交互能力；
2. **强化学习阶段（Stage 2）**：使用 GRPO（Group Relative Policy Optimization）增强模型的推理与思考能力，学会区分“何时需要询问”和“何时不需要询问”。

### 2.2 关键技术细节

- **交互式行动前推理机制（Pre-action Reasoning）**：
  - 在执行关键动作之前，模型先进行两步推理：① 判断当前观察是否需要进行询问；② 生成结构化的文本查询以请求用户输入或表达不确定性。
  - 输出格式为 `<think>`（内部推理过程）+ `<tool_call>`（JSON 格式的动作调用）。

- **两阶段训练策略**：
  - **Stage 1（SFT）**：使用 LoRA（rank=8），2 个 epoch，学习率 1.0×10⁻⁴，训练数据包括 975 条询问数据 + 3,000 条通用 GUI 数据；
  - **Stage 2（GRPO）**：2 个 epoch，每个样本生成 4 条候选响应，探索温度设为 1，最大步数 15，使用基于规则的奖励函数。

- **奖励函数设计**（R = R_F + R_T + R_A）：
  - **格式奖励（R_F）**：鼓励模型输出结构化的 `<think>` 和 `<tool_call>` 格式，匹配为 1，错误为 −1；
  - **动作类型奖励（R_T）**：动作类型是否与真实标签匹配，包括 click、swipe、type、call_user 等 9 种原子动作；
  - **动作参数奖励（R_A）**：
    - 基于坐标的动作（如 click）：预测坐标是否落入真实 GUI 元素的包围框内；
    - 基于文本的动作（如 type、call_user）：计算生成文本与真实文本的 BLEU 分数并归一化到 [0,1]。

### 2.3 数据收集流程（InquireBench）

- **随机游走触发**：在真实 Android 手机（华为、小米）上模拟日常生活行为，执行“随机游走”采集约 80,345 张屏幕截图；
- **人工标注分类**：标注者识别需要人类干预的截屏，分为 5 大类（意图确认、隐私与安全、风险场景、组合类、其他类）；
- **任务与思考生成**：人工标注者为每张图片编写有效任务，并使用 GPT-4o-0806 生成交互原因和交互内容，再经过人工审核与修改。

## 3. 实验设计：数据集、基准与对比方法

### 3.1 数据集与基准（InquireBench）

- **InquireBench**：975 条标注数据，来自 173 个任务、37 个 App（中英双语），跨 5 大类别、22 个子类别；
- **数据分布**：
  - 风险场景 52 条（如微信、Bilibili、WeTV）
  - 隐私与安全 145 条（微信、支付宝、百度网盘）
  - 意图确认 571 条（TikTok、小红书、淘宝）
  - 组合类 80 条（WeTV、爱奇艺、优酷）
  - 其他类 127 条（小红书、淘宝、微博）
- **评测环境**：Android Studio 模拟器 + 两台真实 Android 手机，支持动态逐步交互（区别于静态截屏评测），部分测试场景设计了特殊环境设置（如未登录状态、权限禁用、App 放在深层文件夹中）以触发询问场景。

### 3.2 评测指标

1. **任务成功率（SR）**：任务是否成功完成；
2. **询问成功率（ISR）**：在恰当的时机是否正确地向用户发出询问；
3. **任务完成分数（Score）**：由 GPT-4o 根据轨迹质量评分的 0–4 分制。

### 3.3 对比基线

- **框架类基线**：AppAgent、Mobile-Agent-E（各配多种底层模型）；
- **模型类基线**：Qwen2.5-VL-3B、UI-R1-3B、UI-R1-3B-E、GUI-R1-3B、GUI-Owl；
- **大型闭源模型**：GPT-4o、Gemini-2.5-pro、Claude-3.5-Sonnet v2。

### 3.4 额外实验

- **通用 GUI 执行能力评估**：在 Android Control 和 GUI-Odyssey 两个通用 GUI 基准上进行测试；
- **人类满意度调查**：招募约 200 名参与者，从车站、学校、商场等多个公共场所，对系统进行 0–5 分满意度评分。

## 4. 资源与算力

- 文中明确说明：以 **Qwen2.5-VL-3B** 为基座模型，在 **4 块 H100 GPU** 上完成两阶段训练；
- Stage 1：SFT 2 个 epoch（LoRA rank=8，学习率 1.0×10⁻⁴）；
- Stage 2：GRPO 2 个 epoch（每个样本 4 条生成，温度 1，最大步数 15）；
- 论文**未说明**具体训练时长、总 GPU 小时数或推理阶段的算力消耗，仅提供了 GPU 型号与数量层面的信息。

## 5. 实验数量与充分性

### 5.1 实验组数

论文包含以下实验：
- **主实验**：在 InquireBench 上的中英文双场景评测，对比 10 余种基线模型组合（约 15 个配置）；
- **消融分析**：对比 Stage 1 单独训练、Stage 2 单独训练、Stage 1 + Stage 2 组合的效果；
- **泛化性实验**：Android Control（2 组指标 × 4 个模型对比）和 GUI-Odyssey（TM/EM 指标 × 4 个模型对比）；
- **人类满意度实验**：约 200 名参与者评价 7 种模型配置的中英文满意度；
- **定性可视化**：随机选取若干案例进行轨迹对比分析。

### 5.2 实验充分性与客观性评价

- **充分性**：实验覆盖了不同模型规模（3B vs 7B）、不同训练范式（纯 SFT、纯 RL、两阶段）、不同评测场景（中英文、模拟器/真机）以及多维度指标（ISR/SR/Score/人工满意度），总体比较充分；
- **客观性**：与基线对比时采用了统一的评测环境和度量方式，使用 GPT-4o 作为自动评分器（但 GPT-4o 也参与了数据生成，存在一定潜在偏差）；
- **公平性**：基线涵盖了开源和闭源模型、框架型和模型型方法，对比面较广；部分基线声称“无法启用询问能力”，因此 ISR 标记为不可用，属于合理设定；
- **不足**：训练和测试数据均源于同一数据收集流程（随机游走 + 人工标注），可能存在数据分布偏差；且论文未报告标准差或多次运行结果，统计显著性未验证。

## 6. 论文的主要结论与发现

1. **现有智能体在询问能力上近乎为零**：所有基线方法在 InquireBench 上的 ISR 均极低（最佳也仅约 5.8%），充分验证了“主动求助”能力在现有 VLM 移动智能体中的严重缺失；
2. **InquireMobile 显著提升询问成功率**：在 InquireBench 上达到 **52.6% 的 ISR**，比最佳基线高出 **46.8 个百分点**；
3. **两阶段训练互补效应显著**：
   - 仅 SFT（Stage 1）的模型 ISR 较高（27.9%）但 SR 极低（2.15%），原因在于“过度询问”——在不需要确认的场景中也频繁打扰用户；
   - 仅 GRPO（Stage 2）模型 ISR 仅 5.3%；
   - 两阶段联合训练在保持较高 ISR 的同时实现了更好的任务成功率（SR 7.9%）和轨迹得分（0.78），说明 Stage 2 有效遏制了不必要的询问；
4. **引入询问行为不损害通用 GUI 能力**：在 Android Control 上优于多个 7B 规模模型，在 GUI-Odyssey 上也保持强竞争力，说明询问能力的加入未对基本操作能力造成负面影响；
5. **人类满意度最高**：InquireMobile（两阶段）是唯一满意度超过 2 分（满分 5 分）的模型（2.25/5）；
6. **定性分析**：面对模糊指令时，Qwen2.5-VL-3B 会陷入停滞并反复输出无用信息，而 InquireMobile 能通过主动澄清意图继续完成任务。

## 7. 优点：方法与实验设计的亮点

- **问题选择具有前瞻性与实际价值**：首次系统性地将“智能体主动求助用户”作为核心研究课题，直接回应移动智能体安全部署中的关键痛点；
- **创新的数据收集策略**：采用“反向工作流”（先随机游走收集真实截图，再标注任务与询问场景），避免了传统方法中主观构造交互步骤的偏差，更贴近真实使用；
- **两次审校机制（human-in-the-loop）**：所有标注数据经过人工审核，且 GPT-4o 生成的思想链内容也由标注者保留/编辑/重写，提高了数据质量；
- **中英双语评测覆盖**：考虑到中英文 App 类别和使用模式的差异，分别设置语言环境进行数据采集和评测，增强了基准的覆盖面；
- **两阶段训练策略设计巧妙**：通过实验清晰证明 SFT 与 RL 各自的作用与互补性，为“安全交互”类智能体训练提供了可复制的范式；
- **评估维度全面**：不仅关注任务成功率，还设计了专门的 ISR 指标、GPT-4o 轨迹评分、人类满意度调查以及通用 GUI 基准泛化测试；
- **奖励函数设计简洁有效**：采用规则驱动的格式/类型/参数三级奖励，无需训练额外的价值网络，降低了训练复杂度；
- **对失败案例的归因分析深入**：明确指出 grounding、App 级先验知识、页面理解三个主要失败原因，为后续研究指明方向。

## 8. 不足与局限

- **视觉定位误差**：模型在将文本指令与屏幕上精确触摸目标对齐时仍易出错，对布局变化、缩放、弹窗/横幅等瞬态叠加层敏感；多语言文本、低对比度元素和 OCR 噪声也会降低定位可靠性，导致误触或漏点，可能打断长任务链；
- **动作效率低**：感知–推理–行动循环涉及繁重的视觉解析、模型推理和设备交互，延迟较高；面对动态 UI 或意外应用状态时，模型经常回溯和探索非最优分支，步骤数和完成时间均高于人工操作；
- **任务成功率仍然偏低**：尽管 ISR 大幅提升，总体 SR 仅 7.9%，说明模型在真实复杂环境中的端到端任务执行能力依然薄弱，离实用部署还有明显差距；
- **评测规模有限**：InquireBench 标注数据量仅 975 条，测试任务仅 190 条（中英各 95 条），规模有限；
- **可能存在的偏差**：
  - GPT-4o 既参与训练数据生成，又作为评测打分的裁判模型，存在潜在的利益冲突或同源偏差；
  - 训练与测试数据来自同一收集流程，可能存在分布重叠；
  - “随机游走”采样可能无法覆盖某些低频但在实际中重要的询问场景；
- **统计严谨性不足**：未报告多次实验的标准差或显著性检验结果，对于训练中的随机性鲁棒性缺乏证据支撑；
- **人工满意度调查仅报告平均分**，未提供样本数、置信区间或细粒度分析等附加信息；
- **训练算力与可扩展性**：论文未提供详细的训练时长与成本信息，也未验证方法在更大模型（如 7B/72B）上的推广效果。

（完）
