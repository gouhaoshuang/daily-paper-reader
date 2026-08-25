---
title: Experience-driven Multi-turn Reinforcement Learning for GUI Agents
title_zh: 面向GUI智能体的经验驱动多轮强化学习
authors: "Zhengxi Lu, Jiabo Ye, Fei Tang, Yongliang Shen, Haiyang Xu, Ziwei Zheng, Weiming Lu, Ming Yan, Fei Huang, Jun Xiao, Yueting Zhuang"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.428.pdf"
tags: ["query:mobile-agent"]
score: 7.0
evidence: 面向GUI智能体的经验驱动多轮强化学习，可迁移至移动端智能体训练
tldr: 针对单轮强化学习训练与部署分布不一致以及在线多轮方法成本高的问题，提出经验驱动多轮策略优化（EMPO），利用专家轨迹作为环境经验进行on-policy多轮训练，智能体在rollout中构建自生成历史，并在动作匹配时获得反馈。既避免了分布偏移，又缓解了奖励稀疏和成本问题，为长程GUI智能体训练提供了高效方案。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 801, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1653, \"height\": 1051, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 798, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1640, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1655, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1654, \"height\": 1422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1633, \"height\": 265, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1647, \"height\": 190, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 697, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 700, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 760, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 742, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 655, \"height\": 759, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 768, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1651, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1661, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1656, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1660, \"height\": 266, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1662, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1007, \"height\": 1006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long428/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1663, \"height\": 409, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1646, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1660, \"height\": 1057, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 797, \"height\": 856, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 793, \"height\": 892, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 716, \"height\": 428, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 797, \"height\": 622, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 772, \"height\": 1509, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 787, \"height\": 776, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 785, \"height\": 964, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 677, \"height\": 847, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 504, \"height\": 789, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 496, \"height\": 786, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 508, \"height\": 790, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 696, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 668, \"height\": 735, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 797, \"height\": 958, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long428/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 792, \"height\": 569, \"label\": \"Table\"}]"
motivation: 单轮强化学习存在训练与部署历史分布不一致，多轮在线方法成本高且奖励稀疏。
method: 提出利用专家轨迹作为环境经验的多轮策略优化算法EMPO。
result: 在长程GUI任务上提升了策略性能，并降低了训练成本。
conclusion: 为GUI智能体的长程多轮训练提供了一种实用的强化学习范式。
---

## Abstract
GUI agents have demonstrated remarkable progress in automating complex user interface interactions. However, training such agents for long-horizon tasks remains challenging. Single-turn reinforcement learning conditions on expert histories during training but self-generated histories during deployment, causing distribution mismatch. Online multi-turn methods eliminate this gap via environment interaction but suffer from sparse rewards and prohibitive costs. We propose ̲ E xperience-driven ̲ M ulti-turn ̲ P olicy ̲ O ptimization ( EMPO ), which leverages expert trajectories as environment experiences for on-policy multi-turn training. The agent constructs self-generated history throughout rollouts; when actions match expert experiences, the trajectory provides valid state transitions, and a Patch Module recovers mismatched steps to maintain on-policy rollouts. EMPO further incorporates discounted future rewards and dual-level advantage estimation to capture long-horizon dependencies. We also propose AndroidControl-Real , an evaluation metric strongly correlated with real-world performance (R 2 =0.934). With only 1K public trajectories as RL experiences, our method achieves substantial gains over the base model (e.g., +12.0% on AndroidWorld and +23.8% on AITW) and achieves competitive performance against strong baselines such as UI-TARS-7B and GPT-4o, demonstrating better generalization than prior single-turn RL approaches. Code available: https://anonymous.4open.science/r/UI-S1-0DAF .

---

## 论文详细总结（自动生成）

### 1. 核心问题与研究动机

GUI智能体在自动化复杂用户界面交互方面已取得显著进展，但**长程（long-horizon）任务的训练仍然极具挑战**。论文指出现有训练范式存在两类核心矛盾：

- **单轮强化学习（Single-turn RL）的分布偏移问题**：训练时基于专家历史（expert histories）进行条件化，而部署时却依赖智能体自生成的历史（self-generated histories），导致训练与部署之间的历史分布不一致，损害策略泛化能力。
- **在线多轮强化学习（Online Multi-turn RL）的成本与稀疏奖励问题**：虽然通过与真实环境交互消除了分布偏移，但长程任务中的奖励极其稀疏，且与环境交互的代价高昂，难以规模化应用。

因此，论文的核心目标是提出一种**兼顾分布一致性、奖励信号密集性、训练成本可控性**的多轮强化学习训练范式。

### 2. 方法论：EMPO（Experience-driven Multi-turn Policy Optimization）

#### 核心思想
将**专家轨迹（expert trajectories）作为“环境经验”**注入到on-policy多轮训练流程中。智能体在rollout过程中逐步构建自生成历史，通过将自身动作与专家经验进行匹配来获得有效的状态转移和密集反馈信号，从而在不依赖真实环境交互的前提下，实现训练与部署的历史分布一致性。

