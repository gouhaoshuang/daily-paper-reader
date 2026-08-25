---
title: "ProBench: Benchmarking GUI Agents with Accurate Process Information"
title_zh: ProBench：利用精确过程信息对GUI智能体进行基准测试
authors: "Leyang Yang, Ziwei Wang, Xiaoxuan Tang, Sheng Zhou, Dajun Chen, Wei Jiang, Yong Li"
date: 2026-03-17
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/39974/43935"
tags: ["query:mobile-agent"]
score: 8.0
evidence: 面向GUI智能体的过程级基准测试，可适用于移动GUI智能体框架
tldr: 现有GUI智能体基准往往只依据最终屏幕状态判断任务是否完成，忽略了中间步骤中的关键信息。ProBench提出一种能准确捕获过程信息的基准构建方法，将多步操作中的过程信息纳入评估。这使得对GUI智能体的评测更全面、更接近真实任务执行。该基准可直接用于移动GUI智能体框架的评估，帮助识别任务执行中的局部错误。
source: AAAI-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 850, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1843, \"height\": 653, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 845, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 751, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 859, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-39974/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 853, \"height\": 809, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-39974/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 842, \"height\": 495, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-39974/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 898, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-39974/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1736, \"height\": 828, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-39974/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 873, \"height\": 620, \"label\": \"Table\"}]"
motivation: 仅检查最终屏幕状态无法完整评估GUI智能体的多步任务执行能力。
method: 提出ProBench基准，通过自动捕获中间过程信息来评估GUI智能体，而非只看最终界面。
result: 实现更准确、细粒度的GUI智能体任务执行评估，弥补现有基准缺失。
conclusion: 为移动端及其他设备的GUI智能体提供了更可靠的过程级评估方案。
---

## Abstract
With the deep integration of artificial intelligence and interactive technology, Graphical User Interface (GUI) Agent, as the carrier connecting goal-oriented natural language and real-world devices, has received widespread attention from the community. Contemporary benchmarks aim to evaluate the comprehensive capabilities of GUI agents in GUI operation tasks, generally determining task completion solely by inspecting the final screen state. However, GUI operation tasks consist of multiple chained steps while not all critical information is presented in the final few pages. Although a few research has begun to incorporate intermediate steps into evaluation, accurately and automatically capturing this process information still remains an open challenge. To address this weakness, we introduce ProBench, a comprehensive mobile benchmark with over 200 challenging GUI tasks covering widely-used scenarios. 
Remaining the traditional State-related Task evaluation, we extend our dataset to include Process-related Task and design a specialized evaluation method. A newly introduced Process Provider automatically supplies accurate process information, enabling presice assessment of agent's performance. Our evaluation of advanced GUI agents reveals significant limitations for real-world GUI scenarios. These shortcomings are prevalent across diverse models, including both large-scale generalist models and smaller, GUI-specific models. A detailed error analysis further exposes several universal problems, outlining concrete directions for future improvements.

---

## 论文详细总结（自动生成）

# ProBench 论文总结

## 1. 核心问题与整体含义（研究动机和背景）

- GUI Agent 旨在将目标导向的自然语言指令与真实设备操作连接起来，已成为人工智能与交互技术交叉领域的重要研究方向。
- 现有 GUI 基准（如 AndroidArena、AndroidWorld、AndroidLab 等）普遍**仅依赖最终屏幕状态**判断任务是否成功，忽视了任务执行过程中的关键中间步骤。
- 作者以“购买最便宜的无线鼠标”为例说明：如果未执行“按价格排序”这一关键步骤，即使最终页面显示无线鼠标购买界面，任务实质上也是失败的；但传统评估会将其误判为成功。
- 已有研究工作开始考虑过程信息，如 SPA-Bench 通过预定义刚性步骤序列约束智能体，但忽略了规划能力评估且人工标注难以扩展；A3 依赖 LLM 分解任务，但准确性受限于 LLM 自身的分解能力。
- **核心贡献**：提出 ProBench，一个包含超过 200 个挑战性 GUI 任务、覆盖 34 个主流中英文移动应用的综合基准，能够**自动且准确地捕获过程信息**，从而对 GUI Agent 的中间操作过程进行有效评估。

## 2. 方法论：核心思想、关键技术细节、流程

