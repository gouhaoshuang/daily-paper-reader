---
title: Cost-efficient Collaboration between On-device and Cloud Language Models
title_zh: 设备端与云端语言模型之间的低成本协作
authors: "Avanika Narayan, Dan Biderman, Sabri Eyuboglu, Avner May, Scott Linderman, James Zou, Christopher Re"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=qGDlzt3dKz"
tags: ["query:eca"]
score: 9.0
evidence: 设备端与云端语言模型协作以降低成本
tldr: "端侧模型与云端大模型协作可以降低推理成本，但如何平衡性能是关键。本文探索了本地-远程协作协议MINION，本地模型处理完整上下文，云端模型提供指导，实现了30.4倍成本降低和87%的性能保留。进一步分析了本地模型在多步指令跟随方面的局限性，为高效端云协同提供了重要经验。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1739, \"height\": 598, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 838, \"height\": 837, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 836, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1759, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1560, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1052, \"height\": 859, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1230, \"height\": 746, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1752, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1073, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1724, \"height\": 1381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-qgdlzt3dkz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1588, \"height\": 978, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 858, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1553, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1314, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 643, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 592, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1526, \"height\": 696, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1613, \"height\": 654, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1811, \"height\": 562, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 469, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1578, \"height\": 1523, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1578, \"height\": 1563, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1524, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-qgdlzt3dkz/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1544, \"height\": 387, \"label\": \"Table\"}]"
motivation: 云端大模型推理成本高，而设备端模型性能有限，需探索高效协作方式。
method: 提出MINION协作协议，本地模型处理全上下文，云端模型进行指导。
result: "该协议将云端推理成本降低30.4倍，同时保留了87%的云端模型性能。"
conclusion: 端云协作在降低成本的同时能保持较高性能，具有实际应用价值。
---

## Abstract
We investigate an emerging setup in which a small, on-device language model (LM) with access to local data collaborates with a frontier, cloud-hosted LM to solve real-world tasks involving financial, medical, and scientific reasoning over long documents. 
*Can a local-remote collaboration reduce cloud inference costs while preserving quality?*
First, we consider a naïve collaboration protocol, coined MINION, where the local and remote models simply chat back and forth. Because only the local model ingests the full context, this protocol reduces cloud costs by 30.4x, but recovers only 87% of the performance of the frontier model.
We identify two key limitations of this protocol: the local model struggles to (1) follow the remote model's multi-step instructions and (2) reason over long contexts. Motivated by these observations, we propose MINIONS, a protocol in which the remote model decomposes the task into easier subtasks over shorter chunks of the document, that are executed locally in parallel. MINIONS reduces costs by 5.7× on average while recovering 97.9% of the remote-only performance. Our analysis reveals several key design choices that influence the trade-off between cost and performance in local-remote systems.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **问题**：云端大语言模型（如GPT-4）进行数据密集型推理（如长文档分析）成本高昂（例如处理100万token的代码库需>15美元）。与此同时，小参数模型（1B-8B）已能在个人电脑和手机端运行，但主要用于简单任务（如文本补全）。如何让本地小模型与云端大模型协同工作，在降低云端推理成本的同时保持高性能？
- **背景**：现有工作包括检索增强生成（RAG）、多智能体系统、模型路由等，但很少考虑不对称的本地-云端成本结构以及本地模型的并行化能力。本文旨在探索一种成本高效的本地-云端协作协议。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：通过合理的任务分解，让本地模型处理大部分原始上下文，云端模型仅处理压缩后的信息，从而节省成本。
- **两类协议**：
  - **MINION（朴素的对话协议）**：本地模型持有完整上下文，云端模型通过多轮自然语言对话向本地模型提问，直至能够回答最终查询。本地模型充当“检索与总结”接口。
  - **MINIONS（基于分解的协议）**：针对MINION暴露的本地模型局限（难以同时执行多指令、难以处理长上下文）进行改进。云端模型将任务分解为**原子指令**（每个指令针对一个短文本块），并生成Python代码，在本地执行。代码产生多个“作业”（job），由本地模型并行执行，返回筛选后的结果给云端模型聚合。迭代进行，直至输出答案。
- **关键技术细节**：
  - 云端模型生成代码 `f(c, T_{t-1})`，该代码在本地执行，产生作业列表（指令+文本块）。
  - 本地模型对每个作业输出结构化结果（解释、引用、答案），并依据“无法完成”自动过滤，减少发送给云端的信息。
  - 云端模型聚合结果，决定是输出答案还是进入下一轮迭代。
  - 三个超参数控制成本-性能权衡：**模型选择**（本地/云端模型大小和类型）、**并行作业规模**（每个任务的数量、每个任务的采样次数、块大小）、**顺序通信策略**（最大轮数、上下文维护方式如简单重试或草稿本）。

## 3. 实验设计：使用的数据集、场景、基准与对比方法
- **数据集**（三个数据密集型推理基准）：
  - **FinanceBench**：金融文档理解（64个样本，平均上下文142.9K token）
  - **LongHealth**：纵向医疗记录问答（400个样本，扩展后上下文120.1K token）
  - **QASPER**：科学论文问答（500个样本，上下文54.3K token）
- **基准方法**：
  - **Remote-only**：仅云端模型（GPT-4o）处理完整上下文和查询。
  - **Local-only**：仅本地模型处理完整上下文。
  - **MINION**（朴素协议）作为对比。
  - **RAG**（BM25和OpenAI嵌入）用于部分比较（附录E.3）。
