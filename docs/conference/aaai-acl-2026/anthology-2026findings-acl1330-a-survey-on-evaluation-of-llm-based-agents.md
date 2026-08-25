---
title: A Survey on Evaluation of LLM-based Agents
title_zh: 基于LLM的智能体评估综述
authors: "Asaf Yehudai, Lilach Eden, Alan Li, Guy Uziel, Yilun Zhao, Roy Bar-Haim, Arman Cohan, Michal Shmueli-Scheuer"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1330.pdf"
tags: ["query:mobile-agent"]
score: 4.0
evidence: 关于LLM智能体评估方法的综述，涵盖评估框架与基准，但非移动端特定
tldr: 该论文系统综述了基于LLM的智能体评估方法，围绕核心LLM能力、应用特定基准、通用智能体评估、基准维度分析以及评估框架与工具五个视角进行全面梳理。它指出现有评估正转向更真实、更具挑战性且持续更新的基准，并归纳了对智能体开发者有实用价值的评估工具与平台。尽管该综述并未专门聚焦移动智能体，但其提出的评估维度、框架和方法论可作为移动智能体任务执行评估的重要参考，帮助研究者设计更贴近真实移动场景的评测方案。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1330/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1656, \"height\": 984, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1330/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1656, \"height\": 1979, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1330/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 815, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1330/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1654, \"height\": 294, \"label\": \"Table\"}]"
motivation: LLM智能体的评估方法分散且缺乏系统梳理，需从多视角总结现状与趋势。
method: 从核心LLM能力、应用基准、通用智能体、基准维度与评估工具五个视角对智能体评估领域进行综述分析。
result: 揭示了评估向更真实、动态更新的基准演进的趋势，并归纳了评估框架与工具。
conclusion: 为智能体开发者提供评估方法的全面参考，有助于构建更可靠的评估体系。
---

## Abstract
LLM-based agents represent a paradigm shift in AI, enabling autonomous systems to plan, reason, and use tools while interacting with dynamic environments. This paper provides the first comprehensive survey of evaluation methods for these increasingly capable agents. We analyze the field of agent evaluation across five perspectives: (1) Core LLM capabilities needed for agentic workflows, like planning, and tool use; (2) Application-specific benchmarks such as web and SWE agents; (3) Evaluation of generalist agents; (4) Analysis of agent benchmarks’ core dimensions; and (5) Evaluation frameworks and tools for agent developers. Our analysis reveals current trends, including a shift toward more realistic, challenging evaluations with continuously updated benchmarks. We also identify critical gaps that future research must address—particularly in assessing cost-efficiency, safety, and robustness, and in developing fine-grained, scalable evaluation methods.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

LLM-based agents（基于大语言模型的智能体）代表了人工智能领域的范式转变，使自主系统能够规划、推理、使用工具并与动态环境交互。与传统静态 LLM 不同，这类智能体具备多步决策、工具调用、环境交互和自适应规划的能力。然而，这种从"静态文本生成模型"向"自适应交互体"的转变，对评估方法提出了全新要求：评估必须超越度量 LLM 的文本输出，转而评估智能体的序列决策能力和在动态环境中的操作能力。

当前该领域缺乏对 LLM 智能体评估方法的系统性梳理。这篇论文正是针对这一空白，首次对 LLM 智能体的评估方法进行了全面综述，旨在为开发者、基准创建者、实践者和研究人员提供当前评估格局的完整映射，并识别未来研究的关键缺口。

主要研究动机可概括为：
- LLM 智能体评估的标准与维度高度分散，缺乏统一分析框架；
- 评估基准需要与智能体能力同步演进，不能静态停滞；
- 真实世界应用（尤其是企业级部署）对智能体的安全性、鲁棒性和成本效益提出了新的评估需求。

## 2. 论文提出的方法论：核心思想、关键技术细节、评估框架

论文采用**五视角结构化的综述方法论**，将智能体评估领域划分为五个相互关联的分析维度：

### （1）核心 LLM 能力评估（§2）
从四个关键能力维度对智能体进行递进式拆解评估：

- **规划与多步推理（Planning & Multi-Step Reasoning）**：从经典的数学推理（GSM8K、MATH）和问答基准（HotpotQA），到专门的规划基准（PlanBench、Natural Plan、FlowBench）。研究表明，即便最先进的模型在长程规划上仍面临困难。
- **函数调用与工具使用（Function Calling & Tool Use）**：从早期的一步式交互基准（ToolAlpaca、ToolBench、BFCL v1），演进到多轮交互和多步逻辑（BFCL v2/v3、NESTFUL、ComplexFuncBench），再到基于真实 MCP 服务器的大规模工具基准（MCP Atlas、Tool-Decathlon）。
- **自我反思（Self-Reflection）**：评估智能体基于反馈动态调整推理或行动的能力。相关基准包括 LLM-Evolve、LLF-Bench，但作者指出"标准化评估自我反思的基准或方法论仍是关键缺口"。
- **记忆（Memory）**：从长上下文基准（QUALITY、NarrativeQA）到专用智能体记忆基准（StreamBench、MemBench、MemoryAgentBench），区分情景记忆、语义记忆和程序性记忆。

