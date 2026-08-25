---
title: "OpenPhone: Mobile Agentic Foundation Models"
title_zh: OpenPhone：移动端智能体基础模型
authors: "Yangqin Jiang, Chao Huang"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1518.pdf"
tags: ["query:mobile-agent"]
score: 10.0
evidence: 移动GUI智能体系统，通过设备-云协作实现任务自动化
tldr: 针对移动GUI智能体面临的设备端模型能力不足、云端模型成本高的问题，提出OpenPhone系统，采用设备-云协作策略，通过两阶段训练增强Qwen2.5-VL-3B模型。在移动端任务执行上取得了接近云端大模型的性能，同时降低了部署成本，为在真实手机上进行自主任务执行提供了实用解决方案。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 804, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1649, \"height\": 1088, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 722, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 713, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 780, \"height\": 299, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 634, \"height\": 263, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 640, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 636, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 813, \"height\": 207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1518/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1590, \"height\": 891, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1518/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 799, \"height\": 919, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1518/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 725, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1518/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 797, \"height\": 448, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1518/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1440, \"height\": 656, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1518/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1614, \"height\": 905, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1518/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1289, \"height\": 1344, \"label\": \"Table\"}]"
motivation: 设备端小型模型性能不足，而云端大模型部署昂贵，移动智能体面临性能与成本的两难。
method: 提出设备-云协作架构，利用两阶段训练强化Qwen2.5-VL-3B，并结合云端模型的高能力。
result: 在移动GUI任务上取得优异的执行效果，兼顾成本与性能。
conclusion: 设备-云协同是构建移动智能体的有效范式，能实现部署友好且性能可靠的手机端任务自动化。
---

## Abstract
With the advancement of multimodal large language models (MLLMs), building GUI agent systems has become an increasingly promising direction—especially for mobile platforms, given their rich app ecosystems and intuitive touch interactions. Yet mobile GUI agents face a critical dilemma: truly on-device models (4B or smaller) lack sufficient performance, while capable models (starting from 7B) are either too large for mobile deployment or prohibitively costly (e.g., cloud-only closed-source MLLMs). To resolve this, we propose OpenPhone, a mobile GUI agent system that leverages device-cloud collaboration to tap the cost-efficiency of on-device models and the high capability of cloud models, while avoiding their drawbacks. Specifically, OpenPhone enhances Qwen2.5-VL-3B via two-stage SFT→GRPO training on synthetic GUI data for strong decision-making, integrates an efficient long-reasoning mechanism to utilize historical interactions under tight resources, and defaults to on-device execution—only escalating challenging subtasks to the cloud via real-time complexity assessment. Experiments on the online AndroidLab benchmark and diverse apps show OpenPhone matches or nears larger models, with a significant reduction in cloud costs.

---

## 论文详细总结（自动生成）

## 1. 核心问题与研究动机

- **背景**：多模态大语言模型（MLLMs）的进步推动了 GUI 智能体系统的发展，移动平台因其丰富的应用生态和直观的触屏交互成为该技术的理想测试场。然而，移动平台存在严重的**计算能力和内存限制**。
- **核心困境**：移动 GUI 智能体面临两难选择——
  - 真正能在设备端运行的模型（4B 及以下）**性能不足**，难以胜任实际 GUI 任务；
  - 能力足够的模型（7B 起步）要么**体积过大无法在手机端部署**，要么依赖昂贵的云端闭源大模型（如 GPT-5、Claude-Sonnet-4、Gemini-2.5-Pro），**单次任务成本高到不具实用性**。
- **研究问题**：
  - **问题一**：任务专用 GUI 模型能否进一步缩小到真正能在手机上运行的规模（~3B），同时保持可接受的性能？
  - **问题二**：对能力不可或缺的专有云端大模型，能否大幅降低其使用成本？
- **解决思路**：作者提出 **OpenPhone**，一种**设备-云协作**的移动 GUI 智能体框架，利用设备端小模型的成本效益与云端大模型的高能力互补，避开各自的劣势。

---

