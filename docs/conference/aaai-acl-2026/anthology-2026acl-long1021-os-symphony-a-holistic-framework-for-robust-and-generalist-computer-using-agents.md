---
title: "OS-Symphony: A Holistic Framework for Robust and Generalist Computer-Using Agents"
title_zh: OS-Symphony：鲁棒且通用的计算机使用智能体整体框架
authors: "Bowen Yang, Kaiming Jin, Zhenyu Wu, Zhaoyang Liu, Qiushi Sun, Zehao Li, JingJing Xie, Zhoumianze Liu, Fangzhi Xu, Kanzhi Cheng, Yian Wang, Qingyun Li, Yu Qiao, Zun Wang, Zichen Ding"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.1021.pdf"
tags: ["query:mobile-agent"]
score: 6.0
evidence: 面向计算机使用智能体的整体框架，结合视觉教程检索与记忆机制实现鲁棒自动化
tldr: 针对计算机使用智能体在陌生领域和长程任务中鲁棒性不足的问题，提出OS-Symphony框架，通过编排器协同反射记忆智能体与多功能工具智能体，并加入多模态教程检索与历史视觉上下文控制，实现轨迹级自我修正。实验表明该方法在跨域泛化和长程自动化中表现更优，为移动设备上的GUI智能体提供了可借鉴的整体架构。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 798, \"height\": 834, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1633, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1648, \"height\": 587, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 797, \"height\": 799, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 796, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1654, \"height\": 1168, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1620, \"height\": 1038, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1531, \"height\": 942, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 513, \"height\": 297, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 519, \"height\": 301, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 522, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 509, \"height\": 298, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 517, \"height\": 295, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 551, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1634, \"height\": 1008, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1391, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1021/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 658, \"height\": 305, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1662, \"height\": 1048, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 816, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 803, \"height\": 475, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 509, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1661, \"height\": 694, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1647, \"height\": 2371, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 811, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 789, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 459, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1659, \"height\": 521, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1647, \"height\": 467, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1661, \"height\": 508, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1021/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1590, \"height\": 333, \"label\": \"Table\"}]"
motivation: 现有计算机使用智能体在陌生领域和长程工作流中缺乏鲁棒性，视觉上下文管理不足。
method: 提出包含反射记忆智能体和多模态搜索工具智能体的整体框架，采用里程碑式长期记忆。
result: 在未知领域和长时期任务上提升了鲁棒性，弥补了视觉上下文丢失问题。
conclusion: 为通用计算机使用智能体的鲁棒自动化提供了系统化解决方案。
---

## Abstract
While Vision-Language Models (VLMs) have significantly advanced Computer-Using Agents (CUAs), current agentic frameworks struggle with robustness in novel domains and long-horizon workflows due to the absence of visual-aware tutorial retrieval and the lack of granular control over historical visual context curation and pruning. To bridge these gaps, we introduce OS-Symphony, a holistic framework that comprises an Orchestrator coordinating two key innovations for robust automation: (1) a Reflection-Memory Agent that utilizes milestone-driven long-term memory to enable trajectory-level self-correction, effectively mitigating visual context loss in long-horizon tasks; (2) Versatile Tool Agents featuring a Multimodal Searcher that adopts a “SeeAct” paradigm to navigate a browser-based sandbox to synthesize live, visually aligned tutorials, thereby resolving fidelity issues in unseen scenarios. Experimental results demonstrate that OS-Symphony delivers substantial performance gains across varying model scales, establishing new state-of-the-art results on three online benchmarks, notably achieving 65.84% on OSWorld. All research assets will be made publicly available.

---

## 论文详细总结（自动生成）

# OS-Symphony 论文详细总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究背景**：视觉语言模型（VLMs）的进步推动了计算机使用智能体（CUA, Computer-Using Agent）的发展，使智能体能够通过视觉感知与数字环境交互，实现通用自动化。
- **核心问题**：尽管现有CUA框架取得进展，但仍面临两大关键挑战：
  - **长程任务鲁棒性不足**：现有记忆模块缺乏对历史视觉信息的细粒度控制和裁剪，导致视觉上下文丢失，智能体难以识别意图漂移（intent drift）或循环行为等错误，无法生成有意义的反思来优化规划。
  - **新领域泛化能力弱**：现有RAG方法要么过度依赖单模态（文本）信息，忽略视觉模态的关键语义线索；要么依赖本地知识库，维护成本高且难以适应新软件，无法在分布外（OOD）任务上实现稳健泛化。
- **论文含义**：提出了OS-Symphony整体框架，通过编曲者（Orchestrator）协调反射记忆智能体与多功能工具智能体，系统性地解决上述两大问题，为构建鲁棒且通用的CUA提供了整体解决方案。

## 2. 方法论：核心思想、关键技术细节与算法流程

### 2.1 整体架构

OS-Symphony由三大核心组件构成：

