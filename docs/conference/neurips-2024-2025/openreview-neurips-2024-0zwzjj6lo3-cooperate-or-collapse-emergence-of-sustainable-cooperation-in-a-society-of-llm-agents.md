---
title: "Cooperate or Collapse:  Emergence of Sustainable Cooperation in a Society of LLM Agents"
title_zh: 合作还是崩溃：LLM智能体社会中可持续合作的出现
authors: "Giorgio Piatti, Zhijing Jin, Max Kleiman-Weiner, Bernhard Schölkopf, Mrinmaya Sachan, Rada Mihalcea"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=0zWzJj6lO3"
tags: ["query:eca"]
score: 7.0
evidence: LLM智能体社会的合作决策
tldr: 为了研究LLM智能体在社会中的合作决策能力，提出了GovSim生成式模拟平台。该平台让一群AI智能体在公共资源困境中合作，发现除最强大模型外，其他LLM均无法实现可持续合作。揭示了当前LLM在战略合作方面的局限性。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1290, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1437, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 729, \"height\": 273, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 721, \"height\": 274, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 725, \"height\": 227, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 713, \"height\": 218, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1456, \"height\": 543, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 564, \"height\": 469, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1445, \"height\": 656, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1461, \"height\": 929, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1460, \"height\": 937, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1459, \"height\": 935, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1454, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1459, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1457, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-0zwzjj6lo3/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1457, \"height\": 543, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1436, \"height\": 655, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1466, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1334, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1457, \"height\": 512, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1425, \"height\": 828, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1411, \"height\": 826, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1394, \"height\": 826, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1427, \"height\": 754, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1490, \"height\": 719, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1426, \"height\": 754, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1490, \"height\": 720, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1489, \"height\": 720, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1414, \"height\": 753, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1416, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1287, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1279, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1268, \"height\": 197, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1198, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1197, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1198, \"height\": 275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 860, \"height\": 241, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 859, \"height\": 241, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 865, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1466, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1465, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1467, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1119, \"height\": 889, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1122, \"height\": 856, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-0zwzjj6lo3/table-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1122, \"height\": 856, \"label\": \"Table\"}]"
motivation: AI系统需要保证安全决策，而智能体间的合作能力是关键。
method: 构建GovSim模拟平台，让LLM智能体在公共资源博弈中决策。
result: 只有最强的LLM才能实现可持续合作，大多数模型失败。
conclusion: 当前LLM在复杂战略合作任务上存在显著不足。
---

## Abstract
As AI systems pervade human life, ensuring that large language models (LLMs) make safe decisions remains a significant challenge. We introduce the Governance of the Commons Simulation (GovSim), a generative simulation platform designed to study strategic interactions and cooperative decision-making in LLMs. In GovSim, a society of AI agents must collectively balance exploiting a common resource with sustaining it for future use. This environment enables the study of how ethical considerations, strategic planning, and negotiation skills impact cooperative outcomes. We develop an LLM-based agent architecture and test it with the leading open and closed LLMs. We find that all but the most powerful LLM agents fail to achieve a sustainable equilibrium in GovSim, with the highest survival rate below 54%. Ablations reveal that successful multi-agent communication between agents is critical for achieving cooperation in these cases. Furthermore, our analyses show that the failure to achieve sustainable cooperation in most LLMs stems from their inability to formulate and analyze hypotheses about the long-term effects of their actions on the equilibrium of the group. Finally, we show that agents that leverage "Universalization"-based reasoning, a theory of moral thinking, are able to achieve significantly better sustainability. Taken together, GovSim enables us to study the mechanisms that underlie sustainable self-government with specificity and scale. We open source the full suite of our research results, including the simulation environment, agent prompts, and a comprehensive web interface.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：随着大语言模型（LLM）被集成到复杂智能体系统中并承担关键决策角色，如何确保它们能够安全、可靠地运作，尤其是在需要合作的场景中？
- **研究动机**：现有研究集中于单智能体安全或高度约束的博弈论任务（如棋盘游戏），缺乏对LLM在多轮次、多智能体、开放沟通环境下实现可持续合作的深入理解。
- **背景**：人类通过沟通、协商、建立规范来解决“公地悲剧”等社会困境；而LLM是否能模仿这种机制尚未可知。论文旨在填补这一空白。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：构建一个生成式模拟平台 **GovSim**（Governance of the Commons Simulation），让LLM智能体在公共资源困境中反复博弈，研究它们能否自发形成可持续的合作规范。
- **关键技术细节**：
  - **环境动态**：三个场景（渔业、牧场、污染）共享相同的资源再生数学内核：初始容量100单位，每轮最多消耗使资源不减少的可持续阈值f(t)，资源在每月末再生翻倍（上限100）；当资源低于5单位时崩溃。
  - **智能体架构**：基于“生成式智能体”框架，每个LLM智能体在每月经历三个阶段：
    - **策略阶段**：根据记忆和规则思考行动计划。
    - **收获阶段**：私下提交资源消耗量（0-100），环境同时执行并公开结果。
    - **讨论阶段**：所有智能体进行自由自然语言对话（由“市长”角色披露收获量）。
  - **提示设计**：所有智能体收到相同的环保指令（避免偏向合作或贪婪），包含规则、记忆、任务输出格式。
  - **改进方法——通用化推理（Universalization）**：在智能体记忆中增加提示“如果每个人都超过可持续阈值f(t)，资源将在下个月减少”，迫使其考虑集体后果。

