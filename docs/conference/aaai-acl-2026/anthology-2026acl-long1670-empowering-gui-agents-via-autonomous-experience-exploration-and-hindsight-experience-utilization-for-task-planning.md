---
title: Empowering GUI Agents via Autonomous Experience Exploration and Hindsight Experience Utilization for Task Planning
title_zh: 通过自主经验探索与事后经验利用增强GUI智能体的任务规划能力
authors: "Tianyi Men, Zhuoran Jin, Pengfei Cao (鹏飞 曹), Yubo Chen, Kang Liu, Jun Zhao"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.1670.pdf"
tags: ["query:mobile-agent"]
score: 7.0
evidence: GUI智能体通过自主经验探索与事后经验利用进行任务规划
tldr: 提出PEEU方法，让小型开源多模态语言模型通过自主环境探索收集经验，并利用事后经验合成严格对齐的高层规划数据，从而提升GUI智能体在任务分解与跨站点泛化上的能力。该方法缓解了小型模型规划能力弱的问题，为移动设备上部署轻量级GUI智能体提供了可行的训练途径。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 795, \"height\": 730, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1655, \"height\": 1069, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1650, \"height\": 892, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1657, \"height\": 740, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 803, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1645, \"height\": 794, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1670/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1645, \"height\": 1947, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1670/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1644, \"height\": 1307, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1670/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1648, \"height\": 979, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1670/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 790, \"height\": 647, \"label\": \"Table\"}]"
motivation: 小型开源MLLM相比商业大模型更具成本效益和隐私优势，但任务规划能力弱且跨站泛化有限。
method: 提出规划经验探索与利用(PEEU)方法，自主探索环境并利用事后经验合成对齐的高层训练数据。
result: 在任务规划性能与跨网站泛化能力上显著提升，并进行了定量泛化行为分析。
conclusion: 为资源受限场景下构建GUI智能体提供了经验驱动的训练范式。
---

## Abstract
Multimodal web agents can assist humans in operating repetitive GUI tasks, where effective task planning is essential for decomposing complex tasks into executable actions. While small open-source MLLMs are cost-efficient and privacy-preserving compared with commercial large models, they suffer from weak planning and limited cross-website generalization. To address these limitations, we introduce the planning experience exploration and utilization (PEEU) method, which autonomously explores environments to discover experiences and utilizes hindsight experience to synthesize strictly aligned, high-level training data. To quantitatively analyze the generalization behaviors driving this performance, we propose the task decomposition hierarchical analysis framework (TDHAF) to systematically study compositional generalization across three task granularities: low, middle and high levels. Our analysis reveals that mastering low-level atomic skills does not guarantee high-level planning competence, while high-level task training yields stronger OOD generalization. Experiments on real-world benchmarks demonstrate PEEU’s superior effectiveness: our 7B model achieves 30.6% accuracy, outperforming the much larger Qwen2.5-VL-32B model. These demonstrate constructing hindsight high-level tasks and leveraging experiences is crucial for OOD planning abilities of small MLLMs.

---

## 论文详细总结（自动生成）

# 论文详细总结：Empowering GUI Agents via Autonomous Experience Exploration and Hindsight Experience Utilization for Task Planning

## 1. 核心问题与整体含义（研究动机与背景）

- **研究对象**：多模态网页代理（Multimodal Web Agent），其核心能力是**任务规划**——将复杂的 GUI 任务分解为可执行的原子动作序列。
- **核心矛盾**：商业大模型（如 GPT-4o、Claude）性能强但交互成本高、存在隐私风险；小型开源 MLLM（如 Qwen2.5-VL-3B/7B）成本低、可私有化部署，但**规划能力弱、跨网站泛化能力有限**。
- **现有方法的不足**：
  - **原子级任务训练**（如 Click、Type、Scroll）：无法保证对高层复杂任务的组合泛化能力，缺乏系统性验证框架。
  - **粗粒度高层任务训练**：直接使用探索轨迹训练，但轨迹与任务之间存在**不对齐**（misalignment）问题，且缺少对未知环境的**严格约束**（如任务要求 4.5 星，轨迹实际只达到 3 星）。
- **论文提出的解决思路**：受人类"从交互探索中积累经验、用事后反思指导未来"的学习方式启发，让智能体**自主探索环境**并利用**事后经验（hindsight experience）** 合成高质量、严格对齐的高层训练数据，从而提升小型 MLLM 的任务规划与 OOD 泛化能力。

## 2. 方法论

### 2.1 核心思想

提出 **PEEU（Planning Experience Exploration and Utilization）** 方法，包含两个阶段：
1. **规划树探索（Planning Tree Exploration）**：智能体自主设定探索目标，在陌生网站中进行目标驱动的探索，构建探索树。
2. **规划经验利用（Planning Experience Utilization）**：从探索轨迹中提取经验，利用事后视角将轨迹逆向对齐为**更严格约束、更准确对齐**的高层任务，用于训练模型。

