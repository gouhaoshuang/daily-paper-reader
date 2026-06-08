---
title: On the Resilience of LLM-Based Multi-Agent Collaboration with Faulty Agents
title_zh: 基于LLM的多智能体协作在面对故障代理时的弹性研究
authors: "Jen-tse Huang, Jiaxu Zhou, Tailin Jin, Xuhui Zhou, Zixi Chen, Wenxuan Wang, Youliang Yuan, Michael Lyu, Maarten Sap"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=bkiM54QftZ"
tags: ["query:eca"]
score: 7.0
evidence: 基于LLM的多智能体协作与故障代理
tldr: 现有LLM多智能体协作系统在面对故障或恶意代理时缺乏鲁棒性研究。本文提出AutoTransform和AutoInject两种方法模拟代理错误，并系统评估不同拓扑结构（如链式、全连接）在多种下游任务下的表现。实验揭示了结构对弹性的关键影响，并提出了提升防御能力的策略，为构建可靠的多智能体协作系统提供了新视角。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-bkim54qftz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 806, \"height\": 777, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bkim54qftz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1511, \"height\": 1289, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bkim54qftz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1721, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bkim54qftz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 871, \"height\": 867, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bkim54qftz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1716, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bkim54qftz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 862, \"height\": 951, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 863, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 861, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 859, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1099, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1307, \"height\": 514, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1507, \"height\": 536, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1355, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1690, \"height\": 412, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1277, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1175, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1750, \"height\": 1697, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1748, \"height\": 1656, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1758, \"height\": 723, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1752, \"height\": 1073, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1754, \"height\": 1727, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1742, \"height\": 886, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1745, \"height\": 1024, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1731, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bkim54qftz/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1742, \"height\": 558, \"label\": \"Table\"}]"
motivation: 现有研究忽略了故障或恶意代理对多智能体协作系统整体性能的影响。
method: 提出AutoTransform和AutoInject两种方法模拟代理错误，并在不同系统结构下进行实验。
result: 发现不同系统结构对故障代理的弹性差异显著，并提出了增强弹性的方法。
conclusion: 多智能体协作系统需要设计容错机制以应对故障代理，本文的模拟和评估框架为后续研究提供了基础。
---

## Abstract
Large language model-based multi-agent systems have shown great abilities across various tasks due to the collaboration of expert agents, each focusing on a specific domain. However, the impact of clumsy or even malicious agents—those who frequently make errors in their tasks—on the overall performance of the system remains underexplored. This paper investigates: (1) What is the resilience of various system structures (e.g., A$\rightarrow$B$\rightarrow$C, A$\leftrightarrow$B$\leftrightarrow$C) under faulty agents, on different downstream tasks? (2) How can we increase system resilience to defend against these agents? To simulate faulty agents, we propose two approaches—AutoTransform and AutoInject—which introduce mistakes into the agents' responses. Experiments on four downstream tasks using six systems show that the "hierarchical" structure, i.e., A$\rightarrow$(B$\leftrightarrow$C), exhibits superior resilience with the lowest performance drop of 5.5%, compared to 10.5% and 23.7% of other two structures. To further improve resilience, we introduce (1) Challenger, that introduces a mechanism for each agent to challenge others' outputs, and (2) Inspector, an additional agent to review and correct messages, recovering up to 96.4% errors made by faulty agents. Our code and data are available at https://github.com/CUHK-ARISE/MAS-Resilience.

---

## 论文详细总结（自动生成）

# 基于LLM的多智能体协作在面对故障代理时的弹性研究——论文总结

## 1. 核心问题与整体含义（研究动机与背景）
- **研究动机**：LLM多智能体系统在代码生成、数学推理、翻译、文本评估等任务中展现了卓越性能，但现有研究主要关注智能体之间的正常协作，忽略了系统中出现**笨拙或恶意代理**（即频繁出错、产生误导性输出的代理）对整体协作效果的潜在破坏。这类代理可能来自不同来源，缺乏统一管控，极易破坏协作流程。
- **核心问题**：(1) 不同系统结构（链式、扁平式、层级式）在存在故障代理时，其**弹性（resilience）** 如何？(2) 如何增强系统弹性，以抵御故障代理的破坏？
- **整体意义**：首次系统性地评估多智能体系统的拓扑结构对故障鲁棒性的影响，并为设计更具容错能力的协作系统提供指导和防御策略。

