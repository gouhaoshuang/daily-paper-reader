---
title: "KARMA: Leveraging Multi-Agent LLMs for Automated Knowledge Graph Enrichment"
title_zh: KARMA：利用多智能体LLM实现知识图谱自动化丰富
authors: "Yuxing Lu, Wei Wu, Xukai Zhao, Rui Peng, Jinzhuo Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=k0wyi4cOGy"
tags: ["query:eca"]
score: 7.0
evidence: "多智能体协作实现知识图谱丰富，匹配'协作'需求"
tldr: 知识图谱的维护需要大量人工，难以跟上科学文献增长。KARMA提出多智能体LLM框架，包含实体发现、关系抽取、模式对齐、冲突解决等九个协作智能体，迭代解析文档、验证知识并集成到现有图谱。在1200篇PubMed文章上的实验表明，KARMA能高效准确地丰富知识图谱，减轻人工负担。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-k0wyi4cogy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1164, \"height\": 291, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k0wyi4cogy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 839, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k0wyi4cogy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1177, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k0wyi4cogy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1389, \"height\": 469, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k0wyi4cogy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1391, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k0wyi4cogy/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1389, \"height\": 469, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-k0wyi4cogy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1465, \"height\": 731, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k0wyi4cogy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 682, \"label\": \"Table\"}]"
motivation: 知识图谱的人工维护无法规模化，亟需自动化丰富方法。
method: 构建九个协作智能体分别负责实体发现、关系抽取、模式对齐和冲突解决，迭代处理文本并验证知识。
result: 在三个领域的1200篇PubMed文章上验证了框架的有效性，显著提升知识图谱丰富效率。
conclusion: 多智能体LLM框架能有效自动化知识图谱丰富，降低人工成本。
---

## Abstract
Maintaining comprehensive and up-to-date knowledge graphs (KGs) is critical for modern AI systems, but manual curation struggles to scale with the rapid growth of scientific literature. This paper presents KARMA, a novel framework employing multi-agent large language models (LLMs) to automate KG enrichment through structured analysis of unstructured text. Our approach employs nine collaborative agents, spanning entity discovery, relation extraction, schema alignment, and conflict resolution that iteratively parse documents, verify extracted knowledge, and integrate it into existing graph structures while adhering to domain-specific schema. Experiments on 1,200 PubMed articles from three different domains demonstrate the effectiveness of KARMA in knowledge graph enrichment, with the identification of up to 38,230 new entities while achieving 83.1\% LLM-verified correctness and reducing conflict edges by 18.6\% through multi-layer assessments.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：知识图谱（KG）的维护（丰富）对现代AI系统至关重要，但人工策展难以跟上每年超过700万篇科学文献的爆炸式增长。传统自动方法在处理领域特定术语和上下文依赖关系时存在困难，且缺乏有效的模式对齐、一致性检查和冲突解决机制。
- **整体含义**：论文提出KARMA，一个基于多智能体大语言模型（LLM）的自动化KG丰富框架，通过结构化分析非结构化文本来扩展现有KG。核心在于利用多个专业智能体的协作，实现从文档解析到知识验证与集成的端到端流程，以提升知识图谱丰富的高效性、准确性和可扩展性。

### 2. 论文提出的方法论
- **核心思想**：将KG丰富任务分解为九个协同工作的LLM驱动智能体（Ingestion、Reader、Summarizer、Entity Extraction、Relationship Extraction、Schema Alignment、Conflict Resolution、Evaluator），每个智能体专注于子任务，并通过交叉验证和迭代处理确保输出质量。
- **关键技术细节**：
  - **Ingestion Agents**：文档获取和归一化，返回标准化文本和元数据。
  - **Reader Agents**：将文本分割成段落，并基于与当前KG的相关性评分（公式3），过滤低相关段落（阈值δ）。
  - **Summarizer Agents**：将高相关段落压缩为简洁摘要，保留关键实体和关系（公式4）。
  - **Entity Extraction Agents**：从摘要中识别实体（公式5），并通过嵌入空间距离（公式6）将提及的实体归一化到KG已有实体或标记为新实体（阈值ρ）。
  - **Relationship Extraction Agents**：对实体对进行关系分类（公式7），允许多标签预测（公式8），筛选出概率≥θr的关系。
  - **Schema Alignment Agents**：将新实体/关系映射到KG模式中的已有类型（公式9），若无法匹配则标记为候选添加。
  - **Conflict Resolution Agents**：检测新三元组与KG中已有三元组的逻辑冲突（公式10、11），通过LLM辩论判断是否矛盾，决定丢弃或人工审查。
  - **Evaluator Agents**：对每个三元组计算置信度（公式12）、清晰度（公式13）和相关性（公式14），通过加权平均得到最终得分，若均值≥Θ则集成（公式15）。
- **算法流程**：文档经Ingestion→Reader→Summarizer→Entity Extraction→Relationship Extraction→Schema Alignment→Conflict Resolution→Evaluator，最终将合格三元组加入KG。整个流程由中央控制器协调。

