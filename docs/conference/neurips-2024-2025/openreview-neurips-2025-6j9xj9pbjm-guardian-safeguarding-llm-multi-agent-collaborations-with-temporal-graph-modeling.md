---
title: "GUARDIAN: Safeguarding LLM Multi-Agent Collaborations with Temporal Graph Modeling"
title_zh: GUARDIAN：基于时序图建模的LLM多智能体协作安全防护
authors: "Jialong Zhou, Lichao Wang, Xiao Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=6j9xJ9pBjm"
tags: ["query:eca"]
score: 9.0
evidence: "直接针对多智能体协作的安全问题，契合用户需求'协作'"
tldr: 大型语言模型驱动的多智能体协作面临幻觉放大和错误传播等安全挑战。GUARDIAN提出将协作过程建模为离散时间时序属性图，通过无监督编码器-解码器架构与增量训练范式，学习重构节点属性，从而统一检测与缓解多种安全问题。实验表明该方法能有效捕捉幻觉和错误的传播动态，保障多智能体系统的安全运行。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1415, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1282, \"height\": 660, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1437, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1456, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 710, \"height\": 310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 570, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1416, \"height\": 1953, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1415, \"height\": 2364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6j9xj9pbjm/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1419, \"height\": 2081, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1447, \"height\": 630, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1435, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 688, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 656, \"height\": 241, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 719, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1153, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1184, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1191, \"height\": 1209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1090, \"height\": 1302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1191, \"height\": 619, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 697, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1442, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1444, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1444, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 699, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 700, \"height\": 424, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6j9xj9pbjm/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 700, \"height\": 425, \"label\": \"Table\"}]"
motivation: 多智能体协作存在幻觉放大和错误注入传播等安全隐患，亟需统一的安全检测与缓解方法。
method: 将多智能体协作建模为离散时间时序属性图，采用无监督编码器-解码器架构结合增量训练学习节点属性重构。
result: 该方法能显式捕捉幻觉和错误的传播动态，有效检测并缓解多种安全问题。
conclusion: GUARDIAN为多智能体协作提供了一种统一的安全防护框架。
---

## Abstract
The emergence of large language models (LLMs) enables the development of intelligent agents capable of engaging in complex and multi-turn dialogues. However, multi-agent collaboration faces critical safety challenges, such as hallucination amplification and error injection and propagation. This paper presents GUARDIAN, a unified method for detecting and mitigating multiple safety concerns in GUARDing Intelligent Agent collaboratioNs. By modeling the multi-agent collaboration process as a discrete-time temporal attributed graph, GUARDIAN explicitly captures the propagation dynamics of hallucinations and errors. The unsupervised encoder-decoder architecture incorporating an incremental training paradigm learns to reconstruct node attributes and graph structures from latent embeddings, enabling the identification of anomalous nodes and edges with unparalleled precision. Moreover, we introduce a graph abstraction mechanism based on the Information Bottleneck Theory, which compresses temporal interaction graphs while preserving essential patterns. Extensive experiments demonstrate GUARDIAN's effectiveness in safeguarding LLM multi-agent collaborations against diverse safety vulnerabilities, achieving state-of-the-art accuracy with efficient resource utilization. The code is available at https://github.com/JialongZhou666/GUARDIAN.

---

## 论文详细总结（自动生成）

# GUARDIAN: Safeguarding LLM Multi-Agent Collaborations with Temporal Graph Modeling 中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **安全挑战**：大语言模型（LLM）驱动的多智能体协作在提升复杂任务解决能力的同时，面临两类关键安全问题：
  - **幻觉放大**：一个智能体产生的非事实信息在网络中传播并放大。
  - **错误注入与传播**：恶意智能体通过篡改系统提示（agent-targeted attack）或拦截通信（communication-targeted attack）注入错误，导致错误在网络中扩散。
- **现有方法不足**：
  - 协作错误检测方法（如交叉检验、外部反馈）只关注单个输出，未建模传播动态。
  - 多数投票或不确定性估计简化了智能体依赖关系，且需要修改基础模型，不适用于闭源模型。
- **本文目标**：提出一种统一的方法（GUARDIAN）来检测和缓解多种安全问题，无需修改LLM本身，模型无关。

## 2. 论文提出的方法论
### 核心思想
- 将多智能体协作过程建模为**离散时间时序属性图**：
  - **节点**：每个时间步每个智能体对应一个节点，节点属性使用BERT对智能体响应进行嵌入。
  - **边**：相邻时间步之间表示通信的有向边。
  - 通过图结构显式捕捉幻觉和错误的传播动态。

### 关键技术细节
- **无监督编码器-解码器架构**：
  - **属性图编码器**：使用GCN聚合邻居信息，学习节点嵌入。
  - **时间信息编码器**：基于Transformer处理历史图嵌入序列，动态加权历史模式生成当前时间步表示。
  - **属性重构解码器**：从嵌入重建节点属性，计算重建误差（MSE）检测属性异常。
  - **结构重构解码器**：重建邻接矩阵，计算结构重建误差（BCE）检测结构异常。
