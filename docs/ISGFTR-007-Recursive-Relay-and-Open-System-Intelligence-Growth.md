# ISGFTR-007 — Recursive Relay and Open-System Intelligence Growth

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Directional research hypothesis, conceptual framework, and testable research agenda  
**Version:** v1.0.0  
**Status:** Open research proposal. The mechanisms below are hypotheses and proposed experiments, not established results.

## Abstract

An intelligence capability need not remain confined to the model, task, agent, or time at which it was first exercised. It may be reused by other components, translated into a new representation, incorporated into shared memory, or revised after repeated execution. This paper examines **recursive structural relay** as a candidate mechanism linking capability mobility to durable, transferable intelligence growth. We distinguish spatial relay among components from temporal relay across episodes; one-time coordination from experience-dependent learning; and observed performance gains from retained capability change. A minimal formalism describes relay events, evidence provenance, capability frontiers, and the possibility of losses from error propagation, interference, or resource consumption. We propose a guarded recursive cycle—execute, observe, evaluate, preserve, revise, and retest—and outline controlled experiments with frozen component models, persistent structural memory, and held-out tasks. The hypothesis is deliberately bounded: relay can preserve or transform intelligence-relevant information, but neither recursion nor openness guarantees improvement, generality, or AGI. The intended contribution is an explicit, falsifiable research interface for collective learning.

**Keywords:** structural relay; recursive intelligence; temporal relay; spatial relay; collective learning; open-system intelligence; capability growth; structural memory; negative transfer; evaluation governance; continual adaptation

## 1. Motivation: Beyond a Single Intelligent Performance

A benchmark commonly asks whether a system can solve a specified task under a fixed evaluation protocol. Such measurement is necessary, but it does not directly answer how the system acquires reusable competence after acting. A multi-component system may solve a task by invoking an existing specialist, and may later improve because it has retained evidence, updated routing rules, or developed a new reusable procedure. These are different phenomena.

Within ISGFTR, *relay* denotes a transfer of intelligence-relevant content or operational responsibility between units, representations, contexts, or episodes, subject to explicit provenance and interpretation. Relay can support spillover and transfer, but it is not itself proof of learning. The question here is narrower and testable:

> Under what conditions does repeated, evidence-bearing relay yield persistent, transferable capability improvement rather than temporary coordination or accumulated error?

This question connects the five characteristics defined in ISGFTR-002 with the system-level learning architecture of ISGFTR-006 and the prospective capability discovery process of ISGFTR-008.

## 2. Terminology and Research Boundaries

### 2.1 Intelligence unit

An **intelligence unit** is an operationally identifiable component that can perform or support a task: a model, tool, agent, policy, structured memory, evaluator, or composed subsystem. Units need not share the same internal representation or training method.

### 2.2 Relay event

A **relay event** is a documented transition in which a source makes a capability, task, artifact, observation, hypothesis, or evaluation available to a recipient for further use. A relay may be unsuccessful or may transfer misleading content; success is not part of its definition.

### 2.3 Recursive relay

**Recursive relay** occurs when outputs or evidence from a relay episode influence the selection, construction, or evaluation of subsequent relay episodes. Recursion is a feedback topology, not a guarantee of positive growth.

### 2.4 Open-system growth

**Open-system intelligence growth** is a retained, experience-dependent increase in effective capability over a specified task distribution and resource envelope, potentially mediated by changing components, links, policies, or memory. *Open* refers to adaptable boundaries and extensible interactions, not unlimited resources or unbounded performance.

### 2.5 Three outcomes that must not be conflated

| Outcome | Operational meaning | Does it establish learning? |
|---|---|---|
| Mobility | A capability or artifact is reachable in another context | No |
| Utility | A relay improves performance on a measured task | Not necessarily |
| Durable growth | Experience-dependent changes improve later, held-out performance and survive retention tests | Potentially, with controls |

## 3. Two Fundamental Relay Dimensions

### 3.1 Spatial relay

