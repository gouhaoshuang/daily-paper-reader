---
title: "EcoAgent: An Efficient Device-Cloud Collaborative Multi-Agent Framework for Mobile Automation"
title_zh: EcoAgent：一种高效的设备-云协作移动自动化多智能体框架
authors: "Biao Yi, Xueyu Hu, Yurun Chen, Shengyu Zhang, Hongxia Yang, Fan Wu"
date: 2026-03-17
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/40230/44191"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 面向移动自动化的设备-云端协作多智能体框架
tldr: 现有移动多智能体系统多在云端部署，带来高时延、高成本与隐私问题。EcoAgent提出一种闭环设备-云协作多智能体框架，将云端验证改为设备侧协同，避免上传移动截图，并通过设备到云端的反馈闭环充分利用端侧资源。该框架在降低时延和成本的同时保护了用户隐私，为移动自动化提供了更高效的多智能体协作方案。
source: AAAI-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40230/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1842, \"height\": 927, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40230/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1804, \"height\": 741, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40230/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1838, \"height\": 1043, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40230/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 875, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40230/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1800, \"height\": 591, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40230/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 817, \"height\": 514, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40230/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1548, \"height\": 416, \"label\": \"Table\"}]"
motivation: 云端多智能体部署导致高时延、成本高且泄露用户隐私。
method: 提出闭环设备-云协作框架，避免截图上传并引入设备反馈。
result: 显著降低时延和成本，增强隐私保护。
conclusion: 为移动自动化提供了一种高效且隐私友好的多智能体协作范式。
---

## Abstract
To tackle increasingly complex tasks, recent research on mobile agents has shifted towards multi-agent collaboration. Current mobile multi-agent systems are primarily deployed in the cloud, leading to high latency and operational costs. A straightforward idea is to deploy a device–cloud collaborative multi-agent system, which is nontrivial, as directly extending existing systems introduces new challenges: (1) reliance on cloud-side verification requires uploading mobile screenshots, compromising user privacy; and (2) open-loop cooperation lacking device-to-cloud feedback, underutilizing device resources and increasing latency. To overcome these limitations, we propose EcoAgent, a closed-loop device-cloud collaborative multi-agent framework designed for privacy-aware, efficient, and responsive mobile automation. EcoAgent integrates a novel reasoning approach, Dual-ReACT, into the cloud-based Planning Agent, fully exploiting cloud reasoning to compensate for limited on-device capacity, thereby enabling device-side verification and lightweight feedback. Furthermore, the device-based Observation Agent leverages a Pre-understanding Module to summarize screen content into concise textual descriptions, significantly reducing token usage and device-cloud communication overhead while preserving privacy. Experiments on AndroidWorld demonstrate that EcoAgent matches the task success rates of fully cloud-based agents, while reducing resource consumption and response latency.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）

- **研究背景**：随着（多模态）大语言模型（(M)LLMs）的快速发展，基于 LLM 的移动智能体（mobile agents）成为人机交互领域的研究热点。近年来，移动智能体的研究趋势逐渐从单智能体转向**多智能体协作**，通过将规划、执行、反思等任务分配给不同智能体，以应对日益复杂的移动操作任务。
- **核心问题**：现有移动多智能体系统主要部署在云端，由此产生三大弊端：
  - **高延迟**：每次屏幕理解和决策都需要经过云端的远程通信，响应速度慢；
  - **高运营成本**：大规模调用云端 MLLM 产生大量 token 消耗和计算费用；
  - **隐私泄露风险**：云端验证需要频繁上传移动设备截图，用户的敏感信息面临泄露风险。
- **现有方案的不足**：直接将端云协作扩展到多智能体系统存在两个难以逾越的挑战：
  1. **依赖云端验证**：设备侧缺乏足够的推理能力来判断操作是否成功，仍需上传截图到云端，既增延迟又泄露隐私；
  2. **开环协作**：现有设备-云协作系统（如 UGround）多为单向的“云端→设备”指令流，缺少设备到云端的反馈回路，未充分利用端侧资源，导致延迟和成本仍然偏高。
- **核心贡献**：提出 **EcoAgent**——一个**闭环（closed-loop）设备-云协作多智能体框架**，在保持任务成功率的同时，显著降低延迟、成本和隐私风险，在效率与能力之间取得了较好的平衡。

## 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

### 2.1 整体架构

