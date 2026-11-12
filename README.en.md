# Scientific Ideation and Agent Evolution

[中文 README](README.md)

This repository provides two Agent Skills that can be used independently or together. **Skill 1, Scientific Ideation and Metacognition**, helps researchers make and act on the decision at hand. **Skill 2, Agent Evolution**, helps an agent with project memory capture reusable outcomes during work, review tasks afterward, and improve its practices as new evidence arrives.

## Choose a Skill and language

| Skill | English | 中文 |
| --- | --- | --- |
| **1 · Scientific Ideation and Metacognition** | [`scientific-ideation-en`](skills/scientific-ideation-en/) | [`scientific-ideation`](skills/scientific-ideation/) |
| **2 · Agent Evolution** | [`agent-evolution-en`](skills/agent-evolution-en/) | [`agent-evolution`](skills/agent-evolution/) |

Place the complete directory for the selected edition in an Agent Skills-compatible environment. Invoke it explicitly with `$` followed by the directory name. Choose one language per Skill. Each `SKILL.md` defines a workflow, `references/` contains guidance for on-demand reading, and Skill 2's `scripts/` provides an optional project memory utility. See the [Agent Skills documentation](https://developers.openai.com/plugins/concepts/skills).

## Skill 1 · Enter at the current research stage

| Starting material | Possible deliverable |
| --- | --- |
| An observation, seed paper, or broad topic | A researchable question, existing evidence, and a proposed contribution |
| Competing explanations or a draft protocol | Distinguishable predictions, a minimal comparison, and a study outline |
| Pilot results, execution logs, or a protocol deviation | Criteria for proceeding, revising, or pausing, and the relevant check |
| Data, code, or an unexpected result | A reproducible analysis, limits of inference, and a check that could change the interpretation |
| A manuscript or peer review | Claim-to-evidence mapping, revision locations, and follow-up tests |

The workflow is **locate the decision → do the work → adapt to feedback → deliver**. Start at the relevant step when the question or material is already clear. Deepen verification and the comparison of alternatives when evidence conflicts, the inference is sensitive, or the downstream costs are substantial. Apply evidence standards appropriate to the study type.

> Use `$scientific-ideation-en` to compare these two methods sections with my study plan. I can afford one pilot. Identify what the prior work already established, then propose one check that could change my decision to proceed or revise.

## Skill 2 · Build reusable memory during work

| When | What to retain |
| --- | --- |
| A useful outcome emerges | A prediction table, method, rubric, or confirmed decision, with its location, evidence, scope, and recheck trigger |
| The task closes | Reusable outcomes, helpful practices, hypotheses worth testing, and their limits |
| A later task uses a record | What was used, whether it still held, and whether the record or its scope should change |

Use metacognition to identify what needs adjustment and scientific creativity to generate and test ideas. A finished study design can be recorded immediately, with the scientific hypotheses it contains marked as untested. A practice that worked once can be saved as a candidate. Check it on new tasks and regression cases before making it a standing rule.

> Use `$agent-evolution-en` to continue the study design. Capture reusable prediction tables and decisions as they emerge, then do a short closing review. Mark untested explanations and practices as candidates.

Prefer project memory the host actually loads. The optional file-based utility records outcomes under `.agent-evolution/entries/`, retrieves them by keyword and scope, and keeps durable, recoverable memory in `.agent-evolution/MEMORY.md`. To review every task, configure the project entry point that the host reads and verify retrieval in a new session. See [Memory and Evaluation Operations](skills/agent-evolution-en/references/operations.md) and [Product Patterns and Integration](skills/agent-evolution-en/references/product-patterns.md).

## Design rationale

Both Skills use creative metacognition, Geneplore, and dual-space search. Skill 2 also uses CoALA to organize project memory. The sources are documented below. Human cognition research informs the workflow. LLM research helps define observable agent behavior. Effectiveness is an empirical question for evaluation on research tasks.

### Frameworks linked in the Skill

