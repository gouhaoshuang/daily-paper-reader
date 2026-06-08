---
title: "MetaAgent: Automatically Constructing Multi-Agent Systems Based on Finite State Machines"
title_zh: MetaAgent：基于有限状态机的多智能体系统自动构建
authors: "Yaolun Zhang, Xiaogeng Liu, Chaowei Xiao"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=vOxaD3hhPt"
tags: ["query:eca"]
score: 8.0
evidence: 通过有限状态机自动构建多智能体系统
tldr: 现有自动化多智能体系统设计方法存在工具集成缺失、依赖外部数据等问题。本文提出MetaAgent，基于有限状态机从任务描述自动生成多智能体系统，并通过优化算法进行改进。部署后系统能够灵活适应不同任务，展示了自动化设计的潜力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
motivation: 多智能体系统设计依赖人工，已有自动化方法存在多种限制。
method: 利用有限状态机表示智能体通信与行为，从任务描述自动生成并优化系统结构。
result: 在多种任务上，MetaAgent生成的系统性能接近甚至超越人工设计。
conclusion: 有限状态机为自动化多智能体系统构建提供了一种高效且灵活的方案。
---

## Abstract
Large Language Models (LLMs) have demonstrated the ability to solve a wide range of practical tasks within multi-agent systems. However, existing human-designed multi-agent frameworks are typically limited to a small set of pre-defined scenarios, while current automated design methods suffer from several limitations, such as the lack of tool integration, dependence on external training data, and rigid communication structures. In this paper, we propose \textbf{MetaAgent}, a  \textbf{finite state machine} based framework that can automatically generate a multi-agent system. Given a task description, MetaAgent will design a multi-agent system and polish it through an optimization algorithm. When the multi-agent system is deployed, the finite state machine will control the agent's actions and the state transitions. To evaluate our framework, we conduct experiments on both text-based tasks and practical tasks. The results indicate that the generated multi-agent system surpasses other auto-designed methods and can achieve a comparable performance with the human-designed multi-agent system, which is optimized for those specific tasks.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义（研究动机和背景）

- 大型语言模型（LLM）在多智能体系统中展现出解决多种实际任务的能力，但现有工作存在两大瓶颈：
  1. **人工设计框架**：如 MetaGPT、ChatDev 等，针对特定场景设计，泛化性差且需要大量人工迭代。
  2. **现有自动设计方法**：如 SPP、AutoAgents、EvoAgent 等，存在工具集成缺失、依赖外部训练数据、通信结构僵化（线性、无回溯）等问题。
- 本文提出 **MetaAgent**，旨在自动构建**基于有限状态机（FSM）** 的多智能体系统，克服上述局限，实现无需外部数据的、支持工具使用和可回溯的自动设计框架。

### 论文提出的方法论

#### 核心思想
- 将多智能体系统的通信与控制过程建模为**有限状态机（FSM）**。每个状态对应一个子任务，包含：
  - 任务执行智能体（Task-solving Agent）
  - 状态指令（State Instruction）
  - 条件验证器（Condition Verifier）
  - 监听智能体列表（Listeners）
- 系统通过状态转移（含 null-transition 和状态回溯）灵活应对不同情况。

#### 关键技术细节
1. **智能体设计**：由设计 LLM 根据任务描述生成智能体（名称、系统提示、工具列表），确保成本可控。
2. **状态与转移条件设计**：设计 LLM 预测任务中可能遇到的各种情形，定义状态和自然语言转移条件，每个状态附带条件验证器。
3. **FSM 优化**：通过 LLM 判断可合并状态，迭代合并冗余状态，简化系统结构，提升鲁棒性。
4. **部署阶段**（Algorithm 2）：初始状态 → 执行指令 → 条件验证 → 满足条件则转移（并写入监听者记忆），否则 null-transition（重试），直到达到最终状态或超限。
5. **回溯能力**：支持从当前状态跳回之前状态，修复前序错误。
6. **泛化性**：线性、分散辩论、协调器结构均可视为 FSM 的特例（无回溯、无 null-transition 等）。

#### 算法/公式核心（文字描述）
- **FSM 定义**：M = (Σ, S, s₀, F, δ)。Σ 为任务领域中的具体案例，S 为状态集，s₀ 为初始状态，F 为终止状态，δ 为转移函数。
- **优化算法**（Algorithm 1）：对状态集 S 中每对状态，调用 LLM 判断可否合并（依据角色区分度、信息传递必要性、工具分配可统一性），若可则合并并重新迭代，直至无合并。

### 实验设计

#### 数据集与场景
1. **文本任务**（Text-Based Tasks）：
   - Trivial Creative Writing：100 个任务，要求写故事涵盖问题答案。评价指标为**成功率**。
   - GPQA (Diamond)：198 个研究生级科学选择题。评价指标为**正确率**。
