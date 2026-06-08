---
title: Reimagining Mutual Information for Enhanced Defense against Data Leakage in Collaborative Inference
title_zh: 重新构想互信息以增强协作推理中的数据泄露防御
authors: "Lin Duan, Jingwei Sun, Jinyuan Jia, Yiran Chen, Maria Gorlatova"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=tdZLKY9usl"
tags: ["query:eca"]
score: 9.0
evidence: 边缘云协作推理防御
tldr: 边缘-云协作推理中，中间结果可能泄露边缘设备的输入和预测。本文提出InfoScissors防御策略，通过最小化中间结果与设备数据之间的互信息来阻止信息泄露。在多个数据集和攻击类型下验证了有效性，并提供了理论分析，直接服务于端云协同AI系统的隐私保护需求。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 655, \"height\": 316, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1023, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1462, \"height\": 382, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1430, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1419, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1419, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 867, \"height\": 350, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 237, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-tdzlky9usl/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 819, \"height\": 413, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-tdzlky9usl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1462, \"height\": 382, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-tdzlky9usl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 828, \"height\": 187, \"label\": \"Table\"}]"
motivation: 边缘-云协作推理中，攻击者可从中间结果提取输入和预测，隐私风险严重。
method: 通过最小化中间表示与设备数据之间的互信息，设计InfoScissors防御方法。
result: 在多种攻击下显著降低信息泄露，同时保持推理性能几乎不变。
conclusion: 互信息最小化是防御边缘-云协作推理中数据泄露的有效策略。
---

## Abstract
Edge-cloud collaborative inference empowers resource-limited IoT devices to support deep learning applications without disclosing their raw data to the cloud server, thus protecting user's data. Nevertheless, prior research has shown that collaborative inference still results in the exposure of input and predictions from edge devices. To defend against such data leakage in collaborative inference, we introduce InfoScissors, a defense strategy designed to reduce the mutual information between a model's intermediate outcomes and the device's input and predictions. We evaluate our defense on several datasets in the context of diverse attacks. Besides the empirical comparison, we provide a theoretical analysis of the inadequacies of recent defense strategies that also utilize mutual information, particularly focusing on those based on the Variational Information Bottleneck (VIB) approach. We illustrate the superiority of our method and offer a theoretical analysis of it.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **问题**：在边缘-云协作推理（collaborative inference）中，资源受限的边缘设备将模型的前几层（头模型）部署在本地，中间表示（representation）上传至云端，云端完成剩余计算。这种架构虽避免了原始数据直接暴露，但已有研究表明，攻击者（恶意云服务器）可从中间表示**重构输入**（模型反转攻击），也能从高层特征**推断预测结果**（模型补全攻击），导致严重隐私泄露。
- **动机**：现有防御方法（如差分隐私、噪声添加、压缩、基于变分信息瓶颈 VIB 的互信息正则化）通常会导致模型精度大幅下降，尤其在边缘设备头部网络较浅时防御效果很差。
- **整体含义**：本文提出一种新的互信息视角下的防御方法 InfoScissors，旨在同时保护输入和预测，在保持模型精度前提下显著降低信息泄露。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：通过训练阶段最小化两个互信息项：
  - 中间表示 \( r \) 与输入 \( x \) 之间的互信息 \( I(r;x) \) → 防止输入重构。
  - 云端编码器输出的特征 \( z \) 与标签 \( y \) 之间的互信息 \( I(z;y) \) → 防止预测推断。
- **关键技术**：使用 **CLUB（Contrastive Log-ratio Upper Bound）** 作为互信息的可计算上界，而非传统 VIB 方法。CLUB 上界为：
  \[
  I(r;x) \leq I_{\text{vCLUB}}(r;x) = \mathbb{E}_{p(r,x)}[\log q_\psi(x|r)] - \mathbb{E}_{p(r)p(x)}[\log q_\psi(x|r)]
  \]
  其中 \( q_\psi(x|r) \) 是参数化的变分分布（解码器），通过对抗训练最小化该上界。
- **算法流程**（文字描述）：
  1. 对每个批次，边缘设备计算表示 \( r \)；
  2. 更新解码器 \( \psi \)（最大化 \( \log q_\psi(x|r) \)）；
  3. 云端计算特征 \( z \)，边缘设备更新分类器 \( \theta_c \)（最小化交叉熵）和辅助分类器 \( \phi \)（最大化 \( \log h_\phi(y|z) \)）；
  4. 随机采样负样本，计算负对数项；
  5. 联合优化 \( \theta_h, \theta_e \) 以最小化组合损失：\( (1-\lambda_d-\lambda_l)\mathcal{L}_c + \lambda_d(\mathcal{L}_{d\_a}+\mathcal{L}_{d\_r}) + \lambda_l(\mathcal{L}_{l\_a}+\mathcal{L}_{l\_r}) \)。

