---
title: "Mobile-R1: Towards Interactive Capability for VLM-Based Mobile Agent via Systematic Training"
title_zh: Mobile-R1：通过系统化训练提升基于VLM的移动智能体交互能力
authors: "Jihao Gu, Qihang Ai, Yingyao Wang, Pi Bu, Jingxuan Xing, Yue Cao, Zekun Zhu, Wei Jiang, Ziming Wang, Yingxiu Zhao, Ming-Liang Zhang, Jun Song, Yuning Jiang, Bo Zheng"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.1422.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 面向VLM移动智能体的系统化训练方法，提升交互式任务执行能力
tldr: 现有VLM移动智能体训练多采用离线或在局部动作层面奖励，易陷入局部最优，难以有效探索与纠正错误。Mobile-R1提出一种系统化训练方案，采用层次化机制连接原子动作执行与策略性任务完成，解决直接使用任务级奖励导致的收敛困难。该方法提升了智能体在复杂GUI交互中的探索和纠错能力，为移动智能体训练提供了新思路。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1659, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 804, \"height\": 768, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 792, \"height\": 469, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1657, \"height\": 765, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1656, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 764, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1651, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 751, \"height\": 282, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 777, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 762, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 753, \"height\": 447, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1410, \"height\": 889, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1422/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1657, \"height\": 663, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1412, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 789, \"height\": 151, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 792, \"height\": 474, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1650, \"height\": 514, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1634, \"height\": 481, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 752, \"height\": 1851, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1422/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 727, \"height\": 1849, \"label\": \"Table\"}]"
motivation: 现有训练方法令移动智能体陷入局部最优，难以进行环境探索与错误纠正。
method: 提出层次化训练方案，桥接原子动作执行与策略性任务完成，改进奖励设计。
result: 有效缓解了稀疏奖励下的收敛难题，增强了智能体的交互能力。
conclusion: 为VLM移动智能体的系统化训练提供了可行范式。
---

## Abstract
Vision-language model-based mobile agents have gained the ability to understand complex instructions and mobile screenshots, benefiting from reinforcement learning paradigms like Group Relative Policy Optimization (GRPO). However, existing approaches centers on offline training or local action-level rewards often trap agents in local optima, hindering effective exploration and error correction with the environment. Crucially, we find that directly applying task-level rewards often leads to convergence difficulties due to the sparse nature of GUI interactions. To address these challenges, we present Mobile-R1 , a systematic training recipe that bridges atomic action execution and strategic task completion. We propose a hierarchical curriculum consisting of three stages: (1) format alignment for reasoning structure, (2) on-policy exploration with verifiable action feedback to ground basic execution, and (3) multi-turn task-level training with realistic environment to unlock exploration and self-correction. This hierarchical strategy effectively bootstraps the agent, significantly enhancing its capability for exploration and self-correction (the “Eureka” moments). Furthermore, addressing the critical scarcity of diverse GUI data in non-English ecosystems, we contribute a comprehensive Chinese mobile dataset covering 28 applications with 24,521 high-quality manual annotations, and establish a rigorous benchmark with 500 trajectories. We will open source all resources, including the dataset, benchmark, model weight, and codes: https://mobile-r1.github.io/Mobile-R1/ .

---

## 论文详细总结（自动生成）

## 论文总结：Mobile-R1（ACL 2026 Long Paper）

### 1. 论文的核心问题与整体含义

该论文聚焦于**基于视觉语言模型（VLM）的移动智能体**训练中存在的关键瓶颈。现有训练方法大多采用以下两种方式，且都存在明显缺陷：
- **离线训练**：智能体只能模仿静态轨迹，缺乏与真实环境的动态交互能力；
- **局部动作级奖励**：仅优化单个步骤的正确性，容易让智能体陷入**局部最优解**，导致其无法进行多步策略规划，也缺乏在 GUI 环境中主动探索和自我纠错的能力。

作者进一步发现，如果为了克服上述问题而直接引入**任务级奖励**，又会因为 GUI 交互中奖励的**稀疏性**而引发训练收敛困难。

该论文的核心含义在于：提出了一套**系统化的三阶段层次化训练方案**（Mobile-R1），将"原子动作执行"（点击、滑动等单步操作）与"策略性任务完成"（多步推理与规划）有机衔接，有效解决了上述训练难题，显著提升了 VLM 移动智能体的交互能力。

### 2. 论文提出的方法论

**核心思想**：通过**层次化课程学习（Hierarchical Curriculum）**，自底向上、循序渐进地对智能体进行训练，避免直接使用任务级奖励带来的稀疏奖励收敛问题。

