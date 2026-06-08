---
title: Cross-environment Cooperation Enables Zero-shot Multi-agent Coordination
title_zh: 跨环境合作实现零样本多代理协调
authors: "Kunal Jha, Wilka Carvalho, Yancheng Liang, Simon Shaolei Du, Max Kleiman-Weiner, Natasha Jaques"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=zBBYsVGKuB"
tags: ["query:eca"]
score: 8.0
evidence: 跨环境合作实现零样本多代理协调
tldr: 零样本协调面临对新任务和新伙伴泛化能力不足的问题。本文提出跨环境合作（CEC）范式，通过在程序生成的多样化环境中与单一伙伴进行强化学习，训练出通用协作策略。实验表明，CEC能在多种未见过的任务和伙伴上实现有效零样本协调，远超现有基线，为分布式边缘云代理协作提供了可迁移的协作训练方法。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 813, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 528, \"height\": 356, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 860, \"height\": 180, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 854, \"height\": 179, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 862, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 726, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 842, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 863, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 776, \"height\": 684, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 849, \"height\": 228, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1505, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 888, \"height\": 1209, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 863, \"height\": 577, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1782, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 854, \"height\": 564, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 850, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 847, \"height\": 552, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 848, \"height\": 562, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 816, \"height\": 845, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1772, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 814, \"height\": 844, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 474, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 473, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1765, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 449, \"height\": 329, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1724, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1730, \"height\": 999, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 851, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zbbysvgkub/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 853, \"height\": 323, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zbbysvgkub/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1709, \"height\": 1404, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zbbysvgkub/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1578, \"height\": 778, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zbbysvgkub/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1246, \"height\": 911, \"label\": \"Table\"}]"
motivation: 现有零样本协调研究局限于单一任务，无法泛化到新任务或新伙伴。
method: 提出跨环境合作（CEC）范式，通过在分布环境中与单一伙伴训练学习通用协作技能。
result: CEC在多种新任务和新伙伴上实现零样本协调，超越基线方法。
conclusion: 证明了跨环境分布训练可以学习通用协作技能，对实现类人兼容AI至关重要。
---

## Abstract
Zero-shot coordination (ZSC), the ability to adapt to a new partner in a cooperative task, is a critical component of human-compatible AI. While prior work has focused on training agents to cooperate on a single task, these specialized models do not generalize to new tasks, even if they are highly similar. Here, we study how reinforcement learning on a **distribution of environments with a single partner** enables learning general cooperative skills that support ZSC with **many new partners on many new problems**. We introduce *two* Jax-based, procedural generators that create billions of solvable coordination challenges. We develop a new paradigm called **Cross-Environment Cooperation (CEC)**, and show that it outperforms competitive baselines quantitatively and qualitatively when collaborating with real people. Our findings suggest that learning to collaborate across many unique scenarios encourages agents to develop general norms, which prove effective for collaboration with different partners. Together, our results suggest a new route toward designing generalist cooperative agents capable of interacting with humans without requiring human data.

---

## 论文详细总结（自动生成）

# 论文总结：Cross-environment Cooperation Enables Zero-shot Multi-agent Coordination

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：现有零样本协调（Zero-shot Coordination, ZSC）研究主要聚焦于在**单一任务**上训练代理与不同伙伴协作，这导致代理无法泛化到新的任务场景，即便是高度相似的任务也难以适应。例如，基于人口训练（Population-based Training, PBT）的代理在稍作变动的新环境中需要重新训练，缺乏真正的通用协作能力。
- **背景**：人类擅长即兴协作，能够根据新伙伴和新环境灵活调整行为。然而，当前强化学习方法尚未解决这一挑战。作者旨在探索：**能否仅通过训练代理在大量不同环境中与单一伙伴协作，使其学会能够泛化到新伙伴和新任务的通用协作策略？**
- **含义**：成功实现跨环境协作将推动面向现实世界（如家庭机器人、自动驾驶、自适应教学助手）的类人兼容AI的发展，减少对大量人类数据或每任务重新训练的依赖。

