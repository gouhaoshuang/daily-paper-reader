---
title: "SiriuS: Self-improving Multi-agent Systems via Bootstrapped Reasoning"
title_zh: SiriuS：通过自举推理实现多智能体系统的自我改进
authors: "Wanjia Zhao, Mert Yuksekgonul, Shirley Wu, James Zou"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=IDSTtDw4Cs"
tags: ["query:eca"]
score: 9.0
evidence: 通过自举推理优化多智能体系统，直接涉及协作与优化
tldr: 多智能体系统常依赖脆弱的手动提示与启发式，优化困难。SiriuS提出自我改进框架，构建经验库存储高质量推理轨迹，保留成功推理步骤作为训练数据，并引入库增强机制进一步提高数据质量。该方法无需大量人工标注即可持续优化多智能体系统，在多个复杂任务上取得了性能提升。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1426, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 725, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 686, \"height\": 472, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 680, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 514, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 681, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 418, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-idsttdw4cs/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 686, \"height\": 472, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1364, \"height\": 704, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 703, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1443, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1009, \"height\": 275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-idsttdw4cs/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1446, \"height\": 534, \"label\": \"Table\"}]"
motivation: 多智能体系统的优化依赖于人工设计的提示和启发式，难以自动改进。
method: 构建经验库存储成功推理轨迹，并利用库增强机制提供高质量训练数据，驱动自我改进。
result: 在多个复杂任务上，SiriuS显著提升了多智能体系统的性能。
conclusion: 自举推理经验库是实现多智能体系统持续自我优化的有效途径。
---

## Abstract
Multi-agent AI systems powered by large language models (LLMs) are increasingly applied to solve complex tasks. However, these systems often rely on fragile, manually designed prompts and heuristics, making optimization difficult. A key challenge in optimizing multi-agent systems is acquiring suitable training data for specialized agents. We introduce SiriuS, a self-improving, reasoning-driven optimization framework for multi-agent systems. Central to our approach is the construction of an experience library: a repository of high-quality reasoning trajectories. The library is built by retaining reasoning steps that lead to successful outcomes, providing a robust training set for optimizing multi-agent system. Additionally, we introduce a library augmentation procedure that refines unsuccessful trajectories, further enriching the library. SiriuS boosts performance by 2.86% to 21.88% on reasoning and biomedical QA and enhances agent negotiation in competitive settings. Our results show that SiriuS enhances multi-agent performance while generating reusable data for self-correction and self-play enhancement in the future.

---

## 论文详细总结（自动生成）

# SiriuS：通过自举推理实现多智能体系统的自我改进——论文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：多智能体系统（Multi-agent AI systems）由多个大语言模型（LLM）智能体协作解决复杂任务，在推理、编码、药物发现等领域展现了巨大潜力。然而，这些系统通常依赖脆弱的手动设计提示和启发式规则，难以优化。核心困难在于：（1）为每个智能体获取合适的训练信号非常困难；（2）系统中多个组件的灵敏度高，影响整体性能。尽管任务级别的奖励反馈可用，但信用分配（credit assignment）在多智能体语言交互中极为模糊——无法确定成功或失败究竟归因于哪个智能体的哪一步推理。
- **整体含义**：论文提出一种框架，使多智能体系统能够从成功的合作轨迹中自我学习，无需对中间步骤进行直接监督，从而持续改进协作策略。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：构建**经验库（Experience Library）**——一个存储高质量推理轨迹的仓库。通过保留导致成功结果的推理步骤作为训练数据，并通过**库增强（Library Augmentation）** 过程对失败轨迹进行优化和重写，进一步丰富库内容。然后利用这些数据对每个智能体进行监督微调（SFT），迭代提升性能。
- **关键技术细节**：
  - 多智能体系统形式化定义：一个元组 ⟨S, A, T, R, N, G⟩，其中 N 为智能体集合，每个智能体使用策略 πᵢ，环境反馈通过奖励函数 Rᵢ 给出。
  - **算法流程**（Algorithm 1）：
    1. 初始化智能体策略参数。
    2. 对每个微调迭代：
       - **动作采样**：每个智能体根据自身策略和前序智能体输出采样动作。
       - **轨迹评估与增强**：使用奖励函数评估轨迹，高奖励轨迹加入好轨迹集合 Cⁿ；对未成功轨迹执行增强：由外部智能体基于正确答案生成反馈，引导原智能体重生成解决方案，再重述为直接推理步骤。
       - **监督微调**：在 Cⁿ 上更新每个智能体的策略参数。
  - **三种设置**（Problem-Solving、Actor-Critic、Competitive），对应不同通信结构和奖励设计（见表1、表2）。
  - **Actor-Critic 设置**：Actor 生成解，Judgment 判断正误，Critic 对错误解提供反馈，Actor 根据反馈重新生成。奖励分别赋予正确解、准确判断、有效反馈。
  - **竞争设置**：资源交换、最后通牒博弈、买卖场景，多轮交互，优化每个玩家的策略以最大化自身期望奖励。

