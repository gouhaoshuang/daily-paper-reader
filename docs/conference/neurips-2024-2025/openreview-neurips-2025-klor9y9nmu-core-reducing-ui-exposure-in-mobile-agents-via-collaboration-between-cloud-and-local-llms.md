---
title: "CORE: Reducing UI Exposure in Mobile Agents via Collaboration Between Cloud and Local LLMs"
title_zh: CORE：通过云端与本地LLM协作减少移动代理的UI暴露
authors: "Gucongcong Fan, Chaoyue Niu, chengfei lv, Fan Wu, Guihai Chen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=klOr9y9nMU"
tags: ["query:eca"]
score: 9.0
evidence: 移动代理中云端与本地LLM协作
tldr: 移动代理在执行任务时需上传完整UI状态至云端，存在隐私泄露风险。本文提出CORE框架，通过云端与本地LLM的协同工作，在保证任务准确率的同时大幅减少UI暴露。CORE包含布局感知块划分、本地过滤等组件，实验表明其有效平衡了隐私与性能。该工作为端云协同的移动智能体提供了重要范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1338, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1456, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1439, \"height\": 355, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1334, \"height\": 623, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1151, \"height\": 1156, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1019, \"height\": 1056, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1027, \"height\": 1082, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1018, \"height\": 1074, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-klor9y9nmu/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1025, \"height\": 1084, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1440, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1357, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1370, \"height\": 977, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1364, \"height\": 2339, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1364, \"height\": 2338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1365, \"height\": 421, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1364, \"height\": 1771, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1363, \"height\": 2333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1370, \"height\": 539, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1428, \"height\": 189, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1427, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1442, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1431, \"height\": 129, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1438, \"height\": 135, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1447, \"height\": 162, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1444, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1367, \"height\": 654, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1363, \"height\": 2333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1368, \"height\": 461, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1150, \"height\": 177, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-klor9y9nmu/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1224, \"height\": 173, \"label\": \"Table\"}]"
motivation: 移动代理依赖云端LLM处理UI，但上传完整UI状态存在隐私泄露和冗余问题；本地LLM能力有限导致任务成功率低。
method: 提出CORE框架，包含布局感知块划分、本地LLM过滤及云端LLM补全，实现云端与本地协同决策。
result: "在多个移动任务基准上，CORE在保持高任务准确率的同时，将UI暴露量降低至原来的20%以下。"
conclusion: CORE证明了云端与本地LLM协作可有效减少移动代理的隐私风险，为端云协同智能体设计提供了新思路。
---

## Abstract
Mobile agents rely on Large Language Models (LLMs) to plan and execute tasks on smartphone user interfaces (UIs). While cloud-based LLMs achieve high task accuracy, they require uploading the full UI state at every step, exposing unnecessary and often irrelevant information. In contrast, local LLMs avoid UI uploads but suffer from limited capacity, resulting in lower task success rates. We propose $\textbf{CORE}$, a $\textbf{CO}$llaborative framework that combines the strengths of cloud and local LLMs to $\textbf{R}$educe UI $\textbf{E}$xposure, while maintaining task accuracy for mobile agents. CORE comprises three key components: (1) $\textbf{Layout-aware block partitioning}$, which groups semantically related UI elements based on the XML screen hierarchy; (2) $\textbf{Co-planning}$, where local and cloud LLMs collaboratively identify the current sub-task; and (3) $\textbf{Co-decision-making}$, where the local LLM ranks relevant UI blocks, and the cloud LLM selects specific UI elements within the top-ranked block. CORE further introduces a multi-round accumulation mechanism to mitigate local misjudgment or limited context. Experiments across diverse mobile apps and tasks show that CORE reduces UI exposure by up to 55.6\% while maintaining task success rates slightly below cloud-only agents, effectively mitigating unnecessary privacy exposure to the cloud. The code is available at https://github.com/Entropy-Fighter/CORE.

---

## 论文详细总结（自动生成）

# CORE: Reducing UI Exposure in Mobile Agents via Collaboration Between Cloud and Local LLMs 中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **问题背景**：移动代理（Mobile Agent）依赖云端 LLM（如 GPT-4o）来自动执行智能手机上的任务。在每个决策步骤，代理需要将完整 UI 状态（包括所有 XML 元素）上传至云端，导致大量冗余甚至敏感信息被暴露。而仅使用本地 LLM（如 Gemma2-9B）虽能避免上传，但因模型容量有限，任务成功率显著低于云端方案。
- **核心目标**：提出一种在保持与云端 LLM 相近任务准确率的同时，大幅减少 UI 暴露（即仅上传最小必要 UI 内容到云端）的方法。
- **整体含义**：首次系统地研究移动代理中减少不必要 UI 暴露的问题，并通过云端与本地 LLM 的协作实现准确率与隐私保护的平衡。

