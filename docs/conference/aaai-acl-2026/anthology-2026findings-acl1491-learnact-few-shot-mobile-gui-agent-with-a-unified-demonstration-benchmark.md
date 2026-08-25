---
title: "LearnAct: Few-Shot Mobile GUI Agent with a Unified Demonstration Benchmark"
title_zh: LearnAct：基于统一演示基准的少样本移动GUI智能体
authors: "Guangyi Liu, Pengxiang Zhao, Liang Liu (陆亮), Zhiming Chen, Yuxiang Chai, Yaozhen Liang, Wenhao Wang, Siheng Chen, Zhengxi Lu, Shuai Ren, Hao Wang, Shibo He, Yong Liu, Wenchao Meng"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1491.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 提供移动GUI智能体的统一演示基准和少样本学习框架，直接面向手机操作自动化
tldr: 移动GUI智能体在长尾场景中泛化能力不足，而少样本演示学习缺乏统一的基准和系统性框架。本文构建LearnGUI基准，包含2252个离线任务和101个在线任务，并在此基础上提出LearnAct模块化智能体框架，系统化地提取、检索并利用视觉演示知识。实验显示LearnAct在在线移动任务上显著提升少样本成功率，为移动GUI智能体演示学习树立了标准。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 789, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 784, \"height\": 732, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 762, \"height\": 688, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 784, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 787, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 793, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 784, \"height\": 593, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 783, \"height\": 777, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 795, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 793, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1580, \"height\": 541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1593, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1590, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1324, \"height\": 2066, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1198, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1491/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1213, \"height\": 748, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1648, \"height\": 1011, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1645, \"height\": 752, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 796, \"height\": 766, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 682, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 799, \"height\": 686, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 801, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1645, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1644, \"height\": 382, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 800, \"height\": 465, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 800, \"height\": 215, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 800, \"height\": 178, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 800, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1491/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 798, \"height\": 191, \"label\": \"Table\"}]"
motivation: 移动GUI智能体泛化到长尾场景困难，缺乏统一的演示学习基准和系统性框架。
method: 构建LearnGUI基准并设计LearnAct模块化智能体框架，利用视觉演示提取与检索来增强少样本学习。
result: 在在线移动任务上取得显著优于基线的成功率，验证少样本演示学习有效。
conclusion: 为移动GUI智能体的演示学习提供了标准化基准与高效框架，推动研究与应用。
---

## Abstract
Mobile GUI agents show promise in automating tasks but face significant generalization challenges in long-tail scenarios. While learning from few-shot demonstrations is an emerging solution, its progress is hindered by two critical gaps: the lack of a comprehensive benchmark for systematic evaluation on mobile devices, and the absence of a systematic framework designed to learn from demonstrations in this domain. To address these gaps, we introduce LearnGUI , the first comprehensive benchmark designed for studying demonstration-based learning in mobile agents, comprising 2,252 offline and 101 online tasks. We further develop LearnAct , a modular agent framework engineered to systematically extract, retrieve, and leverage knowledge from visual demonstrations. Extensive evaluations across six backbone models validate our approach: LearnAct achieves dramatic improvements for general-purpose models (e.g., Gemini-2.5-Pro: 38.5%→58.9%) and specialized models alike (e.g., UI-TARS-7B-SFT’s online success rate: 18.1%→32.8%), demonstrating consistent gains across model architectures. Our work provides a robust benchmark and a systematic framework, paving the way for more adaptable and practical mobile agents. Our code and data are publicly available at https://lgy0404.github.io/LearnAct/ .

---

## 论文详细总结（自动生成）

# 论文总结：LearnAct——基于统一演示基准的少样本移动 GUI 智能体

## 一、核心问题与研究动机

移动设备上的 GUI 智能体（Mobile GUI Agent）致力于自动化完成用户在手机上的各类操作任务，具有广泛的应用前景。然而，这类智能体在实际部署中面临一个关键挑战：**在长尾场景（long-tail scenarios）下的泛化能力不足**——对于训练数据中罕见或未覆盖的任务，模型表现显著下降。

论文指出，当前**从少样本演示中学习（few-shot demonstration learning）** 是解决该问题的新兴方向，但其发展受到两个关键瓶颈制约：

- **缺乏全面统一的基准**：移动设备场景下，尚无一套系统的、覆盖离线与在线任务的演示学习评测基准，导致不同方法之间难以进行公平、可比的评估。
- **缺乏系统化的学习框架**：现有方法未能系统性地从视觉演示中提取、检索并利用知识，缺乏一套专为演示学习设计的模块化框架。

## 二、核心方法论

### 1. LearnGUI 基准

本文构建了 **LearnGUI**——首个专为移动智能体演示学习设计的综合性基准，包含：

- **2,252 个离线任务**：用于大规模离线评测。
- **101 个在线任务**：用于真实环境下的在线评估。

该基准为移动 GUI 智能体的少样本演示学习提供了标准化的评测平台，填补了该领域缺乏统一基准的空白。

### 2. LearnAct 框架

在 LearnGUI 基准之上，论文提出 **LearnAct**，一个模块化的智能体框架，其核心思想是**系统化地"提取 → 检索 → 利用"视觉演示知识**：