Spatial relay transfers work or evidence among distinct components or organizational loci. Examples include an agent invoking a specialist tool, a planner delegating verification to an evaluator, or a research group reusing a documented hypothesis from another group. Spatial relay may provide immediate access to capabilities that no single unit possesses, without modifying any component.

### 3.2 Temporal relay

Temporal relay transfers information or operational structure across episodes. Examples include retaining a failure trace, recording a reusable subroutine, updating a precedent registry, or changing a routing policy after evaluation. Temporal relay makes previous execution available to future execution.

### 3.3 Why repetition can count as relay

Repeated execution can produce a sequence of observations, counterexamples, timing measurements, and outcome labels. When those observations are preserved and made available to a later decision, repetition becomes a form of **evidence accumulation relay**. However, repeating the same action without recording usable evidence or modifying subsequent decisions is merely repetition, not demonstrated learning. Redundant, correlated, or biased samples may even reduce effective evidence quality.

A useful test is counterfactual: *Would the system behave differently in a justified and beneficial way if the accumulated evidence were withheld?*

## 4. A Minimal Structural Model

Represent the system at episode \(t\) by

\[
\mathcal{S}_t=(U_t,G_t,P_t,M_t,V_t,B_t),
\]

where \(U_t\) is the available set of intelligence units, \(G_t\) the interaction and calling graph, \(P_t\) the routing and flow policies, \(M_t\) the persistent memory or precedent store, \(V_t\) the evaluation and governance rules, and \(B_t\) the resource and action boundaries.

A candidate relay event is

\[
r_t=(u_s,u_d,a,c,e,p,\kappa),
\]

with source \(u_s\), destination \(u_d\), transferred artifact or responsibility \(a\), context \(c\), supporting evidence \(e\), provenance \(p\), and constraints \(\kappa\).

An update rule can be written abstractly as

\[
\mathcal{S}_{t+1}=\mathcal{U}(\mathcal{S}_t,r_t,o_t,v_t),
\]

where \(o_t\) is the observed outcome and \(v_t\) is a validation result. This is a specification of a research object, not a proposed universal learning algorithm.

Let \(Q(\mathcal{S};D,B)\) measure effective performance on evaluation distribution \(D\) under fixed resource conditions \(B\). An observed gain is

\[
\Delta Q_t=Q(\mathcal{S}_{t+1};D_{\mathrm{holdout}},B)-Q(\mathcal{S}_t;D_{\mathrm{holdout}},B).
\]

For a growth claim, the experiment must establish that the gain is statistically credible, persists after a retention interval, and cannot be explained solely by extra compute, leaked evaluation examples, or access to a previously unavailable expert.

## 5. The Recursive Relay Cycle

A candidate research cycle is:

1. **Locate:** identify a task gap or residual and the relevant units, tools, or memories.
2. **Propose:** construct candidate relay routes or structural modifications.
3. **Execute:** run a bounded probe or task under recorded conditions.
4. **Observe:** collect outcomes, costs, failures, and counter-evidence.
5. **Evaluate:** compare against baselines and apply independent checks.
6. **Preserve:** store useful evidence with provenance and uncertainty.
7. **Revise:** update routing, memory, policy, or composition only when justified.
8. **Retest:** measure retention and transfer on fresh tasks.

The loop may terminate, roll back, or branch into multiple trails. An evaluator should be able to reject an apparently promising update. No stage implies that the next stage must succeed.

**Suggested conceptual figure:** `../figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png` after this section. The figure should distinguish verified growth from speculative routes and depict failure/rollback paths.

## 6. Relay as a Bridge Between Existing and New Capabilities

A relay system can create useful outcomes through several mechanisms, which require different evidence standards:

- **Capability access:** route a task to an already capable unit; this increases accessible capability but does not establish new learning.
- **Capability composition:** coordinate complementary units to solve a task no unit solves alone; this establishes a compositional performance gain, not necessarily a retained new skill.
- **Structural distillation:** extract a reusable procedure, representation, or decision rule from a successful episode.
- **Residual bridging:** use failure evidence to identify missing interfaces, data, or subskills and design a bounded repair.
- **Policy adaptation:** change when and how units are selected based on measured outcomes.
- **Collective accumulation:** preserve findings so later participants can verify, refine, or reject them.

