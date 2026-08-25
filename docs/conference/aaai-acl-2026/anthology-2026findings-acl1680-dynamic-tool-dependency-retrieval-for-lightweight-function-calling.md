---
title: Dynamic Tool Dependency Retrieval for Lightweight Function Calling
title_zh: 轻量级函数调用的动态工具依赖检索
authors: "Bhrij Patel, Davide Belli, Amir Jalalirad, Maximilian Arnold, Aleksandr Ermolov, Bence Major"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1680.pdf"
tags: ["query:mobile-agent"]
score: 8.0
evidence: 面向端侧函数调用智能体的轻量级动态工具依赖检索方法
tldr: 现有端侧函数调用智能体的工具检索依赖静态有限输入，无法捕捉多步工具依赖和动态任务上下文，易引入无关工具。提出DTDR动态工具依赖检索方法，同时基于初始查询和不断演化的工具调用计划进行检索，并从演示中建模工具依赖。该方法在轻量级条件下实现了自适应的工具选择，提升任务效率与准确率。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1680/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1650, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1680/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1334, \"height\": 541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1680/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1639, \"height\": 369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1680/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1465, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1680/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1491, \"height\": 369, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1654, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1492, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 804, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1491, \"height\": 764, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 811, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1375, \"height\": 360, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1651, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1325, \"height\": 1973, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1680/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1485, \"height\": 2118, \"label\": \"Table\"}]"
motivation: 现有工具检索方法输入静态且有限，无法捕获多步工具依赖和动态任务上下文。
method: 提出DTDR，一种轻量级检索方法，结合初始查询与演化中的工具调用计划，建模工具依赖关系。
result: 动态检索方式减少了无关工具引入，提升了端侧智能体的效率和准确率。
conclusion: DTDR为端侧函数调用智能体提供了高效、自适应的工具选择机制。
---

## Abstract
Function calling agents powered by Large Language Models (LLMs) select external tools to automate complex tasks. On-device agents typically use a retrieval module to select relevant tools, improving performance and reducing context length. However, existing retrieval methods rely on static and limited inputs, failing to capture multi-step tool dependencies and evolving task context. This limitation often introduces irrelevant tools that mislead the agent, degrading efficiency and accuracy. We propose Dynamic Tool Dependency Retrieval (DTDR), a lightweight retrieval method that conditions on both the initial query and the evolving tool calling plan. DTDR models tool dependencies from function calling demonstrations, enabling adaptive retrieval as plans unfold. We benchmark DTDR against state-of-the-art retrieval methods across multiple datasets and LLM backbones, evaluating retrieval precision, downstream task accuracy, and computational efficiency. Additionally, we explore strategies to integrate retrieved tools into prompts. Our results show that DTDR improves function calling success rates between 23% and 104% compared to state-of-the-art static retrievers.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 核心问题与整体含义（研究动机与背景）

- **背景**：基于大语言模型（LLM）的函数调用智能体（function calling agents）通过选择外部工具来自动化复杂任务。在端侧（on-device）部署场景中，受限于内存和延迟约束，通常需要一个检索模块从大规模工具集中筛选出相关工具，以提升性能并压缩提示（prompt）长度。
- **核心问题**：现有工具检索方法输入静态且有限，存在两类主要缺陷：
  - 仅依赖查询（query）与工具描述的语义相似度，忽视了多步计划中已选工具的历史信息；
  - 依赖静态工具依赖图，容易检索出与当前查询无关的工具，或偏向高频重复调用函数，无法适应动态变化的任务上下文。
- **后果**：无关工具的引入会误导智能体决策，降低端侧函数调用的效率与准确率。
- **研究意义**：需在轻量级条件下实现既感知当前任务、又感知演化轨迹的自适应工具检索，以支撑端侧智能体的高效规划与工具选择。

---

### 2. 论文提出的方法论

#### 核心思想
- 提出 **动态工具依赖检索（Dynamic Tool Dependency Retrieval, DTDR）**，将检索模块 ω 建模为同时以用户查询 q 和已有的工具调用轨迹 f₀₋ₜ₋₁ 为条件的函数，即 ω(q, f₀:ₜ₋₁)，从而实现随计划演化的自适应检索。

#### 两种轻量级实现变体

- **DTDR-C（基于聚类）**：
  - 使用预训练嵌入模型对演示查询进行 K-Means 聚类，将相似任务归入同一簇；
  - 为每个簇构建加权工具依赖图 G_k（基于高阶马尔可夫链建模下一工具的条件概率）；
  - 测试时，将查询嵌入映射到最邻近簇，结合当前工具历史在该簇的依赖图上检索候选工具集；
  - 该变体为无监督方法，不需额外训练参数，参数量为 e × K（e 为嵌入维度，K 为簇数）。

