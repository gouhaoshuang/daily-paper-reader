---
title: "Mem2ActBench: A Benchmark for Evaluating Long-Term Memory Utilization in Task-Oriented Autonomous Agents"
title_zh: Mem2ActBench：面向任务导向自主智能体长期记忆利用评估的基准
authors: "Yiting Shen, Kun Li, Wei Zhou, Songlin Hu"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.370.pdf"
tags: ["query:mobile-agent"]
score: 4.0
evidence: 面向任务型智能体主动记忆利用的基准，与移动任务执行中的记忆技术相关
tldr: 针对现有基准只测被动检索、不测主动记忆应用的问题，提出Mem2ActBench，模拟用户在同一话题上的长期中断交互，评估智能体是否能在执行工具任务时主动利用长期记忆选择合适的工具并设置参数。为移动端个性化助手等任务型智能体的记忆能力评测提供了更贴近实际使用的方式。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long370/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 689, \"height\": 962, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long370/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1546, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long370/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 777, \"height\": 605, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long370/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 945, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long370/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 799, \"height\": 667, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1645, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 801, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 801, \"height\": 628, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1642, \"height\": 385, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 719, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 805, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1728, \"height\": 1605, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1668, \"height\": 626, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long370/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1652, \"height\": 671, \"label\": \"Table\"}]"
motivation: 现有记忆基准仅测试被动检索，缺乏对记忆驱动任务执行能力的评估。
method: 设计模拟持续用户交互的基准，要求智能体主动利用记忆完成工具任务。
result: 检验了智能体在工具选择与参数设置中利用长期记忆的能力。
conclusion: 为评估任务型智能体的记忆利用提供了更实际的评测手段。
---

## Abstract
Large Language Model (LLM)-based agents are increasingly deployed for complex, tool-based tasks where long-term memory is critical to driving actions. Existing benchmarks, however, primarily test an agent’s ability to passively retrieve isolated facts in response to explicit questions. They fail to evaluate the more crucial capability of actively applying memory to execute tasks. To address this gap, we introduce Mem2ActBench, a benchmark for evaluating whether agents can proactively leverage long-term memory to execute tool-based actions by selecting appropriate tools and grounding their parameters. The benchmark simulates persistent assistant usage, where users mention the same topic across long, interrupted interactions and expect previously established preferences and task states to be implicitly applied. We build the dataset with an automated pipeline that merges heterogeneous sources (ToolACE, BFCL, OASST1), resolves conflicts via consistency modeling, and synthesizes 2,029 sessions with 12 user–assistant–tool turns on average. From these memory chains, a reverse-generation method produces 400 tool-use tasks, with human evaluation confirming 91.3% are strongly memory-dependent. Experiments on seven memory frameworks show that current systems remain inadequate at actively utilizing memory for parameter grounding, highlighting the need for more effective approaches to evaluate and improve memory application in task execution. Code and data are available at https://github.com/Cantaloupe-M/Mem2ActBench.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究背景**：基于大语言模型（LLM）的智能体（agent）被越来越多地部署到复杂的、基于工具（tool-based）的长期任务中。在这些场景下，长期记忆（long-term memory）对于驱动智能体行为至关重要。用户通常会跨多次、被其他无关对话打断的交互中，逐步建立偏好、需求和部分任务状态，并隐含地期望智能体记住并在后续请求中主动应用这些信息。
- **核心问题**：现有的记忆基准（如 MSC、LoCoMo 等）主要测试智能体**被动检索**孤立事实的能力（如回答“用户的预算是多少？”），而忽略了更关键的能力——**主动将长期记忆应用到工具调用中**，即根据欠指定（underspecified）的指令，推断需要从记忆中检索哪些约束，将其转化为可执行的工具调用参数（如 `destination="NYC", max_price=500, non_stop=True`）。
- **论文意义**：为评估任务型智能体的记忆利用能力提供了更贴近实际使用场景的评测方式，填补了“记忆驱动任务执行”评测的空白。

## 2. 论文提出的方法论

- **总体思路**：引入 **Mem2ActBench**，通过三阶段自动化 pipeline 构建基准，评估智能体能否从分散在长历史对话中的记忆中重构可执行的工具参数。
- **阶段一：异构数据整合**
  - 从 **ToolACE**（8000 个样本）和 **BFCL_v3** 中获取任务导向的工具使用轨迹，通过 LLM 重构为连贯、自然的多轮对话。
  - 从 **OASST1** 注入会话噪音（conversational noise），模拟真实世界中被中断的交互。
