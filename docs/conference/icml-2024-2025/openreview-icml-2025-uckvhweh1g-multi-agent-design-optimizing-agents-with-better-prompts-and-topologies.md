---
title: "Multi-Agent Design: Optimizing Agents with Better Prompts and Topologies"
title_zh: 多智能体设计：用更好的提示和拓扑优化智能体
authors: "Han Zhou, Xingchen Wan, Ruoxi Sun, Hamid Palangi, Shariq Iqbal, Ivan Vulić, Anna Korhonen, Sercan O Arik"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=uCKvHweh1g"
tags: ["query:eca"]
score: 7.0
evidence: 多智能体协作与拓扑优化
tldr: 当前多智能体系统的提示和拓扑设计依赖人工，效率低下。本文提出MASS框架，通过分析设计空间并利用搜索算法自动优化提示与交互拓扑。实验表明MASS在多个任务上超越手动设计，证明了自动化多智能体设计的有效性。该方法为边缘云协同AI系统中的智能体协作与拓扑设计提供了通用优化途径。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 854, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 842, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 841, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1672, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 841, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 838, \"height\": 568, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1786, \"height\": 670, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1673, \"height\": 691, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1130, \"height\": 746, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-uckvhweh1g/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1870, \"height\": 2155, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-uckvhweh1g/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1769, \"height\": 929, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uckvhweh1g/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1773, \"height\": 469, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uckvhweh1g/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1757, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uckvhweh1g/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1754, \"height\": 472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-uckvhweh1g/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1758, \"height\": 477, \"label\": \"Table\"}]"
motivation: 多智能体系统的提示和拓扑设计复杂且手动耗时，需要自动化优化。
method: 提出MASS框架，通过分析设计空间并利用搜索算法同时优化提示和交互拓扑。
result: 实验表明MASS能自动发现更有效的多智能体系统，在多个任务上超越手动设计。
conclusion: 自动化多智能体设计可显著提升系统性能，为边缘云协同等复杂场景提供通用优化方法。
---

## Abstract
Large language models, employed as multiple agents that interact and collaborate with each other, have excelled at solving complex tasks. The agents are programmed with prompts that declare their functionality, along with the topologies that orchestrate interactions across agents. Designing prompts and topologies for multi-agent systems (MAS) is inherently complex. To automate the entire design process, we first conduct an in-depth analysis of the design space aiming to understand the factors behind building effective MAS. We reveal that prompts together with topologies play critical roles in enabling more effective MAS design. Based on the insights, we propose Multi-Agent System Search (MASS), a MAS optimization framework that efficiently exploits the complex MAS design space by interleaving its optimization stages, from local to global, from prompts to topologies, over three stages: 1) block-level (local) prompt optimization; 2) workflow topology optimization; 3) workflow-level (global) prompt optimization, where each stage is conditioned on the iteratively optimized prompts/topologies from former stages. We show that MASS-optimized multi-agent systems outperform a spectrum of existing alternatives by a substantial margin. Based on the MASS-found systems, we finally propose design principles behind building effective multi-agent systems.

---

## 论文详细总结（自动生成）

# 论文结构化总结

## 1. 核心问题与整体含义（研究动机和背景）

当前基于大型语言模型（LLM）的多智能体系统（MAS）虽然能胜任复杂任务，但其设计过程——包括智能体的提示词（prompt）和智能体之间的交互拓扑（topology）——高度依赖人工调试，效率低下且易受主观经验影响。现有自动优化工作（如DSPy、ADAS、AFlow）要么只关注提示优化，要么只关注拓扑搜索，缺乏对两者联合优化以及相互影响机制的深入理解。本文旨在揭示提示词与拓扑在多智能体系统中的关键作用，并据此提出一种自动化的、高效的MAS优化框架，以提升系统整体性能。

## 2. 方法论：核心思想、关键技术细节

**核心思想**：通过多阶段、从局部到全局、从提示到拓扑的交替优化，在由提示词和可配置拓扑构成的设计空间中高效搜索，发现性能更优的MAS设计。

**关键技术细节**：

- **设计空间分析**：首先对MAS的常见设计因素（提示优化、智能体数量、拓扑类型）进行深入分析，发现：
  - 提示优化比单纯增加智能体数量更“token高效”（图2）。
  - 并非所有拓扑都有益，只有一小部分能带来正向提升（图3）。因此，设计空间需要被剪枝。
- **MASS框架三阶段**：
  1. **块级（局部）提示优化**：对每种基础拓扑模块（如Predictor、Reflector、Debator等）先独立进行提示优化（包括指令和示范），使用MIPROv2优化器，并评估每个模块的增量影响。
  2. **工作流拓扑优化**：基于阶段1评估出的增量影响，用softmax计算每个拓扑维度的选择概率，通过拒绝采样在剪枝后的空间中搜索最优拓扑组合，受预算（最大智能体数）约束。
  3. **工作流级（全局）提示优化**：基于阶段2找到的最佳拓扑，再次对整个MAS进行提示优化，以建模智能体之间的依赖关系。
