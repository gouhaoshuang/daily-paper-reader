---
title: "Agent-SAMA: State-Aware Mobile Assistant"
title_zh: Agent-SAMA：状态感知的移动助手
authors: "Linqiang Guo, Wei Liu, Yi Wen Heng, Tse-Hsun (Peter) Chen, Yang Wang"
date: 2026-03-17
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/40187/44148"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 基于有限状态机的状态感知多智能体框架，用于移动GUI智能体构建
tldr: 现有移动GUI智能体仅基于当前屏幕反应式推理，缺乏应用导航流程的结构化表示，难以理解执行上下文和从错误中恢复。论文提出Agent-SAMA，将应用执行建模为有限状态机，把UI屏幕视为状态、用户动作视为迁移，并通过四个专门智能体协作构建和使用状态表示。该方法增强了移动智能体的执行上下文理解与错误恢复能力，提高了任务自动化性能。
source: AAAI-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40187/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1530, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/aaai-2026-accepted/aaai-2026-40187/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1721, \"height\": 502, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40187/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 658, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40187/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 713, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40187/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 684, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40187/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/aaai-2026-accepted/aaai-2026-40187/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1263, \"height\": 244, \"label\": \"Table\"}]"
motivation: 移动GUI智能体缺乏应用导航流程的结构化表示，导致上下文理解不足和错误恢复困难。
method: 提出Agent-SAMA，用有限状态机建模应用执行，四个专门智能体协作构建并使用状态信息。
result: 在移动任务上增强了执行上下文理解，提升了错误检测与恢复能力。
conclusion: 为移动GUI智能体提供状态感知框架，显著改善任务的自主完成能力。
---

## Abstract
Mobile Graphical User Interface (GUI) agents aim to autonomously complete tasks within or across apps based on user instructions. While recent Multimodal Large Language Models (MLLMs) enable these agents to interpret UI screens and perform actions, existing agents remain fundamentally reactive. They reason over the current UI screen but lack a structured representation of the app navigation flow, lim-
iting GUI agents’ ability to understand execution context, detect unexpected execution results, and recover from errors. We introduce Agent-SAMA, a state-aware multi-agent framework that models app execution as a Finite State Machine (FSM), treating UI screens as states and user actions as transitions. Agent-SAMA implements four specialized agents that collaboratively construct and use FSMs in real time to guide task planning, execution verification, and recovery. We evaluate Agent-SAMA on two types of benchmarks: cross-
app (Mobile-Eval-E, SPA-Bench) and mostly single-app (AndroidWorld). On Mobile-Eval-E, Agent-SAMA achieves an 84.0% success rate and a 71.9% recovery rate. On SPA-Bench, it reaches an 80.0% success rate with a 66.7% recovery rate. Compared to prior methods, Agent-SAMA improves task success by up to 12% and recovery success by 13.8%. On AndroidWorld, Agent-SAMA achieves a 63.7%
success rate, outperforming the baselines. Our results demonstrate that structured state modeling enhances robustness and can serve as a lightweight, model-agnostic memory layer for future GUI agents.

---

## 论文详细总结（自动生成）

# Agent-SAMA：状态感知的移动助手 — 论文详细总结

## 1. 核心问题与研究动机

- **背景**：多模态大语言模型（MLLM）驱动的移动 GUI 智能体（如 Mobile-Agent 系列）能够根据用户指令在应用内或跨应用自动执行任务（如“用 Chrome 搜索冬奥会开幕日期，并在日历中设置提醒”）。
- **核心问题**：现有 GUI 智能体本质上是**反应式（reactive）**的——它们只基于当前 UI 屏幕推理下一步动作，**缺乏对应用导航流程的结构化表示**。论文用“游客逐街行走却没有城市地图”来类比——智能体知道自己到过哪里，却不理解各页面之间如何连通，因此难以：
  - 理解执行上下文；
  - 检测意外执行结果（如页面跳转异常）；
  - 从错误中有效恢复。
- **研究意义**：如果能把 UI 屏幕视为“状态”、用户动作视为“状态迁移”，构建结构化的导航模型，就能让智能体具备状态感知能力，提升任务完成率和错误恢复率。

## 2. 方法论：基于 FSM 的状态感知多智能体框架

### 核心思想

将移动应用执行建模为**有限状态机（FSM, Finite State Machine）**：
- **状态（S）**= 不同 UI 屏幕（以自然语言描述表示）；
- **迁移（T）**= 用户动作（点击、滑动、输入等）触发的状态转换；
- 形式化定义为 M = (S, A, T, s₀, G)，其中 s₀ 为初始状态，G 为子任务目标状态。

### 四个执行阶段与六个协作智能体

