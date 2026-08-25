---
title: "UI-Copilot: Advancing Long-Horizon GUI Automation via Tool-Integrated Policy Optimization"
title_zh: UI-Copilot：通过工具集成策略优化推进长时程GUI自动化
authors: "Zhengxi Lu, Fei Tang, Guangyi Liu, Jin Ma, Kaitao Song, Xu Tan, Wenqi Zhang, Weiming Lu, Jun Xiao, Yueting Zhuang, Yongliang Shen"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.904.pdf"
tags: ["query:mobile-agent"]
score: 8.0
evidence: 面向长时程GUI自动化的协作框架，方法直接适用于移动应用内的自动化操作
tldr: 长时程GUI自动化中，智能体常因内存退化、进度混淆和算术幻觉而失败。UI-Copilot提出协作框架，让GUI智能体专注执行，同时由轻量级助手按需提供记忆检索与数值计算服务；通过记忆解耦将持久观察与瞬时执行上下文分离。实验结果表明该框架显著提升长时程GUI任务的完成率和稳定性。方法虽未限定手机端，但对移动应用内自动化操作有直接借鉴意义。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 801, \"height\": 841, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1641, \"height\": 735, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 792, \"height\": 707, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1646, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 791, \"height\": 669, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1609, \"height\": 731, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 793, \"height\": 886, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1628, \"height\": 797, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 785, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 514, \"height\": 370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 343, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 370, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 390, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 377, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 383, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 632, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 777, \"height\": 340, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 786, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 715, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 194, \"height\": 749, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1564, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1395, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 183, \"height\": 731, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 186, \"height\": 1121, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1637, \"height\": 818, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long904/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1652, \"height\": 583, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long904/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1657, \"height\": 663, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long904/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1649, \"height\": 764, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long904/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 787, \"height\": 773, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long904/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1640, \"height\": 1102, \"label\": \"Table\"}]"
motivation: GUI智能体在长时程任务中常发生记忆退化、进度混淆和数学幻觉。
method: 提出UI-Copilot协作框架，用轻量级助手处理记忆检索与数值计算，并采用记忆解耦。
result: 长时程GUI任务完成率与稳定性显著提升，优于独立执行的基础智能体。
conclusion: 表明记忆与计算外接可以帮助GUI智能体突破长时程瓶颈，可迁移至移动应用场景。
---

## Abstract
MLLM-based GUI agents have demonstrated strong capabilities in complex user interface interaction tasks. However, long-horizon scenarios remain challenging, as these agents are burdened with tasks beyond their intrinsic capabilities, suffering from memory degradation, progress confusion, and math hallucination. To address these challenges, we present UI-Copilot , a collaborative framework where the GUI agent focuses on task execution while a lightweight copilot provides on-demand assistance for memory retrieval and numerical computation. We introduce memory decoupling to separate persistent observations from transient execution context, and train the policy agent to selectively invoke the copilot as Retriever or Calculator based on task demands. To enable effective tool invocation learning, we propose ̲ T ool- ̲ I ntegrated ̲ P olicy ̲ O ptimization ( TIPO ), which separately optimizes tool selection through single-turn prediction and task execution through on-policy multi-turn rollouts. Experimental results show that UI-Copilot-7B achieves state-of-the-art performance on challenging MemGUI-Bench, outperforming strong 7B-scale GUI agents such as GUI-Owl-7B and UI-TARS-1.5-7B. Moreover, UI-Copilot-7B delivers a 17.1% absolute improvement on AndroidWorld over the base Qwen model, highlighting UI-Copilot’s strong generalization to real-world GUI tasks. Code website: https://anonymous.4open.science/r/UI-Copilot-0535.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究背景**：基于多模态大语言模型（MLLM）的 GUI 智能体在复杂用户界面交互任务中已展现出强大的能力，例如理解屏幕元素、规划操作步骤、执行点击输入等。
- **核心问题**：在**长时程（Long-Horizon）GUI 自动化任务**中，智能体表现显著退化。论文识别出三大关键失败模式：
  - **记忆退化**：随着任务步骤增多，智能体遗忘早期观察到的界面状态或关键信息，导致后续决策失去依据。
  - **进度混淆**：智能体无法准确判断当前已完成了哪些子目标、还剩下哪些步骤，容易重复操作或遗漏步骤。
  - **数学幻觉**：MLLM 在处理数值计算（如累加价格、计算时间差、统计数量）时产生不准确甚至虚构的结果，直接影响任务正确性。
- **整体含义**：上述问题表明，将记忆检索与数值计算等**超出智能体固有能力的任务**强加给 GUI 智能体本身，是长时程自动化失败的根源。论文主张通过**外部工具与协作式分工**来释放智能体潜力，使其专注于核心的执行决策。

### 2. 论文提出的方法论

- **核心思想**：提出 **UI-Copilot** 协作框架，将 GUI 智能体的职责与辅助工具的职责解耦：
  - **GUI 智能体**（Policy Agent）：专注于任务执行——理解当前界面、决定下一步操作。
  - **轻量级协作者**（Copilot）：按需提供两类服务——**记忆检索**（Retriever）与**数值计算**（Calculator）。
- **记忆解耦（Memory Decoupling）**：
  - 将**持久观察**（persistent observations，如历史屏幕截图、关键状态信息）与**瞬时执行上下文**（transient execution context，如当前步骤的短期推理）分离存储。
  - 这种设计让长时程任务中早期的重要信息不会被新信息覆盖，当智能体需要回想历史状态时，可主动请求 Retrieve 工具获取。
