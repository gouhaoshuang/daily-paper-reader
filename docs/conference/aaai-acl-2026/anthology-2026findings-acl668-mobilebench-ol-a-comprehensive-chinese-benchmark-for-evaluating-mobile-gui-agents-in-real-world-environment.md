---
title: "MobileBench-OL: A Comprehensive Chinese Benchmark for Evaluating Mobile GUI Agents in Real-World Environment"
title_zh: MobileBench-OL：真实环境中移动GUI智能体的综合中文基准
authors: "Qinzhuo Wu, Zhizhuo Yang, Hanhao Li, Pengzhi Gao, Wei Liu, Jian Luan"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.668.pdf"
tags: ["query:mobile-agent"]
score: 10.0
evidence: 面向移动GUI智能体的综合在线基准，包含80个中文应用的1080个任务
tldr: 针对现有线上移动GUI智能体基准忽视推理探索能力且未考虑真实环境随机噪声的问题，提出MobileBench-OL在线基准。它包含来自80个中文应用的1080个任务，通过5个子集分别评测任务执行、复杂推理和噪声鲁棒性。该基准更贴近真实移动环境，能够全面评估移动GUI智能体的能力。它为移动智能体框架的开发与评估提供了重要测试平台。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 785, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1646, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 780, \"height\": 687, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1586, \"height\": 717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 800, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 728, \"height\": 1106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1655, \"height\": 603, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 799, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1629, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1647, \"height\": 871, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 762, \"height\": 726, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 619, \"height\": 1056, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1626, \"height\": 2046, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1623, \"height\": 1786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1265, \"height\": 1057, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl668/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1659, \"height\": 801, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 786, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1658, \"height\": 688, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1655, \"height\": 536, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 803, \"height\": 436, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1664, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1643, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1642, \"height\": 377, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 802, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 729, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 801, \"height\": 285, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1652, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 802, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 802, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 803, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1641, \"height\": 1660, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1646, \"height\": 2105, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1658, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 805, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1650, \"height\": 461, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1650, \"height\": 1503, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1646, \"height\": 530, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl668/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 648, \"height\": 237, \"label\": \"Table\"}]"
motivation: 现有移动GUI智能体基准偏离真实环境，忽略推理探索和随机噪声。
method: 构建包含1080个任务、80个中文应用的在线基准，分5个子集评估执行、推理与噪声鲁棒性。
result: 实现了更真实全面的移动GUI智能体能力评测，弥补已有基准不足。
conclusion: 为移动智能体研究提供了贴合实际场景的评估标准。
---

## Abstract
Recent advances in mobile Graphical User Interface (GUI) agents highlight the growing need for comprehensive evaluation benchmarks. While new online benchmarks offer more realistic testing than offline ones, they tend to focus on the agents’ task instruction-following ability while neglecting their reasoning and exploration ability. Moreover, these benchmarks do not consider the random noise in real-world mobile environments. This leads to a gap between benchmarks and real-world environments. To addressing these limitations, we propose MobileBench-OL, an online benchmark with 1080 tasks from 80 Chinese apps. It measures task execution, complex reasoning, and noise robustness of agents by including 5 subsets, which set multiple evaluation dimensions. We also provide an auto-eval framework with a reset mechanism, enabling stable and repeatable real-world benchmarking. Evaluating 13 leading GUI agents on MobileBench-OL shows significant room for improvement to meet real-world requirements. Human evaluation further confirms that MobileBench-OL can reliably measure the performance of leading GUI agents in real environments.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机与背景）

随着多模态大语言模型和移动GUI智能体的迅速发展，如何公平、全面地评估这些智能体在真实移动环境中的表现成为一个关键问题。论文指出，现有评估基准主要存在以下不足：

- **离线基准脱离真实环境**：多数现有基准（如 AITW、AndroidControl）基于静态截图和预定义答案进行评测，无法反映真实环境中动态页面的复杂性。
- **忽视推理与探索能力**：当前线上基准（如 SPA-Bench、AndroidWorld）大多仅评测任务指令跟随能力，任务往往过于简单或路径过于僵化，不评估智能体在未知界面中自主探索、推理和纠错的能力。
- **未考虑真实环境随机噪声**：现有基准未能处理真实移动环境中常见的弹窗广告、网络延迟、页面加载失败、操作无效等噪声干扰。