### 2.2 PEEU 关键流程细节

- **（公式层面，用文字说明）**：
  - **任务列表生成**：给定网站 URL，探索模型 M 根据首页状态 s₀ 生成任务列表 D = M(s₀, URL)。
  - **探索树构建**：R = Explore(M, D, Env, URL)，记录所有探索轨迹 τ = {(s₀, a₀), …, (sₘ, aₘ)}。
  - **原子经验提取**：对每一步动作，比较动作前后观测状态，提取原子经验 ϵₜ = M(sₜ, aₜ, sₜ₊₁)。
  - **轨迹级经验聚合**：将原子经验序列 μ = (ϵ₁, …, ϵ_T) 经 GPT-4o 聚合为 PEEU 高层任务 d̃ = Φ(μ)。
  - **策略学习**：以 SFT 和 GRPO 训练策略 π : S × H × D̃ → A。
  - **GRPO 奖励设计**：格式奖励 r_format + 答案正确性奖励 r_answer，总奖励最高 2.0。
- **关键技术优势**：将"任务去匹配轨迹"的暴力搜索，转换为"轨迹反推任务"的事后对齐，解决了轨迹-任务不对齐和约束不足两个核心问题。

### 2.3 TDHAF 分析框架

提出 **TDHAF（Task Decomposition Hierarchical Analysis Framework）**，系统分析组合泛化能力：
- **三个任务粒度**：低层（原子单步操作）、中层（多步子任务）、高层（长程复杂任务）。
- **两种泛化类型**：域内（ID）与域外（OOD）。
- **三个分析维度**：
  - **ID 自下而上泛化**：低层训练能否泛化到高层任务；
  - **ID 自上而下泛化**：高层训练能否泛化到低层任务；
  - **OOD 多层级泛化**：哪种粒度的训练最有利于跨网站泛化。
- **评估指标**：Id（元素编号准确率）、Action（动作类型准确率）、Value（动作参数准确率）、Step SR（单步完全匹配准确率）以及**覆盖率**（三次粒度同时正确的样本占比）。

## 3. 实验设计

- **PEEU 评估（真实在线多模态基准 WebVoyager）**：
  - 覆盖 8 类真实网站：Allrecipes（训练域内）、Amazon、Apple、Arxiv、Github、Coursera、Map、Wolfram（7 个 OOD 测试网站）。
  - 以**轨迹级成功率**作为最终评估指标。
  - 训练数据规模：**0.1k 轨迹**（仅 Allrecipes）和 **2k 轨迹**（Allrecipes + 其他未见于测试的网站补充）。
  - 对比方法：
    - Vanilla（基座模型直接推理）
    - Atomic-Prompt / Trajectory-Prompt（检索增强提示）
    - Coarse-SFT / Coarse-GRPO（粗粒度高层任务训练，即直接用探索轨迹训练）
    - Atomic-SFT / Atomic-GRPO（原子级任务训练）
    - PEEU-SFT / PEEU-GRPO（本文方法）
  - 基座模型：Qwen2.5-VL-3B-Instruct 和 Qwen2.5-VL-7B-Instruct。
  - 同时对比了开放模型的代表性商用大模型：GPT-4o、Claude 3 Opus、Qwen2.5-VL-32B/72B（Vanilla）。

- **TDHAF 评估（离线基准 Multimodal-Mind2Web）**：
  - 使用人工标注的金标准轨迹数据，训练集 616 样本，测试集 684 样本。
  - 训练和测试数据来自同一轨迹但任务改写（ID），或来自完全不同网站的不同轨迹（OOD）。
  - 分为三种训练设置（低/中/高层任务训练），每种在低/中/高三个测试集上分别评估，覆盖 3B 和 7B 两个模型规模。

## 4. 资源与算力

- 论文明确说明使用 **4 张 A800 GPU** 完成全部实验。
- PEEU 实验（SFT）：batch size 16，学习率 5.0e-6，训练 5 epochs，使用 llama-factory 框架。
- PEEU 实验（GRPO）：batch size 20，学习率 1.0e-6，rollout size 10，训练 7 epochs，使用 verl 框架。
- TDHAF 实验：batch size 8，学习率 5.0e-6，训练 3 epochs。
- **未说明的部分**：论文没有报告具体的训练耗时（如 GPU 小时数）、探索阶段的 API 调用成本，以及 GRPO 相比 SFT 的额外时间开销。

## 5. 实验数量与充分性

