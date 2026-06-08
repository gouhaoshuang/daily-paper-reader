---
title: "Shapley-Coop: Credit Assignment for Emergent Cooperation in Self-Interested LLM Agents"
title_zh: Shapley-Coop：自利LLM智能体中涌现合作的信用分配方法
authors: "Yun Hua, Haosheng Chen, Shiqin Wang, Wenhao Li, Xiangfeng Wang, Jun Luo"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=HnJ1UkuJXS"
tags: ["query:eca"]
score: 5.0
evidence: 自利LLM智能体中的涌现合作
tldr: 自利LLM智能体在开放环境中常因激励错位陷入社会困境，缺乏显式协调则难以合作。本文提出Shapley-Coop工作流，受人类社会临时合作启发，利用沙普利值进行信用分配，使自利智能体通过类似雇佣或分包的方式形成临时协作。实验证明该机制能有效提升集体收益，为多智能体协作中的激励设计提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1372, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1346, \"height\": 970, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 394, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 797, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1022, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 590, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hnj1ukujxs/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 598, \"height\": 532, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 758, \"height\": 142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 766, \"height\": 145, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1437, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1175, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1197, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1173, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1201, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1171, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1203, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1172, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1175, \"height\": 266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1168, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 890, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1438, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 822, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 900, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1150, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 940, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 928, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hnj1ukujxs/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 912, \"height\": 257, \"label\": \"Table\"}]"
motivation: 自利LLM智能体在无显式协调时面临社会困境，难以实现高效合作。
method: 基于沙普利值的信用分配工作流，促使智能体通过临时合作缓解利益冲突。
result: 在多个社会困境场景中，合作涌现，集体收益显著高于无协调基线。
conclusion: 信用分配机制是激发自利智能体合作的关键。
---

## Abstract
Large Language Models (LLMs) are increasingly deployed as autonomous agents in multi-agent systems, and promising coordination has been demonstrated in handling complex tasks under predefined roles and scripted workflows.
However, significant challenges remain in open-ended environments, where agents are inherently self-interested and explicit coordination guidelines are absent. 
In such scenarios, misaligned incentives frequently lead to social dilemmas and inefficient collective outcomes.
Inspired by how human societies tackle similar coordination challenges—through temporary collaborations like employment or subcontracting—a cooperative workflow \textbf{Shapley-Coop} is proposed. 
This workflow enables self-interested Large Language Model (LLM) agents to engage in emergent collaboration by using a fair credit allocation mechanism to ensure each agent’s contributions are appropriately recognized and rewarded.
Shapley-Coop introduces structured negotiation protocols and Shapley-inspired reasoning to estimate agents’ marginal contributions, thereby enabling effective task-time coordination and equitable post-task outcome redistribution. 
This results in effective coordination that fosters collaboration while preserving agent autonomy, through a rational pricing mechanism that encourages cooperative behavior.
Evaluated in two multi-agent games and a software engineering simulation, Shapley-Coop consistently enhances LLM agent collaboration and facilitates equitable outcome redistribution, accurately reflecting individual contributions during the task execution process.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：在开放、无显式协调规则的多智能体环境中，自利的 LLM 智能体倾向于追求自身局部奖励，导致社会困境（如囚徒困境）和次优的集体结果。现有方法（规则导向、角色导向、模型导向）多假设目标对齐，未能有效处理异构目标对齐和公平信用分配这一核心挑战。
- **整体含义**：受人类社会通过雇佣、分包等临时合作解决协调问题的启发，论文提出 **Shapley-Coop** 工作流，利用合作博弈论中的 **Shapley 值**进行公平的边际贡献评估，并通过结构化协商机制实现自利智能体之间的自发合作。这为多智能体 LLM 系统中的激励设计和协调提供了新范式。

## 2. 方法论：核心思想、关键技术细节与流程

- **核心思想**：将多智能体合作视为一种“定价”问题——通过任务时定价（task-time pricing）和事后奖励再分配（post-task reward redistribution），使自利智能体愿意为他人提供帮助或接受补偿，从而对齐异构目标。
- **关键技术细节**：
  - **结构化协商协议**：使用统一消息格式（如 `<s>I propose to {action}</s>`）促进智能体之间的可解释通信，包括意图通知、定价提议和结构化回应。
  - **短期 Shapley Chain-of-Thought (CoT)**：在任务执行阶段，智能体通过启发式推理定性评估自身行动的外部性（正/负外部性），决定是否需要提出或要求补偿（定价）。三个步骤：① 定性评估集体奖励；② 评估自身行动的外部性符号；③ 构建协商策略（正外部性→提议接收补偿，负外部性→提议支付补偿）。
  - **长期 Shapley Chain-of-Thought (CoT)**：任务完成后，智能体基于完整轨迹近似计算 Shapley 值。四个步骤：① 计算集体总奖励 \(R(N,\tau_N)\)；② 估计各联盟下的边际贡献 \(\Delta_i(C,\tau_C)\)；③ 通过加权平均计算 Shapley 值 \(\phi_i(\tau_N)\)；④ 基于 Shapley 值进行协商，达成奖励再分配。
- **Shapley 值公式**：
  \[
  \phi_i = \sum_{C \subseteq N\setminus\{i\}} \frac{|C|!(N-|C|-1)!}{N!} \left[ R(C\cup\{i\}) - R(C) \right]
  \]

## 3. 实验设计

