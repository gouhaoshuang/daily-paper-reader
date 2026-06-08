---
title: "OWL: Optimized Workforce Learning for General Multi-Agent Assistance in Real-World Task Automation"
title_zh: OWL：面向通用多智能体实时任务自动化的优化工作流学习
authors: "Mengkang Hu, Yuhang Zhou, Wendong Fan, Yuzhou Nie, Ziyu Ye, Bowei Xia, Tao Sun, Zhaoxuan Jin, Yingru Li, Zeyu Zhang, Yifeng Wang, Qianshuo Ye, Bernard Ghanem, Ping Luo, Guohao Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=MBJ46gd1CT"
tags: ["query:eca"]
score: 7.0
evidence: 层次化多智能体模块化协作框架
tldr: 现有LLM多智能体系统因领域特异性而难以跨域迁移。本文提出Workforce层次化框架，将策略规划与专业执行解耦，包含领域无关的规划器、协调器和领域专用工人。实验表明该框架在多个真实世界任务中实现零样本迁移，显著降低了跨域部署成本。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-mbj46gd1ct/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1352, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mbj46gd1ct/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1425, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mbj46gd1ct/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 501, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mbj46gd1ct/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1435, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mbj46gd1ct/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1352, \"height\": 719, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mbj46gd1ct/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1396, \"height\": 834, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1496, \"height\": 1079, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 931, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1404, \"height\": 374, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1435, \"height\": 601, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1388, \"height\": 672, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1505, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1448, \"height\": 738, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1018, \"height\": 705, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1158, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mbj46gd1ct/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1382, \"height\": 310, \"label\": \"Table\"}]"
motivation: 当前多智能体系统跨域应用需要完整架构重设计和高成本重训练。
method: 提出层次化框架，解耦规划与执行，支持模块化跨域复用。
result: 在多个领域实现零样本迁移，保持高性能。
conclusion: 解耦设计是实现通用多智能体助手的关键。
---

## Abstract
Large Language Model (LLM)-based multi-agent systems show promise for automating real-world tasks but struggle to transfer across domains due to their domain-specific nature.
Current approaches face two critical shortcomings: they require complete architectural redesign and full retraining of all components when applied to new domains.
We introduce **Workforce**, a hierarchical multi-agent framework that decouples strategic planning from specialized execution through a modular architecture comprising:
*(i)* a *domain-agnostic* **Planner** for task decomposition,
*(ii)* a **Coordinator** for subtask management, and
*(iii)* specialized **Workers** with *domain-specific* tool-calling capabilities.
This decoupling enables cross-domain transferability during both inference and training phases:
During inference, Workforce seamlessly adapts to new domains by adding or modifying worker agents;
For training, we introduce **Optimized Workforce Learning (OWL)**, which improves generalization across domains by optimizing a domain-agnostic planner with reinforcement learning from real-world feedback.
To validate our approach, we evaluate Workforce on the GAIA benchmark, covering various realistic, multi-domain agentic tasks.
Experimental results demonstrate Workforce achieves open-source state-of-the-art performance (**69.70%**), outperforming commercial systems like OpenAI's Deep Research by **2.34%**.
More notably, our OWL-trained 32B model achieves **52.73%** accuracy (**+16.37%**) and demonstrates performance comparable to GPT-4o on challenging tasks.
To summarize, by enabling scalable generalization and modular domain transfer, our work establishes a foundation for the next generation of general-purpose AI assistants.

