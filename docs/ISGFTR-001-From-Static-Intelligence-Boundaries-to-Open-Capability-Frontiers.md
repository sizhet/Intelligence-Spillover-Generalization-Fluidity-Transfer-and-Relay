# ISGFTR-001 — From Static Intelligence Boundaries to Open Capability Frontiers

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Directional research hypothesis and conceptual framework  
**Version:** 1.0.0 (theory-first)  
**Status:** Open hypothesis; not an empirical demonstration  
**Date:** 2026-10-30

## Abstract

Discussions of artificial general intelligence (AGI) often conflate a system's training objective, observed performance, reachable capabilities, and potential for subsequent adaptation. These boundaries need not coincide. A model optimized for a narrow objective can acquire reusable representations; a system built from limited components can access additional capabilities through tools, structural recomposition, and relay. Conversely, neither observed transfer nor open-ended architecture establishes unlimited generalization or the arrival of AGI. This paper introduces the starting hypothesis of **Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)**: intelligence capabilities may extend beyond the tasks and structures in which they were originally developed, subject to representation quality, available resources, feedback, verification, and governance. We distinguish four operational boundaries, outline five candidate characteristics, and propose an evidence-driven program for prospecting, probing, and validating capability extensions. The aim is not to settle the AGI debate, but to make its neglected boundary questions more precise and testable, and to invite collective research and critical relay.

## 1. Motivation: Two Incomplete Inferences

The continuing expansion of large language model (LLM) capabilities has produced two opposed but similarly overconfident arguments.

One treats rapid progress on diverse tasks as evidence that increasingly general intelligence is inevitable. The other infers from next-token prediction as a training objective that language models cannot acquire capabilities extending beyond language completion. Neither conclusion follows directly from its premise.

A training objective is a specification of an optimization process, not an exhaustive catalog of the representations or skills that may emerge. Successful prediction can reward representations of regularities in programs, natural language, scientific descriptions, social interactions, and many other domains. Whether those representations support robust transfer to any particular task remains an empirical question.

Likewise, success across several domains does not establish reliable general competence across all domains. Performance can depend on prompt formulation, training overlap, external tools, task distributions, computational budget, and evaluation design. The existence of a useful transfer mechanism is not a proof of unbounded transfer.

**Research question:** How can we characterize, discover, and evaluate the capabilities that a model or intelligence system may reach beyond its presently observed task boundary, without presuming either a fixed narrow ceiling or an unlimited one?

## 2. Scope and Terminology

In this document, an **intelligence system** is an adaptive problem-solving arrangement comprising one or more models, procedures, representations, memory resources, tools, agents, and control mechanisms. This operational usage does not require consciousness or subjective experience.

A **capability** is an observable ability to achieve a specified class of outcomes under stated task, resource, reliability, and evaluation conditions. Capability claims should identify these conditions rather than treating competence as a context-free attribute.

A **frontier** is a task- and condition-indexed description of what is observed, plausibly reachable, or demonstrably extended. It need not be continuous, scalar, or geometrically smooth.

**Spillover** denotes the emergence or recognition of useful functions outside the original design or training focus. **Generalization** concerns performance on relevant but previously unobserved cases. **Fluidity** concerns adaptive redirection of problem-solving processes across representations, resources, and operational boundaries. **Transfer** concerns reuse or adaptation of knowledge or mechanisms across tasks or domains. **Relay** concerns the transmission and transformation of tasks, capabilities, evidence, or experience across units or time.

These concepts overlap, but should not be used as synonyms. Their separability is itself a research question.

## 3. Four Boundaries of Intelligence

We propose distinguishing four boundaries that are frequently conflated.

### 3.1 Generative or Training Boundary

The objectives, data, architectures, interfaces, and optimization conditions under which a model or system was developed. This boundary explains origins and constraints; it does not by itself enumerate all usable downstream capabilities.

### 3.2 Observed Performance Boundary

The set of tasks and conditions under which capability has been demonstrated by credible evaluation. It is evidence-dependent and can change as testing improves. It must be reported together with uncertainty, task coverage, and failure cases.

### 3.3 Accessible or Reachable Capability Boundary

The tasks a system can address with available tools, memory, external models, coordination, additional inference, or other authorized resources. It is conditional on the resource budget, interfaces, governance, and environment. A model's unaided performance and a tool-augmented system's performance should be measured separately.

### 3.4 Evolvable Capability Boundary