- **阶段二：事实演化链（Memory Evolution Chain）构建**
  - **事实抽取**：LLM 抽取结构化三元组 `(attribute, fact, source_id)`，使用“实体绑定”的 attribute 避免跨实体误合并。
  - **语义聚类**：用 BERTopic（HDBSCAN 后端）对 attribute 聚类，映射至统一规范名。
  - **局部冲突消解**：对每个事实组，LLM 按时间排序、保留逻辑有效的更新（如细化、多值轨迹）、移除冲突/重复事实。
  - **全局演化序列构建**：构建依赖图，使用基于 Kahn 算法的改进拓扑排序；遇到环（冲突）时，确定性启发式地移除“出度最大”的节点（字典序作为平局裁决）。
- **阶段三：基于记忆的问答（Memory-anchored Q&A）构建**
  - **目标工具选择**：混合检索（BM25 + BGE-M3）+ LLM 决策选定目标工具。
  - **参数锚定**：参数值必须能从记忆链中显式提取（explicit）或逻辑推断（inferred），通过模糊匹配 + LLM 验证器进行校验。
  - **反向隐式查询生成**：从已确定的工具调用逆向生成欠指定用户查询，强制满足三条约束：参数省略（不泄露关键值）、指代依赖（使用“book that flight"等指代表达）、意图保持（语义一致）。
  - **筛选与护栏**：① 词法泄漏过滤（规则：精确匹配、数字、token 重叠、结构化标识符）；② 可解性判别器（Blinded LLM Discriminator）——只给查询和工具 schema，若判别器能正确推断参数则拒绝样本。
- **任务形式化**：定义为条件生成问题，给定记忆序列 M 和用户查询 q，最大化正确工具调用 c 的概率；每个参数值需严格锚定于 M。

## 3. 实验设计

- **核心 benchmark**：
  - 共 **400 个**记忆依赖的工具使用任务，源自 **2,029 个**长上下文对话会话（平均 12–13 轮/会话）。
  - 人类验证：事实抽取准确率 96.5%，冲突消解质量 86.7%，记忆依赖有效性 91.3%。
- **评测数据子集**：从全部会话中选出包含 QA 所需证据的 **429 个会话**用于实验。
- **对比方法（7 种记忆框架）**：
  - LTMemory（RAG）、Generative Agents、SCM、Langmem、MemTree、Mem0、A-mem。
- **骨干模型**：Qwen2.5-7B-Instruct、Qwen2.5-32B-Instruct、Qwen2.5-72B-Instruct 三种规模；固定 decoding（temperature=0.0）；检索用 BGE-m3 嵌入。
- **评测指标**：
  - **F1**（参数层面精确率/召回率）；
  - **BLEU-1**（一元词组重叠）；
  - **Tool Accuracy (TA)**（工具正确且所有参数完全匹配）。
- **辅助实验**：
  - 检索策略对比：无检索 vs. 被动检索（BM25/Dense/Hybrid，top-k ∈ {1,5,10}）vs. 完美检索（Oracle）。
  - 记忆距离分析：按最早支撑记忆的归一化位置分四桶（0–25%, 25–50%, 50–75%, 75–100%）。
  - 参数类型与值复杂度分解：Explicit/Inferred/Default × Simple String/Number/Boolean/Complex。
  - 工具选择鲁棒性：候选工具集 N ∈ {1, 2, 5}，随机负样本 vs. 硬负样本。
  - 失败模式诊断：五类错误（Retrieval Miss、Retrieved-but-Unused、Hallucinated Default、Lossless Retention Failure、Tool Selection Error）。
  - 缓解策略评估：Query Expansion、Self-Refine、Interactive Clarification（在 200 样本子集上）。

## 4. 资源与算力

- **论文未明确报告 GPU 型号、数量及训练时长**等具体算力配置。
- 仅在相关部分提到使用 **Qwen3-Next-80B-A3B-Instruct**（数据构建的事实抽取/工具选择）和 **Kimi-K2-Thinking**（反向查询生成），以及推理骨干使用 **Qwen2.5 系列三种规模**的模型，但没有给出具体的推理成本、GPU 卡时等量化数据。

