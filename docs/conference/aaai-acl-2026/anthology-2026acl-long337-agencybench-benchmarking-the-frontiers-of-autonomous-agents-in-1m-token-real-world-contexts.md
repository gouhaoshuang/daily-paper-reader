---
title: "AgencyBench: Benchmarking the Frontiers of Autonomous Agents in 1M-Token Real-World Contexts"
title_zh: AgencyBench：百万词元真实世界上下文中自主智能体前沿能力基准测试
authors: "Keyu Li, Junhao Shi, Yang Xiao, Mohan Jiang, Jie Sun, Yunze Wu, Dayuan Fu, Shijie Xia, Xiaojie Cai, Tianze Xu, Weiye Si, Wenjie Li, Dequan Wang, Pengfei Liu"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.337.pdf"
tags: ["query:mobile-agent"]
score: 4.0
evidence: 面向长上下文自主智能体的综合基准，可应用于移动智能体框架评测
tldr: 针对现有基准只关注单一智能体能力且依赖人工反馈导致扩展性差的问题，提出AgencyBench，基于日常AI使用构建138个任务、32个真实场景，评估六个核心智能体能力，平均需要约90次工具调用和百万词元上下文。为包括移动端在内的复杂自主智能体提供了更贴近真实的评测基准。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long337/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 788, \"height\": 792, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long337/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1633, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long337/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1646, \"height\": 768, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long337/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1496, \"height\": 542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long337/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1498, \"height\": 939, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1478, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1638, \"height\": 564, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 830, \"height\": 559, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1419, \"height\": 574, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 779, \"height\": 565, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 562, \"height\": 486, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 663, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long337/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1676, \"height\": 730, \"label\": \"Table\"}]"
motivation: 现基准确难以覆盖长程真实场景，且依赖人在回路反馈造成扩展瓶颈。
method: 构建源自日常使用的综合基准，包含多场景、多能力任务和具体评分规则。
result: 提供了包含138个任务的基准，任务平均需90次工具调用，测评了六个能力。
conclusion: 为自主智能体的大规模自动化评估提供了可行范式。
---

## Abstract
Large Language Models (LLMs) based autonomous agents demonstrate multifaceted capabilities to contribute substantially to economic production. However, existing benchmarks remain focused on single agentic capability, failing to capture long-horizon real-world scenarios. Moreover, the reliance on human-in-the-loop feedback for realistic tasks creates a scalability bottleneck, hindering automated rollout collection and evaluation. To bridge this gap, we introduce AgencyBench, a comprehensive benchmark derived from daily AI usage, evaluating 6 core agentic capabilities across 32 real-world scenarios, comprising 138 tasks with specific queries, deliverables, and rubrics. These scenarios require an average of 90 tool calls, 1 million tokens, and hours of execution time to resolve. To enable automated evaluation, we employ a user simulation agent to provide iterative feedback, and a Docker sandbox to conduct visual and functional rubric-based assessment. Experiments reveal that closed-source models significantly outperform open-source models (48.4% vs 32.1%). Further analysis reveals significant disparities across models in resource efficiency, feedback-driven self-correction, and specific tool-use preferences.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

**研究动机与背景：**

- 随着大语言模型（LLMs）能力的快速提升，基于LLM的自主智能体（autonomous agents）已具备巨大的经济生产潜力，涵盖了软件开发、科学研究、日常使用等多个领域。
- **现有基准测试存在两大核心缺陷**：
  1. **缺乏长程（long-horizon）真实世界任务**：现有基准大多聚焦于单一智能体能力（如工具使用、软件工程或研究），任务深度不足（通常只有少量工具调用），无法反映真实世界中复杂的、多步骤的问题解决过程，也难以有效区分前沿模型的性能上限。
  2. **依赖人工反馈造成扩展瓶颈**：完成真实任务往往需要人类在回路中（human-in-the-loop）提供多轮、持续性的反馈来引导智能体，这使得自动化的数据收集与评估变得十分困难，规模无法扩展。

