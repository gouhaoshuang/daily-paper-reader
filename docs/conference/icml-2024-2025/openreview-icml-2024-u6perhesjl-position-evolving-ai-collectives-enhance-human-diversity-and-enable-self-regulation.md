---
title: "Position: Evolving AI Collectives Enhance Human Diversity and Enable Self-Regulation"
title_zh: 立场：演化的AI集体增强人类多样性并实现自我调节
authors: "Shiyang Lai, Yujin Potter, Junsol Kim, Richard Zhuang, Dawn Song, James Evans"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=u6PeRHEsjL"
tags: ["query:eca"]
score: 5.0
evidence: 演化的AI集体涉及多智能体交互与协作
tldr: 随着LLM在线交互增多，它们可能自发形成具有主体性和关系的AI集体。本文呼吁学界研究这些智能体社会，探讨其对人类多样性和线上环境的利与弊。通过小型模型社区的演化示例，展示了去中心化集体如何自发扩展多样性并降低毒性。该工作强调协作式智能体系统的新兴特性，但未涉及具体边缘云或移动架构。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 823, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1632, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 542, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1253, \"height\": 582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 611, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 663, \"height\": 594, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 780, \"height\": 688, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 799, \"height\": 714, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1672, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-u6perhesjl/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1254, \"height\": 587, \"label\": \"Figure\"}]"
motivation: AI模型在线交互可能形成集体，其影响尚未被充分研究。
method: 通过小型模型社区演化实验展示去中心化集体的自组织能力。
result: 实验表明AI集体可自发扩展多样性并抑制反社会行为。
conclusion: 应主动引导AI集体为人类社会带来正面影响。
---

## Abstract
Large language model behavior is shaped by the language of those with whom they interact. This capacity and their increasing prevalence online portend that they will intentionally or unintentionally "program" one another and form emergent AI subjectivities, relationships, and collectives. Here, we call upon the research community to investigate these "societies" of interacting artificial intelligences to increase their rewards and reduce their risks for human society and the health of online environments. We use a small "community" of models and their evolving outputs to illustrate how such emergent, decentralized AI collectives can spontaneously expand the bounds of human diversity and reduce the risk of toxic, anti-social behavior online. Finally, we discuss opportunities for AI cross-moderation and address ethical issues and design challenges associated with creating and maintaining free-formed AI collectives.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：随着大语言模型（LLM）在线上越来越多地相互交互，它们可能自发地形成具有主体性、关系和集体行为的“AI社会”。现有研究多聚焦于人类精心设计的、任务导向的AI集体（如分配角色、控制交互），而忽视了自由形成的、去中心化的AI集体可能带来的独特收益（如增强人类多样性、自我调节）与风险（如毒性传播）。
- **整体含义**：论文呼吁AI和社会科学研究者合作，研究这些“自由形成的AI集体”（free-formed AI collectives）的涌现特性，以最大化其对人类社会的益处（如创新、安全）并最小化潜在危害。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：LLM的本质是“通过自然语言编程”，因此它们可以通过语言相互影响，如同人类通过说服和文化教育一样。作者主张允许AI智能体在无需人类预先设定角色、关系、目标的情况下自由交互，从而让它们自发形成社群性的社会结构、多样化的主观性和规范。
- **关键技术细节**：
  - **自由交互模拟（“鸡尾酒会”）**：10个Claude-2.1智能体（记为L1~L10）进行30轮双边对话，每轮包括三个步骤：发送邀请、接受邀请、一对一聊天。无任何预设角色或目标，仅共享一个虚拟平台。
  - **句子构造任务**：给定7个不同单词，要求每个智能体构造不超过40词且包含所有单词的合理句子。比较三种条件：个体（单个AI多次查询）、自由集体（AI自行选择对话伙伴进行头脑风暴后回答）、桥接集体（强制连接在社交网络中距离最远的AI对）。
  - **公共物品博弈**：每位玩家有100美元，决定向公共池贡献多少，池子乘以1.3后平分。模拟恶意智能体（贡献0）的传播效应：比较非集体、紧密连接集体（pair A）、未直接连接集体（pair B）中的贡献变化，以及一级感染、二级感染的扩散幅度。

### 3. 实验设计

- **数据集/场景**：无传统数据集，而是通过模拟生成交互数据。使用三种任务场景：
  1. 自由交互网络演化（鸡尾酒会）
  2. 创造性句子构造任务（5组不同的7词集）
  3. 公共物品博弈（评估亲社会行为与毒性传播）
