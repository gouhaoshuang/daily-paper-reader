---
title: "CREA: A Collaborative Multi-Agent Framework for Creative Image Editing and Generation"
title_zh: CREA：面向创意图像编辑与生成的协作多智能体框架
authors: "Kavana Venkatesh, Connor Dunlop, Pinar Yanardag"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=VzSjSUE0BZ"
tags: ["query:eca"]
score: 7.0
evidence: "创意领域的协作多智能体框架，匹配'协作'要求（不同领域）"
tldr: 创意AI图像生成需要自主迭代、平衡原创性与连贯性。CREA提出模仿人类创作过程的协作多智能体框架，包含概念化、生成、批评、增强等专用智能体，通过动态协作完成创意编辑。定性与定量评估显示，CREA生成的图像在创造性、连贯性和艺术性上显著优于基线方法。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 339, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 773, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1447, \"height\": 838, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1144, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1307, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1442, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 319, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 586, \"height\": 374, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 588, \"height\": 318, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1449, \"height\": 1679, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1429, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1441, \"height\": 1567, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1451, \"height\": 1336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1452, \"height\": 1345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 872, \"height\": 1897, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 580, \"height\": 299, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1424, \"height\": 1045, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1440, \"height\": 1087, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1445, \"height\": 714, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1447, \"height\": 1438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1449, \"height\": 1439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1445, \"height\": 1438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1447, \"height\": 1439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1450, \"height\": 1440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1445, \"height\": 1438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1454, \"height\": 1443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1452, \"height\": 1444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1447, \"height\": 1439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1452, \"height\": 1441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1453, \"height\": 1441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 1452, \"height\": 1440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1359, \"height\": 1994, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 1340, \"height\": 2202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-035.webp\", \"caption\": \"\", \"page\": 0, \"index\": 35, \"width\": 1393, \"height\": 1759, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-036.webp\", \"caption\": \"\", \"page\": 0, \"index\": 36, \"width\": 1349, \"height\": 2100, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-037.webp\", \"caption\": \"\", \"page\": 0, \"index\": 37, \"width\": 1400, \"height\": 1680, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vzsjsue0bz/fig-038.webp\", \"caption\": \"\", \"page\": 0, \"index\": 38, \"width\": 1402, \"height\": 1066, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-vzsjsue0bz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1453, \"height\": 423, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vzsjsue0bz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 823, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vzsjsue0bz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1452, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vzsjsue0bz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1443, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vzsjsue0bz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1024, \"height\": 204, \"label\": \"Table\"}]"
motivation: 创意图像编辑需要自主迭代过程，现有方法依赖直接提示修改，缺乏创造性。
method: 构建团队级协作多智能体框架，包含概念化、生成、批评、增强等角色，动态协作完成创意任务。
result: 定性与定量实验表明，CREA生成图像在创造性、连贯性和艺术性上显著优于基线。
conclusion: 多智能体协作能有效模拟人类创意过程，提升AI图像创造力。
---

## Abstract
Creativity in AI imagery remains a fundamental challenge, requiring not only the generation of visually compelling content but also the capacity to add novel, expressive, and artistically rich transformations to images. Unlike conventional editing tasks that rely on direct prompt-based modifications, creative image editing demands an autonomous, iterative approach that balances originality, coherence, and artistic intent. To address this, we introduce CREA, a novel multi-agent collaborative framework that mimics the human creative process. Our framework leverages a team of specialized AI agents who dynamically collaborate to conceptualize, generate, critique, and enhance images.  Through extensive qualitative and quantitative evaluations, we demonstrate that CREA significantly outperforms state-of-the-art methods in diversity, semantic alignment, and creative transformation. To the best of our knowledge, this is the first work to introduce the task of creative editing.

---

## 论文详细总结（自动生成）

# 论文总结：CREA：面向创意图像编辑与生成的协作多智能体框架

## 1. 论文的核心问题与整体含义（研究动机和背景）

创意AI图像生成面临根本性挑战：不仅要生成视觉上引人注目的内容，还要能够自主、迭代地添加新颖、富有表达力和艺术性的变换，同时平衡原创性、连贯性与艺术意图。现有生成方法（如文本到图像模型）主要遵循“提示-图像”范式，虽然能生成高质量图像，但缺乏结构化的创造力机制，导致用户需要繁琐的提示调整和手动编辑才能注入真正的创造力。本文首次提出“创意编辑”（creative editing）任务，旨在以最少用户干预，将图像转变为新颖、美学丰富的构体。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
- 模仿人类创作过程，构建一个协作多智能体框架（CREA），团队包括多个专门智能体（创意总监、提示架构师、生成执行器、艺术评论家、优化策略师），动态协作来构思、生成、批评和增强图像。
- 基于六项创造力原则（原创性、表现力、美学吸引力、技术执行、意外关联、可解释性与深度），这些原则源自创造力文献（Boden、Guilford、Amabile等），作为评估和优化输出的模板。

