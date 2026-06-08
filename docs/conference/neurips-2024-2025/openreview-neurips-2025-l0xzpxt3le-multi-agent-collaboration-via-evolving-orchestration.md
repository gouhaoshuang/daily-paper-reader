---
title: Multi-Agent Collaboration via Evolving Orchestration
title_zh: 基于演化编排的多智能体协作
authors: "Yufan Dang, Chen Qian, Xueheng Luo, Jingru Fan, Zihao Xie, Ruijie Shi, Weize Chen, Cheng Yang, Xiaoyin Che, Ye Tian, Xuantang Xiong, Lei Han, Zhiyuan Liu, Maosong Sun"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=L0xZPXT3le"
tags: ["query:eca"]
score: 9.0
evidence: "直接研究多智能体协作中的动态编排，核心匹配'协作'需求"
tldr: 现有LLM多智能体协作依赖静态组织结构，随任务复杂度与智能体数量增加导致协调开销与低效。本文提出提线木偶范式，中央编排器（操控者）根据演化任务状态动态指挥智能体（木偶），并通过强化学习训练编排器自适应调整智能体优先级与顺序。实验证明该方法在多任务场景下显著提升协作效率与可扩展性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1436, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 576, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 775, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1438, \"height\": 525, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 564, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 849, \"height\": 427, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 1768, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1424, \"height\": 1391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1445, \"height\": 1193, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l0xzpxt3le/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1344, \"height\": 1090, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-l0xzpxt3le/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 755, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l0xzpxt3le/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 674, \"height\": 630, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l0xzpxt3le/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1125, \"height\": 259, \"label\": \"Table\"}]"
motivation: 静态组织结构的多智能体协作难以适应任务复杂度和智能体数量的增长，导致协调开销和低效。
method: 提出中央编排器动态指挥智能体的提线木偶范式，通过强化学习训练编排器自适应调整智能体优先级与顺序。
result: 在多任务场景下，该方法显著提升了协作效率与可扩展性。
conclusion: 演化式动态编排是实现可扩展多智能体协作的有效途径。
---

## Abstract
Large language models (LLMs) have achieved remarkable results across diverse downstream tasks, but their monolithic nature restricts scalability and efficiency in complex problem-solving. While recent research explores multi-agent collaboration among LLMs, most approaches rely on static organizational structures that struggle to adapt as task complexity and agent numbers grow, resulting in coordination overhead and inefficiencies. To this end, we propose a puppeteer-style paradigm for LLM-based multi-agent collaboration, where a centralized orchestrator ("puppeteer") dynamically directs agents ("puppets") in response to evolving task states. This orchestrator is trained via reinforcement learning to adaptively sequence and prioritize agents, enabling flexible and evolvable collective reasoning. Experiments on closed- and open-domain scenarios show that this method achieves superior performance with reduced computational costs. Analyses further reveal that the key improvements consistently stem from the emergence of more compact, cyclic reasoning structures under the orchestrator’s evolution. Our code is available at https://github.com/OpenBMB/ChatDev/tree/puppeteer.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：大型语言模型（LLM）在诸多下游任务中表现出色，但单体模型在复杂问题求解时受限于可扩展性和效率。近期研究探索基于LLM的多智能体协作，但大多采用**静态组织结构**（如固定拓扑图），难以随任务复杂度和智能体数量增长而适应，导致协调开销增加、效率下降。
- **核心问题**：能否通过**动态编排**同时最大化协作效果与计算效率？这是构建可扩展、鲁棒、实用的集体智能的关键。
- **整体含义**：本文提出一种“提线木偶”范式——中央编排器（puppeteer）根据任务状态动态指挥智能体（puppets），并通过强化学习持续优化编排策略，从而实现灵活、可演化的集体推理，兼顾性能与成本。

## 2. 论文提出的方法论

