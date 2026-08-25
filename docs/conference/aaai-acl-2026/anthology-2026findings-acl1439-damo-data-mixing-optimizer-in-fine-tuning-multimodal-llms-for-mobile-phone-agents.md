---
title: "DaMo: Data Mixing Optimizer in Fine-tuning Multimodal LLMs for Mobile Phone Agents"
title_zh: DaMo：面向手机智能体的多模态大模型微调数据混合优化器
authors: "Kai Shi, Jun Yang, Ni Yang, Binqiang Pan, Qingsong Xie, Zhangchao, Zhenyu Yang, Tianhuang Su, Haonan Lu"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1439.pdf"
tags: ["query:mobile-agent"]
score: 8.0
evidence: 针对手机智能体微调中的数据配比问题进行优化，提升多任务执行能力
tldr: 手机智能体需要同时处理多个手机任务，但多模态大模型在微调时难以确定最优数据混合比例，影响多任务效果。DaMo提出一种可训练的数据混合优化器，通过预测任意数据配比下的下游任务性能来自动搜索最佳数据混合。实验证明DaMo能显著提升多任务手机智能体的综合表现，为移动端智能体的构建提供了一种重要的数据工程工具，缓解手工调参繁琐并提升训练效率。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1650, \"height\": 472, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 372, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 500, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 487, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1052, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1430, \"height\": 951, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 629, \"height\": 985, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 644, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 395, \"height\": 171, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 771, \"height\": 273, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 400, \"height\": 180, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 415, \"height\": 852, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 409, \"height\": 194, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 667, \"height\": 520, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1439/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 648, \"height\": 460, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 686, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1058, \"height\": 322, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1327, \"height\": 215, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1721, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1450, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 809, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 789, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1408, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1439/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 743, \"height\": 807, \"label\": \"Table\"}]"
motivation: 手机智能体多任务微调时数据混合比例难以确定，限制了多任务性能。
method: 提出DaMo数据混合优化器，训练网络预测不同数据配比的下游性能并选取最优配比。
result: 实验证明DaMo能提升多任务手机智能体性能，超过人工数据配比。
conclusion: 为手机智能体的数据驱动构建提供了自动混合优化方法，具有广泛适用性。
---

## Abstract
Mobile Phone Agents (MPAs) have emerged as a promising research direction due to their broad applicability across diverse scenarios. While Multimodal Large Language Models (MLLMs) serve as the foundation for MPAs, their effectiveness in handling multiple mobile phone tasks simultaneously remains limited. Although multitask supervised fine-tuning (SFT) is widely adopted for multitask learning, existing approaches struggle to determine optimal training data compositions for peak performance. To address this challenge, we propose DaMo (Data Mixture Optimizer) – a novel solution employing a trainable network that predicts optimal data mixtures by forecasting downstream task performance for any given dataset ratio. To support comprehensive evaluation, we introduce PhoneAgentBench, the first specialized benchmark to evaluate MLLMs on multimodal mobile phone tasks, comprising 1,235 QA pairs spanning diverse real-world industrial mobile application scenarios. Demonstrating strong predictive capability (R²=0.81) in small-scale pilot experiments, DaMo efficiently extrapolates optimal data mixing configurations. Our results show DaMo achieves 3.06% average score improvement on PhoneAgentBench and open-source benchmarks, including BFCL-v3, MME-Reasoning, MME-Perception, and OCRBench, compared to alternative methods. Through predicting optimal data mixture only on open-source benchmarks, DaMo outperforms other approaches by 6.70% in terms of average score. Moreover, DaMo improves the metrics by 12.74% than other methods when used solely for MLLM optimization on the BFCL-v3 task. Notably, DaMo maintains robust scalability, preserving its effectiveness when applied to other model architectures.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机与背景）