### 2.1 总体框架
- ProBench 基于 adbutils（开源 Python ADB 库）搭建动态 Android 环境。
- 运行流程：实时截图 → 将截图、任务指令、历史操作记录传给 Agent → Agent 返回文本化操作 → ProBench 解析并转换为 ADB 设备控制命令 → 执行后获取新截图，循环直至 Agent 发出完成信号或达到最大步数。

### 2.2 任务构建（Task Curation）
- 以 SPA-BENCH 的应用列表为起点，剔除无法在虚拟设备上执行或具有反自动化机制的应用，最终保留 **34 个应用**（14 个英文、20 个中文），覆盖系统、生产工具、新闻阅读、旅行导航、购物金融、媒体娱乐、生活方式、社交共 8 类场景。
- 人工编写少量种子任务，再利用 Qwen3 生成候选任务，最后经人工筛选和编辑，保证任务正确性和多样性。
- 任务分为两种类型：
  - **State-related Task（状态相关任务）**：只需最终屏幕状态满足要求，如“查询支付宝当前余额”。
  - **Process-related Task（过程相关任务）**：必须执行特定中间操作，如“找到东京评分最高的寿司店并查看完整菜单”，仅看最终屏幕无法判断是否真正完成任务。

### 2.3 动作空间
- 继承 AITW 的基础动作：CLICK、SWIPE、TYPE、ENTER、BACK、COMPLETE。
- 移除 HOME 动作（任务限定在单一应用内）。
- 新增 WAIT 动作，应对网络加载延迟。

### 2.4 评估管线（Evaluation Pipeline）
- 最终结果分为三类：Uncompleted（达到步数上限未发完成信号）、Failure（发了完成信号但未满足要求）、Success（正确完成任务）。
- 对 State-related Task：仅用最终截图判断。
- 对 Process-related Task：引入 **Process Provider** 自动提供过程信息，包含两个可选组件：
  1. **Structure Description Converter**：每次点击后解析 a11y 树，定位包含点击坐标的最小可点击节点，提取 text、content-desc、resource-id（必要时补充子节点信息），生成动作的紧凑文本描述。
  2. **MLLM-based Summarizer**：将操作前后的截图合并并标出点击坐标，使用 MLLM 对比图像，生成操作的自然语言描述性摘要。
- 评估器（Judger）接收完整动作序列和最终截图，综合判断关键过程是否执行以及任务是否完成。
- 评估准确性验证（表 2）：State-related Task 正确率 96.0%；Process-related Task 配合 Structure Description Converter 为 89.7%，配合 MLLM-based Summarizer 为 94.1%。

## 3. 实验设计

### 3.1 数据集 / 基准
- 使用 ProBench 自身作为评测基准：200+ 任务、34 个中英文主流应用、双任务类型。
- 英文应用在 Android 模拟器上运行，中文应用在物理 Android 手机（配合 AdbKeyboard）上运行。
- 每次执行前手动清除应用历史数据，保证初始状态一致；每个任务最多允许 15 步交互。

### 3.2 对比模型
- **专有模型**：GPT-4o、Claude 4 Sonnet、Gemini 2.5 Pro。
- **通用开源模型**：Qwen2.5-VL-7B、Qwen2.5-VL-32B、Qwen2.5-VL-72B、InternVL3-8B。
- **GUI 专用模型**：UI-TARS-1.5-7B、UI-R1-E-3B、GUI-R1-3B。
- 未使用 Set-of-Mark 提示，模型直接输出坐标。
- 主实验中使用 Structure Description Converter 提供过程信息，评估器选用 Gemini 2.5 Pro。

## 4. 资源与算力

- 论文中**没有明确披露**训练或推理所使用的 GPU 型号、数量、训练时长等算力信息。
- 仅提及使用 Gemini 2.5 Pro 作为评估器和 Summarizer，使用 Qwen3 生成候选任务，以及运行环境为 Android 模拟器和物理手机。
- 因此，关于算力规模无法从文中获得具体细节。

## 5. 实验数量与充分性

- **实验数量**：
  - 主实验：9 个模型在中英文、State/Process 两类任务上的完整对比（表 3）。
  - 按应用类别的性能分析（图 5）：展示了 Gemini 2.5 Pro、Qwen2.5-VL-72B、UI-TARS-1.5-7B 在不同应用类别上的准确率。
  - 错误分析统计（表 4）：统计了失败任务中“未完成”的比例、以及“未完成”任务中被早期停止（连续 5 次相同操作）的比例。
  - 额外提供了三个典型错误案例（grounding 失败、历史操作不敏感、任务规划过度简化）。
  - 评估管线正确性验证（表 2）也构成了实验的一部分。