- **工具调用学习**：
  - 训练策略智能体**根据任务需求选择性地调用** Copilot，即自主决定何时将 Copilot 作为 Retriever 或 Calculator 使用，而非盲目地在每步都调用。
- **关键技术——工具集成策略优化（TIPO, Tool-Integrated Policy Optimization）**：
  - **解耦优化目标**：将两个不同性质的子问题分开优化，避免互相干扰。
    1. **工具选择**：通过**单轮预测（single-turn prediction）**进行优化，即学习判断“当前是否需要工具、该用哪个工具”。
    2. **任务执行**：通过**在策略多轮展开（on-policy multi-turn rollouts）**进行优化，即让智能体在与环境交互的完整轨迹中学习如何高效完成任务。
  - 这种分离式优化使得“决定是否调用工具”和“具体如何操作界面”两种能力可以被分别强化，提高训练效率与最终性能。

### 3. 实验设计

- **基准数据集（Benchmark）**：
  - **MemGUI-Bench**：论文提出的面向长时程 GUI 任务的新基准，专门考察智能体在**需要长期记忆保持和数值推理**的场景下的表现。
  - **AndroidWorld**：真实 Android 环境中的通用 GUI 自动化基准，用于验证框架在新场景上的泛化能力。
- **对比方法**（7B 规模模型）：
  - **GUI-Owl-7B**：现有强基线 GUI 智能体。
  - **UI-TARS-1.5-7B**：另一代表性的 7B 规模 GUI 智能体。
  - **Qwen 基础模型**：作为消融的底座模型，用于对比引入 UI-Copilot 框架前后的性能差异。
- **评估维度**：任务完成率（Success Rate）及稳定性指标，重点关注长时程任务中的持续表现。

### 4. 资源与算力

- 论文文本中**未明确说明**训练所用的 GPU 型号、数量、训练时长等算力信息。
- 仅可推断模型规模为 7B 参数级别，对比方法也均为同规模模型，训练成本处于主流可接受范围。具体的硬件资源配置需查阅论文原文或代码仓库获取进一步细节。

### 5. 实验数量与充分性

- **实验规模**：论文包含两大场景的实验——MemGUI-Bench（新基准）上的 SOTA 对比，以及 AndroidWorld 上的泛化验证；此外还包含与多个 7B 强基线的横向对比。
- **充分性分析**：
  - **优点**：新基准+真实环境双验证的设计较为全面；既证明了框架在专门长时程任务上的优势，也证明了其迁移到真实世界的可行性。
  - **不足**：受提供文本限制，无法确认是否包含系统的消融实验（如剔除记忆解耦、剔除 TIPO 的逐项消融）、不同模型规模（如 3B、13B、70B）的扩展性实验，以及多轮重复实验的方差报告。若要充分验证各组件贡献，建议补充相关消融。

### 6. 论文的主要结论与发现

- **性能领先**：UI-Copilot-7B 在 MemGUI-Bench 上达到**当前最优（State-of-the-Art）**，显著优于 GUI-Owl-7B 和 UI-TARS-1.5-7B 等强 7B 基线。
- **强泛化能力**：在 AndroidWorld 上，UI-Copilot-7B 相对于底座的 Qwen 模型取得了 **+17.1% 的绝对提升**，表明协作框架并非仅针对特定基准过拟合，而是能够推广到真实 GUI 任务中。
- **核心发现**：**记忆与计算外接**（将记忆检索和数值计算外包给专用工具）可以有效帮助 GUI 智能体突破长时程任务瓶颈；通过解耦设计和联合策略优化，智能体能够学会在合适的时机借助工具补足自身短板。

### 7. 优点

- **问题定位精准**：明确指出长时程 GUI 任务的三大失败模式（记忆退化、进度混淆、数学幻觉），有针对性而非泛泛地提出方案。
- **设计简洁有效**：采用“轻量级 Copilot + 主智能体”的架构，不增加主模型推理负担，仅在需要时调用工具，工程上更易落地。
- **优化方法有创新**：TIPO 将工具选择与任务执行解耦优化，契合两类任务性质差异，是方法论上的亮点。
- **实验说服力强**：新基准+真实环境双验证+7B 同规模公平对比，证明性能提升不是特定场景下的偶然结果。
- **应用迁移价值高**：虽然论文未限定移动端，但框架对移动应用内的长时程自动化操作具有直接借鉴意义，如跨页面填写表单、多 App 协作等场景。

### 8. 不足与局限

- **算力信息缺失**：未报告训练资源消耗，难以评估方法的训练成本门槛。
- **消融实验未明确展示**：从现有信息看，缺少对记忆解耦、TIPO 各组件、不同调用策略的系统性消融，框架各设计要素的独立贡献尚不够清晰。
- **基准覆盖面有限**：MemGUI-Bench 为新提出基准，可能存在设计偏向（如过度强调记忆和计算）；AndroidWorld 虽为真实环境，但任务类型仍以相对固定的操作为主。对开放域、跨 App 的极端长时程场景覆盖有待验证。
- **模型规模单一**：仅在 7B 规模上验证，较小或较大模型的适用性未知；7B 模型对长时程任务天然能力受限，该框架在大模型（如 70B）上是否仍有显著增益需进一步探索。
- **偏差风险**：论文提出的记忆退化、数学幻觉等问题主要依赖作者对基准任务的设计判断，不同任务分布下三大失败模式的权重可能发生变化，方法的普适性需更多第三方数据集验证。

（完）