- **研究背景**：手机智能体（Mobile Phone Agents, MPAs）因在多样化场景中的实用性而受到广泛关注，其理想形态需要同时掌握环境感知、任务规划、多模态推理、函数调用和个性化记忆等多种能力。多模态大语言模型（MLLMs）被视为构建理想智能体的关键基础，但现有MLLM在同时处理多个手机任务时效果有限。
- **核心问题**：多任务监督微调（SFT）虽被广泛采用，但**难以确定最优的训练数据混合比例**。在数据源和下游任务数量众多的情况下，如何找到最大化模型性能的数据配比策略，是一个关键且未解决的挑战。
- **现有方法的不足**：
  - 已有数据混合优化工作（DoReMi、ODM、BiMix等）主要针对**预训练阶段**，通过预测验证集损失来优化配比，无法直接适用于MLLM微调——因为微调性能与下游任务准确率并非直接相关。
  - 工业界常用的均匀采样、自然采样、随机采样等策略因配比固定或随机而难以达到最优。
  - 网格搜索在数据源数量增大时计算成本不可接受。
- **论文的整体含义**：提出一种新的数据混合优化范式——**直接预测下游任务性能**而非验证损失，以数据驱动方式自动搜索最优混合配比；同时填补了手机智能体领域缺乏**综合性、多模态工业场景基准**的空白。

## 2. 论文提出的方法论（核心思想、关键技术细节、公式与算法流程）

### 2.1 核心思想

- 提出 **DaMo（Data Mixing Optimizer）**，通过 **下游任务性能预测方法（Downstream Task Performance Prediction, DaPP）** 构建一个可训练的神经网络（MLP），以数据混合比例和训练步数为输入，直接预测下游任务性能得分。
- 借助MLP的低推理成本，在整个数据混合空间中**外推预测**所有可能配比的性能，排序后选取最优配比进行实际训练。

### 2.2 关键技术细节

**问题建模**：
- 设有 m 个异构训练数据集 D = ∪Dᵢ，总样本数为 N，批大小为 b，训练步数 T = ⌈N/b⌉。
- 数据混合比例为 p = [p₁, p₂, ..., pₘ]，满足 ∑pᵢ = 1。
- 目标为找到最优配比 p*，使下游任务平均得分最大化：
  - **公式**：p* = arg max_{p∈P, t≤T} E_{θ∼A(p,t,θ₀)} S_θ

**空间剪枝**：
- 原始数据混合空间规模达 |P| = N!/(b!)ᵀ，计算上不可行。通过忽略组内样本顺序并保持混合配比固定，将搜索空间缩小至固定混合空间 P_fix，规模为 |P_fix| = C(m+b-1, m-1)。在 m=12、b=16 时约有 1.3×10⁷ 种可能配比。

**为什么放弃指数/幂律函数**：
- 论文通过系统性实验验证了训练动态的复杂性，如图3所示：
  - **增强效应**：MMU训练显著提升ACU表现
  - **冲突效应**：APP-Rec性能随MMU训练步数增加而退化
  - **中性效应**：MM-NER与MMU训练无相关性
  - **过拟合效应**：MT-Plan随训练呈现先升后降的非单调趋势
- 双数据集混合的3D性能曲面呈**非凸拓扑**，沿两个轴均存在非单调波动，从根本上排除了解析解和传统函数拟合的可能。

**MLP拟合并外推**：
- 将 f 实现为多层感知机（MLP），直接映射（数据混合比例, 训练步数）→ 任务性能。
- 拟合完成后，遍历 P_fix 中所有配比预测得分，排序取Top-k进行实际训练。
- 完整算法流程（Algorithm 1）包括四步：
  1. **边界感知分层随机采样**：随机选择数据集组合（k从1到12），通过平滑概率上采样稀疏和密集组合，再对均匀比例施加随机扰动生成多样配比——避免高维单纯形中纯随机采样的“维度灾难”。
  2. **收集训练样本**：对每个采样的混合配比训练MLLM，按固定间隔保存检查点（4个不同训练步），评估下游任务性能，生成 (p, t, s) 样本点。
  3. **MLP训练与10折交叉验证**：计算R²评估拟合质量。
  4. **最优配比搜索与最终评价**。

## 3. 实验设计（数据集、基准、对比方法）

### 3.1 PhoneAgentBench 基准

论文构建了**首个专用于评估MLLM在手机智能体任务上综合能力的基准**，包含1,235个QA对，覆盖6个数据集：