- 整体流程如Algorithm 1所示，各阶段依次执行，前一阶段的结果作为后一阶段的输入。

## 3. 实验设计

- **数据集/场景**：
  - 推理：MATH、DROP
  - 多跳长上下文理解：HotpotQA、MuSiQue、2WikiMultiHopQA（来自LongBench）
  - 代码生成：MBPP、HumanEval、LiveCodeBench（test output prediction）
- **Benchmark**：共8个任务，涵盖数学推理、阅读理解、代码生成等多样场景。
- **对比方法**：
  - 基础方法：CoT、CoT-SC、Self-Refine、Multi-Agent Debate
  - 自动设计基线：ADAS、AFlow（注：AFlow原meta-prompt仅适用于Claude 3.5 Sonnet，作者用Gemini 1.5 Pro作为执行器、Claude作为优化器进行复现，结果仅作参考）
- **模型**：主要在Gemini 1.5 Pro和Flash上实验，并在Claude 3.5 Sonnet上验证关键结果。
- **公平性**：所有方法限制最大智能体数为10；MASS与其他基线在相同验证集上优化，在独立测试集上报告结果（3次运行取均值和标准差）。

## 4. 资源与算力

论文未明确提及具体GPU型号、数量或训练时长。所有实验基于推理时调用云端LLM API（Gemini 1.5、Claude 3.5 Sonnet），优化阶段也使用相同LLM作为评估器和优化器。算力消耗主要来自多次API调用，但文中没有量化地报告总token数或运行时间。

## 5. 实验数量与充分性

- **实验数量**：
  - 主实验结果：8个任务 × 2个模型（Pro/Flash） × 8个方法（含MASS） = 128个指标值。
  - 消融实验：阶段逐级消融（Base → +APO → +1PO → +2TO → +3PO）在8个任务上的平均结果（图5左）及单独对HotpotQA的消融（图5右）。
  - 优化轨迹可视化：DROP任务上MASS vs ADAS vs AFlow（图6）。
  - Claude 3.5 Sonnet验证：6个任务上的对比（表4）。
  - 成本-性能Pareto分析：MATH任务上总token与准确率关系（图9）。
- **充分性与客观性**：实验覆盖多个领域，基线齐全，消融清晰，统计报告了均值和标准差。但所有研究均使用同一组LLM，未在更多开源模型上验证（如Llama系列），存在一定偏差风险。

## 6. 主要结论与发现

1. **提示词比单纯增加智能体数量更高效**：优化单个智能体提示能在相同token预算下取得更高性能。
2. **仅有部分拓扑有益**：自动搜索应在剪枝后的设计空间中进行，以避免无效甚至有害的拓扑。
3. **MASS显著优于现有方法**：在8个任务上，MASS在Gemini 1.5 Pro上平均78.8%，Flash上74.3%，远超手动和自动基线（如ADAS、AFlow）。
4. **三阶段优化各有增益**：块级提示优化（+约6%）、拓扑优化（+约3%）、工作流级提示优化（+约2%），且三者缺一不可。
5. **设计原则**：
   - 在组合智能体之前先优化每个智能体的提示；
   - 通过组合有影响力的拓扑构建更有效的MAS；
   - 通过工作流级联合优化建模智能体间依赖关系。

## 7. 优点

- **系统性强**：首次将提示优化与拓扑优化统一在一个多阶段框架内，并进行了详细的设计空间分析。
- **实验充分**：涵盖8个不同难度的任务，与多种基线（包括最新自动设计方法）进行公平对比，并提供了消融实验和优化轨迹分析。
- **实用指导**：给出了可复现的设计原则，并在附录中提供了完整的提示模板和优化后的提示示例。
- **高效搜索**：通过分析识别出“有影响力的子空间”，降低了拓扑搜索的复杂度，使优化过程可扩展。

## 8. 不足与局限

- **算力与成本未透明化**：未报告优化所需的总API调用次数、时间或费用，不利于用户评估实际应用成本。
- **模型泛化性有限**：主要基于Gemini 1.5系列，仅在Claude 3.5上做部分验证，未涉及开源模型（如Llama、Qwen等），结论的泛化性有待验证。
- **搜索空间覆盖不够广泛**：虽然涵盖了主流拓扑（聚合、反思、辩论、工具等），但更复杂的、稀疏通信的拓扑（如Li et al., 2024b）未纳入，可能限制性能上限。
- **优化器依赖**：提示优化器使用了MIPROv2，其本身也需要验证集和多次调用，若验证集小或噪声大，可能影响搜索结果。
- **缺乏鲁棒性分析**：未讨论在少样本、噪声数据或任务漂移场景下的表现，实际部署中的鲁棒性未知。

（完）
