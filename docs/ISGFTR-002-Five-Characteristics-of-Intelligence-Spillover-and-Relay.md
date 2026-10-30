# ISGFTR-002 — Five Characteristics of Intelligence Spillover and Relay

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Conceptual taxonomy, mechanism hypotheses, and testable research agenda  
**Version:** 1.0.0 (theory-first)  
**Status:** Open hypothesis; definitions and mechanisms proposed for investigation, not empirically established laws  
**Date:** 2026-10-30  
**Companion:** [ISGFTR-001 — From Static Intelligence Boundaries to Open Capability Frontiers](ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md)

## Abstract

An intelligence system's observed task performance does not fully specify the ways in which its representations, procedures, and resources may be reused or extended. This paper proposes a five-part vocabulary for investigating such extensions: **spillover**, **generalization**, **fluidity**, **transfer**, and **relay**. The terms are related but noninterchangeable. Spillover identifies a useful capability outside an original design or training focus; generalization concerns performance on relevant unseen cases; fluidity concerns adaptive redirection of problem-solving activity across operational boundaries; transfer concerns the reuse or adaptation of knowledge or mechanisms across tasks or domains; and relay concerns the transmission and possible transformation of tasks, capabilities, evidence, or experience across units or time. We specify operational signatures, boundary conditions, failure modes, and candidate measurements for each. We then distinguish capability *mobility*, *utility*, and *growth*, and outline controlled studies to determine whether the five-part framing predicts useful discoveries beyond existing transfer-learning, multi-agent, and continual-learning baselines. The proposal is intended as an open research vocabulary and experimental agenda, not a claim of novelty over all related literatures or a proof of artificial general intelligence (AGI).

## 1. Motivation: Beyond a Single Capability Boundary

Intelligence is often evaluated by fixing a task distribution, model, interface, resource budget, and scoring rule, then reporting performance. Such evaluations are essential, but they do not necessarily describe all ways a capability may be redeployed. A representation learned for one task may be useful in another; a partial analogy may guide a new search; a tool or collaborating agent may bridge an otherwise inaccessible step; and a record of failed attempts may improve future routing.

These possibilities should not be conflated. The observation that a model performs well on unseen inputs is not equivalent to evidence that it can redirect work across tools. The ability to pass information between agents is not equivalent to persistent learning. An apparent new function may have been present in the training distribution, or may depend on external resources not disclosed in a benchmark.

ISGFTR-001 introduced four operational boundaries: **generative**, **observed**, **reachable**, and **evolvable**. The present paper develops five candidate characteristics that may help explain differences between these boundaries. The objective is to turn broad intuitions about intelligence being “open” or “flowing” into distinct, falsifiable research questions.

**Central question:** Under what conditions can an intelligence system exhibit useful capabilities beyond its initial task or structural context, and what evidence is required to attribute the extension to spillover, generalization, fluidity, transfer, relay, or their interaction?

## 2. Working Definitions and Units of Analysis

### 2.1 An operational capability claim

A capability claim should specify at least:

- **System boundary:** the model alone, or the model plus memory, tools, other agents, and control mechanisms.
- **Task family and distribution:** what problems are included and how novelty is established.
- **Available resources:** computation, time, tools, observations, and permissions.
- **Success criterion:** outcome quality, reliability, cost, and safety constraints.
- **Evidence status:** observation, inference, hypothesis, or independently replicated result.

A convenient notation is

\[
\mathcal{C}(S,D,B,E)=\operatorname{Performance}(S\mid D,B,E),
\]

where \(S\) is the specified system, \(D\) the task distribution, \(B\) the resource and operational budget, and \(E\) the evaluation protocol. This notation is a bookkeeping device, not a universal scalar definition of intelligence.

### 2.2 The five characteristics at a glance

| Characteristic | Core question | Minimal observable signature | What it does **not** imply |
|---|---|---|---|
| **Spillover** | Did a capability appear outside the original design or training focus? | Demonstrated useful function in a newly identified task class | That the function was unlearned, surprising to everyone, or unlimited |
| **Generalization** | Does performance extend to relevant unseen cases? | Held-out performance under specified distribution shifts | Autonomous tool use or durable learning |
| **Fluidity** | Can problem-solving activity adaptively cross operational boundaries? | Context-sensitive redirection among representations, tools, or processes | That every redirection is beneficial |
| **Transfer** | Can knowledge or mechanisms be reused in another task or domain? | Improvement over a matched no-transfer baseline | That structural similarity guarantees success |
| **Relay** | Can tasks, evidence, or capabilities be handed onward across units or time? | Traceable handoff and downstream use | That handoff creates a new capability |

