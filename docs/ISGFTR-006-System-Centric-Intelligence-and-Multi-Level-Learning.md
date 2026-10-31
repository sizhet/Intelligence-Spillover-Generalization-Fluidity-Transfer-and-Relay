# ISGFTR-006 — System-Centric Intelligence and Multi-Level Learning

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Directional research hypothesis, conceptual architecture, and testable research agenda  
**Version:** v1.0.0  
**Status:** Open research proposal. The mechanisms and system designs below are hypotheses, not established experimental results.

## Abstract

Many natural adaptive systems exhibit coordinated behavior that cannot be adequately described by listing the capabilities of isolated components. Ant colonies, honeybee swarms, animal groups, and nervous systems offer distinct examples of adaptation across interacting elements and timescales. These examples motivate—but do not prove—a research question for artificial intelligence: **Can a system of individually limited intelligence units acquire durable, transferable capabilities by learning how its units interact, organize, remember, and relay experience, even when the units' internal model parameters remain unchanged?** This paper develops a system-centric view of intelligence within the Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR) hypothesis. It distinguishes execution units from learning units, identifies multiple learning levels, and sketches a resource-bounded structural-learning architecture. It separates coordination gains from durable learning, specifies credit-assignment and evaluation difficulties, and proposes controlled experiments with frozen component models. The proposed contribution is a testable synthesis and an invitation to collective research, not a claim of a new universal learning law or an achieved route to AGI.

**Keywords:** system-centric intelligence; collective intelligence; multi-level learning; learning–execution decoupling; structural learning; multi-agent systems; adaptive routing; structural relay; capability retention; open-ended intelligence

## 1. Motivation: Intelligence Beyond the Isolated Model

A common question in contemporary AI is how much capability an individual model can acquire through training and inference. This is essential, but it does not exhaust the ways an intelligent system can become more capable. An operational system can also change its use of tools, routing rules, external memory, task decomposition, evaluation policies, and interactions among specialized components. Its effective capability may therefore change without a corresponding change in the parameters of any single model.

This observation motivates a distinction between **model-centric learning**, which emphasizes modification of a model's internal parameters or representations, and **system-centric learning**, which studies persistent changes to the organization and behavior of a larger adaptive system. These are complementary research lenses, not mutually exclusive alternatives.

The central question is:

> Under what conditions can a collection of limited intelligence units learn at the system level, retain that learning, and transfer it to previously untested tasks?

The word *learn* must be used carefully. A temporary improvement from allocating more compute or selecting a better pre-existing tool is not automatically learning. The system must retain some experience-dependent change that improves subsequent behavior under controlled evaluation.

## 2. Biological Inspiration: Rich Collective Behavior from Limited Units

Natural systems motivate several potentially useful design principles:

- **Social insects:** local sensing, environmental traces, recruitment, and feedback can support colony-level coordination without requiring each insect to maintain a complete global plan.
- **Animal groups:** interactions among individuals can produce coordinated movement or information aggregation. Coordination alone should not be equated with general reasoning.
- **Nervous systems:** distributed neural populations, recurrent feedback, plasticity, and modulation support adaptive behavior across multiple scales. Neurons are not interchangeable with software agents, and neural plasticity is not the same as changing a tool graph.
- **Human organizations:** specialization, records, conventions, and accumulated practices can preserve knowledge beyond the memory of any one participant; organizational learning may also fail or become rigid.

These systems differ profoundly in substrates, timescales, objectives, and available learning mechanisms. Their common lesson is modest: **the unit that visibly performs an action need not be the only locus of adaptation**. No single biological analogy establishes that a proposed AI architecture will generalize.

### 2.1 What Biology Does Not Establish

Natural collective behavior does not prove unlimited intelligence growth, the absence of individual learning, or a universal relay algorithm. Some seemingly intelligent group behaviors arise from fixed local rules; some depend on substantial individual learning; and some are brittle outside their evolved environments. A useful biomimetic hypothesis must identify a transferable mechanism and specify a falsifiable comparison.

## 3. Model-Centric and System-Centric Perspectives

A simplified model-centric update is

$$
\theta_{t+1}=\mathcal{U}(\theta_t,\mathcal{D}_t),
$$

where $\theta_t$ denotes model parameters and $\mathcal{D}_t$ denotes relevant training experience. This abstraction covers only part of the learning landscape: even model-centric systems may use retrieval, external state, or test-time adaptation.

For system-centric study, define an operational state

