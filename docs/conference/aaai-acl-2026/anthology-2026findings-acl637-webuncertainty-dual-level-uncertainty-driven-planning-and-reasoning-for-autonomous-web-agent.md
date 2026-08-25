---
title: "WebUncertainty: Dual-Level Uncertainty Driven Planning and Reasoning For Autonomous Web Agent"
title_zh: WebUncertainty：面向自主Web智能体的双层不确定性规划与推理
authors: "Lingfeng Zhang, Yongan Sun, Jinpeng Hu, Hui Ma, Ying Yang, Kuien Liu, Zenglin Shi, Meng Wang"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.637.pdf"
tags: ["query:mobile-agent"]
score: 4.0
evidence: 面向自主Web智能体的不确定性规划方法，可迁移至移动智能体任务执行
tldr: 自主Web智能体在复杂动态网页中常因刚性规划策略和易幻觉推理而失败。论文提出WebUncertainty框架，采用任务不确定性驱动的自适应规划机制选择规划模式，并引入动作不确定性驱动的蒙特卡洛树搜索来改善推理。实验表明该方法在真实网页任务上提高了鲁棒性和任务完成率。虽然面向Web，其不确定性规划思想对移动智能体任务执行同样具有参考价值。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl637/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1642, \"height\": 859, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl637/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1654, \"height\": 855, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl637/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 754, \"height\": 559, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl637/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 810, \"height\": 764, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl637/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1660, \"height\": 637, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl637/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 811, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl637/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 812, \"height\": 347, \"label\": \"Table\"}]"
motivation: 自主Web智能体在处理动态交互和长程任务时受制于刚性规划与幻觉推理。
method: 提出WebUncertainty，包含任务不确定性自适应规划与动作不确定性MCTS推理机制。
result: 在真实网页任务上提升了鲁棒性和任务完成率。
conclusion: 为自主智能体提供双层不确定性处理框架，可借鉴到移动设备任务执行。
---

## Abstract
Recent advancements in large language models (LLMs) have empowered autonomous web agents to execute natural language instructions directly on real-world webpages. However, existing agents often struggle with complex tasks involving dynamic interactions and long-horizon execution due to rigid planning strategies and hallucination-prone reasoning. To address these limitations, we propose WebUncertainty, a novel autonomous agent framework designed to tackle dual-level uncertainty in planning and reasoning. Specifically, we design a Task Uncertainty-Driven Adaptive Planning Mechanism that adaptively selects planning modes to navigate unknown environments. Furthermore, we introduce an Action Uncertainty-Driven Monte Carlo tree search (MCTS) Reasoning Mechanism. This mechanism incorporates the Confidence-induced Action Uncertainty (ConActU) strategy to quantify both aleatoric uncertainty (AU) and epistemic uncertainty (EU), thereby optimizing the search process and guiding robust decision-making. Experimental results on the WebArena and WebVoyager benchmarks demonstrate that WebUncertainty achieves superior performance compared to state-of-the-art baselines.

---

## 论文详细总结（自动生成）

# WebUncertainty：面向自主Web智能体的双层不确定性规划与推理——论文总结


## 1. 核心问题与研究动机

- **研究背景**：大语言模型（LLM）的发展使自主Web智能体能够直接在真实网页上执行自然语言指令。然而，现有智能体在处理**动态交互**和**长周期执行（long-horizon）**的复杂任务时仍面临严峻挑战。
- **核心问题（双重不确定性）**：
  - **规划层不确定性**：复杂任务涉及动态网页交互，预规划的子目标难以适应未知环境。显式规划（一步到位分解任务）在网页状态变化时容易失效；而隐式规划（逐步反应式决策）则可能陷入局部最优。
  - **推理层不确定性**：长周期执行中，LLM的幻觉和“雪球效应”（错误逐步累积放大）导致动作高度易错。现有方法过度依赖LLM生成的动作，未考虑其不确定性；虽有研究通过logits引入token级不确定性，但忽略了动作的**语义层面**。
- **研究目标**：通过建模并处理规划与推理两个层面的不确定性，提升自主Web智能体在复杂动态网页任务中的鲁棒性和任务完成率。


## 2. 方法论：WebUncertainty框架

**整体框架**：将Web导航任务建模为部分可观测马尔可夫决策过程（POMDP），框架由两大核心组件构成。

### 2.1 任务不确定性驱动的自适应规划机制（Task Uncertainty-Driven Adaptive Planning）