The five terms can describe different aspects of one episode. They should nevertheless be coded separately in empirical studies.

## 3. Characteristic I — Intelligence Spillover

### 3.1 Definition

**Intelligence spillover** is the observed availability or emergence of a useful function outside the primary task, training objective, or structural purpose for which a capability was originally developed.

Spillover is a *relationship between original focus and subsequent use*, not a claim that a system violates its architecture or that a genuinely new mental faculty has appeared.

### 3.2 Candidate mechanisms

1. **Shared representation reuse:** a representation useful in the original task also encodes regularities relevant elsewhere.
2. **Latent procedure recombination:** familiar operations are composed into a previously untested procedure.
3. **Perspective reinterpretation:** the same structure becomes useful under a different goal or evaluation criterion.
4. **Environmental affordance discovery:** an existing capability becomes valuable when coupled with a newly available tool or context.
5. **Residual-triggered extension:** a newly encountered failure exposes a missing component that can be developed or recruited.

These are hypotheses about possible pathways. Their relative prevalence and distinctness require evidence.

### 3.3 Illustrative example

A system trained to analyze program text may also assist in constructing test cases. To claim spillover, investigators should establish the original training or design focus, the novelty of the downstream use, and the degree to which success depends on preexisting task exposure or auxiliary tools. The example alone does not establish emergent reasoning.

### 3.4 Failure modes and measurements

An apparent spillover can be an artifact of training contamination, benchmark leakage, broad but undisclosed original objectives, or a change in evaluation conditions. Useful measures include the number of independently validated off-focus task classes, the gain relative to matched baselines, and robustness under controlled perturbations.

**Hypothesis S1:** Reusable, task-invariant structural features will predict some off-focus capability gains after controlling for model size, exposure, and evaluation budget.

## 4. Characteristic II — Intelligence Generalization

### 4.1 Definition

**Generalization** is the preservation of useful performance on cases not used to fit or directly select the system, under a declared relationship between training and evaluation distributions.

The relevant distinctions include interpolation within familiar conditions, systematic compositional generalization, out-of-distribution robustness, and transfer across substantially different domains. These should not be reported as interchangeable achievements.

### 4.2 Folding–generalization as a conditional duality

ISGFTR proposes a possible connection between structural folding and generalization. When multiple experiences share a reusable core, folding may reduce task-specific detail and make the core accessible to new tasks:

\[
\{x_1,\ldots,x_n\}\xrightarrow{\text{structure-preserving folding}}K
\xrightarrow{\text{contextual unfolding}}\hat y_{\mathrm{new}}.
\]

This is a *conditional* mechanism. Compression that discards causal variables, boundary conditions, uncertainty, or rare counterexamples can impair generalization. The research target is therefore **structure-preserving folding with validated unfolding**, not compression as an automatic source of intelligence.

### 4.3 Operational tests

Use held-out combinations, domain shifts, counterfactual interventions, and novel compositions; report performance alongside confidence, compute, and error profiles. Distinguish the model's inherent generalization from gains produced by retrieval, search, or external agents.

**Hypothesis G1:** For some task families, representations that preserve cross-task invariants and relevant uncertainty will transfer more reliably than representations optimized only for in-distribution compression.

## 5. Characteristic III — Intelligence Fluidity

### 5.1 Definition

**Intelligence fluidity** is the ability of an adaptive system to redirect or redistribute problem-solving activity across representations, procedures, resources, or operational boundaries in response to context, opportunity, and feedback.

Fluidity concerns *process routing*, not merely possession of many skills. A fixed pipeline can be highly capable but relatively inflexible; a dynamically routed system can be fluid but ineffective.

### 5.2 Selective permeability

A promising mechanism is **selective structural permeability**: a boundary can admit partial representations, weak evidence, analogies, or candidate actions for exploration without granting them authority for final execution.

We distinguish two modes:

- **Exploratory permeability:** low-cost signals may cross a boundary to generate hypotheses or route attention.
- **Validated relay:** higher-consequence actions require evidence, provenance, permission, and conformance checks.

The distinction prevents “openness” from being mistaken for unrestricted access. Biological systems offer suggestive examples of associative activation and gating, but do not prove that any proposed AI mechanism reproduces neural computation.

### 5.3 A candidate flow policy

\[
\pi_{\mathrm{flow}}(a\mid c,e,r,b),
\]