## 5. 实验数量与充分性

- **实验数量**：实验覆盖面较广，包含 7 种方法 × 3 种模型规模的主实验、检索消融（3 策略 × 3 档 top-k）、记忆距离分析、参数复杂度分解、工具选择鲁棒性（N×2 类负样本）、失败模式归因、3 种缓解策略对比，共约数十组量化实验。
- **充分性**：
  - **优点**：多维度、多层次的评测设计，既考察了整体指标也深入分析了失败原因；消融实验（检索条件）和鲁棒性实验（硬/软负样本）增强了结论的可信度；人类验证覆盖三个关键构建阶段。
  - **不足**：所有实验仅基于 Qwen2.5 一个模型家族，无法排除骨干模型偏好带来的偏差；数据只有 400 个任务，规模相对较小；缓解策略只在 200 样本子集上评估；Interactive Clarification 改变了任务定义，作者也承认其与单轮设置不完全可比。

## 6. 论文的主要结论与发现

- **当前记忆系统在主动利用记忆进行参数锚定方面存在显著不足**：所有方法在 72B 规模下平均 F1 仅约 29%，远低于理想水平。
- **检索是主要瓶颈**：无检索 F1≈10.0，被动检索最佳 F1≈30.7，而 Oracle 检索可达 F1≈53.8，差距超过 23 个点，说明核心瓶颈在于证据命中/检索质量而非推理能力。
- **存在“中部记忆低谷”现象**：多数方法在支撑记忆位于历史中间段（25–50%）时性能显著下降，类似“lost-in-the-middle”效应；LTMemory 相对更稳健。
- **参数锚定错误集中在 Default 值**：模型常未察觉到参数从未被指定，而编造看似合理的默认值；复杂值（长字符串、URL、结构化标识符）的保留也较差。
- **工具选择在无关干扰下鲁棒，但对语义相似工具易出错**：随机负样本下 TSA 保持 93%+，硬负样本下从 94.50%（N=1）降至 69.75%（N=5）。
- **失败模式随系统能力迁移**：弱系统以 Retrieval Miss 为主，强系统中 Retrieved-but-Unused 比例上升，表明检索到≠被正确利用。
- **交互式澄清可大幅提升参数 F1**（→48.68），是绕过静态检索瓶颈的有效方向。

## 7. 优点

- **问题定义新颖且实际**：从“被动事实检索”转向“主动记忆驱动的任务执行”，更贴近真实助手使用场景。
- **构建流程严谨**：自动化 pipeline 包含事实抽取、聚类、局部/全局冲突消解、反向生成、双重泄漏过滤（规则 + 判别器），各环节有质量护栏。
- **人类验证充分**：五个专家对三个关键阶段进行验证，验证率分别为 96.5%（事实）、86.7%（冲突消解）、91.3%（记忆依赖性）。
- **多维度的实验分析**：不仅报告主结果，还深入拆解了检索条件、记忆位置、参数类型、值复杂度、工具选择鲁棒性、失败模式及缓解策略，诊断价值高。
- **错误归因清晰**：五类失败模式的细粒度划分有助于社区理解现有系统的瓶颈。

## 8. 不足与局限

- **骨干模型覆盖单一**：仅用 Qwen2.5 一个家族，外部效度受限；作者也承认跨家族评估成本过高。
- **任务规模相对有限**：400 个任务、429 个测试会话，尚不足以覆盖所有可能的记忆-工具交互模式。
- **离线静态评估**：不包含交互式执行、多轮反馈适应等真实部署场景，Interactive Clarification 实验虽然展示了潜力但改变了任务定义，不可严格对比。
- **数据合成偏差风险**：自动化生成（LLM 重构、翻译）可能无法完全捕捉真实用户语言的自然性和歧义性；OASST1 非英语样本经机器翻译可能引入失真。
- **人工验证偏差**：作者承认人类验证在边缘案例上可能引入主观偏差，尽管有分歧解决策略。
- **冲突消解启发式**：全局排序中“移除最大出度节点”的启发式虽然确定性好，但可能并非最优的冲突处理策略，可能丢失语义上重要的约束。
- **相关记忆的定位方式影响分析**：tearliest 的选择可能低估同一参数在多个位置出现时的影响。

（完）
