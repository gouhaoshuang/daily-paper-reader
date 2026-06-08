---
title: Multi-agent Architecture Search via Agentic Supernet
title_zh: 基于智能体超网络的多智能体架构搜索
authors: "Guibin Zhang, Luyang Niu, Junfeng Fang, Kun Wang, LEI BAI, Xiang Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=imcyVlzpXh"
tags: ["query:eca"]
score: 8.0
evidence: 多智能体协作与架构搜索
tldr: 现有方法自动化设计多智能体系统时通常得到静态架构，无法根据查询难度动态分配资源。本文提出MaAS框架，通过优化概率化和连续分布的智能体超网络（agentic supernet）来搜索最佳架构。实验表明，该方法在多个任务上比静态系统更高效灵活，为多智能体系统的自动化设计提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1733, \"height\": 562, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1741, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 833, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 856, \"height\": 869, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 838, \"height\": 1078, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1739, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 858, \"height\": 317, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1432, \"height\": 1256, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 674, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1772, \"height\": 1066, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-imcyvlzpxh/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 680, \"height\": 565, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 796, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 509, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1764, \"height\": 437, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1818, \"height\": 979, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 969, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1207, \"height\": 479, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-imcyvlzpxh/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1205, \"height\": 233, \"label\": \"Table\"}]"
motivation: 现有多智能体系统设计依赖人工且架构静态，无法适应不同查询的难度差异。
method: 提出MaAS框架，将多智能体架构表示为连续概率分布的超网络，通过优化实现自动化搜索。
result: 在多个基准任务上，MaAS自动化搜索的架构优于静态设计，且能动态分配资源。
conclusion: MaAS验证了超网络方法在多智能体架构搜索中的有效性，提升了系统的灵活性和效率。
---

## Abstract
Large Language Model (LLM)-empowered multi-agent systems extend the cognitive boundaries of individual agents through disciplined collaboration and interaction, while constructing these systems often requires labor-intensive manual designs. Despite the availability of methods to automate the design of agentic workflows, they typically seek to identify a static, complex, one-size-fits-all system, which, however, fails to dynamically allocate inference resources based on the difficulty and domain of each query. To address this challenge, we shift away from the pursuit of a monolithic agentic system, instead optimizing the \textbf{agentic supernet}, a probabilistic and continuous distribution of agentic architectures. We introduce \textbf{MaAS}, an automated framework that samples query-dependent agentic systems from the supernet, delivering high-quality solutions and tailored resource allocation (\textit{e.g.}, LLM calls, tool calls, token cost). Comprehensive evaluation across six benchmarks demonstrates that MaAS \textbf{(I)} requires only $6\\sim45\\%$ of the inference costs of existing handcrafted or automated multi-agent systems, \textbf{(II)} surpasses them by $0.54\\%\sim11.82\\%$, and \textbf{(III)} enjoys superior cross-dataset and cross-LLM-backbone transferability.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：当前基于大语言模型的多智能体系统（如AutoGen、MetaGPT等）通常依赖人工设计，或自动搜索一个静态的“一刀切”复杂工作流。然而，这种方法无法根据每个查询的难度和领域动态分配推理资源（如LLM调用次数、工具调用、Token成本）。
- **核心问题**：现有自动设计方法（如AFlow、GPTSwarm）追求一个最优的单一架构，但面对多样化的查询（如简单算术 vs. 高级数学、文件读取 vs. 网页搜索），不存在一个通用的最优系统。因此需要一种能根据查询动态调整的架构分布。
- **整体含义**：论文提出将多智能体系统设计从“搜索单一最优架构”转变为“优化一个概率连续分布的智能体超网络”，从而在每个查询上自适应采样合适的架构，实现高性能和低资源消耗的平衡。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：构建一个**Agentic Supernet（智能体超网络）**，它是一个包含所有可能多智能体候选架构的概率连续分布。超网络通过一个控制器网络，根据输入查询条件采样子网络（即具体的多智能体系统），并通过环境反馈联合优化超网络的分布参数和操作算子（operators）。
- **关键技术细节**：
  - **操作算子定义**：每个算子是一个复合LLM调用过程，包含多个LLM智能体、提示词和工具。例如CoT、ReAct、Multi-agent Debate、Self-Refine、Ensemble等。
  - **超网络结构**：由L层组成，每层包含可选算子的概率分布，且条件依赖于前层选择。引入**早期退出算子**，使得简单查询可以提前终止。
  - **采样过程**：使用MoE风格网络，根据查询嵌入和已选算子历史，计算每个算子的激活分数，通过累积阈值动态确定每层激活的算子数量。
  - **优化目标**：联合优化性能（答案正确性）和成本（Token消耗）。梯度估计采用经验贝叶斯蒙特卡洛采样（用于分布参数π）和**文本梯度**（用于算子本身的优化，如提示词、温度、节点结构）。