where \(a\) is a candidate routing action, \(c\) context, \(e\) evidence, \(r\) risk, and \(b\) resource and permission constraints. This is an abstract policy notation; no specific implementation or learned policy is claimed.

Possible actions include staying with the current solver, invoking a tool, consulting another agent, reframing a problem, initiating a low-cost probe, or stopping.

### 5.4 Failure modes and measurements

Uncontrolled fluidity can cause distraction, tool thrashing, cascading errors, resource waste, and governance violations. Measure net utility of redirection against fixed-routing and random-routing controls, as well as unnecessary handoffs, latency, and policy compliance.

**Hypothesis F1:** Selectively gated, evidence-aware routing will outperform both rigid routing and unrestricted routing on some heterogeneous open tasks under matched budgets.

## 6. Characteristic IV — Intelligence Transfer

### 6.1 Definition

**Intelligence transfer** is the reuse, adaptation, or recomposition of information, representations, procedures, or capabilities from a source task or domain to a target task or domain.

Transfer is related to generalization, but often foregrounds an explicit source–target relationship and a measurable advantage over learning or solving the target without the source contribution.

### 6.2 Degrees of structural correspondence

A source and target may share:

- Surface features or vocabulary;
- Abstract relations or compositional patterns;
- Causal structure or operational constraints;
- Evaluation objectives or directional preferences;
- Tool affordances and executable interfaces.

Correspondence at one level does not imply correspondence at the others. Weak analogies can be useful *search cues*, but should not be treated as verified mappings.

### 6.3 Directional intuition and weak evidence

The proposed BM-ODWEI / Metric-Native Directional Intuition connection suggests a two-phase approach:

1. **Prospect:** use partial evidence, historical precedents, and directional compatibility to nominate transfer candidates.
2. **Validate:** probe candidate mappings with target-specific tests, counterexamples, and explicit failure criteria.

An **OTHERS** residual category can retain potentially useful unmatched signals, provided that their provenance, uncertainty, and later outcomes remain inspectable. It must not function as an unbounded positive score.

### 6.4 Negative transfer

A transferred procedure may harm target performance. Report both positive and negative transfer, including opportunity cost. A minimal outcome measure is

\[
\Delta_T = U_{\mathrm{target,with\ transfer}}-U_{\mathrm{target,without\ transfer}},
\]

with matched budgets and the same target evaluation. Here \(U\) is a declared task-specific utility, not an intrinsic intelligence score.

**Hypothesis T1:** Combining structural correspondence, directional weak evidence, and counterevidence will improve budget-normalized candidate selection over similarity-only heuristics on selected cross-domain tasks.

## 7. Characteristic V — Intelligence Relay

### 7.1 Definition

**Intelligence relay** is the traceable transmission, reuse, or transformation of tasks, representations, evidence, procedures, or capability access between intelligence units, or between successive episodes of the same system.

Relay does not require that every recipient learns. A handoff can support execution without modifying any persistent capability. The term therefore covers several mechanisms that must be separated analytically.

### 7.2 Spatial and temporal relay

**Spatial relay** occurs across agents, models, tools, organizations, or modules. Examples include delegating a subtask, handing off a validated procedure, or transferring evidence with provenance.

**Temporal relay** occurs across episodes. Examples include preserving failed probes, updating a routing policy, recording a precedent, or accumulating reusable task traces. Repeated execution can be a form of temporal relay when it contributes accessible records or state, even if it produces no immediate performance improvement.

### 7.3 Relay and learning are distinct

A relay event may yield:

- **Execution benefit:** a downstream task succeeds using an existing capability;
- **Information benefit:** the system reduces uncertainty without improving task success immediately;
- **Persistent learning:** a retained change improves future performance;
- **Loss:** errors, semantic drift, coordination overhead, or contaminated memory reduce performance.

Thus relay is neither synonymous with collective intelligence nor sufficient for recursive growth.

### 7.4 Evaluation

Track handoff fidelity, provenance completeness, downstream usefulness, coordination cost, retention across episodes, and performance on new tasks after the relay. Test against single-agent, no-memory, and nonadaptive coordination baselines.

**Hypothesis R1:** Traceable temporal relay with explicit validation and retrieval will improve retained task performance on some repeated and related task families relative to ephemeral handoffs at matched resource cost.

## 8. How the Five Characteristics Interact

The five characteristics are not stages that every intelligent system must traverse. They form a vocabulary for possible interactions.

One *candidate* sequence is:

\[
\text{Generalization}\rightarrow\text{Spillover Discovery}
\rightarrow\text{Fluid Routing}\rightarrow\text{Transfer}
\rightarrow\text{Relay}\rightarrow\text{Evaluation}.
\]