**论文提出的整体解决方案：**

- 论文引入了 **AGENCY BENCH**——一个源于日常AI使用场景的综合基准测试，以 **1M级token上下文、约90次工具调用、数小时执行时间** 的高难度任务为标准，系统性地衡量自主智能体在真实、长程场景中的综合表现。

## 2. 论文提出的方法论

### 2.1 核心设计思想：层级结构

- AGENCY BENCH 采用 **"能力（Capabilities）→ 场景（Scenarios）→ 任务（Tasks）"** 的三层层级结构：
  - 评估 **6种核心智能体能力**：游戏开发、前端开发、后端开发、代码生成、研究、MCP（Model Context Protocol）工具使用。
  - 覆盖 **32个真实世界场景**（如从零开发五子棋游戏、项目级代码调试、深度企业调研等）。
  - 总计 **138个具体任务**。每个场景由 1 至 5 个按难度递增、顺序呈现的任务构成，前置任务的完成情况会直接影响后续任务，从而模拟真实世界中由简到繁的工作流，考验智能体的长程上下文保持与执行能力。

### 2.2 任务三大核心组件

- 每个任务由三位一体的规范定义：
  - **Query（查询）**：描述具体的任务需求。
  - **Deliverables（交付物）**：定义预期的文件输出或终端状态。
  - **Rubrics（评分规则）**：建立客观的评估标准。
- 所有数据由 **20位人类专家**（AI研究员、AI实践者、软件工程师）手工构建与验证，并遵循 **100%一致同意政策**：任务只有在所有专家完全同意后才能最终定稿。

### 2.3 自动化评估框架

论文开发了一个完全自动化的"闭环"评估框架，以绕过人工反馈瓶颈：

- **工作区（Workspace）**：每个任务在隔离的工作区中运行，配备代理脚手架（含文件操作、命令行、网络搜索、上下文管理等工具），智能体与模拟环境进行多轮交互以生成交付物。
- **用户模拟代理（User Simulation Agent）**：扮演"用户"角色，当任务评分未达到阈值时，该代理会基于评分规则自动生成具体的、可操作的失败原因反馈，指导智能体进行迭代修复。该代理的可靠性已通过人工验证研究确认为高度一致（平均得分4.69/5）。
- **Docker沙箱环境**：交付物被同步到 Docker 远程沙箱中，该沙箱模拟人类计算机操作（如鼠标点击、UI渲染、屏幕录制），生成视觉化评估工件。
- **评估空间（Eval-space）**：在独立的评估空间中，通过可执行脚本对视觉工件和原始交付物进行基于评分规则的自动化评估（规则评估 + LLM-as-Judge多模态评估）。

### 2.4 评估指标

论文定义了四个关键指标：
- **平均得分（SAvg）**：基于评分规则的百分比得分。
- **平均尝试次数（Att）**：每个场景的平均迭代轮数，衡量智能体的自主性与纠错能力，数值越低越好。计算公式为：`Att = MAtt / M`。
- **通过率（Pass@k）**：在 k 轮反馈内达到60%得分阈值的任务比例。
- **效率（Efficiency）**：包括尝试效率（Eatt = SAvg / Att）和Token效率（Etok = SAvg / Tok），用于归一化性能与资源消耗的比值。

## 3. 实验设计

### 3.1 基准测试构成

- **任务数量**：138个任务，分布在32个真实场景中，覆盖6种核心能力（游戏开发50个任务，代码29个，前端/后端各15个，研究19个，MCP 10个等）。
- **任务规模**：单个场景平均需约 **90次工具调用**、消耗 **约100万token**、执行时间 **需数小时**，显著高于现有基准。

### 3.2 对比模型

