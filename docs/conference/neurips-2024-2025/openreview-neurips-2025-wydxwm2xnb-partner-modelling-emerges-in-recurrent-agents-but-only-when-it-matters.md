---
title: Partner Modelling Emerges in Recurrent Agents (But Only When It Matters)
title_zh: 伙伴建模在循环智能体中涌现（但仅在必要时）
authors: "Ruaridh Mon-Williams, Max Taylor-Davies, Elizabeth Mieczkowski, Natalia Vélez, Neil R Bramley, Yanwei Wang, Thomas L. Griffiths, Christopher G. Lucas"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=WydxWM2xNb"
tags: ["query:eca"]
score: 4.0
evidence: 合作代理中伙伴建模的涌现
tldr: 合作AI需要推断伙伴能力，但现有方法依赖显式建模。本文在Overcooked-AI环境中训练简单无模型RNN智能体与多样化伙伴协作，分析其内部隐状态发现，无需额外结构或归纳偏置，伙伴建模可自发涌现于开放式合作互动中。该发现揭示了合作智能体设计的基本原理，对端云协同中的自适应协作有参考价值。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 732, \"height\": 667, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 1166, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1441, \"height\": 1308, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1456, \"height\": 887, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1449, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1453, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1174, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wydxwm2xnb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1453, \"height\": 338, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-wydxwm2xnb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 569, \"height\": 771, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wydxwm2xnb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1174, \"height\": 262, \"label\": \"Table\"}]"
motivation: 探究合作智能体是否无需显式机制即可自发学习建模合作伙伴。
method: 训练无模型RNN智能体与多样伙伴协作，分析隐状态与伙伴能力的关系。
result: 智能体在开放式协作中自发发展出伙伴建模能力，且仅在任务需要时才启用。
conclusion: 合作压力足以驱动伙伴建模的涌现，简化了协作智能体的设计。
---

## Abstract
Humans are remarkably adept at collaboration, able to infer the strengths and weaknesses of new partners in order to work successfully towards shared goals. To build AI systems with this capability, we must first understand its building blocks: does such flexibility require explicit, dedicated mechanisms for modelling others—or can it emerge spontaneously from the pressures of open-ended cooperative interaction? To investigate this question, we train simple model-free RNN agents to collaborate with a population of diverse partners. Using the 'Overcooked-AI' environment, we collect data from thousands of collaborative teams, and analyse agents' internal hidden states. Despite a lack of additional architectural features, inductive biases, or auxiliary objectives, the agents nevertheless develop structured internal representations of their partners' task abilities, enabling rapid adaptation and generalisation to novel collaborators. We investigated these internal models through probing techniques, and large-scale behavioural analysis. Notably, we find that structured partner modelling emerges when agents can influence partner behaviour by controlling task allocation. Our results show that partner modelling can arise spontaneously in model-free agents—but only under environmental conditions that impose the right kind of social pressure.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：人类能够灵活推断合作者的能力（如优势、弱点），并据此调整协作策略。这种能力（即“伙伴建模”）是否需要专门的、显式的机制，还是可以在开放式合作互动的压力下自发涌现？
- **研究动机**：构建具备类似协作能力的AI系统，理解伙伴建模的底层构建模块。现有工作（如“机器心智理论”）通常依赖专用模块或辅助目标来显式建模他人，而该文试图检验在**无额外架构偏好、无辅助目标**的条件下，简单的无模型循环神经网络（RNN）智能体是否能自发形成对伙伴能力的结构性内部表征。
- **整体含义**：证明社会智能可以在特定环境压力下通过通用学习和记忆机制产生，不必依赖专用架构，为设计更自然的协作AI提供新思路。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用**ad hoc teamwork**（临时团队合作）设定，训练一个“自我智能体”（ego agent）与一群具有不同任务能力的伙伴协作，自我智能体仅通过最大化共享奖励（任务奖励）进行训练，没有任何显式的伙伴建模目标。
- **环境与设置**：基于**Overcooked-AI**（完全合作烹饪游戏），自我智能体和伙伴共同准备汤品，需要分工（准备食材 vs. 盛汤）。自我智能体可以控制伙伴当前执行哪个子任务（即拥有“影响能力”）。
- **关键技术细节**：
  - 自我智能体使用**门控循环单元（GRU）** RNN，输入局部观测，输出策略。
  - 伙伴的策略由两个预训练的子任务网络组成，通过**冷却间隔**（cooldown interval）控制其任务速度（即能力向量\( v = [v_1, v_2] \)，值越小能力越强）。
  - 自我智能体使用**Proximal Policy Optimization (PPO)** 训练，没有辅助损失，仅优化累积期望奖励。
  - 为了检验伙伴建模的涌现，设计了三个实验：实验1——检验子任务分配压力是否驱动建模；实验2——检验是否可以在线适应中途更换的伙伴；实验3——检验盲智能体（仅接收自身位置的自我感知信号）能否仅从任务奖励中建模伙伴能力。
- **分析工具**：
  - **线性探测（Linear Probe）**：从RNN隐状态解码伙伴的任务速度。
  - **UMAP降维**：可视化隐状态结构。
  - **行为分析**：任务分配效率（伙伴最擅长的任务与其实际花费时间的相关性）。
- **对比基线**：
  - **前馈MLP**（无记忆）
  - **单伙伴RNN**（仅训练于固定伙伴）
  - **无影响力RNN**（无法影响伙伴行为，但接触多样伙伴）

### 3. 实验设计：数据集/场景、benchmark、对比方法