- Lebuda, I., & Benedek, M. (2023). A systematic framework of creative metacognition. *Physics of Life Reviews, 46*, 161–181. Organizes regulation before, during, and after a task around knowledge, monitoring, and control. [Source](https://doi.org/10.1016/j.plrev.2023.07.002)
- Finke, R. A., Ward, T. B., & Smith, S. M. (1992). *Creative Cognition: Theory, Research, and Applications*. MIT Press. The Geneplore framework supports iterating between generation and exploration. [Source](https://mitpress.mit.edu/9780262061506/creative-cognition/)
- Klahr, D., & Dunbar, K. (1988). Dual space search during scientific reasoning. *Cognitive Science, 12*(1), 1–48. Links hypothesis and experiment search, using distinguishable predictions to guide the next step. [Source](https://doi.org/10.1016/0364-0213%2888%2990007-9)

### Human metacognition and scientific creativity

- Flavell, J. H. (1979). Metacognition and cognitive monitoring: A new area of cognitive–developmental inquiry. *American Psychologist, 34*(10), 906–911. Distinguishes knowledge of people, tasks, and strategies and discusses metacognitive experience. [Source](https://doi.org/10.1037/0003-066X.34.10.906)
- Nelson, T. O., & Narens, L. (1990). Metamemory: A theoretical framework and new findings. *Psychology of Learning and Motivation, 26*, 125–173. Provides the object-level and meta-level account of monitoring and control. [Source](https://doi.org/10.1016/S0079-7421%2808%2960053-5)
- Ackerman, R., & Thompson, V. A. (2017). Meta-reasoning: Monitoring and control of thinking and reasoning. *Trends in Cognitive Sciences, 21*(8), 607–617. Connects monitoring cues to decisions about time and effort in reasoning. [Source](https://doi.org/10.1016/j.tics.2017.05.004)
- Kaufman, J. C., & Beghetto, R. A. (2013). In praise of Clark Kent: Creative metacognition and the importance of teaching kids when (not) to be creative. *Roeper Review, 35*(3), 155–165. Informs decisions about when the context calls for creative exploration. [Source](https://doi.org/10.1080/02783193.2013.799413)
- Lebuda, I., & Benedek, M. (2025). Contributions of metacognition to creative performance and behavior. *The Journal of Creative Behavior*. Examines associations between components of creative metacognition and human divergent-thinking performance. [Source](https://doi.org/10.1002/jocb.652)
- Kaplan, C. A., & Simon, H. A. (1990). In search of insight. *Cognitive Psychology, 22*(3), 374–419. Provides experimental grounding for changing the problem representation. [Source](https://doi.org/10.1016/0010-0285%2890%2990008-R)
- Gentner, D. (1983). Structure-mapping: A theoretical framework for analogy. *Cognitive Science, 7*(2), 155–170. Informs relational mapping and its limits when borrowing a paradigm. [Source](https://doi.org/10.1207/s15516709cog0702_3)
- Hu, W., & Adey, P. (2002). A scientific creativity test for secondary school students. *International Journal of Science Education, 24*(4), 389–403. Distinguishes traits, processes, and products of scientific creativity in an assessment for secondary school students. [Source](https://doi.org/10.1080/09500690110098912)
- Beaty, R. E., et al. (2026). The Scientific Creative Thinking Test (SCTT): Reliability, validity, and automated scoring. *Creativity Research Journal*. Provides question, hypothesis, and experiment generation as task categories. [Source](https://doi.org/10.1080/10400419.2026.2639038)
- Runco, M. A., & Jaeger, G. J. (2012). The standard definition of creativity. *Creativity Research Journal, 24*(1), 92–96. Informs assessing ideas for both originality and effectiveness. [Source](https://doi.org/10.1080/10400419.2012.650092)
- Dunbar, K. (1997). How scientists think: On-line creativity and conceptual change in science. In *Creative Thought: An Investigation of Conceptual Structures and Processes*. Observations in working labs inform anomaly handling, analogy, and revising explanations. [Source](https://www.ida.liu.se/divisions/hcs/seminars/cogsciseminars/Papers/Dunbar%2C%20K%20%281997%29%20How_scientists_think_On-line_creativity_and_conceptual_change_in_science.pdf)

### Research practice and methods

- National Academies of Sciences, Engineering, and Medicine. (2026). *On Being a Scientist: A Guide to the Responsible and Ethical Conduct of Research* (4th ed.). Provides practice context for responsible conduct, collaboration, openness, and stewardship. [Source](https://nap.nationalacademies.org/pubs/29488/)
- National Academies of Sciences, Engineering, and Medicine. (2019). *Reproducibility and Replicability in Science*. National Academies Press. Distinguishes computational reproducibility with the same inputs and procedures from replication with new data. [Source](https://doi.org/10.17226/25303)
- Nosek, B. A., Ebersole, C. R., DeHaven, A. C., & Mellor, D. T. (2018). The preregistration revolution. *PNAS, 115*(11), 2600–2606. Supports distinguishing prespecified analyses from later exploration. [Source](https://doi.org/10.1073/pnas.1708274114)
- Eldridge, S. M., et al. (2016). Defining feasibility and pilot studies in preparation for randomised controlled trials: Development of a conceptual framework. *PLOS ONE, 11*(3), e0150205. Distinguishes feasibility and pilot objectives in preparation for randomized trials. The Skill adapts feasibility-first thinking as a decision principle. [Source](https://doi.org/10.1371/journal.pone.0150205)
- Sandve, G. K., Nekrutenko, A., Taylor, J., & Hovig, E. (2013). Ten simple rules for reproducible computational research. *PLOS Computational Biology, 9*(10), e1003285. Supports tracking data, code, environments, and analysis steps. [Source](https://doi.org/10.1371/journal.pcbi.1003285)
- Hernán, M. A., & Robins, J. M. (2020). *Causal Inference: What If*. Chapman & Hall/CRC. Aligns causal targets, available data, and identification assumptions. [Source](https://miguelhernan.org/whatifbook)
- Braun, V., & Clarke, V. (2006). Using thematic analysis in psychology. *Qualitative Research in Psychology, 3*(2), 77–101. Provides a qualitative workflow example for thematic analysis. [Source](https://doi.org/10.1191/1478088706qp063oa)
- Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems, 24*(3), 45–77. Provides an example of objectives, design, evaluation, and communication for artifact development. [Source](https://doi.org/10.2753/MIS0742-1222240302)
- Page, M. J., et al. (2021). The PRISMA 2020 statement: An updated guideline for reporting systematic reviews. *BMJ, 372*, n71. Provides reporting guidance for systematic reviews. [Source](https://doi.org/10.1136/bmj.n71)

### LLM implementation and limits

- Yao, S., et al. (2023). ReAct: Synergizing reasoning and acting in language models. *ICLR*. Connects planning with actions that obtain external observations. [Source](https://openreview.net/forum?id=WE_vluYUL-X)
- Huang, J., et al. (2024). Large language models cannot self-correct reasoning yet. *ICLR*. Shows limits of intrinsic self-correction on the tested reasoning tasks. Consequential judgments use checkable evidence. [Source](https://proceedings.iclr.cc/paper_files/paper/2024/hash/8b4add8b0aa8749d80a34ca5d941c355-Abstract-Conference.html)
- Xiong, M., et al. (2024). Can LLMs express their uncertainty? An empirical evaluation of confidence elicitation in LLMs. *ICLR*. Motivates evaluating reported confidence separately from accuracy. [Source](https://proceedings.iclr.cc/paper_files/paper/2024/hash/6733cf15e10e2cd1d59af033c3bb8507-Abstract-Conference.html)
- Si, C., Yang, D., & Hashimoto, T. (2025). Can LLMs generate novel research ideas? A large-scale human study with 100+ NLP researchers. *ICLR*. Separates novelty and feasibility in NLP ideation and reports limits in diversity and self-evaluation. [Source](https://proceedings.iclr.cc/paper_files/paper/2025/hash/ea94957d81b1c1caf87ef5319fa6b467-Abstract-Conference.html)
- Liu, Y., et al. (2026). Perspectra: Choosing your experts enhances critical thinking in multi-agent research ideation. *CHI*. Illustrates researcher control over discussion branches and perspectives in human–AI collaboration. [Source](https://doi.org/10.1145/3772318.3791560)

### Memory architecture for Skill 2

- Sumers, T. R., Yao, S., Narasimhan, K., & Griffiths, T. L. (2024). *Cognitive architectures for language agents*. Transactions on Machine Learning Research. CoALA informs the distinction between episodes, semantic knowledge, and procedural practices. [Source](https://openreview.net/pdf/07475727a2787df12052196b9f2624497ef3c3bd.pdf)
- For product examples of in-task capture, closing review, scoped retrieval, and version recovery, see [Product Patterns and Integration](skills/agent-evolution-en/references/product-patterns.md).