## 2. 方法论
### 核心思想
作者提出两种自动引入错误的方法来模拟故障代理：
- **AutoTransform**：通过修改代理的角色描述（profile），使其在保留原有功能的同时，**自主生成隐蔽的错误输出**。类似于手动将代理“黑化”，但自动化完成。流程包括：分析原始代理任务 → 列出可能的错误注入方式 → 重写提示词，强调“生成不易被其他代理发现的微妙错误”。
- **AutoInject**：直接**拦截代理之间的消息**，在消息中注入特定类型和数量的错误。支持精确控制错误率（消息层面`Pm`、行/句层面`Pe`）和错误类型（语法/语义）。由LLM自动生成错误内容并替换原始文本。

此外，为提升弹性，提出两种防御策略：
- **Challenger**：在每个代理的profile中添加“质疑其他代理输出”的能力，使其能主动识别和指出错误。
- **Inspector**：引入一个额外的“审查代理”，拦截所有通信消息，检查并修正错误，类似“警察”角色。

**关键细节**：所有方法均基于提示工程，不修改模型参数；错误注入与防御均使用LLM（GPT-3.5/4o）自动完成，无需人工干预。

## 3. 实验设计
### 数据集/Benchmark
- **代码生成**：HumanEval（164个手写编程问题，评估Pass@1）
- **数学问题求解**：CIAR（50道反直觉算术推理题，要求多步推理，准确率）
- **翻译**：CommonMT（100条最难的“Lexical”类型句子，评估BLEURT-20分数）
- **文本评估**：FairEval（80个“Win/Tie/Lose”标注，比较ChatGPT与Vicuna-13B回答，准确率）

### 对比方法（多智能体系统）
按结构分类：
- **链式（Linear）**：MetaGPT（5个代理）、Self-collab（3个代理，用于代码生成）
- **扁平式（Flat）**：Camel（2个代理）、SPP（2~5个角色，用于代码）
- **层级式（Hierarchical）**：MAD（辩论框架，2个辩手+1个裁判）、AgentVerse（动态招募4个代理）

**单智能体基线**：使用相同任务提示的单GPT-3.5/4o模型。

**实验设置**：每个系统每次只引入一个故障代理，且其他正常代理对故障代理不知情（信息不对称）。使用GPT-3.5和GPT-4o作为主干模型，温度设为0。所有系统均采用直接消息传递，无广播/摘要等处理。

## 4. 资源与算力
论文**未明确说明**具体使用的GPU型号、数量或训练时长。所有实验基于GPT-3.5和GPT-4o的API调用，未涉及模型微调或大规模训练，因此算力主要消耗在推理请求上。作者仅提及代码和数据已开源。

## 5. 实验数量与充分性
- **主实验**：6个多智能体系统 × 4个任务 × 2种错误注入方法 × 2种主干模型（GPT-3.5、GPT-4o） = 96种设置组合，加上单智能体基线、无错误基线等。
- **错误率分析**（RQ3）：仅用代码生成任务、GPT-3.5、AutoInject，控制`Pm`（0.2/0.4/0.6/1.0）和`Pe`（0.2/0.4/0.6），共9种组合 × 6个系统 = 54组实验。
- **错误类型分析**（RQ4）：语义 vs. 语法错误，同样6系统 × 1任务 = 12组。
- **防御实验**：在Self-collab和Camel两个系统上测试Challenger、Inspector及二者组合，共2系统 × 4设置（无改善、仅Challenger、仅Inspector、两者） × 3条件（无错误、AutoTransform、AutoInject）= 24组。
- **额外分析**：多个故障代理（2个）、更高级系统（星型/全连通图）、更复杂任务（Snake游戏）、非GPT骨干模型（LLaMA-3.1-70B、o1-Mini）等扩展实验。