- **任务不确定性分析**：在每个规划步骤前，一个**分析Agent（π_ana）** 基于全局指令I、当前网页观测O_t和执行历史H_t，判断剩余任务目标T_rem并量化任务不确定性u_plan ∈ [0,1]：
  - 公式：`T_rem, u_plan = π_ana(I, O_t, H_t)`
  - 高u_plan表示网页结构陌生、剩余任务复杂度高；低u_plan表示环境熟悉、任务简单。
- **自适应规划模式切换**：规划Agent根据阈值δ选择子目标生成策略：
  - **低不确定性（u_plan ≤ δ）**：激活**显式规划器**，一次性分解任务并执行序列中的第一个子目标，保证长周期一致性。
  - **高不确定性（u_plan > δ）**：切换至**隐式规划器**，直接预测当前最合适的即时子目标，灵活适应环境动态变化。
  - 随着执行推进，不确定性降低时可从隐式规划动态切回显式规划。

### 2.2 动作不确定性驱动的MCTS推理机制（Action Uncertainty-Driven MCTS Reasoning）

该模块采用蒙特卡洛树搜索（MCTS）进行执行决策，引入**ConActU（Confidence-induced Action Uncertainty）**策略量化不确定性，贯穿MCTS四个阶段：

- **选择（Selection）**：使用PUCT（Predictor-corrected Upper Confidence Bound）选择子节点，将动作置信度作为先验引导搜索：
  - `a_t = argmax_a [Q(s,a) + U(s,a)]`，其中`U(s,a) = w_puct · P_con(s,a) · √(Σ_b N(s,b)) / (1 + N(s,a))`
- **扩展（Expansion）**：推理Agent生成K个候选动作并输出置信度c = [c₁, c₂, …, c_K]：
  - 归一化为伪概率分布pᵢ = cᵢ / Σcⱼ；
  - 计算平均置信度作为总证据代理E = (1/K)Σcᵢ；
  - 计算归一化预测熵H_norm = −(1/log K)Σpᵢlog pᵢ；
  - **EU（认知不确定性）= 1 − E**：反映整体置信度不足导致的幻觉风险；
  - **AU（偶然不确定性）= H_norm · E**：反映模型具备知识（高E）但面临多个竞争性有效选项（高H_norm）时的固有歧义。
- **模拟（Simulation）**：评估Agent给出基础可行性得分S_base，根据得分和不确定性类型进行调制：
  - 成功（S_base ≥ τ）：接受动作，奖励R = S_base；
  - **高EU + 高AU（严格惩罚）**：状态混乱不可靠，R = −5，禁止搜索选择该路径；
  - **高EU + 低AU（宽松惩罚）**：缺乏领域知识（幻觉），R = −1，鼓励回溯探索父节点的兄弟节点；
  - **低EU + 高AU（正常）**：具备知识但存在随机歧义，R = S_base，鼓励在同一节点下探索不同候选动作；
  - **低EU + 低AU（重新生成）**：置信度高但执行得分低（确定性错误），R = 0，触发基于当前节点重新生成动作。
- **回传（Backpropagation）**：更新路径上所有祖先节点的访问次数和Q值：
  - `N(s,a) ← N(s,a) + 1`
  - `Q(s,a) ← Q(s,a) + (R − Q(s,a)) / N(s,a)`


## 3. 实验设计

### 3.1 数据集与基准（Benchmark）

- **WebArena**：主要模拟环境，包含812个任务，覆盖GitLab、Reddit等真实平台。采用基于可访问性树（accessibility tree）的纯文本设置。
- **WebVoyager**：真实网页环境，评估开放域鲁棒性。采用**129个精选任务**（覆盖13个不同环境，包括Amazon、Google Maps），剔除不稳定页面和开放式问题，聚焦确定性结果。

### 3.2 对比方法（Baselines）

| 方法 | 范式特点 |
|------|----------|
| Browser Use | 标准Web自动化基础基线 |
| Agent-E | 常规分层架构，用于对比任务不确定性驱动规划 |
| WebPilot | 基于MCTS的搜索方法，直接对比动作不确定性策略 |
| AgentOccam | 强调观测-动作对齐鲁棒性 |

### 3.3 实现细节

- 两个LLM骨干：**GPT-4-Turbo-2024-04-09**和**Qwen-Max-2025-01-25**，温度固定0.3；
- MCTS：每个子目标最大节点扩展数10，探索权重w_puct = 5；
- 评估指标：**成功率（Success Rate, SR）**。


## 4. 资源与算力

论文中**未明确说明**所使用的GPU型号、数量、训练时长或具体算力资源。仅提及使用两个商用LLM API（GPT-4-Turbo和Qwen-Max）作为骨干模型，并报告了推理时间（如WebVoyager上平均每个任务351.4秒），但未披露硬件配置和API调用成本细节。


