---
title: "OS-Sentinel: Towards Safety-Enhanced Mobile GUI Agents via Hybrid Validation in Realistic Workflows"
title_zh: OS-Sentinel：通过混合验证在真实工作流中增强移动GUI智能体安全性
authors: "Qiushi Sun, Mukai Li, Zhoumianze Liu, Zhihui Xie, Fangzhi Xu, Zhangyue Yin, Kanzhi Cheng, Zehao Li, Zichen Ding, Qi Liu, Zhiyong Wu, Zhuosheng Zhang, Ben Kao, Lingpeng Kong"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.431.pdf"
tags: ["query:mobile-agent"]
score: 8.0
evidence: 针对移动GUI智能体的安全风险与混合验证，属于部署中的关键挑战
tldr: 移动GUI智能体在完成用户任务时存在系统被破坏和隐私泄露等安全隐患。现有方法缺乏对真实工作流中安全风险的检测手段。为此，论文提出OS-Sentinel，并构建动态沙盒环境MobileRisk-Live及细粒度轨迹的安全检测基准。该工作为移动智能体安全研究建立了基础，为安全部署提供了验证依据。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 738, \"height\": 817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1575, \"height\": 515, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 682, \"height\": 555, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1681, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 632, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 638, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 707, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 762, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1607, \"height\": 541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 525, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 527, \"height\": 524, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1652, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long431/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1660, \"height\": 384, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1415, \"height\": 991, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 770, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 674, \"height\": 558, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 831, \"height\": 184, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 798, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 829, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1656, \"height\": 1996, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1641, \"height\": 1047, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1655, \"height\": 2314, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long431/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1332, \"height\": 263, \"label\": \"Table\"}]"
motivation: 移动GUI智能体存在系统破坏与隐私泄露等安全风险，且真实工作流中的安全检测尚属空白。
method: 提出OS-Sentinel混合验证方法，并构建MobileRisk-Live动态沙盒环境与安全检测基准用于识别危险操作。
result: 在真实轨迹基准上验证了安全检测能力，识别出系统被破坏与隐私泄露等风险。
conclusion: 为移动智能体安全研究提供基础，提升任务执行中的安全性并支持安全部署。
---

## Abstract
Computer-using agents powered by Vision-Language Models (VLMs) have demonstrated human-like capabilities in operating digital environments like mobile platforms. While these agents hold great promise for advancing digital automation, their potential for unsafe operations, such as system compromise and privacy leakage, is raising significant concerns. Detecting these safety concerns across the vast and complex operational space of mobile environments presents a formidable challenge that remains critically underexplored. To establish a foundation for mobile agent safety research, we introduce MobileRisk-Live, a dynamic sandbox environment accompanied by a safety detection benchmark comprising realistic trajectories with fine-grained annotations. Built upon this, we propose OS-Sentinel, a novel hybrid safety detection framework that synergistically combines a Formal Verifier for detecting explicit system-level violations with a VLM-based Contextual Judge for assessing contextual risks and agent actions. Experiments show that achieves 10%–30% improvements over existing approaches across multiple metrics. Further analysis provides critical insights that foster the development of safer and more reliable autonomous mobile agents. Our code, environment, and data are available at https://qiushisun.github.io/OS-Sentinel-Home/.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义

**研究动机与背景：**
- 基于视觉语言模型（VLM）的计算机使用智能体（Computer-using Agents）已能在移动端GUI上模拟人类操作，实现数字自动化。然而，这类智能体在真实工作流中可能产生系统破坏、隐私泄露等不安全行为，且威胁不仅来自恶意用户指令，还来自智能体自身的意外行为。即使在普通用户请求下，智能体也可能触发隐私违规、不当内容等安全问题。
- 现有研究存在显著空白：移动端安全基础设施不足（现有环境主要为桌面与Web设计）、应用覆盖有限、无法捕获完整系统状态（如运行时进程）；安全检测方法上，确定性规则验证难以扩展、模型方法过于通用或仅针对狭窄GUI攻击场景、多数研究偏向步级检测而与真实多动作轨迹脱节。

**整体含义：** 论文面向移动GUI智能体的安全检测问题，构建了动态沙盒环境（MobileRisk-Live）和带细粒度标注的真实轨迹基准（MobileRisk），并提出了混合检测框架OS-Sentinel，为移动智能体安全研究奠定基础。

## 2. 论文提出的方法论

**核心思想：** OS-Sentinel 采用“确定性验证 + 语义判断”的混合范式，融合两套互补机制：

- **Formal Verifier（形式验证器）**：统一、通用的确定性系统级检查器，利用系统状态迹（System State Trace, T_sys）进行三类检查：
  1. **系统状态完整性监控**：对文件系统元数据（大小、属主、修改时间戳）计算 SHA256 哈希，比较前后步哈希差异，发现越权改动；
  2. **敏感关键词检测**：基于维护的敏感词表（金融、个人标识、安全凭证等）对屏幕可见文本做精确匹配；
  3. **敏感模式匹配**：通过正则表达式识别邮箱、密码、信用卡号、电话号码等结构化敏感信息，加权计分。
  当系统完整性被破坏或聚合风险分超过阈值时，该步被判定为不安全。

