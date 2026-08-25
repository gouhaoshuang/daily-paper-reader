---
title: "A3: Android Agent Arena for Mobile GUI Agents with Essential-State Procedural Evaluation"
title_zh: A3：移动GUI智能体安卓Agent竞技场与关键状态程序化评估
authors: "Yuxiang Chai, Shunye Tang, Han Xiao, Weifeng Lin, Hanhao Li, Jiayu Zhang, Liang Liu (陆亮), Pengxiang Zhao, Guangyi Liu, Guozhi Wang, Shuai Ren, Rongduo Han, Haining Zhang, Siyuan Huang, Hongsheng Li"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.184.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 提出了面向移动GUI智能体的基准测试与关键状态程序化评估方法
tldr: 现有移动GUI智能体评测多依赖静态帧或离线静态应用，难以反映动态真实在线应用中的表现。为此，论文提出A3（安卓Agent竞技场），采用基于关键状态的程序化评估方法，包含20个广泛使用应用中的100个任务。实验证明该评测能更有效地区分智能体在真实动态环境中的能力，为移动智能体评估提供了新基准。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl184/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1285, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl184/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 767, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl184/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 738, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl184/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1413, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl184/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1425, \"height\": 692, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1616, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 788, \"height\": 546, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1616, \"height\": 1111, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 779, \"height\": 1401, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1611, \"height\": 680, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1615, \"height\": 1137, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 790, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl184/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1664, \"height\": 1895, \"label\": \"Table\"}]"
motivation: 现有移动GUI智能体评测无法覆盖动态真实在线应用，静态评估存在明显不足。
method: 提出A3基准，基于关键状态的程序化评估系统，包含100个任务与20个应用。
result: 在动态真实应用上实现了更准确的性能评测，能更好区分智能体能力。
conclusion: 为移动GUI智能体的动态环境评估提供了标准化基准与评测范式。
---

## Abstract
The advancement of Large Language Models (LLMs) and Multimodal Large Language Models (MLLMs) has catalyzed the development of mobile graphic user interface (GUI) AI agents, which is designed to autonomously perform tasks on mobile devices. However, a significant gap persists in mobile GUI agent evaluation, where existing benchmarks predominantly rely on either static frame assessments such as AndroidControl or offline static apps such as AndroidWorld and thus fail to capture agent performance in dynamic, real-world online mobile apps. To address this gap, we present Android Agent Arena (A3), a novel "essential-state" based procedural evaluation system for mobile GUI agents. A3 introduces a benchmark of 100 tasks derived from 20 widely-used, dynamic online apps across 20 categories from the Google Play Store, ensuring evaluation comprehension. A3 also presents a novel "essential-state" based procedural evaluation method that leverages MLLMs as reward models to progressively verify task completion and process achievement. This evaluation approach address the limitations of traditional function based evaluation methods on online dynamic apps. Furthermore, A3 includes a toolkit to streamline Android device interaction, reset online environment and apps and facilitate data collection from both human and agent demonstrations. The complete A3 system, including the benchmark and tools, will be publicly released to provide a robust foundation for future research and development in mobile GUI agents.

---

## 论文详细总结（自动生成）

## 1. 核心问题与研究动机

- **背景**：LLM 与 MLLM 的进步推动了移动 GUI 智能体的发展，这类智能体直接通过屏幕像素感知环境并执行任务，无需依赖 API 或文本化界面。
- **现有评估方法的缺陷**：
  - **静态评估**（如 AITW、AndroidControl、AMEX）仅预测单步动作，无法反映真实环境中的动态状态变化和级联错误效应，也会误判合法的多样化解法路径。
  - **动态评估**（如 AndroidWorld、AndroidLab）依赖开源/离线应用，无法覆盖用户日常使用的购物、旅行、新闻等闭源在线应用；或存在环境不稳定、状态重置困难、人工评估成本高等问题。
- **核心研究问题**：如何在不依赖应用源码内部状态的前提下，对动态、在线、闭源的移动应用中的 GUI 智能体进行可靠、可扩展、细粒度的自动评估？

## 2. 方法论

