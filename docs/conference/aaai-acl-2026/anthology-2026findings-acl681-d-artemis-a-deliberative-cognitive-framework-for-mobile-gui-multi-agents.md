---
title: "D-Artemis: A Deliberative Cognitive Framework for Mobile GUI Multi-Agents"
title_zh: D-Artemis：面向移动GUI多智能体的深思认知框架
authors: "Hongze Mi, Yibo Feng, WenJie Lu, Yuqi Wang, Jinyuan Li, Song Cao, He Cui, Tengfei Tian, Xuelin Zhang, Haotian Luo, Di Sun, Jun Fang, Hua Chai, Naiqiang Tan, Gang Pan"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.681.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 面向移动GUI多智能体的认知框架，属于移动端智能体构建框架
tldr: 移动GUI智能体自动化任务时面临数据瓶颈、错误检测延迟和指令冲突等挑战。论文提出D-Artemis深思认知框架，模拟人类思考-对齐-反思循环，利用细粒度应用技巧检索和预执行对齐机制，通过Thought-Action Consistency检查与动作修正Agent协同降低风险。该方法提升了移动GUI多智能体的可靠性与任务自动化能力。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 749, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1468, \"height\": 832, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 703, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 702, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1376, \"height\": 676, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 745, \"height\": 376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 484, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1476, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1379, \"height\": 990, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1659, \"height\": 1153, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1660, \"height\": 1206, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1499, \"height\": 1473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1488, \"height\": 1899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl681/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1393, \"height\": 712, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1509, \"height\": 927, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1505, \"height\": 822, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 815, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1480, \"height\": 806, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1504, \"height\": 906, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1219, \"height\": 456, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1367, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1463, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl681/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1464, \"height\": 1351, \"label\": \"Table\"}]"
motivation: 移动GUI智能体存在数据瓶颈、错误检测延迟和指导冲突等问题，影响任务自动化效果。
method: 提出D-Artemis框架，结合思考-对齐-反思循环、应用技巧检索和预执行对齐机制。
result: 在移动GUI多智能体任务中降低了错误率，提高了任务完成可靠性。
conclusion: 为移动GUI多智能体提供了有效的认知框架，推动移动设备任务自动化的发展。
---

## Abstract
Graphical User Interface (GUI) agents aim to automate a wide spectrum of human tasks by emulating user interaction. Despite rapid advancements, current approaches are hindered by several critical challenges: data bottleneck in end-to-end training, high cost of delayed error detection, and risk of contradictory guidance. Inspired by the human cognitive loop of Thinking, Alignment, and Reflection, we present D-Artemis—a novel deliberative framework in this paper. D-Artemis leverages a fine-grained, app-specific tip retrieval mechanism to inform its decision-making process. It also employs a proactive Pre-execution Alignment stage, where Thought-Action Consistency (TAC) Check module and Action Correction Agent (ACA) work in concert to mitigate the risk of execution failures. A post-execution Status Reflection Agent (SRA) completes the cognitive loop, enabling strategic learning from experience. Crucially, D-Artemis enhances the capabilities of general-purpose Multimodal large language models (MLLMs) for GUI tasks without the need for training on complex trajectory datasets, demonstrating strong generalization. D-Artemis achieves SOTA among open-source general models on AndroidWorld (75.8%) and ScreenSpot-V2 (96.8%). Extensive ablation studies further demonstrate the significant contribution of each proposed component.

---

## 论文详细总结（自动生成）

## D-Artemis 论文详解

### 1. 论文的核心问题与整体含义（研究动机与背景）

- **研究背景**：GUI（图形用户界面）智能体旨在通过模拟人类交互来自动化广泛的移动端任务。当前视觉型 GUI 智能体主要沿两条技术路线发展：一是通过设计智能体框架来增强认知能力，二是通过专门训练范式（如 RL 或 SFT）直接提升端到端模型的 GUI 能力。
- **核心痛点**：论文指出现有方法面临三大关键挑战：
  - **数据瓶颈**：端到端训练高度依赖大规模轨迹数据，而数据来源有限、多样性不足，导致模型指令遵循能力下降，跨 GUI 框架兼容性差。
  - **错误检测延迟**：多数框架采用"事后反思"策略，错误只有在错误动作已导致任务偏离轨迹后才被发现，且反馈往往只给出成败结论，缺乏可诊断信息，容易陷入重复失败循环。
  - **矛盾性指导风险**：常见的通用提示或示例轨迹作为外部知识源，可能引入不同应用间相互冲突的操作逻辑，反而阻碍决策。
