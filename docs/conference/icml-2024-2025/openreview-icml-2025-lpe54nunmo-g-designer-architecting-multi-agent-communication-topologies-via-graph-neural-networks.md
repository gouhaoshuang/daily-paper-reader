---
title: "G-Designer: Architecting Multi-agent Communication Topologies via Graph Neural Networks"
title_zh: G-Designer：基于图神经网络构建多智能体通信拓扑
authors: "Guibin Zhang, Yanwei Yue, Xiangguo Sun, Guancheng Wan, Miao Yu, Junfeng Fang, Kun Wang, Tianlong Chen, Dawei Cheng"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=LpE54NUnmO"
tags: ["query:eca"]
score: 8.0
evidence: 面向分布式系统的动态多智能体通信拓扑设计
tldr: 多智能体系统通信拓扑的选择至关重要但缺乏自动化方法。本文提出G-Designer，利用图神经网络动态生成任务感知的个性化通信拓扑。实验表明，G-Designer在多种任务中降低了通信开销并提升了质量。该方法可直接应用于分布式边缘云智能体架构的拓扑设计，实现高效协作。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 822, \"height\": 472, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 853, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1762, \"height\": 1031, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 841, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 852, \"height\": 301, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 494, \"height\": 202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 117, \"height\": 143, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 107, \"height\": 143, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 623, \"height\": 224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 515, \"height\": 202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lpe54nunmo/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 515, \"height\": 239, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-lpe54nunmo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 884, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lpe54nunmo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lpe54nunmo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lpe54nunmo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1307, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lpe54nunmo/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 661, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lpe54nunmo/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 907, \"height\": 1023, \"label\": \"Table\"}]"
motivation: 多智能体系统的通信拓扑选择困难，需要自适应且任务导向的设计方法。
method: 提出G-Designer，利用图神经网络动态生成任务感知的个性化通信拓扑。
result: 在多种多智能体任务中，G-Designer在降低通信开销的同时提升了任务完成质量。
conclusion: 自适应拓扑设计可有效平衡通信效率与性能，适用于分布式边缘云智能体架构。
---

## Abstract
Recent advancements in large language model (LLM)-based agents have demonstrated that collective intelligence can significantly surpass the capabilities of individual agents, primarily due to well-crafted inter-agent communication topologies. Despite the diverse and high-performing designs available, practitioners often face confusion when selecting the most effective pipeline for their specific task: \textit{Which topology is the best choice for my task, avoiding unnecessary communication token overhead while ensuring high-quality solution?} In response to this dilemma, we introduce G-Designer, an adaptive, efficient, and robust solution for multi-agent deployment, which dynamically designs task-aware, customized communication topologies. Specifically, G-Designer models the multi-agent system as a multi-agent network, leveraging a variational graph auto-encoder to encode both the nodes (agents) and a task-specific virtual node, and decodes a task-adaptive and high-performing communication topology. Extensive experiments on six benchmarks showcase that G-Designer is: \textbf{(1) high-performing}, achieving superior results on MMLU with accuracy at $84.50\\%$ and on HumanEval with pass@1 at $89.90\\%$; \textbf{(2) task-adaptive}, architecting communication protocols tailored to task difficulty, reducing token consumption by up to $95.33\\%$ on HumanEval; and \textbf{(3) adversarially robust}, defending against agent adversarial attacks with merely $0.3\\%$ accuracy drop.

---

## 论文详细总结（自动生成）

# 论文总结：G-Designer: Architecting Multi-agent Communication Topologies via Graph Neural Networks

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：基于大语言模型（LLM）的多智能体系统通过精心设计的通信拓扑能够显著超越单个智能体的能力。然而，现有的多智能体拓扑设计（如链式、星型、树型、完全图、随机图等）多为静态或输入无关，无法针对具体任务动态调整，导致实践中面临“该用哪种拓扑”的困扰：简单任务使用复杂结构浪费令牌（token），复杂任务使用简单结构性能不足。
- **核心问题**：如何为给定任务自动设计任务感知、高效且鲁棒的多智能体通信拓扑，在保证高质量解决方案的同时最小化通信开销。
- **整体含义**：本文提出首个面向LLM多智能体系统的通信协议（MACP），并设计了自适应拓扑生成器G-Designer，旨在实现多智能体协作的自动化、高效化和鲁棒化，推动集体智能的发展。

## 2. 方法论：核心思想、关键技术细节、算法流程

- **核心思想**：将多智能体系统建模为图，智能体作为节点，通信作为边。使用变分图自编码器（VGAE）编码智能体节点特征和任务特定虚拟节点，解码得到任务自适应的稀疏通信拓扑。
- **关键技术细节**：
  - **多智能体网络构建**：
    - 每个智能体由LLM底座、角色、状态、外部插件组成，通过轻量文本嵌入模型（如all-MiniLM-L6-v2）编码为特征向量。
    - 引入一个与所有智能体双向连接的任务特定虚拟节点，编码任务查询信息。
    - 提供锚定拓扑（anchor topology，默认为链式结构）作为先验。
  - **通信拓扑设计**：
    - 编码器：使用两层GCN从多智能体网络（含虚拟节点）中学习潜在表示。
    - 解码器分两步：
      - 第一步（草图生成）：基于潜在表示和虚拟节点，通过FFN和Gumbel-Sigmoid技巧生成稠密非负草图矩阵S。
      - 第二步（精炼）：通过锚定正则化和稀疏正则化（核范数最小化）将S精炼为稀疏的最终通信拓扑G_com。
  - **优化配置**：采用策略梯度优化不可导的目标。总损失函数包括效用损失、锚定正则化损失和稀疏正则化损失。仅用少量训练查询（40~80条）即可泛化到新任务。
