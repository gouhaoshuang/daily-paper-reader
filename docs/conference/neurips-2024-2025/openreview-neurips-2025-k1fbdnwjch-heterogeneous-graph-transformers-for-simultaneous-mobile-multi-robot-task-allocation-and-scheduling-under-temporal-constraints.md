---
title: Heterogeneous Graph Transformers for Simultaneous Mobile Multi-Robot Task Allocation and Scheduling under Temporal Constraints
title_zh: 异构图变换器用于移动多机器人任务分配与时间约束调度
authors: "Batuhan Altundas, Shengkang Chen, Shivika Singh, Shivangi Deo, Minwoo Cho, Matthew Craig Gombolay"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=k1fbdnwjCH"
tags: ["query:eca"]
score: 6.0
evidence: 移动多机器人任务分配中的异构智能体
tldr: 针对大规模异构移动机器人团队的任务分配与调度难题，本文提出基于残差异构图变换器的同步决策模型。模型通过边和节点注意力编码智能体能力与时空约束，在物流与应急响应场景中显著提升了调度效率与可扩展性，为移动智能体协同提供了有效方法。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1386, \"height\": 447, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 483, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 805, \"height\": 469, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1412, \"height\": 539, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1413, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1410, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1394, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1375, \"height\": 676, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 733, \"height\": 759, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1451, \"height\": 550, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1449, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k1fbdnwjch/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1446, \"height\": 524, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-k1fbdnwjch/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k1fbdnwjch/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1357, \"height\": 1931, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k1fbdnwjch/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 961, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k1fbdnwjch/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 924, \"height\": 2361, \"label\": \"Table\"}]"
motivation: 现有方法无法处理大规模异构移动智能体的任务依赖与时间约束。
method: 提出残差异构图变换器，通过边和节点注意力同步优化分配与调度。
result: 在模拟环境中调度性能优于传统启发式和优化方法。
conclusion: 图神经网络能有效解决移动智能体团队的复杂协同问题。
---

## Abstract
Coordinating large teams of heterogeneous mobile agents to perform complex tasks efficiently has scalability bottlenecks in feasible and optimal task scheduling, with critical applications in logistics, manufacturing, and disaster response. Existing task allocation and scheduling methods, including heuristics and optimization-based solvers, often fail to scale and overlook inter-task dependencies and agent heterogeneity. We propose a novel Simultaneous Decision-Making model for Heterogeneous Multi-Agent Task Allocation and Scheduling (HM-MATAS), built on a Residual Heterogeneous Graph Transformer with edge and node-level attention. Our model encodes agent capabilities, travel times, and temporospatial constraints into a rich graph representation and is trainable via reinforcement learning. Trained on small-scale problems (10 agents, 20 tasks), our model generalizes effectively to significantly larger scenarios (up to 40 agents and 200 tasks), enabling fast, one-shot task assignment and scheduling. Our simultaneous model outperforms classical heuristics by assigning 164.10\% more feasible tasks given temporal constraints in 3.83\% of the time, metaheuristics by 201.54\% in 0.01\% of the time and exact solver by 231.73\% in 0.03\% of the time, while achieving $20\times$-to-$250\times$ speedup from prior graph-based methods across scales.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：大规模异构移动智能体团队（如无人机、机器人）在物流、制造、灾难响应等场景中需要高效的任务分配与调度。现有方法（启发式、精确求解器、元启发式）面临可扩展性瓶颈，难以处理任务间依赖（如时间窗口、顺序约束）和智能体异构性（不同速度、执行时间）。
- **核心问题**：如何在满足时间和空间约束的前提下，实现多智能体任务的**同时**分配与调度（Simultaneous Decision-Making），并确保模型对更大规模问题具有良好的泛化能力。
- **整体含义**：提出一个基于异构图变换器（Heterogeneous Graph Transformer）的端到端学习框架——TARGETNET，将问题编码为图，通过强化学习训练，实现单次前向传播即可输出完整计划，显著提升速度与可扩展性。

### 2. 方法论
- **核心思想**：将HM-MATAS（异构移动多智能体任务分配与调度）建模为一个异构图，包含Agent、Task、Assignment、State等节点类型，以及表示异质性信息（如旅行时间、执行时间、时间窗口）的边。采用**残差异构图变换器（Residual Heterogeneous Graph Transformer）**，引入节点和边的注意力机制，同时进行任务分配（哪个智能体执行哪个任务）和调度（任务执行的顺序）。
- **关键技术细节**：
  - **图表示**：每个Assignment节点表示一个(Agent, Task)对，边编码异构旅行时间和执行时间。总节点数O(|A||T|)，边数O(|A||T|²)。
  - **消息传递**：在HGT基础上增加边注意力与边消息（Eq. 2-5），利用分配律将边特征与节点特征结合更新节点表示，并更新边特征。使用多头注意力但不使用softmax归一化（允许注意力权重为零，增强灵活性）。
  - **残差连接**：采用graph-raw残差，将初始输入特征附加到每一层，缓解深层GNN的梯度消失。
  - **同时决策策略**：单次前向传播得到任务分配矩阵（通过Assignment节点输出）和调度顺序（通过Task Order节点输出）。训练使用REINFORCE算法，奖励结合密集可行性奖励和稀疏最终性能奖励（Eq. 1, 6）。