- **算法流程**：对每个训练样本，分层采样架构，执行并获取反馈，计算性能-成本加权损失，分别更新分布参数和算子。

## 3. 实验设计

- **数据集/场景**：6个公开基准，覆盖三个领域：
  - 数学推理：GSM8K、MATH、MultiArith
  - 代码生成：HumanEval、MBPP
  - 工具使用：GAIA（多模态、网页浏览等）
- **Benchmark**：使用Pass@1（代码）、Accuracy（数学）、以及成本指标。
- **对比方法**：三类14个基线：
  - 单智能体方法：CoT、ComplexCoT、Self-Consistency
  - 手工多智能体系统：MultiPersona、LLM-Debate、LLM-Blender、DyLAN、AgentVerse、MacNet
  - 自动多智能体系统：GPTSwarm、AutoAgents、ADAS、AgentSquare、AFlow
  - 额外GAIA基线：AutoGPT、TapeAgent、Sibyl

## 4. 资源与算力

- 论文**未明确说明**使用的GPU型号、数量或训练时长。但提到了：
  - 训练Token消耗：MaAS在MATH上训练仅需3.38美元（远低于AFlow的22.50美元），训练墙钟时间为53分钟（低于DyLAN的508分钟和GPTSwarm的129分钟）。
  - 推理成本：MaAS推理API成本0.42美元，为所有对比方法中最低之一。
  - 所有LLM通过API访问，基础模型为gpt-4o-mini（闭源）以及Qwen-2.5-72b、llama-3.1-70b（开源），温度设为1。
- 结论：论文侧重于成本效率而非原始算力，未提供GPU硬件细节。

## 5. 实验数量与充分性

- **实验数量**：主表（Table 1）报告了5个基准（GSM8K、MATH、MultiArith、HumanEval、MBPP）上MaAS与14个基线的对比；Table 2报告GAIA上10个基线的对比。此外包含：
  - **成本分析**（Table 3、Figure 4）：在MATH上详细对比Token消耗、API成本、墙钟时间。
  - **参数敏感性分析**（Figure 7）：对层数L、成本惩罚系数λ、采样次数K进行实验。
  - **消融实验**（Table 4）：移除文本梯度、移除早期退出、移除成本约束，共3个消融变体。
  - **迁移性分析**（Table 7-8）：跨模型（gpt-4o-mini→Qwen/llama）和跨数据集（MATH→GSM8K等）实验。
  - **归纳性分析**（Figure 8-10）：将Debate算子作为未见算子测试泛化能力。
- **充分性与公平性**：
  - 对比方法覆盖全面，包括近期SoTA（AFlow、AgentSquare等）。
  - 所有基线基础LLM统一为gpt-4o-mini，确保公平。
  - 消融实验验证了各组件的必要性。
  - 实验覆盖了多个领域，且包含迁移和归纳测试，较为充分。

## 6. 主要结论与发现

- **性能优势**：MaAS在6个基准上超越所有手动/自动方法，平均提升0.54%~11.82%（Table 1）。在GAIA上提升显著（20.69% vs. 次优16.34%）。
- **成本高效**：MaAS仅需现有方法6%~45%的推理成本，训练成本仅为AFlow的15%左右。
- **动态资源分配**：通过早期退出和算子条件采样，MaAS能根据查询难度自动分配资源（简单查询多用1-2层，复杂查询用满4层）。
- **强迁移性**：在不同LLM后台和数据集之间表现良好，无需微调即能适应。
- **归纳能力**：即使训练时未见过Debate算子，MaAS在推理时仍能合理激活并使用它。

## 7. 优点

- **范式创新**：首次将多智能体架构搜索从单一架构优化提升为分布优化，更贴合实际动态需求。
- **方法完备性**：联合优化架构分布和算子本身（通过文本梯度），实现全自动自演进。
- **成本-性能平衡**：通过显式成本约束和早期退出，在保持高性能的同时大幅降低开销。
- **实验全面且公平**：覆盖多领域、多类型基线，包含消融、敏感性、迁移、归纳实验，验证方法鲁棒性。
- **实际可用性**：最终框架可直接用于不同查询的推理，无需重新搜索。

## 8. 不足与局限

- **基础模型依赖**：所有实验基于gpt-4o-mini等有限模型，未测试更大模型（如GPT-4）下的行为。
- **搜索空间限制**：算子集是手动预定义的（7个初始算子+退出算子），未证明能否自动发现全新的、未预设的协作模式。
- **训练成本**：虽然比AFlow等低，但仍需每查询多次采样（K=4）和环境反馈，对大规模部署可能有开销。
- **领域覆盖**：未涉及开放域对话、多模态理解（GAIA仅部分涉及）、实时交互等场景。
- **理论分析缺失**：未提供超网络收敛性、泛化误差界等理论保证。
- **公平性细节**：部分基线（如AFlow）可能本有更强配置（claude-3.5），但被限制为gpt-4o-mini以保证公平，可能弱化了其表现。

（完）
