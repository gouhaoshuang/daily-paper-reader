---
title: "MAS-Bench: A Unified Benchmark for Shortcut-Augmented Hybrid Mobile GUI Agents"
title_zh: MAS-Bench：面向快捷方式增强的混合移动GUI智能体的统一评测基准
authors: "Pengxiang Zhao, Guangyi Liu, Yaozhen Liang, Weiqing He, Zhengxi Lu, Wenhao Wang, Yuehao Huang, Yuxiang Chai, Zhaolu Kang, Yaxuan Guo, Hao Wang, Kexin Zhang, Liang Liu (陆亮), Yong Liu"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.316.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 面向移动GUI智能体的统一评测基准，聚焦快捷方式增强的混合体
tldr: 现有基准对GUI与快捷方式混合的移动智能体缺乏系统评测。为此提出MAS-Bench，首个专注该范式的基准，包含11个真实应用的139个复杂任务和88个预定义快捷方式知识库。它不仅评估智能体使用已有快捷方式的能力，还考察其自动发现和创建可复用低成本工作流的生成能力。该基准为混合移动智能体的发展提供了统一评测标准。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 799, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 706, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1592, \"height\": 899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 731, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 807, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 781, \"height\": 932, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1577, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1574, \"height\": 640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1502, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1506, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long316/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1500, \"height\": 589, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 796, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1634, \"height\": 1388, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 802, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 799, \"height\": 591, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1636, \"height\": 789, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1626, \"height\": 657, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 793, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1635, \"height\": 1392, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1646, \"height\": 676, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1635, \"height\": 1388, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1522, \"height\": 551, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1364, \"height\": 372, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 801, \"height\": 989, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 797, \"height\": 1110, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 797, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 795, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long316/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1623, \"height\": 1125, \"label\": \"Table\"}]"
motivation: 现有评测缺乏对GUI与快捷方式混合的移动智能体的系统评估。
method: 提出MAS-Bench基准，涵盖139个跨11个应用的复杂任务和88个预定义快捷方式知识库，并评估智能体自主生成快捷方式的能力。
result: 基准通过多维评估揭示了智能体在快捷方式使用与生成上的表现差异。
conclusion: 为GUI-快捷方式混合移动智能体提供了统一、可扩展的评测框架。
---

## Abstract
Shortcuts such as APIs and deep-links have emerged as efficient complements to flexible GUI operations, fostering a promising hybrid paradigm for MLLM-based mobile automation. However, systematic evaluation of GUI–shortcut hybrid agents remains largely underexplored. To bridge this gap, we introduce **MAS-Bench**, a benchmark that pioneers the evaluation of GUI-shortcut hybrid agents with a specific focus on the mobile domain. Beyond merely using predefined shortcuts, MAS-Bench assesses an agent’s capability to *autonomously generate* shortcuts by discovering and creating reusable, low-cost workflows. It features 139 complex tasks across 11 real-world applications, a knowledge base of 88 predefined shortcuts (APIs, deep-links, RPA scripts), and 9 evaluation metrics. Experiments demonstrate that hybrid agents achieve up to 68.3% success rate and 39% greater execution efficiency than GUI-only counterparts. Furthermore, our evaluation framework effectively reveals the quality gap between predefined and agent-generated shortcuts, validating its capability to assess shortcut generation methods. MAS-Bench addresses the lack of systematic benchmarks for GUI-shortcut hybrid mobile agents, providing a foundational platform for future advancements in creating more efficient and robust intelligent agents.

---

## 论文详细总结（自动生成）

# 论文总结：MAS-Bench——面向快捷方式增强的混合移动 GUI 智能体的统一评测基准

## 1. 论文的核心问题与整体含义

- **研究背景**：基于多模态大语言模型（MLLM）的移动智能体通常通过 GUI 操作完成用户任务。然而，纯 GUI 操作方式步骤冗长、效率较低。API、深度链接（deep-links）、RPA 脚本等**快捷方式（shortcuts）**可以作为 GUI 操作的高效补充，形成“GUI + 快捷方式”的混合智能体范式。
- **核心问题**：现有移动智能体评测基准几乎都只关注纯 GUI 交互，**缺乏对 GUI–快捷方式混合智能体的系统评测**，导致该范式的发展缺乏统一衡量标准和可比较的评估框架。
- **整体含义**：论文提出 **MAS-Bench**，首次面向 GUI-快捷方式混合移动智能体进行系统评测，不仅考察智能体**使用**已有快捷方式的能力，还创新性地考察其**自主发现、创建和复用低成本工作流（即快捷方式生成）**的能力，为混合移动智能体的发展提供了基础性评测平台。

## 2. 论文提出的方法论

- **核心思想**：构建一个能够同时覆盖两种能力维度的评测框架——
  - **快捷方式使用（shortcut usage）**：智能体能否在真实应用中检索、理解并调用预定义的快捷方式（API、deep-links、RPA 脚本）完成任务；
  - **快捷方式生成（shortcut generation）**：智能体能否通过自身操作轨迹发现可复用的高效工作流，并将其转化为新的快捷方式，从而降低未来同类任务的执行成本。
- **MAS-Bench 构成**：
  - **任务集**：覆盖 11 个真实世界移动应用的 **139 个复杂任务**；
  - **知识库**：包含 **88 个预定义快捷方式**，涵盖 API、deep-links、RPA 脚本三种类型；
  - **评估指标**：设计 **9 个评测指标**，用于多维度衡量任务完成质量、执行效率、快捷方式生成质量等。
