---
title: "Towards Self-Evolving Agents: Enabling Autonomy through Interactive Experience Refinement"
title_zh: 迈向自我演化智能体：通过交互经验精炼实现自主性
authors: "Cheng Yang, Xuemeng Yang, Licheng Wen, Daocheng Fu, Jianbiao Mei, Rong Wu, Pinlong Cai, Yufan Shen, Nianchen Deng, Jia Xu, Botian Shi, Yu Qiao, Haifeng Li"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1522.pdf"
tags: ["query:mobile-agent"]
score: 4.0
evidence: 面向长程操作任务的自我演化智能体框架，未针对移动设备
tldr: 大语言模型在复杂多步操作任务中因无法从过去经验学习而表现受限。提出MUSE框架，通过层次化记忆模块组织跨领域知识，并利用执行后自动批判机制将操作日志蒸馏为结构化可复用知识，使智能体动态演化。在TAC生产力基准上验证了有效性。该框架虽非移动专用，但其经验学习机制可迁移至移动智能体。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 795, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1584, \"height\": 898, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 789, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 443, \"height\": 286, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 937, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 830, \"height\": 158, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 853, \"height\": 309, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 356, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 856, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 876, \"height\": 260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 864, \"height\": 254, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1374, \"height\": 1560, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1535, \"height\": 749, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1522/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1535, \"height\": 749, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1469, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1472, \"height\": 421, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1503, \"height\": 246, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1527, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 794, \"height\": 1256, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 727, \"height\": 346, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1311, \"height\": 1250, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1332, \"height\": 1826, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1280, \"height\": 1654, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1376, \"height\": 1017, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1455, \"height\": 2471, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1456, \"height\": 2541, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1456, \"height\": 2535, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1455, \"height\": 2535, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1522/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1464, \"height\": 814, \"label\": \"Table\"}]"
motivation: 静态智能体无法从经验中学习，难以完成复杂多步任务。
method: 构建层次化记忆模块与执行后批判机制，蒸馏经验为可复用知识。
result: 在TAC基准上带来性能提升，兼具自演化能力。
conclusion: 为操作型智能体的持续学习提供了通用框架，可适配移动场景。
---

## Abstract
Large Language Models often struggle with complex, multi-step operational tasks because they remain static during inference and cannot learn from past experience. To address this, we propose MUSE, a framework that enables iterative self-improvement through a hierarchical Memory Module. MUSE organizes cross-domain insights to facilitate the orchestration of long-horizon workflows. The core of our approach is an autonomous post-execution critique mechanism: after completing each sub-task, the system analyzes its operational logs and distills raw execution data into structured, reusable knowledge. This allows the agent to evolve dynamically rather than relying on fixed parameters. Evaluated on the rigorous TAC productivity benchmark, MUSE achieves new state-of-the-art results, significantly outperforming previous methods using only the streamlined Gemini-2.5 Flash model. Our analysis demonstrates that MUSE’s performance scales with the accumulation of insights and exhibits strong cross-task transferability, marking a key step toward autonomous systems capable of lifelong learning in professional environments. Demo videos can be found in our supplementary materials.

---

## 论文详细总结（自动生成）

# 《迈向自我演化智能体：通过交互经验精炼实现自主性》论文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **核心痛点**：现有大规模语言模型（LLM）在复杂、多步骤操作任务上表现欠佳，根本原因在于**推理时静态不变**——模型在推理过程中无法从过去的经验中学习。
- **现有不足**：
  - 传统基准（如问答、数学推理、代码生成）仅度量单一领域能力，无法评估通用智能体的真实水平。
  - 交互式基准（OSWorld、WebArena）虽设计了环境，但仅评估单平台内的隔离功能，任务长度仅约20步，复杂度远低于真实工作场景。
  - 基于强化学习的方法虽可通过参数更新积累知识，但样本效率低且仅限训练时优化；面对封闭/冻结的商用LLM（如GPT、Gemini），微调不可行，模型能力在训练结束后即被“冻结”。
  - 现有智能体的每次任务执行如同一场“失忆”过程：成功与失败经验都无法固化为有效知识，无法像人一样通过“熟能生巧”在重复任务中不断提升效率。
- **研究意义**：本文旨在突破“一次性交互”模型的局限，让智能体在**不做任何权重更新**的前提下，通过“在岗学习”（learning on the job）实现能力持续增长与自我演化。

## 2. 方法论：MUSE 框架

### 2.1 核心思想

MUSE（**M**emory-**U**tilizing and **S**elf-**E**volving）是一个以记忆模块为中心的、经验驱动的闭环系统。其核心逻辑可概括为**“计划（Plan）—执行（Execute）—反思（Reflect）—记忆（Memorize）”**四步循环。通过将原始动作轨迹自动蒸馏为结构化、可复用的知识，MUSE 使智能体的能力边界超越其静态预训练参数，实现动态演化。

### 2.2 层次化记忆模块（Memory Module M）