$$
\mathcal{S}_t=(U_t,G_t,R_t,P_t,M_t,E_t),
$$

where:

- $U_t$: available intelligence units and their declared capabilities;
- $G_t$: interaction, dependency, and invocation structure;
- $R_t$: task, evidence, and experience relay mechanisms;
- $P_t$: routing, scoring, control, and safety policies;
- $M_t$: retained memories, precedents, and evaluation records;
- $E_t$: environment, resource access, and feedback channels.

A candidate system-level learning operator is

$$
\mathcal{S}_{t+1}=\mathcal{L}_{\mathrm{sys}}(\mathcal{S}_t,\tau_t,f_t),
$$

with $\tau_t$ an observed execution trace and $f_t$ validated feedback. This is a **descriptive schema**, not a validated universal algorithm. Its value is to make the possible locations of adaptation explicit. The units' internal parameters can remain fixed while $G,R,P,M$ change.

### 3.1 Operational Definition of System Learning

A system has demonstrated system-level learning in a given experimental setting when (1) it experiences training or feedback episodes; (2) it retains a reproducible change in persistent system state; (3) the changed state improves a specified held-out outcome relative to an appropriate baseline; and (4) the improvement cannot be fully attributed to extra evaluation-time compute, leaked test data, or a change in task difficulty. This definition is task- and protocol-dependent, not a claim about general intelligence.

## 4. The Learning–Execution Unit Decoupling Hypothesis

**H-LEU — Learning–Execution Unit Decoupling**

> The unit or organizational level that executes an intelligent action need not coincide with the unit or level at which experience-dependent adaptation is stored and expressed.

For example, a fixed-parameter classifier may execute a classification while a system-level router learns which classifier to invoke under different conditions. A fixed-parameter language model may generate plans while an external precedent registry learns which plans and verification steps work for recurring task classes. In each case, the execution component is unchanged, but the larger system may improve.

This hypothesis has precedents in hierarchical control, ensembles, organizational learning, and multi-agent systems. Its proposed ISGFTR contribution is to connect this decoupling explicitly to capability spillover, structural relay, and measurable expansion of effective capability frontiers.

### 4.1 Three Distinct Outcomes

1. **Selection gain:** choosing a better existing unit more often. This may be valuable but need not create a new capability.
2. **Compositional gain:** a new arrangement of units solves tasks that no single unit could solve under the same constraints.
3. **Persistent growth:** experience-dependent structural changes improve future held-out performance and can be reused or transferred.

The strongest system-centric learning claim concerns the third outcome. Reports must not conflate these outcomes.

## 5. Six Levels of Potential System Learning

| Level | Adaptation target | Example persistent change | Principal risk |
|---|---|---|---|
| Unit | Internal capability | Parameter or local policy update | Forgetting or overfitting |
| Interaction | Communication and coordination | Revised handoff protocol | Coordination overhead |
| Structural | Graph of dependencies and roles | New or removed routing edge | Structural bloat |
| Relay | Transfer of tasks, evidence, and experience | Improved relay contract or precedent | Error propagation |
| Collective | Group-level memory and policy | Shared evaluator or registry update | Groupthink and contamination |
| Evolutionary | Population and organizational composition | Replacement or generation of units | Unbounded search cost |

These levels overlap. They should not be treated as a rigid biological hierarchy or as evidence that higher levels always improve performance. A useful research program isolates which level changed and measures its marginal contribution.

![Fig-006-System-Centric-Multi-Level-Learning.png](../figures/Fig-006-System-Centric-Multi-Level-Learning.png)

*Fig-006. Candidate learning loci across execution units, interactions, structures, relay histories, and collectives. The learning and execution mechanisms may be decoupled.*

## 6. Structural Learning Without Updating Component Weights

Consider $n$ frozen intelligence units $u_1,\ldots,u_n$. The system receives a task $x$, selects a composition $g$, executes it, obtains feedback, and updates a structural policy $\phi$:

$$
 g_t\sim\pi_{\phi_t}(g\mid x_t,M_t,C_t),
$$

$$
 y_t=\mathrm{Execute}(g_t,x_t;u_1,\ldots,u_n),
$$

$$
 (\phi_{t+1},M_{t+1})=\mathrm{Update}(\phi_t,M_t,x_t,g_t,y_t,f_t).
$$

Here $C_t$ represents resource and governance constraints. No claim is made that the router must be differentiable: candidate implementations include bandits, Bayesian selection, rule revision, search, or learned policies. Freezing unit weights is an experimental isolation choice, not a recommendation to prohibit model learning in practical systems.

