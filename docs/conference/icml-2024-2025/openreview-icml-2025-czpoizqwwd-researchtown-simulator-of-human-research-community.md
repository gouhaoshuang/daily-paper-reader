---
title: "ResearchTown: Simulator of Human Research Community"
title_zh: ResearchTown：人类研究社区的模拟器
authors: "Haofei Yu, Zhaochen Hong, Zirui Cheng, Kunlun Zhu, Keyang Xuan, Jinwei Yao, Tao Feng, Jiaxuan You"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=CZPOIZqWwd"
tags: ["query:eca"]
score: 5.0
evidence: 模拟研究社区协作关系的多智能体框架
tldr: 现有模拟研究社区的尝试缺乏对学术协作网络的细粒度建模。本文提出ResearchTown，将研究人员和论文分别建模为代理节点和数据节点，并基于协作关系构建图结构。引入TextGNN进行文本推理，成功模拟了研究社区中的对话、审稿等交互过程。实验表明该框架能有效复现人类研究社区的动态特征，为理解科学发现过程提供新工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-czpoizqwwd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1499, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-czpoizqwwd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1407, \"height\": 435, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-czpoizqwwd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 536, \"height\": 354, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-czpoizqwwd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 538, \"height\": 356, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-czpoizqwwd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 549, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-czpoizqwwd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1764, \"height\": 420, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 865, \"height\": 261, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 844, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 858, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 846, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1760, \"height\": 1056, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1315, \"height\": 788, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1371, \"height\": 2258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1375, \"height\": 1582, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1391, \"height\": 928, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1383, \"height\": 1332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1383, \"height\": 1407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1380, \"height\": 1740, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1378, \"height\": 795, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1376, \"height\": 798, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1367, \"height\": 1092, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1389, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1368, \"height\": 1446, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1676, \"height\": 1661, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1680, \"height\": 1690, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1680, \"height\": 1688, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1678, \"height\": 1688, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1691, \"height\": 2252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1691, \"height\": 1530, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1695, \"height\": 1470, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1694, \"height\": 1531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1694, \"height\": 1587, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1693, \"height\": 1504, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1696, \"height\": 1587, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1695, \"height\": 1683, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1696, \"height\": 1614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1694, \"height\": 1682, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-czpoizqwwd/table-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 1697, \"height\": 1705, \"label\": \"Table\"}]"
motivation: 缺乏能够模拟人类研究社区协作动态的LLM框架。
method: 构建代理-数据图，研究人员和论文作为节点，基于协作关系连接并引入TextGNN。
result: 成功模拟了包括对话、审稿在内的研究社区交互，复现了真实协作模式。
conclusion: ResearchTown为自动发现科学见解和理解研究过程提供了有效平台。
---

## Abstract
Large Language Models (LLMs) have demonstrated remarkable potential in scientific domains, yet a fundamental question remains unanswered: Can we simulate human research communities with LLMs? Addressing this question can deepen our understanding of the processes behind idea brainstorming and inspire the automatic discovery of novel scientific insights. In this work, we propose ResearchTown, a multi-agent framework for research community simulation. Within this framework, the human research community is simplified as an agent-data graph, where researchers and papers are represented as agent-type and data-type nodes, respectively, and connected based on their collaboration relationships. We also introduce TextGNN, a text-based inference framework that models various research activities (e.g., paper reading, paper writing, and review writing) as special forms of a unified message-passing process on the agent-data graph. To evaluate the quality of the research community simulation, we present ResearchBench, a benchmark that uses a node-masking prediction task for scalable and objective assessment based on similarity. Our experiments reveal three key findings: (1) ResearchTown can provide a realistic simulation of collaborative research activities, including paper writing and review writing; (2) ResearchTown can maintain robust simulation with multiple researchers and diverse papers; (3) ResearchTown can generate interdisciplinary research ideas that potentially inspire pioneering research directions.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：能否利用大语言模型（LLM）模拟人类研究社区？这是一个根本性但尚未回答的问题。
- **动机**：模拟人类研究社区有助于深入理解研究思想的发现过程，并可能自动激发新的科学洞察，从而加速科学发现。
- **背景**：现有的多智能体LLM框架（如社交模拟、游戏模拟）难以处理研究活动的复杂性（如论文写作、审稿等协作过程），而其他单智能体研究自动化系统无法模拟多研究者合作的动态。

## 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

### 核心思想
- 将研究社区抽象为**代理-数据图**（Agent-Data Graph）：研究人员作为**代理节点**，论文作为**数据节点**，节点间通过协作关系（作者、引用、审稿等）连接。
- 提出**TextGNN**，一种基于文本的消息传递框架，将研究活动（论文阅读、论文写作、审稿写作）建模为图上的统一消息传递过程。

### 关键技术细节
- **代理-数据图定义**：异构图 \(G = (V, E)\)，其中 \(V = V_a \cup V_d\)（agent节点和数据节点），\(E = E_{aa} \cup E_{ad} \cup E_{dd}\)。数据节点有文本属性，agent节点有agent函数（LLM+提示模板）。
- **TextGNN消息传递**：所有隐藏状态为文本形式。标准GNN的公式被改编为文本聚合：
  - agent节点更新：\(h_u^{(k)} = \text{AGG}(f_u(\cdot), h_u^{(k-1)}, \{h_d^{(k-1)}\}, \{f_a(\cdot), h_a^{(k-1)}\})\)
  - 数据节点更新：\(h_v^{(k)} = \text{AGG}(h_v^{(k-1)}, \{h_d^{(k-1)}\}, \{f_a(\cdot), h_a^{(k-1)}\})\)