EcoAgent 由三个智能体组成，形成闭环协作：
- **云端 Planning Agent**（规划智能体）：基于 MLLM（GPT-4o），负责任务分解、动作规划与失败重规划，承担强推理任务；
- **设备端 Execution Agent**（执行智能体）：基于微调的小规模多模态语言模型（MSLM，如 ShowUI 2B / OS-Atlas-Pro 4B），负责在设备上执行具体的 UI 操作；
- **设备端 Observation Agent**（观察智能体）：基于通用 MSLM（Qwen2-VL-2B），负责验证每个步骤的执行结果，并将屏幕内容压缩为文本描述。

### 2.2 关键技术一：Dual-ReACT 规划机制

- 这是对经典 **ReACT**（Reasoning + Acting）框架的扩展，在**全局（global）**和**局部（local）**两个层级上分别应用 ReACT 推理；
- **全局 ReACT**：根据用户指令和初始屏幕，将复杂任务分解为多个中间子目标，生成高层执行计划；
- **局部 ReACT**：针对每个子目标，进一步推理得出具体的执行步骤（ST）和对应的预期结果（EX）。
- 初始计划形式化为：  
  P₀ = GlReACT(Ins, S₀) = {LoReACT(ST₁, EX₁), ..., LoReACT(STₜ, EXₜ)}
- **核心意义**：每个步骤都附带明确的“预期结果”，这使得设备端可以执行轻量级的验证任务（将屏幕内容与预期描述进行比对），而无需复杂的推理能力——把复杂的任务分析转化为简单的判断问题，充分发挥云端强推理能力为弱小的端侧模型“减负”。

### 2.3 关键技术二：Memory（记忆）+ Reflection（反思）重规划

- 执行失败时，规划智能体启动**记忆驱动的反思重规划**过程：  
  Pₙ = Reflection(Ins, Pₙ₋₁, Memory)
- **记忆模块**存储屏幕状态（压缩后的文本描述）和动作执行轨迹，作为反思模块的上下文输入；
- **反思模块**分析错误轨迹，自适应地修订任务计划，生成新的执行方案，直至任务成功完成。

### 2.4 关键技术三：Pre-Understanding Module（预理解模块）

- 位于 Observation Agent 中，将原始屏幕截图转换为**简洁的文本描述**：
  - 单张截图在 MLLM 中通常消耗 **1400+ tokens**；
  - 经过压缩后的文本描述仅需 **50–150 tokens**，压缩幅度超过 90%；
- 一举三得：
  1. **降低通信开销**：设备到云端的传输数据量大幅减少；
  2. **降低 MLLM 消耗**：云端的 token 成本大幅下降；
  3. **保护隐私**：不再上传原始截图，而只上传语义级文本描述，降低隐私泄露风险。

### 2.5 扩展动作空间

- 在原有输入操作（Tap、Swipe、LongPress、InputText、OpenApp）基础上，新增 **DeleteText()** 操作，用于清空当前聚焦输入框的全部内容，解决了已有移动智能体无法有效删除误输入文本的问题，特别有助于重命名类任务的成功执行。

### 2.6 完整算法流程（文字描述）

1. **初始规划**：云端 Planning Agent 基于用户指令和初始屏幕执行 Dual-ReACT，生成包含步骤和预期结果的初始计划 P₀；
2. **循环执行与观察**：对计划中的每一步：
   - 设备端 Execution Agent 根据当前屏幕和步骤描述执行操作；
   - 设备端 Observation Agent 将执行后的屏幕与预期结果比对，给出成功/失败判断；
   - 同时将屏幕经过 Pre-Understanding 压缩后存入记忆模块；
   - 若失败，则触发规划智能体的反思重规划，生成新计划并重新执行；
3. **任务完成**：所有步骤成功执行后，返回最终系统状态。

## 3. 实验设计：数据集、Benchmark 与对比方法

### 3.1 Benchmark

- 使用 **AndroidWorld** 动态基准测试环境，包含 **116 个程序化任务**，覆盖 **20 个真实 Android 应用**；
- 运行环境：Pixel 6 设备模型 + Android 13（API Level 33）的实时模拟器；
- 选择 AndroidWorld 的原因：该基准提供**完全程序化的评估**（无需人工判断），可复现性、可扩展性和评估效率均优于依赖人工评估的 MobileAgentBench 和 AndroidLab。