MobileBench-OL 正是针对上述空白提出的解决方案——一个真实环境下的综合中文在线基准，旨在弥合学术评估与现实部署之间的差距，从**任务执行、复杂推理、噪声鲁棒性**三个核心维度全面评测移动 GUI 智能体。

## 2. 方法论：核心思想与关键技术细节

### 2.1 基准总体架构

- **规模**：包含来自 80 个中文 App 的 1080 个真实任务，覆盖 12 个应用类别（视频、音乐、新闻、办公、阅读、社交、交通、生活、工具、购物、金融、体育）。
- **真实环境**：基于真实手机设备（而非模拟器）运行，支持需要账号登录、高内存占用的应用，通过在线移动控制平台提供 ADB 访问，所有操作在真实网络条件下进行。
- **三层评估维度**：基础能力（Base + Long-Tail 子集）、复杂推理（Long-Horizon + GUI-Reasoning 子集）、鲁棒性（Noise-Robust 子集）。

### 2.2 五种子集设计

| 子集 | 任务数 | 核心测试能力 |
|------|--------|--------------|
| Base | 310 | 主流 App 基础功能操作（搜索、个人中心、设置等），覆盖 28 个功能点 |
| Long-Tail | 340 | 在 68 个长尾冷门 App 上的泛化适应能力 |
| Long-Horizon | 60 | ≥20 步的复杂多子任务长序列规划与长期记忆 |
| GUI-Reasoning | 60 | 界面探索推理能力（图标理解、隐藏功能发现、层级导航） |
| Noise-Robust | 310 | 对四类真实噪声的鲁棒性（重复执行、未执行、延迟、弹窗） |

### 2.3 难度分层机制

- **常规子集**：按黄金步数分 Easy（<8 步）、Medium（8–19 步）、Hard（≥20 步）。
- **GUI-Reasoning 子集**：按探索权重分难度——图标理解（0.5）、隐藏功能发现（1）、层级导航（2），任务总权重 ≤1 为 Easy、1–2 为 Medium、>2 为 Hard。

### 2.4 噪声注入机制

在推理阶段以 20% 概率随机触发以下四类噪声：

- **Repeat**：同一动作连续执行两次。
- **Unexecuted**：动作被系统拦截未执行。
- **Delay**：展示预定义的加载延迟页面，若智能体不等待而执行操作，操作将在真实结果页面上执行。
- **Pop-up**：展示预定义的弹窗页面，必须精准点击关闭按钮才能继续。

### 2.5 任务成功条件定义

- 采用基于 XPath-like 规则的评估条件，综合匹配 UI 元素的 text、resource-id、package、bounds 等属性以及动作坐标。
- 要求满足**完整性**（所有成功轨迹均满足条件）和**可靠性**（任何失败轨迹不完全满足条件），从而兼容多条有效 GUI 路径。
- 例如，任务“更换 Bilibili 随机头像”的成功条件为：点击“Avatar/Change Avatar”按钮 + 点击弹窗中的“Shuffle”选项，不限制具体导航路径。

### 2.6 自动化评估框架（Auto-Eval）

- **轨迹生成循环**：观察设备状态与历史交互 → 生成动作 → 统一格式转换并执行 → 循环直至任务完成或达到最大步数限制（3 倍黄金步数）。
- **四类终止结果**：Success（满足全部条件并以 Complete 结束）、Overdue Termination（已完成但超出步数限制）、Early Termination（提前结束未完成）、Failure（未完成也未报告结束）。
- **重置机制**：使用可靠智能体执行细粒度逆任务，分四类——任务级重置（单任务状态恢复）、应用级重置（多任务共享）、无需重置（纯浏览类）、不可行重置（服务端交互类，通过扩展成功条件处理）。每次完整评测后执行 255 个重置任务，成功率超过 90%。

### 2.7 数据构建流程