The capabilities that might become available through further learning, structural adaptation, recomposition, and recursive relay over a defined time and resource horizon. This is a prospective research construct, not an established maximum or a guarantee of improvement.

These boundaries are not necessarily nested in every operational definition. For example, a tool may increase reachable task coverage while reducing reliability under a strict latency constraint. A learned update may improve one domain while degrading another.

### 3.5 Boundary Non-Equivalence Hypothesis (H1)

> **H1:** The objective that generates or trains an intelligence system does not necessarily determine the full boundary of capabilities that the system can express, access, or subsequently develop.

H1 is a caution against invalid inference, not a claim that every model will generalize broadly. A useful empirical test must specify a model family, tasks, resources, and a measurable capability boundary.

**Suggested illustration:** `../figures/Fig-002-Four-Intelligence-Boundaries.png` (conceptual, not to scale).

## 4. Five Candidate Characteristics

The ISGFTR hypothesis proposes five potentially interacting characteristics.

### 4.1 Spillover

A structure learned or built for one purpose may support additional purposes. Spillover may be discovered accidentally or through systematic probing. To avoid post hoc storytelling, studies should record failed as well as successful candidate extensions.

### 4.2 Generalization

A system may preserve useful performance when inputs, contexts, or tasks change. Generalization is conditional: changes in data distribution, required reasoning depth, embodiment, or feedback can expose sharp limits.

### 4.3 Fluidity

An adaptive system may redirect attention, representation, search, tool use, or control toward a newly promising path. Fluidity should be measured by changes in routes and resulting utility, not by activity volume alone.

### 4.4 Transfer

Knowledge, policies, representations, or procedures may be adapted across contexts. Structural similarity can provide a weak cue, but superficial analogy can produce negative transfer. Successful transfer requires target-domain evidence.

### 4.5 Relay

Intelligence-relevant artifacts can pass between agents, tools, components, generations of execution, or research communities. Relay may preserve, transform, or degrade information. Repeated execution can serve as *temporal relay* when experience is captured and made useful for later adaptation; repetition without usable retention is not automatically learning.

**Working proposition (H2):** Some capability extensions can be explained by structural reuse, recomposition, perspective transformation, and residual-driven exploration. Their relative contributions must be tested rather than assumed.

**Suggested illustration:** `../figures/Fig-003-Five-Characteristics-of-Intelligence-Flow.png`.

## 5. Folding, Shared Structure, and Transfer

Compression and generalization are related but not identical. A representation that extracts task-relevant shared structure may support transfer because some incidental details of the original task are no longer required. Yet compression can also erase essential variables or boundary conditions and thereby impair transfer.

A useful conceptual sequence is:

`Experiences → Structure-preserving folding → Reusable core → Context-sensitive unfolding → Candidate capability`

Each arrow is conditional. The quality of the reusable core, the match between source and target, and the validity of unfolding determine whether the candidate becomes a demonstrated capability.

This motivates a research distinction between **mere compression** and **transfer-preserving abstraction**. Studies should compare both successful and failed transfers under matched resources, rather than infer generality from representational compactness alone.

**Suggested illustration:** `../figures/Fig-004-Folding-Generalization-and-Structural-Transfer.png`.

## 6. Open Boundaries and Directional Exploration

Many scientific and engineering workflows deliberately close a problem around fixed inputs, outputs, and interfaces. Such closure is valuable for reproducibility and safety. However, adaptive systems can also benefit from crossing boundaries: a task may reveal a related tool, a partial analogy, a relevant memory, or an unexpected intermediate objective.

The proposed principle is **selective structural permeability**: allow weak evidence and partial correspondences to generate candidate paths, while requiring stronger evidence before consequential execution, durable knowledge updates, or broad deployment.

A possible two-stage pattern is:

1. **Exploratory permeability:** identify promising directions using partial structure, weak evidence, analogies, historical precedents, and directional scoring.
2. **Validated relay:** evaluate candidates against target-domain evidence, safety constraints, provenance, and explicit acceptance criteria before promoting them to reliable capability claims.

This pattern should not be mistaken for a neuroscientific theory. Biological systems offer motivating examples of distributed association and gating, but the proposed computational architecture requires independent validation.

**Suggested illustration:** `../figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png`.

## 7. Model-Centric and System-Centric Paths

The ISGFTR framework distinguishes two nonexclusive paths toward broader capability.

**Model-centric development** improves the generality, reasoning, adaptation, or learning of a model itself.

