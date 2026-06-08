---
title: "G-Memory: Tracing Hierarchical Memory for Multi-Agent Systems"
title_zh: G-Memory：面向多智能体系统的分层记忆追踪
authors: "Guibin Zhang, Muxin Fu, Kun Wang, Guancheng Wan, Miao Yu, Shuicheng YAN"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=mmIAp3cVS0"
tags: ["query:eca"]
score: 8.0
evidence: 智能体间协作轨迹
tldr: 针对多智能体系统缺乏对协作轨迹记忆的问题，提出G-Memory分层记忆系统，通过三层图结构管理协作历史。实验表明该方法提升了智能体在协作任务中的表现，为多智能体协作记忆提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 820, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1451, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1029, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1421, \"height\": 701, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1444, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 1275, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 632, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1465, \"height\": 263, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 625, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1020, \"height\": 771, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 988, \"height\": 746, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mmiap3cvs0/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1045, \"height\": 749, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-mmiap3cvs0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 984, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mmiap3cvs0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 403, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mmiap3cvs0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 1162, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mmiap3cvs0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1442, \"height\": 966, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mmiap3cvs0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1202, \"height\": 549, \"label\": \"Table\"}]"
motivation: 现有记忆机制忽视智能体间协作轨迹，限制了多智能体系统的演化能力。
method: 提出基于组织记忆理论的三层图记忆系统，专门追踪和存储智能体间协作历史。
result: 在协作任务上显著提升了智能体的表现和记忆利用效率。
conclusion: 分层记忆能够有效捕捉协作轨迹，增强多智能体系统的自演化能力。
---

## Abstract
Large language model (LLM)-powered multi-agent systems (MAS) have demonstrated cognitive and execution capabilities that far exceed those of single LLM agents, yet their capacity for self-evolution remains hampered by underdeveloped memory architectures. Upon close inspection, we are alarmed to discover that prevailing MAS memory mechanisms (1) are overly simplistic, completely disregarding the nuanced inter-agent collaboration trajectories, and (2) lack cross-trial and agent-specific customization, in stark contrast to the expressive memory developed for single agents. To bridge this gap, we introduce G-Memory, a hierarchical, agentic memory system for MAS inspired by organizational memory theory, which manages the lengthy MAS interaction via a three-tier graph hierarchy: insight, query, and interaction graphs. Upon receiving a new user query, G-Memory performs bi-directional memory traversal to retrieve both \textit{high-level, generalizable insights} that enable the system to leverage cross-trial knowledge, and \textit{fine-grained, condensed interaction trajectories} that compactly encode prior collaboration experiences. Upon task execution, the entire hierarchy evolves by assimilating new collaborative trajectories, nurturing the progressive evolution of agent teams. Extensive experiments across five benchmarks, three LLM backbones, and three popular MAS frameworks demonstrate that G-Memory improves success rates in embodied action and accuracy in knowledge QA by up to $20.89\\%$ and $10.12\\%$, respectively, without any modifications to the original frameworks.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义
论文指出当前基于大语言模型的多智能体系统（MAS）虽然展现出超越单智能体的能力，但其自我演化能力受到记忆架构的限制。现有MAS记忆机制存在两大不足：
- **过于简单**：完全忽视了智能体间细粒度的协作轨迹；
- **缺乏跨试验与智能体定制化**：不同于单智能体已有的丰富记忆设计，MAS缺乏针对性的记忆管理。

为此，论文提出 **G-Memory**——一个受组织记忆理论启发的分层、智能体记忆系统，旨在通过三层图结构管理MAS中冗长的协作交互历史，使智能体团队能够从过去经验中学习并不断进化。

## 2. 论文提出的方法论
### 核心思想
G-Memory 将MAS的交互历史组织成三层图层次：
- **交互图（Interaction Graph）**：存储智能体间原子级的话语及时序关系。
- **查询图（Query Graph）**：存储已处理的任务查询及其元数据（状态、关联的交互图），节点间边表示语义关联。
- **洞察图（Insight Graph）**：存储从历史经验中提炼的可泛化高层洞察，每个洞察节点关联一组支持它的查询。

### 关键技术细节与流程
1. **粗粒度检索**：对新查询Q，利用嵌入相似度从查询图中检索top-k相关查询，再通过1-hop扩展获得候选集。
2. **双向记忆遍历**：
   - **向上遍历**：从候选查询节点投射到洞察图，获取相关高层洞察。
   - **向下遍历**：利用LLM对候选交互图进行稀疏化（提取核心协作子图），得到精炼的交互轨迹。
