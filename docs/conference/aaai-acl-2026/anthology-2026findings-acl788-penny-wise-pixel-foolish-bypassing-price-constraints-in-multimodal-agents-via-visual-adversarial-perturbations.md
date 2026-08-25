---
title: "\"Penny Wise, Pixel Foolish\": Bypassing Price Constraints in Multimodal Agents via Visual Adversarial Perturbations"
title_zh: 图便宜反而吃亏：通过视觉对抗扰动绕过多模态智能体的价格约束
authors: "Jiachen Qian, Zhaolu Kang"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.788.pdf"
tags: ["query:mobile-agent"]
score: 5.0
evidence: 揭示移动智能体部署中对抗鲁棒性挑战的视觉攻击研究
tldr: 移动智能体在金融交易等场景中展现出较强操作能力，但其对抗鲁棒性堪忧。论文发现视觉主导幻觉漏洞，并提出PriceBlind隐写式白盒攻击框架，通过不可察觉的视觉对抗信号覆盖截图中的价格文本证据，迫使智能体做出非理性经济决策。该研究揭示了移动智能体在高风险任务中的安全盲区，为部署安全带来重要警示。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl788/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 788, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl788/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1152, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl788/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 797, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl788/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 798, \"height\": 539, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 815, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 809, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 814, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 813, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 814, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 809, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 806, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 680, \"height\": 365, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 802, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 802, \"height\": 345, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 804, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 806, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl788/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 806, \"height\": 210, \"label\": \"Table\"}]"
motivation: 多模态智能体在金融交易中的对抗鲁棒性存在盲区。
method: 提出视觉主导幻觉概念，并设计白盒攻击框架PriceBlind，利用视觉对抗信号压制文本价格证据。
result: 攻击能迫使智能体忽略价格约束，产生非理性决策。
conclusion: 强调了移动智能体部署中安全对抗研究的重要性。
---

## Abstract
The rapid proliferation of Multimodal Large Language Models (MLLMs) has ushered in the era of the “Agentic Economy,” where Mobile Agents autonomously execute high-stakes financial transactions. While these agents demonstrate impressive operational capabilities, their adversarial robustness remains a glaring blind spot. In this paper, we identify a systemic vulnerability termed Visual Dominance Hallucination (VDH), where imperceptible adversarial visual cues can act as a “super-stimulus,” overriding textual price evidence in our evaluated screenshot-based price-constrained settings and forcing the agent into irrational economic decisions. We propose PriceBlind, a stealthy, white-box adversarial attack framework for controlled screenshot-based evaluation. Unlike prior works that rely on conspicuous artifacts like pop-ups, PriceBlind exploits the modality gap in CLIP-based encoders via a novel Semantic-Decoupling Loss. Rather than literally making a luxury item “look cheap,” this regularizer weakens the consistency between high-price text and visual value cues by aligning the image embedding with a low-cost/value-associated anchor region while preserving pixel-level fidelity. On our main E-ShopBench benchmark with clear price constraints, screenshot-based white-box evaluation yields ASRs around 80% on the evaluated agents. Under the evaluated single-turn coordinate-selection protocol in a simplified layout-aware setting, our Ensemble-DI-FGSM strategy also yields non-trivial black-box transfer, with ASR roughly 35–41% across GPT-4o, Gemini-1.5-Pro, and Claude-3.5-Sonnet. In the same screenshot-based setting, standard robust encoders reduce ASR only partially, while a Verify-then-Act stack with robust encoders lowers ASR to below 10% at some clean-accuracy cost.

---

## 论文详细总结（自动生成）

# 论文总结：《"Penny Wise, Pixel Foolish": Bypassing Price Constraints in Multimodal Agents via Visual Adversarial Perturbations》

## 1. 核心问题与整体含义

- **背景**：多模态大语言模型（MLLMs）的快速发展推动了"智能体经济"（Agentic Economy）的兴起，移动智能体（Mobile Agents）开始自主执行高风险的金融交易任务。尽管这些智能体展现出较强的操作性能力，但其对抗鲁棒性研究严重不足，构成了一个明显的安全盲区。
- **核心问题**：论文识别出多模态智能体存在一个系统性漏洞——**视觉主导幻觉（Visual Dominance Hallucination, VDH）**，即不可察觉的视觉对抗线索可以作为"超级刺激"（super-stimulus），覆盖基于截图的、受价格约束场景中的文本价格证据，从而迫使智能体忽略价格约束，做出不理性的经济决策。
- **整体含义**：该研究揭示了移动智能体在金融交易等高风险场景中的安全脆弱性，表明"智能体经济"的部署安全性尚未得到充分保障，具有重要的风险警示意义。

## 2. 方法论

- **核心思想**：提出 **PriceBlind**，一种隐蔽的、白盒对抗攻击框架，用于受控的截图式评估。与以往依赖弹窗等明显伪影的攻击不同，PriceBlind利用基于CLIP编码器中的模态间隙（modality gap），通过一种新颖的**语义解耦损失（Semantic-Decoupling Loss）**来实施攻击。
- **关键机制**：攻击并不直接让奢侈品"看起来便宜"，而是通过正则化手段**削弱高价格文本与视觉价值线索之间的语义一致性**——做法是将图像嵌入与一个低成本/价值关联的锚点区域对齐，同时保持像素级保真度（即保证扰动对人类不可察觉）。
- **攻击流程（文字描述）**：
  1. 将包含价格约束的截图作为输入；
  2. 以最小化语义一致性为目标，迭代优化对抗扰动；
  3. 扰动幅度限制在人类不可感知的范围内，保持视觉呈现的"原样性"；
  4. 将生成的对抗样本输入智能体，使其视觉感知压过文本价格证据，继而做出非理性选择。