**三阶段训练流程**（文字说明）：
1. **阶段一：格式对齐（Format Alignment）**
   - 目标：让模型学会输出符合要求的**推理结构**（reasoning structure），为后续强化学习打下稳定的输出格式基础。
2. **阶段二：在线策略探索（On-policy Exploration with Verifiable Action Feedback）**
   - 目标：利用**可验证的动作级反馈**（verifiable action feedback），在真实环境中进行在线策略探索，将模型的动作生成基础能力（如坐标点击、动作序列）扎实落地。
3. **阶段三：多轮任务级训练（Multi-turn Task-level Training）**
   - 目标：在**真实环境的模拟器**中，进行多轮任务级强化学习训练。此阶段解锁了智能体的**主动探索（exploration）**和**自我纠错（self-correction）**能力，即论文所称的"Eureka"时刻。

**关键机制**：层次化训练有效桥接了"原子动作执行"与"策略性任务完成"之间的鸿沟。在训练范式上沿用 GRPO（Group Relative Policy Optimization）等强化学习策略，但通过分阶段设计规避了稀疏奖励导致的收敛风险。

### 3. 实验设计

- **数据集**：论文构建了**中文移动智能体数据集**，覆盖 **28 个应用（App）**，包含 **24,521 条高质量人工标注数据**（解决非英语生态系统中 GUI 数据稀缺的问题）。
- **Benchmark**：建立了**包含 500 条任务轨迹**的严格评测基准。
- **对比方法**：与现有 VLM 移动智能体训练方案（包括离线训练方法、局部动作级奖励方法等）进行对比，以验证 Mobile-R1 在任务完成率、探索能力、纠错能力等指标上的优势。
- **实验内容**：除主实验外，论文包含消融实验（对应 7 张表格），验证了各训练阶段、奖励设置的有效性。

### 4. 资源与算力

**论文摘要和元数据中未明确说明**使用的 GPU 型号、GPU 数量、训练时长等算力细节。用户若需了解算力需求，需查阅论文原文的实验设置部分，当前提供的材料中未包含此类信息。

### 5. 实验数量与充分性

- **实验数量**：从表格数量（7 张表）和图像数量（13 张图）判断，实验覆盖了主实验、多组对比实验、消融实验以及案例分析，实验量较为丰富。
- **充分性评估**：论文包含：
  - 三阶段训练策略的消融验证；
  - 中文挑战性基准的构建与评测；
  - 与传统离线/局部奖励方法的对比。
- 由于摘要和元数据中未提供具体数值（如任务成功率、提升幅度等），无法从当前材料中定量评估实验的公平性和显著性。但从方法论设计上看，对比实验和消融实验结构较为完整。

### 6. 论文的主要结论与发现

1. 现有 VLM 移动智能体训练方法（离线训练、局部动作奖励）会使智能体陷入**局部最优**，阻碍探索与纠错能力。
2. 直接使用任务级奖励会因 GUI 环境中奖励**过于稀疏**而导致训练收敛困难。
3. Mobile-R1 提出的**三阶段层次化训练方案**有效缓解了稀疏奖励下的收敛难题，成功增强了智能体的**探索与自我纠错能力**。
4. 论文为 VLM 移动智能体的**系统化训练**提供了新的可行范式，并开源了数据集、基准、模型权重和代码。

### 7. 优点

- **方法论创新性强**：提出"原子动作执行 → 策略性任务完成"的层次化训练桥接机制，设计合理，有效规避了稀疏奖励陷阱。
- **具备可复现性和开源精神**：数据集、benchmark、模型权重和代码将全部开源，具有较高的研究价值。
- **填补非英语界面数据空白**：贡献了高质量、大规模的中文移动端 GUI 数据集（28 应用、24.5K+ 标注），对 VLM 智能体的多语言应用具有重要意义。
- **问题切中要点**：精准指出了 GUI 环境中"稀疏奖励"这一被忽视的难点，为后续研究提供了明确方向。

### 8. 不足与局限

- **资源细节缺失**：当前材料未提供算力信息（GPU 型号/数量/时长），难以评估其复现成本。
- **定量结果未在摘要中体现**：论文摘要未给出具体的成功率提升数字，需要阅读原文表格以确认实验幅度。
- **区域覆盖受限**：数据集聚焦中文应用生态，虽然填补了空白，但英文及其他语言生态的泛化能力尚未验证。
- **GUI 应用覆盖范围**：覆盖 28 个应用虽已较广，但相比真实移动端用户所接触的海量应用仍有局限，benchmark 规模（500 条轨迹）也可能不足以完全反映真实世界的长尾任务分布。
- **强化学习训练稳定性**：三阶段训练虽然缓解了稀疏奖励问题，但多轮任务级训练的整体稳定性、超参数敏感性等仍需在更广泛的任务类型上进一步验证。

（完）
