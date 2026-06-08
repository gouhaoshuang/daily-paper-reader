---
title: "STRATUS: A Multi-agent System for Autonomous Reliability Engineering of Modern Clouds"
title_zh: STRATUS：面向现代云环境的自主可靠性工程多智能体系统
authors: "Yinfang Chen, Jiaqi Pan, Jackson Clark, Yiming Su, Noah Zheutlin, Bhavya Bhavya, Rohan R. Arora, Yu Deng, Saurabh Jha, Tianyin Xu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=fYW1PKawwJ"
tags: ["query:eca"]
score: 7.0
evidence: 基于多智能体的云可靠性工程系统，与分布式边缘云智能体架构主题相关
tldr: 现代云环境故障频发，人工SRE难以应对规模增长。STRATUS提出基于LLM的多智能体系统，包含故障检测、诊断、缓解等专用智能体，通过状态机组织以实现系统级安全推理与强制执行。该系统自主完成云服务可靠性工程，提升了故障响应效率与安全性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1385, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 413, \"height\": 215, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 617, \"height\": 295, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 476, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 478, \"height\": 243, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1067, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1009, \"height\": 804, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fyw1pkawwj/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 942, \"height\": 792, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 748, \"height\": 487, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 715, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 884, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1406, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1406, \"height\": 710, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1424, \"height\": 623, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 775, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 753, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1448, \"height\": 1072, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1282, \"height\": 609, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1460, \"height\": 926, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1401, \"height\": 593, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1394, \"height\": 399, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1398, \"height\": 483, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fyw1pkawwj/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1404, \"height\": 470, \"label\": \"Table\"}]"
motivation: 云规模系统故障频发，现有依赖人工的可靠性工程实践无法跟上规模增长。
method: 构建LLM驱动的多智能体系统，包含多个专用智能体（检测、诊断、缓解），以状态机形式组织并强制执行安全推理。
result: 系统能够自主完成云服务的可靠性工程任务，提升故障处理效率。
conclusion: STRATUS实现了云环境下自主可靠性的新范式。
---

## Abstract
In cloud-scale systems, failures are the norm. A distributed computing cluster exhibits hundreds of machine failures and thousands of disk failures; software bugs and misconfigurations are reported to be more frequent. The demand for autonomous, AI-driven reliability engineering continues to grow, as existing human-in-the-loop practices can hardly keep up with the scale of modern clouds. This paper presents STRATUS, an LLM-based multi-agent system for realizing autonomous Site Reliability Engineering (SRE) of cloud services. STRATUS consists of multiple specialized agents (e.g., for failure detection, diagnosis, mitigation), organized in a state machine to assist system-level safety reasoning and enforcement. We formalize a key safety specification of agentic SRE systems like STRATUS, termed Transactional No-Regression (TNR), which enables safe exploration and iteration. We show that TNR can effectively improve autonomous failure mitigation. STRATUS significantly outperforms state-of-the-art SRE agents in terms of success rate of failure mitigation problems in AIOpsLab and ITBench (two SRE benchmark suites), by at least 1.5 times across various models. STRATUS shows a promising path toward practical deployment of agentic systems for cloud reliability.

---

## 论文详细总结（自动生成）

# STRATUS论文详细中文总结

## 1. 核心问题与研究动机

- **背景**：现代云规模系统中，故障已成为常态。一个分布式计算集群可能经历数百次机器故障和数千次磁盘故障，软件缺陷和配置错误的频率更高。
- **问题**：现有的人工参与（human-in-the-loop）可靠性工程实践（Site Reliability Engineering, SRE）难以跟上云规模的增长，成本高、响应慢，迫切需要自主的、AI驱动的可靠性工程系统。
- **目标**：实现**自主SRE**——无需人工干预，自动完成故障检测、定位、根因分析和缓解，尤其是**缓解（mitigation）**环节，因为它涉及改变系统状态，安全风险最大。

## 2. 方法论与技术细节

### 核心思想
- 构建一个**基于LLM的多智能体系统**，将SRE任务分解给多个专用智能体，通过**确定性状态机**协调，确保系统级安全。
- 提出**事务性无回归（Transactional No-Regression, TNR）**安全规范，使智能体能够**安全地探索和迭代**，即使缓解失败也能回滚到之前的状态，保证系统恶化程度不会超过初始严重度。

### 多智能体架构
系统包含四个智能体：
- **检测代理（αD）**：观察环境，识别故障，建立初始错误状态。
- **诊断代理（αG）**：定位故障组件并进行根因分析（仅读操作）。
- **缓解代理（αM）**：制定并执行缓解计划（写操作）。
- **撤销代理（αU）**：在事务中止时执行撤销序列，恢复系统状态。

### 安全规范 TNR（第三章）
- **假设**：
  1. **写互斥（A1）**：任何时候只有一个写代理（αM或αU）执行，持有读者-写者锁。
  2. **忠实撤销（A2）**：撤销操作精确恢复检查点状态。
  3. **有限风险窗口（A3）**：每个事务的命令数上限为K（实验中设为20）。
- **事务语义**：
  - 检查点：记录起始状态s_pre。
  - 执行：顺序执行k个命令。
  - 提交/中止：若最终状态s_post不是崩溃态且严重度μ(s_post) ≤ μ(s_pre)则提交，否则中止并调用撤销。