### （2）应用特定智能体评估（§3）
聚焦四类代表性应用场景：

- **Web 智能体**：从早期简化模拟（WebShop）向真实动态环境演进（Mind2Web、WebArena），并逐步纳入多模态交互（WebVoyager）和安全合规评估（ST-WebAgentBench）。
- **软件工程智能体**：以 SWE-bench 为核心框架，利用真实 GitHub issue 数据，配以 Docker 容器化验证环境。后续的 SWE-bench Verified（人工筛选 500 样本）、SWE-Lancer（百万美元级真实自由职业任务）和 SWE-bench Pro（长程多文件任务）持续推进评估难度。
- **科学智能体**：覆盖研究全流程——从科学选题（Ideation）、实验设计（AAAR-1.0）、代码生成（SciCode、ScienceAgentBench、CORE-Bench、PaperBench）到同行评审，最终走向全研究周期评估。
- **对话智能体**：从传统任务导向对话（MultiWOZ）到需要工具交互的 τ-Bench 及其改进版 τ²-Bench，引入合成场景生成（IntellAgent、ALMITA）实现动态可扩展评估。

### （3）通用智能体评估（§4）
两种互补路径：
- **内生综合型**：构建天然需要多种能力协同的基准，如 GAIA 及其更新版 GAIA2、OSWorld、AppWorld；
- **统一集成型**：将多个任务特定基准纳入统一评估框架，如 AgentBench、HAL；以及致力于统一协议的新框架（Harbor、Exgentic、CUBE）。

### （4）基准核心维度分析（§5）
提出五个正交的基准设计维度作为横切分析框架：
- **数据策展策略**（人工 vs 混合 vs 合成）
- **环境动态性**（静态 vs 动态）
- **交互界面**（代码/终端、工具调用、图形用户界面）
- **评估指标**（单元测试、状态匹配、答案匹配）
- **安全与鲁棒性度量**（pass^k、策略合规）

### （5）评估框架与工具（§6）
将现有开发框架按评估粒度分为四个层次：最终响应评估、逐步评估、轨迹级评估、支持能力（A/B 测试、合成数据生成、人机协同标注）。

## 3. 实验设计：覆盖的数据集、基准与对比分析

作为一篇综述论文，其"实验设计"体现为系统化的文献分析和基准对比：

### 覆盖的主要 Benchmark 与数据集

| 评估类别 | 主要 Benchmark/数据集 |
|---------|----------------------|
| 规划与推理 | PlanBench、FlowBench、Natural Plan、HotpotQA、GSM8K、MATH、MINT |
| 工具使用 | BFCL（v1/v2/v3）、ToolBench、ComplexFuncBench、NESTFUL、ToolSandbox、MCP Atlas |
| Web 智能体 | WebShop、Mind2Web、WebArena、WebVoyager、AssistantBench、VisualWebArena |
| 软件工程 | SWE-bench、SWE-bench Verified、SWE-Lancer、SWE-bench Pro、Terminal-Bench |
| 科学智能体 | SciCode、ScienceAgentBench、CORE-Bench、PaperBench、AAAR-1.0 |
| 对话智能体 | τ-Bench、τ²-Bench、IntellAgent、ALMITA |
| 通用智能体 | GAIA、GAIA2、OSWorld、AppWorld、AgentBench、HAL、TheAgentCompany |

### 关键对比要素
- **Table 1** 从数据策展、环境动态性、交互界面、评估指标、安全性五个维度对比了 8 个代表性基准（SWE-bench Verified、SWE-Lancer、Mind2Web、WebArena、PaperBench、TAU-Bench、AppWorld、GAIA）。
- **Table 2** 对比了 8 个评估框架（LangSmith、Langfuse、Vertex AI、Arize、Galileo、Patronus AI、AgentEvals、Mosaic AI）在逐步评估、监控、轨迹评估、人机协同、合成数据生成、A/B 比较等维度的能力支持。

论文未运行新实验，而是通过横向对比揭示不同基准在结构上的共性和差异。

## 4. 资源与算力

**论文未提及任何具体的算力投入**（如 GPU 型号、数量、训练/推理时长、能源消耗等）。这符合综述论文的性质——其主要工作在于文献检索、归类分析、专家咨询和作者团队的研究积累，而非训练或评估模型本身。

这一点也在其局限性中有所隐含：综述的内容深度和覆盖面受限于所分析的文献，而非通过自身实验验证。