**System-centric development** improves the capability of an arrangement of models, tools, memory, routing policies, evaluators, and cooperating units. The system may learn by changing connections, assignments, control policies, shared memory, or structural composition even when individual model weights remain fixed.

Biological collective behavior and multi-level neural organization motivate investigation of such mechanisms, but do not prove that a particular artificial system will attain AGI.

A particularly useful research hypothesis is **learning–execution unit decoupling (H3)**:

> The component that performs an action need not be the same component or organizational level at which adaptation and learning occur.

Experiments should distinguish genuine retained system improvement from temporary gains caused solely by extra compute, additional tools, or access to previously unavailable information.

**Suggested illustration:** `../figures/Fig-006-System-Centric-Multi-Level-Learning.png`.

## 8. From Passive Observation to Capability Prospecting

A major practical problem is that capability spillovers are often recognized only after someone happens to demonstrate them. Waiting for accidental discovery gives an incomplete and potentially biased view of the frontier.

We therefore propose **Intelligence Spillover and Transfer Prospecting (ISTP)**: an evidence-driven process for generating and prioritizing candidate capability extensions *before* their direct demonstration.

A candidate opportunity can be represented conceptually as:

`O = (source capability, target task, transfer path, evidence, relay resources, constraints)`

Potential evidence includes structural affinity, directional compatibility, historical positive and negative transfer, available relay pathways, and residual-bridging opportunities. Weak evidence may guide cheap probes; it should not be reported as proof or as a calibrated probability without validation.

An exploration policy may balance expected benefit, cost, risk, uncertainty, and information gain. These quantities require explicit operational definitions and should not be combined as if they shared units automatically.

The proposed cycle is:

`Prospect → Probe → Validate → Relay → Learn → Prospect`

Failed probes are valuable evidence if retained with their conditions and counterexamples. A successful probe expands the *validated* frontier only within its tested scope.

**Working proposition (H4):** A calibrated, evidence-aware prospecting policy may discover useful transfers more efficiently than random probing or a simple structural-similarity baseline under matched budgets.

**Suggested illustration:** `../figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png`.

## 9. Open-System Growth Is Not Guaranteed Growth

An open architecture can route tasks, share experience, and reorganize itself without necessarily increasing effective intelligence. Potential losses include negative transfer, semantic drift, interface mismatch, correlated agent errors, unreliable evaluators, feedback contamination, and escalating resource costs.

A conceptual accounting identity is:

`Net capability change = verified gains from reuse, relay, and learning − measured degradation and overhead`

This is not a universal additive intelligence law. The terms must be operationalized for a specified evaluation distribution and utility function; overlapping gains must not be double-counted.

In particular, *mobility*, *utility*, and *growth* should be measured separately:

- **Mobility:** Can a capability or useful artifact cross a boundary?
- **Utility:** Does that crossing improve target-task outcomes under relevant costs and risks?
- **Growth:** Is a new capability retained and reusable beyond the immediate episode?

**Suggested illustration:** `../figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png`.

## 10. Implications for AGI: A Research Question, Not a Forecast

ISGFTR does not establish that an LLM will become AGI, that a multi-agent system is necessarily general, or that the reachable frontier has no upper bound. It instead questions whether model training objectives and current benchmark results are sufficient to characterize all system-level capabilities.

A useful AGI evaluation program may need to examine both independent model competence and system-level access to tools, learning, coordination, and sustained adaptation. Results should disclose the extent of external assistance, autonomy, resource use, and reliability. The distinction matters: an ensemble that succeeds through extensive human intervention is not equivalent to an autonomous system that discovers and validates new skills.

A broader claim about AGI requires an explicit definition of generality, autonomy, robustness, and learning, together with tests across diverse tasks and environments. The present paper offers no such proof.

## 11. Testable Research Agenda

The following questions define an initial empirical program.

| ID | Proposed test | Baseline / counterfactual | Evidence of failure or limitation |
|---|---|---|---|
| T1 | Predict cross-task reuse from shared structural features | Similarity-only and random selection | No predictive gain on held-out target tasks |
| T2 | Compare directional weak-evidence probing with fixed task routes | Fixed routing and equal-budget random probing | No improvement in validated discoveries per unit cost |
| T3 | Test selectively permeable interfaces | Always-open and always-closed interfaces | More interference, risk, or cost than benefit |
| T4 | Test multi-unit structural learning with frozen model weights | Fixed topology, fixed memory, equal tools/compute | No retained out-of-sample improvement |
| T5 | Compare relay with and without evidence provenance and counterexamples | Relay without structured evidence records | No improvement in reliability or learning retention |
| T6 | Evaluate opportunity scores against future probe outcomes | Uncalibrated heuristic ranking | Poor ranking, calibration, or robustness under distribution shift |

