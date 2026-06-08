---
title: "Collaborative Reasoner: Self-Improving Social Agents with Synthetic Conversations"
title_zh: 协作推理者：通过合成对话自我改进的社会智能体
authors: "Ansong Ni, Ruta Desai, Yang Li, Xinjie Lei, Dong Wang, Jiemin Zhang, Jane Yu, Ramya Raghavendra, Gargi Ghosh, Shang-Wen Li, Asli Celikyilmaz"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=dye9w8IOV0"
tags: ["query:eca"]
score: 7.0
evidence: 评估和提升LLM智能体协作推理能力的框架
tldr: 当前LLM训练忽视多轮协作技能。本文提出Coral框架，通过合成对话训练和评估智能体的说服、断言等协作推理能力。实验表明，经Coral训练的智能体在需要协作辩论的任务中正确率大幅提升，为构建高效社会性智能体提供了评估与训练工具。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1464, \"height\": 643, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1426, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1432, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 867, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 573, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1150, \"height\": 703, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1213, \"height\": 344, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dye9w8iov0/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1421, \"height\": 550, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1309, \"height\": 452, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1323, \"height\": 392, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 637, \"height\": 396, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1341, \"height\": 597, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 782, \"height\": 418, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1238, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1453, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dye9w8iov0/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1280, \"height\": 176, \"label\": \"Table\"}]"
motivation: 现有单轮训练忽视了智能体间有效说服与争执等协作能力。
method: 构建包含多种协作任务的合成对话数据集，进行训练与评估。
result: 协作任务准确率显著高于基线模型。
conclusion: 针对性训练能有效提升智能体的协作推理能力。
---

## Abstract
With increasingly powerful large language models (LLMs) and LLM-based agents tackling an ever-growing list of tasks, we envision a future where numerous LLM agents work seamlessly with other AI agents and humans to solve complex problems and enhance daily life. To achieve these goals, LLM agents must develop collaborative skills such as effective persuasion, assertion and disagreement, which are often overlooked in the prevalent single-turn training and evaluation of LLMs. In this work, we present Collaborative Reasoner (Coral), a framework to evaluate and improve the collaborative reasoning abilities of language models. In particular, tasks and metrics in Coral necessitate agents to disagree with incorrect solutions, convince their partners of a correct solution, and ultimately agree as a team to commit to a final solution, all through a natural multi-turn conversation. Through comprehensive evaluation on six collaborative reasoning tasks covering domains of coding, math, scientific QA and social reasoning, we show that current models cannot effectively collaborate due to undesirable social behaviors, collapsing even on problems that they can solve singlehandedly. To improve the collaborative reasoning capabilities of LLMs, we propose a self-play method to generate synthetic multi-turn preference data and further train the language models to be better collaborators. Experiments with Llama-3.1, Ministral and Qwen-2.5 models show that our proposed self-improvement approach consistently outperforms finetuned chain-of-thought performance of the same base model, yielding gains up to 16.7% absolute. Human evaluations show that the models exhibit more effective disagreement and produce more natural conversations after training on our synthetic interaction data.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：当前的大语言模型（LLM）主要针对单轮问答或问题求解进行训练和评估，忽略了多轮对话中的协作技能（如有效说服、坚持正确观点、指出错误、团队达成一致等）。然而，未来AI智能体需要与人类及彼此通过自然语言进行无缝协作，因此必须学会这些“社交技能”。
- **核心问题**：现有前沿LLM在协作推理场景中表现不佳——即使它们能单独解决某个问题，但在多轮对话中却因过度顺从、缺乏说服力和坚持己见而失败，往往过早同意错误答案。
- **整体含义**：这项工作旨在填补LLM协作推理能力评估与训练的空缺，通过构建专用框架和合成数据来提升智能体的协作表现，最终推动更自然、更高效的人机/多智能体协作。

## 2. 方法论：核心思想与关键技术细节