*Our code is available at [Anonymous URL](https://anonymous.4open.science/r/annonymous-owl/), and our data is available at [Anonymous URL](https://huggingface.co/anonymous21016).*

---

## 论文详细总结（自动生成）

### 论文总结：OWL: Optimized Workforce Learning

#### 1. 核心问题与整体含义（研究动机和背景）
- **问题**：现有基于大语言模型（LLM）的多智能体系统（MAS）在跨领域迁移时面临严重障碍：需要完整的架构重新设计和所有组件的完全重训练，导致灵活性差、成本高。
- **背景**：尽管MAS在复杂任务中表现优异（如MetaGPT、CAMEL等），但它们的领域特异性限制了通用性。例如，MetaGPT专门用于软件工程，无法直接扩展到其他领域。现有训练方法（如MALT）需要优化每个智能体，迁移时需重训整个系统。
- **目标**：提出一种可跨领域迁移的通用模块化多智能体架构，实现“即插即用”的领域适应，同时降低训练成本。

#### 2. 方法论：核心思想、关键技术细节
- **核心架构 — Workforce**：层次化多智能体框架，将**策略规划**与**领域执行**解耦。
  - **Planner（规划器）**：领域无关，负责将高层任务分解为子任务列表。
  - **Coordinator（协调器）**：管理子任务分配，根据工人能力注册表指派任务，并整合中间结果。
  - **Worker Nodes（工人节点）**：领域专用，每个工人配有专用工具集（如Web Agent、文档处理Agent、推理/编码Agent），执行子任务并返回结果。
  - **通信机制**：通过共享任务通道（Task Channel）进行，工人仅访问当前子任务和前置结果，避免直接agent间消息传递，提升可扩展性。
  - **重规划机制**：工人失败时，将失败信息发布到通道，规划器收到反馈后生成新的子任务，实现测试时自我纠正。
- **训练方法 — OWL（Optimized Workforce Learning）**：仅优化领域无关的规划器，实现高效跨域迁移。
  - **两阶段训练**：
    1. **监督微调（SFT）**：使用Workforce + GPT-4o-mini合成的专家轨迹初始化规划器。轨迹来自四个数据集（HotpotQA、WikiTableQuestions、Math-related、Infinity-MM），经过过滤（准确率/余弦相似度/LLM评判）。
    2. **强化学习（DPO）**：利用SFT初始化模型生成4条轨迹，根据正确性构建偏好对，进行直接偏好优化（DPO），进一步提升泛化能力。
  - **训练数据统计**：共收集3466条轨迹，过滤后SFT用1599条，DPO用1009对。每个轨迹平均3.41个子任务、22.75步。

#### 3. 实验设计
- **基准**：GAIA验证集（通用AI助手基准），包含三个难度级别（Level 1/2/3），涉及多模态推理、代码执行、实时网络搜索等。
- **对比方法**：
  - **专有框架**：OpenAI Deep Research（o3）、h2oGPTe Agent、Trase Agent v0.3、Langfun Agent v2.1等。
  - **开源框架**：Open Deep Research、Magnetic-One、AutoAgent、TapeAgents、Single Agent、Role Playing（CAMEL）等。
  - **基线控制**：单智能体和角色扮演使用与Workforce相同的工具集，确保公平对比。
- **评价指标**：准确率（accuracy %），采用pass@3（GPT-4o）或pass@1（Claude-3.7-sonnet）采样。阻止了GAIA答案泄露网站。

#### 4. 资源与算力
- **训练配置**：8块NVIDIA H100 GPU，使用LlamaFactory框架，bfloat16混合精度，学习率1e-5，有效batch size=12（每设备1×梯度累积12），训练2个epoch。**未明确说明训练总时长**。
- **推理**：通过API访问模型，无需GPU；使用贪心解码，默认重规划阈值2次。

#### 5. 实验数量与充分性
- **主实验**：表1对比了14个基线（含专有和开源），显著表明Workforce-Claude（69.70%）超越所有开源方法和Deep Research（67.36%）。
- **OWL训练实验**：表3对比了不同规划器（GPT-4o-mini、Qwen2.5-72B、Claude-3.7-sonnet等），证明32B模型经OWL后提升16.37%，达52.73%。
- **消融实验**：
  - 轨迹过滤效果（图2a）：过滤后性能显著提升。
  - 规划器 vs. 工人训练（图4c）：只训练规划器（45.45%）远优于只训练工人（31.51%），与两者都训练（46.68%）接近。
  - 重规划次数影响（图3b）：随重规划次数增加，性能提升（测试时扩展）。
- **鲁棒性分析**（图4b、表9）：Workforce在多能力要求任务中保持稳定（标准差3.05），而角色扮演下降严重（标准差11.39）。
- **错误分析**（表7、表8）：手动分类了52个错误案例，规划器错误占21.15%，工具限制占32.69%。
- **统计显著性检验**（附录H）：Wilcoxon符号秩检验p值均<0.05，证明改进显著。
- **充分性**：实验覆盖了性能对比、训练策略、模块贡献、鲁棒性、错误模式等，设计合理、对比公平（控制基础模型和工具集），结论可信。

#### 6. 主要结论与发现
- **Workforce**达到开源SOTA（69.70%），首次超过OpenAI Deep Research（2.34%），并刷新Level 1最佳成绩。
- **OWL训练**使32B模型（Qwen2.5-32B-Instruct）性能提升16.37%，与GPT-4o在Level 3任务上相当，超越GPT-4o-mini和Qwen2.5-72B。
- 解耦设计的关键性：只训练规划器即可获得大部分收益，验证了“稳定核心、可变外围”设计的有效性。
- 错误模式：规划器错误和工具限制是主要失败原因，提示未来改进方向。
- 重规划机制实现了测试时自我纠正，使性能随尝试次数递增。
- OWL训练在所有能力类型（网页浏览、多模态、推理、编码）上均带来一致提升。

#### 7. 优点
- **模块化与可迁移性**：架构解耦规划与执行，新增领域仅需更换工人节点，无需重训整个系统，显著降低部署成本。
- **高效训练**：只优化规划器，大幅节省算力（相比全系统训练），且效果卓越。
- **开源SOTA性能**：超过所有已知开源框架，甚至超越部分商业系统（如Deep Research）。
- **全面开源**：代码、模型、数据全部公开，促进可复现研究和社区发展。
- **详实的分析**：提供了错误分类、鲁棒性、测试时扩展等多视角分析，深入理解系统行为。

#### 8. 不足与局限
- **工具依赖性**：性能受限于领域专用工具的质量与可用性，在缺乏可靠工具包的领域可能出现执行瓶颈。
- **延迟问题**：从真实世界反馈中进行强化学习时，在线搜索等工具调用会引入延迟，影响训练效率。
- **基础模型限制**：19.23%的错误源于模型自身能力不足（如上下文长度限制、幻觉、编码能力弱），随基础模型进步可能自然缓解。
- **数据污染风险**：GAIA基准可能存在答案泄露（尽管已阻止部分网站），需持续监控。
- **实验范围**：仅在GAIA上评估，虽然涵盖多领域，但未在更多真实场景（如企业级工作流）测试泛化性。
- **重规划机制依赖工人自评**：工人可能误判失败，引入噪声；且重规划次数增加推理成本。

（完）
