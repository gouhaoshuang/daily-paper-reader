---
title: "Mobile-Agent-RAG: Driving Smart Multi-Agent Coordination with Contextual Knowledge Empowerment for Long-Horizon Mobile Automation"
title_zh: Mobile-Agent-RAG：上下文知识赋能的多智能体协同，推动长时程移动自动化
authors: "Yuxiang Zhou, Jichang Li, Yanhao Zhang, Haonan Lu, Guanbin Li"
date: 2026-03-17
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/40241/44202"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 面向移动端长时程任务的移动智能体，通过上下文知识增强规划与UI操作
tldr: 现有移动智能体在真实长时程跨应用任务上成功率偏低，主要瓶颈是过度依赖多模态大模型内部的静态知识，导致规划时出现策略幻觉、执行时出现UI操作错误。Mobile-Agent-RAG提出按层级分离知识的思路：高层规划依赖策略性经验，低层UI操作依赖精确指令，并通过检索增强为两者提供上下文知识。实验在真实移动自动化基准上验证了该方法显著提升任务成功率，为移动端任务执行智能体提供了可行框架。
source: AAAI-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40241/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1823, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40241/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1648, \"height\": 614, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40241/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 845, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40241/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1824, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40241/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 891, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40241/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 883, \"height\": 187, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40241/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1713, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40241/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 883, \"height\": 448, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40241/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 882, \"height\": 626, \"label\": \"Table\"}]"
motivation: 现有移动智能体在长时程跨应用任务上成功率低，主要因过度依赖MLLM内部静态知识。
method: 提出Mobile-Agent-RAG，通过检索增强为高层规划和低层UI操作提供异质上下文知识。
result: 在真实长时程移动自动化任务上显著提升成功率，减少策略幻觉和操作错误。
conclusion: 验证了按层级解耦知识可有效增强移动智能体，为移动自动化提供新范式。
---

## Abstract
Mobile agents show immense potential, yet current state-of-the-art (SoTA) agents exhibit inadequate success rates on real-world, long-horizon, cross-application tasks. We attribute this bottleneck to the agents' excessive reliance on static, internal knowledge within MLLMs, which leads to two critical failure points: 1) strategic hallucinations in high-level planning and 2) operational errors during low-level execution on user interfaces (UI). The core insight of this paper is that high-level planning and low-level UI operations require fundamentally distinct types of knowledge. Planning demands high-level, strategy-oriented experiences, whereas operations necessitate low-level, precise instructions closely tied to specific app UIs. Motivated by these insights, we propose Mobile-Agent-RAG, a novel hierarchical multi-agent framework that innovatively integrates dual-level retrieval augmentation. At the planning stage, we introduce Manager-RAG to reduce strategic hallucinations by retrieving human-validated comprehensive task plans that provide high-level guidance. At the execution stage, we develop Operator-RAG to improve execution accuracy by retrieving the most precise low-level guidance for accurate atomic actions, aligned with the current app and subtask. To accurately deliver these knowledge types, we construct two specialized retrieval-oriented knowledge bases. Furthermore, we introduce Mobile-Eval-RAG, a challenging benchmark for evaluating such agents on realistic multi-app, long-horizon tasks. Extensive experiments demonstrate that  Mobile-Agent-RAG significantly outperforms SoTA baselines, improving task completion rate by 11.0% and step efficiency by 10.2%, establishing a robust paradigm for context-aware, reliable multi-agent mobile automation.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究背景**：移动智能体（Mobile Agents）在手机自动化领域具有巨大潜力，但当前最先进（SoTA）的智能体在真实世界、长时程、跨应用任务上的成功率仍然很低。
- **核心问题**：作者将这一瓶颈归因于智能体过度依赖 MLLM（多模态大语言模型）内部的静态知识，由此引发两类关键失败：
  - **策略幻觉（Strategic Hallucination）**：高层规划阶段需要多步推理，模型仅凭内部知识容易生成错误或不可行的整体计划。
  - **操作错误（Operational Error）**：低层执行阶段需要精准的 UI 元素定位与原子动作生成，模型对具体 App 界面不熟悉，容易点击错误位置或选择错误操作。
- **核心洞察**：高层规划与低层 UI 操作需要**本质不同类型的知识**——规划需要策略导向的宏观经验，操作需要与具体 App UI 紧密绑定的微观指令。现有方法未区分这两类知识，统一依赖模型内部参数化知识，导致错误累积。

## 2. 论文提出的方法论

