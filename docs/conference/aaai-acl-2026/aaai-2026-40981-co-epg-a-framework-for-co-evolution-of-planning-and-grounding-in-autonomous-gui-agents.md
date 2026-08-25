---
title: "Co-EPG: A Framework for Co-Evolution of Planning and Grounding in Autonomous GUI Agents"
title_zh: Co-EPG：自主GUI智能体中规划与接地协同演化的框架
authors: "Yuan Zhao, Hualei Zhu, Tingyu Jiang, Shen Li, Xiaohang Xu, Hao Henry Wang"
date: 2026-03-17
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/40981/44942"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 用于训练自主GUI智能体的规划与接地协同演化框架，是移动智能体的核心技术
tldr: 针对现有GUI智能体忽视规划与接地能力的协同、且过度依赖合成数据的问题，提出Co-EPG自迭代训练框架。该框架通过基于接地奖励的组相对策略优化（GRPO）形成正反馈循环，让规划模型在接地模型引导下探索更优策略，并更充分利用已有数据。实验表明该方法能有效提升GUI智能体的规划与接地能力。它为移动端自主智能体的构建提供了可复用的训练范式。
source: AAAI-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1831, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 777, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 850, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 728, \"height\": 549, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 687, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 684, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40981/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 774, \"height\": 508, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40981/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1820, \"height\": 670, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40981/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 811, \"height\": 729, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40981/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 499, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40981/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 638, \"height\": 244, \"label\": \"Table\"}]"
motivation: GUI智能体规划与接地能力缺乏协同训练，且对合成数据利用不足。
method: 提出Co-EPG自迭代框架，利用GRPO与接地奖励形成规划与接地的协同演化正反馈循环。
result: 显著提升GUI智能体的规划质量和动作接地准确率。
conclusion: 为包括移动端在内的自主GUI智能体提供了高效的协同训练方法。
---

## Abstract
Graphical User Interface (GUI) task automation constitutes a critical frontier in artificial intelligence research. While effective GUI agents synergistically integrate planning and grounding capabilities, current methodologies exhibit two fundamental limitations: (1) insufficient exploitation of cross-model synergies, and (2) over-reliance on synthetic data generation without sufficient utilization. To address these challenges, we propose Co-EPG, a self-iterative training framework for Co-Evolution of Planning and Grounding. Co-EPG establishes an iterative positive feedback loop: through this loop, the planning model explores superior strategies under grounding-based reward guidance via Group Relative Policy Optimization (GRPO), generating diverse data to optimize the grounding model. Concurrently, the optimized Grounding model provides more effective rewards for subsequent GRPO training of the planning model, fostering continuous improvement. Co-EPG thus enables iterative enhancement of agent capabilities through self-play optimization and training data distillation. On the Multimodal-Mind2Web and AndroidControl benchmarks, our framework outperforms existing state-of-the-art methods after just three iterations without requiring external data. The agent consistently improves with each iteration, demonstrating robust self-enhancement capabilities. This work establishes a novel training paradigm for GUI agents, shifting from isolated optimization to an integrated, self-driven co-evolution approach.

---

## 论文详细总结（自动生成）

好的，我将严格按照要求，基于提供的论文文本，生成一份详细的中文总结。

---

## Co-EPG 论文深度解析与总结

### 1. 核心问题与研究背景（动机）

- **核心问题**：当前 GUI（图形用户界面）智能体在架构和训练方法上存在两大根本性缺陷：
    1. **跨模型协同不足**：成熟的 GUI 智能体通常需要将 "规划"（决定做什么）和 "接地"（决定点哪里）两种能力进行解耦。然而，现有的模块化设计大多对规划模型和接地模型进行**孤立的、独立的优化**，忽视了二者在功能上的强互补性与潜在协同演化可能。
    2. **合成数据过度依赖**：许多 SOTA 方法为了提升性能，严重依赖大规模、高成本的合成数据生成，这种模式不仅效率低下，而且可能引入噪声，同时**未能充分挖掘和利用已有的标注数据**。
- **研究动机**：鉴于上述瓶颈，本文旨在探索一个全新的协同范式——通过构建一种自我迭代的正反馈循环，使规划模型与接地模型在训练过程中能够相互促进、协同进化，从而在不依赖外部数据的情况下，最大化利用现有数据价值，持续提升智能体的整体能力。

### 2. 方法论：Co-EPG 框架

- **总体架构（P-G 双模型）**：
    - 采用解耦的 "规划器 (Planner, π) + 接地器 (Grounding model, φ)" 架构。
    - **规划模型 (π)**：作为高层策略器，根据当前观测（截图、HTML）、任务描述和历史交互，生成包含语义文本计划（Plan）、动作类型（Type）和动作值（Value）的复合决策。
    - **接地模型 (φ)**：利用规划模型生成的具体计划作为文本提示（Prompt），结合视觉截图，精确定位目标元素的坐标（Coordinate）。