- **充分性评价**：
  - 优点：模型覆盖范围较广（专有/通用开源/GUI 专用），中英文任务、两类任务、类别分析、错误分析均有涉及。
  - 不足：缺少传统意义上的消融实验（例如评估器 MLLM 的选择对结果的影响、两种 Process Provider 组件在不同任务上的差异等）；没有人类基线对比；未报告统计显著性检验；任务规模为 200+，相对较小；主评估依赖单一 MLLM（Gemini 2.5 Pro），可能引入选择偏差。

## 6. 主要结论与发现

- 当前最先进的 GUI Agent 在 ProBench 上的成功率普遍偏低：**最好的 Gemini 2.5 Pro 平均准确率仅为 40.1%**，没有任何模型超过 50%。
- **State-related Task 的准确率普遍高于 Process-related Task**，说明考虑过程信息的任务对智能体提出了更高要求。
- 通用开源模型存在明显的**规模效应**：Qwen2.5-VL 系列随参数量增大稳步提升，72B 版本在英文任务上达到 53.3%，接近甚至超过专有模型。
- GUI 专用模型泛化能力有限：UI-R1-E-3B 因训练阶段缺乏 COMPLETE 动作示例而无法完成任何任务；UI-TARS-1.5-7B 虽在英文任务上强于其基础模型，但仍显著落后于大参数通用模型。
- 应用类别层面：智能体在**生产工具和系统应用**上表现较好，在**社交和生活方式类应用**上表现最差，原因是这类应用界面刷新频繁、信息碎片化、图标按钮多、广告干扰大。
- 错误分析揭示三大普遍问题：
  1. **接地能力不足**：GPT-4o、Claude 4 Sonnet 等无法准确点击目标元素，

1. **接地能力不足**：GPT-4o、Claude 4 Sonnet 等无法准确点击目标元素，表现为点击坐标偏移或点错相邻控件，尤其在图标密集、无文本标注的界面中失败率显著上升。
2. **历史操作不敏感**：部分模型（如 Qwen2.5-VL-7B）在连续操作中忽略自身之前的动作，导致重复点击同一位置、未形成有效推进，甚至陷入死循环。
3. **任务规划过度简化**：许多模型倾向于用最少的步骤直接尝试完成最终目标，而忽略关键中间过程（如跳过排序、筛选、进入详情页等），从而在 Process-related Task 上表现显著下降。

## 7. 局限性与未来方向

- **基准自身的局限性**：
  - 任务规模为 200+，相对于真实世界的 GUI 操作场景仍显有限，尤其缺少跨应用协作、多意图复合任务。
  - 过程信息的自动提取依赖于 a11y 树和 MLLM 摘要，在复杂动态界面（如视频播放、游戏界面）下可能丢失关键状态信息。
  - 评估器使用 Gemini 2.5 Pro 单一模型，对评估结果的稳定性和公平性存在潜在偏差。
  - 动作空间较为简化（6 种基础动作），未覆盖拖拽、长按、手势缩放、多指操作等真实交互行为。
- **模型评测层面的局限**：
  - 未设置人类基线，无法直观对比智能体与人类操作水平的差距。
  - 没有进行消融实验，无法清晰区分“模型自身能力”“过程信息提供方式”“评估器选择”等因素对最终结果的影响。
  - 未报告多次运行的方差或统计显著性检验，结论的稳定性有待验证。
- **未来方向**：
  - 拓展至更多语言、更多应用类型以及跨应用任务。
  - 改进过程信息捕获机制，使其在非标准 UI 下依然可靠。
  - 引入可扩展的自动化任务生成与验证流程，降低人工成本。
  - 探索将过程评估作为训练信号，引导 GUI Agent 学习关键中间步骤。

## 8. 总体评价

ProBench 是 GUI Agent 评估领域的扎实、有实用价值的贡献。它提出的“过程相关任务”概念以及自动化的过程信息捕获机制，弥补了以往基准只关注最终屏幕状态的缺陷，为后续研究提供了更严格的评测标准。实验设计覆盖面较广，模型对比和错误分析具有参考意义。但在任务规模、评估稳健性、消融深度和统计严谨性方面仍有提升空间。总体而言，该基准能够有效推动 GUI Agent 从“看起来成功”到“真正正确操作”的方向发展。

（完）
