---
title: "MAGNET: Towards Adaptive GUI Agents with Memory-Driven Knowledge Evolution"
title_zh: MAGNET：迈向具有记忆驱动知识演化的自适应GUI智能体
authors: "Libo Sun, Jiwen Zhang (张霁雯), Siyuan Wang (王思远), Zhongyu Wei (魏忠钰)"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.1299.pdf"
tags: ["query:mobile-agent"]
score: 10.0
evidence: 面向移动GUI智能体的记忆驱动自适应框架，支持自主任务执行与知识演化
tldr: 论文针对移动GUI智能体因应用频繁更新导致的界面变化和工作流重组而失效的问题，提出MAGNET自适应框架。它采用静态记忆与程序记忆分别关联视觉特征与功能语义、捕获跨工作流的稳定任务意图，并通过动态记忆演化机制持续优化记忆。该框架增强了智能体在真实移动环境中的动作定位与任务执行鲁棒性，是移动端任务执行代理的重要基础。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 792, \"height\": 654, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1496, \"height\": 665, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1632, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 819, \"height\": 817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1153, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 405, \"height\": 804, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 376, \"height\": 802, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 375, \"height\": 800, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 208, \"height\": 281, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 210, \"height\": 219, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1299/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1595, \"height\": 512, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1554, \"height\": 642, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 771, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 743, \"height\": 703, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 733, \"height\": 507, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 689, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 406, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 805, \"height\": 556, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 684, \"height\": 505, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1633, \"height\": 1099, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 803, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 598, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 806, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 806, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 797, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1299/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 620, \"height\": 211, \"label\": \"Table\"}]"
motivation: 移动应用界面频繁变化导致GUI智能体无法稳定执行任务，需要自适应机制。
method: 提出双级记忆机制：静态记忆关联视觉与功能语义，程序记忆捕获稳定任务意图，并动态演化记忆。
result: 有效提升智能体在界面变化下的动作定位与任务执行鲁棒性。
conclusion: 为移动GUI智能体提供了抗环境变化的记忆驱动框架。
---

## Abstract
Mobile GUI agents powered by large foundation models enable autonomous task execution in applications, but frequent updates that alter UI appearance and reorganize workflows cause agents trained on historical data to fail. Despite these surface changes, we observe that functional semantics and task intents remain fundamentally stable. Building on this insight, we introduce MAGNET, a memory-driven adaptive agent framework with dual-level memory: stationary memory that links diverse visual features to stable functional semantics for robust action grounding and procedural memory that captures stable task intents across varying workflows. Furthermore, we propose a dynamic memory evolution mechanism that continuously refines both memories by prioritizing frequently accessed knowledge. Evaluations on the online benchmark AndroidWorld demonstrate substantial improvements over memory-augmented baselines, while offline benchmarks confirm consistent gains under distribution shifts. These results validate that leveraging stable structures across interface changes improves agent performance and generalization in evolving software environments.

---

## 论文详细总结（自动生成）

# MAGNET：迈向具有记忆驱动知识演化的自适应GUI智能体 — 论文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **核心问题**：移动应用界面频繁更新（UI外观变化、工作流重组）导致基于历史数据训练的GUI智能体在真实环境中任务执行失败。
- **关键观察**：尽管界面表层不断变化，但应用的功能语义（functional semantics）与任务意图（task intents）在本质上保持稳定。
- **整体含义**：现有方法过度依赖历史界面特征，缺乏对环境变化的适应能力。论文指出，若能从变化表象中提取稳定结构，智能体便能在不断演化的软件环境中保持可靠性能。

## 2. 方法论：MAGNET 框架

- **总体思路**：构建一个记忆驱动的自适应agent框架，利用“表面多变、语义稳定”这一核心洞察，将界面变化中的稳定知识进行显式建模与持续利用。
- **双级记忆机制（Dual-Level Memory）**：
  - **静态记忆（Stationary Memory）**：将多样的视觉特征与稳定的功能语义进行关联，用于支持鲁棒的动作定位（action grounding）。即使界面外观改变，仍能通过功能语义识别可操作元素。
  - **程序记忆（Procedural Memory）**：捕获跨不同工作流（varying workflows）依然稳定的任务意图（task intents），使agent在流程重组后仍能理解任务目标与执行步骤。