- **Contextual Judge（上下文评判器）**：基于VLM的语义风险分析器，分两种粒度：
  - **步级监控**：处理当前观察-动作对 (o_t, a_t)，输出安全与否，支持实时拦截；
  - **轨迹级评估**：提供两种模式——Consecutive模式将轨迹切分为W步窗口分别评估，任一窗口不安全即整条轨迹不安全；Sampled模式均匀采样N个关键转换点（N自适应于模型上下文长度）。

- **混合判定**：最终决策通过可配置聚合函数 `Verdict(τ) = F_mode(Formal_rule(τ), Context_VLM(τ))` 实现，支持严格模式（F ≡ ∨，零容忍策略，漏报最小化，作为默认标准）和共识模式（F ≡ ∧，要求两组件一致，提升高置信度判断）。

**配套基础设施：**
- **MobileRisk-Live**：基于Android模拟器的动态沙盒，统一接口记录GUI观察（截图+无障碍树）、智能体动作与系统状态迹；预装48个应用（第三方案、系统原生应用、开发调试工具、Web服务），可灵活扩展并重置状态。
- **MobileRisk**：由204条真实轨迹构成（102条不安全+102条安全），每条轨迹包含GUI观察序列、系统状态迹、轨迹级二元安全标签、首不安全步位置t*、风险类别。

## 3. 实验设计

**数据集/场景：**
- 主评估在 **MobileRisk** 基准上进行（204条轨迹，覆盖10类安全风险：恶意使用、提示注入、有害内容、破坏性操作、隐私泄露、安全规避、UI操控、资源滥用、合规违规、过度自动化）。
- 动态环境对比实验在 **MobileRisk-Live** 上进行（选取104条无账号创建且不影响他人的指令，在真实时检测中对比动态环境与冻结轨迹的检测结果一致性）。

**任务生成：**
- 使用GPT-4o + M3A智能体提示框架生成轨迹；数据收集融合自动执行与人工标注，包含指令池构建、轨迹筛选（保留率约18%）、人工精修与标注三步流水线。

**对比方法（基线）：**
1. **规则评估器**：改编Lee et al. (2024)的MobileSafetyBench任务特定规则检查器；
2. **LLM-as-a-Judge**：基于a11ytree文本输入；
3. **VLM-as-a-Judge**：基于截图输入，在步级与轨迹级两种粒度上评估。

**检测器骨干模型**：
- 闭源模型：GPT-4o、GPT-4o mini、Claude-3.7-Sonnet、Claude-4.5-Sonnet；
- 开源模型：gpt-oss-120B、Qwen2.5-VL-7B-Instruct。

**评估协议**：
- **轨迹级**：Accuracy与F1分数；
- **步级**：延迟惩罚评分（delay-penalized scoring），`s = max(0, 1 − |t̂ − t*| / B)`，B=3窗口预算，精确匹配得1分，早报/晚报按时间距离线性衰减，超出预算得0分。

## 4. 资源与算力

论文**未明确说明**具体的GPU型号、数量或训练时长等算力投入。这主要是因为：
- 论文提出的方法（OS-Sentinel）本质上是一个**推理型检测框架**，不涉及从头训练新模型，而是调用现成的商用API模型（GPT-4o、Claude系列等）与开源模型（gpt-oss-120B、Qwen2.5-VL-7B）进行零样本安全判断。
- 文中提到一个实用性数据：API模型每次检测的平均延迟约为 **66ms**，7B规模的开源模型可以量化并在移动设备本地运行，说明框架具有实际部署可行性。
- 数据标注过程约投入 **300小时的标注人力**，而非计算资源。

## 5. 实验数量与充分性

**主要实验组：**
- **主实验**（表1）：在MobileRisk上对比OS-Sentinel与各类基线在步级、轨迹级（consecutive与sampled两种模式）的检测性能，覆盖6种骨干模型，共形成12行系统对比（每种骨干对应baseline与OS-Sentinel两行）。
- **动态与冻结设置对比**（表2）：在MobileRisk-Live与MobileRisk上并行运行104条指令，验证两者的评估结果一致性。
- **组件消融分析**（图5、图6）：比较仅用Formal Verifier、仅用Contextual Judge与完整OS-Sentinel的轨迹级Accuracy与F1。
- **类别层面分析**（图7）：按10种风险类别对比基线方法与OS-Sentinel的检测覆盖率。
- **模式消融**（表10）：比较严格模式（F ≡ ∨）与共识模式（F ≡ ∧）的性能差异。
- **Formal Verifier内部消融**（图10、图11）：分析状态完整性、敏感模式、敏感关键词三个检测模块的触发频率与占比。
- **错误分析/人机不一致分析**（附录D.3）：质性分析误报案例（如“清缓存”被误判为破坏性操作、过度自动化边界分歧）。

