---
title: Learning to Plan with Personalized Preferences
title_zh: 学习带有个性化偏好的规划
authors: "Manjie Xu, Xinyi Yang, Wei Liang, Chi Zhang, Yixin Zhu"
date: 2025-01-21
pdf: "https://openreview.net/pdf?id=r53lwSSfcI"
tags: ["query:eca"]
score: 4.0
evidence: 学习具有个性化偏好的规划，针对协作角色
tldr: AI智能体在协作中需要理解和适应用户的个性化偏好，但现有方法采用通用策略。本文提出从少量演示中学习偏好并自适应规划策略的方法，并引入PbP基准。实验表明该方法能有效捕捉用户偏好并提升协作体验，但更侧重人机协作而非智能体间协作。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1772, \"height\": 779, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1774, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 861, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1601, \"height\": 662, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 853, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1599, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-r53lwssfci/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 849, \"height\": 367, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-r53lwssfci/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1433, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r53lwssfci/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1390, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r53lwssfci/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 882, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r53lwssfci/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 928, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r53lwssfci/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1174, \"height\": 711, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-r53lwssfci/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1488, \"height\": 1175, \"label\": \"Table\"}]"
motivation: 现有智能体在协作规划中忽视了个体用户的偏好差异。
method: 从少量演示中学习隐式偏好，并自适应调整规划策略。
result: 在PbP基准上，该方法能较好泛化用户偏好，提升规划效果。
conclusion: 学习个性化偏好是提升人机协作质量的重要方向。
---

## Abstract
Effective integration of AI agents into daily life requires them to understand and adapt to individual human preferences, particularly in collaborative roles. Although recent studies on embodied intelligence have advanced significantly, they typically adopt generalized approaches that overlook personal **preferences in planning**. We address this limitation by developing agents that not only learn preferences from few demonstrations but also learn to adapt their planning strategies based on these preferences. Our research leverages the observation that preferences, though implicitly expressed through minimal demonstrations, can generalize across diverse planning scenarios. To systematically evaluate this hypothesis, we introduce PbP benchmark, an embodied benchmark featuring hundreds of diverse preferences spanning from atomic actions to complex sequences. Our evaluation of SOTA methods reveals that while symbol-based approaches show promise in scalability, significant challenges remain in learning to generate and execute plans that satisfy personalized preferences. We further demonstrate that incorporating learned preferences as intermediate representations in planning significantly improves the agent's ability to construct personalized plans. These findings establish preferences as a valuable abstraction layer for adaptive planning, opening new directions for research in preference-guided plan generation and execution.

---

## 论文详细总结（自动生成）

# 论文总结：Learning to Plan with Personalized Preferences

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：现有AI代理在协作规划中通常采用通用策略，忽视个体用户的个性化偏好，导致协作效率与满意度不足。
- **背景**：自然语言指令存在歧义，无法充分捕捉用户偏好（如准备苹果时的清洗方式、切割风格、容器选择等细节）。心理学研究表明偏好引导人类行为，但现有方法（如NeatNet、SAND）局限于特定任务（如整理），无法泛化。
- **目标**：开发能从少量演示（few-shot demonstrations）中隐式学习用户偏好，并基于偏好自适应调整规划的智能体，实现个性化协作。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：将偏好作为“中间表示”（intermediate representation）进行学习，再将学到的偏好用于指导规划。
- **关键技术**：两阶段框架。
  - **第一阶段：偏好学习**  
    从观测集合 \( O = \{ (S_i, A_i, M)^N \} \)（含第一人称视频、动作序列、可选场景地图）中学习偏好表示 \( p = f(O; \theta_f) \)。可输出隐式表示或显式文本标签。
  - **第二阶段：偏好引导规划**  
    给定当前状态 \( s_i \) 和偏好 \( p \)，生成动作序列，优化损失：  
    \[
    L = \sum_{i=1}^N \ell(g(s_i, f(O; \theta_f); \theta_g), a_i)
    \]
- **偏好层次结构**：
  - **Action Level**（75种）：细粒度执行细节（如水量、书架层数）。
  - **Option Level**（135种）：子任务的替代方式（如水果放冰箱 vs. 放桌子）。
  - **Sequence Level**（80种）：任务排序与优先级（如“烹饪前先洗”、“清洁后整理”）。
- **少样本学习**：从3个示例子（不同场景/物体）中提取通用偏好模式。