## 2. 方法论

OpenPhone 框架由三个关键模块组成：

### 2.1 高效推理 GUI 智能体（On-Device Agent）

- **长时推理增强（Long-Horizon Reasoning Enhancement）**
  - 受 CoT 推理和测试时扩展定律启发，为小模型引入多步推理链：分析屏幕可操作元素 → 结合历史数据评估先前操作 → 判断任务进展 → 选择动作并生成输出。
  - 若历史显示先前操作未达到预期，模型会**主动反思并调整策略**，避免重复错误和循环。
- **高效记忆管理（Efficient Memory Management）**
  - 高分辨率截图占用大量 token，无法在历史中长期保存原始图像。
  - 方案：将每一步的状态压缩为**结构化文本摘要**（STATE_ASSESSMENT），包含界面状态、任务进度、推断的下一步动作、预期结果和潜在问题。
  - 文本摘要 token 远少于图像，可在资源受限环境下保留 10–20 步的长历史。
- **形式化定义**：整个流程为顺序决策框架——在每个时间步 t，推理函数 R 将（历史 h_t、当前屏幕 s_t、任务指令 τ）映射为（新评估 a_t、要执行的函数 f_t），历史通过拼接 a_t 持续更新。

### 2.2 设备-云协作智能体系统（Device-Cloud Collaboration）

- **动机**：对设备端模型失败的分析发现，**许多任务仅仅在最后一步失败**——意味着设备端模型大多数时候表现良好，只需在关键节点引入云端干预。
- **任务复杂度评估（Task Complexity Assessment）**：执行前，基于设备端模型的历史表现数据评估任务难度，确定两个关键参数：
  - γ：开始监控的步骤数；
  - ω：监控频率（每隔多少步检查一次）。
- **动态编排策略（Dynamic Orchestration Policy）**：执行中，当步数 ≥ γ 且每 ω 步进行一次检查，通过函数 F_switch 评估三个切换标准：
  1. 出现**重复动作模式**；
  2. **偏离预期任务轨迹**；
  3. **动作质量不足**。
  - 满足任一条件即从设备端模型 M_device 切换到云端模型 M_cloud，切换后不再监控，直至任务完成。这保证了"仅在必要时调用云端"。
- **算法流程**（Algorithm 1）：先调用 F_assess 确定 γ 和 ω → 初始化设备端模型为当前模型 → 循环执行函数调用并更新历史 → 到达监控条件时评估是否切换 → 切换后由云端模型接管至任务结束。

### 2.3 轻量级 MLLM 训练

- **合成数据生成管线**：
  - 人类标注的轨迹数据通常仅含指令、截图和真实动作，缺乏推理链，小模型难以从中获得推理和反思能力。
  - 方案：使用高级 MLLM（如 Gemini-2.5-Pro）基于任务指令、目标函数和历史交互生成 CoT 推理 → 再使用强大的 LLM（如 Qwen3-32B）根据生成的推理和原始指令合成完整训练实例。
- **两阶段训练协议**：
  - **第一阶段（SFT）**：在合成数据上监督微调，赋予小模型基础推理能力和 GUI 任务基础能力，为后续强化学习提供有意义的初始行为。
  - **第二阶段（GRPO）**：组相对策略优化（Group Relative Policy Optimization），直接优化模型输出动作的正确性。
- **奖励设计**：
  - **准确率奖励 R_accuracy**：
    - 操作类任务（如 Tap(index)）：预测与真实值**严格匹配**得 1 分；
    - 查询类任务（如 Finish(answer)）：基于嵌入相似度，sim ≥ λ 时给分。
  - **格式奖励 R_format**：根据输出是否符合三块结构（REASONING / STATE_ASSESSMENT / CALLED_FUNCTION）给予基础奖励，并对模板外内容施加惩罚系数 ψ^c，专门抑制小模型常见的无关生成。
  - 总奖励：R_total = R_accuracy + R_format。
- **GRPO 目标函数**（公式 5-7）：使用组内相对优势（advantage），无需单独的 critic 模型；通过组内奖励的均值和标准差标准化；加入基于无偏估计器的 KL 散度正则化。