- **核心机制——协同演化循环**：框架的核心是建立两个模型间的**正反馈闭环**，该循环由两大步骤迭代构成（本文进行了 3 轮迭代）：
    1.  **迭代训练（Iterative Training）**：
        - 首先，用当前迭代的数据集 `Dk` 对规划模型和接地模型进行基础的 SFT 微调。
        - 接着，**利用 C-DREM 机制引导规划模型进行 GRPO 强化学习训练**。接地模型在此处充当"裁判"，其预测坐标的准确性被转化为奖励信号，以引导规划模型探索更高效、语义更清晰、更易于被接地模型理解和执行的策略。
        - 同时，经过优化的规划模型在后续的数据增强中产出更高质量的轨迹数据，用于进一步微调接地模型，从而提升其感知和定位能力。这就形成"规划指导接地，接地反馈规划"的循环。
    2.  **数据增强（Data Enhancement）**：
        - 构建一个"自我进化"的数据集生成管道。初始（k=0）时，由开源的 Planner 和 Verifier 模型生成并验证初始数据集。
        - 在后续迭代（k≥1）中，将最新的规划模型和接地模型纳入数据生产池。规划模型用于增加数据的多样性，接地模型则用于提升数据筛选（验证）的可靠性。
        - 通过这种机制，每一轮迭代生成的数据质量（纯度）和多样性都得到提升，从而为下一轮的模型训练提供更优质的"燃料"。
- **关键技术细节——C-DREM（基于置信度的动态奖励集成机制）**：
    - **背景**：单一接地模型作为奖励模型存在固有偏见且 OOD（分布外）表现不佳，导致奖励信号噪声大。
    - **核心思想**：集成多个接地模型（包括当前训练的 φk 和开源 VLM 模型）的反馈，并**动态赋予权重**。
    - **公式与逻辑**：
        - 总奖励 `r_plan` 是各模型奖励 `Acc_plan_j` 的加权和。
        - 权重 `wj` 由**静态先验（σj）** 和**动态置信度（cj）** 共同决定。静态先验对自家训练的模型给予更高重视度；动态置信度则基于模型预测坐标的 Token 对数似然（log-likelihood）归一化后得出，可以反映模型在当前输入上的"底气"。这确保了高置信度的模型在集成中获得更高的发言权。
    - **奖励构成**：最终奖励由三部分构成：`r_plan`（坐标是否落在目标框内）、`r_type`（动作类型是否完全匹配）、`r_value`（动作值的 F1 分数是否达标）。最终奖励为三元组的综合判定，并通过 GRPO 的组内归一化计算 Advantage。

### 3. 实验设计

- **基准数据集**：
    - **Multimodal-Mind2Web**：用于评估网页交互任务（跨任务、跨网站、跨领域三个子任务）。
    - **AndroidControl**：用于评估移动端应用操作任务（高层级和低层级任务）。
- **对比方法（SOTA）**：
    - **网页端**：对比了基于 GPT-4/4o 的各种提示方法（如 SoM, SeeClick）、以及专门训练的模型（如 Explorer-4B/7B, AgentTrek-7B, AGUVIS-7B, SeeClick-9.6B）。
    - **移动端**：对比了 OS-Atlas-4B/7B, UI-TARS-2B/7B, InfiGUI-R1-3B, GUI-R1 等前沿模型。
- **评价指标**：网页端关注元素准确率（Ele.Acc）、操作F1（Op.F1）和步骤成功率（Step SR）；移动端关注步骤准确率（Step Acc）。
- **核心结果**：
    - **Co-EPG-Web-7B** 在 Multimodal-Mind2Web 上平均 Step SR 达 **58.4%**，超越前 SOTA 模型 AGUVIS-7B（57.2%）和 Explorer-7B（54.3%）。
    - **Co-EPG-Mob-7B** 在 AndroidControl 上平均 Step Acc 达 **83.1%**，超越前 SOTA 模型 UI-TARS-7B（81.7%）。
    - 同时，3B 小参数版本的 Co-EPG 也能在各自基准上优于或媲美同量级或更大量级的 SOTA 模型，展现了显著的跨规模泛化能力。

### 4. 资源与算力

- **文中明确提及的硬件环境**：Linux 服务器，配备 984GB RAM，Intel Xeon Platinum 8369B CPU @ 2.90GHz，以及 Nvidia A100 Tensor Core 80GB GPU。
- **需要指出的是**：论文正文中**并未明确说明**具体使用了多少块 A100 GPU、精确的训练时长、以及在训练/推理阶段的具体算力开销。这些详细信息可能存放于论文的附录或补充材料中。不过，从模型参数规模（7B/3B）和使用的框架（MS-SWIFT）可以推测，其资源需求主要取决于微调和 GRPO 迭代轮次。

### 5. 实验数量与充分性

