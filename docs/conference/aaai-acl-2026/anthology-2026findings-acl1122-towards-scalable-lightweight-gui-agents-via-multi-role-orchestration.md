---
title: Towards Scalable Lightweight GUI Agents via Multi-role Orchestration
title_zh: 通过多角色编排实现可扩展的轻量级GUI智能体
authors: "Ziwei Wang, Junjie Zheng, Leyang Yang, Sheng Zhou, Xiaoxuan Tang, Fang Zhouhua, Zhiwei Liu, Dajun Chen, Yong Li, Jiajun Bu"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1122.pdf"
tags: ["query:mobile-agent"]
score: 8.0
evidence: 通过多角色编排提升轻量级GUI智能体的可扩展性
tldr: 轻量级GUI智能体在资源受限设备上面临部署成本高和任务可扩展性差的问题，端到端学习难以适应复杂场景。论文提出多角色编排方法，协调多个轻量级模型参与真实GUI工作流，在成本与可扩展性之间取得平衡。方法使得轻量级MLLM能够在现实GUI任务中发挥作用，降低了部署门槛。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1636, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1617, \"height\": 648, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1301, \"height\": 2168, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1360, \"height\": 2254, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1638, \"height\": 1547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1636, \"height\": 2067, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1648, \"height\": 934, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1643, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1631, \"height\": 927, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1657, \"height\": 941, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1122/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1617, \"height\": 1836, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1598, \"height\": 701, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 774, \"height\": 396, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 710, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 774, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 756, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 767, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1751, \"height\": 1049, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 443, \"height\": 467, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 803, \"height\": 495, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1122/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 800, \"height\": 460, \"label\": \"Table\"}]"
motivation: 轻量级GUI智能体受限于容量和任务可扩展性，难以适应复杂场景。
method: 提出多角色编排机制，协同多个轻量级模型完成GUI自动化任务。
result: 在降低资源消耗的同时提升了任务处理能力。
conclusion: 为资源受限设备上的GUI智能体提供了一种成本-扩展性平衡方案。
---

## Abstract
Autonomous Graphical User Interface (GUI) agents powered by Multimodal Large Language Models (MLLMs) enable digital automation on end-user devices. While scaling both parameters and data has yielded substantial gains, advanced methods still suffer from prohibitive deployment costs on resource-constrained devices. When facing complex in-the-wild scenarios, lightweight GUI agents are bottlenecked by limited capacity and poor task scalability under end-to-end episodic learning, impeding multi-agent systems (MAS) adaptation, while training multiple skill-specific experts remains costly. Can we strike an effective trade-off in this cost–scalability dilemma, enabling lightweight MLLMs to participate in realistic GUI workflows? To address these challenges, we propose LAMO framework, which endows a lightweight MLLM with GUI-specific knowledge and task scalability, allowing multi-role orchestration to expand their capability boundary for GUI automation. LAMO combines role-oriented data synthesis with a two-stage training recipe: (i) supervised fine-tuning with Perplexity-Weighted Cross-Entropy optimization for knowledge distillation and visual perception enhancement, and (ii) reinforcement learning for role-oriented cooperative exploration. Via LAMO, we develop a task-scalable native GUI agent LAMO-3B supporting monolithic execution and MAS-style orchestration. When paired with advanced planners, as a plug-and-play policy executor, LAMO-3B can continuously benefit from planner advances, enabling a higher performance ceiling. Extensive static and online evaluations validate the effectiveness of our designs.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究背景**：基于多模态大语言模型（MLLM）的自主 GUI 智能体旨在实现终端设备上的数字自动化操作。然而，尽管参数和数据规模的扩展带来了显著性能提升，先进方法在资源受限设备上的部署成本仍然过高。
- **核心矛盾**：轻量级 GUI 智能体在复杂真实场景中面临双重瓶颈：
  - **容量限制**：端到端情景学习下，模型能力不足以应对复杂的真实 GUI 工作流。
  - **任务可扩展性差**：多智能体系统（MAS）的适配困难，而训练多个技能专属专家模型成本高昂。
- **研究问题**：能否在“成本—可扩展性”困境中找到一个有效平衡，使轻量级 MLLM 能够参与现实 GUI 工作流？
- **整体含义**：论文旨在为资源受限设备上的 GUI 智能体提供一种兼顾部署成本与任务扩展能力的方案，降低轻量级模型在真实应用中的使用门槛。

## 2. 方法论

- **核心思想**：提出 **LAMO 框架**，通过**多角色编排（Multi-role Orchestration）** 扩展轻量级 MLLM 的能力边界，使其在无需大规模参数的前提下胜任复杂的 GUI 自动化任务。
- **关键技术细节**：
  1. **角色导向的数据合成（Role-Oriented Data Synthesis）**：为模型注入 GUI 特定知识，并通过多角色任务划分提升数据的多样性和针对性。
  2. **两阶段训练方案**：
     - **阶段一：监督微调（SFT）**，采用 **Perplexity-Weighted Cross-Entropy（PWE）** 优化目标，实现知识蒸馏与视觉感知增强。该策略可对不同难度的训练样本赋予不同权重，从而更高效地从强教师模型中蒸馏知识。
     - **阶段二：强化学习（RL）**，用于**角色导向的协作探索**，使多个轻量级模型在交互中学习如何协作完成复杂任务。
