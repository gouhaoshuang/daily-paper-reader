---
title: "AgentNet: Decentralized Evolutionary Coordination for LLM-based Multi-Agent Systems"
title_zh: AgentNet：面向LLM多智能体系统的去中心化进化协调
authors: "Yingxuan Yang, Huacan Chai, Shuai Shao, Yuanyi Song, Siyuan Qi, Renting Rui, Weinan Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=tXqLxHlb8Z"
tags: ["query:eca"]
score: 7.0
evidence: 去中心化协调机制支持分布式多智能体系统
tldr: 针对现有集中式多智能体协调存在的可扩展性瓶颈和隐私问题，本文提出AgentNet，一种基于RAG的去中心化框架。该框架允许LLM智能体在有向无环图结构中自主进化能力并高效协作。实验表明其在大规模场景下优于现有集中式方法，为分布式智能体协作提供了新范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1365, \"height\": 643, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1440, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 699, \"height\": 562, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1376, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 677, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1376, \"height\": 270, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1436, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1352, \"height\": 326, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 675, \"height\": 95, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 744, \"height\": 569, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1402, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-txqlxhlb8z/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1477, \"height\": 748, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-txqlxhlb8z/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1480, \"height\": 1055, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-txqlxhlb8z/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1284, \"height\": 156, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-txqlxhlb8z/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 741, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-txqlxhlb8z/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1402, \"height\": 308, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-txqlxhlb8z/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1402, \"height\": 1379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-txqlxhlb8z/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1446, \"height\": 825, \"label\": \"Table\"}]"
motivation: 现有集中式协调方式存在可扩展性差、单点故障和隐私泄露风险。
method: 提出基于RAG的去中心化框架，智能体在有向无环图中自主进化和协作。
result: 实验显示在协作效率与可扩展性上超越传统集中式方法。
conclusion: 去中心化进化协调能有效提升多智能体系统的鲁棒性与隐私保护。
---

## Abstract
The rapid advancement of Large Language Models (LLMs) has catalyzed the development of multi-agent systems, where multiple LLM-based agents collaborate to solve complex tasks.   However, existing systems predominantly rely on centralized coordination, which introduces scalability bottlenecks, limits adaptability, and creates single points of failure.   Additionally, concerns over privacy and proprietary knowledge sharing hinder cross-organizational collaboration, leading to siloed expertise.   To address these challenges, we propose AgentNet, a decentralized, Retrieval-Augmented Generation (RAG)-based framework that enables LLM-based agents to autonomously evolve their capabilities and collaborate efficiently in a Directed Acyclic Graph (DAG)-structured network.   Unlike traditional multi-agent systems that depend on static role assignments or centralized control, AgentNet allows agents to specialize dynamically, adjust their connectivity, and route tasks without relying on predefined workflows.
AgentNet’s core design is built upon several key innovations: (1) Fully Decentralized Paradigm: Removing the central orchestrator, allowing agents to coordinate and specialize autonomously, fostering fault tolerance and emergent collective intelligence. (2) Dynamically Evolving Graph Topology: Real-time adaptation of agent connections based on task demands, ensuring scalability and resilience.
(3) Adaptive Learning for Expertise Refinement: A retrieval-based memory system that enables agents to continuously update and refine their specialized skills.
By eliminating centralized control, AgentNet enhances fault tolerance, promotes scalable specialization, and enables privacy-preserving collaboration across organizations.      Through decentralized coordination and minimal data exchange, agents can leverage diverse knowledge sources while safeguarding sensitive information.      Experimental results demonstrate that AgentNet outperforms traditional centralized multi-agent systems, significantly improving efficiency, adaptability, and scalability in dynamic environments, making it a promising foundation for next-generation autonomous, privacy-respecting multi-agent ecosystems.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

**核心问题**：现有基于大语言模型（LLM）的多智能体系统大多采用**集中式协调**架构（如AutoGen、MetaGPT），导致以下严重缺陷：
- **可扩展性瓶颈**：中央控制器处理所有任务分配，系统规模增大时性能下降。
- **单点故障风险**：中央控制器一旦失效，整个系统瘫痪。
- **适应性差**：固定角色和工作流无法动态响应实时任务需求变化。
- **隐私和跨组织协作困难**：集中式架构要求共享敏感数据和专有知识，阻碍跨企业、跨研究机构的协作，导致知识孤岛。