A system may progress from access to composition to retained structural learning. That progression is a hypothesis to test, not a mandatory evolutionary sequence.

## 7. Learning–Execution Decoupling Across Time

ISGFTR-006 distinguishes the unit executing a task from the level at which learning occurs. Recursive relay extends this distinction temporally. An executing model can remain frozen while a shared memory, graph, evaluator, or policy changes after each episode. The resulting system may learn even if its individual components do not undergo parameter updates.

This creates an experimental opportunity: hold component weights fixed, constrain tool availability, and permit only selected structural updates. If later held-out performance improves under equal budgets, researchers can investigate whether the improvement came from better organization, preserved experience, or retrieval. The attribution matters: simply expanding memory or making more calls may improve scores without demonstrating an efficient or generalizable learning rule.

## 8. Evidence, Provenance, and the Problem of Error Relay

Relay transfers errors as readily as insights. A speculative claim may be repeated by several agents and acquire the appearance of consensus despite originating from a single unverified source. Repeated executions may share the same bias. Structural changes may optimize the evaluator instead of the intended task.

Each retained relay artifact should therefore record at least:

| Field | Purpose |
|---|---|
| Source and transformation history | Trace where the claim or procedure originated |
| Task and environmental context | Prevent decontextualized reuse |
| Evidence and counter-evidence | Support critical re-evaluation |
| Validation status | Separate conjecture, probe, replication, and accepted use |
| Resource cost | Compare gains fairly |
| Known failure modes | Limit unsafe or misleading transfer |
| Expiration or recheck condition | Avoid treating stale evidence as permanent |

Evidence should not be counted as independent merely because it passes through multiple relay nodes. Provenance-aware aggregation and adversarial checks are essential to prevent self-reinforcing false confidence.

## 9. Growth, Loss, and Stability

A heuristic accounting identity is

\[
\Delta I_{\mathrm{net}}=\Delta I_{\mathrm{reuse}}+\Delta I_{\mathrm{composition}}+\Delta I_{\mathrm{learning}}-\Delta I_{\mathrm{loss}},
\]

where each term must be defined using a consistent evaluation measure before numerical use. The expression is conceptual; it is not a physical conservation law or a generally additive decomposition.

Possible losses include negative transfer, interface mismatch, catastrophic interference, memory contamination, coordination overhead, evaluation drift, and escalating computation. A successful system needs **stability–plasticity governance**: enough flexibility to adapt, and enough validation and rollback to preserve useful prior competence.

Open-ended exploration also requires explicit stopping criteria. More trails, more agents, or more recursion can reduce net utility when marginal information gain is lower than marginal cost or risk.

## 10. Directional Scoring and Relay Portfolio Selection

When several relay paths are available, a control plane can rank them by expected value rather than assume every path should be explored. A conceptual selection rule is

\[
V(r)=\widehat{p}_{\mathrm{success}}(r)\,\widehat{G}(r)+\lambda\widehat{IG}(r)-\widehat{C}(r)-\widehat{R}(r),
\]

where success probability, growth value, information gain, cost, and risk are estimates, not known quantities. Terms require compatible units or a separately justified multi-objective ranking scheme. In early research, an ordinal score may be more defensible than a numerical probability.

Weak-evidence directional intuition, discussed in ISGFTR-005, can propose unconventional routes. The control plane should allocate some budget to uncertain, potentially informative alternatives while reserving stricter gates for durable updates and consequential actions. This connects relay governance to UCPSF-style multi-perspective scoring and the prospecting questions of ISGFTR-008.

## 11. Spatial–Temporal Relay in Collective Research

Collective research is a practical case of combined relay. A team publishes a candidate structural mechanism; another group tests it on a different domain; a third identifies a counterexample; and a later system incorporates both the result and the counterexample into a revised protocol.