- **核心思想**：提出 **Coral（Collaborative Reasoner）** 框架，用于评估和提升语言模型的协作推理能力。关键在于：
  - **多轮自由对话**：两个智能体就一个推理问题进行自然讨论，要求最终达成一致（Agreement）并给出正确解答。
  - **社交行为度量**：定义并自动提取智能体的信念（Belief），进而计算**一致性正确率**（Agreement Correctness）、**说服力**（Persuasiveness）、**坚持力**（Assertiveness）等指标。
  - **自我改进数据生成**：通过自我对弈（Self-Play）生成合成多轮对话，再经过树搜索（Tree Sampling）+ 信念过滤构造偏好数据，用DPO（Direct Preference Optimization）训练模型。

- **关键技术细节**：
  - **问题定义**：给定问题 \(x\) 和标准答案 \(y^*\)，两个智能体轮流发言（最多20轮），直到达成一致或达到上限。首轮由Agent A发起。
  - **信念提取**：每轮后使用单独提示的LLM提取智能体的当前答案信念（如“答案A”、“不确定”）。
  - **度量公式**：
    - 一致性：\(\alpha(C) = \mathbb{I}(\beta_A = \beta_B \neq \phi)\)
    - 一致性正确率：\(\alpha^*(C) = \mathbb{I}(\alpha(C)=1 \text{ 且 } \beta = y^*)\)
  - **树采样**：每轮采样 \(d=5\) 个响应分支，每个问题独立采样5棵对话树，增加多样性。
  - **信念过滤**：根据提取的信念是否与标准答案匹配，将每个回合标记为正面（正确）或负面（错误），构造偏好对。
  - **DPO训练**：使用上述偏好对进行直接偏好优化，无需独立奖励模型。
  - **Matrix框架**：为支持大规模并行生成合成对话，构建了可扩展的模型服务框架Matrix，集成vLLM/SGLang/API后端、Ray自动扩展、Slurm作业调度，吞吐量比llm-swarm快1.87倍。

## 3. 实验设计

- **数据集/场景**（共6个任务）：
  - **MATH**（数学推理，7.5k训练/1k测试）
  - **MMLU-Pro**（通用多学科，10.8k训练/1.2k测试）
  - **GPQA**（研究生级科学QA，448题，仅测试）
  - **ExploreToM**（心智理论推理，10.4k训练/1.5k测试）
  - **Hi-ToM**（高阶心智理论，600题，仅测试）
  - **MBPP-CR**（改编自MBPP的代码正确性二分类任务，4k训练/1k测试）

- **Benchmark与对比方法**：
  - **强推理模型**：GPT-4o、O1、Gemini-1.5 Pro、Gemini-2.5 Flash、Claude-3.7 Sonnet、Llama-3.1-405B-Instruct。
  - **单智能体基线**：CoT（直接推理）、CoT + SFT（拒绝采样监督微调）、CoT + DPO（单级树采样偏好训练）。
  - **协作基线**：Coral（基础多轮对话）、Coral + SFT（仅用正确回合做监督微调）、Coral + DPO（本文完整方法）。
  - **交叉验证**：训练后模型与其他不同智能体（Qwen-2.5、GPT-4o、Gemini等）配对，评估泛化能力；也在不同数据集间（MMLU-Pro→GPQA、ExploreToM→Hi-ToM）测试迁移。
  - **人类评估**：100个MMLU-Pro样本，对比训练前后Llama-3.1-70B的对话质量（自然度、有效分歧、说服力、礼貌、冗长程度）。

## 4. 资源与算力

- **文中明确信息**：
  - 所有实验在 **AWS p5.48xlarge** 实例上进行，每个实例配备 **8×H100 80GB GPU**。
  - 训练步骤：SFT/DPO训练 **1,000~3,000步**，批大小 **20~50**，序列长度限制 **8,192 token**。
  - 合成数据规模（示例）：Llama-3.1-8B生成的训练对话总回合数：MBPP-CR 33.8k、MATH 85.1k、MMLU-Pro 160.6k、ExploreToM 100.1k；70B模型数据量相似。
  - 未明确说明总GPU小时数，但根据实例配置和数据量，估算需数十至上百GPU小时。