- **算法流程**（文字说明）：
  - 输入初始状态，构建图。
  - GNN编码，输出任务分配logits和调度logits。
  - 对每个任务，从调度logits中采样顺序，并根据分配logits采样负责的智能体。
  - 执行动作，获得奖励；累积轨迹后更新策略参数。

### 3. 实验设计
- **数据集/场景**：合成生成四种规模的问题：
  - 小型：10智能体，20任务
  - 中型：10智能体，50任务
  - 大型：20智能体，100任务
  - 超大型：40智能体，200任务
  所有实例均通过MILP验证存在可行解。约束包括随机时间窗口（0-10%）、25%任务有等待时间约束等。
- **Benchmark**：对比方法包括：
  - 精确求解器：MILP（Gurobi，12小时限制）
  - 启发式：EDF、Constraint-Aware EDF
  - 元启发式：遗传算法（Gen-Random, Gen-EDF，1或3代）
  - 基于GNN的序列模型：HetGAT、Res-HetGAT、序列版TARGETNET及其消融变体
  - 同时决策消融版：去除残差/边特征等
- **评估指标**：最优性率（相对MILP）、可行任务分配百分比、训练/推理时间。

### 4. 资源与算力
- 论文明确说明：小到大规模实验在 **Mac Studio（Apple M1芯片，32GB RAM）**上完成；超大规模实验在 **AMD EPYC 7452处理器（Ubuntu 20.04.6）** 的高性能服务器上运行。**未提及GPU型号或具体训练时长**，但给出了训练时间对比图（Fig. 6b），显示每episode训练时间对比。
- 所有学习模型仅在小规模问题上训练（200个实例），然后在更大规模上测试泛化能力。

### 5. 实验数量与充分性
- 实验数量：每个对比方法以3个不同随机种子运行，报告最佳种子结果（应对策略敏感性问题）。测试集规模：小/中200个问题，大30个，超大10个。消融实验包括5种同时决策变体（去除残差/边特征/两者），以及序列模型变体。额外进行了**灵敏度分析**：变化时间窗口宽度、等待时间概率、智能体速度三种约束。
- 充分性评价：实验覆盖多尺度、多基线、多种约束变化，且统计了均值和标准差，结果较为可靠。但**仅在模拟环境中验证**，缺乏真实机器人平台的大规模测试（仅附录H有Robotarium小规模演示）。对比的MILP在超大尺度只能返回部分可行解，这限制了最优性比较的全面性。

### 6. 主要结论与发现
- TARGETNET（同时决策+残差+边注意力）在所有规模上**显著优于非学习基线**：比启发式多分配164.10%可行任务，时间只需3.83%；比元启发式多分配201.54%，时间仅0.01%；比MILP精确求解器多分配231.73%，时间仅0.03%（超大尺度12小时后MILP仅获得部分解）。
- 训练于小规模，可直接**泛化到40智能体200任务的超大问题**，无需重新训练。
- 推理速度：相比序列GNN方法（如HetGAT）快20–250倍，同时保持相当或更好的最优性。
- 消融实验证实**边注意力**和**残差连接**对性能稳定性和泛化能力至关重要：无边特征或残差的变体性能显著下降且方差更大。

### 7. 优点
- **创新性**：首次在移动多智能体任务分配与调度中实现**同时决策**，通过单次前向传播完成分配和排序，显著降低复杂度。
- **模型设计**：边注意力机制使模型能有效利用异构旅行时间和执行时间等关键关系信息；残差连接使深度网络训练稳定。
- **高效可扩展**：训练在小型问题上，泛化到10倍大的问题，推理时间仅毫秒级，适合实时应用。
- **实验完备**：与多种先进方法对比，且进行了充分的消融和灵敏度分析，验证各组件贡献。

### 8. 不足与局限
- **动态环境缺失**：模型假设静态预计算的运动规划，未考虑智能体间碰撞避免和环境实时变化，可能导致实际执行偏差。
- **可解释性不足**：作为图神经网络，策略内部机制不透明，在安全关键任务中难以验证。
- **实验局限**：所有实验均为模拟合成数据，缺乏真实机器人或物理测试（仅附录有小规模Robotarium演示，且未计入正式对比）。超大规模问题的MILP基准不完整（部分解），影响完全公平的比较。
- **训练不确定性**：模型对随机种子敏感，需要多个种子并选取最佳结果，表明训练稳定性仍有改进空间。
- **忽略多智能体路径冲突**：调度未考虑路径交叉造成的延迟，未来需集成碰撞避免。

（完）