- **Orchestrator（编曲者）**：系统的“大脑”，负责任务理解、协调所有工具智能体并最终选择动作。其决策过程形式化为：`tᵢ, aᵢ = F_O(I, Rᵢ, oᵢ, T, H_short)`，其中Rᵢ是RMA提供的反思反馈，H_short是最近K轮的短期记忆滑动窗口。

### 2.2 Reflection-Memory Agent（RMA，反射记忆智能体）

- **Step-Level Summary（步骤级摘要）**：利用辅助VLM对上一动作进行总结和正确性验证，形式化为 `Sᵢ, sᵢ = F_S(Oᵢ₋₁, oᵢ₋₁, oᵢ, õᵢ₋₁)`，其中õ是对动作区域的局部放大图。
- **Milestone-Driven Long-Term Memory（里程碑驱动的长期记忆）**：构建 `H_long = {(Sⱼ, oⱼ, mⱼ)}`，仅当里程碑标记mⱼ为真时才保留对应截图，兼顾信息保留与上下文压缩。
- **Trajectory-Level Reflection（轨迹级反思）**：RMA执行三项核心功能：里程碑识别、轨迹级反思生成、从视觉输入中提取相关信息。反思遵循结构化消息协议，将执行状态分为四类：
  - **On-track**（正常进行）
  - **Completed**（任务完成）
  - **Infeasible**（任务不可行）
  - **Off-track**（偏离轨迹），细分为四种错误类型：
    - GUI Error（GUI操作错误）：步骤级动作未达预期效果
    - Lack of Tutorial（缺乏教程）：随机动作或重复循环表明需要外部指导
    - Code Error（代码错误）：Coder执行与实际GUI状态不匹配
    - Other Error（其他错误）：如意图漂移
- **循环检测算法**：设计了基于相似度规则的循环检测算法 `D_loop(H, N)`，采用pHash+SSIM的级联验证策略和多种动作相似度度量。

### 2.3 Versatile Tool Agents（多功能工具智能体）

- **Multimodal Searcher（多模态搜索器）**：核心创新之一。
  - 采用VLM驱动的**See-Act范式**，在隔离的浏览器沙盒环境中导航网页。
  - 动作空间限制为 `A_search = {click, type, scroll} ∪ {done, fail}`，降低搜索复杂度。
  - 仅在执行暴露知识缺口时按需调用，避免污染主环境上下文。
  - 将访问内容提炼为结构化分步教程T，并永久附加到Orchestrator上下文。
- **Grounders（定位器）**：
  - General Grounder（通用定位器）：整合低层视觉线索（位置、外观）和高层语义上下文（功能、相关性）
  - OCR-based Grounder（OCR定位器）：针对文本密集型应用（如PowerPoint、Word），构建{text, id, bbox}结构化表格。
- **Coder（代码智能体）**：处理大规模表格操作、文件编辑等细粒度任务，遵循“定位→检查→修改→验证”的严格内部工作流，执行后由Orchestrator通过GUI状态检查验证。

## 3. 实验设计：数据集、基准与对比方法

- **主要基准（OSWorld-Verified）**：369个真实世界任务，覆盖Ubuntu环境中五个领域（OS、Chrome、GIMP、LibreOffice套件、Thunderbird、VSCode、VLC等），排除8个Google Drive任务后为361个任务。
- **跨平台基准**：
  - WindowsAgentArena：154个任务，涵盖Office、Web、System、Code、Media、Utilities等领域
  - MacOSArena：63个任务，涵盖单应用与多应用场景
- **对比方法**：
  - 通用模型：Qwen3-VL系列（8B/32B Instruct与Thinking变体）
  - 专用模型：UI-TARS、UI-TARS-2、DeepMiner-Mano、OpenCUA等
  - Agentic框架：Agent S3、CoAct-1、GTA1、UiPath等
  - 以Agent S3和CoAct-1为主要基线（相似动作空间）
- **模型配置**：基于GPT-5、GPT-5-Mini、Qwen3-VL系列；Grounder使用UI-TARS-1.5-7B和EasyOCR；温度设为0.1。

## 4. 资源与算力

- 论文**未明确说明**具体GPU型号、数量或训练时长。
- 间接透露的信息：
  - Claude-Sonnet-4.5因推理成本高昂仅在Workflow领域测试（约500美元）
  - GPT-5配置约150美元，GPT-5-Mini约30美元，开源模型为0美元（本地部署）
  - 平均每任务token消耗约550k，平均延迟约653.7秒
  - 未涉及模型训练，主要聚焦于推理阶段的框架设计

## 5. 实验数量与充分性分析

### 5.1 实验数量

- **主实验**：三大基准上的多模型、多步数限制系统评估
- **消融实验**（GPT-5-Mini + UI-TARS-1.5-7B，50步限制）：
  - 搜索模块消融：w/o Search、w/o Search+Refl、Unimodal Search、Multimodal Search
  - 反思与记忆消融：w/o Reflection、Refl w/ STM、Refl w/ LTM