- **实验组涵盖面广**：
    - **主实验**：在两个主流 benchmark（网页+移动）上进行了全面的基准对比，实验规模充足。
    - **消融实验（Ablation）**：涵盖了三个核心设计点的验证，包括：
        - P-G 双模型 vs. 端到端模型（证明解耦架构有效性）。
        - 迭代演化 vs. 纯 SFT、w/o GRPO（证明 RL 与数据迭代的双驱动作用）。
        - C-DREM 机制的多组消融（w/o C-DREM, w/o Confidence & Prior Weights, w/o Confidence Weights），系统地剥离了各子组件的贡献。
    - **效率实验（Efficiency）**：包含数据效率（只用 2.42% 的 AGUVIS 数据量达到更优性能）和 C-DREM 训练效率的对比分析。
    - **质量分析（Analysis）**：对迭代过程中数据集纯度（+8.84%）和多样性（增加近4）的变化进行了量化；评估了模型在跨任务/跨网站/跨领域上的逐步提升。
    - **案例研究（Case Study）**：通过可视化案例直观展示了从 M1 到 M3 规划器从语义模糊到精准、接地器定位从错到对的具体改进过程。
- **充分性与客观性评价**：实验设计**较为充分且逻辑严谨**。
    - 优势：消融实验完整，不仅证明了组件有效，还通过"w/o Confidence & Prior Weights"到"w/o Confidence Weights"再到完整的 C-DREM 的渐进对比，清晰揭示了各部件（静态权重 vs. 动态置信度）的贡献增量。
    - 潜在局限：实验主基座仅使用了 Qwen2.5-VL，虽然保证了对比的公平性，但未在更多不同架构的基座模型（如 Llama， Qwen2）上验证框架的普适性，这是未来可以增强的一环。

### 6. 主要结论与发现

- **协同进化有效**：规划与接地模型之间通过奖励信号和高质量数据进行闭环协同训练，能够实现相互增强。
- **自迭代提升显著**：智能体性能（Step SR）在每一轮迭代中均呈现稳定且持续的增长，验证了框架具备很强的自增强能力。
- **打破数据依赖**：通过深度挖掘内部数据价值，Co-EPG 只用极少的标注数据（约为 SOTA 模型的 1/40）就达到并超越了依赖大规模合成数据的模型的性能，是一种极具潜力的数据高效型训练范式。
- **强化学习是关键加速器**：仅靠数据迭代（SFT）虽能带来性能提升，但 GRPO 协同训练在提供探索性奖励、突破纯数据驱动的性能瓶颈方面扮演着至关重要的"加速器"角色。
- **C-DREM 的优越性**：动态、多模型的奖励集成机制能有效降噪，显著提升强化学习训练的稳定性和收敛速度。

### 7. 方法亮点

- **首创的协同训练新范式**：将 RL（GRPO）不仅仅用于端到端策略学习，而是作为一种"桥梁"连接并协同优化解耦的双模型架构。规划器通过 RL 学会了"如何产出更好的自然语言指令"，从而让接地器更容易理解，这是很有洞察力的设计。
- **高可用的 C-DREM 机制**：通过“静态先验”+“动态置信度”的加权方式，自适应地聚合多个奖励源，有效缓解了单一奖励模型的噪声和认知盲区问题。该机制设计巧妙且具有普适性，可以作为通用强化学习奖励建模的参考。
- **极致的**数据利用策略**：完全依赖 benchmark 自带数据进行自迭代优化，不引入任何外部合成数据，不仅展示了框架的实用价值，也为低资源场景下的智能体训练提供了新的思路。
- **强大的溯源分享精神**：实验细节考虑周到，如将 3B 与 4B 模型对比，更清晰地展示了方法在参数效率上的优势。

### 8. 不足与局限

- **基座模型单一**：实验仅在 Qwen2.5-VL 基座模型上验证，缺乏在 GPT-OV、其他开源 VLM 等更多样化基座上的迁移性和鲁棒性验证。
- **基准覆盖有限**：尽管涉及网页和移动端，但真实世界的 GUI 环境还包括桌面应用（Windows）、游戏 UI 等更为复杂多变的场景，论文尚未覆盖。
- **计算成本未透明**：虽然数据量少，但 GRPO 需要多轮采样（Rollouts），其总训练所需的 GPU 资源和时间成本未被明确量化，这对于资源受限的研究团队是一个需要考虑的重要因素。
- **奖励机制仍有偏置风险**：C-DREM 虽然优于单一模型，但最终的坐标匹配（`Acc_plan`）本身就是一种启发式规则，在复杂交互（如拖拽、悬浮）或模糊定位场景下的准确性仍有待探究。
- **"Value"奖励的简化**：对于动作值（如输入的文本），仅以 F1 分数超过 0.5 作为一个二值化奖励，可能丢失部分关键的细粒度语义信息。

（完）