This is not necessarily a monotonic chain of discoveries. Failed replication, incompatible terminology, and changing environments can interrupt the relay. A useful research artifact should therefore be small enough to reuse, explicit about its assumptions, and accompanied by a validation interface.

For the ISGFTR project, the proposed relay objects include capability profiles, opportunity hypotheses, evidence records, probe reports, structural modifications, and negative results. They can be documented before any universal runtime is implemented.

## 12. Six Testable Hypotheses

**H7.1 — Temporal evidence relay:** Under matched execution budgets, a system retaining validated episode evidence will outperform a no-retention control on a specified family of later tasks.

**H7.2 — Structural policy adaptation:** With component models frozen, experience-dependent routing updates will produce retained gains beyond static routing and random policy updates.

**H7.3 — Composition-to-learning transition:** A compositional solution can sometimes be converted into a reusable procedure that improves subsequent related tasks without replaying the full original coordination process.

**H7.4 — Provenance-aware governance:** Tracking source dependence and counter-evidence will reduce false confidence and error amplification compared with naive relay aggregation.

**H7.5 — Selective exploration:** A bounded multi-strategy relay portfolio will discover useful transfers more efficiently than exhaustive or purely greedy routing in at least some heterogeneous task environments.

**H7.6 — Transferable growth:** A structurally updated system will show gains on genuinely held-out task variants, not only on repetitions or near-duplicates of the training episodes.

Each hypothesis is conditional and domain-bounded. Failure to observe the proposed effect under a credible protocol is informative evidence against the corresponding mechanism in that setting.

## 13. Controlled MVP: Frozen Units, Adaptive Relay

### 13.1 Setup

Construct a small system with three to five fixed-capability units, such as a planner, domain specialist, tool operator, verifier, and memory service. Freeze model weights and define a task suite with compositional, transfer, and adversarial variants. Partition tasks into development, validation, and untouched evaluation sets.

### 13.2 Experimental arms

| Arm | Configuration | Main question |
|---|---|---|
| A | Single unit, no relay | What can a component do alone? |
| B | Fixed multi-unit routing, no persistent memory | What does composition alone add? |
| C | Fixed routing plus persistent evidence memory | What does temporal evidence retention add? |
| D | Adaptive routing plus validated memory | Does structural learning add further gains? |
| E | Randomized routing or memory updates | Are gains due to the proposed learning rule? |
| F | Adaptive relay without provenance safeguards | What is the cost of weak governance? |

Control model versions, tool access, total inference calls, latency or token budgets, and evaluator exposure. Include repeated-task and held-out transfer conditions, as well as an ablation that removes accumulated memory after learning.

### 13.3 Primary measures

Measure held-out success, reliability, cost per successful task, retention after delay, transfer distance, error propagation, and rate of validated reusable procedure formation. Report uncertainty intervals and negative results. Where a claim concerns efficiency, compare performance at equal budgets rather than only maximum achievable performance.

### 13.4 Interpretation

If Arm D exceeds B and C on held-out tasks under matched budgets, this supports a limited structural-learning claim. If performance gains disappear after memory removal, the mechanism may be externalized memory rather than a changed routing policy. If all gains vanish on new task families, the result is task-specific adaptation, not broad transfer. None of these outcomes independently establishes AGI.

## 14. Failure Cases and Falsification Conditions

A credible research program should actively search for:

1. **Relay inflation:** many transfers, little net utility.
2. **Evidence echo:** repeated copies of one observation treated as independent support.
3. **Overfitting:** impressive gains on familiar tasks with no held-out transfer.
4. **Evaluator gaming:** policies improve the metric while degrading real task quality.
5. **Structural bloat:** increased graph complexity and maintenance cost without commensurate benefit.
6. **Negative transfer:** a reusable procedure harms performance outside its original domain.
7. **Unstable recursion:** repeated self-modification produces oscillation or degradation.
8. **Unjustified autonomy:** a system crosses permission or safety boundaries in pursuit of a score.