| 数据集 | 评估能力 | 数据规模 |
|---|---|---|
| MT-Plan | 多模态任务规划（DAG结构） | 100 |
| MM-RR | 多模态指代消解（二分类） | 130 |
| ACU | 智能体上下文理解（多轮对话） | 100 |
| MM-NER | 多模态命名实体识别（7类实体，F1评估） | 376 |
| APP-Rec | 手机应用识别 | 100 |
| Mobile-FC | 移动端函数调用（50个核心接口） | 429 |

- **质量设计**：50个核心移动接口的覆盖规模与BFCL-v4（29个核心API）对齐；MT-Plan复杂度评分为0.661，是T-Eval（0.122）的5.4倍；数据经过三标注者交叉验证，不一致数据被剔除。

### 3.2 训练数据集

共12个数据源：
- **自建**：MMIE（1.8k）、APP-Rec（22.8k）、MMU（21.1k）、RR（10.5k）、TP（26.8k）、FC（10.4k）、ITR（9.7k）
- **开源**：ShareGPT4（36k）、NER（8k）、Infinity-MM（37.2k）、OCR（33k）、SuperCLUE-Agent（1.5k）

### 3.3 对比方法

- **Uniform Mixture**：均匀采样
- **Natural Mixture**：按数据集规模比例采样
- **Random(250)**：随机采样250种配比并取最佳性能
- **DML (Data Mixing Laws)**：SOTA方法，基于损失拟合指数函数推导最优配比
- **DaMo**、**DaMo(\*)**（单任务优化）

### 3.4 评估基准

- **主实验**：PhoneAgentBench + 开放基准（BFCL-V3、MME-Perception、MME-Reasoning、OCRBench）
- **未见数据集泛化**：BFCL-V4、MMBench、DocVQA、MMMU
- **模型迁移**：Qwen2.5VL-3B-Instruct、Qwen2.5VL-7B-Instruct、InternVL3-14B

## 4. 资源与算力

- **基础模型**：InternVL2.5-4B；训练使用 **8块 NVIDIA H20 GPU**。
- **采样训练成本**：250个混合配比样本、每个4个检查点，共1000次下游评估，消耗 **4,225 GPU小时**。
- **最终训练**：DaMo和DML在各自最优配比上额外微调一次，总成本分别为 **4,242和4,244 GPU小时**。
- **低预算基线**：Uniform/Natural仅需21 GPU小时；但延长至63 GPU小时无性能提升（模型已收敛），说明其性能次优源于配比设计不佳而非算力不足。
- **部署开销**：DaMo不引入任何额外推理开销，最终模型尺寸不变；一次性采样成本在工业大规模部署中被充分摊薄。
- 论文未单独报告每轮训练的具体墙钟时间，仅提供GPU小时综合指标。

## 5. 实验数量与充分性评估

### 5.1 实验规模概览

论文包含**六组核心实验**，覆盖面较广：

1. **MLP拟合能力验证**：50→250样本的R²增长曲线（0.58→0.81），含10折交叉验证
2. **主实验**：PhoneAgentBench + 4个开放基准的综合对比（表2、表3）
3. **Top-50配比验证**：预测最优的50个配比的实际训练得分分布（图4）
4. **未见数据集泛化**：BFCL-V4、MMBench、DocVQA、MMMU（表4）
5. **跨模型迁移**：3个不同架构/规模的模型（表5、图5），含原始DaMo和线性校正DaMo(lin)
6. **成本效益分析**：GPU小时对比（表2）

### 5.2 充分性与客观性评估

- **优点**：
  - 对比方法覆盖了常用的启发式基线和SOTA方法，较为全面
  - 同时评估了基准内和基准外、已见和未见数据集，验证泛化能力
  - 跨模型迁移实验增加了结论的普适性
  - 10折交叉验证保证了R²结果的可靠性
  
- **不足**：
  - **DML基线在BFCL-V3上表现异常低（25.47）**，甚至低于w/o SFT（29.32），这可能是由于DML基于验证损失而非下游任务性能的天然劣势，但也可能存在超参数适配问题
  - 未报告实验的随机种子数或多次运行的标准差/方差，统计显著性未知
  - PhoneAgentBench的**Golden Plan评估依赖T-Eval的评估器**，该评估器在复杂DAG结构上的准确性未单独验证
  - 250个混合样本中约60%的样本对应单个数据集训练（k=1），可能造成对边界区域过拟合