- **注意**：文中未详细列出每次训练的精确时长或总能耗，仅给出了关键超参数。

## 5. 实验数量与充分性

- **实验数量**：覆盖6个任务、3个基础模型系列（Llama-3.1 8B/70B、Qwen-2.5-7B、Ministral-8B）、多个对比基线（CoT/CoT+SFT/CoT+DPO/Coral/Coral+SFT/Coral+DPO）、交叉泛化实验（4种搭档模型）、跨数据集泛化、人类评估。
- **充分性**：
  - **多样性**：任务涵盖数学、代码、科学、常识、心智理论，领域广泛。
  - **对比严谨**：不仅与单智能体CoT对比，还比较了相同基线的SFT/DPO，控制了推理成本的影响。
  - **消融实验**：包含SFT vs DPO、Coral vs CoT训练、跨模型/跨数据集泛化，以及人类评估。
  - **局限性**：未在更大模型（如405B）上做完整训练（仅评估）；部分任务（MATH）上Llama-3.1未提升，但在其他模型上有效；实验未报告多次运行的标准差（提到方差约1%但未系统展示）。总体而言，实验设计比较客观、充分，但可进一步扩展。

## 6. 主要结论与发现

- **当前LLM协作能力不足**：在多数任务上，多轮协作（Coral）表现不优于甚至差于单智能体CoT，尽管使用了更多推理计算。原因在于模型过度顺从、缺乏坚持和有效说服，导致过早同意错误答案（一致性正确率低）。
- **自我改进显著提升协作推理**：Coral + DPO在所有6个任务上普遍优于CoT基线，最高提升16.7%绝对值（绝对准确率）。
- **泛化能力强**：训练后的协作推理者能与不同模型（Qwen、GPT-4o、Gemini、Claude）有效协作，也能迁移到同领域不同数据集（如MMLU-Pro→GPQA提升5.2%~9.2%）。
- **人类评估证实质量提升**：训练后模型在“有效分歧”和“自然度”上明显优于训练前，但冗长程度增加。
- **同时提升单智能体推理**：Coral训练后的模型在CoT评估中也有提升（如MMLU-Pro: Llama-3.1-8B从44.4→46.7；70B从63.8→67.2），说明协作训练不仅改善社交技能，也强化了推理本身。

## 7. 优点

- **评估框架创新**：首次全面定义并自动计算多轮协作中的信念一致性、说服力、坚持力等社交指标，为后续研究提供标准化工具。
- **合成数据高效**：通过自我对弈+树搜索生成高质量偏好数据，无需人工标注，可扩展性强。
- **训练方法简洁有效**：DPO直接优化，搭配信念过滤，无需复杂奖励模型或强化学习。
- **工程系统先进**：Matrix框架支持大规模并行生成，开源发布，有利于社区复现和扩展。
- **实验设计全面**：涵盖多种任务、模型、对比基线、泛化测试和人类评估，论证充分。
- **跨模型泛化验证**：展示了协作技能的可迁移性，实际应用价值高。

## 8. 不足与局限

- **信念提取的鲁棒性**：依赖LLM-as-judge提取信念，对长上下文或推理模型（如Gemini-2.5、O1）可能不准确，影响训练标签质量。
- **训练信号为二元结果**：仅根据回合是否包含正确答案来标记正负，缺乏过程奖励，可能鼓励“版本化”答案而非真正的逐步推理。
- **冗长性问题**：训练后模型更“礼貌”也更冗长，影响对话效率，需进一步优化。
- **MATH任务上Llama模型未提升**：原因未深入分析（可能与数学任务的具体特性或样本量有关）。
- **未探索迭代训练**：作者提到未从多轮DPO迭代中获益，但未展示详细消融。
- **计算成本**：Coral训练需要更长输入序列（比CoT长89%），计算开销较大。
- **仅含闭源/开源模型子集**：未尝试Mistral Large、DeepSeek等更多主流模型，泛化性验证有限。

（完）
