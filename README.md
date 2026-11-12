# 科学创造与元认知

[English](README.en.md) · [中文版 Skill](skills/scientific-ideation/SKILL.md) · [English Skill](skills/scientific-ideation-en/SKILL.md)

一个用于科研工作的 Agent Skill。给它研究现象、文献、方案、数据或审稿意见，它从当前科研决策切入，完成相应工作，依据反馈调整策略，并交付下一步可以接手的结果。

## 选用版本

| 版本 | 目录 | 显式调用 |
| --- | --- | --- |
| 中文 | [scientific-ideation](skills/scientific-ideation/) | `$scientific-ideation` |
| English | [scientific-ideation-en](skills/scientific-ideation-en/) | `$scientific-ideation-en` |

把所选版本的完整目录放到支持 Agent Skills 的环境中。目录内的 `SKILL.md` 定义工作流，随附的科研实务操作表按需读取。通常启用一个版本即可。参见 [Agent Skills 说明](https://developers.openai.com/plugins/concepts/skills)。

## 从项目的当前阶段进入

| 手里已有 | 可以交付 |
| --- | --- |
| 一个现象、一篇种子论文或一个过宽的选题 | 可研究的问题、已有证据与拟议增量 |
| 几个可能的解释或一版方案 | 有区分力的预测、最小比较、设计草案 |
| 预实验、执行日志或偏差记录 | 继续、调整或暂停的条件，以及相应的检查 |
| 数据、代码或反常结果 | 可复核分析、推断边界、会改变判断的检查 |
| 手稿或审稿意见 | 主张与证据的对应、修改位置、后续检验 |

固定工作流为 **定位决策 → 完成当前工作 → 根据反馈调节 → 交付**。已有明确问题或材料时直接进入对应步骤。证据冲突、结论敏感或后续成本较高时，加深核查和替代解释的比较。适用的证据标准随研究类型调整。

> 用 `$scientific-ideation` 看这两段方法和我的方案。我只有一次预实验预算。请先确认原研究已经回答了什么，再给出一个能改变继续或调整决定的检查。

## 设计依据

Skill 正文链接直接采用的三个框架。其他研究依据集中列在本页。人的认知研究提供设计启发，LLM 研究帮助界定可观察的智能体行为。这里给出的是工作流，效果需要用实际科研任务评估。

### 直接进入 Skill 的框架

- Lebuda, I., & Benedek, M. (2023). A systematic framework of creative metacognition. *Physics of Life Reviews, 46*, 161–181. 用知识、监控与控制组织任务前、中、后的调节。 [来源](https://doi.org/10.1016/j.plrev.2023.07.002)
- Finke, R. A., Ward, T. B., & Smith, S. M. (1992). *Creative Cognition: Theory, Research, and Applications*. MIT Press. Geneplore 框架支持生成与探索反复切换。 [来源](https://mitpress.mit.edu/9780262061506/creative-cognition/)
- Klahr, D., & Dunbar, K. (1988). Dual space search during scientific reasoning. *Cognitive Science, 12*(1), 1–48. 把假设搜索和实验搜索结合，用可区分的预测指导下一步。 [来源](https://doi.org/10.1016/0364-0213%2888%2990007-9)

### 人的元认知与科学创造

- Flavell, J. H. (1979). Metacognition and cognitive monitoring: A new area of cognitive–developmental inquiry. *American Psychologist, 34*(10), 906–911. 区分关于人、任务与策略的知识，并讨论元认知体验。 [来源](https://doi.org/10.1037/0003-066X.34.10.906)
- Nelson, T. O., & Narens, L. (1990). Metamemory: A theoretical framework and new findings. *Psychology of Learning and Motivation, 26*, 125–173. 提供对象层与元层之间监控和控制的理论背景。 [来源](https://doi.org/10.1016/S0079-7421%2808%2960053-5)
- Ackerman, R., & Thompson, V. A. (2017). Meta-reasoning: Monitoring and control of thinking and reasoning. *Trends in Cognitive Sciences, 21*(8), 607–617. 说明推理中的监控线索与投入时间、努力的关系。 [来源](https://doi.org/10.1016/j.tics.2017.05.004)
- Kaufman, J. C., & Beghetto, R. A. (2013). In praise of Clark Kent: Creative metacognition and the importance of teaching kids when (not) to be creative. *Roeper Review, 35*(3), 155–165. 支持按情境决定何时扩大创造性探索。 [来源](https://doi.org/10.1080/02783193.2013.799413)
- Lebuda, I., & Benedek, M. (2025). Contributions of metacognition to creative performance and behavior. *The Journal of Creative Behavior*. 以人的发散思维任务检验创造性元认知各成分与表现的关系。 [来源](https://doi.org/10.1002/jocb.652)
- Kaplan, C. A., & Simon, H. A. (1990). In search of insight. *Cognitive Psychology, 22*(3), 374–419. 为通过改变问题表征推进探索提供实验依据。 [来源](https://doi.org/10.1016/0010-0285%2890%2990008-R)
- Gentner, D. (1983). Structure-mapping: A theoretical framework for analogy. *Cognitive Science, 7*(2), 155–170. 借鉴范式时关注关系对应和对应失效处。 [来源](https://doi.org/10.1207/s15516709cog0702_3)
- Hu, W., & Adey, P. (2002). A scientific creativity test for secondary school students. *International Journal of Science Education, 24*(4), 389–403. 区分科学创造的特征、过程和产物。原测验针对中学生。 [来源](https://doi.org/10.1080/09500690110098912)
- Beaty, R. E., et al. (2026). The Scientific Creative Thinking Test (SCTT): Reliability, validity, and automated scoring. *Creativity Research Journal*. 以科学问题、假设和实验设计作为产出类型参考。 [来源](https://doi.org/10.1080/10400419.2026.2639038)
- Runco, M. A., & Jaeger, G. J. (2012). The standard definition of creativity. *Creativity Research Journal, 24*(1), 92–96. 构思筛选同时考虑原创性和有效性。 [来源](https://doi.org/10.1080/10400419.2012.650092)
- Dunbar, K. (1997). How scientists think: On-line creativity and conceptual change in science. In *Creative Thought: An Investigation of Conceptual Structures and Processes*. 真实实验室观察为处理异常、类比和修订解释提供依据。 [来源](https://www.ida.liu.se/divisions/hcs/seminars/cogsciseminars/Papers/Dunbar%2C%20K%20%281997%29%20How_scientists_think_On-line_creativity_and_conceptual_change_in_science.pdf)

### 科研实践与方法

- National Academies of Sciences, Engineering, and Medicine. (2026). *On Being a Scientist: A Guide to the Responsible and Ethical Conduct of Research* (4th ed.). 为研究责任、协作、公开与材料管理提供实践背景。 [来源](https://nap.nationalacademies.org/pubs/29488/)
- National Academies of Sciences, Engineering, and Medicine. (2019). *Reproducibility and Replicability in Science*. National Academies Press. 区分同一数据和步骤下的计算复现，与新数据下的复验。 [来源](https://doi.org/10.17226/25303)
- Nosek, B. A., Ebersole, C. R., DeHaven, A. C., & Mellor, D. T. (2018). The preregistration revolution. *PNAS, 115*(11), 2600–2606. 为区分预先指定的分析和后续探索提供依据。 [来源](https://doi.org/10.1073/pnas.1708274114)
- Eldridge, S. M., et al. (2016). Defining feasibility and pilot studies in preparation for randomised controlled trials: Development of a conceptual framework. *PLOS ONE, 11*(3), e0150205. 区分可行性和试点工作的目的。适用范围为随机试验准备，Skill 将可行性优先用作一般决策原则。 [来源](https://doi.org/10.1371/journal.pone.0150205)
- Sandve, G. K., Nekrutenko, A., Taylor, J., & Hovig, E. (2013). Ten simple rules for reproducible computational research. *PLOS Computational Biology, 9*(10), e1003285. 支持记录数据、代码、环境及分析步骤。 [来源](https://doi.org/10.1371/journal.pcbi.1003285)
- Hernán, M. A., & Robins, J. M. (2020). *Causal Inference: What If*. Chapman & Hall/CRC. 将因果目标、可用数据与识别假设对齐。 [来源](https://miguelhernan.org/whatifbook)
- Braun, V., & Clarke, V. (2006). Using thematic analysis in psychology. *Qualitative Research in Psychology, 3*(2), 77–101. 提供适用于主题分析的质性工作示例。 [来源](https://doi.org/10.1191/1478088706qp063oa)
- Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems, 24*(3), 45–77. 为方法与技术开发的目标、设计、评价和传播提供范例。 [来源](https://doi.org/10.2753/MIS0742-1222240302)
- Page, M. J., et al. (2021). The PRISMA 2020 statement: An updated guideline for reporting systematic reviews. *BMJ, 372*, n71. 为系统综述提供报告标准。 [来源](https://doi.org/10.1136/bmj.n71)

### LLM 的实现依据与边界

- Yao, S., et al. (2023). ReAct: Synergizing reasoning and acting in language models. *ICLR*. 将计划与获取外部反馈的行动结合。 [来源](https://openreview.net/forum?id=WE_vluYUL-X)
- Huang, J., et al. (2024). Large language models cannot self-correct reasoning yet. *ICLR*. 所测推理任务中的内在自我纠错有局限。关键判断应有可复核依据。 [来源](https://proceedings.iclr.cc/paper_files/paper/2024/hash/8b4add8b0aa8749d80a34ca5d941c355-Abstract-Conference.html)
- Xiong, M., et al. (2024). Can LLMs express their uncertainty? An empirical evaluation of confidence elicitation in LLMs. *ICLR*. 提示对模型自报信心和实际准确性分别评估。 [来源](https://proceedings.iclr.cc/paper_files/paper/2024/hash/6733cf15e10e2cd1d59af033c3bb8507-Abstract-Conference.html)
- Si, C., Yang, D., & Hashimoto, T. (2025). Can LLMs generate novel research ideas? A large-scale human study with 100+ NLP researchers. *ICLR*. 在 NLP 构思中分别检验新颖性、可行性，并观察到多样性与自评的局限。 [来源](https://proceedings.iclr.cc/paper_files/paper/2025/hash/ea94957d81b1c1caf87ef5319fa6b467-Abstract-Conference.html)
- Liu, Y., et al. (2026). Perspectra: Choosing your experts enhances critical thinking in multi-agent research ideation. *CHI*. 为研究者掌控讨论分支与视角提供人机协作例子。 [来源](https://doi.org/10.1145/3772318.3791560)