- **核心引理**：任何外部可见状态（即事务之外的状态）的严重度始终不超过初始错误状态的严重度b。证明通过归纳法完成。

### 实现要点（第四章）
- 基于CrewAI框架，状态机控制流。
- **写互斥**：通过沙箱隔离和状态机序列化实现；检测/诊断代理只能读；缓解代理写前可dry-run。
- **忠实撤销**：基于栈的回滚机制，记录每个动作之前的系统状态对象（如Kubernetes资源），按顺序撤销。拒绝对不可恢复的破坏性操作，或将其替换为可恢复版本（如文件删除改为移动）。
- **有限风险窗口**：设置K=20（基于经验分析）。
- **其他**：自然语言转kubectl工具（NL2Kubectl）、引导诊断（通过调用链追踪定位故障区域）、终止条件（三个检查：告警清除、用户请求健康、系统组件健康）。

## 3. 实验设计

### 数据集与场景
- **AIOpsLab**：包含13个缓解问题（以及32个检测、28个定位、26个根因分析问题），模拟云系统故障（如Kubernetes环境中的配置错误、资源问题等）。
- **ITBench**：包含18个缓解问题，同样是实时的云系统模拟环境。

### 对比方法
- AIOpsLab基准：ReAct、Flash、AOL-agent（参考代理）。
- ITBench基准：ITB-agent。
- 所有方法都使用相同的LLM后端：GPT-4o、GPT-4o-mini、Llama 3.3（温度设为0）。

### 评估指标
- 成功率（Success Rate）、平均时间（秒）、步数（Steps）、成本（美元，基于token消耗）。
- 此外进行了消融实验（无重试、无撤销的重试）和步数限制影响分析。

## 4. 资源与算力

- **未明确说明**使用的GPU型号、数量或训练时长。因为STRATUS使用现成LLM（GPT-4o等，通过API调用），不需要训练。
- 论文提及每个基准任务运行STRATUS需要**15-20机器小时**。
- 实验中记录了每个任务的API成本（如GPT-4o成本约0.877美元/问题）。

## 5. 实验数量与充分性

- **缓解任务**：AIOpsLab 13个问题，ITBench 18个问题，以及检测、定位、RCA共86个问题（其中缓解13个独立问题）。
- **消融实验**：在AIOpsLab上进行了“无重试”和“无撤销重试”的消融（表3），在ITBench上也有消融（附录C）。
- **超参数实验**：温度对成功率的影响（附录F）。
- **步数限制影响**：分析了不同最大步数（3~30）下的成功率。
- **评估充分性**：实验覆盖了多种LLM模型、多个基准、多种任务类型，结果统计显著（报告了多次运行的中位数）。但缓解任务的样本量较小（13+18），可能不足以完全泛化。此外，ITBench中有8个问题可通过重启pod解决，简化了挑战，存在一定偏差。

## 6. 主要结论与发现

1. **缓解有效性**：STRATUS（GPT-4o）在AIOpsLab缓解问题上成功率达69.2%（9/13），在ITBench上达50.0%（9/18），分别比最佳基线（AOL-agent 46.2%, ITB-agent 9.2%）提升**1.5倍和5.4倍**。使用更弱的模型（GPT-4o-mini、Llama）时优势依然一致。
2. **TNR的关键作用**：消融实验表明，禁用重试后成功率降至15.4%；禁用撤销的直接重试成功率仅23.1%，远低于完整的69.2%。证明安全回滚和迭代探索至关重要。
3. **检测与定位**：STRATUS在检测任务上成功率超过90%，定位任务约51%，高于其他代理；RCA成功率较低（34.6%），但部分原因为基准标签歧义。
4. **安全保证**：TNR确保了任何外部可见状态不会比初始错误更差，为实际部署提供了信任基础。

## 7. 优点（亮点）

- **创新性安全规范**：首次形式化定义了用于自主SRE的TNR安全规范，将事务处理概念引入智能体系统，保证可回滚且不恶化。
- **多智能体设计**：通过专用智能体和确定性状态机解耦任务，增强了可定制性和可扩展性，同时使安全推理更容易。
- **实际可行性**：利用现代云平台（如Kubernetes）的状态协调原则实现undo，设计了沙箱、linting等安全机制，使得在生产环境中部署成为可能。
- **全面实验**：在两个公开基准上对比多种模型和基线，消融实验验证了TNR的必要性，结果有说服力。

## 8. 不足与局限

- **完美撤销的挑战**：在复杂真实环境中，并非所有系统状态变化都能被完美undo（如外部API副作用、持久化状态），论文承认这一局限，但指出云原生系统通常支持状态协调，可被利用。
- **并发支持有限**：当前版本假设单写代理，扩展至多写代理需要资源级锁机制（文中提出了扩展思路但未实现）。
- **实验规模受限**：缓解问题共31个（13+18），样本量较小；ITBench中部分问题可通过简单重启解决，可能低估了真实挑战。
- **模型依赖性**：性能高度依赖底层LLM能力，幻觉或规划失误可能产生错误动作，尽管TNR保证了回滚，但无效探索会增加成本和时间。
- **评估指标争议**：RCA的评估基准标签存在歧义，STRATUS的正确回答可能被误判为错误，影响结果可比性。
- **未涉及实际生产部署**：所有实验在模拟环境中进行，真实生产环境的复杂性和动态性（如多团队、版本变更、不可预见故障）未测试。

（完）