## 5. 实验数量与充分性

### 覆盖范围
- 引用了超过 200 篇文献，覆盖 5 大分析视角、4 类应用场景、4 种核心能力、8 个代表性基准的维度对比、8 个评估框架的功能对比；
- 综述方法采用**三阶段系统化流程**：系统搜索（Google Scholar、ACL Anthology、HuggingFace Papers、arXiv）→ 结构化筛选（包含/排除标准）→ 专家验证（与基准创建者和架构开发者直接咨询）。

### 充分性与客观性分析
- **充分性**：覆盖面广、代表性较强，从早期基础能力评估到前沿的实时基准均有涉猎，并嵌入"未来方向"的前瞻性分析；
- **客观性**：作为综述不偏向某一特定方法，对各个基准的优缺点做了均衡讨论。但也存在一定的选择性偏差（如排除了纯传统 LLM 评估工作）；
- **可验证性**：作者承诺通过持续更新的 GitHub 仓库跟踪该领域的后续工作，意图缓解综述固有的时效性问题。

## 6. 论文的主要结论与发现

### 两大当前趋势
1. **向真实、有挑战性的评估演进**：评估从简化静态环境转向真实、动态、长程的专业级任务（如 WebArena 取代早期模拟、SWE-bench 使用真实 GitHub issue），反映业界对智能体"真实实用价值"的关切。
2. **"活"基准（Live Benchmarks）的兴起**：静态基准迅速过时和饱和，促使 BFCL 系列、SWE-bench 系列（Verified/Pro）等持续迭代更新，以适应模型能力增长和生态演进（如 MCP 工具调用标准）。

### 五大未来研究方向
1. **推进细粒度评估**：现有二进制端到端指标不足以诊断中间失败原因，需开发标准化、轨迹级的细粒度评测方法；
2. **成本与效率度量**：当前评估过度聚焦性能而忽视 token 消耗、API 费用、推理时间等成本要素，可能误导开发出"强但贵"的智能体；
3. **扩展与自动化评估**：人工标注型的静态基准难以扩展且迅速过时，亟需合成数据生成和"智能体作为裁判"（Agent-as-a-Judge）的自动化手段；
4. **安全与合规**：现有基准缺乏安全意识，需引入对抗性鲁棒性、偏差缓解和组织/社会政策合规等守卫指标；
5. **LLM 与 Harness 解耦评测**：当前基准混淆了"骨干 LLM 的固有能力和"智能体框架（Harness）的设计贡献"，需建立独立控制变量的评估协议以实现系统性的归因分析。

## 7. 优点

- **首创性与全面性**：首次系统性地将 LLM 智能体评估划分为五个互补视角，覆盖从核心能力到应用场景、从基准维度到开发工具的全栈评估问题；
- **结构化分析框架**：提出的五个基准核心维度（数据策展、环境动态性、交互界面、评估指标、安全性）为后续基准设计提供了清晰的参考坐标系，具有方法论价值；
- **实践导向**：附录 E 提供了针对不同应用场景（Web、SWE、科学、对话、通用）的具体基准选择建议，对开发者极具实操参考价值；
- **系统化文献综述方法**：采用三阶段流程（系统搜索→结构化筛选→专家验证），提升了综述的可信度和覆盖面；
- **前瞻性识别关键缺口**：明确指出成本效益、安全性、细粒度评估、解耦评测等被忽视的重大空白，为社区指明研究方向；
- **时效性维护机制**：通过持续更新的 GitHub 仓库追踪进展，缓解了综述难以跟上快速演进领域的固有弱点。

## 8. 不足与局限

- **时效性受限**：该领域发展极快，综述本质上只是"某个时间点的快照"，部分最新工作（如更前沿的 MCP 生态基准、动态更新的移动端场景）可能未被纳入；
- **选择存在代表性偏差**：虽然覆盖面广，但为保持聚焦，一些特定或小众的评估方法未获深入讨论；筛选标准排除了不具"评价方法论贡献"的智能体架构论文，可能遗漏与该领域相关的边缘见解；
- **分析深度受限**：由于覆盖范围广，对每个单一基准或框架的分析深度有限；作者建议读者进一步查阅原始文献以获得更深入的理解；
- **未来方向的推理性**：对关键缺口的判断涉及一定程度的前瞻与解读，实际研究轨迹和这些领域的重要性会随时间演变；
- **缺乏实证验证**：综述本身未运行实验来检验其对各基准间关系（如性能相关性、难度层级）的推断，更多依赖对文献的定性归纳；
- **微观层面借鉴价值有限**：对特定任务（如移动端智能体）的评估设计虽提供了方法论框架，但缺乏针对性的场景适配指南和细粒度指标定义，实际落地仍需研究者自行转化。

（完）