**充分性评价**：实验覆盖了三种主流结构、四种代表性任务、两种错误注入方法、两种主流LLM，并进行了错误率、错误类型、防御策略、多故障、泛化性等消融与分析。实验设计较为系统全面，对比公平（均使用相同主干模型、相同温度、相同评估指标）。

## 6. 主要结论与发现
1. **层级结构弹性最强**：层级式系统平均性能下降仅5.5%，而扁平式下降10.5%，链式下降23.7%。原因在于层级式存在高层代理（如裁判）整合多个子代理的输出，易于发现和纠正单个代理的错误。
2. **任务敏感性差异**：代码生成（-22.6%）和数学（-9.9%）受故障影响最大（客观性任务），翻译（-4.7%）和文本评估（-5.4%）相对稳健（主观任务）。多智能体系统总体优于单智能体，但故障时可降至单智能体水平以下。
3. **注入错误有时可提升性能**：在MAD、Camel等系统中，故意注入明显错误会触发其他代理的“双重检查”或“发散思维”，反而修复了原有错误或打破僵局，最高提升12.1%（MAD在文本评估）。
4. **错误率影响**：增加**消息出错比例**（`Pm`）比增加**单消息内错误数量**（`Pe`）更显著地降低性能。但当`Pe`过高（如0.6）时错误变得显眼，反而促使系统修正。
5. **错误类型影响**：**语义错误**比**语法错误**更具破坏性。LLM对语法错误（如格式、拼写）识别能力强，但对语义错误（逻辑正确但意图错误）难以察觉。
6. **LLM偏重自然语言而非代码**：在代码生成中，干扰性注释（如“已修正bug”）可以误导其他代理放过错误代码，揭示LLM的注意力偏差。
7. **高层级规划者更重要**：对Camel的User代理、MetaGPT的Product Manager注入错误比直接对执行者注入错误导致更严重性能下降，说明指挥者角色更关键。
8. **通信轮数与性能无关**：在Camel中，错误注入后正确通过的例子用时更短，失败例子用时更长但依然失败，说明增加轮次不能自动增强弹性。
9. **防御策略有效**：Challenger与Inspector组合可恢复Self-collab中96.4%的由故障代理导致的性能损失，显著提升了链式和平扁式系统的弹性。

## 7. 优点
- **方法创新**：提出了两种自动化模拟故障代理的方法（AutoTransform/AutoInject），具有通用性，可应用于任何代理profile和任务，并支持精确控制错误率与类型。
- **结构维度研究**：首次从管理学视角（链式、扁平、层级）系统对比不同拓扑结构在面对故障时的弹性，结论具有理论支撑和实践指导意义。
- **防御策略实用**：Challenger和Inspector简单有效，不依赖额外训练或外部知识，可通过修改提示词直接嵌入现有系统。
- **实验充分且分析深入**：覆盖多种任务、系统、错误条件，并进行了详细的案例研究和因素分析（如错误率、错误类型、多故障、泛化性），结论稳健。

## 8. 不足与局限
- **模型与任务局限**：实验主要使用GPT-3.5/4o（温度0），未涉及其他更弱或更强模型（仅在附录补充了LLaMA-70B和o1-Mini的部分实验）。任务集中于文本（代码、数学、翻译、评估），未覆盖多模态、长对话、复杂规划等场景。
- **评估指标依赖自动化**：使用自动指标（Pass@1、准确率、BLEURT），缺乏人类评估验证误差对实际可用性的影响。
- **系统实现差异**：不同系统使用不同作者提供的提示词实现（如MetaGPT自带SOP），可能隐含prompt engineering偏差，虽然论文通过选择每个结构两个系统来缓解，但无法完全消除。
- **信息不对称假设简化**：假设正常代理不知晓故障代理存在，且仅引入一个故障代理，现实中可能存在多个协作故障或恶意代理蓄意传播错误。
- **未探索自适应攻击**：AutoTransform和AutoInject均为静态错误注入，未考虑故障代理根据上下文动态调整策略的情况。
- **防御策略的局限性**：Challenger和Inspector依赖额外LLM调用，可能增加延迟和成本，且其效果可能随骨干模型能力变化。

（完）
