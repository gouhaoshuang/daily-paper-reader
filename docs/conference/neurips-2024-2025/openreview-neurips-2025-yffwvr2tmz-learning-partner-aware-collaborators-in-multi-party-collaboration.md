---
title: Learning “Partner-Aware” Collaborators in Multi-Party Collaboration
title_zh: 学习多方协作中的“伙伴感知”协作者
authors: "Abhijnan Nath, Nikhil Krishnaswamy"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=yFfWVr2TmZ"
tags: ["query:eca"]
score: 7.0
evidence: 学习面向多方协作的伙伴感知型协作者
tldr: LLM作为人类协作者时缺乏对伙伴的适应性。本文基于对齐理论提出学习“伙伴感知”协作者的框架，通过干预信息增加共同背景。实验显示RLHF训练的智能体在多方协作任务中能更有效地收集信息，提升团队表现，为构建自适应协作智能体提供了理论基础。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-yffwvr2tmz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1434, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-yffwvr2tmz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1419, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-yffwvr2tmz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1409, \"height\": 817, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 451, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1349, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 564, \"height\": 676, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1466, \"height\": 706, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 813, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1452, \"height\": 891, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1451, \"height\": 810, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 927, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-yffwvr2tmz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1455, \"height\": 847, \"label\": \"Table\"}]"
motivation: LLM作为协作者时未能根据伙伴信息调整行为，影响协作效率。
method: 利用RLHF训练智能体从干预中学习，增加与伙伴的共识。
result: 在模拟任务中，训练后的智能体协作表现优于基线。
conclusion: 伙伴感知能力可通过强化学习从人类反馈中习得。
---

## Abstract
Large Language Models (LLMs) are increasingly being deployed in agentic settings where they act as collaborators with humans. Therefore, it is increasingly important to be able to evaluate their abilities to collaborate effectively in multi-turn, multi-party tasks. In this paper, we build on the AI alignment and “safe interruptability” literature to offer novel theoretical insights on collaborative behavior between LLM-driven *collaborator agents* and an *intervention agent*. Our goal is to learn an ideal “partner-aware” collaborator that increases the group’s common-ground (CG)—alignment on task-relevant propositions—by intelligently collecting information provided in *interventions* by a partner agent. We show how LLM agents trained using standard RLHF and related approaches are naturally inclined to ignore possibly well-meaning interventions, which makes increasing group common ground non-trivial in this setting. We employ a two-player Modified-Action MDP to examine this suboptimal behavior of standard AI agents, and propose **Interruptible Collaborative Roleplayer (ICR)**—a novel “partner-aware” learning algorithm to train CG-optimal collaborators. Experiments on multiple collaborative task environments show that ICR, on average, is more capable of promoting successful CG convergence and exploring more diverse solutions in such tasks.

---

## 论文详细总结（自动生成）

# 论文总结：Learning “Partner-Aware” Collaborators in Multi-Party Collaboration

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：Large Language Models (LLMs) 越来越多地被部署为与人类协作的智能体，但在多轮、多方协作任务中，它们往往缺乏对合作伙伴行为（尤其是来自干预代理的“干预”信息）的适应性。标准 RLHF 或偏好对齐方法训练出的 LLM 协作智能体倾向于忽视甚至错误响应可能有益的干预，导致无法有效增加团队的共同基础（common ground, CG）。
- **背景**：本研究建立在 AI 对齐和“安全可中断性”（safe interruptability）文献之上，旨在理论化和解决协作智能体在接收干预时的鲁棒性问题。
- **核心目标**：训练一个理想的“伙伴感知”（partner-aware）协作智能体，使其能够智能地收集和整合合作伙伴提供的干预信息，从而促进团队在任务相关命题上的对齐（即共同基础的增长）。

## 2. 方法论

- **核心思想**：面对质量参差不齐的干预（可能有帮助或误导），协作智能体应具备选择性采纳的能力，即“安全可中断性”——既不过度信任也不完全忽视干预。作者提出 Interruptible Collaborative Roleplayer (ICR) 算法，通过**反事实不变性 KL 散度正则化**来训练伙伴感知型智能体。
- **关键模型框架**：采用 Modified-Action MDP (MAMDP) 建模协作智能体 π_C 与干预智能体 π_I 的交互。状态 s_t 包含对话历史，每个时间步干预智能体生成动作 a_t^I，协作智能体生成响应 ˆa_t^C，环境转移并给出奖励。
- **技术细节**：
  - 标准优化目标：`J(θ_C) = E[Σ γ^t U_task] - λ_H D_KL(π_C || π_Ref)`
  - ICR 加入反事实 KL 项：`J*(θ_C) = J(θ_C) - λ_Intent D_KL(π_C(·|s,a^I) || π_C_CF(·|s_CF,a^I))`，其中 s_CF 为反事实状态（明确告知干预不会提升任务效用）。
  - 反事实策略 π_C_CF 通过简单修改提示前缀实现（例如“干预不会改善你的表现”），并利用 stop-gradient 避免梯度干扰。
  - 训练算法：使用 PPO 优化，额外计算反事实条件下的 token 级对数概率差异，计算高效（仅需一个额外前向传播）。
- **理论支撑**：定理 3.2 证明标准偏好对齐策略在 MAMDP 中次优；定理 B.4 证明反事实不变性正则化可以界定期望性能差距，当 λ_Intent → ∞ 时，策略性能接近最优。

## 3. 实验设计