### 6.1 What Counts as a Structural Delta?

A structural delta may add an invocation edge, remove a redundant stage, change role assignments, insert a verification gate, alter an evidence-sharing rule, or revise a memory retrieval index. Every delta should carry provenance, a motivating residual, estimated costs, and a rollback option.

### 6.2 Credit Assignment

A successful result may reflect a strong component, a useful combination, favorable task sampling, additional compute, or luck. Candidate attribution methods include randomized ablation, counterfactual replay, controlled substitution, and approximate marginal-contribution analysis. None fully resolves credit assignment in all adaptive systems. Evaluation should report uncertainty and the limits of attribution.

## 7. System-Centric Learning as a Mechanism for Spillover

Within ISGFTR, the five characteristics can interact with multi-level learning:

- **Spillover:** an existing unit becomes useful in a task family outside its original intended purpose.
- **Generalization:** learned routing or composition remains effective under task variation.
- **Fluidity:** the system redirects work and evidence among units as conditions change.
- **Transfer:** an experience-dependent structure improves a new target task compared with a baseline.
- **Relay:** reusable evidence, configurations, and lessons pass across units or episodes.

This is a *candidate causal chain*, not a necessary sequence. Some spillover occurs without relay, and some relay does not produce learning. The research goal is to determine when these mechanisms interact productively.

## 8. Spatial and Temporal Relay

**Spatial relay** transfers a task, intermediate representation, or evidence package among units. **Temporal relay** carries experience forward through stored traces, updated policies, or validated precedents. Repeated execution can become a form of temporal relay if its results are retained and used, but mere repetition without usable feedback is not learning.

A relay record might include source and target identifiers, task context, action taken, evidence provenance, counter-evidence, outcome metrics, uncertainty, and reuse conditions. Such records can support both reproducibility and selective forgetting when evidence becomes stale.

A system may become less capable when relay spreads incorrect assumptions. Thus, a useful design separates **exploratory relay** from **validated operational relay** and preserves rejected hypotheses as negative evidence rather than silently discarding them.

![Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png](../figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png)

*Fig-008. Recursive evidence-bearing relay across systems and time. Durable growth is an outcome to be tested, with negative results, saturation, and rollback explicitly represented.*

## 9. Selective Permeability and Directional Flow Policies

A completely closed modular architecture can miss useful cross-domain opportunities. A fully open one can flood units with irrelevant signals and increase error propagation. A candidate middle path is **selective structural permeability**: allow cheap exploratory crossings while requiring stronger evidence before operational adoption.

A flow policy $\pi_{\mathrm{flow}}$ may condition on task context, structural affinity, weak evidence, estimated benefit, uncertainty, risk, and resource budget. This policy is itself a possible learning target. It should be evaluated against fixed routing, fully open broadcast, and random routing baselines.

This connects to ISGFTR-004 (permeability), ISGFTR-005 (directional intuition), and the BM-ODWEI / MDI proposals (weak-evidence direction scoring). These are conceptual interfaces, not empirical proof of a shared algorithm.

## 10. Capability Frontiers in a System-Centric Setting

We distinguish three experimentally useful frontiers:

1. **Observed frontier:** task families on which a fixed protocol has demonstrated competence.
2. **Prospective frontier:** unverified task families selected for investigation using indirect evidence.
3. **Validated extended frontier:** newly demonstrated capabilities after structural adaptation, transfer, or relay.

Frontiers depend on task distribution, allowed resources, success thresholds, and measurement protocols. They need not be smooth, nested, or monotonic. A system may improve one domain while degrading another. A larger prospective frontier is not evidence of a larger validated frontier.

A further concept, **evolvable intelligence potential**, concerns expected future improvements under specified budgets and learning opportunities. It should be operationalized through learning curves or transfer performance rather than treated as an intrinsic scalar property of a model.

## 11. Proposed Minimal Experimental Architecture

**Research question:** Can three to five limited, frozen-parameter units acquire durable system-level improvements through structural learning?

A possible experimental platform contains:

1. **Specialist units:** several fixed models or deterministic solvers with deliberately complementary strengths and blind spots.
2. **Router and composition manager:** selects units, order, and verification steps.
3. **Shared evidence registry:** stores successes, failures, contexts, and provenance.
4. **Evaluator:** measures outcome quality, cost, and reliability against withheld references.
5. **Structural update mechanism:** proposes bounded changes to routing, composition, or memory rules.
6. **Governance gate:** prevents unverified structural deltas from silently entering the operational configuration.