### 核心思想
- **动态编排**：抛弃静态协作模式，采用一个中央编排器在每个推理步骤根据当前上下文（任务状态）选择激活哪个智能体。该过程建模为**序列决策问题**，隐式生成推理图，支持灵活、可扩展的智能体协调。
- **自适应演化**：利用强化学习（REINFORCE）根据已完成任务的反馈（联合考虑解质量和资源消耗）持续更新编排策略，逐步偏好有效智能体链，剪除低效路径，推动系统向更高效率演化。

### 关键技术细节
- **智能体抽象**：每个智能体表示为 `a = (m, r, t)`，其中 `m` 为基础模型，`r` 为推理模式/提示策略，`t` 为外部工具集。
- **序列化编排**：将协作推理过程“展开”为按拓扑序遍历的推理序列，满足马尔可夫性：`P(a_{t+1} | S_{0..t+1}, τ) = P(a_{t+1} | S_{t+1}, τ)`。
- **策略优化**：使用REINFORCE算法，优化目标为期望回报 `J(θ) = E_{π_θ}[R(τ)]`，梯度近似为 `∇_θ J(θ) ≈ (1/N) Σ_n Σ_t ∇_θ log π_θ(a_t|S_t) · R(τ)`。
- **奖励设计**：终端奖励 `r` 为正确性（0/1或[0,1]质量分数），整体奖励递归定义，包含步级成本 `C_t = F · log(1 + t/φ)`，其中 `λ` 权衡准确率与效率，`γ` 为折扣因子。鼓励紧凑推理、早停。

### 算法流程（文字说明）
1. 初始化编排策略 π_θ（基于Llama-3.1奖励模型）。
2. 对于每个任务 τ，从初始状态 S_0 开始，循环：
   - 策略 π 根据当前状态 S_t 和任务 τ 选择智能体 a_t。
   - 激活 a_t，执行推理或工具调用，产生输出 o_t。
   - 更新系统状态 S_{t+1} = Φ(S_t, o_t)。
   - 若满足终止条件（如选择终止智能体或资源耗尽），则停止。
3. 获得完整轨迹 τ 后，计算总奖励 R(τ)。
4. 使用REINFORCE更新策略参数 θ。
5. 重复，直至收敛或达到预设轮次。

## 3. 实验设计

### 数据集与场景
- **封闭域任务**（需精确客观答案）：
  - **GSM-Hard**：复杂多步数学推理，使用**准确率**。
  - **MMLU-Pro**：多学科多选题，涵盖事实知识与逻辑推理，使用**准确率**。
- **开放域任务**（创意、开放结束）：
  - **SRDD**：软件需求开发，评估完整性、可执行性、一致性，使用官方综合指标。
  - **CommonGen-Hard**：用不相关概念生成连贯句子，评估语法、相关性、逻辑一致性及概念覆盖率。
- **附加具身环境**（正文附录A.4）：
  - **ALFWorld**：模拟具身环境，需实时交互与动作序列。

### 基准（Benchmark）设置
- 划分两个智能体子空间：
  - **Mimas**（小模型）：Qwen-2.5-7B/14B, LLaMA-3.1-8B, LLaMA-3.2-3B, Mistral-7B, Mistral-Nemo-12B 等。
  - **Titan**（大模型）：GPT-4-Turbo, GPT-4o-Mini, Gemini-1.5-Pro/Flash, Claude-3-Sonnet/Haiku, Qwen-2.5-72B, LLaMA-3.1-405B 等。

### 对比方法
- **纯模型**（无智能体结构）：LLaMA-3.1-8B/405B, GPT-4o-Mini, GPT-4-Turbo 等。
- **单智能体方法**：Self-Refine（迭代自修正）、AFlow（MCTS优化工作流）。
- **多智能体方法**：MacNet（静态DAG）、EvoAgent（演化算法自动生成MAS）。
- **本文方法**：Puppeteer（默认使用异构模型驱动智能体）和 Puppeteer-Mono（所有智能体同模型），并记录**初始阶段**与**演化阶段**结果。

## 4. 资源与算力