- **核心思想**：提出"关键状态"（Essential-State）概念，即任务执行中必须达成的关键、可观察的语义里程碑。评估不再只做二元的最终成功/失败判定，而是将整个执行轨迹分解为一系列关键状态的渐进验证。
- **A3 基准**：
  - 从 Google Play 商店热门榜单中筛选 20 个类别、20 个广泛使用的动态在线应用（平均下载量 1.15 亿次）。
  - 设计了 100 个日常任务，按目标分为**操作型**（Operation）和**信息查询型**（Information Query）；按人类专家完成所需步数分为 Easy（N<7）、Medium（7≤N≤11）、Hard（N>11）三档难度。
- **关键状态定义协议**：通过三阶段人机协作流程确保标注质量——(1) 两名操作者用不同策略独立完成任务，生成多样成功轨迹；(2) 协同提出关键状态，满足"视觉可验证、关键性、充分性"三准则；(3) 独立审计员审核状态集的逻辑性、全面性与跨方法可达性。
- **评估指标**：
  - **ESAR**（Essential-State Achieved Rate）= 已达关键状态数 / 关键状态总数。
  - 任务总体成功判定：所有关键状态均达成时任务成功。
- **滑动窗口机制**：用预定义大小和间隔的窗口遍历轨迹中的屏幕帧序列，将窗口内帧组合成一张合成图，交由 MLLM 判断窗口内是否达成了某个关键状态。
- **MLLM 评判器**：
  - **商业模型方案**：采用 Gemini-2.5-pro 作为评判器。通过滑动窗口参数优化（实验得出窗口=4、间隔=2 为最优配置）在保真度和 API 成本之间取得平衡。
  - **开源模型方案（A3RM）**：基于 Qwen3-VL-8B 微调，使用 DAPO 强化学习算法训练，窗口大小为 2、间隔为 1。训练数据由 100 个任务各 3 条人类成功轨迹构成（981 个正样本、7260 个负样本），并用 Gemini 标注的智能体轨迹负样本挖掘（1083 个）增强判别能力。
- **AITK 工具包**：提供 Android 设备交互管理、环境重置、统一动作空间转换以及人类/智能体轨迹数据采集的完整流水线。

## 3. 实验设计

- **Benchmark**：A3 基准（100 任务，20 个动态在线应用，20 个 Google Play 分类）。
- **评估器对比**：Gemini-2.5-pro vs. 微调的 A3RM（Qwen3-VL-8B 基础模型）。
- **被测智能体**：
  - 7 个单模型智能体：Qwen2.5-VL-7B、Qwen3-VL-8B、UI-TARS-1.5-7B、UI-Genie-7B、UI-Venus-7B、InfiGUI-R1-3B、GUI-OWL-7B。
  - 2 个智能体框架：Mobile-Use（Qwen2.5-VL-7B）和 T3A（分别搭配 Gemini-2.5-pro 和 Qwen2.5-VL-7B）。
- **评估设置**：所有智能体使用官方公开提示词和推理设置，确保公平可复现。

## 4. 资源与算力

- 论文正文未详细说明全部实验的算力开销。
- 附录 A.8 提及 A3RM 训练使用 L40s（48G）GPU，共约 **600 GPU 小时**，基于 EasyR1 代码库和 DAPO 强化学习算法。
- 商业 MLLM（Gemini-2.5-pro）作为评估器的 API 调用成本在附录 A.3 中有详细分析（30 个任务的评估成本约为 0.05–0.196 美元，取决于窗口参数）。

## 5. 实验数量与充分性

- **主要实验**：在 A3 基准上评估了 9 种智能体配置，分别用 A3RM（表 3）和 Gemini-2.5-pro（附录表 6）评估，报告了 SR 和 ESAR，并按难度（Easy/Medium/Hard）和类型（操作/信息查询）分层分析。
- **消融实验**：滑动窗口大小与间隔的系统研究（窗口大小 2–6，间隔多档），验证了参数选择对评估准确率和成本的影响，并解释了小窗口导致上下文断裂、大窗口导致图像分辨率下降的问题。
- **泛化实验**：在 25 个新任务上测试 A3RM 的跨分布泛化能力，并与 Gemini 和继续训练版 A3RM-Continued 对比，验证关键状态表示的可扩展性。
- **案例研究**：分析了智能体的典型失败模式（进度无感知、屏幕误读、动态干扰等）。
- **客观性与公平性**：实验设计较为严谨——所有智能体采用官方设置与提示；A3RM 与 Gemini 双评估器互为参照，并揭示 Gemini 存在"乐观偏差"；滑动窗口研究覆盖了关键超参数的影响。需注意 A3RM 的训练数据来自 A3 任务本身，评估自家基准时存在一定的域内优势；泛化实验中 A3RM-Continued 额外使用了新任务数据，与 Gemini 的对比并非完全同等条件下的比较。