**充分性评估：**
- 实验覆盖多骨干（闭源+开源、不同规模）、多粒度（步级/轨迹级）、多基准维度（整体/消融/类别/动态对比），整体较为全面。
- 但数据集规模仅204条轨迹，属于中等偏小规模；检测任务为零样本推理（不使用训练数据），未对比监督式微调方法的潜力。
- 公平性方面，严格模式设计上偏向召回（漏报最小化），在低误报要求场景下可能需要调整，属于设计权衡而非实验不公。

## 6. 主要结论与发现

- **OS-Sentinel显著优于现有方法**：在步级和轨迹级检测上，相比规则评估器与纯VLM/LLM评判基线，OS-Sentinel在多个指标上实现 **10%–30%的改进**。以Claude-4.5-Sonnet为骨干时，步级准确率从24.6%提升至31.4%，轨迹级（consecutive）准确率从57.1%提升至73.0%。
- **混合设计的互补优势明显**：单独使用两个组件各有局限，但结合后性能持续优于任一组件（>80%准确率针对不安全实例），验证了确定性验证与语义判断的互补性。
- **动态与冻结设置高度接近**：在MobileRisk的冻结轨迹上评估可近似反映MobileRisk-Live中的真实检测表现，支持基准的可复现性。
- **模型无关性与实用性强**：7B规模开源骨干也能取得有竞争力结果（步级F1 57.4、轨迹级F1 66.1），API模型检测延迟低（66ms/次），具备实际部署可行性。
- **组件特性**：敏感模式匹配在Formal Verifier中触发最多（44.53%），状态完整性检查对破坏性操作尤为敏感；严格模式相比共识模式F1高17.4个百分点，但共识模式能更好过滤模糊误报。
- **安全优先设计原则**：论文强调漏报（错过恶意操作）的代价远高于误报（暂停验证），框架默认优先保证召回率，且可通过模式切换调节灵敏度。

## 7. 优点

- **开创性研究定位**：论文是移动GUI智能体安全检测中少有的系统性研究，同时填补了环境基础设施与检测方法两方面的空白。
- **混合检测范式新颖有效**：将确定性形式验证与VLM语义判断结合，克服了纯规则方法无法处理语义歧义、纯LLM判断难以捕获系统级变更的局限，形成"系统底层明确规则+语义层上下文推理"的双层防线。
- **多粒度、多层次的安全标注设计**：MobileRisk同时提供轨迹级标签、首不安全步定位和10类风险分类，支持步级实时防护、轨迹级事后审计等多种检测范式，并配套延迟惩罚评分机制。
- **动态环境与冻结基准分离设计**：MobileRisk-Live作为可扩展沙盒（支持48个应用、状态重置、指令重初始化），MobileRisk保证可复现性并隔离智能体能力对安全研究的干扰，两者结合兼顾真实性与可重复性。
- **可调安全策略**：严格与共识双模式设计允许开发者在零容忍与高置信度之间灵活调节，适应不同部署场景。
- **轻量实用**：7B模型可本地运行，66ms延迟支持实时护栏场景，工程上可行。
- **大量辅助性分析**：包括IAA验证（Cohen's κ=0.78，步级定位MAE 0.41步）、组件贡献、类别覆盖等多角度分析，实验体系严谨。

## 8. 不足与局限

- **数据规模有限**：MobileRisk仅204条轨迹，每类风险平均约20条，对于10类安全问题的细粒度评估统计效力有限；数据分布也偏向中等长度轨迹（5-12步为主），长轨迹场景覆盖率不足。
- **平台依赖性强**：Formal Verifier依赖Android系统状态迹获取（UIAutomator2、Android Runtime等），对iOS等封闭系统不适用；虽然文中指出可通过用户授权在Android上无root部署，但跨平台泛化仍是问题。
- **模拟环境与真实差距**：仿真环境无法完全复现真实网络条件下的推送通知、动态广告等干扰因素；部分应用存在反虚拟化机制，因此在物理设备上补采数据，说明环境代表性存在边际局限。
- **零样本检测的天花板**：所有检测器均无训练/微调，使用现成VLM的零样本判断能力；对于需要领域知识或微妙语义判断的风险（如合规性违规、过度自动化的边界），模型表现仍有限且难以通过该框架结构直接改进。
- **误报率偏高**：严格模式优先召回导致较高的误报率，例如"清缓存"等良性维护操作会因文件系统哈希变化被标记为"破坏性操作"，在实际部署中需要额外的人工确认成本。
- **Agent能力影响轨迹质量**：虽然冻结轨迹隔离了智能体能力对检测的影响，但轨迹本身由GPT-4o单一智能体生成，存在智能体行为的模型偏差，不一定覆盖其他类型智能体的安全失败模式。
- **敏感信息与伦理风险**：基准中包含涉及银行信息、隐私数据的轨迹，虽经脱敏处理并有严格数据使用声明，但在发布与传播中仍需持续关注隐私合规。

（完）