记忆模块由三种功能各异的记忆类型组成：

- **战略记忆（Strategic Memory, M_strat）**：
  - 保存智能体在任务中遇到的困境（Dilemma）及其解决策略（Strategy），以 `<Dilemma, Strategy>` 键值对形式存储。
  - 每次任务完成后由反思智能体抽象生成，并在系统提示词中全量加载，指导全局任务执行策略。
  - 通过合并、去重、精炼维持精简体积，防止上下文膨胀。

- **程序记忆（Procedural Memory, M_proc）**：
  - 以标准操作流程（SOP）形式归档成功的子任务轨迹，形成层次化知识库。
  - 索引结构为“应用名 → SOP索引 → 详细内容”；仅将轻量索引加载入上下文，细节内容按需通过专用工具主动检索，模拟人类专家查阅过往案例的方式。
  - 采用两阶段更新：子任务成功后立即动态新增SOP；整体任务完成后进行全局精炼（去重、泛化）。

- **工具记忆（Tool Memory, M_tool）**：
  - 充当智能体对单个工具使用的“肌肉记忆”，包含静态描述（启动时加载入系统提示词）和动态指令（工具使用后随环境观测返回）。
  - 每次任务结束后由反思智能体自动更新，指导智能体的下一步动作（如建议后续调用工具或进行某项分析）。

### 2.3 规划-执行智能体（PE Agent）

- **子任务规划与再规划**：PE Agent将主任务分解为有序子任务队列 `Q = [st₁, st₂, ..., st_M]`，每个子任务定义为 `(descᵢ, goalᵢ)` 元组；每完成一个子任务后根据新信息动态更新队列。
- **子任务执行与重试**：基于记忆增强的 ReAct 循环，即迭代“思考（θ）→ 动作（a）→ 观测（o）”。每个子任务设最大动作数 N（实验中 N=20），达到上限时由反思智能体介入评估并给予一次重试机会——重试时**不允许使用程序记忆**，以促进探索、发现新方法。
- **最小可用工具集**：仅配备浏览器交互、代码解释器、Shell、视觉提取器、记忆检索器五种通用工具，而非针对特定应用的专用API，强调“创造性地组合基础工具”而非机械调用预定义函数。
- **程序记忆检索机制**：启动时仅加载SOP索引，执行过程中通过内置工具按需查询详细SOP内容，兼顾效率与上下文长度限制。

### 2.4 反思智能体（Reflect Agent）

- **角色定位**：独立、第三方监督者，接收子任务定义与执行轨迹，且可直接与环境交互以独立验证信息。
- **三维度评估清单**：
  1. **真实性验证**：确保结论根植于实际环境反馈，抑制幻觉。
  2. **交付物验证**：检查所有输出文件/报告的完整性、存在性与正确性。
  3. **数据保真**：确认数据在处理过程中无丢失、截断或篡改。
- **两种核查方法**：
  1. **轨迹回溯**：将PE Agent的结论显式追溯到执行历史中的具体观测。
  2. **主动验证**：使用工具主动交互环境，用实时反馈交叉核验关键信息。
- **记忆更新机制**：评估输出成功/失败标志与详细报告；成功则提炼新SOP存入程序记忆；失败则生成失败原因分析报告。整体任务完成后，反思智能体进行全量记忆升级，提炼战略记忆与工具记忆，并对三类记忆统一精炼整合。

## 3. 实验设计

### 3.1 评估基准与数据集

- **基准**：TheAgentCompany（TAC）——一个高保真企业环境模拟基准，包含175个任务，覆盖6种核心职业角色（HR、PM、SDE等），平均每个任务约需40步动作，常跨两个以上应用，具有长时程、跨平台、高复杂度特点。
- **三个评测集合**：
  - **T_cl（连续学习集）**：从TAC中精选18个中等难度任务，覆盖全部6个职业角色。
  - **T_hard（泛化测试集）**：12个强模型（如Claude-4 Sonnet）几乎无法得分的极难任务，用于零样本泛化测试。
  - **完整TAC集**：全部175个任务，用于全面对比。

### 3.2 对比方法

- 与OpenHands、OpenHands-Versa、OWL-RolePlay等主流Agent框架对比；
- 对比模型包括：Gemini-2.5 Pro/Flash、Claude-4 Sonnet、Claude-3.7 Sonnet、GPT-4o + o3-mini、DeepSeek-V3等。
- 主要评估指标：部分完成分数（S_partial）与检查点完成率（S_ckpt）。

## 4. 资源与算力

- **论文未明确说明**使用了多少 GPU 型号、数量或训练时长。
- 从文中信息可推断：
  - PE Agent与Reflect Agent均使用 **Gemini-2.5 Flash**（轻量级商用模型），TAC环境中NPC由GPT-4o驱动；
  - 实验包含5次完整重复运行、3轮迭代，属于测试时推理（test-time inference），无需额外的模型训练成本；
  - 附录提及了上下文压缩机制（超过十倍压缩率）以控制token成本，但未给出具体算力投入数字。

