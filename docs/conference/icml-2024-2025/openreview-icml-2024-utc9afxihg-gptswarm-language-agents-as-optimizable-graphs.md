---
title: "GPTSwarm: Language Agents as Optimizable Graphs"
title_zh: GPTSwarm：作为可优化图的语言智能体
authors: "Mingchen Zhuge, Wenyi Wang, Louis Kirsch, Francesco Faccio, Dmitrii Khizbullin, Jürgen Schmidhuber"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=uTC9AFXIhg"
tags: ["query:eca"]
score: 8.0
evidence: 语言智能体作为可优化图，支持智能体间协作
tldr: 人类设计的提示工程技术分散且难以统一。本文提出GPTSwarm，将基于LLM的智能体描述为计算图，节点处理数据或调用LLM，边表示信息流。通过自动优化节点提示和边的连接方式，提升了智能体协作效率。实验证明该方法在多种任务上优于人工设计。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1708, \"height\": 781, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 794, \"height\": 511, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 794, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 810, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 778, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 646, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1730, \"height\": 1275, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1364, \"height\": 1028, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1741, \"height\": 1849, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 865, \"height\": 642, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 658, \"height\": 568, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-utc9afxihg/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 649, \"height\": 632, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 872, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 866, \"height\": 380, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 870, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 875, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1779, \"height\": 623, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1796, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1791, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1752, \"height\": 491, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1437, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1730, \"height\": 2230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1753, \"height\": 798, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1749, \"height\": 2375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1755, \"height\": 1971, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-utc9afxihg/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1774, \"height\": 663, \"label\": \"Table\"}]"
motivation: 现有LLM智能体设计方法分散，缺乏统一优化框架。
method: 将智能体表示为计算图，通过节点优化和边优化自动提升性能。
result: 在多个任务上，自动优化的图结构显著优于人工设计的提示工程。
conclusion: 计算图视角为LLM智能体系统的统一优化提供了新的框架。
---

## Abstract
Various human-designed prompt engineering techniques have been proposed to improve problem solvers based on Large Language Models (LLMs), yielding many disparate code bases. We unify these approaches by describing LLM-based agents as computational graphs. The nodes implement functions to process multimodal data or query LLMs, and the edges describe the information flow between operations. Graphs can be recursively combined into larger composite graphs representing hierarchies of inter-agent collaboration (where edges connect operations of different agents). Our novel automatic graph optimizers (1) refine node-level LLM prompts (node optimization) and (2) improve agent orchestration by changing graph connectivity (edge optimization). Experiments demonstrate that our framework can be used to efficiently develop, integrate, and automatically improve various LLM agents. Our code is public.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

近年来，基于大型语言模型（LLM）的智能体（agent）设计方法层出不穷，如 Chain of Thought、ReAct、Tree of Thought、Reflexion 等，但这些方法通常以分散的代码库形式存在，缺乏统一的表达和自动化优化手段。随着多智能体系统的发展，不同角色智能体间的协作编排也越来越多依赖人工设计，难以自动调整。论文提出 **GPTSwarm**，将语言智能体描述为**可优化的计算图**，统一了现有提示工程技术，并通过自动优化图的节点和边来提升性能，探索了智能体系统的自组织与自动改进。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：受“心智社会”（Society of Mind）启发，将单个语言智能体建模为有向无环图（DAG），节点表示基本操作（如 LLM 推理、工具调用、函数调用等），边表示信息流；多个智能体通过跨智能体边连接形成复合图（swarm），实现层级协作。
- **关键技术细节**：
  - **节点优化**：每个节点关联一个可优化的提示文本，通过迭代执行图并收集节点输入‑输出对，利用一个改进函数 I（例如采用 OPRO 风格的提示优化方法）基于历史记录和功能描述更新节点提示。算法 3 描述了该过程。
  - **边优化**：将边选择问题建模为连续优化，参数 θ 表示每条潜在边被选中的概率。采用 REINFORCE 算法（Williams, 1992）优化目标函数：  
    \[
    \max_{\theta} \mathbb{E}_{G' \sim D_\theta}[u_\tau(G')]
    \]
    其中 D_θ 是参数化的 DAG 分布，u_τ 是任务效用函数。梯度估计为：
    \[
    \nabla_\theta \approx \frac{1}{M}\sum_{i=1}^M \hat{u}_\tau(G_i)\nabla_\theta \log p_\theta(G_i)
    \]
    采样时确保图保持无环。算法 2 给出了详细步骤。