2. **实际编码任务**（Real-World Coding Tasks）：
   - Machine Learning Bench（ML Bench）：5 个数据集（Titanic、House Prices 等），要求训练 ML 模型并报告指标。评价指标为归一化性能分数 (NPS)。
   - 软件发展（Software Development）：5 个任务（2048、贪吃蛇、打砖块、Excel 应用、天气预报）。评价指标为**基于客观检查点的通过率**（每个任务 4 个检查点）。

#### 对比方法
- **文本任务**：Direct、CoT、CoT-SC、llm-debate、Self-Refine、SPP。
- **ML Bench**：AutoGen、Open Interpreter、TaskWeaver、MetaGPT、Data Interpreter、SPP、AutoAgents。
- **软件发展**：MetaGPT、AutoAgents、SPP。

#### 实验充分性
- **主要实验**：在各任务上对比，结果表格（Table 2、3、4、5、6、7）显示 MetaAgent 超越所有自动设计方法，性能接近或超越人类设计系统（如 Data Interpreter）。
- **消融实验**：对工具使用、优化、回溯进行了消融（Table 6），证明各组件重要性。
- **模型质量实验**：使用 GPT-4o 和 GPT-3.5-Turbo 作为设计者/执行者，分析性能变化（Table 5）。
- **成本分析**：对比 MetaGPT、AutoAgents 和 MetaAgent 的总 token 成本（Table 7）。
- **客观性/公平性**：所有实验使用 GPT-4o 作为基座，温度 0，保证可复现；软件任务采用客观检查点，避免主观偏差。

### 资源与算力

- 论文**未明确说明**使用的 GPU 型号、数量或训练时长。文中提到使用 GPT-4o 作为基础模型，并设置温度为 0，因此推理费用由 API 调用产生，未提供具体硬件细节。成本分析仅提供了 token 数量（如 5 个 ML 任务总 token 46,289，6 个软件任务总 token 47,752），未给出货币成本或算力资源。

### 实验数量与充分性

- 实验覆盖**4 类任务**（文本、ML、软件、消融），含 **3 个主要 benchmark**，**5 个 ML 数据集**，**5 个软件任务**，**10 个以上对比方法**。消融实验包含 3 个组件（工具、优化、回溯），以及模型质量（2 种组合）和成本分析。整体设计**充分且客观**，对比方法涵盖主流的自动和人工设计系统，评价指标明确（如 NPS、成功率、检查点通过率）。公平性方面，软件任务采用客观检查点避免主观评判；所有方法使用相同基础模型。

### 论文的主要结论与发现

1. **性能优势**：MetaAgent 在文本任务上超过 SPP 等自动方法 9%（写作 0.86 vs 0.79，GPQA 0.60 vs 0.45）；在 ML Bench 上达到人类最优系统 Data Interpreter 的 97% 性能（0.83 vs 0.86），且超越所有自动方法；在软件任务上平均通过率 0.85，远超 MetaGPT（0.35）。
2. **组件有效性**：工具使用（搜索+代码解释器）显著提升文本任务准确率；回溯能力使软件任务能修复 bug（通过率提升 58.8%）；优化合并状态减少了冗余（性能下降 26.5% ~ 35.3%）。
3. **执行器质量更关键**：执行器使用 GPT-4o 比设计器使用 GPT-4o 对性能影响更大（0.39 vs 0.26）。
4. **成本低**：MetaAgent 的部署成本低于 MetaGPT，且设计成本仅为 AutoAgents 的约 1/4，适合大规模应用。

### 优点

- **自动化程度高**：无需外部训练数据，仅凭任务描述即可生成完整多智能体系统。
- **结构灵活**：FSM 支持 null-transition 和回溯，能应对复杂任务中多种情景，优于固定线性/辩论结构。
- **工具集成好**：自动为智能体分配搜索、代码解释器，增强能力。
- **可自优化**：通过 LLM 合并冗余状态，减少推理开销且不损失功能。
- **实验结果扎实**：在多个实际场景中验证，消融实验设计合理，对比基线全面，评价指标客观（软件任务使用检查点）。

### 不足与局限

- **基础模型依赖**：性能受限于基座 LLM（GPT-4o），实验中 GPT-3.5-Turbo 作为执行器性能大幅下降，未测试开源模型（如 LLaMA）的泛化能力。
- **实验覆盖有限**：
  - 仅包含 5 个 ML 数据集和 5 个软件任务，样本量较小，统计显著性未报告。
  - 未在更多领域（如对话、机器人控制）验证。
- **未提供算力成本**：仅给出 token 数量，无实际 GPU 时长或 API 费用，难以直接复现。
- **状态合并依赖 LLM 判断**：优化算法可能合并了不应合并的状态，文中未提供失败案例分析。
- **可解释性**：FSM 结构虽直观，但条件验证器使用二阶段 LLM 调用，增加了延迟和不确定性。
- **假设通用性**：论文声称 FSM 是通用结构，但仅验证了三种已知结构的退化关系，未与更多新型结构（如分层 FSM）对比。

（完）