## 5. 实验数量与充分性

### 主要实验组

| 实验类型 | 内容 | 数量 |
|---------|------|------|
| 连续学习实验 | 3轮迭代 × 5次完整运行（在T_cl上） | 图3 |
| 泛化实验 | 在T_hard上对比有/无记忆 | 表1 |
| 全基准评估 | 全部175个任务 | 表2 |
| 组件消融 | PE/Reflect/Memory三组逐步添加 | 表3 |
| 模型消融 | 开源模型（DeepSeek-V3）与闭源模型（Gemini 2.5 Flash/Pro） | 表4 |
| 案例分析 | 2个成功案例 + 2个失败案例分析 | 图4-7 |

### 充分性与公平性评估

- **优点**：实验设计较全面——既验证了连续学习能力（多轮迭代），也验证了跨任务泛化能力（记忆迁移至未见任务）；消融实验既有组件贡献分析、也有跨模型适配分析；重复运行取均值降低了随机性干扰。
- **客观性**：TAC官方评估协议具有确定性评分机制；对开源模型（DeepSeek-V3）和闭源模型均做了评估，结论具有较强说服力。
- **潜在不足**：
  - 连续学习实验T_cl仅18个任务，样本量相对有限；
  - 泛化实验仅12个任务，统计显著性可能受限；
  - 记忆模块仅在T_cl上积累3轮，其长期演化（更多轮次）行为未经充分验证。

## 6. 主要结论与发现

- **新SOTA成绩**：在TAC全175个任务上，MUSE仅用轻量级的Gemini-2.5 Flash模型即达到 **S_partial = 51.78%**，首次突破50%大关，较此前最强方法（OpenHands-Versa w/ Claude-4 Sonnet，43.19%）相对提升约20%。
- **持续自我演化**：在T_cl上连续学习3轮后，S_ckpt从基线（无记忆）稳步增长，最终较无记忆基线提升超过10%，表现单调稳定增长。
- **强跨任务迁移性**：在T_hard上，从T_cl学到的记忆带来显著提升（S_partial从23.65%升至33.41%），证明学到的是可迁移的通用知识而非任务记忆。
- **架构本身亦有增益**：即使无记忆模块，MUSE的PE+Reflect架构也已大幅超越同模型的其他Agent框架。
- **模型无关性**：记忆以自然语言存储，可跨LLM迁移——DeepSeek-V3和Gemini 2.5 Flash均能从同一份记忆中获益；Gemini 2.5 Pro + MUSE达到S_ckpt 80.00%。
- **效率与性能兼得**：记忆检索仅增加约97.86秒/任务的平均开销，却带来最大的性能增益。

## 7. 优点与亮点

1. **无需微调的测试时学习范式**：在闭源/冻结LLM上也能实现智能体的持续进化，实用性强。
2. **自动化的知识蒸馏**：无需人工标注或地面真值（GT-free），反思智能体在子任务粒度上实时验证和蒸馏知识，在全局失败的任务中仍能捕获有效的局部流程——相较于依赖GT筛选轨迹的ExpeL方法更具实际部署价值。
3. **层次化记忆设计合理**：战略/程序/工具三类记忆各司其职，从宏观策略到微观操作覆盖不同抽象层级；索引与内容分离的检索机制有效平衡了上下文长度与知识利用。
4. **最小工具集理念**：强调通用工具的组合运用而非专用工具堆砌，有利于发现创造性解决方案（如案例中通过创建多人聊天群组同时收集反馈）。
5. **创新的重试机制**：失败后重试禁用程序记忆，在“利用”与“探索”之间显式切换，有利于发现既有知识盲区。
6. **上下文压缩机制**：实现了超过十倍的token压缩率，显著控制成本，支持长时间运行。

## 8. 不足与局限

1. **架构适用边界**：作者承认当前记忆架构并非万能，在处理**高层级规划、多跳搜索**等特定任务时能力有限。
2. **基准本身的缺陷**：
   - TAC部分任务描述存在**语义歧义**或**轻微事实错误**，可能误导智能体推理。
   - 评估脚本较为**僵化**，无法覆盖所有合法解路径，导致智能体有效的创新方案（如创建群聊而非逐一对话）被低估或误判为零分。
3. **环境感知局限**：智能体的感知是被动、线性的，对PDF中嵌入的图片、Excel中的千位分隔符等非标准数据格式存在感知盲区，与人类的主动直觉和并行多模态感知存在差距。
4. **实验覆盖有限**：连续学习和泛化实验的任务量（18+12）在175个任务的全集中占比有限，记忆在更多任务类型上的长期演化效果未充分展现。
5. **缺少算力信息**：未明确报告训练/推理的具体算力消耗（GPU型号、数量等），可复现性和成本评估方面信息不足。
6. **仅评估单一基准**：未在OSWorld、WebArena等其他Agent基准上验证框架的通用性（尽管TAC复杂度更高）。

（完）