The architecture is deliberately small. Its aim is to isolate a mechanism, not to simulate a biological brain or demonstrate AGI.

### 11.1 Task Design

Use task families that require complementary skills: for example, symbolic transformation, retrieval of permitted facts, constrained planning, and independent checking. Partition tasks by structural patterns rather than only by surface wording. Reserve genuinely held-out compositions and changed task distributions for transfer tests.

### 11.2 Experimental Conditions

- **B0 — Single-best-unit:** the strongest standalone component under matched resources.
- **B1 — Fixed composition:** a static hand-designed pipeline.
- **B2 — Random composition:** randomized routes under a matched compute budget.
- **B3 — Adaptive routing without persistent memory:** controls for online selection effects.
- **B4 — Persistent memory without structural change:** isolates retrieval and precedent gains.
- **T1 — Structural learning:** frozen units with persistent routing and composition updates.
- **T2 — Structural learning plus evidence relay:** adds provenance-aware temporal and spatial relay.

Where feasible, compare against a trained model-centric baseline with matched development cost; such cost matching is difficult and should be documented rather than assumed.

### 11.3 Measurements

Measure held-out success rate, cost per successful task, latency, robustness to distribution shift, retention after an interruption, reuse of learned structures, negative transfer, and calibration of the router's uncertainty. Report the number of trials, confidence intervals, seeds, and failure cases. If the system gains performance solely by spending more compute, that is not evidence of learning efficiency.

## 12. Testable Hypotheses

**H1 — Frozen-Unit Structural Learning:** With component weights fixed and compute controlled, a system that persistently adapts routing or composition will outperform fixed-composition and random-composition baselines on at least some held-out task families.

**H2 — Learning–Execution Decoupling:** Changes stored outside the executing units will produce measurable retained gains after the learning episodes end.

**H3 — Relay Benefit:** Provenance-aware evidence relay will improve future transfer efficiency relative to a structurally similar system without persistent relay records.

**H4 — Permeability Tradeoff:** A selective exploratory gate will outperform both fully closed and unrestricted sharing policies on a predefined quality–cost–risk objective in at least some heterogeneous settings.

**H5 — Composition Beyond Selection:** Some tasks will be solved by learned unit compositions that none of the individual units solves alone under the same task constraints; ablation will establish whether the gain is attributable to composition rather than hidden extra resources.

**H6 — Transfer and Retention:** Learned structural changes will transfer to at least one unseen task family and retain part of their benefit after a defined delay or system restart.

These are research hypotheses, not predictions that must hold universally. Null results are informative and should be reported.

## 13. Failure Modes and Counterarguments

### 13.1 Coordination Is Not Learning

A group can outperform its members through fixed rules. That is an important system effect but does not, by itself, demonstrate learning. The experiment must show experience-dependent retained changes.

### 13.2 Hidden Model-Centric Adaptation

If supposedly frozen units retain session state, change hidden caches, or access newly updated retrieval stores, an apparent structural-learning gain may be misattributed. Freeze or log all mutable state and state exactly what remains adaptive.

### 13.3 Benchmark Leakage and Adaptive Overfitting

Repeated exploration against the same test set can produce apparent progress without generalization. Use held-out distributions, delayed evaluation, and independent assessment.

### 13.4 Cost, Latency, and Fragility

Multi-unit systems can be expensive, slow, and sensitive to a single unreliable interface. Improvements must be compared at matched budgets and with robustness tests.

### 13.5 Collective Error Amplification

Shared memory can spread false claims and make independent units agree for the wrong reasons. Counter-evidence, source separation, provenance, and independent verification are essential.

### 13.6 Biological Overreach

Ant colonies, neurons, and software agents do not share a demonstrated universal learning rule. Biological inspiration should generate experiments, not substitute for them.

### 13.7 System-Centric AGI Does Not Follow Automatically

A system that coordinates specialists effectively may still lack autonomy, causal understanding, broad transfer, or reliable long-term learning. No result proposed here establishes a necessary or sufficient condition for AGI.

## 14. Evaluation and Governance Principles

A minimally credible evaluation should specify: the exact system boundary; all mutable states; component versions; allowed tools and resources; train–validation–test separation; success and failure criteria; structural deltas; rollback procedures; and provenance of evidence. Distinguish *discovery of a useful route* from *validation of a new capability*. Require stronger evidence for irreversible actions or consequential deployment than for sandbox exploration.

