---
title: "Chain of Agents: Large Language Models Collaborating on Long-Context Tasks"
title_zh: 智能体链：大语言模型协作处理长上下文任务
authors: "Yusen Zhang, Ruoxi Sun, Yanfei Chen, Tomas Pfister, Rui Zhang, Sercan O Arik"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=LuCLf4BJsr"
tags: ["query:eca"]
score: 8.0
evidence: 多智能体协作处理长上下文任务
tldr: 针对长上下文处理中信息丢失问题，提出Chain-of-Agents框架，通过多智能体自然语言协作进行信息聚合与推理。实验表明CoA在多个长上下文基准上优于RAG和长窗口方法，为多智能体协作处理长文本提供了有效方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 321, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 714, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 719, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 983, \"height\": 179, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 725, \"height\": 671, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-luclf4bjsr/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 447, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 811, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1449, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1451, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1446, \"height\": 204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 238, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1466, \"height\": 580, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1444, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1227, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1531, \"height\": 873, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1534, \"height\": 743, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1556, \"height\": 950, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1553, \"height\": 1184, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1556, \"height\": 680, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1445, \"height\": 133, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 774, \"height\": 177, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1381, \"height\": 458, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-luclf4bjsr/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1446, \"height\": 461, \"label\": \"Table\"}]"
motivation: 现有方法如RAG和扩大窗口在长上下文任务中各有不足。
method: 提出Chain-of-Agents框架，让多个LLM通过自然语言链式协作处理长文本。
result: CoA在多个基准上显著优于对比方法。
conclusion: 多智能体协作是处理长上下文的有效途径。
---

## Abstract
Addressing the challenge of effectively processing long contexts has become a critical issue for Large Language Models (LLMs). Two common strategies have emerged: 1) reducing the input length, such as retrieving relevant chunks by Retrieval-Augmented Generation (RAG), and 2) expanding the context window limit of LLMs. However, both strategies have drawbacks: input reduction has no guarantee of covering the part with needed information, while window extension struggles with focusing on the pertinent information for solving the task. To mitigate these limitations, we propose Chain-of-Agents (CoA), a novel framework that harnesses multi-agent collaboration through natural language to enable information aggregation and context reasoning across various LLMs over long-context tasks. CoA consists of multiple worker agents who sequentially communicate to handle different segmented portions of the text, followed by a manager agent who synthesizes these contributions into a coherent final output. CoA processes the entire input by interleaving reading and reasoning, and it mitigates long context focus issues by assigning each agent a short context. We perform a comprehensive evaluation of CoA on a wide range of long-context tasks in question answering, summarization, and code completion, demonstrating significant improvements by up to 10% over strong baselines of RAG, Full-Context, and multi-agent LLMs.

---

## 论文详细总结（自动生成）

# 论文《Chain of Agents: Large Language Models Collaborating on Long-Context Tasks》详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：大语言模型（LLM）在处理长上下文任务时面临两大挑战：
  - **输入缩减方法**（如RAG）：通过检索相关片段来缩短输入，但可能遗漏关键信息，导致“感受野”不完整。
  - **窗口扩展方法**（如扩大上下文窗口）：虽能处理更长的输入，但模型容易“迷失在中间”，无法有效聚焦于任务所需的信息，且成本高昂。
- **整体含义**：本文旨在提出一种无需额外训练、任务无关且可解释的框架，通过多智能体协作自然语言交流，同时克服上述两种方法的缺点，实现高效、准确的长上下文处理。

## 2. 论文提出的方法论

### 核心思想
- 灵感来源于人类在有限工作记忆下“边读边处理”的认知模式。
- 将长文本分割成多个短块，每个块由一个“工作智能体”（Worker Agent）负责处理；工作智能体之间通过“通信单元”（Communication Unit, CU）顺序传递信息；最后由一个“管理智能体”（Manager Agent）综合所有信息生成最终答案。

### 关键技术细节
- **Stage 1：工作智能体链式通信**
  - 将长输入 \(x\) 分割成 \(l\) 个块 \(c_1, c_2, \dots, c_l\)，每块长度不超过窗口大小 \(k\)。
  - 初始化 \(CU_0 = \text{空}\)。
  - 第 \(i\) 个工作智能体 \(W_i\) 输入：指令 \(I_W\)、前一个通信单元 \(CU_{i-1}\)、当前块 \(c_i\)、查询 \(q\)；输出 \(CU_i = LLM_{W_i}(I_W, CU_{i-1}, c_i, q)\)。
  - 通信单向传递，使得最后一个工作智能体能获取整个文本的推理链。

- **Stage 2：管理智能体信息整合**
  - 管理智能体 \(M\) 输入：指令 \(I_M\)、最后一个通信单元 \(CU_l\)、查询 \(q\)；输出最终答案 \(\text{Response} = LLM_M(I_M, CU_l, q)\)。

- **时间复杂度分析**（解码器架构）：
  - Full-Context: 编码 \(O(n^2)\)，解码 \(O(nr)\)。
  - CoA: 编码 \(O(nk)\)，解码 \(O(nr)\)（\(k \ll n\)，因此编码更高效）。
  - RAG: 编码 \(O(nk') + O(k^2)\)，解码 \(O(n/k') + O(kr)\)。