**整体含义**：论文提出一种**去中心化、自进化**的多智能体协调框架 AgentNet，旨在打破集中式限制，实现鲁棒、可扩展、隐私保护的分布式智能体协作，为下一代自主、隐私尊重的大规模 AI 生态系统奠定基础。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
AgentNet 基于 **检索增强生成（RAG）** 和**有向无环图（DAG）** 动态拓扑，让 LLM 智能体在无中央控制器的情况下，通过本地决策和记忆进化实现自主专业化与协作。

### 关键技术细节

- **网络定义**：系统形式化为 \( G = (A, E) \)，其中 \(A\) 为智能体集合，每个智能体 \(a_i\) 包含：
  - **Router** (\(rou_i\))：负责路由决策（转发、拆解、执行）。
  - **Executor** (\(exe_i\))：负责具体任务执行。
  - **固定容量记忆模块**：\(M^{rou}_i\)（路由记忆）和 \(M^{exe}_i\)（执行记忆），用于存储过往任务轨迹片段。

- **动态任务分配机制**：
  - 新任务到达时，根据任务需求向量 \(c_{t_{m+1}}\) 与智能体能力向量 \(cv^m_i\) 的相似度选择初始智能体：  
    \(a_{initial} = \arg\max \text{sim}(c_{t_{m+1}}, cv^m_i)\)。
  - 智能体可执行三种操作：
    - **Forward**：将任务原样转发给更合适的智能体。
    - **Split**：将任务拆解为子任务，保留擅长部分，其余路由给其他智能体。
    - **Execute**：独立完成任务。
  - 操作由 Router 基于检索的历史片段和当前上下文通过 LLM 推理决定。

- **自适应权重更新**：
  - 边权重矩阵 \(w^{m+1}(i,j) = \alpha \cdot w^m(i,j) + (1-\alpha) \cdot S(a_i, a_j, t_{m+1})\)，其中 \(S\) 为协作成功度量。
  - 低于阈值 \(\theta_w\) 的边被剪枝，保持网络高效。

- **RAG 记忆机制**：
  - 每个智能体从记忆池中检索 \(k\) 个最相关的轨迹片段，用于增强推理和决策（公式4-6）。
  - 采用**动态记忆管理**，当容量超限时自动剪除最不重要的轨迹。

- **能力向量更新**：  
  \(cv^{m+1}_i = \beta \cdot cv^m_i + (1-\beta) \cdot \Delta cv^{m+1}_i\)，反映智能体从成功执行中获得的新能力。

- **算法流程**（伪代码见附录A.1）：
  - 初始化智能体、边、权重、记忆等。
  - 对每个任务：选择初始智能体 → 循环直到任务完成或智能体被访问过 → 根据 Router 决策执行 Forward/Split/Execute → 更新边权重和拓扑 → 更新参与智能体的能力向量和记忆。

## 3. 实验设计

### 数据集与场景
- **MATH**：数学问题，7种类型，训练集700题，测试集140题。
- **BBH (Big-Bench Hard)**：逻辑问答，训练集627题（20个任务），测试集100题。
- **API-Bank**：函数调用/工具增强任务，训练集100题，测试集100题。

### Benchmark 与对比方法
- **单智能体基线**：Direct、ReAct、Synapse、Self-Consistency、Self-Refinement。
- **多智能体基线**：MorphAgent、MetaGPT、AFLOW、GPTSwarm。
- 所有多智能体方法均使用3个智能体以保证公平比较。

### 额外实验
- **异构性实验**（表2）：在BBH上测试3 agent和5 agent下完全同构、能力异构、LLM异构、两者皆异构的配置。
- **消融实验**：
  - 路由器有效性（图5）：对比完全随机、随机操作、随机下一agent、全局路由器等。
  - 进化阶段影响（表3）：对比有无进化阶段。
- **可扩展性与鲁棒性**（图6）：改变智能体数量和executor池大小。
- **网络演化可视化**（图7）、自主专门化分析（图8）。
- **案例研究**（图9-10）：对比ReAct和AgentNet在BBH上的推理轨迹。

## 4. 资源与算力

论文**未明确说明**使用的GPU型号、数量或训练时长。实验通过调用LLM API（DeepSeek-V3、GPT-4o-mini、Qwen-turbo）完成，配置温度为0.0，最大token 2048，top-p 1.0。记忆相似度计算使用 `BAAI/bge-large-en-v1.5` 模型。由于依赖外部API，实际算力消耗取决于API调用次数和输入长度，论文未提供具体估计。