- **扩展分析**：
  - Pass@K结果（Pass@1至Pass@5）
  - 不同基于VLM的影响（Qwen3-VL系列8B/32B、Claude-Sonnet-4.5、GPT-5、GPT-5-Mini）
  - 不同Grounder配置对比（UI-TARS-1.5-7B、GTA1-32B、ScaleCUA-32B、Holo2-30B）
  - 指令重写影响、Coder消融、视觉上下文长度敏感性
  - 成本与延迟分析、消息协议统计、动作使用统计

### 5.2 充分性与客观性评估

- **优点**：实验覆盖广泛，包含跨平台（3个OS）、跨模型规模（8B到前沿模型）、多维度分析，消融实验设计规范，并辅以人工验证（如RMA输出与真实状态的100步人工核对）和案例研究。
- **不足之处**：
  - 部分基线结果为复现或引用，可能有环境差异
  - MacOSArena上未测试GPT-5（成本限制），对比不够完整
  - 基准的环境限制可能无法代表真实世界使用场景
- **整体评价**：实验设计较为全面，消融实验充分验证了各组件的独立贡献，各分析维度相互补充，在一定程度上保证了客观性和公平性。

## 6. 主要结论与发现

- **SOTA性能**：在三个基准上均取得新最佳成绩——OSWorld 65.84%（100步）、WindowsAgentArena 63.5%、MacOSArena 46.03%。
- **框架增益显著**：相比原生模型，Qwen3-VL-32B-Instruct相对提升约45%，GPT-5-Mini配置超越更强大的Agent S3（GPT-5）。
- **RMA是关键**：在Workflow（多应用长程任务）领域增益最大（优于基线约7%），可有效防止错误累积，提升时间稳定性。
- **多模态搜索有效**：对知识密集域（Daily）提升显著，对小模型的补偿效应尤为突出——GPT-5-Mini调用Searcher频率比GPT-5高34倍。
- **小模型民主化**：GPT-5-Mini配置与Agent S3（GPT-5）仅差约3%，成本降低约80%，展示出极高性价比。
- **模式洞察**：nave Last-K反思（STM）甚至不如无反思，说明不恰当的反思机制可能适得其反。
- **Pass@5达79.4%**：超过人类基线（72.4%），说明模型具备解决问题的高潜力，但缺乏一致性。

## 7. 优点与亮点

- **视觉中心的设计理念**：突破纯文本RAG局限，首创将多模态搜索作为工具集成到CUA框架中，通过See-Act范式主动导航网页合成高保真教程，与执行状态实时对齐。
- **里程碑式记忆机制**：利用截图的时间冗余性，仅保留关键里程碑截图，在保证信息完整性的同时有效压缩上下文，缓解了长程任务的上下文过载问题。
- **结构化反思协议**：消息协议将执行状态细分为九种类型，配合规则辅助的循环检测和步骤级验证，形成可解释的错误诊断与修正机制。
- **模块化解耦设计**：将推理、定位、执行分离到不同智能体，降低基于VLM的多任务认知负担，使小模型也能取得显著提升。
- **丰富的实验分析**：包含跨平台、跨模型、跨组件配置的系统评估，以及成本、延迟、消息协议分布等多维度统计分析，对社区有较高参考价值。
- **可复现性**：代码和项目已公开。

## 8. 不足与局限

- **环境泛化局限**：仅在桌面环境验证，移动平台（Android/iOS）因动作空间差异而未覆盖，跨平台普适性有待验证。
- **视觉感知粒度瓶颈**：RMA在细微视觉线索（如高亮、重叠窗口）上存在感知盲区，导致误报/漏报，在视觉复杂域中甚至劣于无RMA基线。
- **规划与执行信息瓶颈**：Orchestrator与Grounder之间的文本语义传达存在信息瓶颈（如“边界”等视觉属性难以精确描述），需依赖端到端方案突破。
- **推理随机性**：任务级结果波动显著（Pass@1与Pass@5差距达14%），部署稳定性不足，抑制了实际应用价值。
- **结构复杂性与效率**：多智能体系统引入较高延迟和token消耗（平均缩短记忆后仍需每任务约550k tokens、延迟约654秒），实用性受限。
- **实现细节依赖现成组件**：记忆机制依赖传统摘要范式，搜索器可能被更强大的商业搜索引擎替代，部分组件为当前实现选择而非长期方案。
- **评估缺陷**：基准中不可行任务的评估容易被滥用（模型在步数耗尽时输出fail即可得分），可能高估实际能力；部分失败源于指令歧义或评估函数过严而非智能体缺陷。
- **安全与隐私风险**：视觉智能体天然处理敏感截图像流，存在提示注入攻击风险和双重用途滥用可能，实际部署需多层防护。

（完）