- **评估流程（文字说明）**：
  1. 给定用户自然语言任务描述和当前手机界面状态；
  2. 智能体可选择执行 GUI 操作（点击、滑动、输入等），或调用/创建快捷方式；
  3. 系统记录操作序列、执行时长、是否成功及快捷方式使用情况；
  4. 通过多维度指标自动评估任务成功率、效率提升幅度以及生成快捷方式的可复用性、成本与效果。
- **亮点机制**：对智能体生成的快捷方式与人工预定义的快捷方式同时进行质量评估，从而量化“自动生成捷径”与“专家预定义捷径”之间的差距。

## 3. 实验设计

- **基准数据集**：MAS-Bench 本身即评测基准，包含：
  - **11 个真实移动应用**；
  - **139 个复杂（多步、跨页面）任务**；
  - **88 条预定义快捷方式知识库**（API + deep-links + RPA script）。
- **对比方法**：
  - 主要对比 **混合智能体（GUI + Shortcut）** 与 **纯 GUI 智能体（GUI-only）** 在同一任务集上的表现；
  - 同时评估不同大模型在 MAS-Bench 上的差异（论文摘要未列出具体模型清单，推测基于多种主流 MLLM 进行评估，需结合全文确认）。
- **关键实验结果**（来自摘要）：
  - 混合智能体成功率最高达 **68.3%**；
  - 相比纯 GUI 智能体，执行效率提升最高达 **39%**；
  - MAS-Bench 的评估框架能有效揭示预定义快捷方式与智能体生成快捷方式之间的质量差异。

## 4. 资源与算力

- **未明确说明**：论文摘要和元数据中**没有**披露训练或评测所用的 GPU 型号、数量、训练时长等具体算力信息。
- 由于 MAS-Bench 是一个评测基准而非训练方法，其主要算力消耗推测主要集中在运行大规模 MLLM 推理评估上，但具体硬件配置需要查阅论文全文（如实验设置部分）才能确认。

## 5. 实验数量与充分性

- **从元数据推断**：论文包含 **11 张图**和 **17 张表**，可见实验章节内容较为丰富，可能涵盖：
  - 主实验（不同模型 × 使用/不使用快捷方式）；
  - 快捷方式生成质量评估实验；
  - 各维度指标细粒度分析；
  - 对不同快捷方式类型（API / deep-link / RPA）的分解实验；
  - 可能存在的消融或鲁棒性分析。
- **充分性评估**：
  - **优点**：任务规模（139 个真实任务）、应用覆盖（11 个）、指标维度（9 个）在同类移动智能体基准中属于中等偏上水平；同时评估“使用”和“生成”两条路径，使实验设计具有较好的完整性。
  - **不足**：基于当前提供的文本，尚无法确认是否有严格的消融实验（如去掉知识库、去掉生成能力等）以及跨模型规模（小模型 vs 大模型）的系统对比；这些需依赖全文验证。
  - **公平性**：摘要未提及是否控制模型版本、推理预算等变量；对于“效率提升 39%”的统计口径（如步数减少 vs 时间减少）也需要进一步核实。

## 6. 论文的主要结论与发现

1. **混合范式显著优于纯 GUI**：GUI + 快捷方式混合智能体可达 68.3% 的成功率，比纯 GUI 智能体效率提升最高 39%，验证了快捷方式作为 GUI 操作补充的有效性。
2. **首个系统性评测框架成立**：MAS-Bench 成功弥补了 GUI-快捷方式混合移动智能体缺乏统一基准的空缺。
3. **生成与预定义之间存在质量差距**：智能体自动生成的快捷方式与专家预定义的快捷方式仍有明显质量差距，说明“快捷方式自动生成”这一研究方向仍有较大提升空间。
4. **基准的可扩展性**：MAS-Bench 为未来更高效、更鲁棒的混合移动智能体的研究提供了标准化评测基础。

## 7. 优点

- **选题新颖、定位精准**：首次系统化提出并评测“GUI-快捷方式混合移动智能体”范式，填补领域空白。
- **能力维度双覆盖**：不只测“用捷径”，还测“造捷径”，将快捷方式生成这一重要能力纳入评测，具有前瞻性。
- **真实应用 + 多种快捷方式类型**：覆盖 11 个真实 App，并整合 API、deep-link、RPA 三类快捷方式，贴近真实部署场景。
- **指标设计多维**：9 个评测指标兼顾成功率与效率等多重维度，避免单一成功率指标的片面性。
- **统一可扩展框架**：任务、知识库、指标解耦，便于后续扩展更多应用和快捷方式类型。

## 8. 不足与局限

- **任务规模有限**：139 个任务、11 个应用虽具代表性，但与真实世界中海量移动应用和长尾任务相比覆盖仍有限。
- **快捷方式库规模偏小**：88 条预定义快捷方式可能不足以覆盖真实场景中快捷方式的多样性。
- **生成的快捷方式质量评估难度高**：如何自动评估“生成工作流”的可复用性、可读性和稳定性是一个开放问题，论文所使用的自动评估方法可能存在度量偏差。
- **效率指标的统计口径**：摘要仅给出“执行效率提升 39%”的单一数字，未区分步数减少/时间减少/API 调用成本等不同口径，可能存在对比偏差。
- **应用地域与生态偏差**：11 个真实 App 的选择可能偏向某些平台或地区，跨地域/跨系统（Android/iOS）的泛化能力未在摘要中体现。
- **算力与复现细节未公开**：未提供模型推理资源和完整超参数配置，可能影响实验的可复现性。

（完）