Every study should report negative results, distribution shifts, uncertainty, resource costs, and the difference between exploratory evidence and validated performance. Pre-registration and held-out evaluations are encouraged where practical.

## 12. Related Research and Positioning

The proposed framework intersects established work in transfer learning, domain adaptation, representation learning, meta-learning, continual learning, modular and tool-augmented AI, multi-agent reinforcement learning, collective intelligence, swarm intelligence, open-ended learning, and scientific discovery systems.

ISGFTR does **not** claim to originate these fields or their underlying mechanisms. Its proposed contribution is to organize several boundary-related questions into a common conceptual and experimental agenda: how capabilities extend, how extensions can be prospectively discovered, when relay yields retained learning, and how system-level growth can be assessed without assuming unbounded generality.

A future literature review should identify precise precedents, competing definitions, and empirical baselines before stronger novelty claims are made. This theory-first release intentionally avoids presenting an incomplete bibliography as a comprehensive survey.

## 13. Limitations and Counterarguments

1. **Terminological overlap:** Spillover, transfer, and generalization may be difficult to separate empirically. If they add no explanatory or predictive value, the taxonomy should be simplified.
2. **Anthropomorphic interpretation:** Metaphors such as flow and permeability should not be mistaken for literal fluids or human-like intentionality.
3. **Selection bias:** Retrospective success stories can overstate the prevalence of transfer; negative probes must be recorded.
4. **Weak evidence and false positives:** Open exploration can increase discovery while also producing more errors and wasted resources.
5. **System-level confounding:** Additional tools, compute, data, or human guidance may explain gains attributed to structural learning.
6. **No implied universality:** Biological analogies and isolated engineering cases cannot establish a universal law of intelligence.
7. **No AGI guarantee:** Neither capability extension nor recursive relay implies unlimited intelligence growth.

These objections are part of the research program, not obstacles to be dismissed.

## 14. Collective Learning and Structural Relay

The project is intended as an open research starting point. Researchers may contribute independent conceptual critiques, benchmark designs, negative examples, transfer datasets, weak-evidence scoring approaches, or system-learning experiments.

A useful relay contribution should specify:

- the source capability and target task;
- the proposed transfer or spillover mechanism;
- evidence, counter-evidence, and provenance;
- the resources and assumptions required;
- the evaluation protocol and observed outcomes;
- unresolved residuals and next questions.

Where possible, artifacts should be portable, versioned, and comparable across implementations. Disagreement and failed experiments are legitimate contributions to collective learning.

**Suggested overview illustration:** `../figures/Fig-001-ISGFTR-Grand-Architecture.png`.

## 15. Conclusion

Intelligence should not be characterized solely by the objective under which a model was trained or by the tasks on which it has already been tested. Capabilities may be reused, redirected, transferred, combined, or relayed across changing contexts and system structures. Yet these possibilities are conditional, and the mechanisms that produce reliable, retained capability growth remain open research questions.

ISGFTR proposes a modest shift in emphasis: from arguing about an unknown ultimate ceiling to studying the evidence, mechanisms, costs, and constraints of capability-frontier extension. Its most practical implication is the prospect of actively searching for valuable transfers rather than waiting for them to appear by chance.

The framework is offered for critique, experimental validation, revision, and collective relay—not as a settled theory of intelligence or AGI.

---

## Document Relationships

- **ISGFTR-002:** Detailed distinctions among the five characteristics.
- **ISGFTR-003:** Folding, generalization, and structural reuse.
- **ISGFTR-004:** Fluidity and selective structural permeability.
- **ISGFTR-005:** Directional intuition and weak-evidence transfer.
- **ISGFTR-006:** System-centric and multi-level learning.
- **ISGFTR-007:** Recursive relay and open-system growth.
- **ISGFTR-008:** Capability prospecting and evaluation.
- **ISGFTR-009:** AGI implications, limits, and counterarguments.
- **ISGFTR-010:** Open research architecture and collective learning.

**Research status:** All named hypotheses and architectural proposals in this document are provisional unless independently supported by empirical evidence. The repository welcomes critical replication and constructive alternatives.