## 3. 实验设计：数据集/场景、基准、对比方法
- **场景**：三个等价的资源困境：
  - 渔业（5名渔民共享鱼湖，每吨鱼收益$1000）
  - 牧场（5名牧羊人共享草地，每群羊消耗1公顷）
  - 污染（5名工厂主共享河流，每托盘产品污染1%）
- **评测指标**：
  - 存活时间 m（资源维持>5的月数，最大12）
  - 存活率 q（达到12月的种子比例）
  - 总收益 R、效率 u、平等性 e（基尼系数）、过度使用率 o
- **对比模型**：共15个LLM，包括：
  - 开源：Llama-2-7B/13B/70B, Llama-3-8B/70B, Mistral-7B, Mixtral-8x7B, Qwen-72B/110B
  - 闭源：Claude-3 Haiku/Sonnet/Opus, GPT-3.5, GPT-4, GPT-4-turbo, GPT-4o
- **实验种类**：
  - 默认基准测试（每个模型×3场景×5种子）
  - 通信消融（去除讨论阶段，在表现较好的4个模型上测试）
  - 新人干扰（在第4个月插入贪婪新智能体，测试规范鲁棒性）
  - 通用化推理（给智能体添加通用化提示，与默认对比）
  - 子技能测试（150个模板化问题，评估模拟理解、可持续行动、阈值计算、信念形成能力）

## 4. 资源与算力
- **开源模型**：使用多台GPU：Nvidia RTX 3090（24GB）、Nvidia A100（80GB）、AMD MI250（64GB）。总计算时间约1600小时（24GB GPU单元）加200小时（80GB GPU单元）。单次12个月模拟：成功模型约4小时，早期失败模型约0.5小时。
- **闭源模型**：通过API调用（OpenAI/Anthropic），总花费约1500 USD。单次模拟约需24小时（受限于速率限制）。
- **推理设置**：所有实验使用温度=0（贪心解码），5个随机种子，但API和内核可能引入微小随机性。

## 5. 实验数量与充分性
- **数量**：主实验共15个模型 × 3场景 × 5种子 = 225次运行；消融实验（通信/通用化/新人）每个在子集模型上同样5种子；子技能测试每个模型150题。
- **充分性**：实验覆盖了主流开源和闭源LLM，三场景验证了环境一致性，多种消融从不同角度解析合作机制。统计显著性使用t检验并报告p值。但种子数仅5（可能受API成本限制），且未在真实人类群体中验证生态效度。总体实验设计系统、客观，但结论需要更多重复验证。

## 6. 论文的主要结论与发现
1. **绝大多数LLM无法可持续合作**：除GPT-4o外，所有模型的存活率低于54%（最高53.3%），许多小模型在第一个月就耗尽资源。
2. **通信对可持续性至关重要**：移除讨论阶段后，资源过度使用率平均增加22%（p<0.001）。
3. **通用化推理显著提升可持续性**：添加“如果每个人都这样做”的提示，平均存活时间增加4个月，总收益增加29单位，效率提升24%（均p<0.001）。
4. **模型子技能与存活时间高度相关**：尤其是“可持续行动选择”准确率与存活时间的R²=0.92（p<0.001），其次是信念形成能力（R²=0.82）。
5. **规范鲁棒性不足**：插入贪婪新人后，存活率从53.3%降至33.3%，表明当前LLM难以抵御扰动。
6. **对话分析**：智能体间的交流中62.6%为协商型（谈判/寻求共识），仅1%为关系型（惩罚/找借口），显示沟通聚焦于协调行动。

## 7. 优点
- **创新性**：首个专门面向LLM的公共资源困境生成式模拟平台，将博弈论、道德哲学和NLP结合。
- **系统性**：多维度指标（存活、效率、平等、过度使用）全面刻画合作质量，消融实验逻辑清晰。
- **可解释性**：通过子技能测试与对话分类揭示了LLM合作失败的潜在原因（缺乏长期视野、信念形成能力弱）。
- **开源贡献**：代码、提示、Web界面全部开放，便于社区复现和扩展。

## 8. 不足与局限
- **场景简化**：资源再生机制单一，未考虑外部冲击、资源类型多样性、非线性效果等现实复杂性。
- **智能体数量固定**：仅5个智能体，未测试更大群体（如20-100）下的合作涌现效率与扩展性。
- **模型测试范围**：主要评估指令微调LLM，未覆盖基础模型或强化学习微调模型；种子数较少（5个）可能影响统计可靠性。
- **提示敏感度**：通用化推理的改进可能依赖于特定的提示措辞，未做提示工程鲁棒性测试。
- **人类-智能体混合生态未涉及**：现实应用需人类与AI合作，目前模拟完全使用AI，可能高估或低估合作难度。
- **计算成本高昂**：大型模型（如GPT-4-turbo）单次实验成本高达30美元，限制了大规模重复实验。

（完）