- **场景 / 数据集**：
  1. **Escape Room（两人博弈）**：一个智能体拉杆（付出−1），另一个开门（获得+10），需要合作才能获得最优集体收益。
  2. **Raid Battle（四人 RPG 游戏）**：四个英雄（各拥有嘲讽、火球、治疗技能）协作击败 Boss，每个英雄有不同奖励（火球+2，嘲讽/治疗+0.5），存在自利倾向。分为 Level 1/2/3（Boss HP 依次增加）。
  3. **ChatDEV（软件工程仿真）**：模拟软件公司中的多角色（CEO、CTO、程序员等）合作开发任务，使用加权挣值（WEV）衡量贡献。两个任务：BMI Calculator 和 ArtCanvas。
- **对比方法**：
  - **LLM-only**：无协商或合作。
  - **LLM+NEG**：仅用标准协商（无 Shapley 推理）。
  - **LLM+STS**：仅用短期 Shapley CoT。
  - **LLM+SC**：完整 Shapley-Coop。
- **基准**：在 Escape Room 中，最优公平收益为每人 4.5；在 Raid Battle 中，对比了 LLM+STS 和 LLM+NEG 的奖励分配与实际 Shapley 值的偏差；在 ChatDEV 中，对比了 WEV 计算的预期奖励与人为主观分配。

## 4. 资源与算力

- **明确说明**：论文在附录 B 中指出，“实验在拥有 24 核 CPU 和 32GB DRAM 的小型服务器上的虚拟机上运行。由于实现仅涉及 API 调用，未使用 GPU 资源。” **未使用 GPU**，也未报告具体运行时长或 token 消耗量。

## 5. 实验数量与充分性

- **实验数量**：共三个主要场景，每个场景包含多个条件：
  - Escape Room：对比四种配置，报告成功率和个体收益（图 3 为单次结果？但组图显示了100%、25%、0%成功率，但未说明重复次数）。
  - Raid Battle：三个难度等级，每个等级比较贡献分数（图 4）和奖励分配（图 5），且设置了不同协商轮次（附录表 7）验证收敛性。
  - ChatDEV：两个具体任务，给出各角色的代码、决策、文档、修复的计数，并计算 WEV 范围及调整量（表 3）。
- **充分性与公平性**：
  - 实验覆盖了从简单二人博弈到复杂多步多角色任务，验证了方法的有效性。
  - 对比了逐步消融（STS、NEG、Only），但 **未报告多次重复实验的统计误差（标准差或置信区间）**，尽管论文声称有误差条，但正文图表中未清晰展示。这削弱了结果的可靠性。
  - 在 Raid Battle 中，不同难度下结论一致；在 ChatDEV 中，WEV 权重的选择依据了 COCOMO 等工程基准，较为合理。
  - 未在多种 LLM 模型（仅 DeepSeek-v3）上测试，泛化性有待验证。

## 6. 主要结论与发现

- **Shapley-Coop 能够有效促进自利 LLM 智能体的涌现合作**：在 Escape Room 中，LLM+SC 实现 100% 成功率和接近最优公平收益（4.5）；LLM+NEG 仅 25% 成功，LLM-only 完全失败。
- **公平信用分配**：在 Raid Battle 中，LLM+SC 的奖励分配与理论 Shapley 值偏差极小（多数在 1% 以内），而 LLM+STS 显著低估关键角色（如坦克、治疗）的贡献（偏差可达 6.26%）。LLM+SC 促使智能体更均衡地分配角色（如嘲讽承担更多伤害），提高团队生存和总体表现。
- **在真实复杂任务中的适用性**：在 ChatDEV 中，WEV 计算的公平奖励与人为主观分配的差距很小（多数 <6%），验证了方法对实际多角色协作的适用性。

## 7. 优点

- **新颖的定价视角**：将合作问题转化为基于边际贡献的定价机制，从博弈论角度提供了严谨的理论基础，且无需对 LLM 进行额外训练。
- **模块化设计**：结合短期启发式推理和长期精确计算，兼顾实时协调和事后公平，灵活适应不同时间尺度。
- **覆盖多种场景**：从简单社会困境到复杂多步游戏、再到真实软件工程任务，展示了广泛适用性。
- **可解释性**：协商协议和 Chain-of-Thought 过程透明，易于理解智能体决策依据。
- **零样本/少样本能力**：利用 LLM 内置的推理能力，无需大规模 RL 训练即可实现合作。

## 8. 不足与局限

- **可扩展性与理论纯度**：论文承认近似可能不满足 Shapley 值的效率性质（分配总和等于全局奖励），作为实用化折衷。
- **通信开销**：协商过程引入 token 消耗，在大规模智能体系统中可能成为瓶颈。
- **动态调整缺失**：当前无法在协作过程中动态调整定价，仅依赖事前短期推理和事后分配。
- **实验统计分析不足**：未提供多次重复实验的标准差或显著性检验，结论的稳健性证据有限。
- **模型通用性**：仅使用 DeepSeek-v3 一种模型，不同 LLM 的推理能力差异可能影响结果。
- **环境简化**：Raid Battle 和 Escape Room 仍为模拟环境，与真实世界复杂交互尚有差距；ChatDEV 中的 WEV 权重依赖工程经验，可能存在主观性。
- **未与其他信用分配方法（如 Banzhaf 值、边际贡献平均）做定量对比**，仅在附录 F 中简单说明 Banzhaf 在此任务上表现不佳但未提供系统比较。

（完）