## 6. 主要结论与发现

1. **MLP拟合高效性**：仅需250个混合配比样本即可达到 **R²=0.81** 的预测精度（10折交叉验证），表明"数据配比→下游性能"的映射函数具有良好的平滑性（低Lipschitz常数），采样复杂度由内在维度而非搜索空间基数决定。
2. **主实验全面超越**：在PhoneAgentBench+开放基准的总体平均分上，DaMo（68.13%）超越最佳基线DML（65.07%）**3.06%**，超越Uniform（59.22%）8.91%。
3. **单任务优化增益更大**：DaMo(\*)（仅针对单任务预测最优配比）在MT-Plan上达到62.00%（vs. uniform 54.50%），APP-Rec达到67.00%，在开放基准上BFCL-V3达到47.43%（vs. uniform 34.69%），提升12.74%。
4. **随机搜索不可靠**：图4(a)显示250种随机配比的得分分布缺乏右尾长尾，最优配比极为稀疏；图4(b)显示DaMo预测的Top-50配比性能显著高于所有基线。
5. **跨模型迁移稳健**：直接迁移DaMo至Qwen2.5VL-3B/7B和InternVL3-14B，仍优于Uniform/Natural/DML；经20个校准样本进行线性映射后，Pearson相关系数从0.75以上提升至0.9以上。
6. **最优配比与数据规模无关**：多出的GPU训练时长（21→63小时）对Uniform/Natural无增益，证明其性能瓶颈在配比设计而非算力。

## 7. 优点（方法/实验设计的亮点）

1. **任务-性能直接预测范式创新**：与预训练数据混合优化（预测loss）不同，DaMo直接预测下游任务性能，避免了"损失低但性能差"的失配问题。论文通过图3实证展示了SFT阶段任务的相互作用模式（增强/冲突/中性/过拟合），有力证明了指数/幂律函数的不适用性。
2. **边界感知分层采样策略**：利用高维单纯形体积集中于边界的几何特性，设计平滑概率上采样稀疏（小k）和密集（大k）组合的采样方法，以250个样本覆盖约1.3×10⁷级的配比空间，样本效率高且具有理论支撑（L-Lipschitz函数度量熵理论）。
3. **成本效益分析完整**：明确比较了各方法的GPU小时成本，证明DaMo在相同预算下性能更优，且一次性采样成本可被工业部署摊薄。
4. **全面评估体系设计**：不仅给出核心基准结果，还扩展至未见数据集、跨模型迁移、单任务优化等多个维度，多角度验证方法有效性。
5. **PhoneAgentBench设计合理**：规模虽小但覆盖全面（1235个样本、6个任务、50个核心移动接口），复杂度显著高于已有基准（MT-Plan复杂度为T-Eval的5.4倍），并设置严格的数据质量控制流程（三标注者交叉验证、Golden Plan）。
6. **卓越的工程实用性**：最终模型大小不变、零额外部署推理开销、可无缝迁移至新基准和新模型，适合工业大规模应用。

## 8. 不足与局限

1. **实验覆盖的局限性**：
   - 论文自述因算力和时间限制，**未测试更大规模模型**（如Qwen3-VL-235B-A22B-Instruct），无法验证DaMo在超大规模模型上的有效性。
   - 采样训练仅在**InternVL2.5-4B单一模型**上进行，未做多模型采样训练的对比实验来验证基模型选择对配比预测的影响。
   - PhoneAgentBench虽为首次提出，但作为自我构建基准，**缺乏第三方独立评估**，其标注质量与标准性有待外部验证。

2. **性能预测精度仍有空间**：R²=0.81说明仍有约19%的方差未被解释，意味着预测的Top-1配比可能并非全局最优。对于性能敏感的下游任务，预测误差可能带来实际性能损失。

3. **统计严谨性欠缺**：未报告多次运行的均值±标准差，未提供显著性检验；关键结果（如表3中DaMo在BFCL-V3的43.15）可能对特定检查点、特定训练运行敏感。

4. **Baseline适配性问题**：DML在BFCL-V3上的较差表现可能部分源于方法本身的局限性（基于loss而非任务性能），但也可能与未充分调参有关，存在一定的不公平竞争风险。

5. **线性映射校正的机制不明确**：DaMo(lin)通过20