- **三个关键阶段**：
  1. **论文阅读**（Stage 1）：新agent节点插入，聚合邻域论文信息生成角色描述。
  2. **论文写作**（Stage 2）：新数据节点插入，基于agent和引用论文生成论文内容（五点问题格式）。
  3. **审稿写作**（Stage 3）：新数据节点插入，基于论文内容、引用和agent生成审稿意见（优缺点+评分）。
- **算法流程**：整体可视为2层GNN，第一层为论文阅读，第二层为论文写作和审稿写作。具体见Algorithm 1。

## 3. 实验设计：数据集、Benchmark、对比方法

- **Benchmark**：提出**ResearchBench**，包含1,000个论文写作任务和200个审稿写作任务。
  - 数据来源：NeurIPS 2024和ICLR 2024论文，确保GPT-4o-mini知识截止日期后，避免信息泄露。
  - 论文写作任务按难度分为**Hard**（333）、**Medium**（334）、**Easy**（333），基于数据聚合结果划分。
  - 审稿写作任务中，评委通过检索论文最相关的前5名研究者（排除作者）确定。
- **对比方法**：四种聚合策略：
  - **AGG-self**：仅目标节点
  - **AGG-agent**：目标节点+邻接agent节点
  - **AGG-data**：目标节点+邻接数据节点
  - **AGG-global**（即ResearchTown）：所有邻接节点
- **生成模型**：GPT-4o-mini（主要）、Qwen-2.5-7B-Instruct、Deepseek-v3
- **嵌入模型**：text-embedding-3-large（主要）、voyage-3
- **评估指标**：嵌入余弦相似度（论文写作：五点问题平均分；审稿写作：Recall式最大相似度+评分差ΔS）；LLM-as-judge细粒度评估；人类评估（40样本）。

## 4. 资源与算力

- **未明确说明**：论文未提供使用的GPU型号、数量、训练时长等信息。
- 仅提到使用GPT-4o-mini、Qwen-2.5-7B-Instruct、Deepseek-v3的API，以及OpenAI/VoyageAI的嵌入服务。所有计算均通过API调用完成，未报告具体耗时或硬件配置。

## 5. 实验数量与充分性

- **实验数量**：丰富且系统。
  - 核心结果：表1（论文写作，4种聚合×3难度×整体）、表2（审稿写作，4种聚合×优缺+ΔS）。
  - 不同生成模型：表3（三种模型×聚合策略）
  - 消融实验：论文数量影响（图3）、代理数量影响（图4、图5）、不同嵌入模型（voyage-3对比）
  - 额外评估：LLM-as-judge细粒度相似度（图6）、新颖性和可行性（表4）、人类评估（40样本）
  - 案例分析：跨学科生成（表23-32多个组合）
- **充分性**：实验覆盖多种聚合策略、多个模型、多个难度、多种评估方式，对比充分（baseline包括自聚合、仅代理、仅数据）。消融实验验证了超参数鲁棒性。
- **客观性**：使用嵌入相似度、LLM评判、人类评判三重视角，大部分结果一致。但人类评估样本量较小（40），且与LLM在新颖性可行性上相关性低。

## 6. 论文的主要结论与发现

1. **ResearchTown能提供真实的研究活动模拟**：论文写作平均相似度0.68，审稿写作0.49（strength 0.51, weakness 0.47）。Easy子集更高（0.74）。
2. **多研究者协作改善质量**：论文写作中，加入邻接论文和数据（AGG-global）比纯数据聚合提升2.21分；尤其在Hard场景提升显著（56→61）。审稿写作中多审稿人也有帮助。
3. **ResearchTown能生成跨学科研究想法**：案例显示，组合NLP+天文学、NLP+犯罪学等产生新颖研究问题（如用运动学模型分析语言演化）。
4. **鲁棒性**：改变论文数量、代理数量、生成模型、嵌入模型，趋势一致，表明框架稳定。
5. **生成内容质量略低于真实论文**：新颖性（7.39 vs 7.85）和可行性（6.82 vs 7.13）仍有差距。

## 7. 优点

- **图结构自然建模**：代理-数据图简洁且可扩展，能表达研究者与数据之间的复杂关系。
- **TextGNN统一活动建模**：将论文阅读、写作、审稿统一为消息传递，便于扩展。
- **节点掩码预测评估**：利用图结构实现客观、可扩展的相似度评估，避免主观性。
- **跨学科生成能力**：通过组合不同领域研究者，自动生成未在真实文献中出现的新颖交叉研究思路。
- **多维度评估**：嵌入相似度、LLM细粒度评估、人类评估，提高结论可信度。
- **伦理讨论**：明确讨论了防止抄袭、低质量输出、冒充研究者等问题，并提出了缓解措施。

## 8. 不足与局限

- **审稿模拟较弱**：审稿写作相似度远低于论文写作（0.49 vs 0.68），尤其是弱项识别较差，可能与真实审稿噪声大有关。
- **生成内容质量有限**：自动评估显示新颖性和可行性低于真实论文，人类评估也发现灵感不足。
- **跨学科组合过多时效果不佳**：例如结合LLM、生物学、犯罪学、天文学等多个领域时，生成内容变成术语堆砌，缺乏焦点。
- **依赖专有LLM API**：主要实验基于GPT-4o-mini，且未说明计算成本，可能限制可重复性。
- **人类评估样本量小**：仅40个样本，且与LLM评估在内在质量上相关性低，可能不够可靠。
- **信息泄露风险**：尽管论文声称使用最新会议论文避免，但高影响力论文基准（HIGH IMPACT PAPER BENCH）中部分经典论文可能已被LLM训练数据包含，不过作者分析显示未导致异常高分。
- **框架设计简化**：省略了agent-agent边（如合作沟通），可能遗漏一些社会动态。
- **输出格式受限**：论文写作仅输出五点问题答案，不包含完整论文（引言、实验等），不能直接用于出版。

（完）