## 6. 主要结论与发现

- **A3 具有较强区分度**：最强系统（T3A + Gemini-2.5-pro）成功率仅 53%（A3RM 评估），表明当前智能体在动态在线应用场景中仍有巨大提升空间。
- **开源模型与商业模型差距显著**：开源单模型中 InfiGUI-R1 最优（SR 27.0%），但几乎是商业模型（53.0%）的一半。
- **框架能弥补基础模型不足**：Qwen2.5-VL 单独使用时仅 3.0% 成功率，嵌入 Mobile-Use 或 T3A 后分别提升至 16.0% 和 15.0%；但基础模型能力仍是性能上限，同一 T3A 框架换用 Gemini-2.5-pro 后飙升至 53.0%。
- **ESAR 普遍显著高于 SR**：说明当前智能体的主要失败模式不是无法开始任务，而是缺乏长程鲁棒性，难以稳定完成全部关键状态而不出现终止性错误。
- **A3RM 优于商业 MLLM**：在关键状态级别和任务级别均实现更高准确率（96.6% vs. 89.5%；98.0% vs. 95.0%），且无 API 成本、可本地部署。Gemini 存在"乐观偏差"（对未达成的状态产生幻觉性误判）。
- **关键状态表示具备可迁移性**：在新任务上 A3RM 仍优于 Gemini，继续训练后进一步提升，说明关键状态捕获了 GUI 任务执行中的可迁移结构规律。

## 7. 优点

- **生态效度高**：首次将广泛使用的商业在线应用（购物、旅行、新闻、导航等）纳入可复现的动态评估体系，解决了生态效度与可复现性之间的根本矛盾。
- **评估粒度精细且灵活**：ESAR 指标揭示部分成功与渐进进展，优于二元的 SR；关键状态基于高层语义而非 UI 元素细节，对界面变化和多样化路径具有鲁棒性。
- **成本可控**：商业模型自带滑动窗口参数优化；轻量级 A3RM 消除了每次评估 API 调用费用，兼具精度与可及性。
- **开源完整工具链**：AITK 提供统一动作空间、设备控制和轨迹采集模块；评估器与智能体无关，社区易于定制和采用。
- **严谨的标注流程**：三阶段人机协作协议（轨迹多样性、协同定义、独立审计）保障了关键状态定义的质量与客观性。
- **研究设计具有前瞻性**：MLLM-as-a-Judge 的"任务分解为关键状态"范式比直接端到端判断整条轨迹更可靠，为动态 GUI 评估指明了新方向。

## 8. 不足与局限

- **平台限制**：仅限于 Android 生态。iOS 因系统限制无法虚拟化和程序化控制，难以实现可复现测试。
- **应用覆盖盲区**：排除了即时通讯等高频类别，原因是严格的身份验证协议和隐私顾虑使自动化账号重置不可行。
- **A3RM 的假设性质**：A3RM 本质仍是概率模型，存在幻觉可能，高精度但不绝对可靠；且其针对 A3 分布优化，是专用模型而非通用评估器，在新领域中使用时需谨慎。
- **关键状态定义的人工成本和维护**：初始定义需要人工标注投入；虽然论文主张关键状态具有长期稳定性，但若应用的重大改版改变核心任务逻辑，仍可能需要重新标注。
- **域内评估的双重身份**：A3RM 在 A3 任务上训练又在 A3 基准上评估，存在过拟合基准的风险，其相对 Gemini 的优越性在完全陌生的任务分布上可能衰减（尽管泛化实验显示仍具优势）。
- **实验范围仍有限**：被测智能体主要来自开源社区；信息查询类任务在多数智能体上的成功率显著低于操作类任务，论文对此深层原因探讨尚不充分。

（完）