- **最终产物**：训练得到 **LAMO-3B**，一个具备任务可扩展性的原生 GUI 智能体，支持两种运行模式：
  - **单体执行模式（Monolithic Execution）**
  - **MAS 风格编排模式（MAS-style Orchestration）**
- **插件式设计**：LAMO-3B 可作为即插即用的策略执行器（policy executor），与更先进的规划器（planner）配合使用时，能持续从规划器的进步中获益，从而突破自身性能上限。

## 3. 实验设计

- **评估方式**：论文采用了**静态评估（static evaluation）** 与**在线评估（online evaluation）** 相结合的方式。
- **对比方法**：文中与多种基线方法进行了对比，但具体对比方法列表在摘要中未详细列出，元数据显示共包含 10 张表格和 11 张图，涉及多组对比实验。
- **数据集/场景**：从图表元数据来看，实验覆盖了多个真实 GUI 工作流场景，具体数据集名称和基准细节在论文正文中有详述（摘要部分未穷举）。

## 4. 资源与算力

- **未明确说明**：在提供的论文内容（摘要及元数据）中，**没有明确提及**所使用的GPU型号、数量、训练总时长或计算资源开销等具体细节。
- 论文仅强调了所提方法在部署阶段具有较低的运行成本（轻量级模型），但训练阶段的具体算力投入需要查阅论文原文（如实验章节或附录）方可获取。

## 5. 实验数量与充分性

- **实验数量**：从元数据看，论文拥有 **10 张表格**和 **11 张图**，实验数量较为丰富，包括多组对比实验、消融研究以及不同场景下的性能验证。
- **充分性分析**：
  - ✅ **优点**：采用静态+在线双重评估，能更全面地反映模型在现实环境中的表现；多组消融实验有助于验证各设计组件的有效性；插件式策略执行器的实验设计能够体现系统在不同规划器下的泛化能力。
  - ⚠️ **客观性考量**：由于缺乏正文细节，无法判断实验是否涵盖了足够的基线方法和多样化的真实应用场景。论文为 ACL Findings 论文，实验规模在同类工作中处于合理水平，但要想全面评估统计显著性和泛化性，还需进一步查阅原文中的具体实验设置。

## 6. 主要结论与发现

- **核心结论**：LAMO 方法能够有效地通过多角色编排机制，使轻量级 MLLM 在真实 GUI 工作流中发挥作用，在降低资源消耗的同时提升任务处理能力。
- **具体发现**：
  - Perplexity-Weighted 交叉熵优化和强化学习协作探索的结合，能够有效提升轻量级模型的 GUI 感知与决策能力。
  - LAMO-3B 作为**即插即用的策略执行器**，能够持续受益于更强规划器的发展，实现更高的性能天花板。
  - 方法在成本（轻量级模型）与可扩展性（支持多角色编排）之间找到了有效的平衡点。

## 7. 优点

- **问题定位精准**：直面轻量级 GUI 智能体在部署成本和任务可扩展性上的核心矛盾，研究动机清晰、实际价值突出。
- **方法设计创新**：提出“多角色编排”作为扩展轻量级模型能力的核心机制，并设计了与之配套的两阶段训练方案（PWE 优化的 SFT + 角色导向 RL），方法体系完整且自洽。
- **成本—性能平衡**：仅使用 3B 参数的模型，就能实现可与更重模型竞争的性能，显著降低了部署门槛。
- **良好的系统集成性**：插件式设计使得模型可以与时下的先进规划器无缝配合，具备良好的生态兼容性和持续进化能力。
- **评估方式全面**：同时采用静态与在线评估，增加了实验结果的可信度。

## 8. 不足与局限

- **算力信息缺失**：提供的文本未透露训练所需的具体算力资源，这使得读者难以评估方法的训练成本是否真的“轻量”。
- **实验细节不完整**：摘要中未详细列出对比的具体基线方法、数据集规模、评估指标及在线实验的平台与环境，限制了对外部有效性的判断。
- **潜在偏差风险**：部分实验可能使用了合成数据（角色导向数据合成），存在数据分布与真实世界场景不一致的风险。
- **应用范围有限**：论文聚焦于 GUI 智能体领域，其“多角色编排”方法论是否可迁移到其他领域（如文本代理、机器人控制等）尚未得到验证。
- **模型规模单一**：仅验证了 3B 参数的版本，未充分探讨不同参数量下方法的表现，对于“轻量级”的适用范围界定不够完整。

---

（完）