- **研究动机**：受到人类在复杂任务中"学习—规划—校准—反思"的深思熟虑认知循环启发，论文提出 D-Artemis 框架，模拟人类的"思考—对齐—反思"认知过程，旨在无需复杂轨迹数据训练的情况下，显著增强通用多模态大语言模型（MLLM）在移动 GUI 任务上的表现。

---

### 2. 论文提出的方法论

#### 核心思想
D-Artemis 是一个基于视觉的多智能体框架，采用"思考（Thinking）—对齐（Alignment）—反思（Reflection）"三维度认知循环，通过细粒度应用级提示检索、预执行主动对齐和事后策略性反思，实现更稳健、更自适应的移动 GUI 自主操作。

#### 关键技术细节

**(a) 动作生成（Action Generation）**
- 由 **Manager Agent** 作为主动作生成器，输入为用户任务 \(T_u\) 与环境截图观察 \(O_t\)。
- 采用**细粒度、应用专属的提示检索机制**：
  \[
  P_{T_u} = \text{RetrieveTips}(K, \text{App}(T_u))
  \]
  即从知识库 \(K\) 中按任务涉及的具体应用检索高相关提示，避免跨应用的逻辑冲突。
- **工作记忆 \(M_t\)**：由步历史 \(H_t\)（滑动窗口，保存最近 5 步的 thought-action 对）和最新反思 \(R_t\)（来自 SRA 输出）组成。
- Manager Agent 的决策过程可表示为：
  \[
  s_t = \langle \tau_t, a_t \rangle = \pi(T_u, O_t, P_{T_u}, M_t)
  \]

**(b) 预执行对齐（Pre-execution Alignment）**
- **TAC Check 模块**：基于 Qwen2.5-VL-7B 微调而成的轻量级专家模型，判断 thought-action 对是否一致：
  \[
  c_t = \text{TAC}(\tau_t, a_t, V_{a_t}), \quad c_t \in \{0,1\}
  \]
  其中 \(V_{a_t}\) 为动作可视化（在截图上标注动作坐标）。
- **动作修正智能体（ACA）**：当 \(c_t = 0\) 时触发，分析三类主流错误（动作类型错误、动作参数错误、无效动作），并输出修正后的 thought-action 对：
  \[
  s_t = \langle \hat{\tau}_t, \hat{a}_t \rangle =
  \begin{cases}
  f_{AC}(\tau_t, a_t, V_{a_t}), & \text{if } c_t = 0 \\
  \langle \tau_t, a_t \rangle, & \text{if } c_t = 1
  \end{cases}
  \]

**(c) 事后反思（Post-execution Reflection）**
- **状态反思智能体（SRA）**：以任务目标、已执行的 thought-action 对环境状态的变化 \(O_t \to O_{t+1}\) 为输入，判断步骤有效性，并对失败步骤进行深入分析、生成策略性建议，更新工作记忆：
  \[
  r_t = f_{SR}(T_u, s_t, O_t, O_{t+1})
  \]

#### 工作流程
每个步骤经历"动作生成 → 预执行对齐 → 事后反思"三阶段生命周期，形成完整的"思考—对齐—反思"认知闭环。

---

### 3. 实验设计

#### 数据集与基准（Benchmark）
- **AndroidWorld**：在线动态移动智能体基准，在真实 Android 模拟器上运行，包含 20 个应用上的 116 个核心任务，通过参数随机化可产生数百万个任务变体，用于评估动态任务执行能力。
- **ScreenSpot-V2（移动子集）**：跨平台通用 GUI 元素定位基准，包含 1,272 条单步指令及对应边界框，涵盖文本元素、图标和控件（如待办清单），用于评估 GUI 元素 grounding 能力。

#### 对比方法与基线
- **AndroidWorld 对比**：
  - 闭源模型：Gemini-1.5-Pro、Claude Computer-Use、GPT-4o、Aguvis (GPT-4o)、UGround (GPT-4o)、Aria-UI (GPT-4o)、AndroidGen (GPT-4o)、Agent-S2 (Claude-3.7-Sonnet)。
  - 开源通用模型：Qwen2-VL-72B、Qwen2.5-VL-72B、UI-TARS-72B、Seed1.5-VL、MobileUse、UI-Venus。
  - GUI 专用模型：V-Droid、Mobile-Agent-v3 (GUI-Owl-7B/32B)。