- **算法流程**（文字说明）：
  1. 定义单智能体图 G = (N, E, F, o)，按拓扑序执行节点，每个节点接收前驱节点输出和原始输入，应用函数 f_n，最终输出节点给出答案。
  2. 对多智能体复合图，通过添加跨智能体边形成新图 G_E，边集合 E 为待优化对象。
  3. 边优化：初始化 θ，每轮采样 M 个图，计算效用并更新 θ；节点优化：对每个节点，收集执行历史，用改进函数 I 更新其提示。

## 3. 实验设计：使用的数据集 / 场景、benchmark、对比方法

- **MMLU**（多选题问答）：
  - **对抗设置**：在 swarm 中混入同等数量的正常智能体和对抗智能体（故意输出错误答案），测试边优化能否自动屏蔽有害节点。对比基线为单 IO 智能体、全连接图、随机连接图。
  - **协作设置**：7 个不同角色 IO 智能体，观察性能提升。
- **Mini Crosswords**（填字游戏）：
  - 使用 20 道题目进行优化与评估。三种基础智能体：Tree of Thought (ToT)、Reflexion、Chain of Thought (COT)。对比方法包括单独的 ToT、Reflexion、COT 的 best-of-three、以及固定参数均匀分布基线。
- **HumanEval**（代码生成）：
  - 测试节点优化。智能体采用 ReAct 风格，先写代码，失败后根据执行反馈重试。优化方法：挑选最近成功/失败的输入‑输出对作为示范示例嵌入节点提示。对比无优化基线。
- **GAIA**（通用AI助手基准）：
  - 包含多模态推理、网页浏览、工具使用。构建多种 swarm（不同数量 TOT 智能体、不同节点操作如直接回答、网页搜索、文件分析等），采用自洽性（self-consistency）或“选择最佳”策略决定最终答案。对比 GPT-3.5、GPT-4、GPT-4-Turbo、AutoGPT 以及 GPT-4 with plugins 的报告结果。

## 4. 资源与算力

论文并未明确说明训练或推理所用的 GPU 型号与数量。在附录 F 中给出了代表性实验的 token 消耗、运行时间和大致花费（使用 OpenAI API），例如：
- MMLU 3T3A 优化：耗时 0.9 小时，花费 5.32 美元。
- Mini Crosswords 边优化（GPT-3.5-Turbo）：耗时 2.82 小时，花费 77.42 美元。
- GAIA Level 1 单 TOT 智能体：耗时 1.05 小时，花费 2.21 美元。
所有实验均通过调用 OpenAI API 完成，未提及自行训练的 GPU 使用情况。

## 5. 实验数量与充分性

- **MMLU**：在对抗设置中测试了 1T1A、3T3A、5T5A、7T7A 四种规模；每组使用 10% 的验证集（153 题）评估；优化 200 次迭代，每次 4 个采样。协作设置：7 个角色，5 个训练种子取平均。与 Multiagent Debate、DyLAN 对比，展示了成本和性能。
- **Mini Crosswords**：3 次运行取平均，报告标准误差；优化 10 轮，每轮采样 20 个图；还对比了均匀参数分布（控制边密度），并评估了用 GPT-4 测试优化后分布的效果。另外做了节点优化后续实验。
- **HumanEval**：在 8 次迭代中画出准确率曲线，3 次重复；从无优化 0.76 提升至 0.88。
- **GAIA**：14 种不同的 agent/swarm 配置（表 2），每种运行 5 次取均值和标准差；在同表还报告了人类表现。