- **PEEU 实验**：覆盖 2 种模型规模（3B/7B）× 2 种数据规模（0.1k/2k）× 2 种训练方法（SFT/GRPO）× 8 种方法对比，在 8 个真实网站上评测，实验矩阵相对完整，并且**严格控制了数据规模与训练设置一致**，确保了公平性。
- **TDHAF 实验**：3 种训练粒度 × 3 种测试粒度 × ID/OOD 两个域 × 2 种模型规模，加上对 8 种泛化类型的分布分析，实验设计较为系统。
- **关于充分性的评价**：
  - 优点：在同等数据规模（0.1k/2k 轨迹）下进行对比，排除了数据量差异对结论的干扰；同时验证了多个模型规模下的趋势一致性；检索与训练方法的对比也验证了"训练优于检索"的结论。
  - 不足：OOD 测试网站相对有限（7 个），覆盖的网站类型（烹饪、购物、学术、代码、地图等）以信息获取和导航类任务为主，未涵盖登录、支付、表单提交等交互复杂度更高的场景；TDHAF 的 ID 与 OOD 划分仅来自单一数据集（Mind2Web），泛化结论的普适性仍需更多数据集验证。

## 6. 主要结论与发现

1. **PEEU 显著优于现有方法**：7B 模型 + PEEU-SFT（2k 轨迹）在 7 个 OOD 网站上达到 **30.6%** 平均准确率，不仅大幅超过 Coarse-SFT（19.0%）和 Atomic-SFT（21.7%），甚至超过参数量更大的 Qwen2.5-VL-32B Vanilla（22.7%），展现了高效的数据利用能力。
2. **高层任务训练优于低层任务训练**：在 2k 数据规模下，PEEU-SFT（30.6%）> Atomic-SFT（21.7%）> Coarse-SFT（19.0%），且该趋势在 3B/7B 两种模型、0.1k/2k 两种数据量下保持一致，说明**高层、对齐、受约束的规划经验训练**是跨网站泛化的关键。
3. **直接训练优于基于检索的提示**：对小型模型而言，不经过参数更新的检索提示方法效果甚至低于基座模型（7B 模型 Atomic-Prompt 和 Trajectory-Prompt 均为 3.7%，低于 Vanilla 的 7.8%），说明小型模型有限的推理能力无法有效利用检索到的上下文。
4. **TDHAF 分析揭示组合泛化的关键规律**：
   - **掌握低层原子技能并不保证高层规划能力**：7B 模型低层训练在低层测试上取得 89.6%，但高层测试仅 18.8%。
   - **高层训练可自上而下泛化且覆盖率更高**：7B 模型在 ID 场景下，高层训练的覆盖率为 51.9%，中层为 36.4%，低层仅为 9.1%；OOD 场景下同样呈现 37.8% > 29.7% > 25.7% 的趋势。
   - **高层任务训练带来更强的 OOD 多层级泛化能力**。

## 7. 优点

- **方法设计上的亮点**：
  - **事后经验（hindsight）机制**：从探索轨迹中逆向提炼任务，实现了任务-轨迹的严格对齐，将原本"不对齐、弱约束"的探索数据变废为宝（"turn trash into treasure"），这是方法层面最大的创新点。
  - **自主探索无需人工标注**：用户只需提供 URL，系统即可自动完成探索、经验提取和数据构建，具有良好的可扩展性。
  - **组合泛化分析框架（TDHAF）**：首次系统地从任务分解粒度角度量化分析 GUI 智能体的组合泛化行为，为后续研究提供了评估方法论。
- **实验设计上的亮点**：
  - 严格控制数据规模（同一轨迹量）和训练设置（同一超参数），保证了不同方法间的公平对比。
  - 在多个模型规模（3B/7B）和多种训练方法（SFT/GRPO）上验证了方法的一致性，结论具有较强的稳健性。
  - 引入较大参数量模型（32B/72B）与商用闭源大模型作为参照，突显了小型模型+高质量数据的性价比。

## 8. 不足与局限

- **任务类型覆盖有限**：受隐私与安全约束，未涉及用户登录、验证码破解、实际支付等敏感操作场景，任务以信息检索、商品搜索、行程规划等导航类为主，对真实世界更复杂的 GUI 交互（表单填写、多步交易等）覆盖不足。
- **测试网站数量有限**：OOD 评估仅在 7 个真实网站上完成，而训练探索仅从 Allrecipes 少量网站出发，网站的多样性和领域覆盖有待扩展。
- **数据规模仍然较小**：最大训练数据规模为 2k 轨迹，与工业界动辄数十万级别的数据量相比仍较小；虽然论文证明了高效性，但更大规模数据下的行为尚未验证。
- **探索模型与训练模型不一致**：探索和经验提取均使用 GPT-4o 完成，训练的是 Qwen2.5-VL 系列模型；探索模型本身的能力上限可能成为数据质量的天花板，论文没有讨论若使用更弱的探索模型的影响。
- **仅报告模型规模层面的比较**：论文没有报告训练时间、推理开销和 API 调用的总成本，对于实际部署的经济性评估不够完整。
- **TDHAF 评价指标存在一定局限**：Step SR 仅衡量单步完全匹配，对动作顺序和部分正确的容忍度较低；覆盖率指标对"全部三层正确"的要求严苛可能导致对部分泛化能力的低估。

（完）