## 2. 方法论：核心思想、关键技术细节与算法流程

### 核心思想
利用云端 LLM 的强大规划推理能力与本地 LLM 对完整 UI 的本地可访问性，构建不对称协作架构：本地 LLM 负责粗粒度过滤与候选生成，云端 LLM 负责细粒度确认与决策，从而仅传输少量关键 UI 块。

### 关键技术细节
- **布局感知块划分（Layout-aware Block Partitioning）**：
  - 基于 XML 树结构，通过深度优先遍历提取重要 UI 元素（可点击、含语义、可编辑等）。
  - 记录每个重要元素的祖先路径（ancestor path），按不同深度层级将共享相同祖先的元素分组为语义连贯的块。
  - 选择第一个能产生至少 3 个块的深度层级作为最终划分结果。
- **协同规划（Co-planning）**：
  - 本地 LLM 对每个 UI 块独立生成候选子任务（block-level sub-task）。
  - 所有候选子任务发送给云端 LLM，云端 LLM 综合分析后选择或修正最合适的子任务，作为当前步骤的目标。
- **协同决策（Co-decision-making）**：
  - 本地 LLM 根据确认的子任务，对各 UI 块进行重要性打分（归一化为概率，和为 1），并将得分最高的块上传至云端。
  - 云端 LLM 基于该块进行元素级决策（选择具体 UI 元素和动作类型）。
  - **多轮累积机制**：若云端 LLM 认为当前块信息不足，则请求本地 LLM 按分数顺序发送下一个块，云端逐步累积信息直至能做出可靠决策。

### 算法流程（Algorithm 1）
1. 对每个 UI 块，本地 LLM 生成子任务候选，加入集合 S。
2. 云端 LLM 从 S 中确认最佳子任务 s*。
3. 本地 LLM 根据 s* 对所有块排序，得 Branked。
4. 按 Branked 顺序依次将块加入累积集合 C，每次由云端 LLM 尝试做出决策 (动作, 元素)；若决策非 None 则返回，否则继续累积。
5. 若最终无法决策则返回 None（后续可能触发滚动等处理）。

## 3. 实验设计

### 数据集
- **DroidTask**：158 任务（过滤后 143 任务，12 个 App），如 Calendar、Clock、Contacts 等。
- **AndroidLab**：98 操作任务，9 个 App，如 Maps、Music、Zoom，UI 更复杂。
- **额外验证集**（附录）：LlamaTouch 的社交 App 子集（64 任务，Instagram、Pinterest、Reddit、X/Twitter）；AndroidWorld（116 任务）。

### 基准方法（baselines）
- **云端-only**：GPT-4o 全 UI 上传（任务准确率上界，UI 暴露上界）。
- **本地-only**：Gemma2-9B、Qwen2.5-7B、LLaMA3.1-8B 独立部署（UI 暴露下界，但成功率低）。
- **CORE 变体**：
  - 替换本地排序为固定顺序（基本顺序排名）、随机顺序排名；
  - 消融实验中去除自身模块（无块划分、无协同规划、无多轮交互、无累积机制）。

### 评估指标
- **任务成功率**：按对应数据集的官方准则判断。
- **UI 减少率**：与 GPT-4o 基线相比，仅统计相同决策轮次的元素数量减少百分比。
- **敏感 UI 元素减少率**：由 Qwen2.5-Max 分类敏感类型（身份、位置、联系人等）。
- **延迟与 token 用量**：分别统计本地和云端推理时间，以及 GPT-4o 的 API token 消耗。

## 4. 资源与算力

- **本地 LLM 部署**：使用量化版本（Gemma2-9B Q5_K_M、Qwen2.5-7B Q6_K_L、LLaMA3.1-8B Q6_K），每个模型约 6.5 GB 磁盘空间。推理在 **NVIDIA GeForce RTX 4090D**（消费级 GPU）上运行，利用 **Ollama** 框架。
- **云端 LLM**：GPT-4o-2024-11-20，通过 OpenAI 官方 API 调用。
- **实验执行环境**：DroidTask 使用荣耀 Play3 真实手机（Android 9）；AndroidLab 使用官方 Pixel 7 Pro 模拟器（Android 13）。UI 提取通过 uiautomator2，动作执行通过 ADB。
- **训练时长**：论文未提及训练过程（方法为训练无关的 prompt-based），仅给出推理延迟对比（见表 11：本地 LLM 在 4090D 上平均每任务 32.12s，云端 GPT-4o 29.15s，总延迟为基线的 1.52×；若部署在手机 Xiaomi 15 Pro 则总延迟达 170.19s，为基线的 4.22×）。

## 5. 实验数量与充分性