- **图抽象机制（信息瓶颈理论）**：最小化 \( L_{GIB} = I(X_t; Z_t) - \beta I(Z_t; Y_t) \)，压缩冗余信息同时保留任务相关模式。
- **增量训练范式**：按时间顺序处理交互图，利用先前时间步训练当前步，每轮移除已检测的异常节点，逐步积累正常行为知识。

### 损失函数
- 总损失：\( L_{total} = L_{rec} + \lambda L_{GIB} \)，其中 \( L_{rec} = \alpha L_{att} + (1-\alpha)L_{stru} \)。

### 理论保证
- 定理证明智能体间信息流有界（可控压缩率），时间状态转移受先验约束，防止级联放大。

## 3. 实验设计
### 数据集与场景
- **数据集**：MMLU（多学科知识）、MATH（数学推理）、FEVER（事实验证）、Biographies（传记生成）。
- **安全场景**：
  1. 幻觉放大（Hallucination Amplification）。
  2. Agent-targeted 错误注入与传播。
  3. Communication-targeted 错误注入与传播。
- **基准方法**：
  - 基础框架：LLM Debate、DyLAN。
  - 幻觉检测：SelfCheckGPT。
  - 错误检测：Challenger、Inspector。
- **LLM后端**：GPT-3.5-turbo、GPT-4o、Claude-3.5-sonnet、Llama3.1-8B。
- **评估指标**：模型准确率、异常检测率、错误发现率（FDR）、API调用次数、运行时间。

### 实验设置
- 每个数据集随机抽样100个问题，三次独立测试。
- 默认4个智能体，额外实验3-7个智能体。
- 稀疏拓扑测试（25%、50%、75%连接）。
- 消融实验：参数α（属性-结构平衡）、γ（压缩-相关权衡）。

## 4. 资源与算力
- 论文**未明确说明**所使用的GPU型号、数量或训练时长。
- 提及使用闭源模型API（GPT-3.5-turbo、GPT-4o、Claude-3.5-sonnet）和开源模型（Llama3.1-8B），运行成本以API调用次数和运行时间（秒/问题）衡量。
- 因此，无法获得具体的算力配置信息。

## 5. 实验数量与充分性
- **实验数量**：
  - 主对比表（Table 1）：涵盖3种安全场景×3个数据集×3种LLM后端×6种方法，共>50组结果。
  - 额外实验：Biographies实验结果、不同agent数量（3-7）的准确率与API调用（Table 7）、稀疏拓扑（Table 3）、异常检测率（Table 6）、FDR（Table 2）、消融（Figure 6）、运行时间（Table 5）、Llama3.1-8B结果（Table 8）等。
  - 总计超过10张表格，多组消融和分析。
- **充分性与公平性**：
  - 实验覆盖了多数据集、多LLM、多安全场景，且对比了多种基线方法，包括无防御和有防御方法。
  - 消融实验验证了关键组件的作用。
  - **不足**：未报告误差线或置信区间；未在更大规模智能体（如>7）上测试；只针对in-distribution场景（同一数据集内增量训练），未讨论跨分布泛化。

## 6. 论文的主要结论与发现
- GUARDIAN在幻觉放大、agent-targeted错误注入、communication-targeted错误注入三大场景下，**准确率普遍超过所有基线**，平均提升约4-7%，尤其在MATH数据集上提升显著（最高15.4%）。
- **异常检测率高**：平均>80%，最高达94.74%。
- **误警率（FDR）较低**：大部分场景低于20%，MATH上仅8.32%。
- **资源效率高**：API调用次数最低（相比DyLAN等更少），运行时间最短或接近最短，远超SelfCheckGPT、Inspector等高开销方法。
- 拓扑鲁棒性：在稀疏连接下仍保持优势。
- 消融表明：α在0.3-0.5、γ在0.001-0.01之间取得最佳平衡。

## 7. 优点
- **统一检测多种安全问题**：同时处理幻觉放大和两类错误注入，无需为每种问题单独设计方法。
- **模型无关**：不修改底层LLM，适用于闭源和开源模型。
- **可解释性**：时序图表示自然可视化信息传播路径，帮助定位异常源。
- **理论支撑**：信息瓶颈理论提供信息流上界，防止级联放大。
- **增量训练适应动态环境**：逐步移除异常节点，保持检测能力随交互演变。
- **资源友好**：通过节点删除减少后续API调用和运行时间，总体成本低。

## 8. 不足与局限
- **运行时开销**：虽然优于多数基线，但比LLM Debate略高（尤其在MATH任务上，平均多约5秒）。
- **误删风险**：存在一定FDR（最高30.67%），错误移除正确智能体会降低协作质量，尽管冗余智能体可部分补偿。
- **实验规模有限**：agent数量仅到7，未验证更大规模（如数十个agent）下的性能和通信瓶颈。
- **未讨论长对话或轮次很多的场景**：实验最多3-4轮，长时间交互中增量训练的遗忘问题或异常积累未被评估。
- **缺乏统计误差报告**：未提供标准差或置信区间，结果稳健性需进一步验证。
- **in-distribution假设**：增量训练在同一数据集内进行，跨分布迁移能力未测试。

（完）
