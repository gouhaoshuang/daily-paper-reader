---
title: Enhancing Cooperative Multi-Agent Reinforcement Learning with State Modelling and Adversarial Exploration
title_zh: 通过状态建模与对抗性探索增强协作多智能体强化学习
authors: "Andreas Kontogiannis, Konstantinos Papathanasiou, Yi Shen, Giorgos Stamou, Michael M. Zavlanos, George Vouros"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=TCsdlqzZNL"
tags: ["query:eca"]
score: 8.0
evidence: 协作多智能体强化学习，结合状态建模
tldr: 在部分可观测环境中无通信的协作多智能体学习面临挑战。本文提出一种状态建模框架，让智能体从局部观测推断有意义的状态信念表示，过滤冗余信息，并利用对抗性探索增强协作策略。实验表明该方法在多个基准任务上提升了学习效率和协作性能。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1482, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1764, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1411, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1047, \"height\": 733, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1696, \"height\": 291, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1258, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 710, \"height\": 515, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 463, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 485, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 752, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 947, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1470, \"height\": 406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1459, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1762, \"height\": 316, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 734, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1567, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1765, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 580, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 569, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 567, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1728, \"height\": 302, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 682, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 691, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tcsdlqzznl/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1457, \"height\": 890, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1687, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 568, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1653, \"height\": 1026, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 532, \"height\": 711, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 724, \"height\": 1143, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 744, \"height\": 1012, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tcsdlqzznl/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 537, \"height\": 795, \"label\": \"Table\"}]"
motivation: 部分可观测环境中无通信的多智能体协作学习存在困难。
method: 提出状态建模框架，智能体推断状态信念并利用对抗性探索优化策略。
result: 在多个MARL基准上，该方法显著提升了协作任务的性能。
conclusion: 状态建模与对抗性探索有效增强了无通信环境下的多智能体协作学习。
---

## Abstract
Learning to cooperate in distributed partially observable environments with no communication abilities poses significant challenges for multi-agent deep reinforcement learning (MARL). This paper addresses key concerns in this domain, focusing on inferring state representations from individual agent observations and leveraging these representations to enhance agents' exploration and collaborative task execution policies. To this end, we propose a novel state modelling framework for cooperative MARL, where agents infer meaningful belief representations of the non-observable state, with respect to optimizing their own policies, while filtering redundant and less informative joint state information. Building upon this framework, we propose the MARL SMPE$^2$ algorithm. In SMPE$^2$, agents enhance their own policy's discriminative abilities under partial observability, explicitly by incorporating their beliefs into the policy network, and implicitly by adopting an adversarial type of exploration policies which encourages agents to discover novel, high-value states while improving the discriminative abilities of others. Experimentally, we show that SMPE$^2$ outperforms a plethora of state-of-the-art MARL algorithms in complex fully cooperative tasks from the MPE, LBF, and RWARE benchmarks.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

该论文聚焦于**无通信的协作多智能体强化学习（MARL）**，特别关注在**部分可观测环境**中智能体如何高效协作。主要挑战包括：
- 部分可观测性导致的非平稳性，使智能体难以准确理解全局状态。
- 缺乏显式通信通道，智能体必须仅依赖自身局部观测进行决策。
- 稀疏奖励场景下，探索高价值状态极为困难。

现有方法（如对手建模）往往将状态表示学习作为与策略优化脱节的任务，且未考虑冗余信息过滤，也难以改善初始探索策略。论文旨在解决两个核心问题：
- **Q1**：智能体能否从局部观测中推断出有信息量的（潜在）状态表示，以增强自身策略的协调能力？
- **Q2**：智能体能否利用这些表示更有效地探索状态空间，发现更优策略？

### 2. 论文提出的方法论：核心思想、关键技术细节与算法流程

**（1）核心思想**  
提出**状态建模（State Modelling, SM）** 优化框架：允许每个智能体仅基于自身观测 $o^i$ 推断关于未观测全局状态的信念表示 $z^i$，且该推断过程直接面向优化联合策略的价值函数（而非作为辅助任务）。同时引入**AM过滤器（Agent Modelling Filters）** 过滤冗余、非信息性的状态特征。

**（2）关键技术细节**  
- **变分推断编码-解码器（ED）**：每个智能体 $i$ 学习概率编码器 $q_{\omega^i}(z^i|o^i)$ 和解码器 $p_{\phi^i}(\hat{o}^{-i}|z^i)$，目标为正则化重构损失（含 KL 散度）。
- **AM 过滤器 $w^i$**：为其他每个智能体 $j$ 学习可学习的权重 $w^{ij} = \sigma(\phi_w^{i}(o^j)) \in [0,1]$，用于在重构目标中屏蔽不重要的观测特征。
- **双重 Critic**：除标准 MAA2C 的 critic $V_\xi(s)$ 外，额外训练一个基于过滤后状态 $\hat{s} = o^i \oplus (w^i \cdot o^{-i})$ 的 critic $V_k(\hat{s})$，确保 $w^i$ 优化与策略价值相关。
- **对抗性探索**：对潜在信念 $z^i$ 使用 SimHash 进行计数式内在奖励，鼓励智能体发现新观测，从而迫使其他智能体更困难地重构，提升其建模能力。