- **ScreenSpot-V2 对比**：
  - 闭源模型：GPT-4o。
  - 开源通用模型：Qwen2.5-VL-7B/72B。
  - SFT 类 GUI 专用模型：SeeClick、UGround、Aguvis、OS-Atlas、UI-TARS-7B/72B、GUI-Actor。
  - RL 类 GUI 专用模型：Phi-Ground、UI-R1-E、LPO、GTA1-7B/72B。

#### 基座模型设置
- 采用 Qwen2.5-VL-72B-Instruct 和 GUI-Owl-32B 作为基座模型，解码温度固定为 0 以确保输出确定性。
- 动作空间定义了 11 种动作类型：key、click、long_press、swipe、type、clear_text、system_button、open、wait、take_note、terminate。

---

### 4. 资源与算力

- **推理实验环境**：服务器配备 4 × 8 × NVIDIA A100 80G GPU（即共 32 张 A100 80G），用于搭建实验环境并运行评估。
- **TAC 模块训练环境**：
  - 2 节点 × 8 张 A100 80GB（共 16 张 A100 80GB）。
  - 采用 DeepSpeed ZeRO-3 优化策略。
  - 基座模型为 Qwen2.5-VL-7B，全参数微调，BF16 混合精度 + FlashAttention-2。
  - 有效批大小 64（Per-device 批大小 1 × 梯度累积 4 × 16 GPU），训练 6 个 epoch。
  - 基础学习率 1e-5，视觉编码器学习率 1e-6，采用余弦退火调度、梯度裁剪（max norm = 1.0）。
- **未明确说明**：论文中未明确披露 TAC 模块的具体训练时长、总 GPU 小时数以及 ACA/SRA 推理的硬件开销。

---

### 5. 实验数量与充分性

#### 实验种类统计
论文共进行了以下多组实验：

| 实验类型 | 数量/范围 | 目的 |
|---|---|---|
| 主实验（AndroidWorld） | 1 组，覆盖 20 个应用 | 对比 15+ 种基线方法 |
| 主实验（ScreenSpot-V2） | 1 组，1,272 个样本 | 对比 14+ 种基线方法 |
| 消融实验（逐步叠加） | 4 个条件（Baseline、+SRA、+ACA、+TAC、+Tips） | 验证各组件独立贡献 |
| 消融实验（逐步去除） | 3 个条件（完整模型、-SRA、-可视化、-预执行对齐） | 验证关键组件必要性 |
| 提示检索策略对比 | 3 种策略（无提示、混合提示、应用专属提示） | 验证细粒度检索优势 |
| ACA 性能评估 | 179 个错误案例 | 验证修正能力与延迟 |
| TAC 模块评估 | 450 个样本的独立测试集 | 验证检测准确率与召回 |
| 错误分析 | 2 个模型（baseline vs D-Artemis） | 分类失败原因 |

#### 充分性与客观性评估
- **优势**：消融实验设计系统完整，采用逐模块叠加和逐模块去除的双向验证；对比基线覆盖全面，涵盖闭源、开源、通用、GUI 专用（SFT/RL）各类方法；确保与同基座模型（Qwen2.5-VL-72B）对比时体现纯框架增益；TAC 评估采用分层采样保证负样本充足并单独报告有效动作召回率。
- **潜在不足**：AndroidWorld 上仅报告成功率一个指标，缺少任务步数效率、恢复成本等细粒度指标；ScreenSpot-V2 仅用 Qwen2.5-VL-72B 一个基座，未验证框架对不同基座模型的泛化；消融实验仅在同一基座模型上验证，未在 GUI-Owl-32B 上重复消融。

---

### 6. 论文的主要结论与发现