- **主要对比实验**：表 1 展示了 3 种云-本组合（GPT-4o + Gemma2-9B/ Qwen2.5-7B/ LLaMA3.1-8B）在 DroidTask 和 AndroidLab 上的成功率与 UI 减少率，共 6 个主要配置。
- **敏感 UI 分析**：表 2 细粒度统计了 8 类敏感元素上传数量对比。
- **延迟与 token 分析**：图 4 柱状图显示各方法的延迟和 token 用量。
- **逐 App 表现**：图 5 对两个数据集的每个 App 分别给出成功率和减少率，共 21 个 App 子图。
- **消融实验**：表 3 在 DroidTask 上对块划分、协同规划、多轮交互、累积机制、排序策略进行消融，共 6 组变体。
- **限制块数量的实验**（附录 D）：比较限制最多 3 块与原始版本在成功率和资源消耗上的差异。
- **多模态扩展实验**（附录 H）：在 DroidTask 和 AndroidLab 上测试截图+掩码模式的多模态 CORE。
- **额外数据集**（附录 I）：在 LlamaTouch（64 任务）和 AndroidWorld（116 任务）上验证。

**充分性评价**：实验覆盖了多种本地模型、两个主要基准数据集、补充数据集、消融、超参数影响（块数限制）、多模态扩展等，对比基线合理，结果统计充分。但缺少多次运行的标准差/误差条（因 API 调用成本高），是常见折衷。整体实验设计客观公平。

## 6. 主要结论与发现

- **主要结果**：
  - DroidTask 上，CORE (GPT-4o + Gemma2-9B) 实现 **55.6% UI 减少**，成功率 69.23%，仅比 GPT-4o 基线低 4.9%。
  - AndroidLab 上，CORE (GPT-4o + Qwen2.5-7B) 实现 **29.97% UI 减少**，成功率 41.84%，仅低 3.06%。
  - 敏感 UI 元素上传减少 70.49%（DroidTask）和 38.84%（AndroidLab）。
- **协同有效性**：即使使用较弱的本地模型（如 LLaMA3.1-8B），CORE 的成功率也显著优于本地-only 基线（+39.86% 及 +23.47%），证明协作框架有效。
- **消融重要性**：去除协同规划或多轮累积导致成功率大幅下降（-9.79% 和 -32.87%），说明各模块不可或缺。
- **延迟与 token 成本**：总延迟约为 GPT-4o 基线的 1.5-1.66 倍，云端 token 用量略增（1.1×）或持平（0.94-1.01×），代价可控。
- **模态无关性**：CORE 可扩展到截图+掩码的多模态输入，性能与 XML 版本相当。

## 7. 优点（方法与实验设计亮点）

1. **问题新颖**：首次聚焦移动代理中 UI 暴露的隐私问题，并给出系统解决方案。
2. **协作架构巧妙**：利用本地 LLM 的完整可视性与云端 LLM 的强大推理，形成“本地粗筛 + 云端精审”的非对称协作，无需训练即可落地。
3. **布局感知块划分**：保留 XML 树结构语义，划分更符合 UI 设计逻辑，提升过滤效果。
4. **多轮累积机制**：动态决定所需信息量，兼具信息充分性与最小暴露，对本地错误具有容错性。
5. **实验全面**：覆盖两个主流数据集、三类本地模型、消融、限制条件、多模态扩展、额外数据集，结果一致验证方法有效性。
6. **隐私量化细致**：不仅统计总体 UI 元素减少，还逐类分析敏感信息暴露减少，使隐私收益具体可感。

## 8. 不足与局限

1. **延迟增加**：由于本地额外推理，整体延迟约为云端基线的 1.5-1.66 倍，在移动设备全本地部署时（如 MNN 推理）延迟更高（4.22×），可能影响实时体验。
2. **云端 token 可能增加**：在 DroidTask 上 CORE 的云端 token 用量高于基线（1.1×），因多轮交互和候选生成带来额外开销。
3. **对本地模型能力敏感**：更弱的本地模型（如 LLaMA3.1-8B）导致成功率和减少率均下降，表明框架上限受本地模型质量制约。
4. **依赖 XML 结构**：若 UI 元素缺乏分层或 XML 结构混乱（如某些复杂 App），块划分效果可能下降，从而影响过滤效率。
5. **未考察安全/对抗场景**：未分析恶意应用通过 UI 诱导泄露敏感信息的可能性，也没有健壮性测试。
6. **统计不确定性未报告**：缺乏多次重复实验的误差条，无法评估结果的波动范围（虽因 API 成本合理）。
7. **任务范围限制**：仅覆盖菜单、表单、导航等操作任务，未涵盖需全面理解页面（如购物对比、多步推理）的复杂场景，此类场景下局部 UI 可能不足。

（完）