## 2. 方法论：核心思想、关键技术细节与算法流程
- **核心思想**：提出**跨环境合作（Cross-environment Cooperation, CEC）** 范式。与现有方法侧重**伙伴多样性**不同，CEC通过**环境多样性**来训练协作能力：代理在**程序化生成的大量不同任务**中，使用**自我对弈（Self-Play, SP）**（即与自身副本协作）进行训练，从而学习一般性的协作规范。
- **关键技术细节**：
  - **程序化环境生成**：设计了两套基于Jax的快速程序生成器：
    - **Dual Destination游戏**：一个简单网格世界，通过随机化目标位置和代理起始位置生成数十亿种不同的协调挑战。
    - **Overcooked环境**：基于原始五个布局（Asymmetric Advantages, Coordination Ring 等）的结构骨架，均匀采样墙壁结构后随机放置目标、锅、盘子、洋葱等物体，并确保布局可解（保持物体可到达）。可生成约1.16×10^17种不同且可解的厨房布局。同时支持随机旋转以增强表示学习。
  - **训练算法**：使用**IPPO**（Independent PPO）作为底层多智能体强化学习算法，代理通过自我对弈优化目标函数：
    \[
    J(\pi_C) = \mathbb{E}_{m_i \sim \mathcal{M}} [S(\pi_C, \pi_C, m_i)]
    \]
    其中 \(m_i\) 为环境任务，\(\mathcal{M}\) 为任务分布，\(S\) 为合作得分。
  - **网络架构**：采用卷积编码器 + LSTM循环核心 + 分离的actor-critic head。LSTM使代理具备基础元学习能力，能够基于历史适应伙伴行为。
  - **CEC-Finetune**：在预训练CEC后，针对某个特定布局（原始五个布局之一）进行100M步微调（降低学习率），以权衡泛化与专业化。

## 3. 实验设计
- **场景与数据集**：
  - **Dual Destination游戏**：一个5×5网格，两个代理需移动到对方起始位置的绿色方格以获得奖励。设置了固定任务（基准）和程序化生成任务。
  - **Overcooked**：两个版本的评估：
    - **原始5个布局**（Asymmetric Advantages, Coordination Ring, Counter Circuit, Cramped Room, Forced Coordination）——这些布局从CEC训练分布中完全留出。
    - **100个程序化生成的布局**（由生成器创建，未在训练中出现）。
- **基准方法**：
  - **IPPO**：单任务自我对弈基线。
  - **FCP**（Fictitious Co-Play）：流行的PBT方法，训练代理对一个多样化的伙伴种群作最佳反应。
  - **E3T**（Efficient End-to-End Training）：当前单任务ZSC的SOTA方法，通过向伙伴策略添加随机性和辅助动作预测网络提升跨玩家迁移。
  - **CEC**：本文提出的跨环境自我对弈方法。
  - **CEC-Finetune**：CEC在特定布局上微调后的变体。
  - **IPPO-、FCP-**（仅用于人类实验）：单任务代理在从未见过的布局上测试。
- **评估指标**：
  - **交叉对弈（Cross-Play, XP）奖励**：代理与不同种子训练的伙伴协作的平均得分。
  - **人类-AI协作**：成功率（平均每局完成食谱个数）、主观评分（Likert量表：适应性、一致性、类人程度、干扰度、挫败感、享受度、协调能力）。
  - **碰撞次数**：人类与AI之间的冲突数量。
- **对比策略**：模拟实验中比较所有方法在原始5布局和100程序生成布局上的XP奖励；人类实验中比较CEC、CEC-FT、E3T、FCP、IPPO等。

## 4. 资源与算力
- 文中明确提到：环境、训练和测试代码全部基于Jax实现，**训练速度可达每秒1000万步（10M steps/min on a single GPU）**。所有模型（CEC及基线）均训练**30亿步（3 billion steps）**。
- **未明确说明具体GPU型号和数量**，仅提到“single GPU”。从Jax的高效并行性推断，可能使用一张NVIDIA V100或A100等消费级GPU即可完成训练。算力消耗相对可控。