### 3.2 对比基线（涵盖四类架构）

| 架构类型 | 对比方法 |
|---------|----------|
| 设备端单智能体 | ShowUI (2B)、InfiGUIAgent (2B)、OS-Atlas (4B)、V-Droid (8B) |
| 云端单智能体 | AppAgent (GPT-4o)、MobileAgent |
| 云端多智能体 | M3A（GPT-4o×2）、Agent S2（GPT-4o×4） |
| 开环设备-云协作 | UGround-V1-2B、UGround-V1-7B（均为 GPT-4o + 设备端模型） |
| 闭环设备-云协作（本文） | EcoAgent（ShowUI）、EcoAgent（OS-Atlas） |

- **公平性保障**：所有基线的云端智能体均使用 GPT-4o，EcoAgent 的规划智能体也用 GPT-4o；执行智能体分别集成当前最先进的设备端模型 ShowUI (2B) 和 OS-Atlas-Pro (4B)；观察智能体基于 Qwen2-VL-2B。

### 3.3 评估指标

- **任务成功率（SR）**：成功完成任务的百分比；
- **运营成本**：平均 MLLM 调用次数（MC）和平均 MLLM Token 消耗量（MT）；
- **端到端延迟**：每个执行步骤的平均耗时。

## 4. 资源与算力

- **论文未明确说明**训练或评估过程中使用的 GPU 型号、数量或具体训练时长；
- 可推断的信息：
  - 云端规划智能体使用了 **GPT-4o**（闭源 API 服务）；
  - 设备端执行模型（ShowUI、OS-Atlas）和观察模型（Qwen2-VL-2B）为**已有的预训练/微调模型**，论文未报告对执行模型进行二次微调的算力成本；
  - 实验主要关注**推理阶段**的成本（MLLM 调用次数和 token 消耗），而非训练阶段的算力开销。

## 5. 实验数量与充分性

### 5.1 实验组数

论文进行了三大类实验：

1. **主实验**：在 AndroidWorld 上与 10+ 个基线方法进行任务成功率、运营成本、延迟三个维度的对比；
2. **消融实验**：针对两种执行模型（ShowUI 和 OS-Atlas），分别设置三组配置——仅执行智能体（Executor）、执行+规划智能体（Executor + Planner）、完整三智能体（Executor + Planner + Observer），共 **6 组消融实验**；
3. **成本与延迟对比实验**：对各架构代表方法的 MC、MT 和延迟进行了量化对比。

### 5.2 充分性与客观性评估

**充分的方面**：
- 覆盖了四种主流架构类型（设备端、云端单/多智能体、开环端云协作、闭环端云协作），对比范围较全面；
- 消融实验清晰地验证了每个组件（Planning Agent、Observation Agent、Dual-ReACT、Pre-Understanding Module）的独立贡献；
- 使用 AndroidWorld 的程序化评估，避免了人工评估的主观偏差和可复现性问题；
- 报告了效率和成本指标，跳出了“只看成功率”的传统评价框架。

**尚可加强的方面**：
- 仅在 AndroidWorld 单一基准上评估，缺乏跨基准（如 MobileAgentBench、AndroidLab）的泛化验证；
- 任务成功率（25.6% / 27.6%）距离最强基线 V-Droid（59.5%）仍有较大差距，论文将其归因于“架构正交、未来可结合”，但该论述需要更多实验证据支撑；
- 未报告多次运行的标准差/置信区间，统计显著性不明；
- 基线数量充分，但部分基线（如 AutoDroid、CogAgent）仅出现在延迟对比表中，未参与成功率对比，对比表之间的覆盖率不完全一致。

## 6. 主要结论与发现