3. **未提供动态配比的上界对比**：论文将搜索空间从完整的排列空间（含批次内顺序、动态配比变化）压缩至固定混合空间，这在计算上是必要的，但论文未通过任何实验或理论分析说明：固定配比下的最优性能与动态配比（如课程学习、分阶段切换数据源）的最优性能之间是否存在差距。如果动态配比的上界显著高于固定配比，则DaMo所搜索的“最优”本身可能只是次优空间中的最优。

4. **对数据源数量扩展性缺乏讨论**：所有实验均在m=12个数据源下完成。随着数据源数量增长到数十甚至数百（例如大型工业平台按领域、语言、任务粒度拆分的细粒度数据池），采样策略是否仍能高效覆盖高维单纯形、MLP是否还能在有限样本下保持R²≥0.8，均未得到验证。换言之，DaMo的样本复杂度与数据源数量之间的关系是未知的。

5. **DaMo(\*)的适用场景未详细讨论**：单任务优化版本的DaMo在部分任务上取得了很大增益，但也可能牺牲其他任务的表现。论文未报告DaMo(\*)在其他任务上相对各基线的性能折损程度，也未能给出何时选择单任务优化而非多任务优化（或两者结合）的清晰准则。

6. **任务评估中可能存在的评估器依赖**：MT-Plan任务的Golden Plan评估依赖于T-Eval评估器，但T-Eval最初设计于文本型任务规划场景，将其迁移至包含多模态截图输入和DAG结构的复杂规划场景时，其评分准确性、容错性（如对语义等价但结构不同的合法计划的判定）并未单独验证，可能引入噪声。

## 9. 总体评价与展望

### 9.1 总体定位

DaMo是一项**工程导向鲜明、方法论有新意**的数据混合优化工作。它的核心贡献不是提出新的模型架构或训练算法，而是解决了MLLM微调中一个现实且棘手的问题——**如何在众多数据源和下游任务之间科学地分配训练数据**。论文将“预测验证损失”的传统数据混合优化范式，转向“预测下游任务性能”的新范式，这一转变在SFT/指令微调场景下具有直观合理性和坚实实验支撑。

### 9.2 对领域的可能影响

- **方法层面**：DaMo提供了一种可复用的数据配比搜索框架。其“采样少量配比→训练小模型→MLP拟合→外推搜索”的流程，可以被后续研究广泛应用于其他模型家族、其他微调场景（如代码生成、数学推理、多轮对话），具有较好的可扩展性。
- **基准层面**：PhoneAgentBench填补了手机智能体方向缺乏统一、多模态、面向工业场景评估基准的空白。尽管规模不大，但其任务设计（DAG规划、50核心函数调用、多轮上下文理解等）贴近真实手机助手的使用方式，有望成为该领域后续研究的参考基准。
- **实践层面**：DaMo不改变最终模型结构、不引入推理开销，一次性搜索成本可被大规模生产摊薄，这使其具备被工业界直接采用的潜力。

### 9.3 未来可能的研究方向

1. **将DaMo扩展至更大规模模型**（如70B以上），验证采样阶段的小模型（4B）预测的大模型最优配比是否仍然准确，探索“代理模型”加“大模型”的两阶段搜索范式。
2. **引入动态配比搜索**，将时间维度上的配比变化（课程学习、阶段性切换）纳入搜索空间，进一步逼近全局最优。
3. **针对不同下游任务设置不同权重**，设计多目标优化版本，使配比选择可以按业务需求灵活调整。
4. **结合自动化数据质量评估**，将数据质量信号作为MLP的辅助输入，提升预测精度并降低对采样量的依赖。

### 9.4 结论

综上，DaMo是一篇**问题真实、方法可靠、实验充分、工程价值高**的工作。它在数据混合优化这一传统问题上提出了新的视角，并以系统的实验证明了“直接预测下游任务性能”这一思路在MLLM微调场景中的有效性。虽然存在统计严谨性、基准独立验证、训练基模型单一等局限，但整体而言，该工作对于手机智能体及相关多模态模型的数据工程实践具有重要的参考意义和实用价值。论文中的PhoneAgentBench以及DaMo方法，均有望成为后续研究的重要基础。

（完）