## 3. 实验设计：使用了哪些数据集/场景、benchmark、对比方法
- **基准**：**PbP (Preference-based Planning) benchmark**，基于NVIDIA Omniverse和OmniGibson。
  - 50个场景，290种偏好，5000个测试实例（每个实例含egocentric视频、鸟瞰图、帧级动作标注）。
  - 演示池：15,000条独特记录。
- **对比方法**：
  - **视频输入模型**：ViViT、LLaVA-NeXT、EILEV、GPT-4V。
  - **符号输入模型**：DAG-Opt（因果结构学习）、Llama3-8B、GPT-4。
- **实验设置**：
  - 端到端设置：直接根据演示和当前状态生成动作序列。
  - 两阶段设置：先预测偏好标签，再基于标签规划（含使用真实标签的上界对照）。
  - 评估指标：Levenshtein距离（动作序列差异）、偏好预测准确率。

## 4. 资源与算力
- **算力说明**：所有实验在单台机器上运行，配备**8块NVIDIA A100 GPU**。LLM推理使用保守解码参数（温度0.05，top-k=1，top-p=0.05）。
- **未明确信息**：训练总时长、各模型具体训练轮次/推理时间未报告。仅ViViT提到训练30个epoch，学习率3e-5；其余模型多为预训练或API调用。

## 5. 实验数量与充分性
- **实验组数**：
  - 主要实验（Table 1 & 2）：端到端 vs 两阶段，涵盖选项级和序列级，6种模型对比。
  - 消融实验：去除演示（ablative）、泛化（direct vs original）、演示数量影响（1,2,3,5）。
  - 案例分析（Table A3）：提供具体场景的规划输出对比。
- **充分性评价**：
  - **优点**：涵盖不同模态（视频/符号）、不同偏好层级、不同学习范式（端到端 vs 分解），并进行了系统消融和泛化分析。
  - **不足**：
    - 视频模型受限于输入帧数（GPT-4V仅8帧），与符号模型比较可能存在不公平。
    - 缺乏真实环境或人类参与者评估。
    - 标准偏差较大（部分结果±超过10），说明性能不稳定，但未深入分析方差来源。
    - 未报告统计显著性检验。

## 6. 论文的主要结论与发现
- **端到端学习失败**：所有视频模型Levenshtein距离接近平均序列长度（选项级15.80，序列级35.87），表明无法从原始视频提取偏好。
- **两阶段显著提升**：引入偏好中间表示后，规划性能大幅改善；使用真实偏好标签时，GPT-4V和GPT-4几乎完美对齐（距离~0.12~1.26）。
- **符号模型优越**：GPT-4在偏好预测（86.27%选项级）和规划上都大幅优于视频模型（GPT-4V 48.48%）。
- **泛化差异**：符号模型对场景变化鲁棒（direct vs original差别小），视频模型依赖视觉特征，场景变化时准确率下降明显（如EILEV从46.93%降至38.33%）。
- **演示数量效应**：更多演示（1→5）总体提升性能，但过多演示（如5个）可能导致过拟合（偏好预测准确率下降）。

## 7. 优点
- **新颖基准**：PbP覆盖多层次、多场景偏好，支持可重复评估，代码和数据可扩展。
- **清晰的问题分解**：将偏好学习与规划分离，验证了偏好作为抽象层的有效性，为后续研究提供框架。
- **全面模型评估**：同时对比视频和符号模型，并排除视觉复杂度干扰（符号输入），揭示核心瓶颈在于偏好抽象而非感知。
- **丰富的消融实验**：包括演示数量、泛化条件、有无演示等，增强结论可靠性。

## 8. 不足与局限
- **合成数据局限**：依赖Omniverse合成场景，不能完全代表真实世界的噪声、多样性及用户行为复杂性。
- **偏好定义人为**：290种偏好由作者预设，可能无法覆盖真实用户细粒度偏好（如文化差异、临时偏好变化）。
- **评估指标单一**：仅使用Levenshtein距离和准确率，缺乏用户满意度、交互自然度等主观指标。
- **计算资源与可复现性**：未公开训练代码/超参数细节（除ViViT外），且未报告模型推理成本。
- **公平性问题**：视频模型受限于API帧数限制（GPT-4V 8帧），可能低估其潜力；符号模型获得完整动作序列，感知负担更低，比较基础不完全等。
- **未验证真实机器人**：规划输出未在真实机器人上执行，仅停留在模拟器内评估。

（完）