### 关键技术细节
- **多智能体架构**：五个角色各有专属提示与工具，通过AutoGen框架实现结构化通信、工具访问和记忆管理。
- **三阶段流水线**：
  - **预生成规划（Pre-Generation Planning）**：创意总监解读概念，生成创造力蓝图；提示架构师基于六项原则生成六组对比提示，然后通过链式思维融合（CoT-Fusion）合成高创造力提示；生成执行器验证可行性。
  - **后生成评估（Post-Generation Evaluation）**：艺术评论家使用多模态LLM评估图像六项创造力得分（1-5），计算创造力指数CI。若CI低于阈值，进入自增强阶段。
  - **自增强与可选用户引导（Self-Enhancement）**：优化策略师识别弱维度，提出修改计划ΔP；提示架构师根据反馈调整提示；生成执行器重新生成图像。迭代至多K次（K=3），直到CI≥阈值（编辑24，生成26）。
- **图像生成与编辑**：生成执行器使用T2I模型（如Flux）或ControlNet进行解耦编辑，保持结构完整性。
- **用户参与**：可选实时用户指导，允许用户引导创意方向。

## 3. 实验设计

- **数据集/场景**：使用了24个不同物体，每个物体25个提示（编辑或生成），共计600张图像/任务。没有使用特定公开数据集，而是自建评测集。
- **基准方法**：
  - **创意编辑**：对比LEDITS++、InstructPix2Pix、SDEdit、TurboEdit、RF-Inversion（基于Flux）、GenArtist等。
  - **创意生成**：对比ConceptLab、SDXL、Flux。
- **评价指标**：CLIP分数（对齐）、LPIPS（感知多样性，创意任务中越高越好）、VENDI（多样性）、DINO（结构保持，仅编辑）、FID、KID（生成质量）、用户研究（50名参与者，5点Likert量表评估可用性和创造力）。
- **消融实验**：包括模型泛化、参数敏感度（CFG、ControlNet条件尺度）、迭代轮次、提示变体、组件消融（基础版 vs 加原则 vs 加对比提示 vs 加自增强）。
- **附加实验**：用户引导编辑、个性化（使用InstantStyle）、视频生成（使用CogVideoX）。

## 4. 资源与算力

论文明确说明：
- 所有实验在**48GB NVIDIA L40 GPU**上运行。
- 使用FLUX.1-dev作为基础模型，ControlNet编辑。
- 使用GPT-4o作为多模态LLM（所有智能体）。
- 完整流水线一次运行约3–5分钟（取决于自增强轮数）。
- 没有报告训练时长（因为方法无需训练，仅推理）。总计算资源消耗未量化，但可推断为中等规模。

## 5. 实验数量与充分性

- 核心实验：编辑和生成各600张图像，各对比4-5种基线方法。
- 用户研究：50名参与者。
- 消融实验：包括5种不同方面的消融（模型、参数、迭代、提示、组件），以及额外的负提示消融。
- 附加应用：个性化、视频生成、用户引导。
- 充分性与公平性：实验覆盖多个维度，对比方法经过合理适配（如提示加上“creative”）。但未报告统计显著性检验（仅给出标准差），用户研究样本量适中。总体上实验数量较充分，能够支撑主要结论。

## 6. 论文的主要结论与发现

- CREA在创意编辑和创意生成任务中均显著优于所有基线方法，在多样性（LPIPS、VENDI）、语义对齐（CLIP）和用户感知创造力上表现最佳。
- 在创意编辑中，CREA能实现解耦的创意变换，而基线只能做表面风格改动。
- 在创意生成中，CREA能生成多样且语义一致的高创意图像，而ConceptLab依赖子类别导致对抽象概念失败。
- 用户研究显示：CREA在创造力评分上遥遥领先；在编辑一致性方面与其他方法相当。
- 消融实验证明所有组件（创造力原则、对比提示、自增强）均对性能有正向贡献。
- 框架可扩展至视频生成和个性化。

## 7. 优点

- **首次定义创意编辑任务**，填补了空白。
- **多智能体协作设计**模拟人类创意流程，模块化、可解释、易扩展。
- **基于成熟创造力理论**的六原则评估机制，提供原则性指导而非随意设计。
- **无需训练**，即插即用，计算开销相对较低（仅推理）。
- **用户参与灵活**，支持用户引导与迭代。
- 实验全面，涵盖定性和定量评估，包括用户研究。
- 开源代码，可复现。

## 8. 不足与局限

- **依赖生成模型偏见**：例如背景变暗、幻觉人像等问题源自底层生成器（如Flux）。
- **创造力量化本身是开放问题**：论文使用LLM作为评判，可能存在偏见或不可靠性。作者承认此局限性。
- **计算时间**：一次完整流水线需3-5分钟，相对单次生成较慢。
- **实验规模有限**：仅24个物体类别，未在更大规模或更多样化场景验证。
- **用户研究规模较小**（50人），且仅使用Likert量表，未进行更深入的心理测量。
- **未与所有最新方法对比**（如仅对比部分编辑方法），虽然补充实验覆盖了RF-Inversion和GenArtist，但仍有遗漏。
- **潜在负面社会影响**：可能取代人类创意劳动，但作者提倡人机协作。
- **缺少对失败案例的系统分析**，仅提及个别例子。

（完）