- **总体框架**：提出 **Mobile-Agent-RAG**，一个层级化多智能体框架，继承并扩展了 Mobile-Agent-E 的架构，核心创新在于将**双层级检索增强生成（Dual-Level RAG）**融入 Manager（管理器）与 Operator（操作器）两个核心智能体。
- **核心智能体与模块**：
  - **Manager Agent（管理器）**：负责高层战略规划与子任务分解，由 **Manager-RAG** 赋能。
  - **Operator Agent（操作器）**：负责将子任务转化为具体原子动作（如 Tap、Swipe、Type、Open App 等），由 **Operator-RAG** 赋能。
  - **Perceptor（感知器）**：将截图转换为结构化细粒度视觉信息（文本、图标、坐标、描述）。
  - **Action Reflector（动作反射器）**：比较动作前后 UI 状态，判断动作结果（成功/失败/无变化），更新进度与错误日志。
  - **Notetaker（笔记记录器）**：跨步骤聚合任务关键动态信息，维持长时程任务的上下文。
- **Manager-RAG（高层规划检索）**：
  - 在任务初始时刻（t=1），以用户任务指令为查询，从 Manager-RAG 知识库中检索 top-k 个最相关的人工作业步骤文档（任务指令 + 人类操作步骤）。
  - 使用 Contriever-MSMARCO 模型进行语义相似度检索。
  - 检索到的高层计划作为 few-shot 示例提供给 MLLM，生成整体计划 P 与子任务 T。
  - 目标：减少高层规划中的策略幻觉。
- **Operator-RAG（低层执行检索）**：
  - 当 Operator 即将执行原子动作时，以当前子任务+App 名为查询，在**该 App 专属的知识库**中检索 top-1 最相关的（子任务、截图、动作）文档。
  - 检索到的实例作为详细上下文供 MLLM 生成精确的原子动作（含精确坐标）。
  - 目标：提升低层 UI 操作精度。
- **知识库构建**：
  - **Manager-RAG 知识库（K_MR）**：由（任务指令，人类标注操作步骤）构成，直接提取自作者构建的 Mobile-Eval-RAG 数据集，人工收集与审核。
  - **Operator-RAG 知识库（K_OR^app）**：半自动化构建——在智能体执行过程中实时记录（子任务、截图、动作）三元组，再由人工标注者审核修正；按 App 分别建立独立检索库，避免跨 App 干扰。
- **执行流程**：感知 → 高层规划（Manager+RAG）→ 低层动作（Operator+RAG）→ 动作后感知 → 反射评估 → 信息聚合，构成动态迭代循环，直至任务完成或失败终止。

## 3. 实验设计

- **数据集/Benchmark**：作者新构建了 **Mobile-Eval-RAG** 基准，共 50 个多样化且具有挑战性的真实任务：
  - 在 Mobile-Eval-E 的 5 个类别（信息搜索、热点趋势、餐厅推荐、在线购物、旅行规划）基础上扩展。
  - 强调跨应用协同与长时程规划，平均 16.9 步，涉及 2-3 个 App。
  - 分为简单操作（信息搜索、热点趋势）与复杂操作（餐厅推荐、在线购物、旅行规划）两组；查询由 MLLM 生成并经人工验证。
- **对比方法**：与多种单智能体与多智能体 SoTA 方法对比，包括 AutoDroid、AppAgent (Auto)、AppAgent (Demo)、Mobile-Agent、Mobile-Agent-v2、Mobile-Agent-E、Mobile-Agent-E+Evo。
- **推理模型**：使用 Gemini-1.5-Pro（默认骨干）、GPT-4o、Claude-3.5-Sonnet 三种 MLLM。
- **评估指标**：成功率（SR）、完成率（CR）、操作准确率（OA）、反射准确率（RA），并新增步数（Steps）与效率（Efficiency）。

## 4. 资源与算力

- 论文中**未明确说明**使用的 GPU 型号、数量、训练时长等具体算力资源信息。
- 由于 Mobile-Agent-RAG 不涉及模型微调或训练，仅依赖提示工程与知识库检索，可以推断其算力开销主要在推理阶段（MLLM API 调用）与知识库构建阶段（人工+半自动采集），但论文未提供量化细节。

## 5. 实验数量与充分性