- **DTDR-L（基于线性分类器）**：
  - 将查询 q 与当前工具历史 f₀:ₜ₋₁ 拼接后输入冻结的嵌入模型，在顶层训练一个单层线性分类器；
  - 使用 softmax 输出各工具作为下一函数的概率，通过阈值 α 筛选出检索的工具集合 Fₜ = {f | φ(ζ) > α}；
  - 该变体为有监督方法，参数量为 e × |F|，仅依赖于嵌入维度和工具总数，适合低资源场景。

#### 优化目标
- 将函数选择问题形式化为提示优化目标：最大化智能体采样函数属于真实可行函数集合的概率；
- DTDR-L 的训练目标为最小化逐步骤的二进制交叉熵损失之和。

#### 提示编码策略
- 论文探索了硬掩码（Hard Masking）、软掩码（Soft Masking）及其加权变体（Weighted Hard/Soft Masking），将检索到的工具及依赖关系高效编码进 LLM 提示中。

---

### 3. 实验设计

#### 数据集
- **TinyAgent**：典型端侧设备工具集，约 39874 个计划，17 个工具，平均每个计划有 1.9 个工具依赖；
- **TaskBench-DailyLife**：41 个工具，约 3860 个计划，工具依赖约 0.1 个（几乎无依赖）；
- **TaskBench-HuggingFace**：24 个工具，约 4959 个计划，工具依赖约 1.1 个；
- **TaskBench-Multimedia**：41 个工具，约 4310 个计划，工具依赖约 1.5 个。
- 每个数据集约 30% 作为测试集，其余作为演示轨迹用于检索和 ICL 方法。

#### LLM 后端
- 覆盖 7 种模型：**Qwen3 系列（0.6B, 1.7B, 4B, 8B, 14B）**、**GPT-4o**（云端）、**Gorilla-V2**（端侧函数调用微调模型）；
- Qwen3 4B 及以下模型可在典型移动设备上高效运行（INT4 量化，KV cache 约 1 万 token）。

#### 对比基线（按类别划分）
- **BM-25**：经典词项相似度检索；
- **QTS（Query-Tool Similarity）**：包括 Vanilla 嵌入相似度、Tool Graph Retriever（Gao et al., 2025）、Less-is-More Level 1（Paramanayakam et al., 2025）；
- **DR（Dependency Retriever）**：如 ToolNet（Liu et al., 2024a），仅基于最近一次工具调用检索；
- **LR（Learned Retriever）**：如 TinyAgent 的线性分类器（Erdogan et al., 2024），仅基于查询检索；
- **DTDR-C / DTDR-L**：本文提出的动态检索变体。

#### 评估指标
- **检索性能**：MRR（Mean Reciprocal Rank）、F1 score；
- **下游性能**：函数选择准确率（FSA）、端到端任务成功率（SR，同时考虑函数选择与参数填充）；
- **效率**：提示长度（prefill 延迟代理）、模型参数量。

---

### 4. 资源与算力

- 论文中**未明确说明具体 GPU 数量、训练时长、总计算量**等详细算力资源信息；
- 仅提及所有实验在 **NVIDIA A100 GPU** 上进行；Qwen 系列和 Gorilla-V2 使用 FP16 精度，GPT-4o 通过云端 API 调用；
- 模型规模较小（最大 14B），加上检索器为轻量级线性层或聚类模型，整体算力需求相对较低，符合端侧研究定位。

---

### 5. 实验数量与充分性

#### 实验数量（丰富度较高）
- **主检索性能对比**：4 个数据集 × 8 种方法，报告 FSA、MRR、F1 指标；
- **端到端评估**：4 个数据集 × 3 种端侧模型（0.6B、1.7B、4B），报告 FSA 和 SR；另有 8B、14B、Gorilla-V2、GPT-4o 的完整 FSA 结果（附录）；
- **ICL 编码策略对比**：4 种策略（No ICL、Raw Demos、Hard Mask、Soft Mask 及加权变体）在多个数据集上的对比；
- **消融实验**：
  - 历史长度影响（l = 0 到 5+）；
  - K-Means 簇数量影响；
  - 演示数据量影响（1k 到 10k+）；
  - 计划长度对各类检索器的影响；
  - 加权 vs 非加权掩码的对比分析。