But alternative sequences are common. A relay may precede transfer; fluid routing may discover an external capability rather than a new internal one; transfer may occur without spillover; and generalization may be observed without any cross-unit relay.

### 8.1 Mobility, utility, and growth

Three outcome levels help prevent category errors:

| Level | Question | Example evidence |
|---|---|---|
| **Mobility** | Did a representation, task, or capability cross a boundary? | Valid trace of a mapping or handoff |
| **Utility** | Did the crossing improve the target outcome under constraints? | Controlled improvement in quality, cost, or reliability |
| **Growth** | Did it create a persistent, reusable increase in effective capability? | Retained improvement on later held-out tasks |

A system can be mobile without being useful, useful without learning, or capable of learning without being broadly general.

### 8.2 Four boundaries revisited

The **generative boundary** describes the objectives and conditions that produced the system; the **observed boundary** records demonstrated performance; the **reachable boundary** concerns capabilities accessible under specified tools, resources, and composition options; the **evolvable boundary** concerns potential future changes under specified learning and adaptation mechanisms.

These are condition-indexed descriptions, not nested circles that must always expand. A reachable capability may disappear when a tool is withdrawn; a learned system may regress; an observed benchmark may overestimate robust competence. The boundary framework is useful only when the conditions and evidence are explicit.

## 9. A Minimal Research and Measurement Program

### 9.1 Experimental design

For each source capability and candidate target:

1. Register the source system, training/design focus, known capabilities, and evaluation conditions.
2. Generate candidate off-focus tasks or transfer opportunities without revealing held-out target outcomes.
3. Record evidence for each of the five characteristics independently, including uncertainty and counterevidence.
4. Allocate a fixed probe budget using candidate-selection policies.
5. Evaluate outcomes on target tasks and compare with matched controls.
6. Test whether gains persist in subsequent tasks or episodes.
7. Publish successes, failures, negative transfers, and untested residuals.

### 9.2 Baselines

At minimum, compare against **random candidate selection**, **surface-similarity selection**, **fixed expert rules**, and **equal-budget direct solving without the proposed relay or flow mechanism**. Additional baselines should include established transfer-learning or multi-agent methods when applicable.

### 9.3 Candidate metrics

- **Validated discovery yield:** number of new, independently confirmed task capabilities per fixed exploration budget.
- **Transfer utility:** target improvement relative to no-transfer controls.
- **Routing value:** net task utility gained from adaptive routing relative to fixed routing.
- **Relay fidelity and retention:** correctness of transmitted information and persistence of later benefits.
- **Calibration:** alignment between predicted and observed outcomes *only when* probabilistic forecasts have been explicitly trained and calibrated.
- **Negative-transfer rate:** fraction of transfers that reduce target utility.
- **Governance compliance:** frequency and severity of unauthorized or unsafe boundary crossings.

Exploration-priority scores are not automatically probabilities. Any probability claims require separate calibration and out-of-sample testing.

## 10. Counterarguments, Limits, and Falsification

### 10.1 Existing terminology may already suffice

Transfer learning, domain generalization, modular computation, meta-learning, continual learning, tool use, and collective intelligence cover substantial parts of the phenomena described here. ISGFTR should earn its usefulness by producing clearer distinctions, better predictions, or more efficient discovery protocols—not by relabeling established results.

### 10.2 Apparent spillover may reflect hidden exposure

A supposedly new capability may have been directly or indirectly represented in training data. Without exposure audits or robust experimental proxies, attribution to spillover remains uncertain.

### 10.3 Fluidity may be costly rather than intelligent

Additional routing and communication can increase latency, coordination failures, and unsafe actions. If dynamic routing fails to outperform fixed or simpler policies under fair budgets, the proposed fluidity mechanism has not demonstrated added value.

### 10.4 Relay may amplify errors

Long chains can accumulate distortion and false confidence. Provenance, counterevidence, stopping rules, and evaluator independence are necessary research controls, not optional decorations.

### 10.5 Open structure does not imply unbounded growth or AGI

Compute, data, embodiment, observation, physical constraints, permissions, and evaluative quality can impose hard limits. Neither a successful transfer nor a recursively composed architecture establishes AGI. The model-centric and system-centric approaches are complementary possibilities, not an empirically settled dichotomy.

### 10.6 What would count against the framing?

Evidence against specific ISGFTR mechanisms includes: no predictive value beyond standard transfer baselines; no budget-normalized gain from selective routing; no retention after temporal relay; or systematic failure of proposed structural affinity measures to predict target outcomes. A broad conceptual taxonomy is not itself falsified by one failed mechanism, but its practical value weakens if none of its distinctions improve prediction, explanation, or intervention.