**充分性评价**：实验覆盖了多个任务类型（问答、填字、代码、通用助手），涵盖了边优化和节点优化两种机制。但也存在不足：对抗设置的 MMLU 实验仅使用 GPT-4-Turbo 一个模型，未检查模型泛化；GAIA 实验未进行节点或边优化，仅展示框架的模块化能力；总体实验规模较小（如 HumanEval 仅 8 次迭代），统计严谨性（如多次随机种子）在部分实验中未完全贯彻（MMLU 对抗仅用固定子集）。

## 6. 论文的主要结论与发现

1. **边优化可有效屏蔽有害智能体**：在 MMLU 对抗设置中，优化后 swarm 的得分恢复到基线水平（≈0.7），而全连接和随机连接均显著低于基线。
2. **边优化自动发现更好的算法结构**：在 Mini Crosswords 上，优化后的 swarm 平均准确率 0.575（±0.0275），显著优于 best-of-three（0.320）和均匀参数分布（0.510）。用 GPT-4 评估优化后分布达到 0.800，超过先前最优方法 ToT（0.675）。
3. **节点优化可提升代码生成性能**：在 HumanEval 上，从 0.76 提升至 0.88（±0.007）。
4. **框架通用性**：在 GAIA 上，简单组合多智能体即可大幅超越 GPT-4 和 AutoGPT，达到 18.45 平均分（Level 1 提升 47.3%，Level 2 提升 260.2%）。

## 7. 优点

- **统一视角**：用计算图统一了多种提示工程技术，便于模块化组合和自动优化。
- **双层次优化**：同时支持节点（提示）和边（拓扑）的自动改进，首次将多智能体协作编排纳入优化范畴。
- **算法简洁有效**：边优化采用 REINFORCE 连续松弛，避免离散搜索，且能产生新的有效结构；节点优化基于历史输入‑输出对，轻量且有效。
- **开源框架**：提供 Python/PyTorch 实现，支持多种工具和智能体快速搭建（如代码开源）。
- **实验覆盖广**：在多个基准上验证了不同优化类型，尤其是 Mini Crosswords 上超越之前 SOTA，展示了自动发现新算法的潜力。

## 8. 不足与局限

- **实验规模有限**：Mini Crosswords 仅 20 题、HumanEval 只优化 8 轮，统计显著性可能受影响；MMLU 仅用子集（10% 验证集）且只有 GPT-4-Turbo 一个模型。
- **未进行全基准测试**：GAIA 实验未使用节点/边优化，仅展示框架组合能力；HumanEval 的节点优化只与无优化基线对比，未与手工提示的 SOTA 比较。
- **计算成本**：虽未自建 GPU 集群，但每次优化仍依赖 OpenAI API 多次调用（例如 Mini Crosswords 边优化消耗约 5000 万提示 token），对研究重现可能造成经济障碍。
- **DAG 限制**：当前只支持有向无环图，不能建模循环或反馈结构（如某些智能体内部迭代），可能限制某些算法的表达。
- **可扩展性未验证**：实验中最大 swarm 为 14 个节点（7 对抗 + 7 正常）或 7 个 TOT 智能体，未测试更大规模（如百个以上智能体）下的优化收敛性和通信效率。
- **优化稳定性**：Mini Crosswords 中边优化在前几轮变化混沌，之后才趋于单调，对初始超参数敏感（如学习率 0.4、初始概率 10%），通用调参建议不足。
- **缺乏与更强基线的对比**：例如在 HumanEval 未与 Reflexion、Codex 等专用方法做直接对比；GAIA 中仅比较了 GPT-4 with plugins 的非官方结果，且未与近期工作（如 AutoGen、MetaGPT）对比。

（完）