---

## 3. 实验设计

### 3.1 基准与数据集

- **AndroidLab**：在线 GUI 任务评估基准，基于 Android 平台，包含 **9 个常用应用、138 个评估任务**，支持 XML 和 SoM 两种输入模式。OpenPhone 主要采用 **SoM（Set-of-Mark）模式**。
- **追加应用评估**：补充 4 个常用应用——**Chrome、TikTok、Reddit、Gmail**，共 25 个自定义任务，用于评估真实世界性能。

### 3.2 评估指标

- **成功率（SR）**：任务完成百分比。任务仅在智能体输出 finish() 确认完成时视为结束，通过中间步骤日志、最终截图和输出综合评估。

### 3.3 对比方法

- **通用视觉大模型**：
  - 闭源：GPT-4o、GPT-5-nano、GPT-5-mini；Gemini-1.5-Pro、Gemini-2.5-Pro、Gemini-2.5-Flash；Claude-3.5-Haiku、Claude-Sonnet-4
  - 开源：Qwen2.5-VL、Llama-3.1、GLM 系列
- **GUI 专用/微调模型**：AutoGLM、AutoGLM-Mobile、UI-Tars 家族、V-Droid、UI-Genie-Agent、MobileUse、Llama-3.1-8B (ft)、GLM-4-9B (ft)
- **OpenPhone 变体**：仅设备端模型（Ours w/o Cloud LLM）、设备-云端协作（Ours w Gemini-2.5-Pro / Flash）

### 3.4 关键结果

| 模型 | SR（AndroidLab） |
|---|---|
| Gemini-2.5-Pro | 56.5 |
| GLM-4.5-V | 49.3 |
| **Ours w Gemini-2.5-Pro** | **47.1** |
| AutoGLM-Mobile | 46.4 |
| Claude-Sonnet-4 | 40.6 |
| UI-Tars-7B | 32.6 |
| **Ours w/o Cloud LLM（3B）** | **15.2** |

---

## 4. 资源与算力

- 论文中**没有明确披露训练所使用的 GPU 数量、型号和训练时长**。
- 仅在效率对比实验中提及：模型通过 **vLLM** 部署，在 **1 或 2 张 NVIDIA RTX 3090** 上测试推理延迟。
- 据此可以确认的是：OpenPhone（3B）在单张 RTX 3090 上即可运行，而 GLM-4.1V-9B 在单卡上无法维持所需上下文长度。但具体的训练算力消耗（GPU 时数、显存占用等）**未被报告**。

---

## 5. 实验数量与充分性

### 实验组数概览

| 实验类型 | 数量/规模 |
|---|---|
| AndroidLab 在线评估 | 138 个任务，9 个应用 |
| 追加应用评估 | 25 个任务，4 个应用 |
| 主对比方法数 | 约 24 个基线模型/变体 |
| 消融实验 | 5 个变体（w/o Tuning、w/o SFT、w/o GRPO、w/o Reasoning、w/o History） |
| GRPO 变体分析 | 3 个变体（标准、小批量、Zero） |
| 设备-云协作分析 | 多个 MLLM 作为云端模型的对比 |
| 效率对比 | 3 个模型 × 2 种硬件配置 |

### 充分性评估

- **优势**：采用了**在线真实环境评估**（AndroidLab），而非仅离线指标，结果更具说服力；补充了常用应用的真实场景测试；消融较全面（训练、推理、历史、协作策略均覆盖）；GRPO 变体分析深入（批量大小、有无 SFT 的对比）。
- **不足**：
  - 追加应用任务仅 25 个且只展示了 12 个（附录 Table 5），样本量有限；
  - 未报告多次运行的标准差，无法判断结果稳定性；
  - 论文未说明其 LLM-based 评估器与 AndroidLab 规则评估器的一致性验证；
  - 设备模型在高难度任务（如 Bluecoins、Map.me）上的成功率接近 0%，说明测试任务分布可能偏向简单任务。