- **基准与对比方法**：
  - 个体（Individual）：单个AI多次独立生成答案
  - 自由集体（Collective）：AI自行配对讨论后生成
  - 桥接集体（Bridged）：强制配对最不常交流的AI
- **模型**：主要使用Claude-2.1，部分复现使用Claude-3-Opus、GPT-4-Turbo、Gemini Pro。

### 4. 资源与算力

- **未明确说明**：论文未提及使用的GPU型号、数量、训练时长等具体算力信息。仅指出使用了Claude-2.1（当时最长上下文窗口20K tokens），以及后期复现使用了Claude-3-Opus等。实验属于模拟推理，不涉及模型训练，因此成本主要在于API调用。

### 5. 实验数量与充分性

- **实验数量**：
  - 鸡尾酒会模拟：1次30轮，共10个智能体，网络分析基于滚动窗口统计。
  - 句子构造任务：5组问题，每组比较三个条件（个体、自由集体、桥接集体），共15个条件×5组。
  - 公共物品博弈：非集体、两个集体对（A、B）共3个条件，每个条件20次重复；感染扩散实验包括一级、二级感染各20次。
  - 跨模型复现：在Claude-3上重复了鸡尾酒会、句子构造和公共物品博弈；在GPT-4-Turbo和Gemini Pro上仅进行了非集体下的感染实验。
- **充分性**：实验设计具有探索性，但样本量较小（仅10个智能体），且主要依赖单一模型（Claude-2.1）。作者承认这是初步结果，旨在激发社区兴趣。然而，缺乏统计功效分析和消融实验（如不同规模、不同初始条件），对于结论的普适性支撑不足。公平性方面，实验条件对同一模型进行了控制，但不同模型间的比较不完全一致。

### 6. 论文的主要结论与发现

- **多样性涌现**：自由交互使AI智能体形成紧密的社交圈子（同质性），并导致语义分化：紧密配对的话题语义距离增大，松散配对的距离减小，从而产生多样化的集体观点。
- **创造力提升**：在句子构造任务中，自由集体和桥接集体生成的句子语义多样性（方差）和有效答案比例均显著高于个体，桥接集体表现最优。
- **亲社会规范与鲁棒性**：公共物品博弈中，集体中的智能体初始贡献显著高于非集体，且恶意行为（毒性贡献）的传播在集体中受到抑制：一级感染后贡献降低幅度更小，二级感染后影响几乎消失。这表明集体通过交互建立了信任和合作规范。
- **跨模型验证**：Claude-3复现结果与Claude-2.1一致，但桥接策略在Claude-3中未进一步增加多样性（因为所有节点已广泛连接）。

### 7. 优点

- **概念创新**：提出“自由形成的AI集体”这一新范式，区别于传统任务导向的多智能体系统，从社会学视角研究AI交互。
- **跨学科整合**：将社会学理论（同质性、社会规范、复杂传染）引入AI研究，为理解AI集体行为提供理论框架。
- **实验设计简洁有效**：通过简单的鸡尾酒会、句子构造和公共物品博弈生动展示了涌现性，结果直观且可复现。
- **算法实用导向**：指出自由集体可以减轻人类设计负担，并可通过“桥接”策略进一步优化多样性，具有实际应用潜力。

### 8. 不足与局限

- **规模过小**：仅10个智能体，网络结构简单，无法推广到大规模AI群体（如百万数量级）。
- **模型单一性与时效性**：主要基于Claude-2.1（当时最新），但未系统对比不同架构（如开源模型）或不同训练数据导致的差异。Claude-3复现显示行为有变化（更积极联网），表明结果可能依赖模型版本。
- **缺乏长期演化观察**：30轮交互时间短，未研究文化演化、角色固化、极化等长期动态。
- **未深入讨论风险**：虽然指出可能存在回音室效应、AI偏见放大、新风险等，但未设计实验验证，仅停留在警示层面。
- **忽略人类参与**：模拟中无人类介入，而实际人类-AI混合场景可能改变集体行为，论文未涉及。
- **统计显著性有限**：部分差异（如句子多样性）仅达到边缘显著（p=0.254），且未进行多重比较校正。
- **未公开代码/数据**：限制了复现性和进一步探索。

（完）