### 3. 实验设计
- **数据集**：从PubMed收集1200篇论文，分三个领域：基因组学（720篇）、蛋白质组学（360篇）、代谢组学（120篇）。所有论文以PDF格式输入。
- **基准（Baseline）**：对比了单智能体方法（Single-Agent，即所有三元组由单个LLM一次生成），以及使用三种不同LLM骨干（GLM-4、GPT-4o、DeepSeek-v3）的KARMA完整版本。
- **对比方法**：在三个领域上，KARMA vs. 单智能体；不同骨干之间的对比；以及消融实验（移除Summarizer、Conflict Resolution、Evaluator智能体）。
- **评估指标**：包含核心指标（平均置信度M_Con、平均清晰度M_Cla、平均相关性M_Rel）、图统计（覆盖增益ΔCov、连通性增益ΔCon）、质量指标（冲突率R_CR、LLM正确率R_LC、QA连贯性C_QA、人类评估得分R_HE）。所有LLM验证均使用DeepSeek-v3。

### 4. 资源与算力
- **说明**：论文未明确报告使用的具体GPU型号、数量或训练时长。实验通过LLM API（如GPT-4o、DeepSeek-v3、GLM-4）进行推理，未涉及模型训练。文中仅分析了提示令牌（prompt tokens）、完成令牌（completion tokens）和处理时间（图3），显示基因组学处理时间较长（平均96.58秒，std=46.90）。因此，无法给出具体算力细节。

### 5. 实验数量与充分性
- **实验数量**：主实验（表1）包含3个领域×4种配置（Single-Agent、GLM-4、GPT-4o、DeepSeek-v3）共12个实验组，每组报告9项指标。消融实验（表2）包含3个领域×4种配置（w/o Summarizer、w/o Conflict Resolution、w/o Evaluator、Full）共12组。此外还有成本分析（图3）和附录中的示例知识图谱。
- **充分性与客观性**：实验覆盖了三个不同生物医学领域，考虑了不同LLM骨干，并进行了系统的消融研究。评估指标多元化（包括人类评估和QA测试），减少单一指标偏差。单智能体基线提供了合理的下限。实验设计较为充分和客观，但缺乏跨领域迁移或更大规模数据集验证，且人类评估仅由两位专家进行，可能存在主观性。

### 6. 论文的主要结论与发现
- KARMA多智能体框架显著优于单智能体方法，在所有领域上均提升了知识图谱丰富效果。
- DeepSeek-v3骨干在实体覆盖增益（ΔCov）上表现最佳（基因组学中达38,230），且正确率（R_LC=83.1%）接近GPT-4o，体现了MoE架构在召回与精度间的平衡。
- GPT-4o在正确率方面领先（基因组学R_LC=88.0%），但连通性增益较低，可能未充分利用隐含关系。
- GLM-4在代谢组学清晰度和蛋白质组学QA连贯性上表现突出，展示了小参数模型在特定领域的适配能力。
- 消融实验表明，每个智能体都不可或缺：移除Summarizer导致噪声增加（准确率下降），移除Conflict Resolution降低一致性，移除Evaluator降低整体可用性。
- 多智能体架构通过交叉验证和冲突解决机制，将LLM验证正确率提升4.6%–14.4%，并将冲突边减少18.6%。

### 7. 优点
- **架构设计**：模块化多智能体架构，每个智能体任务明确，易于扩展和替换。通过交叉验证（如实体提取与关系抽取互检）、LLM辩论（冲突解决）等机制，有效缓解了单一LLM的幻觉和不一致问题。
- **领域适应性**：通过领域自适应的提示策略和模式对齐智能体，能够处理基因组学、蛋白质组学、代谢组学等专门术语，并在不同领域间展现不同优势。
- **评估完整性**：采用了多维度的评估体系（置信度、清晰度、相关性、图结构指标、LLM验证、QA测试、人类评估），从多个角度衡量知识质量，比单一指标更全面。
- **可解释性**：提供了附录中详细的智能体提示示例以及提取的三元组示例，便于理解系统行为。

### 8. 不足与局限
- **验证依赖LLM**：主要评价指标（R_LC、C_QA等）仍依赖LLM自身判断，可能存在循环验证的风险；人类评估仅两位专家，样本量小，不够严谨。论文承认需要领域专家在临床等高风险场景下进行最终验证。
- **领域覆盖有限**：仅在三个生物医学领域（基因组学、蛋白质组学、代谢组学）实验，未涉及其他科学或工业领域（如金融、法律）。领域间性能差异较大（代谢组学QA连贯性比基因组学低约12%），表明对稀疏关系建模仍有挑战。
- **计算成本未量化**：未报告GPU、训练时长等具体算力消耗，仅给出API调用层面的令牌数和时间，难以全面评估可扩展性。多智能体系统可能比单模型产生更高的计算开销。
- **缺乏开放架构**：未明确代码和数据是否完全公开（仅说明代码在补充材料中，接受后开源），可能影响可重复性。
- **未讨论所有偏差**：仅提及LLM可能引入的偏差，未深入分析PubMed数据源本身的出版偏差、领域覆盖偏差等对结果的影响。

（完）