### 公式与算法流程（文字说明）
- **算法1（CoA流程）**：
  1. 将源输入 \(x\) 按句子分割成块 \(c_1, \dots, c_l\)，每块长度 < \(k\)。
  2. 初始化 \(CU_0\) 为空。
  3. 循环 \(i=1 \dots l\)：调用 \(W_i\) 生成 \(CU_i\)。
  4. 管理智能体 \(M\) 根据 \(CU_l\) 和 \(q\) 生成最终回答。

## 3. 实验设计

### 数据集与场景
- **9个数据集**，涵盖三类任务：
  - **问答（QA）**：HotpotQA（多跳）、MuSiQue（更难的多跳）、NarrativeQA（整本书/电影）、Qasper（NLP论文）、QuALITY（长文章多项选择）。
  - **摘要（Summarization）**：QMSum（基于查询的会议摘要）、GovReport（政府报告通用摘要）、BookSum（书籍级叙事摘要）。
  - **代码补全（Code Completion）**：RepoBench-P（基于仓库的下一行代码）。

### Benchmark
- 每个数据集使用标准指标：QA用F1（除QuALITY用精确匹配）、摘要用ROUGE几何平均、代码补全用代码相似度。

### 对比方法
- **基线**：
  - **Vanilla**：直接截断输入到窗口大小。
  - **RAG**：使用SOTA检索器（基于BGE嵌入）重排序，将最相关块拼入窗口。
  - **多智能体变体**：
    - **Merge**：各工作智能体独立生成答案，多数投票。
    - **Hierarchical**：树形结构，工作智能体只向管理智能体汇报，无同级通信。
- **骨干LLM**：PaLM 2（text-bison, text-unicorn，窗口8k）、Gemini 1.0（ultra，窗口32k）、Claude 3（haiku/sonnet/opus，窗口200k）。

## 4. 资源与算力

- **明确说明**：论文未公开GPU型号、数量或训练时长。
- **间接信息**：实验通过API调用商业模型（Vertex model garden）完成；RAG检索使用Huggingface模型在A100 GPU上运行；所有实验温度设为0（确定性生成）。
- **时间成本分析**：文中给出了理论时间复杂度，并基于llama3-8b进行了实际运行时间比较（见表9），但未提供完整算力需求。

## 5. 实验数量与充分性

- **实验数量**：非常充分。
  - **主要结果**：基于6种LLM在9个数据集上的完整对比（表4、表5）。
  - **消融实验**：验证管理智能体必要性、阅读顺序（左→右、右→左、随机）、多路径增强（双向、自洽、排列）。
  - **鲁棒性分析**：不同窗口大小（4k~128k）、不同输入长度、信息丢失度量、NIAH测试。
  - **案例研究**：展示多跳推理链。
- **公平性与客观性**：
  - 使用标准基准（LongBench、SCROLLS）和公平的基线（RAG采用SOTA检索器，Full-Context采用相同模型但使用最大窗口）。
  - 所有实验温度设为0，消除随机性。
  - 对长上下文LLM（Claude 3）也进行了对比，显示CoA在即使200k窗口下依然大幅领先。
- **结论**：实验设计系统、全面，覆盖多种任务、多种模型和多个维度，充分支持论文的声称。

## 6. 论文的主要结论与发现

- **CoA显著优于所有基线**：在9个数据集上，CoA相比Vanilla和RAG提升最高达10%（如NarrativeQA提升13.30%）。
- **即使与长上下文LLM（Claude 3 200k）相比，CoA（8k窗口）仍显著更强**，说明多智能体链式通信比单纯扩大窗口更有效。
- **CoA缓解了“迷失在中间”问题**：通过给每个智能体分配短上下文，使模型能更好地聚焦。
- **CoA对长输入更有效**：输入越长，CoA相对于Vanilla的提升越明显。
- **多路径增强可进一步提升性能**：如5路排列投票或判断可带来额外增益，且仍有较大提升空间（oracle上限很高）。

## 7. 优点

- **方法新颖且简洁**：首次将去中心化链式通信引入长上下文任务，无需训练，即插即用。
- **任务与模型无关**：灵活适用于QA、摘要、代码补全等多种任务，且可替换不同LLM作为骨干。
- **高可解释性**：通信单元（CU）记录了推理链，用户可追溯每个智能体的贡献。
- **成本效率**：相比Full-Context，编码复杂度从 \(O(n^2)\) 降至 \(O(nk)\)；且可通过并行解码进一步降低延迟。
- **鲁棒性强**：对窗口大小不敏感，性能稳定，且能有效处理不同输入长度。
- **实验全面**：在9个数据集、6种LLM上进行了详尽评估，并包含消融、鲁棒性、案例分析等。

## 8. 不足与局限

- **沟通效率可优化**：当前LLM的训练对齐（RLHF）可能导致冗余或拒绝性回应，需进一步微调或提示工程来提高智能体间通信质量。
- **未探索复杂通信形式**：仅采用单向链式传递，未尝试辩论、多轮讨论等更复杂的协作模式。
- **成本与延迟**：虽然理论上并行可降低延迟，但实际多步调用仍可能增加API调用次数和总延迟。文中仅给出近似并行加速，缺乏真实分布式部署评估。
- **信息丢失**：约1%-4%的信息在链式传播中丢失，尽管最终结果影响不大，但仍有提升空间。
- **提示工程依赖**：性能可能受提示设计影响，对未见过的LLM需手动调整。
- **实验覆盖有限**：未在更大规模（如>100个智能体）或更动态的场景（如流式输入）中验证。
- **统计显著性**：虽温度固定，但未报告多次运行的标准差或置信区间，基线对比缺乏误差棒。

（完）