### 3. 实验设计：数据集、场景、基准、对比方法

- **数据集**：CIFAR10、CIFAR100。
- **模型**：ResNet18，将第一个卷积层作为头模型（边缘设备），最后一个 basic block 作为分类器，中间层为云端编码器。
- **攻击方法**：
  - 输入泄露：**Knowledge Alignment (KA)**（黑盒 MI）、**Regularized MLE (rMLE)**（白盒 MI）。
  - 预测泄露：**Passive Model Completion (PMC)**、**Active Model Completion (AMC)**（自适应攻击）。
- **对比基线**：
  - **DP**（差分隐私）
  - **AN**（加噪）
  - **DC**（数据压缩）
  - **PPDL**（隐私保护深度学习，综合策略）
  - **MID**（基于 VIB 的互信息正则化，SOTA 基线）
- **评估指标**：
  - 效用：模型测试准确率（Accuracy）。
  - 输入防御：重构图像 SSIM（越低越好）。
  - 预测防御：攻击者分类准确率（越低越好）。

### 4. 资源与算力

- **文中明确说明**：实验在一台配备 **4 块 RTX TITAN GPU** 的服务器上进行。
- **未提供的细节**：未给出具体训练时长、批次数量或总计算量。

### 5. 实验数量与充分性

- **实验组数**：
  - 输入保护：在不同防御强度下，对 CIFAR10 和 CIFAR100 分别测试 KA 和 rMLE 攻击，绘制 Accuracy vs SSIM trade-off 曲线。
  - 预测保护：对两种攻击（PMC、AMC）各使用两种分类器架构（MLP、MLP_sim），同样绘制 trade-off 曲线。
  - 集成保护：同时设置 \( \lambda_d \) 和 \( \lambda_l \)，展示联合防御效果。
  - 附加实验：使用更大辅助数据集（双倍样本）测试 KA 攻击鲁棒性。
- **充分性评估**：实验覆盖了黑盒/白盒攻击、不同数据集、多种基线，且通过调整超参数得到完整的 trade-off 曲线，对比公平、客观。消融和补充实验进一步验证了方法的稳健性。

### 6. 论文的主要结论与发现

- InfoScissors 在**输入保护**方面：在 CIFAR10 上仅以不到 2% 的精度下降即可将重构 SSIM 降至 0.2 以下，而所有基线需要损失 10% 以上精度才能达到类似效果。
- 在**预测保护**方面：可将攻击准确率降至随机猜测水平（CIFAR10 上约 10%，CIFAR100 上约 1%），精度损失小于 1%，显著优于基线。
- **理论分析**：证明了 VIB 方法在输入保护场景下的不足（强制表示接近固定高斯会同时丢失对任务有用的信息），而 InfoScissors 直接优化 \( p(x|r) \) 更贴近防御目标。
- **集成防御**：可同时防御输入和预测泄露，整体精度损失小于 2%。

### 7. 优点：方法或实验设计上的亮点

- **理论创新**：精准指出 VIB 在防输入泄露中的缺陷，并采用更合适的 CLUB 上界，理论分析严谨。
- **方法统一**：同时处理输入和预测两种泄露，且训练流程对服务器方透明（服务器仅感知正常协作训练）。
- **实验设计**：绘制详细的 accuracy vs 防御效果 trade-off 曲线，而非仅单一指标，能全面反映方法优势；对比基线全面且最新。
- **鲁棒性验证**：考虑了自适应攻击（AMC）和大规模辅助数据集，显示良好泛化性。

### 8. 不足与局限

- **场景单一**：仅考虑单个边缘设备，文中指出可扩展到多设备但未实验验证。
- **计算开销**：未讨论训练额外解码器 \( g_\psi \) 和辅助分类器 \( h_\phi \) 带来的额外计算成本。
- **攻击类型覆盖**：未测试更复杂的联合攻击（如同时利用表示和特征进行重构），也未评估对梯度泄露等其他攻击的防御。
- **假设限制**：理论分析假设 \( p(x|r) \) 为高斯分布，实际中不一定成立，可能影响上界紧度。
- **可迁移性**：仅在 CIFAR 数据集上验证，未在更大规模或更复杂模型（如 Transformer）上测试。
- **偏差风险**：实验中的防御强度通过超参数调节，但不同防御方法的最佳超参数搜索未系统说明，可能存在调参不公平。

（完）