人工从零设计任务以避免 LLM 数据污染，流程包括：人工设计并执行获取黄金轨迹 → 专家定义成功条件 → UI-TARS-1.5 和标注者采样多样轨迹 → 自动评估 → 专家核验并修正条件。

## 3. 实验设计

### 3.1 评估指标

- **Success Rate (SR)**：核心指标，任务完整满足成功条件且以 Complete 动作结束时计为成功。
- **Sub-condition Success Rate (Sub-SR)**：已满足的子条件比例，不取决于任务如何终止。
- **Step Ratio**：智能体实际步数与人类黄金步数的比值，上限为 3 倍。
- **Failure Reasons**：Early Termination / Overdue Termination / Failure 三类占比分析。

### 3.2 基线模型

共评估 **13 个** GUI 智能体（摘要中明确说明）：

- **闭源模型（4 个）**：GPT-4o、M3A、T3A、Mobile-Agent-V2（均基于 GPT-4o 作为骨干）。
- **开源模型（9 个）**：InternVL2-8B、CogAgent-9B、UGround-V1-7B、OS-Atlas-Pro-7B、Qwen2-VL-7B、Qwen2.5-VL-7B、UI-TARS-7B、UI-TARS-1.5-7B，以及补充的 Qwen3-VL-8B、Mobile-Agent-V3、MAI-UI-8B。

所有开源模型在 80GB NVIDIA A100 GPU 上部署（但论文同时声称“部署在 80GB 上”以及“一个 80GB A100”，未明确说明具体数量和训练时长）。每个动作后等待 3 秒，最大步数为黄金步数的 3 倍。

## 4. 资源与算力

论文对算力信息的披露较为有限，具体情况如下：

- **训练/推理硬件**：仅明确提到开源模型部署在“80GB NVIDIA A100 GPU”上，未说明具体的 GPU 数量。
- **训练时长**：未提及任何模型训练时长或计算量（FLOPs）信息——这是评估可重复性时的一个不足。
- **推理成本**：未说明 13 个模型在 1080 个任务上的总推理耗时或 API 调用费用。
- **设备资源**：使用了 3 台真实智能手机，预装 80 个应用并通过在线控制平台管理。

若需复现实验，论文指出发布所有 APK 文件，允许用户在自己设备上安装运行。

## 5. 实验数量与充分性

论文进行了较为充分的多维度实验，可归纳为以下几组：

### 5.1 主实验
- 13 个模型在全部 1080 个任务（5 个子集）上的 SR 和 Sub-SR 对比。

### 5.2 消融与分析实验
1. **Long-Horizon 误差分析**：将 UI-TARS-1.5 在 60 个长程任务上的错误归为 5 类（推理规划失败 15%、子任务遗漏 6.7%、功能导航失败 16.7%、属性遗漏/错误 25%、视觉定位失败 21.7%）。
2. **GUI-Reasoning 难度分析**：按 Easy/Medium/Hard 分层对比成功率，发现难度越高性能下降越剧烈。
3. **噪声类型分析**：按 Repeat/Unexecuted/Delay/Pop-Up 四类噪声分解成功率，发现 Pop-Up 噪声影响最大。
4. **失败原因统计**：对 6 个高性能模型统计 Early Termination / Overdue Termination / Failure 三类失败占比。
5. **难度层级分析**：按黄金步数分层对比各子集成功率。
6. **Auto-Eval 人类评估**：对 UI-TARS-1.5 结果进行人工标注对比，Auto-Eval 准确率超过 95%（97.5%）。
7. **重置机制人类评估**：对 255 个重置任务进行人工验证，成功率超 90%。
8. **补充实验（附录 H）**：Step Ratio 分析、Pass@k（k=1,3,5）评估，以及基于 60 个长程任务的细粒度错误分类。

### 5.3 实验充分性评估

- **优点**：实验覆盖面广，从基础能力到复杂推理、噪声鲁棒性均有系统评估；包含人类评估交叉验证，增强了结论可信度；消融实验针对性强，能够定位模型的具体能力瓶颈。
- **不足**：所有评估基于单一厂商（小米）的真实设备，未涉及 iOS 或其他 Android 品牌；任务全部为中文应用场景，对非中文环境和应用的泛化性未验证；未进行跨设备、跨版本的稳定性测试（虽提及版本变化引起 ≤5% 波动，但未系统验证）。