- **实验组数**：共约 4 组核心实验——
  1. 主实验（表 1）：与 7 个基线方法在单 App 与多 App 任务上的对比。
  2. 任务复杂度实验（表 2）：简单操作 vs 复杂操作任务的细分对比。
  3. 不同 MLLM 泛化实验（表 3）：3 种 MLLM（Gemini-1.5-Pro、GPT-4o、Claude-3.5-Sonnet）上的对比；图 4 展示了不同方法的性能增益来源。
  4. 消融实验（图 5a/5b、图 6）：去除 Manager-RAG 或 Operator-RAG 的变体对比；错误类型分布分析；10 次试验的 CR 稳定性对比。
- **充分性评估**：
  - **充分之处**：对比方法覆盖单/多智能体两大路线；评估了不同任务复杂度与不同骨干模型；消融实验覆盖两个核心模块；错误类型分析揭示了失败模式；10 次重复试验提供了稳定性证据。整体实验设计较为系统、合理。
  - **不足之处**：基准规模有限（仅 50 个任务）；没有与更多近期方法（如 AppAgent-v2、AppAgentX）直接对比；未做跨设备/跨 Android 版本的泛化测试；未报告推理时间成本与 API 调用开销。

## 6. 论文的主要结论与发现

- Mobile-Agent-RAG 在各项指标上显著超越所有基线，尤其在复杂多 App 任务上优势明显：
  - 主实验（Gemini-1.5-Pro）：CR 达 75.7%，相比 Mobile-Agent-E（58.3%）提升 17.4 个百分点，相比 Mobile-Agent-E+Evo（61.2%）提升 14.5 个百分点；OA 达 90.1%；SR 达 76.0%（Mobile-Agent-E 仅 48.0%）。
  - 步骤效率：18.8 步完成任务，高于基线（22.4 步）；Efficiency 4.03 vs 基线的 2.60/2.81。
- 任务复杂度方面：简单任务 CR 78.0%（提升 9.7~14.6 个百分点），复杂任务 CR 74.2%（提升 17.7~19.3 个百分点），说明 RAG 对复杂长时程任务的帮助更大。
- 不同 MLLM 上均表现一致：Gemini-1.5-Pro 上 CR 提升 23.6%，GPT-4o 上提升 5.8%，Claude-3.5-Sonnet 上提升 8.4%——**RAG 的收益与模型强度呈负相关**，对较弱模型补偿更大，对强模型仍有增益。
- 消融实验发现：移除 Operator-RAG 会显著降低 OA、Efficiency 和 SR（增加重复与错误低层动作）；移除 Manager-RAG 会降低最大可达 CR；二者互补——Manager-RAG 保障全局规划，Operator-RAG 保障精确执行。

## 7. 优点

- **问题洞察准确**：将“知识类型不匹配”作为核心切入点，区分策略性知识与操作知识，思路清晰合理。
- **架构设计巧妙**：在原有层级化多智能体框架（Manager/Operator）基础上，将 RAG 精准嵌入两个不同层级，双 RAG 设计与框架天然契合。
- **知识库构建严谨**：人工审核+半自动采集保证数据质量；按 App 隔离的 Operator-RAG 知识库提高检索精度，避免跨应用干扰。
- **基准设计合理**：Mobile-Eval-RAG 面向 RAG 评估，任务覆盖真实场景与跨应用协同，难度区分明确。
- **实验分析充分**：不仅报告主结果，还做了任务复杂度、多种 MLLM、消融、错误类型、稳定性等多维度分析。
- **开源可复现**：提供代码与补充材料。

## 8. 不足与局限

- **基准规模偏小**：仅 50 个任务，统计功效有限，可能不足以完全反映模型在不同场景下的真实表现。
- **知识库构建代价高**：依赖大量人工标注与修正，扩展到更多 App 和新任务时成本较高，实际部署的可持续性存疑。
- **检索模型局限性**：使用 Contriever-MSMARCO 进行语义相似度检索，对任务指令表达方式的变化（词汇改写、语序变化等）可能不够鲁棒。
- **基线与对比范围有限**：未与 AppAgent-v2、AppAgentX、M3A 等近期框架对比；也未与纯强化学习或微调类方法比较。
- **算力/成本信息缺失**：未报告 API 调用次数、推理延迟、经济成本等，不利于实际应用评估。
- **MLLM 间增益不均衡**：在 GPT-4o 与 Claude-3.5-Sonnet 等较强模型上增益较小（CR 仅提升约 6~8 个百分点），说明方法对强模型的边际收益正在收窄。
- **设备与系统泛化未知**：未测试不同 Android 设备、分辨率或操作系统版本上的表现。
- **错误类型分析较粗**：仅划分三类失败模式（步骤过多、判断错误、重复动作），未深入分析 RAG 检索失败等场景的具体影响。

（完）