**（3）算法流程（文字描述）**  
在每个时间步：
1. 智能体 $i$ 接收局部观测 $o^i_t$，采样信念 $z^i_t \sim q_{\omega^i}(z^i|o^i_t)$。
2. 根据增强策略 $\pi_{\psi^i}(a^i_t | h^i_t, z^i_t)$ 选择动作。
3. 环境返回全局奖励 $r_t$，每个智能体计算内在奖励 $\hat{r}^i_t = 1/\sqrt{n(\text{SH}(z^i_t))}$，组合总奖励 $\tilde{r}^i_t = r_t + \beta \hat{r}^i_t$。
4. 存储转移元组到经验回放缓冲区。
5. 周期性地：
   - 更新 actor、标准 critic 和 $w$ critic（基于 MAA2C 梯度）。
   - 更新编码-解码器（最小化重构损失 + KL 散度 + $w$ 的 L2 正则）。
   - 软更新目标网络。

完整算法见论文附录 Algorithm 1。

### 3. 实验设计：数据集/场景、Benchmark 与对比方法

- **Benchmark 环境**：
  - **MPE**：Spread（3、4、5、8 智能体）和 Double Speaker-Listener。
  - **LBF**：6 个任务（如 2s-9x9-3p-2f、4s-11x11-3p-2f 等，包含稀疏奖励）。
  - **RWARE**：3 个困难任务（tiny-2ag-hard、tiny-4ag-hard、small-4ag-hard）。

- **对比方法**：
  - 非探索类：MAA2C、COMA、MAPPO、ATM（基于 Transformer）。
  - 探索类：EOI（多样性）、EMC（好奇心）、MASER（子目标）、QMIX 变体。
  - 建模类：SIDE、多智能体扩展 LIAM（MLIAM）。

- **实验设置**：每个设置 6 个随机种子，报告 25%-75% 置信区间。总步数：MPE/LBF 为 10M，RWARE 为 40M。

### 4. 资源与算力

论文在附录 E.4.12 给出了各方法在 LBF 一个任务上的运行时间表（表 2），同时注明硬件环境为：  
**GPU RTX 3080ti、CPU 11th Gen Intel(R) Core(TM) i9-11900、64 GB RAM**。  
例如，SMPE$^2$ 在该任务上耗时约 1 小时 13 分，远快于 EOI（约 17 小时）、EMC（约 1 天 5 小时）等。  
但论文未明确报告总训练 GPU 时长或 GPU 数量。

### 5. 实验数量与充分性

论文进行了**大量实验**，包括：
- 在 3 个基准共约 11 个任务上的主实验结果。
- 多组消融实验：组件选择（无内在奖励、无 AM 过滤器、无 KL、无 L2 正则、标准 SimHash 替代）、第二 critic 必要性、超参数 $\lambda_{rec}$ 和 $\lambda_{norm}$ 的敏感性、$w^i$ 可解释性可视化、t-SNE 可视化 $z^i$ 表达性。
- 与 MLIAM 和 SIDE 的额外对比（图 6）。
- 灵活性验证：以 MAPPO 为骨干的 SMPE-PPO（图 22）。
- 内在奖励动态分析（图 19）。

**充分性评价**：对比方法全面（包括最新 SOTA），消融完整，且进行了量化分析（如 logistic 回归分类器）。实验设计公平（相同随机种子数、置信区间报告）。结论可信。

### 6. 论文的主要结论与发现

- SMPE$^2$ 在所有三个基准的多个任务上**显著优于** SOTA 方法，尤其在稀疏奖励的 LBF 和 RWARE 任务中，部分任务此前被标记为公开挑战。
- 状态建模（AM 过滤器 + 双重 critic）**直接面向策略优化**，比传统对手建模更有效。
- 对抗性探索策略**优于标准 SimHash**，能够引导智能体发现高价值状态并帮助改善其他智能体的建模能力。
- 消融实验确认：AM 过滤器、KL 散度、L2 正则、第二 critic 均为必要组件；$w^i$ 可学习到具有可解释性的过滤模式。

### 7. 优点

1. **方法创新**：将状态表示学习与策略优化紧密耦合，突破传统 AM 作为辅助任务的局限。
2. **冗余过滤机制**：通过 AM 过滤器自适应选择信息量大的特征，避免冗余信息对策略的干扰。
3. **对抗性探索**：基于信念的内在奖励自动鼓励智能体协作探索，而非仅追求多样性。
4. **实验全面性**：覆盖多个基准、多种环境规模，与 10+ 种基线比较，消融设计合理。
5. **可解释性**：通过 t-SNE 和 AM 过滤器可视化展示了信念表示的有用性。
6. **灵活性**：可与不同 MARL 骨干（MAA2C、MAPPO）结合。

### 8. 不足与局限

1. **计算复杂度**：每个智能体需维护编码-解码器、AM 过滤器、双重 critic，参数和损失项较多，训练开销高于基础 MAA2C。
2. **假设限制**：论文假设无通信，但真实应用可能允许有限通信；方法未在随机动力学或噪声观测下验证。
3. **可扩展性**：实验最大智能体数为 8（Spread）和 7（LBF），更大规模问题（>20 智能体）未测试。
4. **理论保证有限**：证明状态建模目标等价于原 Dec-POMDP 目标，但提出的优化目标（含重构正则项）仅为近似，最优性无法保证。
5. **超参数敏感性**：$\lambda_{rec}$、$\beta$ 等需手动调节，不同任务可能需不同设定。
6. **缺少与其他探索方法的直接比较**：例如 MAVEN、Fox 等未纳入对比，实验覆盖仍可扩大。

（完）