- **闭源模型**：GPT-5.2、Claude-4.5-Opus、Claude-4.5-Sonnet、Gemini-3-Pro、Grok-4.1-Fast。
- **开源模型**：GLM-4.6、DeepSeek-V3.2、Qwen-3-235B-A22B-Thinking、Kimi-K2-Thinking。
- 所有模型均通过 OpenRouter API 访问，温度设置为0.7。

### 3.3 附带实验

- **用户模拟反馈影响实验**：比较 Pass@1 和 Pass@2 之间的提升幅度（Rise%），衡量模型的反馈驱动自我纠错能力。
- **资源消耗对比实验**：比较各模型的token消耗量（百万级）、执行时间和工具调用轮数。
- **效率分析实验**：绘制尝试效率和Token效率对比图。
- **工具调用模式分析实验**：统计各模型在不同工具（如 shell命令、文件读写、内存管理等）上的调用频率，揭示行为特征。
- **Agentic Scaffold的影响消融实验**：在10个代表性场景上，使用了三种框架（自有脚手架、Claude-Agent-SDK、OpenAI-Agents-SDK），评测不同脚手架对模型性能的影响。

## 4. 资源与算力

- **论文未明确说明** 训练或实验使用了多少GPU型号、数量或具体的算力消耗。
- 论文仅提及所有模型通过 **OpenRouter API** 访问（云端推理），并报告了 **推理阶段** 的token消耗（如GPT-5.2平均消耗340万token、Claude-4.5-Sonnet消耗410万token）和运行时间（如Kimi-K2-Thinking和Qwen-3系列平均每场景耗时约1.2~1.4小时）。
- 因此，论文 **缺乏关于训练成本或本地推理硬件配置的详细披露**。

## 5. 实验数量与充分性

### 5.1 实验数量

- **主实验**：在138个任务上，对9个前沿模型（5闭源+4开源）进行了系统评估。
- **消融实验**：1组脚手架对比实验（在10个代表性场景上，3种不同脚手架）。
- **可靠性验证实验**：
  - 用户模拟代理有效性研究（50条采样交互，4位专家独立验证，得分4.69/5）。
  - LLM评判者与人类标注对比（50个保留任务，Kappa系数0.93）。
  - 人类专家对任务数据集的全面审查（4位专家，100%一致同意政策）。

### 5.2 实验充分性与客观性评估

- **优点**：实验设计较为全面，不仅对比了整体得分，还从反馈纠错、资源效率、工具偏好、脚手架敏感度等多维度进行了深度剖析，展现了模型的差异化行为特征。
- **公平性考量**：论文使用统一脚手架对所有模型进行评估，基本保证了对比的公平性；采用可视化、规则化和LLM评判相结合的方式，减少了单一评估源的偏差。
- **不足之处**：尽管实验数量丰富，但部分分析（如工具调用模式、资源效率）基于的是平均数或有限的描述性统计，缺乏更细粒度的统计分析（如方差、显著性检验）；用户模拟代理的反馈质量虽经验证，但仍可能无法完全模拟真实人类用户复杂、微妙的沟通方式；评估集中于软件/数字环境，未覆盖需要物理世界交互的具身智能场景。

## 6. 论文的主要结论与发现

1. **闭源模型显著优于开源模型**：闭源模型平均得分48.4%，开源模型平均32.1%，差距明显。
2. **GPT-5.2 综合表现最佳**：在闭源模型中得分最高（56.5%），在反馈驱动的自我纠错、后端和代码生成能力上表现突出；**GLM-4.6 领跑开源阵营**（38.6%），但Qwen-3-235B-A22B-Thinking得分最低（27.0%）。
3. **前沿模型仍有较大提升空间**：即使在AGENCY BENCH上表现最好的GPT-5.2，得分也仅56.5%，说明当前模型在长程真实任务上并未真正"掌握"。
4. **模型能力存在明显分化与"个性"**：
   - **Gemini-3-Pro** 主导游戏与前端开发场景，并展现出独特的显式内存管理策略。
   - **Claude-4.5-Sonnet** 在研究任务上得分最高（71.4%）。
   - **GroK-4.1-Fast** 具有最高的Token利用效率和经济性。
   - **Claude-4.5-Opus** 和 **GPT-5.2** 偏好shell类工具（"执行者"），**Gemini-3-Pro** 偏好文件与内存工具，**GLM-4.6** 偏好文件覆盖与导航，**Qwen-3** 高度依赖文件操作。