- **GPU**：NVIDIA A800 × 8。
- **峰值显存**：每GPU 28.8–78.4 GB。
- **训练时间**：2–6小时（因任务复杂度而异）。
- **说明**：训练是在线进行的，参数更新与多智能体推理交错，难以精确分离。文中指出与基线（如AFlow）计算模式不同，不宜直接比较计算成本。

## 5. 实验数量与充分性

- **实验组数**：主表（Table 1）覆盖4个数据集 × 2个子空间（Titan/Mimas） × 多种基线（纯模型、单智能体、多智能体） × 本文两种配置（Puppeteer/Puppeteer-Mono） × 两个阶段（初始/演化），总计超过80组对比。
- **消融与分析**：
  - 效率分析：展示Token消耗与智能体数量随训练步数的演化（LOWESS拟合），验证性能提升不增加计算开销。
  - 拓扑分析：图密度分布、循环分布，揭示“紧凑化”和“循环性”演化趋势。
  - 超参数影响（图7）：深度与宽度对准确率和Token消耗的非单调关系。
  - 具身环境泛化（附录A.4）：ALFWorld案例验证。
  - 性能-成本权衡曲线（附录A.2）：多个任务上性能/成本比持续上升。
- **充分性评价**：实验覆盖封闭域与开放域、不同模型规模、多种基线、多维度消融，设计较为系统。但部分基线（如AFlow、MacNet）仅使用同一基模型（如LLaMA-3.1-8B/405B），可能未完全体现其最佳性能；且部分数据集（如GSM-Hard）上基线准确率极低（如LLaMA-3.1-8B为0.0），可能存在模型适配问题。总体实验设计客观、公平，但需注意基线复现时的超参数未详述。

## 6. 论文的主要结论与发现

- **性能提升**：Puppeteer在演化阶段几乎在所有任务上取得最高平均分，Puppeteer-Mono也显著优于同基模型的基线方法。
- **效率同步提升**：性能提升不以增加计算开销为代价；Token消耗和智能体数量随训练下降（Titan子空间尤其明显），Mimas子空间Token减少主要来自优选低成本智能体而非早停。
- **结构演化**：编排策略促使MAS组织拓扑从松散链状演变为**紧凑、多循环**的图结构，图密度和循环数量显著增加，表明协同推理深化。
- **超参数控制**：深度和宽度存在最优平衡，默认设置（W4D2）取得最佳权衡。

## 7. 优点

- **动态编排思想新颖**：将多智能体协作转化为序列决策问题，引入中央编排器解耦智能体选择与内部行为，显著提升灵活性和可扩展性。
- **强化学习驱动的自适应演化**：通过奖励函数联合优化效果与效率，实现自动剪枝和链缩短，避免人工调参。
- **实验设计全面**：涵盖封闭/开放域、不同模型规模、多种基线、消融分析，以及具身环境泛化，证据充分。
- **分析深入**：对拓扑结构演化（紧凑化、循环性）进行定量分析，揭示了性能提升的潜在机制。
- **代码开源**：促进可复现性。

## 8. 不足与局限

- **奖励信号粗粒度**：仅依赖最终输出和Token消耗，缺乏过程级监督（如步骤正确性），可能限制优化效率。
- **固定智能体与工具集**：框架假设智能体和工具固定不变，无法在推理过程中动态添加或修改，适应性和鲁棒性受限。
- **偶尔的协调失败**：可能出现智能体间错误一致或误协调，需要更健壮的交互协议和激励机制。
- **基线复现局限**：部分基线仅使用单一基模型（如LLaMA-3.1-8B），未充分利用其最佳配置（如AFlow可能受益于更强模型），比较可能偏向本文方法。
- **训练成本不透明**：在线训练与推理交叉，难以精确分离计算开销；虽提到2-6小时，但未与基线进行公平成本对比（如AFlow推理式搜索的成本）。
- **数据集多样性局限**：主要面向推理、编程、创意写作；未在更广泛任务（如对话、问答）上验证。具身环境仅提供案例，缺乏系统评估。

（完）