#### 关键技术细节
- **自生成历史构建**：在训练rollout中，智能体不直接使用专家历史，而是持续基于自身策略生成动作并累积历史轨迹，模拟部署时的真实推理过程。
- **动作匹配与状态转移**：当智能体的动作与专家轨迹中的某一步匹配时，该轨迹段被视为有效的“环境经验”，提供合法的下一状态与奖励信号。
- **Patch Module（补丁模块）**：当智能体动作与专家经验不匹配时，Patch Module负责修复这些失配步骤，使rollout能够从错误中恢复，从而**维持on-policy rollouts的连续性**，避免因单步偏差导致整条轨迹失效。
- **折扣未来奖励（Discounted Future Rewards）**：引入折扣因子，将未来多步的奖励信号折算到当前步，以缓解长程任务的奖励稀疏问题。
- **双层优势估计（Dual-level Advantage Estimation）**：在多个粒度（如动作级与轨迹级）上估计优势函数，更好地捕捉长程任务中的时序依赖与决策价值差异。

### 3. 实验设计

#### 数据集与Benchmark
- **训练数据**：仅使用 **1K 条公开的专家轨迹（public trajectories）** 作为RL经验，数据成本极低。
- **评估基准**：
  - **AndroidWorld**：真实安卓环境下的长程GUI任务基准，用于检验智能体在真实世界环境中的性能。
  - **AITW（Android in the Wild）**：大规模真实人类操作数据集基准，用于评估跨任务泛化能力。
  - 自定义评估指标 **AndroidControl-Real**：一种与真实世界性能强相关（R²=0.934）的新评估指标，旨在弥补现有离线指标与真实部署表现之间的差距。

#### 对比基线
- **基础模型（Base Model）**：EMPO的初始策略模型，用于衡量提升幅度。
- **强基线**：
  - **UI-TARS-7B**：基于视觉语言模型的GUI智能体。
  - **GPT-4o**：通用大模型作为GUI操作智能体。
  - 先前的工作，特别是**单轮RL方法**，用于对比训练范式的优劣。

### 4. 资源与算力

论文摘要及所提供内容中**未明确提及具体GPU型号、数量及训练时长**。仅能从上下文推断：该方法仅需1K条专家轨迹即可完成训练，暗示其训练成本显著低于依赖海量环境交互的在线多轮RL方法，但具体硬件配置与时间开销在提供的文本中未做披露。

### 5. 实验数量与充分性

- **实验组数**：论文包含了多个数据集上的主实验（AndroidWorld、AITW）、新评估指标（AndroidControl-Real）的验证实验、以及与多个强基线的对比实验。此外，方法设计中包含若干关键模块（Patch Module、双层优势估计等），在完整论文中大概率配有对应消融实验。
- **充分性评估**：
  - **正面**：覆盖了从真实环境（AndroidWorld）到大规模离线数据集（AITW）的评估，兼顾性能与泛化性；引入与真实表现强相关的指标，提升了评估结果的可信度。
  - **潜在问题**：实验验证主要局限于**安卓移动端GUI领域**，对PC桌面端、Web端等更广泛的GUI环境未在摘要中提及；对比的强基线虽有代表性，但数量有限，是否涵盖最新的同类型方法（如其他多轮RL方案）尚不明确。

### 6. 主要结论与发现

- EMPO在**长程GUI任务上显著提升策略性能**：相比基础模型，在AndroidWorld上提升 **+12.0%**，在AITW上提升 **+23.8%**。
- 仅使用 **1K条专家轨迹**即达到与 **UI-TARS-7B** 和 **GPT-4o** 等强基线竞争力的性能水平。
- EMPO相比先前的单轮RL方法，**展现出更好的泛化能力**，验证了“经验驱动的多轮训练”范式的有效性。
- 提出的 **AndroidControl-Real** 指标与真实世界性能高度相关（R²=0.934），可作为评估GUI智能体离线性能的可靠参考。

### 7. 方法亮点与优点

- **训练/部署分布一致性**：通过自生成历史与专家经验匹配，有效化解了单轮RL分布偏移的顽疾。
- **高成本效益**：利用专家轨迹替代真实环境交互，大幅降低训练成本，仅需1K轨迹即可高效训练。
- **流程完整性保障**：Patch Module的设计巧妙处理了动作失配情况，保证了on-policy训练的稳定性和数据有效性。
- **有效应对长程稀疏奖励**：折扣未来奖励 + 双层优势估计，针对性提升了长程任务的学习效率。
- **评估指标创新**：提出并验证了AndroidControl-Real指标，为GUI智能体领域的评估提供了更具现实意义的参考标准。

### 8. 不足与局限

- **领域覆盖有限**：实验主要聚焦于移动端（安卓）GUI环境，未展示在桌面端、Web端或跨平台GUI任务上的有效性，其泛化性仍待验证。
- **算力信息不透明**：论文未披露详细的硬件配置与训练时长，外部研究者难以准确评估方法的实际训练门槛。
- **对专家轨迹质量的依赖**：方法高度依赖专家轨迹作为环境经验，若专家轨迹质量不佳或覆盖不足，可能影响匹配有效性进而限制策略上限。
- **指标适用性未知**：AndroidControl-Real虽与真实软件环境（AndroidWorld）有强相关，但它对硬件/平台环境的依赖程度，以及在更广泛真实场景中的普适性仍有待检验。
- **奖励信号仍存在简化假设**：基于动作匹配的奖励虽然缓解了稀疏性问题，但“动作匹配”并不完全等于“任务成功”，可能存在奖励噪声。

（完）