## 6. 主要结论与发现

1. **现有智能体距离真实世界需求仍有显著差距**：最强模型 UI-TARS-1.5-7B 在 Base 子集 SR 为 60.97%，Long-Horizon 仅 15.00%，GUI-Reasoning 仅 38.33%，全部子集均未达到实用水平。
2. **Long-Horizon 是所有智能体的共同瓶颈**：该子集综合考验任务理解、分解、多步执行和长期记忆，性能最低。
3. **长尾应用泛化是短板**：在 Long-Tail 子集上各智能体性能明显下降，说明缺乏对新颖界面结构的适应能力。
4. **真实噪声处理能力普遍薄弱**：Pop-Up 噪声影响最为严重，多数智能体无法准确点击关闭按钮，导致任务卡死。
5. **基础能力强的模型推理不一定强**：Qwen3-VL-32B 参数规模最大，在 Base 和 Noise-Robust 上显著领先，但在 Long-Horizon 和 GUI-Reasoning 上的提升有限，说明参数扩展主要增强基础能力而非复杂推理。
6. **多图输入有助于状态追踪**：能接收多张截图输入的模型（如 GPT-4o）表现更好，可感知动作前后状态变化。
7. **Sub-SR 与 SR 的差距揭示**：长程任务中，智能体常能完成部分子任务但无法独立完成全流程；MAI-UI-8B 相比 UI-TARS-1.5-7B 总体 SR 仅提升 0.27%，但 Sub-SR 提升 4.49%，说明难点在全任务收尾而非子任务执行。
8. **Auto-Eval 框架可靠**：与人类评估的一致性超过 95%，可作为大规模自动评估的有效方案。

## 7. 优点

- **真实环境还原度高**：使用真实设备而非模拟器，支持账号登录和高内存应用，更接近实际部署场景。
- **评估维度全面**：同时覆盖基础能力、复杂推理、探索能力和噪声鲁棒性，填补了现有基准的能力评估盲区。
- **任务多样性丰富**：1080 个任务覆盖 80 个应用的 28 个功能点，从简单搜索到 20+ 步复杂任务再到探索推理任务，难度梯度合理。
- **考虑多路径有效性**：任务成功条件设计允许同一任务有多个有效 GUI 轨迹，更符合真实使用情形。
- **自动化评估可靠性高**：规则化的 XPath 条件定义方式清晰可扩展，Auto-Eval 与人类评估高度一致（>95%），支持大规模评测。
- **重置机制设计精心**：四类重置策略有效解决任务间的状态干扰问题，确保可重复性。
- **补充实验扎实**：包含误差细分类、难度分层分析、噪声类型分解、Pass@k 等多种分析视角，诊断性强。

## 8. 不足与局限

- **缺少跨应用任务**：作者承认当前基准缺乏需要组合多个应用完成的复杂跨应用任务，规划的后续方向。
- **单一语言与地域限制**：全部为中文应用生态，未覆盖英文或其他语言应用，限制了国际通用性（虽然也可视为“中文基准”的定位所致）。
- **硬件与算力信息披露不足**：未说明具体 GPU 数量、训练时长、推理总耗时等，降低了实验可复现性和成本评估的透明度。
- **设备品牌单一**：仅使用小米手机，未验证不同厂商设备的差异（不同 ROM、屏幕分辨率、系统行为可能影响结果）。
- **基础模型版本时效性**：评测的 12 个基线中部分模型（如 GPT-4o、InternVL2）在论文发布时已非最新版本，可能无法反映当前最优性能。
- **噪声模拟的人工性**：Delay 和 Pop-up 噪声使用预定义模板页面而非真实随机噪声，与完全随机的真实环境仍有差距。
- **重置机制局限**：对不可逆或服务端交互类任务（如“一键已读”）无法完全恢复原始状态，只能扩展成功条件作为补偿。

（完）