- **效果达成**：EcoAgent 在 AndroidWorld 上取得 25.6%（ShowUI）和 27.6%（OS-Atlas）的成功率，超越所有单智能体基线，与云端多智能体系统 M3A（28.4%）持平，且显著高于开环端云协作方案 UGround（32.8% 和 44.0% 为 UGround 本身结果，EcoAgent 在更低成本下达接近水平）；
- **成本显著下降**：与云端单智能体 AppAgent 相比，MC 降低 76%、MT 降低 79%；与云端双智能体 M3A 相比，MC 降低 89%、MT 降低 96%；与开环的 UGround-V1-2B 相比，MC 降低约 85%、MT 降低约 93%；
- **延迟大幅优化**：EcoAgent（ShowUI）的平均步延迟为 **3.9 秒**，显著低云端多智能体（M3A 为 15.3 秒、MobileAgent 为 15.9 秒）和开环端云协作（UGround 为 18.2 秒）；
- **组件有效性**：消融实验表明：
  - 单独使用执行智能体效果差（SR 仅 4.3%–7.0%）；
  - 加入 Dual-ReACT 规划智能体后，SR 提升至 15.5%–19.0%（约 2–4 倍提升）；
  - 加入带有 Pre-Understanding 的观察智能体后，SR 进一步提升至 25.6%–27.6%，而 MC 和 MT 的增加幅度趋于适度（MC 从 1 增至 1.5–1.9，MT 从约 2100 增至 3200–3500），说明闭环协作的成本代价是被有效控制的。

## 7. 优点

- **问题定位精准**：精准识别了现有端云协作移动智能体的两大痛点——云端验证的隐私风险和开环协作的效率损失，问题定义清晰且实际价值高；
- **Dual-ReACT 设计巧妙**：通过“全局规划 + 局部推理+预期结果生成”的两阶段推理范式，将云端强推理能力转化为设备端可执行的轻量验证任务，实现了推理能力与端侧资源约束之间的优雅平衡；
- **预理解模块兼顾效率与隐私**：将截图压缩为极简文本描述（1400+ tokens → 50–150 tokens），同时解决了 token 成本、通信延迟和隐私保护三个问题，是方法中最具工程价值的创新；
- **闭环设计理念先进**：设备到云端的反馈回路使系统具备自纠错能力（失败触发反思重规划），远超现有开环方案，代表了端云协作移动智能体的正确演进方向；
- **成本-效果综合考量**：评估不只关注成功率，还系统报告了成本和延迟，为实际部署提供了可量化的决策依据；
- **资源需求低、部署可行性高**：设备端模型仅需 2B–4B 参数规模，使用业界已有开源模型即可搭建，实用性较强；与强执行模型（如 V-Droid）正交，未来有进一步提升的空间。

## 8. 不足与局限

- **成功率差距明显**：EcoAgent 的绝对成功率（25.6%–27.6%）虽然超越了多数基线，但与最强设备端模型 V-Droid（59.5%）仍存在约 30 个百分点的大幅差距。论文以“未来可将 V-Droid 作为执行智能体”作为辩护，但这种正交性和增益尚未经过实证验证；
- **单一基准评估**：仅在 AndroidWorld 一个基准上进行实验，未在 MobileAgentBench、AndroidLab 等其他主流基准上验证，泛化性说服力有限；
- **缺乏统计显著性分析**：未报告多次实验的标准差、置信区间或显著性检验，无法判断不同配置之间的性能差异是否具有统计显著性；
- **隐私保护的相对性**：虽然预理解模块避免上传原始截图，但文本描述仍可能包含高敏感语义内容（如应用名称、搜索关键词、通信内容），是否构成充分的隐私保护仍值得商榷；
- **依赖特定云模型**：规划智能体依赖 GPT-4o 级别的云端能力，如果替换为更弱的云端模型，Dual-ReACT 的规划质量和反思能力可能显著下降，方法的鲁棒性未做评估；
- **延迟统计口径不统一**：不同基线的延迟数据可能来自不同硬件/网络环境（如设备端模型的推理延迟依赖具体设备），直接比较存在一定的公平性偏差风险；
- **未报告算力细节**：缺少对设备端模型的微调资源消耗、推理时端侧算力占用以及云端 API 调用时间分布的具体分析，限制了对其真实部署成本的精确评估；
- **实验视角偏研究原型**：AndroidWorld 的模拟器环境与真实用户设备之间存在差异，真实场景中的碎片化设备生态、系统版本差异、应用状态多样性等因素未在实验中覆盖.

## 总结一句话

EcoAgent 通过**闭环端云协作 + 双层级 ReACT 规划 + 屏幕预理解压缩**三重机制，在任务成功率与云端多智能体系统基本持平的前提下，将 MLLM 调用次数降低 89%以上、token 消耗降低 96%以上、步延迟降至 3.9 秒，为隐私敏感、成本敏感的移动自动化应用提供了切实可行的新范式。但其单基准验证、成功率偏低和缺乏统计显著性分析等问题仍需后续工作加以解决。

（完）