**（1）规划阶段 — Planner Agent**
- 将用户指令分解为带理由的子任务序列 π = [(g₁, r₁), (g₂, r₂), …]；
- 生成 **5 个候选计划**，再用 **LLM-as-judge** 按评估准则（目标相关性、执行效率、鲁棒性、清晰度）选出最优计划；
- 可结合长期记忆中的复用知识 K 辅助规划。

**（2）执行阶段 — 三个智能体协作**
- **Screen Parser（“眼睛”）**：对当前截图做 OCR 文本检测（DBNet + ConvNextViT）、图标定位（GroundingDINO）、图标描述（Qwen-VL-Plus），输出元素-坐标对列表；
- **State Agent**：实时增量构建 FSM——每个状态节点包含：屏幕自然语言描述 dᵢ、下一状态预测 dᵢ₊₁、**前置条件与后置条件**（pre/post-condition）。迁移定义为 T(sᵢ, aᵢ) = (sᵢ₊₁, preᵢ₊₁, postᵢ)。引入**状态信标（state beacon）**：对相似屏幕做语义匹配、复用已有节点，减少状态爆炸；
- **Actor Agent**：基于当前子任务和感知信息选择并执行具体动作（点击坐标、输入文本等）。

**（3）验证与错误恢复 — Reflection Agent**
- 执行动作后，将 **FSM 预测的状态**（含前后置条件）与实际新屏幕进行比对；
- 输出三分类判定：`Success` / `NoChange` / `Fail`，并附失败原因；
- 失败时从 FSM 中找出**已确认的稳定状态**，生成回退恢复计划逐步重试；
- 若连续失败 2 次，则终止恢复，重新调用 Planner 生成修订计划，避免陷入死循环。

**（4）知识保留 — Mentor Agent**
- 任务结束后分析执行历史、错误日志和迁移历史，提取可复用知识 K：动作序列（带前置条件）、指导提示（guidance cues）、以及完整 FSM；
- 存储到长时记忆库中，供未来相似任务（如跨应用购物流程）作为外部上下文加载。

## 3. 实验设计

### 三个 Benchmark

| 基准 | 规模 | 特点 | 评价方式 |
|---|---|---|---|
| Mobile-Eval-E | 25 任务、15 应用、364 动作，76% 跨应用 | 最高复杂度跨应用任务 | 物理设备 Pixel 7 Pro + ADB，人工评估 |
| SPA-Bench | 20 英文任务、25 应用、262 动作 | 跨应用系统+第三方应用 | 物理设备 + 人工评估 |
| AndroidWorld | 116 任务模板、20 应用 | 约 90% 单应用、严格步骤限制、低容错 | 模拟器（emulator）+ 自动评估 |

### 评估指标
- **Success Rate (SR)**：任务完全完成比例；
- **Satisfaction Score (SS)**：评分细则满足比例（部分完成度）；
- **Action Accuracy (AA)**：与人工参考轨迹的动作匹配率；
- **Termination Rate (TR)**：非成功提前终止比例（越低越好）；
- **Recovery Success (RS)**：失败子任务中成功恢复的比例。

### 对比方法
- 主要基线：**Mobile-Agent-E+Evo**（唯一具有长时记忆的知识复用基线，重跑 5 次取均值）；
- 其他基线：AppAgent、Mobile-Agent、Mobile-Agent-v2、AgentS2、V-Droid、UI-TARS、GPT-4o+UGround 等；
- 骨干模型测试：GPT-4o（2024-11-20）、Claude 3.5 Sonnet、Gemini 1.5 Pro（温度设为 0）。

### 消融实验
对四个关键组件逐一移除：
1. 移除 Planner（完全无规划）；
2. 移除多计划选择（LLM-as-judge）；
3. 移除 State Agent 的前置/后置条件；
4. 移除 Mentor 知识保留。

## 4. 资源与算力

- **论文未明确说明**使用的 GPU 型号、数量、训练时长或推理成本；
- 仅提及使用 GPT-4o 等闭源商业 MLLM API 作为骨干，本地部署的 Screen Parser 组件（DBNet、GroundingDINO、Qwen-VL-Plus）需要一定的 GPU 推理资源，但具体硬件配置和能耗数据未披露；
- 实验在物理手机（Google Pixel 7 Pro）上部署，但同样未说明实际运行时间和智能体推理开销。

## 5. 实验数量与充分性

### 实验组数统计
- **主实验**：3 个基准（Mobile-Eval-E、SPA-Bench、AndroidWorld），覆盖跨应用和单应用场景；
- **骨干模型敏感性实验**：3 种 MLLM × 2 个主要基准，共 6 组结果；
- **消融实验**：4 个组件配置 × 2 个主要基准，共 8 组（表5中实际展示了 5 行设置）；
- 基线重跑保证一致性：Mobile-Agent-E+Evo 重跑 5 次并取均值。