## 5. 实验数量与充分性
- **实验组数**：
  - **模拟实验**：Dual Destination（固定任务+100个程序生成任务，含部分可观测、多任务变体）；Overcooked（原始5布局+100个程序生成布局）；跨算法对弈（IPPO, FCP, E3T, CEC, CEC-FT两两配对）。每个条件训练6个种子（seed）。
  - **人类研究**：80名参与者，每人在两个最难布局（Counter Circuit, Coordination Ring）上依次与多个模型（IPPO, FCP, E3T, CEC, CEC-FT）协作，每个布局40人。约30分钟实验，收集主观评分和成功次数。
  - **消融实验**：部分可观测性下的CEC、多任务变体下的CEC、结合环境与伙伴多样性（CEC-E3T）、无LSTM的CEC等。
- **充分性与公平性**：
  - 实验覆盖了简单（Dual Destination）和复杂（Overcooked）环境，同时测试了对新伙伴和新环境的泛化能力。
  - 严格留出测试布局，使CEC对原始布局无训练优势。
  - 人类实验中双盲（参与者不知模型身份），顺序随机化，每个模型使用不同种子。
  - 统计学检验（t-test）和Cronbach's alpha（≈0.874）证明主观指标可靠性。
  - 缺点：部分模型（如CEC-E3T）未完整收敛，训练步数可能不足；人类样本存在WEIRD偏差（仅英语流利者）。

## 6. 主要结论与发现
1. **环境多样性优于伙伴多样性**：CEC（仅自我对弈，单一伙伴）在交叉对弈中系统性优于PBT方法（FCP），表明增加环境多样性比增加伙伴多样性更有效。
2. **CEC可实现零样本协调**：CEC代理能泛化到从未见过的任务和伙伴，而单任务方法（IPPO, FCP, E3T）在程序生成布局上得分为0，完全失败。
3. **微调提升单任务性能但牺牲泛化**：CEC-Finetune在原始布局上超越所有基线（包括E3T），但在程序生成布局上泛化下降，体现通用性与专业性之间权衡。
4. **人类主观偏好偏向CEC**：尽管CEC在协作得分上略低于E3T，但人类用户在所有7项主观指标上给予CEC和CEC-FT最高评分，尤其体现在适应性、低挫败感、低碰撞次数上。碰撞次数CEC最低。
5. **学习通用规范**：CEC代理的访问热力图显示其对任务相关物体（锅、洋葱堆等）分布更均匀，而非固定路线，表明其学会更高层次的结构化协作策略。

## 7. 优点
- **方法创新**：首次系统性地证明环境多样性可替代伙伴多样性实现零样本协调，挑战了“自我对弈在协作游戏中无效”的既有观点。
- **基础设施贡献**：设计了两个快速Jax程序生成器，特别是Overcooked生成器能产生1.16×10^17种可解布局，支持高效训练（10M步/分钟）。
- **实验严谨**：同时包含模拟和人类实验，使用多种指标（奖励、主观评分、碰撞数、博弈论分析），通过统计检验验证显著性。
- **可复现性**：提供完整代码和训练/测试脚本，开源。
- **实际意义**：无需人类数据即可训练通用协作AI，降低对齐成本，适用于边缘云代理协作等实际场景。

## 8. 不足与局限
- **性能未达SOTA奖励**：在原始布局上CEC的协作奖励低于E3T，仅在主观评分上胜出，可能需要更长训练或更优网络才能达到奖励最优。
- **训练未收敛**：图7显示CEC的XP性能仍在上升，3B步训练可能未充分，最佳性能上限未探明。
- **结合环境与伙伴多样性未获益**：CEC-E3T表现不佳，表明如何有效融合两种多样性仍需研究。
- **人类样本偏差**：仅招募英语流利者（WEIRD样本），可能影响主观评分的文化普适性。
- **环境范围限制**：仅测试了Overcooked和网格世界，未来需在更复杂任务（如机器人）上验证。
- **碰撞避免可能过度**：CEC为减少碰撞牺牲了效率，导致奖励略低；实际应用中可能需权衡效率与合作感。

（完）
