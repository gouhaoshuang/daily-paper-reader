---
title: "Learning Preferences without Interaction for Cooperative AI: A Hybrid Offline-Online Approach"
title_zh: 无需交互学习偏好用于合作AI：一种混合离线-在线方法
authors: "Haitong Ma, Haoran Yu, Haobo Fu, Shuai Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=QVheAhJefR"
tags: ["query:eca"]
score: 4.0
evidence: 合作AI与人类偏好学习
tldr: 合作AI常忽略人类偏好，而人类仅提供少量离线偏好反馈，无法在线交互。本文提出混合离线-在线强化学习方法，利用离线反馈预训练偏好模型，再通过在线微调解决分布偏移，使协作智能体更好地对齐人类偏好，提升合作任务中的用户满意度。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-qvheahjefr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1201, \"height\": 682, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qvheahjefr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1430, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qvheahjefr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 563, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qvheahjefr/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1438, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qvheahjefr/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 792, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qvheahjefr/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1246, \"height\": 974, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 695, \"height\": 238, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 697, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 840, \"height\": 133, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1183, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1145, \"height\": 540, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 905, \"height\": 183, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 775, \"height\": 930, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 779, \"height\": 1148, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1440, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 847, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1186, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1441, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qvheahjefr/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 800, \"height\": 238, \"label\": \"Table\"}]"
motivation: 合作智能体需要对齐人类偏好，但人类仅提供少量离线反馈，导致在线学习分布偏移。
method: 混合离线-在线强化学习框架，先用离线偏好数据学习模型，再进行在线适应。
result: 在合作任务中，智能体行为更符合人类偏好，任务成功率与满意度均提升。
conclusion: 离线-在线混合学习有效对齐合作AI与人类偏好。
---

## Abstract
Reinforcement learning (RL) for collaborative agents capable of cooperating with humans to accomplish tasks has long been a central goal in the RL community. While prior approaches have made progress in adapting collaborative agents to diverse human partners, they often focus solely on optimizing task performance and overlook human preferences—despite the fact that such preferences often diverge from the reward-maximization objective of the environment.
Addressing this discrepancy poses significant challenges: humans typically provide only a small amount of offline, preference-related feedback and are unable to engage in online interactions, resulting in a distributional mismatch between the agent’s online learning process and the offline human data. To tackle this, we formulate the problem as an online&offline reinforcement learning problem that jointly integrates online generalization and offline preference learning, entirely under an offline training regime.
We propose a simple yet effective training framework built upon existing RL algorithms that alternates between offline preference learning and online generalization recovery, ensuring the stability and alignment of both learning objectives.
We evaluate our approach on a benchmark built upon the Overcooked environment—a standard environment  for human-agent collaboration—and demonstrate remarkable performance across diverse preference styles and cooperative scenarios.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究动机**：在多智能体合作场景（如多人游戏）中，传统强化学习（RL）协作智能体只优化环境奖励（任务表现），而忽略了人类用户的个性化偏好。例如在《Overcooked》游戏中，人类玩家偏好做土豆汤，但智能体只追求最大奖励可能独立做番茄汤，导致协调不佳。
- **现实背景**：许多游戏（如《英雄联盟》《王者荣耀》）已提供“点赞”机制，用户可在赛后对队友行为进行正向反馈，这些离线轨迹隐含地反映了偏好。但人类只能提供少量离线偏好反馈，无法在线交互，造成智能体在线学习分布与离线数据分布不匹配。
- **问题定义**：提出一种新颖的 **online & offline RL 问题**，需同时满足：
    1. 零样本泛化到未见过的合作伙伴；
    2. 对齐少量离线偏好轨迹中的人类偏好。
- **三大假设**：
    - 存在支持在线交互的环境；
    - 有策略池可用于训练协作智能体的泛化能力；
    - 有少量反映人类偏好的离线轨迹（仅正向标签）。

## 2. 方法论：核心思想、关键技术与算法流程

### 核心思想
受 NLP 中“预训练 + 监督微调（SFT）”范式的启发，将协作智能体学习分为：
- **预训练阶段**（对应通用泛化能力）→ 在线与策略池交互，使用 MAPPO 算法最大化环境奖励；
- **偏好学习阶段**（对应下游微调）→ 对少量偏好轨迹进行行为克隆（BC）；
- **泛化恢复阶段** → 重新在线交互，恢复因偏好学习而下降的泛化性能。
进一步提出 **Epoch-wise Alternation Recovery (EAR)** 策略：交替执行轻量 BC（仅 1 epoch）和泛化恢复，逐步提升偏好对齐且保持泛化。

### 关键技术细节
- **预训练**：使用 FCP 方法构建策略池（包含不同能力的子策略），协作智能体与其在线交互，通过 MAPPO 进行优化。
- **偏好学习**：对少量“点赞”轨迹进行行为克隆（BC），最大化动作似然。
- **泛化恢复**：再次与策略池在线交互，直到平均环境回报恢复至预训练水平。
- **EAR 循环**：
    1. 在已恢复的智能体上执行 1 epoch BC；
    2. 再次在线恢复泛化至基线；
    3. 检查偏好准确率是否达到第二阶段完全收敛时的水平，若未达到则继续迭代。

### 算法流程（文字描述）
1. **Stage 1**：在线预训练协作智能体 \(\pi\)，与策略池交互，获得泛化基线回报 \(r_{gen}\)。
2. **Stage 2**：在偏好数据集上对 \(\pi\) 进行完整 BC 直至收敛，记录准确率 \(\eta\)；然后在线恢复泛化至 \(r_{gen}\) 或达到预算。
3. **Stage 3（EAR）**：
    - 重复：
        - 在偏好数据上执行 1 epoch BC；
        - 在线恢复泛化至 \(r_{gen}\)；
        - 评估当前偏好准确率 \(\eta_{curr}\)；
    - 直到 \(\eta_{curr} \ge \eta\) 或预算耗尽。