3. **记忆增强**：将检索到的洞察和交互片段，根据每个智能体的角色进行个性化筛选与注入，初始化各智能体的记忆状态。
4. **层次更新**：任务执行后，分别更新交互图（记录新轨迹）、查询图（添加新节点并建立关联）、洞察图（提炼新洞察并更新支持集）。

公式与符号：文中定义了MAS的图结构、各智能体元组、查询图、洞察图等数学形式化表示，以及检索、稀疏化、更新操作的具体函数。

## 3. 实验设计
### 数据集/基准
使用五个广泛采用的基准，覆盖三个领域：
- **知识推理**：HotpotQA（多跳问答）、FEVER（事实验证）
- **具身动作**：ALFWorld（家务任务）、ScienceWorld（科学实验）
- **游戏**：PDDL（策略游戏）

### 对比方法
- **单智能体记忆基线**：无记忆、Voyager、MemoryBank、Generative Agents
- **多智能体记忆基线**：MetaGPT-M、ChatDev-M、MacNet-M（分别来自对应框架的原始记忆设计）

### MAS框架与LLM骨干
- 三个MAS框架：AutoGen、DyLAN、MacNet
- 三个LLM骨干：gpt-4o-mini（闭源）、Qwen-2.5-7b、Qwen-2.5-14b（开源，本地部署）

### 参数配置
嵌入函数使用ALL-MiniLM-L6-v2；检索相关交互图数量M∈{2,3,4,5}；检索查询数k∈{1,2}。

## 4. 资源与算力
论文未明确说明使用的GPU型号、数量及训练时长。仅提及Qwen系列模型通过Ollama本地部署，GPT模型通过OpenAI API访问。实验为推理与评估，未涉及训练开销。

## 5. 实验数量与充分性
- **主实验**：在5个数据集×3个LLM骨干×3个MAS框架的组合下，对比了8种基线（包括无记忆），共报告了大量结果（见表1-3及附录）。
- **消融实验**：分别隔离洞察模块和交互模块的影响（图4c）。
- **敏感性分析**：对跳扩展数（hop）和检索查询数（k）进行了调参分析（图4a,4b）。
- **案例研究**：展示了三类任务中的实际记忆提示示例（图5）。
- **成本分析**：绘制了性能与token成本的权衡图（图3、7）。
- **延迟分析**：报告了部分设置的推理延迟（表4）。

**充分性评价**：实验覆盖广泛、对比公平（集成在同一框架下）、消融与敏感性分析揭示各组件贡献及鲁棒性，整体充分且客观。

## 6. 论文的主要结论与发现
1. **G-Memory一致提升性能**：在具身动作任务中最高提升20.89%，知识QA中最高提升10.12%，且无需修改原始MAS框架。
2. **MAS需要专门记忆设计**：多数已有记忆机制（如Voyager、MemoryBank）在MAS场景中反而可能降低性能，证明单智能体记忆不能直接迁移。
3. **分层结构有效**：高层洞察和细粒度交互轨迹均重要，其中交互轨迹贡献略大。
4. **资源友好**：G-Memory在实现高性能的同时，token消耗相对于其他记忆设计并未显著增加，甚至更优。

## 7. 优点
- **方法创新性**：首次针对MAS提出分层图记忆架构，结合组织记忆理论，设计精细。
- **即插即用**：作为模块可无缝嵌入主流MAS框架，无需修改原始框架。
- **双向记忆遍历**：同时提供高层抽象洞察和具体协作轨迹，适应智能体角色定制需求。
- **实验全面**：覆盖多种域、多种LLM骨干、多种MAS框架，对比充分，消融分析扎实。
- **效率验证**：不仅报告性能，还分析了token成本、延迟，证明实用性。

## 8. 不足与局限
- **任务多样性有限**：虽覆盖三个领域，但作者自述还需在更多任务（如医学QA）上验证。
- **依赖LLM质量**：记忆检索与稀疏化均依赖LLM，若底层LLM存在偏差或对抗攻击，可能放大错误。
- **未讨论隐私与公平性**：记忆存储涉及用户查询与交互历史，可能带来隐私风险。
- **资源消耗未明确量化**：缺乏具体GPU型号、推理时间等硬件资源的详细报告。
- **大规模扩展性未验证**：当智能体数量或历史轨迹极大增长时，图存储与检索效率有待后续研究。

（完）