---

## 6. 主要结论与发现

1. **Small-but-Mighty（小而强）**：训练后的 OpenPhone（3B）能够匹配大一个量级的模型（如 Qwen2.5-VL-7B、GLM-4-9B(ft)），甚至超越部分轻量闭源模型（GPT-5-nano、Claude-3.5-Haiku）。
2. **性能-成本平衡**：设备-云协作框架相比纯云端大模型，性能下降很小（47.1% vs 56.5%，搭配 Gemini-2.5-Pro），但云调用成本显著降低。
3. **推理能力依赖基础模型强度**：对强模型（Gemini-2.5-Flash）加入推理可提升性能（22.5 → 36.2），但对弱模型（GPT-5-nano）反而有害（18.1 → 2.9），说明推理技术要求模型具备一定的基线能力。
4. **GRPO 的价值**：单独使用 GRPO（w/o SFT）比单独使用 SFT（w/o GRPO）效果更好，表明强化学习能独立学习有用策略；较大批量（150-160 vs 24-32）带来更稳定的训练和更高的成功率。
5. **设备-云协作的改进空间**：云端模型仍承担约 65% 的步骤，协作框架约减少 10% 的云调用——方向正确但仍有提升空间。
6. **效率优势**：3B 模型在单卡 RTX 3090 上比 7B 快约 50%，9B 模型无法在单卡运行；在真实移动设备更严苛的约束下，效率差距会进一步拉大。

---

## 7. 优点

- **问题定位精准**：识别出了移动 GUI 智能体的核心矛盾（设备端容量 vs 云端成本），并提出了实际可行的解决方案。
- **设备-云协作范式创新**：不同于传统的"设备端完成所有任务"或"云端完成所有任务"，通过实时复杂度评估动态切换，找到性能与成本的平衡点，具有较好的实用价值。
- **两阶段训练设计合理**：SFT 提供基础的推理和 GUI 能力，GRPO 直接优化任务目标（动作正确性），奖励设计细致（操作严格匹配／查询语义相似 + 格式惩罚），有效克服了小模型的训练难点。
- **记忆管理的工程智慧**：用文本摘要替代图像历史，以极低 token 代价保留长期上下文，解决了资源受限环境下的长上下文难题。
- **评估充分重视真实在线环境**：采用 AndroidLab 在线测试+自定义应用任务，比纯离线 checkpoint 评估更贴近实际部署。
- **丰富的消融与深层分析**：不仅报告主结果，还对训练组件、GRPO 变体、推理模式、设备-云各环节做了多层次剖析。

---

## 8. 不足与局限

- **对云端模型的依赖仍然很高**：设备-云协作中约 65% 的步骤仍由云端执行，云调用仅减少约 10%，距离"以设备端为主"的理想目标仍有差距。
- **小模型本身的性能天花板**：独立运行的 OpenPhone 在 AndroidLab 上仅 15.2% 成功率，距可用阈值（UI-Tars-7B 的 32.6%）仍有显著距离，在复杂任务上（财务类、导航类应用）表现接近失败。
- **推理技术不普适**：推理增强对弱模型（如 GPT-5-nano）反而造成显著性能下降，说明该方法的有效性依赖模型基线能力，适用范围有限。
- **训练算力未披露**：论文没有报告训练 GPU 配置和时长，削弱了可复现性和成本透明性。
- **训练数据规模有限**：仅用少量人工标注+合成数据训练，真实数据多样性和覆盖度可能不足，影响模型对未见应用的泛化。
- **评估覆盖有限**：仅测试安卓平台、9+4 个应用；iOS 生态、更多元化的应用类型未涉及。自定义任务数（25 个）偏少，结果可能有随机性。
- **无误差线/置信区间**：未报告多次独立运行的标准差，很难判断结果差异的统计显著性。
- **设备-云协作分析仅作观察描述**：约 10% 的云调用减少是在特定任务子集上的观察值，且未系统分析该削减在不同任务类型中的差异及相应的性能代价。

（完）