### 为什么有效
实验表明：完整 BC 后泛化性能下降 1/3 以上，但泛化恢复后部分偏好信息仍被保留；采用轻量交替逐步注入偏好，可稳定地同时维持两类目标。

## 3. 实验设计

### 环境与基准
- **环境**：Overcooked 游戏中的两个布局 —— **Coordination Ring**（环形厨房，需协调移动）和 **Many Orders**（方形厨房，多食谱偏好）。
- **模拟人类偏好**：参考 HSP 方法，通过给关键游戏事件赋予偏差权重来定义偏好奖励函数 \(R_w\)，并训练出相应的人类代理（proxy）策略。
- **离线偏好数据集**：对每个偏好风格，从 2N 条轨迹中筛选出偏好回报达到最大 80% 的轨迹作为“点赞”轨迹。三种偏好风格（Style A/B/C）的轨迹数量见附录表 7（如 Coordination Ring 下分别为 12/24/20 条）。
- **策略池**：包含 18 个不同能力级别的自博弈检查点（FCP 方式），用于泛化训练和恢复。

### 对比方法
1. **BC Only**：仅对偏好轨迹进行行为克隆（无预训练）。
2. **ZSC (Pretrain)**：仅用 FCP 预训练（无偏好学习），选择次优检查点。
3. **Pretrain + BC**：预训练后直接进行完整 BC。
4. **Pretrain + BC + Recover**：预训练→完整 BC→泛化恢复（即本文 Stage 2 方法）。
5. **EAR**：本文三阶段交替方法。
此外，在消融中对比了 MEP、TrajDi 等多样性预训练方法。

### 评估指标
- **环境回报 (Env. Return)**：成功交付的汤数 ×20，衡量任务完成能力。
- **偏好得分 (Preference Score)**：根据偏好奖励函数计算的事件加权和，衡量偏好对齐程度。
- **动作准确率 (Action Accuracy)**：在偏好测试集上的动作一致性。

### 实验组数
- 主实验：2 个布局 × 3 种偏好风格，每种方法重复 3 个随机种子，结果以均值±标准差报告。
- 泛化测试：对每个方法在所有 benchmark 人类代理（N个）上评估平均环境回报。
- 消融与可视化：包括 UMAPP 行为分析、EAR 收敛步数记录、以及对抗多样性方法的对比。

## 4. 资源与算力

- **硬件**：所有实验在单张 NVIDIA GeForce RTX 2080 Ti GPU 上运行。
- **训练预算**：每次 rollout batch 包含 200 条轨迹（每条 400 步），总交互步数上限为 \(2 \times 10^6\) 步。EAR 收敛所需 batch 数在 188~206 之间（Coordination Ring 布局）。
- **执行时间示例**（Many Orders, Style A）：
    - 1 epoch BC：27.1 秒；
    - 一次环境 rollout：5.7 秒；
    - 一次 PPO 更新（15 epoch）：10.5 秒。

## 5. 实验数量与充分性

- **数量**：覆盖两张地图、三种偏好、多种基线，进行了充分的消融和对比。
- **充分性**：
    - 主实验结果（表 1、表 10）清晰展示了 EAR 在偏好得分和环境回报上的优势。
    - 泛化测试（表 2、表 11）验证了 EAR 保持了良好的零样本泛化能力。
    - 消融实验（表 3）显示 EAR 比“Pretrain+BC+Recover”能更好地保留偏好准确率。
    - 与 MEP、TrajDi 的对比（表 13）说明仅增加多样性无法解决偏好偏移问题。
    - 行为可视化（图 3、图 6）直观展示了 EAR 智能体的风格对齐。
- **公平性**：对比方法均选用公开且匹配的设置；随机种子重复三次，报告统计误差。

## 6. 主要结论与发现

- **预训练至关重要**：从头开始进行偏好学习会导致严重过拟合，且后期难以恢复泛化性能。
- **偏好学习与泛化存在冲突**：完整 BC 后泛化回报可能下降 1/3；但泛化恢复后偏好信息不会完全丢失。
- **EAR 能有效平衡两者**：通过交替 1 epoch BC 和泛化恢复，逐步提升偏好对齐同时保持泛化，优于直接完整 BC+恢复的方法。
- **在多个偏好风格和布局上均取得提升**：偏好得分和环境回报均显著优于 ZSC 基线，且泛化能力与原始预训练智能体相当。

## 7. 优点

- **问题新颖**：首次明确将“零样本泛化+少量离线偏好对齐”定义为 online & offline RL 问题，贴合游戏工业实际需求。
- **方法简洁有效**：借鉴 NLP 的预训练+微调范式，提出交替训练策略，不依赖复杂模型或额外假设。
- **实验充分**：涵盖多个布局、多种偏好、多种基线，并进行消融、行为分析和泛化测试，验证了方法的鲁棒性。
- **计算高效**：在单 GPU 上即可完成，训练预算可控。

## 8. 不足与局限

- **环境泛化性有限**：实验仅基于 Overcooked 环境，虽具有代表性但相对简单，更复杂环境（如 5v5 团队游戏）的应用有待验证。
- **偏好模拟偏差**：使用预设的权重偏差模拟人类偏好，与真实人类行为存在差距。
- **未利用未标记数据**：大量无偏好的玩家轨迹（可能包含有用信息）未被采用，未来可探索半监督或自监督方法。
- **方法较为基础**：可直接使用更高级的离线偏好学习技术（如 DPO、IPO）替代行为克隆，可能进一步提升性能。

（完）