- **SOTA 性能**：D-Artemis 在 AndroidWorld 上达到 75.8% 成功率（使用 GUI-Owl-32B），较 Mobile-Agent-v3（73.3%）提升 2.5% 绝对值；在 Qwen2.5-VL-72B 基座上达到 68.1%，超越 UI-Venus（65.9%）2.2%。在 ScreenSpot-V2 移动子集上达到 96.8% 平均成功率，其中图标/控件类任务达 95.6%，超越此前 SOTA（GTA1-72B 的 96.4%）。
- **预执行对齐的显著增益**：TAC + ACA 协作机制带来 22.4% 的绝对性能提升（从 38.8% 到 61.2%），其中 ACA 单独贡献 8.6%，TAC 的引入额外增加 13.8%，体现了其双重功能（错误过滤器 + 防止错误修正）。
- **动作可视化不可或缺**：移除动作可视化导致性能大幅下降（从 68.1% 降至 45.3%），证明视觉信息在修正坐标类错误中的关键作用。
- **事后反思的双重能力**：SRA 在基础模型上带来 3.8% 增益，但在完整框架中贡献达 15.9%，说明其在增强环境变化感知和提供有效决策引导方面的协同价值。
- **细粒度提示检索的必要性**：应用专属提示检索带来 6.9% 性能增益。对比实验证实，混合提示策略不仅无效，甚至比无提示更差，验证了矛盾性指导确实会损害决策。
- **错误重心转移**：错误分析表明，D-Artemis 大幅降低了 Grounding 和 Navigation 类错误，剩余失败主要归因于更高层的 Planning 和 Perception 错误，反映了基座模型固有的端到端推理局限。

---

### 7. 优点

- **无需训练即可增强通用模型**：D-Artemis 不需要在复杂轨迹数据上进行训练，即可显著提升通用 MLLM 的 GUI 任务能力，回避了数据瓶颈问题，具有强泛化能力。
- **预执行对齐的创新设计**：将错误修正从传统的"事后补救"前移到"执行前校准"，通过 TAC 轻量过滤器 + ACA 深度修正的双层设计，既控制了开销又保证了修正质量。
- **细粒度、应用专属的知识检索**：不同于传统粗粒度通用提示，D-Artemis 的检索机制有效避免了跨应用逻辑冲突，以实证数据验证了"混合提示有害"的假设。
- **完整的认知循环建模**：思考—对齐—反思三阶段循环完整模拟了人类精细动作调整与经验反思学习过程，具有理论启发意义。
- **模块化、可解释性强**：每个组件职能清晰、可独立评估，ACA 的错误分类体系明确（Action Type Error / Action Parameters Error / Invalid Action），便于诊断与改进。
- **工程落地细节完善**：TAC 模块平均推理延迟仅约 380 ms，ACA 平均修正延迟约 2.12 秒，以极小开销换取任务成功率的显著提升；数据标注通过多人协作 + Fleiss Kappa（0.83）保证质量。

---

### 8. 不足与局限

- **底层模型认知瓶颈**：如前文错误分析所示，框架虽能有效解决执行层和引导层问题，但最终性能仍受限于基座模型的推理和感知能力。案例中，智能体因"幻觉"认为前置步骤已完成而过早执行动作，此类高层认知错误 D-Artemis 无法预防。
- **知识库依赖人工构建**：当前提示知识库为预定义的、面向特定应用的，需要人工编写且不具实时更新能力。论文虽提出未来将研究自动生成高质量提示，但现阶段这构成应用扩展瓶颈。
- **框架规模与算力要求较高**：框架涉及多个智能体（Manager、ACA、SRA）和 TAC 模块协同工作，对推理算力提出较高要求。论文承认需要探索更轻量的模型设计，尤其面向端侧部署时，多模型协同可能成为实际限制。
- **实验覆盖有限**：仅在 AndroidWorld 和 ScreenSpot-V2 两个基准上评估，未涉及 iOS 或其他操作系统环境；AndroidWorld 上的应用范围有限（20 个），知识库也仅覆盖其中部分应用，未验证全应用覆盖效果。
- **评测指标单一**：AndroidWorld 主实验仅报告成功率一个指标，缺少任务效率、平均步数、修正率、恢复成本等维度，对框架在"效率与可靠性"上的全面权衡评估略显不足。
- **消融实验基座单一**：消融实验仅在 Qwen2.5-VL-72B 上开展，GUI-Owl-32B 基座未进行消融验证。框架组件在不同能力水平的基座模型上的增益是否一致，缺乏数据支撑。
- **TAC 模块的局限**：TAC 数据集基于 Qwen2.5-VL-72B 的轨迹采样，可能存在基座模型特定偏差；非坐标类动作的负样本比例较低（如 system_button 类负样本为 0），检测能力在这些类别上的验证不够充分。

---

（完）