- **算法流程**（文字描述）：
  1. 对输入查询，构建多智能体网络：编码各智能体特征，添加虚拟节点，设定锚定拓扑。
  2. 变分图自编码器编码网络，经解码两步生成稀疏通信图G_com。
  3. 根据G_com的拓扑执行K轮多智能体对话，聚合得到最终答案。
  4. 基于效用反馈，使用策略梯度更新编码器和解码器参数。

## 3. 实验设计

- **数据集与场景**：
  - 通用推理：MMLU（多选问答）
  - 数学推理：GSM8K、MultiArith、SVAMP、AQuA
  - 代码生成：HumanEval
- **Benchmark**：以准确率（MMLU）、Pass@1（HumanEval）等为指标。
- **对比方法**：
  - 单智能体：Vanilla、CoT、ComplexCoT、Self-Consistency、PHP
  - 多智能体拓扑：Chain、Star、Tree、Complete Graph、Random Graph
  - 先进多智能体框架：AutoGen、MetaGPT、LLM-Debate、LLM-Blender、DyLAN、GPTSwarm
- **实现细节**：主要使用gpt-4和gpt-3.5-turbo，温度设为0（单次执行）或1（多智能体）。K=3次对话，使用all-MiniLM-L6-v2作为编码器，维度384，锚定拓扑为链式，采样次数M=10，温度τ=1e-2，稀疏系数ζ=1e-1。

## 4. 资源与算力

- 论文中明确提到了训练的资源消耗：
  - **GPU内存**：训练G-Designer代理数从5到1000时，GPU内存需求仅2.7~3.8 GB（见表5）。
  - **训练令牌消耗**：在GSM8K上，G-Designer训练令牌仅2.7×10^5，远低于DyLAN的9.6×10^6和GPTSwarm的5.5×10^6。
  - **训练时间**：GSM8K上训练时间0.3小时，而DyLAN需2.8小时，GPTSwarm需2.1小时。
- **未说明的具体GPU型号**，仅提及其它方法（GPTSwarm等）运行于类似环境。

## 5. 实验数量与充分性

- **实验组数**：共开展六大类实验：
  - 主实验结果（表1）：6个数据集，对比15+种方法。
  - 令牌消耗与性能可视化（图4）：4个数据集下的多方法对比。
  - 可扩展性实验（表6）：5/10/20个智能体规模下的性能、时间、令牌、成本对比。
  - 鲁棒性分析（图5）：对5个智能体中的一个实施系统提示攻击，对比7种方法攻击前后的准确率。
  - 消融实验（表3）：移除稀疏正则化、锚定、节点编码器、虚拟节点共4个变体，测试MMLU和GSM8K清洁与攻击下性能。
  - 案例研究（图6）：可视化HumanEval和GSM8K上拓扑的复杂度适应性。
- **充分性与客观性**：
  - 覆盖多种任务类型（通用、数学、代码），对比基线全面，包含单智能体与多智能体方法。
  - 消融实验验证了各组件的贡献，鲁棒性实验验证了防御能力。
  - 实验设置公平（所有多智能体方法使用相同5个gpt-4代理），但缺少在更多基座模型（如Llama）上的验证，且在更大规模智能体（>20）上的实验不充分。

## 6. 主要结论与发现

- **高效性**：G-Designer在6个基准的5个上取得最优，平均准确率89.84%，超越GPTSwarm（87.32%）和DyLAN（85.64%）。在HumanEval上Pass@1达89.9%，超越MetaGPT。
- **任务自适应**：能够根据任务复杂度动态调整拓扑：简单任务使用极简图（如只有2个节点），复杂任务使用更密集的图。令牌消耗降低高达95.33%（HumanEval），在MMLU上令牌消耗仅1.5e+5，而DyLAN需2.6e+6。
- **鲁棒性**：面对单个代理的提示攻击，准确率仅下降0.3%，而DyLAN下降6.2%，AutoGen下降9.9%。
- **可扩展性**：在20个智能体时，性能超过GPTSwarm 2.44%，令牌消耗仅为GPTSwarm的6.11%。
- **训练高效**：仅需40~80条训练查询即可泛化，资源消耗极低（<4GB GPU内存）。

## 7. 优点

- **创新性**：首次提出面向LLM多智能体系统的通信协议（MACP），并设计变分图自编码器实现任务自适应的拓扑生成，突破了静态拓扑的局限性。
- **全面性**：同时考虑了性能、效率、鲁棒性三个维度，实验验证充分，指标覆盖准确率、令牌消耗、训练成本、攻击防御。
- **实用性**：训练只需少量查询，GPU内存需求小，可直接部署；代码开源。
- **可解释性**：通过案例可视化展示了不同难度任务的定制拓扑，说明模型能意识到任务复杂度。

## 8. 不足与局限

- **基座模型单一**：主要实验使用gpt-4和gpt-3.5，未在开源模型（如Llama系列）上验证泛化性。
- **智能体规模有限**：最大实验规模为20个智能体，未见更大规模（如50/100）下的性能与效率分析，尽管GPU内存测试到1000节点，但实际对话实验未扩展。
- **训练数据依赖**：需要少量训练查询进行优化，在完全零样本情景下的能力未讨论。
- **拓扑生成的计算开销**：虽训练成本低，但每次推理时仍需运行图编码-解码过程，对于极其轻量的任务，该开销可能不必要。
- **鲁棒性测试简化**：仅考虑单智能体提示攻击，未深入探讨多智能体联合攻击或攻击后拓扑动态调整的细节。
- **应用限制**：方法依赖文本嵌入模型对智能体特征和任务描述进行编码，编码质量可能受限于预训练嵌入模型的能力。

（完）