## 3. 实验设计：数据集/场景、基准、对比方法

- **数据集/场景**：
  - **Problem-Solving 设置**：College Physics（MMLU、GPQA、TheoremQA 组合）、College Chemistry（类似组合）、PubMedQA（生物医学问答，500训练/500测试）。
  - **Actor-Critic 设置**：PubMedQA。
  - **Competitive 设置**：资源交换游戏、多轮最后通牒游戏、买卖博弈。
- **基准方法**：
  - **Single-Agent**：单一LLM直接响应。
  - **STaR**（Self-Taught Reasoner）：单智能体自监督推理增强。
  - **CoMM**：训练自由的多智能体协作框架。
  - **TextGrad**：通过文本梯度反向传播优化提示。
  - **DSPy（MIPROv2）**：联合优化指令和少样本示例的提示优化器。
  - 在竞争设置中，对比了Self-Correct、单纯Prompt等。
- **模型**：GPT-3.5-turbo-0125、GPT-4o-mini-2024-07-18、Llama-3.2-3B-instruct，温度设为0，使用OpenAI微调API。

## 4. 资源与算力

- **未明确说明**：论文未提及使用的GPU型号、数量、训练时长、计算资源等详细信息。仅提到使用OpenAI Fine-tuning API，未披露微调的具体计算成本。因此无法量化资源消耗。

## 5. 实验数量与充分性

- **实验数量**：涵盖三大设置共多个细化任务：
  - Problem-Solving：3个数据集 × 3种基座模型 × 多基线对比，主表（表3）报告了全部结果。
  - Actor-Critic：PubMedQA上的TP Accuracy和Overall Accuracy对比（表5），包括消融。
  - Competitive：资源交换（两种初始资源配置，并额外做泛化测试）、Ultimatum（两种资源规模）、Sell&Buy（两种估价配置），每个都有多组矩阵（图2-7）。
  - 消融实验（表4）：PubMedQA上回答了五个问题（混合基座智能体、是否角色专用、增强模块效果、额外微调迭代等）。
- **充分性**：实验中报告了均值和标准差（±符号），表明进行了多次重复。数据集划分、基线选择合理，覆盖了不同模型规模（GPT-3.5、GPT-4o-mini、Llama-3.2）和不同任务类型（科学推理、生物医学QA、竞争博弈）。消融实验验证了各组件的贡献。总体较为充分、客观、公平。

## 6. 论文的主要结论与发现

- SiriuS 显著提升多智能体系统性能：在College Physics上提升2.86%-21.88%（不同模型），在PubMedQA上提升至75.33%（GPT-3.5）和73.67%（GPT-4o-mini），优于所有基线。
- Actor-Critic设置下，SiriuS提升了TP Accuracy（判断正确率）和Overall Accuracy，减少了错误修改正确解的问题。
- 竞争设置中，SiriuS作为强势方提高了胜率和收益，作为弱势方减少了损失，且在不同初始配置下展示了泛化能力。
- 消融表明：联合优化所有智能体比优化单个好；角色专用微调优于合并微调；经验增强模块有帮助；额外迭代可微增性能。

## 7. 优点

- **自我改进**：无需人工标注中间步骤，从自生成成功轨迹中学习，可迭代优化。
- **经验库机制**：存储高质量轨迹并增强失败轨迹，有效解决训练数据稀缺问题。
- **通用框架**：适用于多种多智能体设置（问题求解、Actor-Critic、竞争博弈），且可结合不同基座模型。
- **实验设计全面**：覆盖多个任务、模型规模、基线方法，附带消融和泛化测试，论证充分。
- **开源代码**：论文提供代码链接，有利于复现和进一步研究。

## 8. 不足与局限（论文自身及补充）

- **依赖基座LLM能力**：SiriuS性能受限于底层LLM的推理、指令遵循等能力；在弱模型上提升幅度相对有限（例如Llama-3.2提升较小）。
- **信用分配问题仍存**：虽然框架通过从成功轨迹学习来规避直接信用分配，但本质上多智能体间奖励归因问题并未彻底解决，可能影响细粒度优化。
- **交互协议设计复杂**：当前探索了特定通信结构（如Physicist-Mathematician-Summarizer），最优协议可能因任务而异，设计成本较高。
- **计算资源信息缺失**：未报告微调所需计算量，不利于评估可扩展性。
- **泛化性验证有限**：竞争设置中对初始资源配置变化的泛化测试仅做了一两种变化；不同领域（如编程、安全辩论）未覆盖。
- **潜在偏见与安全风险**：系统可能继承LLM的偏见，在竞争场景中可能被滥用（如不公平谈判），论文仅简要提及。

（完）