- **动态记忆演化机制（Dynamic Memory Evolution）**：
  - 通过持续交互，优先强化被频繁访问的知识，不断细化和更新两类记忆。
  - 使记忆库能够随环境变化自适应调整，避免知识陈旧或失效。
- **算法/流程要点**（文字说明）：
  - 输入当前UI界面 → 利用静态记忆匹配视觉特征到功能语义 → 结合程序记忆识别任务意图与执行规划 → 执行动作 → 根据结果与访问频率动态更新记忆。

## 3. 实验设计

- **在线基准**：**AndroidWorld**（在线真实环境benchmark），用于评估agent在真实、动态移动环境中的自主任务执行能力。
- **离线基准**：验证在**分布偏移（distribution shifts）** 条件下的性能表现，考察模型的泛化能力。
- **对比方法**：与**记忆增强基线（memory-augmented baselines）** 进行对比，具体基线方法在摘要中未逐一列出（需参考正文）。

## 4. 资源与算力

- **原文未明确提及**具体的GPU型号、数量、训练时长或推理资源消耗。
- 摘要及元数据中未包含任何算力相关的技术细节，因此无法对此进行量化总结。

## 5. 实验数量与充分性

- **实验类型**：至少包含两大类——在线基准测试（AndroidWorld）与离线基准测试（分布偏移场景）。
- **充分性评估**：
  - **积极面**：在线+离线双重评估覆盖了真实环境与可控偏移场景，能够较好地反映方法在动态环境中的鲁棒性和泛化能力。
  - **局限性**：由于仅有摘要信息，不明确是否包含逐组件的消融实验（如静态记忆/程序记忆/动态演化机制的各自贡献）、跨不同应用类型（如社交、购物、工具类App）的覆盖范围，以及对比基线的数量和种类。这些信息需依赖论文正文补充。

## 6. 主要结论与发现

- MAGNET在AndroidWorld在线benchmark上显著优于记忆增强基线方法。
- 在离线benchmark的分布偏移条件下取得一致的性能提升。
- 核心结论：**利用界面变化中存在的稳定结构（功能语义与任务意图），能有效提升GUI智能体在动态软件环境中的表现与泛化能力**，验证了记忆驱动的自适应范式在移动智能体领域的有效性。

## 7. 优点

- **问题定位精准**：切中移动GUI智能体实际部署中界面频繁更新的痛点，具有明确的现实意义。
- **核心洞察简洁有力**：“表象多变、语义稳定”的观察为设计自适应机制提供了合理且可操作的理论支撑。
- **双级记忆设计清晰**：静态记忆负责感知层（视觉→语义映射），程序记忆负责任务层（意图→工作流），分层解耦合理。
- **动态演化机制新颖**：将记忆视为随时间持续更新的动态资源，而非静态知识库，增强了框架的长期适应能力。
- **评估场景全面**：同时采用在线真实环境（AndroidWorld）与离线分布偏移基准，兼顾真实性与可控性。

## 8. 不足与局限

- **算力信息缺失**：论文摘要及元数据未报告训练/推理资源消耗，不利于复现成本估算。
- **实验细节不透明**：对比基线、消融实验、应用类别覆盖范围等关键细节未在摘要中体现，难以判断实验设置的完备性与公平性。
- **记忆演化的长期行为未知**：动态记忆演化可能面临知识冲突、遗忘偏差或记忆无限增长等问题，摘要中未提及相关处理机制。
- **安全性与稳定性考量不足**：在线环境中的错误动作可能导致不可逆后果，摘要中未涉及安全策略或失败恢复机制。
- **评估范围有限**：仅涉及Android生态，未覆盖iOS或其他平台；仅报告了任务成功率类指标，未提及效率、成本或用户满意度等维度。
- **泛化风险**：静态记忆与视觉特征的关联可能仍受特定UI渲染方式、语言或文化习惯的影响，跨区域/跨语言的有效性尚未验证。

（完）