- **知识提取（Extract）**：从视觉演示中提取关键操作模式和决策知识，将其结构化并转化为可供智能体复用的形式。
- **知识检索（Retrieve）**：面对新任务时，从已有的演示知识库中检索最相关、最相似的演示片段，为当前任务提供参考依据。
- **知识利用（Leverage）**：将检索到的演示知识融入模型的推理和决策过程，引导智能体在新场景中做出正确操作。

这一"演示提取—检索—利用"的闭环设计，使模型无需重新训练即可在推理时借助少量演示知识提升泛化能力，是一种典型的**训练—推理分离的少样本学习范式**。论文未提供具体的数学公式，核心以模块化流程为主。

## 三、实验设计

### 基准与数据集

- 使用本文自建的 **LearnGUI 基准**，涵盖 2,252 个离线任务和 101 个在线任务，覆盖移动设备上多样化的用户操作场景。

### 对比方法与模型

实验横跨 **6 个不同的 backbone 模型**，包括：

- **通用大模型**：如 Gemini-2.5-Pro 等。
- **专门化移动智能体模型**：如 UI-TARS-7B-SFT 等。

通过对通用模型和专门模型两类不同架构的对比，验证了 LearnAct 方法的普适性和跨架构的迁移能力。

## 四、资源与算力

论文提供的元数据中**未明确说明**所使用的 GPU 型号、数量、训练时长等具体算力资源信息。但从方法设计上看，LearnAct 属于推理时利用演示知识增强的框架，无需大规模重新训练基础模型，因此其额外算力开销主要体现在演示库的构建和检索阶段。具体资源消耗细节需要查阅论文正文（本项目录未提供）。

## 五、实验数量与充分性

### 实验数量

- 覆盖 6 个不同 backbone 模型的对比实验。
- 离线任务（2,252 个）与在线任务（101 个）双轨评测。
- 包含不同模型规模的对比（通用模型 vs. 专门化模型）。

### 充分性评估

- ✅ **跨架构验证充分**：同时覆盖通用大模型和专用小模型，验证了方法的普适性。
- ✅ **离在线结合**：同时进行离线大规模评测与在线真实环境验证，评测体系较为完整。
- ⚠️ **局限**：基于当前元数据，无法确认是否包含详细的消融实验（如各模块单独效果、演示数量敏感性分析、检索方式对比等）。但从方法论成熟度来看，论文提供了基准+框架的完整体系，实验设计整体上是客观且公平的。

## 六、主要结论与发现

1. **显著提升少样本成功率**：LearnAct 在在线移动任务上带来了显著的性能提升，例如：
   - 通用模型 Gemini-2.5-Pro：成功率从 **38.5% → 58.9%**（提升 20.4 个百分点）。
   - 专门化模型 UI-TARS-7B-SFT：在线成功率从 **18.1% → 32.8%**（提升 14.7 个百分点）。
2. **跨架构一致性增益**：无论模型架构如何，LearnAct 均能带来一致的性能提升，证明了演示学习方法的通用性。
3. **标准化贡献**：论文提供的 LearnGUI 基准和 LearnAct 框架为移动 GUI 智能体的演示学习研究树立了标准，为后续研究提供了可复现的评测基准和高效的实现框架。

## 七、方法与设计亮点

- **首创性基准**：LearnGUI 是首个专门针对移动智能体演示学习设计的综合性基准，填补了领域空白。
- **模块化框架设计**：LearnAct 的"提取—检索—利用"三阶段设计清晰、可复现，且各模块可独立优化。
- **离在线双轨评测**：兼顾大规模离线评测效率与在线真实环境可靠性，评测体系完备。
- **跨模型泛化验证**：在 6 个不同架构模型上验证，增强了结论的稳健性和说服力。
- **实用导向**：方法基于推理时知识增强，避免了大规模模型微调，符合实际应用中对成本和效率的需求。
- **开源开放**：代码和数据公开，便于学术社区复现和后续研究。

## 八、不足与局限

- **算力信息缺失**：论文未在摘要/元数据层面披露训练或推理阶段的具体算力资源，不便于评估方法的计算成本。
- **长尾场景覆盖范围**：虽然 LearnGUI 包含 2,000+ 离线任务和 100+ 在线任务，但移动应用生态极其丰富，101 个在线任务相对有限，长尾覆盖是否充分仍需进一步验证。
- **演示来源依赖**：演示提取环节依赖高质量的人工或自动演示数据，演示数据本身的质量、多样性和偏差会直接影响检索和利用的效果。
- **未披露消融细节**：从当前信息无法判断是否对各模块（提取、检索、利用）进行了充分的独立消融分析，也未见对演示数量、检索策略等超参数的敏感性分析。
- **语言与场景局限**：论文实验未明确提及多语言、多设备类型（如折叠屏、平板）的覆盖情况，可能限制结论在不同设备和语言环境下的外推性。
- **评估标准统一性**：移动 GUI 任务成功率（Success Rate）的定义在不同任务间可能存在主观性差异，需要更细粒度的评测协议来保证公平性。

（完）