### 充分性评价
- **优点**：实验覆盖面较广（跨应用 + 单应用、物理设备 + 模拟器），消融设计完整，验证了每个组件的贡献；多人独立评估并引入第三人仲裁，降低主观偏差；温度设 0、使用同一骨干模型与基线对比，公平性较好。
- **局限**：跨应用基准只有 25+20 个任务，样本量偏小，统计显著性未报告；消融实验仅在两个跨应用基准上完成，AndroidWorld 上未做消融；对 MLLM 敏感性的测试只有 3 个模型，未覆盖更多开源模型。

## 6. 主要结论与发现

- **显著超越现有基线**：Mobile-Eval-E 上 SR 达 84.0%（比基线 Mobile-Agent-E+Evo 提升 12%）、RS 达 71.9%（提升 4.53%）；SPA-Bench 上 SR 达 80.0%（提升 5%）、RS 达 66.7%（**大幅提升 13.81%**）；AndroidWorld 上 SR 达 63.7%，超过全部基线（含 V-Droid 59.5%、AgentS2 54.3%）。
- **错误更少、恢复更强**：Agent-SAMA 遇到的错误明显少于基线（Mobile-Eval-E：32 vs 49，SPA-Bench：63 vs 70），且恢复成功率更高——FSM 结构化表示既能帮助正确决策，也能有效辅助错误恢复。
- **骨干模型影响大**：GPT-4o 最优，Claude 3.5 次之，Gemini 1.5 Pro 最弱；但即使使用更弱的 Claude 3.5，Agent-SAMA 的表现仍优于基于 GPT-4o 的 Mobile-Agent-E+Evo——说明 FSM 框架本身可弥补骨干模型的不足。
- **消融结果**：全部组件共同作用效果最佳。规划影响最大（SR 降 32-35%），其次是多计划选择、Mentor、前后置条件；各组件互补协同。

## 7. 方法与设计亮点

1. **首次将 FSM 引入移动 GUI 智能体**：以 UI 屏幕为状态、动作为迁移，为智能体赋予结构化导航视图，突破反应式局限；
2. **多智能体职责分离清晰**：规划（Planner）、感知（Screen Parser）、状态建模（State Agent）、执行（Actor）、验证恢复（Reflection）、知识沉淀（Mentor）各司其职，协同高效；
3. **状态信标 + 语义复用**：有效控制状态数量，避免冗余节点导致的 FSM 爆炸；
4. **前后置条件**：为每个状态和迁移附加逻辑约束，使智能体能形式化地验证“是否应该处于此状态”，而不是仅凭视觉相似性判断；
5. **多计划 + LLM-as-judge**：避免单一路径规划导致的次优解；
6. **模型无关的轻量记忆层**：FSM 作为附加记忆结构，可与不同 MLLM 骨干和现有智能体设计兼容，易于推广；
7. **恢复机制稳健**：失败→回退→重试→连续失败则重新规划的级联方案，避免陷入死循环。

## 8. 不足与局限性

### 实验覆盖有限
- 仅覆盖 Mobile-Eval-E、SPA-Bench（英文子集）和 AndroidWorld，未覆盖更多基准（如 AutoDroid、MobileAgentBench 等）；
- 动态内容（如信息流刷新）、外部干扰（如第三方广告弹窗）、系统通知等不可预测状态未充分测试；
- SPA-Bench 的中文任务未被评估，语言泛化性未知。

### 偏差与公平性风险
- 人工评估虽双人独立 + 第三人仲裁，但 25/20 个任务的样本量较小，置信区间和统计检验缺失；
- Mobile-Agent-E+Evo 重跑结果与原论文报告值有差异（论文承认这一点），虽然重跑 5 次降低方差，但基线稳定性仍是潜在问题；
- 主要对比基线限于 Mobile-Agent 系列，对其他框架（如 AgentS2、V-Droid）的对比仅在 AndroidWorld 上报告 SR 单一指标；
- 消融实验未在 AndroidWorld 上进行，无法评估各组件在严格单应用场景中的独立贡献。

### 应用限制
- 依赖商业 MLLM API（GPT-4o），成本与延迟未讨论；FSM 构建和状态匹配的推理开销未量化；
- 跨应用任务中为每个应用维护独立 FSM，应用间跳转的整体建模仍有待加强；
- 针对状态爆炸问题仅通过“语义匹配复用”缓解，复杂应用（大量相似页面）下的扩展性未验证。

---

（完）