For collective research, release protocols and negative results when feasible, while protecting private data and avoiding unsafe or unauthorized external actions. A theory-first DOI should document how experiments could be reproduced without implying they have already been run.

## 15. Relationship to Earlier Structural Intelligence Proposals

This paper provides a system-level research bridge to several previously proposed Structural Intelligence components:

- **SIF:** structural capability addressing, residual-based growth, and evaluator governance.
- **UIERU:** composable intelligence units, multi-trail exploration, and bidirectional relay.
- **BUI-DSI:** dynamic structural differences and perspective-aware queries.
- **UCPSF:** multi-perspective scoring and control-plane policy selection.
- **AQSI:** generation of new exploration questions and unresolved capability gaps.
- **BM-ODWEI / MDI:** weak-evidence direction scoring and hypothesis prioritization.
- **Structural RSI:** controlled, evaluated changes to the system's own operating structures.

These connections identify possible interfaces for future work. They are not independent validation of the ISGFTR hypotheses, and no runtime implementation is claimed in this document.

## 16. Relationship to Established Research

Relevant established lines of research include multi-agent reinforcement learning, distributed optimization, ensemble methods, hierarchical reinforcement learning, swarm intelligence, organizational learning, collective intelligence, continual learning, meta-learning, modular neural networks, active learning, and open-ended evolutionary systems. These fields already investigate important parts of coordination, adaptation, credit assignment, and group-level learning.

The intended contribution here is a **carefully bounded synthesis**: connect learning–execution decoupling and structural adaptation to the ISGFTR concepts of spillover, fluidity, transfer, relay, and capability-frontier expansion, then define comparisons that could determine whether this synthesis adds practical predictive or engineering value. This document does not claim priority over those established fields. A future scholarly edition should add verified primary references and a detailed related-work comparison before making novelty claims.

## 17. Open Questions for Collective Learning

1. What is the smallest collection of fixed units that can demonstrate persistent structural learning rather than simple selection?
2. How should system-level credit be allocated when successful behavior depends on several interacting components?
3. Can a learned routing policy transfer across task distributions without memorizing task identities?
4. Which evidence records support useful temporal relay, and which merely accumulate noise?
5. Can a system learn selective permeability without suppressing rare but valuable distant transfers?
6. How can structural growth be constrained to prevent complexity from expanding faster than measurable utility?
7. What distinguishes durable new system capability from better exploitation of an existing capability portfolio?
8. How should researchers measure accessible and evolvable intelligence potential under explicit budgets?
9. When does model-centric training complement structural learning, and when is one approach more cost-effective?
10. Which biological principles remain useful after substrate-specific assumptions are removed?

These questions are offered as independently investigable relay points. Researchers may test, revise, or reject individual mechanisms without endorsing the entire framework.

## 18. Conclusion

System-centric intelligence directs attention from the competence of an isolated model to the adaptive capabilities of a larger, interacting system. Natural collective systems motivate this shift but do not validate any particular AI design. The central proposed hypothesis is that **learning and execution may be distributed across different organizational levels**, allowing fixed component models to participate in experience-dependent structural learning. Such learning may support capability spillover, cross-domain transfer, and recursive relay, but only when gains are retained, validated, and measured against appropriate controls.

A small frozen-unit experiment is a practical next step. Positive results would establish a limited system-level learning effect under specified conditions—not AGI. Negative results would help identify the boundaries of structural learning and improve the hypothesis. The purpose of this paper is to make that research path explicit and accessible to collective investigation.

---

## Relationship to Other ISGFTR Documents

- **ISGFTR-001:** static boundaries and open capability frontiers.
- **ISGFTR-002:** the five intelligence characteristics and their distinctions.
- **ISGFTR-003:** folding–generalization and structural reuse.
- **ISGFTR-004:** fluidity, selective permeability, and flow policy.
- **ISGFTR-005:** directional intuition and weak-evidence transfer.
- **ISGFTR-007:** recursive relay and durable open-system growth.
- **ISGFTR-008:** prospecting for candidate capabilities and experiments.
- **ISGFTR-009:** AGI implications, limits, and counterarguments.
- **ISGFTR-010:** open research architecture and collective learning.
- **SPEC-004:** proposed structural relay and collective-learning contract.
- **CASE-002:** proposed minimal system-centric collective-learning experiment.

**License:** See the repository's planned `LICENSE.txt` file (Apache-2.0).  
**Citation:** See `CITATION.cff` after publication metadata is finalized.  
**DOI:** To be assigned following versioned release and archival deposit.