## 5. 实验数量与充分性

| 类型 | 实验数量 | 充分性评价 |
|------|----------|------------|
| **主任务性能**（表1） | 3个LLM backbone × 3个任务 × 10+方法 = 90+个结果 | 全面对比了单智能体和多智能体方法，覆盖数学、逻辑、函数调用三类任务。 |
| **异构性**（表2） | 2种agent数量 × 4种异构设置 = 8个结果 | 初步探索了异构影响，但仅基于BBH，未在其他任务验证。 |
| **消融-路由**（图5） | 5种路由器变体 × 训练/测试 = 10个数据点 | 揭示了路由器设计的关键性，但仅用BBH单一任务。 |
| **消融-进化**（表3） | 2种方法 × 3个任务 = 6个结果 | 直接证明进化阶段的重要性。 |
| **可扩展性**（图6） | 多组智能体数和executor池大小组合 | 展示了系统随资源增加的性能趋势，但未在更大规模（如100+ agent）测试。 |
| **网络演化/专门化**（图7-8） | 可视化案例 | 定性展示了自组织现象，缺乏定量指标。 |

**总体评价**：实验设计较充分，涵盖主要基准和消融，对比基线合理，统计结果清晰。但存在局限：异构性实验仅测BBH；可扩展性实验未达到极大规模；缺乏对隐私保护效果的定量评估。

## 6. 主要结论与发现

- **性能优势**：AgentNet 在 MATH、BBH、API-Bank 上均达到或超过所有对比方法，尤其在逻辑推理（BBH）上以 GPT-4o-mini 为 backbone 时达86%，DeepSeek-V3 下达94%。
- **去中心化路由有效性**：完全随机路由或随机操作导致准确率大幅下降（从86%降至55%），证明路由决策至关重要。
- **进化阶段增益显著**：在 MATH、API-Bank、BBH 上，带进化机制的 AgentNet 比无进化版本分别提升7.14%、9%、10%绝对准确率。
- **异构性与规模关系**：3 agent时同构最优，5 agent时异构更优，表明异构带来的协调开销在小团队中占主导，但在大团队中收益超过成本。
- **可扩展性良好**：增加智能体数量和 executor 池可小幅提升性能（测试准确率从80%升至86%），且未见明显退化。
- **自组织与专门化**：AgentNet 智能体无需预定义角色，能在任务执行中自然形成专业化分工和高效连接。

## 7. 优点

- **完全去中心化设计**：消除单点故障，每个智能体独立决策，系统具有天然鲁棒性。
- **动态图拓扑**：边权重自适应更新与剪枝，使网络随任务需求自我优化。
- **RAG 记忆进化**：智能体通过检索历史成功轨迹持续提升能力，无需重新训练。
- **隐私保护**：仅交换最小任务元数据，敏感数据和知识本地保存，适合跨组织协作。
- **灵活的任务路由**：Forward/Split/Execute 三种操作结合能力向量匹配，实现高效的分布式任务分解与分配。
- **丰富的实验验证**：在多个基准和多种 backbone 上验证了性能，并提供消融、异构性、可扩展性等多维度分析。

## 8. 不足与局限

- **异构环境下的性能未充分探索**：仅基于 BBH 任务测试了异构性，缺乏在 MATH、API-Bank 等任务上的验证，结论泛化性有限。
- **大规模路由挑战**：当前路由从有限候选池中选择，在数百或上千智能体时，准确识别最佳 agent 的难度急剧上升，论文未提出高效的大规模路由算法。
- **探索与发现机制不足**：系统倾向于利用已知高效 agent，缺乏鼓励路由探索新智能体或新能力的激励机制。
- **计算开销分析不完整**：论文仅给出理论复杂度（\(O(km)\)），但未报告实际运行时间或 API 调用次数，难以评估实际资源消耗。
- **隐私保护效果无定量评估**：仅做定性说明，未设计实验量化隐私泄露风险或通信开销的降低。
- **依赖 LLM API 性能**：所有实验基于商业 API，结果可能随底层模型更新而变化，且未讨论成本问题。
- **应用范围受限**：主要验证于知识推理和工具调用任务，对其他类型任务（如多轮对话、物理仿真）效果未知。

（完）