If adaptive relay repeatedly fails to outperform budget-matched fixed systems, or if apparent gains can be fully attributed to additional resources, the stronger growth hypothesis should be revised or rejected for those conditions.

## 15. Boundaries of the AGI Interpretation

Recursive relay is relevant to discussions of system-centric AGI because a system's reachable capabilities can exceed those of its isolated components. However, there is no implication that adding components, memories, or feedback loops yields general intelligence. Important constraints include incomplete world models, weak causal understanding, poor transfer, limited feedback, inaccessible tools, finite computation, and human governance requirements.

Model-centric and system-centric research can complement each other. A stronger component may improve the quality of candidate relay artifacts; a better relay system may make fixed components more effective. The scientific task is to measure the contribution of each mechanism without confusing architectural complexity with intelligence.

## 16. Open Research Questions

- What is the smallest evidence record sufficient for useful temporal relay?
- When does repeated execution create independent information rather than correlated noise?
- Can a system learn transferable relay policies without updating model weights?
- How should relay credit be assigned among sources, transformations, and evaluators?
- What operational tests distinguish retained new capability from retrieval of a prior answer?
- Can relay portfolios remain exploratory without destabilizing established competence?
- Which negative results are most useful to preserve for future capability prospecting?
- How should trust and validation thresholds vary across task risk levels?

## 17. Collective Learning and Research Relay Opportunities

This paper invites small, independently testable contributions rather than requiring adoption of the whole ISGFTR architecture. Useful relay contributions include a minimal provenance schema, a public benchmark of cross-episode transfer, a frozen-unit routing baseline, an analysis of correlated evidence, a negative-transfer case, or a replication of a structural-learning claim in a different domain.

A proposed contribution should state its assumptions, evaluation budget, held-out protocol, observed failures, and what remains unknown. The objective is to make progress legible to later researchers—even when the result is a well-documented counterexample.

## 18. Conclusion

Recursive relay offers a candidate bridge between intelligence mobility and durable growth. Spatial relay can make capabilities accessible across units; temporal relay can preserve experience across episodes; and validated structural updates may convert some interactions into reusable, transferable competence. The word *may* is central: repeated execution, multi-agent coordination, and recursive feedback are not by themselves evidence of learning.

The practical next step is a controlled, resource-matched experiment with frozen component models and explicit structural memory. If such systems exhibit retained held-out gains, researchers can identify the responsible mechanisms and their limits. If they do not, the resulting failures still sharpen the boundaries of the hypothesis. This document offers a research structure for open validation and collective relay, not a claim of universal intelligence growth.

---

## Figure Placement

**Primary planned figure:** `../figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png`, recommended after Section 5.  
**Secondary cross-reference:** `../figures/Fig-006-System-Centric-Multi-Level-Learning.png`, recommended after Section 7.  
**Optional cross-reference:** `../figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png`, recommended after Section 10.

All figures are conceptual until accompanied by experimental evidence.

## Relationship to Other ISGFTR Documents

- **ISGFTR-001:** intelligence boundaries and capability frontiers.
- **ISGFTR-002:** definitions and distinctions among the five characteristics.
- **ISGFTR-003:** structural reuse, folding, and transferable unfolding.
- **ISGFTR-004:** intelligence fluidity and selective permeability.
- **ISGFTR-005:** directional intuition and weak-evidence transfer.
- **ISGFTR-006:** system-centric and multi-level learning.
- **ISGFTR-008:** prospective discovery and evaluation of relay opportunities.
- **ISGFTR-009:** AGI implications and counterarguments.
- **ISGFTR-010:** open research architecture and collective learning.
- **SPEC-003:** prospecting, probing, and validation lifecycle.
- **SPEC-004:** structural relay and collective-learning contract.
- **CASE-002:** minimal system-centric collective learning.
- **CASE-003:** weak-evidence capability prospecting and relay.

**License:** See the repository's planned `LICENSE` file (Apache-2.0).  
**Citation:** See `CITATION.cff` after publication metadata is finalized.  
**DOI:** To be assigned following versioned release and archival deposit.