## 11. Interfaces to the Wider SI Research Program

The following are **proposed research connections**, not claims of validated integration:

| Research line | Potential contribution to ISGFTR |
|---|---|
| **Structural Folding / Unfolding** | Reusable cores, loss analysis, contextual reconstruction |
| **BM-ODWEI and Directional Intuition** | Weak evidence, OTHERS residuals, directional candidate discovery |
| **UCPSF** | Perspective-aware evaluation and multi-strategy scoring governance |
| **SIF** | Capability addressing, residual identification, structural growth |
| **UIERU** | Portable units, multi-trail exploration, spatial and temporal relay |
| **BUI-DSI** | Dynamic perspectives and structural difference analysis |
| **AQSI** | Autonomous generation and prioritization of exploration questions |
| **Structural RSI** | Evidence-driven revision, retention, and anti-Goodhart evaluation |

The research interfaces should remain open to alternative algorithms and independent replication. Conformance specifications should identify what must be recorded, not prescribe one privileged implementation.

## 12. Open Questions for Collective Learning

1. Can spillover be distinguished empirically from ordinary generalization and unobserved training exposure?
2. Which representations preserve enough causal or relational structure to support robust unfolding?
3. Can fluidity be measured independently of system size, number of tools, or search budget?
4. Which weak signals predict useful transfer, and which merely correlate with superficial similarity?
5. When does selective permeability improve exploration without undermining safety or reliability?
6. How can spatial and temporal relay be disentangled from simple retrieval or delegation?
7. What conditions allow a relay event to become persistent learning rather than transient task completion?
8. Can prospecting policies find valuable low-probability opportunities without being dominated by noisy OTHERS signals?
9. How should negative transfer, failed probes, and nonresults be represented so that other teams can reuse them?
10. What new evidence, if any, would justify connecting these mechanisms to broader AGI claims?

## 13. Research Relay Invitation

This document offers a vocabulary and experimental scaffold, not a finished theory. Researchers are invited to challenge the proposed distinctions, identify prior work that already addresses them, devise counterexamples, and contribute controlled experiments. Particularly valuable contributions include negative results, alternative definitions, calibrated prediction methods, open datasets of attempted transfers, and reproducible studies of relay fidelity and retention.

A useful collective relay should preserve **claim provenance, test conditions, counterevidence, unresolved residuals, and explicit limitations**. Progress is measured by what becomes more understandable and testable, not by how strongly a broad intelligence claim is stated.

## 14. Conclusion

Spillover, generalization, fluidity, transfer, and relay describe five related but distinguishable ways in which intelligence may operate beyond an initially specified task or structural context. Their value lies in supporting more precise observation and experimentation: recognizing an off-focus capability, testing generalization, tracing adaptive routing, measuring source-to-target transfer, and evaluating cross-unit or cross-time relay. None guarantees persistent growth. Together, however, they motivate an evidence-driven shift from passively waiting for surprising capabilities to systematically **prospecting, probing, validating, and learning from** candidate capability extensions.

The next paper, **ISGFTR-003**, investigates the conditional relationship between structural folding, generalization, and reusable cores.

---

## Suggested Figure Placement

- **Fig-002 — Four Intelligence Boundaries:** after Section 2, to situate the five characteristics within the boundary framework.
- **Fig-003 — Five Characteristics of Intelligence Flow:** after Section 2.2 or at the start of Section 8, to distinguish and connect the five characteristics.
- **Fig-008 — Recursive Relay and Collective Intelligence Growth:** optional cross-reference in Section 7 or Section 8; distinguish potential growth from demonstrated improvement.

*Figure files are planned research illustrations; this document does not imply that the figures or their depicted mechanisms have been empirically validated.*

## Related Research Areas (Orientation, Not an Exhaustive Bibliography)

Relevant bodies of research include transfer learning, domain generalization, compositional generalization, meta-learning, continual learning, modular neural networks, tool-augmented reasoning, multi-agent reinforcement learning, collective intelligence, swarm intelligence, and open-ended learning. A formal scholarly release should add verified primary citations and distinguish prior findings from ISGFTR-specific hypotheses. No priority or first-discovery claim is made here.

## Document Status

**ISGFTR v1.0.0 — theory-first.** Definitions, equations, and experiments in this document are proposed research constructs. No benchmark results, trained prospecting model, or validated AGI pathway are claimed.