#### 充分性与客观性分析
- **优势**：覆盖面较广，涵盖不同模型规模（0.6B–14B + 云端模型）、不同依赖密度的数据集、多种方法类别，结论具有较强的泛化支撑；消融实验较全面，能验证各组件贡献；
- **不足**：
  - 部分数据集（如 TaskBench-DL）本身工具依赖很少，难以充分体现动态检索优势；
  - 端到端评估中较小模型（0.6B）的 SR 普遍偏低（0.4%–8.3%），在较难任务上可能因模型能力达到天花板，难以完全归因于检索方法的差异；
  - 未报告多次运行的方差或显著性检验，统计稳健性未量化。

---

### 6. 主要结论与发现

- **DTDR 大幅提升检索质量**：动态检索（同时条件化查询与工具历史）在所有数据集上显著优于静态检索基线。DTDR-L 在 TinyAgent 上 FSA 达 65.1%，对比静态 LR（25.6%）提升超过 150%；DTDR-C 对比静态 DR 提升 50%–100%。
- **端到端成功率显著提升**：在有工具依赖的数据集（TA、TB-HF、TB-MM）上，DTDR 相比无 ICL 基线将 SR 提升 300%–600%，相比最佳静态检索基线提升 15%–200%；论文摘要指出函数调用成功率较最先进静态检索器提升 23%–104%。
- **小模型也能获得较大收益**：DTDR-L 配合 Qwen3 4B/8B 可超越无检索情况下的 Qwen3 14B 甚至 GPT-4o（部分数据集），缩小了端云模型性能差距。
- **ICL 编码策略影响显著**：硬掩码对小型模型最有效；加权掩码在检索置信度高时更优，而非加权掩码在数据分布偏移较大时更稳健。
- **提示长度显著降低**：DTDR 相比 Raw Demonstrations 可将总提示长度降低最多 73%，动态变量部分降低最多 48%。
- **历史长度与数据量的作用**：历史长度取 3 为最优平衡点；DTDR-L 在少于 1k 演示时过拟合风险明显，DTDR-C 对数据量变化更稳健。

---

### 7. 优点

- **方法设计巧妙且轻量**：两种变体（无监督聚类 + 有监督线性层）均参数量极小，适合端侧部署；同时满足工具依赖感知、免工具描述、查询感知、多步历史感知和小模型适配五个所需条件（现有方法中唯一一个同时满足者）。
- **检索与 LLM 解耦，组合灵活**：DTDR 可搭配任意 LLM backbone 和任意的 ICL 编码策略，适配性较强。
- **对检索与推理的联合影响分析深入**：不仅关注检索指标（MRR/F1），还系统分析了检索质量对下游函数选择准确率和端到端成功率的影响，论证链条完整。
- **定性案例分析直观**：通过具体示例展示了 DR、LR、DTDR-L 检索结果的差异，使方法优势更加可解释。
- **实验规模与消融较丰富**：覆盖多数据集、多模型规模、多种提示策略、多个超参数维度的消融，验证了方法的鲁棒性和适用边界。
- **实际应用导向明确**：着眼于端侧场景并考虑了提示长度、预填充延迟、缓存可行性等实际部署关键因素。

---

### 8. 不足与局限

- **分布外（OOD）泛化受限**：DTDR-C 对 OOD 任务性能下降明显，因为聚类和高阶马尔可夫建模需要足够的训练数据覆盖来可靠估计转移结构；
- **领域特定工具词汇的语义鸿沟**：当工具名称和描述高度专业化（如 HuggingFace 风格）时，预训练嵌入模型可能无法充分捕捉语义相似性，影响聚类效果；DTDR-L 可通过学习适应部分缓解；
- **强 OOD 依赖结构完全失效**：当工具名或依赖结构在训练中完全未出现时，所有基于检索的方法均会失效，需引入不确定性感知的降级机制（如马氏距离 OOD 检测）；
- **依赖专家级演示数据**：方法假设可获取正确的、专家级的演示轨迹，当数据含有错误或不完整标注时可能影响学习质量；
- **实验覆盖不充分之处**：
  - 未包含真实用户行为数据或生产中动态变化的工具集场景；
  - 端侧设备上的实际延迟和功耗评测缺失，仅以提示长度作为代理指标；
  - 未评估工具集合规模进一步扩大（数百/数千个）时的检索扩展性。
- **可复现性限制**：作者声明无法发布完整实现代码，仅提供伪代码，对精确复现实验结果有一定影响。

---

（完）