- **对比方法**：主要对比不同本地模型（LLaMA-3.2 1B/3B/8B、Qwen2.5 3B/7B等）与固定云端模型GPT-4o的组合，以及不同云端模型（GPT-4系列、LLaMA-70B等）与固定本地模型的组合。

## 4. 资源与算力
- **本文未明确说明训练过程使用的具体算力**。实验中的本地模型运行在单张A100 GPU或消费级显卡（RTX 4090、RTX 6000 Ada）上。云端模型通过API调用（如GPT-4o）。文中给出了延迟测量，但未提及训练时长或总GPU小时数。
- **关键点**：论文强调本地模型推理成本假设为“免费”（忽略硬件和能耗边际成本），仅计算云端API费用；对于能耗分析，使用nvidia-smi和powermetrics测量本地能耗，云端能耗则采用Epoch AI的估算方法。

## 5. 实验数量与充分性
- **实验组数非常充分**：主要结果见表1（3个数据集 × 3种本地模型 × 3种协议 = 27个主要配置），以及大量消融实验：
  - 本地模型大小和家族对比（1B、3B、8B；LLaMA vs Qwen）
  - 云端模型变化（GPT-4o、GPT-4-turbo、GPT-3.5、LLaMA-70B等）
  - 并行作业规模消融：任务数（1-16）、采样数（1-32）、块大小（5页到100页）
  - 顺序通信轮数（1-5轮）和上下文维护策略（简单重试 vs 草稿本）
  - 按问题复杂度分层分析（FinanceBench按信息提取 vs 数值推理；LongHealth按证据跨度数）
  - 额外实验：RAG比较、能耗分析、智能体工具使用、多模态扩展（MathVision）、监督微调（初步）
- **充分性评估**：实验设计客观、公平，涵盖了多种实际场景和超参数空间，消融实验系统地隔离了各因素的影响。但部分数据集（如FinanceBench仅64个样本）规模较小，可能影响统计显著性。此外，大多数实验仅使用单一云端模型GPT-4o，对泛化性有潜在偏差。

## 6. 论文的主要结论与发现
1. **MINION**可实现30.4×成本降低，但仅恢复87%的云端性能。
2. **MINIONS**在成本降低5.7×的同时恢复97.9%的云端性能（Llama-8B本地 + GPT-4o云端），并可在1B本地模型下恢复49.5%，3B下恢复93.4%。
3. **本地模型的关键局限**：多指令跟随能力差（将多子任务拆分为单任务可提升56%准确率）；长上下文处理能力弱（上下文从1K增至65K时准确率下降13%）。
4. 增加并行任务数（最多16个）和减小块大小可显著提升性能，但增加云端成本；增加采样数收益递减。
5. 多轮通信可提升性能（每轮约增加4.2个准确率点，成本增加$0.006），草稿本策略优于简单重试。
6. MINIONS在更复杂的任务上（如需要多证据合成）相对云端基线的性能提升更显著。
7. 模型性能随时间演进：直到2024年7月（GPT-4-turbo + LLaMA-3.1-8B）才达到接近当时前沿模型的性能（相差12%以内）。

## 7. 优点：方法或实验设计上的亮点
- **创新的协作协议**：将任务分解与代码生成结合，使云端模型能在不直接访问上下文的情况下指导本地处理，并支持并行执行，是一种新颖的“分而治之”策略。
- **系统性超参数分析**：全面探讨了模型规模、并行程度、通信轮数等对成本-准确的权衡，提供了可操作的设计指南。
- **丰富的评估维度**：除标准准确率和成本外，还分析了延迟、能耗、隐私潜力、智能体工具扩展、多模态任务等，体现了研究的广度。
- **实际部署导向**：使用消费级GPU（RTX 4090）测量延迟，并构建理论框架预测不同硬件配置的性能，贴近实际应用场景。
- **开源性**：所有模型和数据集均为公开可用，实验可复现。

## 8. 不足与局限
- **实验局限**：多数实验仅使用GPT-4o作为云端模型，缺乏对其他前沿模型（如Claude、Gemini）的系统评估，可能限制泛化性。部分数据集（FinanceBench）样本量小（64个），统计可靠性需进一步验证。
- **成本模型简化**：假设本地推理成本为0，忽略了硬件折旧、能耗及边际运行成本。能耗分析中的云端估计依赖外部API数据，精度有限。
- **未深入探讨隐私与安全**：虽提及MINIONS可保持数据本地化，但未给出严格的形式化隐私保证，也未见分析对抗性攻击（如提示注入或逆向工程）。
- **协议复杂度**：MINIONS依赖云端模型生成正确且安全的Python代码，代码质量直接影响结果，存在失败风险（如逻辑错误、无限循环）。当前实验未报告代码生成失败率。
- **应用限制**：方法假设任务可分解为独立的原子指令，对需要全局推理或跨块引用的任务（如复杂因果推理）可能效果有限。且本地模型必须支持工具调用和结构化输出，对1B模型能力要求高。
- **缺少与更多基线对比**：未与最新的RAG变体（如HyDE、迭代检索）或长上下文模型（如Claude 2.0 200K）进行直接比较，尽管附录E.3做了部分RAG对比，但不够全面。

（完）