5. **反馈驱动的自我纠错能力存在显著差异**：GPT-5.2通过额外反馈提升明显（Rise 88.9%），而DeepSeek-V3.2几乎无法从反馈中受益（0.0%提升）。
6. **"生态协同效应"（Ecosystem Synergy）显著**：模型在与其原生的Agentic Scaffold协同工作时表现最佳。例如，Claude-4.5-Opus 在 Claude-Agent-SDK 上性能提升20.5%，GPT-5.2在OpenAI-Agents-SDK上表现更好；这揭示模型性能并非纯粹的模型内在属性，而是"模型+脚手架"耦合后的结果。

## 7. 优点

- **真实性与长程性**：任务源自日常AI使用，包含大量真实的、多步骤、长时耗且上下文密集的场景（平均1M token），远超市面上大多数基准的规模与难度。
- **全自动化评估框架**：通过"用户模拟代理 + Docker沙箱 + 多模态LLM评判"的集成设计，绕过了人工反馈的扩展瓶颈，实现了大规模、可复现的自动评估。
- **分级与多维度的指标体系**：不仅关注最终得分，还通过平均尝试次数、反馈纠错提升幅度（Pass@1→Pass@2）、资源使用效率等指标，从"能力"与"经济效率"两个维度对智能体进行立体评估。
- **严格的评估可靠性验证**：通过人类评估用户模拟代理的有效性（4.69/5），并通过Kappa系数（0.93）验证LLM评判者（文本和视觉）与人类判断的高度一致性，保障了自动评估的可信度。
- **深度的行为模式分析**：不仅报告性能分数，还细致地分析了不同模型的工具调用偏好、内存管理策略、自我纠错机制和脚手架耦合效应，为后续研究提供了丰富的洞察。
- **工程上考虑了任务隔离与可复现性**：Workspace与Eval-space的分离和Docker沙箱的应用确保了环境的一致性和无跨任务干扰。

## 8. 不足与局限

- **模型覆盖的时效性**：由于LLM领域快速演进，评估所选取的模型组合无法穷尽所有最新的模型变体、中间版本或特定微调模型，研究结果只能代表当前时间点的一个"快照"。
- **领域特定性**：该基准聚焦于计算机软件界面内的数字环境任务（如游戏开发、软件工程、网络研究），不涉及具身智能（Embodied AI）或需要物理世界交互的任务（如机器人），限制了结论的泛化范围。
- **评估方法的固有偏差风险**：尽管LLM评判与人类判断有很高的一致性（Kappa 0.93），但在带有主观审美或开放性解答的任务中（如游戏视觉效果、前端设计），LLM评判仍可能带有系统性偏好，无法完全等同于真实用户的主观感受。
- **用户模拟代理的忠实度**：虽然用户模拟代理被验证高度一致，但它本质上是基于评分规则生成的反馈，可能无法完全捕捉真实人类用户微妙、复杂的意图（如"我觉得这里风格不对"），这可能会使智能体在真实部署环境中的泛化受影响。
- **计算资源与成本的不透明性**：论文未详细披露构建该基准（含专家评审、脚本开发等）以及模型评估时使用的具体算力资源（GPU型号/数量/训练时长），不利于研究者复制或评估该工作的工程成本。
- **对高难度任务"通过"的定义存在武断性**：以60%得分为及格线（Pass）来区分成功与失败，这一阈值的选定缺乏针对不同任务复杂度的差异化论证。

（完）