- **数据集/场景**：
  - **DeliData Wason Card Selection Task**：测试逻辑规则验证（如“所有元音卡片背面是偶数”），智能体通过对话决定翻转哪些卡片。
  - **Weights Task**：多智能体合作推断彩色块重量（红=10g, 蓝=10g, 绿=20g 等）。
- **评估设置**：分为“full-press”（自由自然语言对话）和“no-press”（离散行动/信念表示）两种条件。
- **对比方法**：
  - BC-Collaborator（行为克隆）
  - DPO, IPO（离线偏好优化）
  - PPO（在线强化学习）
  - PSO-Intent（因果路径目标）
  - ICR（本文方法）
- **主要指标**：
  - Weights Task: ACC（正确性 × 共同基础大小）
  - DeliData: ACC（最终方案准确率）和 CG gain（共同基础增益，即对话中新出现方案类型数减去初始方案数）
- **训练数据**：使用 GPT-4o 作为专家，生成 15 轮交互轨迹，作为所有方法的训练/专家演示。

## 4. 资源与算力

- **训练硬件**：
  - full-press 实验使用 2 张 NVIDIA A100 GPU。
  - no-press 实验使用 1 张 A100 GPU。
  - OPT-1.3B 奖励模型（full-press）训练也使用 1 张 A100。
- **训练时间**：
  - 标准基线（BC, DPO, IPO 等）约 12 GPU 小时。
  - PPO（包括 ICR）约 24 小时（6000 小批量，有效批次大小 8）。
- **说明**：论文明确指出由于计算预算限制，仅训练了 8B 参数规模的模型（Meta-Llama-3-8B-Instruct），更大规模的集中式协同未尝试。

## 5. 实验数量与充分性

- **主要实验**：每个数据集/设置各进行 100 次对话（每次 15 轮），报告平均值和标准误差（见表 1），覆盖 full-press 和 no-press 两种条件。
- **消融实验**：对反事实正则化强度 λ_Intent 进行调参（0.01, 0.2, 1.0），展示在 DeliData no-press 下的训练曲线（图 1b），基于 3 个随机种子。
- **附加实验**（附录 A）：
  - 替换反事实前缀变体测试鲁棒性（ICR-Phrasing）。
  - 遮蔽干预或使用更弱干预智能体（ICR-Masked, ICR-Small）。
  - 改变干预极性（PSO-Skeptical）。
  - 使用 GPT-4o-mini 和 GPT-4o 配对作为专家基线。
- **充分性与公平性**：实验设计较全面，对比方法覆盖行为克隆、偏好优化、在线强化学习等主流类型，且所有基线从相同 BC 模型初始化。指标既包含任务正确性也包含共同基础度量。但论文仅测试了两种任务，且干预智能体固定为 GPT-4o，未评估人类干预或不同 LLM 干预下的泛化，存在一定局限。

## 6. 主要结论与发现

- ICR 在所有设置（full-press & no-press，两个任务）下显著优于所有基线。
  - Weights Task full-press: ICR ACC 14.06 vs 第二名 DPO 9.56（提升约 47%）。
  - DeliData full-press: ICR ACC 0.88, CG 3.35, 比 BC-Collaborator（ACC 0.71, CG -0.13）大幅提升。
  - no-press 下 ICR 仍保持领先，显示反事实正则化即使在没有语言互动时也有效。
- 共同基础增长在复杂命题（如排序关系）上尤为显著（图 1a），ICR 在后期对话轮次持续拓展知识。
- 反事实正则化强度 λ_Intent = 0.2 取得最佳平衡，既避免过度忽略干预也防止过度依赖。
- 训练时不使用共同基础奖励，ICR 仍能通过优化任务效用自然产生共同基础对齐（emergent property）。

## 7. 优点

- **理论创新**：将 MAMDP 引入协作对话建模，并提出反事实不变性正则化，理论证明了其对次优性间隙的约束。
- **方法高效**：反事实 KL 计算不额外采样 token，仅一次额外前向传播，计算成本低。
- **训练无需显式共同基础信号**：ICR 在无 CG 奖励下仍能涌现更好的共识，说明其学到了内在的协作原则，泛化潜力大。
- **实验设计严谨**：区分 full-press 和 no-press，控制语言因素；对比多种基线；进行消融和多种替代条件验证；提供 GPT-4o 干预质量的人工验证（Cohen’s κ 高）。

## 8. 不足与局限

- **模型规模有限**：仅训练 8B 参数模型，更大模型是否受益未验证。
- **干预智能体固定**：所有实验中干预智能体同为 GPT-4o（专家级），未测试来自不同性能或不同类型 LLM 的干预，也未包含人类干预。真实场景中干预风格多变。
- **任务覆盖有限**：仅测试了 DeliData 和 Weights Task 两类协作推理任务，未在更长时域或需欺骗/博弈的任务（如 Diplomacy）中评估。
- **训练数据来源**：全为 GPT-4o 生成的模拟数据，缺乏真实人类协作数据，可能引入分布偏差。
- **反事实前缀敏感性**：虽然论文测试了变体且表现稳健，但仅基于 50 个样本和 6 种前缀，更大规模测试可能揭示差异。
- **潜在滥用风险**：伙伴感知能力可能被恶意用于操纵（sleeper agents 等），论文提到需配合红队测试和伦理审查，但未提供具体保障。
- **可扩展性**：集中式梯度通信方法难以应用于大型 LLM，当前分散式训练可能效率不足。

（完）