## 5. 实验数量与充分性评估

**实验规模与类型**：
1. **主实验**：两个基准（WebArena 812任务、WebVoyager 129任务）× 两个LLM骨干 = **4组完整对比实验**；
2. **消融实验**：3个变体（去动作不确定性、纯显式规划、纯隐式规划）× 2个基准 = **6组消融对照**；
3. **性能-成本分析**：推理时间对比（6种方法）；
4. **敏感性分析**：对阈值δ（6组）和τ（6组）的系统扫描。

**充分性评价**：
- **优点**：实验覆盖全面——多个数据集、双骨干模型验证了架构泛化性；消融实验精准分离了两大核心组件的贡献；敏感性分析验证了超参数鲁棒性。
- **客观性与公平性**：对比方法代表不同技术范式（基础自动化、分层架构、MCTS搜索、观测对齐），基准选择合理；采用双骨干模型区分了架构贡献与模型能力。但**没有报告多次运行的方差/标准差**，也未提及统计显著性检验，结果的稳定性缺乏统计支撑。


## 6. 主要结论与发现

1. **整体性能领先**：WebUncertainty在WebArena上以GPT-4-Turbo达到**46.9% SR**（超过AgentOccam 43.1%、WebPilot 37.6%）；在WebVoyager上达到**65.9% SR**（超过AgentOccam 64.3%）。
2. **弱骨干模型可弥补能力差距**：使用Qwen-Max的WebUncertainty达到63.6%（WebVoyager）和40.1%（WebArena），**超越了使用GPT-4-Turbo的WebPilot**，说明不确定性管理比原始推理能力更关键。
3. **领域适应性**：在Reddit（高歧义、高交互复杂度）上表现最优（67.0%），验证了AU量化促使更好探索；在GitLab（长周期工作流）上超越搜索基线（40.0% vs. 33.3%），验证了自适应规划的有效性。
4. **动作不确定性建模是最大贡献点**：去除ConActU策略导致WebVoyager上SR下降9.3%、WebArena上下降3.4%，为所有消融中最显著的退化。
5. **效率优势**：相比WebPilot，推理时间减少**56%以上**（351.4s vs. 803.7s）且SR更高，证明了不确定性引导的MCTS显著优于盲目搜索。


## 7. 方法亮点

- **概念创新**：明确区分规划层和推理层的**双层不确定性**，分别建模并设计针对性解决方案，角度新颖且实用。
- **不确定性语义化**：ConActU策略将不确定性从token级提升到**动作语义级**，用AU和EU解耦两种性质不同的不确定性来源（知识缺失 vs. 固有歧义），为MCTS提供了精细化的搜索引导。
- **不确定性驱动的惩罚策略**：四种EU/AU组合对应四种差异化的反馈调制机制（严格/宽松惩罚、保留/零奖励），并非简单加减惩罚，逻辑清晰且有可解释性。
- **自适应规划模式切换**：用不确定性作为显式/隐式规划的切换信号，兼顾全局一致性与局部灵活性，规避了单一模式的固有缺陷。
- **成本可控**：通过不确定性感知剪枝大幅降低搜索开销，解决了MCTS类方法推理成本高企的痼疾。
- **双骨干验证**：在不同能力等级的LLM上均验证了有效性，增强了架构泛化性的说服力。


## 8. 不足与局限

- **计算开销**：虽然比WebPilot减少56%推理时间，但MCTS多候选生成的整体推理成本仍远高于非搜索方法（351.4s vs. Agent-E的224.7s），难以部署于实时或低成本场景。
- **纯文本感知限制**：依赖可访问性树（DOM），对视觉密集型网站（依赖空间布局、颜色编码等传递关键信息的网页）处理能力存疑，未涉及多模态感知。
- **超参数敏感性**：依赖经验阈值δ和τ，虽有敏感性分析支撑鲁棒性，但在高度动态变化的环境中固定阈值可能导致次优的模式切换。
- **实验覆盖不足**：WebVoyager只用了129个精选任务子集（原始数据集含492个任务），且排除了开放式问答任务；缺乏多模态视觉输入的评估；未报告实验结果方差和统计显著性。
- **可复现性问题**：使用商用非开源API模型（GPT-4-Turbo、Qwen-Max）且未披露温度以外的详细采样参数和随机种子管理方式，复现存在一定难度。
- **伦理与部署风险**：论文承认LLM固有的偏见传播和幻觉动作风险，在关键真实应用中需人工监督回路，尚不适合完全自主部署。

---

（完）