- **黑盒迁移策略**：在简化布局感知设置下，论文还采用了**集成DI-FGSM（Ensemble-DI-FGSM）**策略来增强黑盒攻击的迁移性。

## 3. 实验设计

- **基准与场景**：论文构建了 **E-ShopBench** 基准，包含明确价格约束的电商交易场景。评估采用基于截图的白盒测试，并使用简化的布局感知设置、单轮坐标选择协议（single-turn coordinate-selection protocol）。
- **被评估智能体**：包括 GPT-4o、Gemini-1.5-Pro 和 Claude-3.5-Sonnet。
- **对比与防御方案**：
  - 标准鲁棒编码器（Standard Robust Encoders）；
  - 鲁棒编码器 + Verify-then-Act（验证后行动）堆栈架构。
- **评估指标**：白盒攻击成功率（ASR）、黑盒迁移成功率、加入防御后的ASR，以及防御带来的干净准确率成本。

## 4. 资源与算力

- **提取文本中未明确提及** GPU 型号、数量、训练时长、推理成本等算力相关信息。因此，无法对该方法的经济成本与计算开销做进一步量化评估。

## 5. 实验数量与充分性

- **主要实验**：
  - 白盒攻击实验（E-ShopBench 上 ASR 约 80%）；
  - 黑盒迁移实验（三种商业模型上 ASR 约 35–41%）；
  - 防御有效性实验（鲁棒编码器单独使用及与 Verify-then-Act 联合使用）。
- **充分性评估**：实验覆盖了攻击效能、迁移性和防御对抗三个基本层面，逻辑自洽且具有初步的说服力。但受限于摘要篇幅，**文中未呈现具体的消融实验（如扰动幅度敏感性、价格约束粒度影响、语义解耦损失的贡献分解等）**，也缺少详细的表格数据描述，因此从现有文本难以全面判断实验的完整性与公平性。总体而言，核心结论有实证支撑，但覆盖广度有限，需要借助全文进一步验证。

## 6. 主要结论与发现

- 在价格约束清晰的截图场景下，PriceBlind 对评估中的智能体实现了 **约 80% 的白盒攻击成功率**，表明视觉主导幻觉是当前多模态智能体的系统性安全盲区。
- 黑盒迁移效果虽弱于白盒（ASR 约 35–41%），但**在多种商业模型中均能产生非平凡的攻击成功率**，说明该方法具有一定通用性。
- 单独使用标准鲁棒编码器**只能部分降低攻击成功率**，防御效果有限。
- 而采用 **Verify-then-Act 架构 + 鲁棒编码器** 可将 ASR 降至 **10% 以下**，但其代价是干净场景下的准确率下降。
- 总体结论：移动智能体在高风险金融交易任务中的对抗鲁棒性存在显著缺口，有必要在部署前纳入对抗安全评估与防御机制。

## 7. 优点

- **问题新颖且具有现实紧迫性**：指出了一个尚未被充分研究的攻击面——通过视觉对抗干扰来绕过文本价格约束，具有明确的现实危害性。
- **攻击方式隐蔽性强**：PriceBlind 不依赖弹窗等明显伪影，而是采用隐写式扰动，贴近真实攻击场景。
- **方法论具有创新性**：通过语义解耦损失显式打破文本-视觉之间的跨模态价值一致性，而非简单地改变物品"外观"，在对抗攻击的思路上有独到之处。
- **防御评估较完整**：同时考虑了鲁棒编码器与高层级验证机制（Verify-then-Act）两类防御，并报告了防御的准确率代价，具有实际参考价值。
- **迁移实验增强说服力**：在多个商业级模型上进行黑盒验证，有助于说明攻击的非偶然性。

## 8. 不足与局限

- **白盒假设的限制**：攻击框架的核心设计基于白盒访问模型权重，在实际部署中攻击者往往难以获得完全的白盒访问。
- **黑盒成功率尚有限**：黑盒迁移 ASR 仅为 35%～41%，实际攻击中的可靠性与威胁程度仍受限。
- **防御的代价**：有效的防御组合（Verify-then-Act + 鲁棒编码器）会牺牲一定的干净准确率，实用部署中需要权衡安全性与功能性。
- **场景覆盖单一**：主要基于电商价格约束场景、简化布局与单轮坐标选择协议，未覆盖真实移动智能体典型的多轮、动态交互环境。
- **理论分析不足**：对"视觉主导幻觉"产生机制的揭示仍停留在现象层面，尚缺乏深入的认知科学或模型可解释性层面的理论验证。
- **信息保密程度不足**：提取文本未提供完整的实验设置细节（如超参数、扰动预算、评估统计量等），对实验复现与公平性评估造成障碍。

（完）