- **环境与场景**：
  - 主环境：**Overcooked-AI**（5种不同厨房布局：cramped room, coord ring, fivebyfive, cramped_room_v3, cramped_room_v4）。
  - 附加环境：**CoinGame**（辅助验证，收集红蓝硬币，类似任务分配）。
- **Benchmark**：没有标准benchmark，而是论文自己设计的任务：要求自我智能体在未知伙伴面前最大化合作产出（汤品数量）。
- **对比方法**：
  1. **多伙伴RNN（本文主模型）**：训练于多样伙伴，拥有影响力。
  2. **前馈MLP**：无记忆。
  3. **单伙伴RNN**：只训练于固定伙伴。
  4. **无影响力RNN**：暴露多样伙伴但无法影响其行为。
- **伙伴生成**：训练时伙伴的冷却间隔从{1,2,3,4,7,9}采样；评估时从未见过的新组合（如{0,2,3,8,10}）。在实验3中，伙伴的随机动作概率在0~1变化。

### 4. 资源与算力

- 论文明确报告：
  - **GPU型号**：A100 GPU。
  - **总算力**：**462 GPU-hours**（训练225小时，评估207小时）。
  - 训练使用了**256个并行环境实例**，每个实验运行**15M时间步**。
  - 所有实验运行在JAX框架下，使用`jax.jit`加速。

### 5. 实验数量与充分性

- **实验数量**：
  - 主实验在5种布局上进行，每个布局训练5个随机种子，最终选择表现最好的种子进行详细分析。
  - 评估时，每个布局下测试24种未见伙伴，每个伙伴进行20次rollout（20个随机种子），总计**2400次rollout**。
  - 实验2（在线适应）在3种布局上测试，每episode 600步，中途切换伙伴。
  - 实验3（盲智能体）在5种布局上测试6种未见伙伴，每个种子10次rollout。
  - 额外在CoinGame环境上复制了主要发现（附录A）。
  - 线性探测：对每个时间窗口训练独立探针，使用80-20训练-测试划分。
- **充分性**：
  - 实验覆盖了不同布局、不同伙伴分布、不同记忆条件（RNN vs MLP）、不同影响力条件，比较全面。
  - 提供了置信区间（bootstrapped 95% CI）和线性探针的准确性曲线，统计严谨。
  - 实验3（盲智能体）进一步验证了即使在极度有限的观测下也能涌现建模，增强了结论鲁棒性。
- **公平性**：对比基线设计合理，考虑了记忆、多样性、影响力三个核心因素。伙伴生成过程确保评估伙伴完全未见，防止过拟合。

### 6. 论文的主要结论与发现

1. **伙伴建模可以自发涌现**：简单的无模型RNN智能体在仅优化协作奖励的条件下，内部隐状态发展出对伙伴任务能力的结构性表征，无需显式建模机制。
2. **涌现依赖于“影响力”**：只有当自我智能体能够影响伙伴的行为（控制任务分配）时，隐状态才显著编码伙伴能力；无影响力的RNN甚至不如单伙伴训练RNN（见图3）。
3. **在线适应能力**：在训练中经历伙伴中途切换，智能体能够动态调整任务分配，隐状态在切换后迅速转向与新伙伴匹配的表征（见图4）。
4. **盲智能体也能建模**：即使没有视觉信息，仅凭自我感知和任务奖励，RNN智能体依然能形成伙伴能力表征，并与多样伙伴有效协作。
5. **性能提升**：多伙伴RNN在总奖励和任务分配相关性上均显著优于单伙伴RNN和MLP。

### 7. 优点：方法或实验设计亮点

- **极简主义范式**：不依赖显式建模网络或辅助目标，仅靠环境压力和记忆机制，体现了“生态理性”视角。
- **清晰的因果分解**：通过对比“有/无影响力”等条件，直接证明了任务分配压力是伙伴建模涌现的必要条件。
- **多维度验证**：使用了线性探测、UMAP可视化、行为相关性分析、在线切换实验等多种手段，从表征、行为、动态适应等多角度提供证据。
- **盲智能体实验**：进一步压缩观测，排除了视觉信息作为捷径的可能性，强化了“互动结构本身”驱动建模的结论。
- **附加环境验证**：在CoinGame上复现主结果，提升了泛化性。
- **资源公开**：提供完整代码（GitHub仓库），便于复现。

### 8. 不足与局限

- **环境单一**：主实验仅基于Overcooked-AI，虽然附加了CoinGame，但仍是简单网格世界，离真实复杂协作场景有距离。
- **影响力过于直接**：自我智能体对伙伴的控制是“直接指定子任务”，人类影响力更加微妙（如通过建议、沟通等），因此该设置可能高估了涌现的条件。
- **规模限制**：仅涉及一个伙伴和一个自我智能体，未测试多伙伴场景。理论预测可以推广，但实际需求验证。
- **表征简单**：仅建模伙伴的任务速度，未涉及意图、信念、递归心智理论等高级社会认知。
- **伙伴策略固定**：伙伴是预训练+固定策略，未考虑伙伴也动态适应自我智能体的情况（类似于共同演化）。
- **未与显式建模方法直接对比**：没有比较如“Machine Theory of Mind”等显式方法在相同任务上的性能，因此无法量化隐含建模的效率损失。
- **线性探测的局限性**：探测只能反映隐状态中可线性解码的信息，可能存在更复杂的关系未被捕获。
- **潜在选择性偏差**：选择最高奖励种子进行后续分析，可能高估了模型的能力；但论文在附录中提供了5个种子的整体趋势。

（完）
