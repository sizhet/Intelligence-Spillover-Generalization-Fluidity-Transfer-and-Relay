# ISGFTR-004 — Intelligence Fluidity and Permeable Structural Boundaries

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Directional research hypothesis and conceptual architecture  
**Version:** v1.0.0  
**Status:** Open research proposal; mechanisms and predictions require empirical validation

## Abstract

Intelligence is often evaluated inside fixed task, model, and interface boundaries. Yet adaptive systems can redirect attention, reuse partial representations, solicit external capabilities, and revise their own problem-solving pathways as circumstances change. This paper proposes **intelligence fluidity** as a research construct for such context-sensitive movement of problem-solving processes across representational, functional, organizational, and temporal boundaries. It further introduces **selective structural permeability**: the hypothesis that adaptive boundaries can admit incomplete evidence and exploratory influences while restricting consequential actions until suitable validation occurs. Fluidity is distinguished from generalization, transfer, spillover, relay, and durable learning. The paper outlines a minimal conceptual model, potential control mechanisms, failure modes, and falsifiable experiments. Its objective is not to claim that biological cognition or artificial intelligence is universally fluid, but to establish a precise, open framework for investigating when controlled boundary crossing improves capability, efficiency, and learning.

**Keywords:** intelligence fluidity; structural permeability; adaptive routing; weak evidence; directional intuition; cross-domain transfer; cognitive control; structural intelligence; relay; AGI research

## 1. Motivation: The Limits of Closed-Task Descriptions

Scientific and engineering practice often favors a clearly specified input, bounded process, and measurable output. This is indispensable for reproducibility and safety. However, the boundaries of a task specification need not coincide with the boundaries of all processes that could contribute to solving the task.

A problem-solving system may discover that its initial representation is inadequate; retrieve an analogy from another domain; request a tool or collaborator; redirect computation toward a prerequisite; or change its strategy after new evidence arrives. Such behavior suggests an important distinction between **the boundary of a task as defined** and **the boundary of capabilities that may be mobilized to address it**.

This document investigates that distinction. It does not advocate abandoning formal contracts. Instead, it asks whether *selectively permeable* boundaries can combine open-ended exploration with controlled, verifiable execution.

## 2. Position in the ISGFTR Hypothesis

ISGFTR distinguishes five related constructs:

- **Spillover:** a capability developed in one setting becomes useful beyond its original purpose.
- **Generalization:** learned competence remains effective under changes in inputs or task distributions.
- **Fluidity:** problem-solving processes are adaptively redirected across available representations, capabilities, resources, or boundaries.
- **Transfer:** information, representations, strategies, or competence from a source context contribute to a target context.
- **Relay:** tasks, evidence, capabilities, or results are handed off across units or over time, potentially supporting accumulation and further learning.

Fluidity is a **process-level** construct. It need not imply successful transfer, and successful transfer need not imply durable growth. The distinctions established in ISGFTR-001 and ISGFTR-002 remain essential: *mobility is not utility; utility is not growth*.

## 3. Proposed Definition of Intelligence Fluidity

> **Intelligence fluidity** is the context-sensitive capacity of an adaptive system to redirect, redistribute, or transform its problem-solving activity across accessible representations, capabilities, resources, and operational boundaries in response to goals, opportunities, evidence, and feedback.

This definition emphasizes four properties:

1. **Directionality:** transitions are guided by objectives, value estimates, or control policies rather than being arbitrary movement.
2. **Cross-boundary reach:** the system may traverse task, modality, tool, memory, agent, or organizational interfaces.
3. **Adaptivity:** routing and transformation respond to new evidence or changing conditions.
4. **Operational observability:** the transitions can, at least in principle, be logged and evaluated.

A system that repeatedly calls tools without changing its policy may exhibit extensive activity but little fluidity. Conversely, a small system that detects a representational mismatch and selects an effective alternative may exhibit meaningful fluidity without being broadly intelligent.

### 3.1 Boundaries Are Multidimensional

Potential boundaries include:

| Boundary | Example crossing | Primary concern |
|---|---|---|
| Representation | prose to graph or program | semantic preservation |
| Task | main task to prerequisite | relevance and cost |
| Capability | reasoner to planner or solver | interface compatibility |
| Modality | text to spatial or sensor evidence | grounding |
| Agent | individual to collaborator | provenance and trust |
| Time | current execution to stored precedent | memory quality and drift |
| Governance | exploration to authorized action | permissions and safety |

Not all boundaries should be equally permeable. A speculative analogy may be harmless as a candidate hypothesis but unacceptable as an authorization to perform an irreversible action.

## 4. Selective Structural Permeability

> **Selective structural permeability** is the ability of a system to admit, transform, delay, reject, or validate cross-boundary influences according to context, evidence quality, expected value, and risk.

This is a proposed engineering abstraction, not a claim that all brains or AI systems implement a single permeability algorithm.

A useful boundary can support multiple modes:

- **Closed:** no crossing is permitted for the current purpose.
- **Exploratory:** weak evidence, partial matches, and candidate hypotheses may pass, but do not establish truth or execution authority.
- **Conditionally validated:** additional tests, translation, or review are required before use.
- **Operational:** a validated, authorized capability may be invoked under an explicit contract.
- **Learning relay:** outcomes and counter-evidence may be recorded for later reassessment.

Permeability is thus neither a binary open/closed property nor a synonym for unlimited connectivity. It is a policy-controlled interface characteristic.

### 4.1 The Two-Gate Principle

The central proposal is to separate:

**Gate A — Exploratory permeability.** Admit plausible but incomplete cross-domain signals to generate hypotheses and candidate routes.

**Gate B — Validated relay.** Permit consequential execution, trusted reuse, or durable capability claims only after evidence and conformance checks appropriate to the stakes.

This separation preserves the creative advantages of loose coupling without granting weak signals unjustified authority. The gates may be implemented at different levels of rigor depending on task risk.

## 5. Directional Intuition as a Candidate Front-End

Human problem solving often begins with an imperfect sense that one situation resembles another. Such intuitions can be useful search cues, but are also vulnerable to superficial analogy and confirmation bias. ISGFTR treats this phenomenon as motivation for a **directional candidate generator**, not as evidence of a universal neural algorithm.

A candidate pathway may be proposed from:

- shared structural features or relational patterns;
- weak or incomplete observations;
- historical successes and failures;
- partial metric or non-metric compatibility;
- residual gaps and possible bridging units;
- available tools, collaborators, or prior relay artifacts.

The BM-ODWEI / Metric-Directional-Intuition line of SI research motivates retaining **OTHERS** signals: observations not yet captured by the current matching vocabulary. Such signals should be tagged as exploratory and retain source, uncertainty, and validation requirements. An OTHERS channel must not become an unconstrained source of positive scores.

## 6. A Minimal Conceptual Model

Let a system at time \(t\) have state

\[
X_t=(q_t,\mathcal{U}_t,\mathcal{G}_t,\mathcal{M}_t,\mathcal{E}_t,\mathcal{P}_t),
\]

where \(q_t\) is the current task context, \(\mathcal U_t\) accessible capability units, \(\mathcal G_t\) their connectivity, \(\mathcal M_t\) memory, \(\mathcal E_t\) available evidence, and \(\mathcal P_t\) governing policies.

A candidate cross-boundary transition \(a\) can be evaluated by a routing policy:

\[
\pi_{\mathrm{flow}}(a\mid X_t),
\]

subject to a gate \(g(a,X_t)\in\{\text{reject},\text{explore},\text{validate},\text{execute}\}\).

A research prototype could prioritize candidate exploration using

\[
V(a\mid X_t)=\widehat{B}(a)-\widehat{C}(a)-\widehat{R}(a)+\lambda\widehat{IG}(a),
\]

where estimated benefit, cost, risk, and information gain are expressed on a compatible decision scale. These terms are placeholders requiring empirical definition; \(V\) is **not** automatically a calibrated probability of success. Hard safety or permission constraints should be enforced separately, not traded away against estimated benefit.

After probing, the system records an outcome \(o_t\) and updates its evidence or routing policy:

\[
(X_{t+1},\mathcal H_{t+1})=\mathcal L(X_t,\mathcal H_t,a_t,o_t).
\]

Here \(\mathcal H_t\) denotes a provenance-aware history. Learning may update a model, memory, interface, routing policy, or structural graph. It is not restricted to parameter gradient updates.

## 7. Fluidity, Learning, and Growth Are Different

Three outcomes should be evaluated separately:

1. **Movement:** did a cross-boundary candidate route actually occur?
2. **Utility:** did the route improve task performance, reliability, or cost relative to controls?
3. **Growth:** did the system retain a new capability or improve subsequent adaptation on held-out tasks?

A one-time tool call may improve performance without changing future capability. Repeated relays may produce extensive logs without useful learning. Conversely, a failed probe may still yield valuable counter-evidence that improves later decisions.

The research objective is to determine **when and how** fluidity produces utility or durable growth, not to equate them by definition.

## 8. Biological Inspiration: Opportunity and Caution

Biological nervous systems exhibit distributed representations, associative processing, attention, inhibition, and feedback. Collective organisms may also adapt through local interactions and environmental traces. These phenomena motivate studying adaptive cross-boundary influence and multi-level control.

However, several distinctions are necessary:

- The brain performs physical and quantitative computation; it is not the opposite of numerical processing.
- Flexible association is not the absence of constraints. Inhibition and selective attention can be as important as activation.
- Ant colonies, bird flocks, and human cognition differ substantially in mechanisms and learning objectives.
- Analogies from biology do not establish that a proposed AI architecture reproduces neural mechanisms.

The useful engineering question is not whether artificial systems can dispense with formalism, but whether **early exploratory stages can tolerate partial structure while later stages enforce appropriate rigor**.

## 9. Structural Intelligence Interfaces

The proposed framework can be investigated using existing SI concepts as candidate building blocks:

| SI research direction | Possible role in fluidity research |
|---|---|
| Folding / Unfolding | expose reusable cores and candidate transformations |
| BM-ODWEI / MDI | generate weak-evidence directional hypotheses |
| UCPSF | combine perspectives and govern scoring |
| SIF | locate capability units, residuals, and structural alternatives |
| UIERU | support multi-trail exploration and relay |
| BUI-DSI | represent dynamic, perspective-dependent structural changes |
| AQSI | propose questions that expose potential boundary crossings |
| Structural RSI | evaluate and retain validated structural improvements |

These are **proposed interfaces**, not evidence that a unified implementation already exists or outperforms established baselines. An independent implementation should be possible without adopting SI-specific terminology.

## 10. Failure Modes and Governance

Selective permeability introduces distinctive risks:

- **False analogy:** a plausible structural resemblance masks incompatible causal or operational conditions.
- **Negative transfer:** a previously successful strategy harms performance in the target setting.
- **Semantic drift:** information changes meaning across representations or relay stages.
- **Contaminated evidence:** low-quality or adversarial inputs propagate through the network.
- **Runaway exploration:** unconstrained branching consumes resources without improving outcomes.
- **Evaluation gaming:** the router learns to optimize a proxy rather than real capability.
- **Unauthorized boundary crossing:** exploratory information is incorrectly treated as permission to act.
- **Group error amplification:** repeated relay makes unsupported claims appear well established.

Mitigations include provenance tracking, separate exploratory and operational channels, risk-adjusted budgets, independent validators, counter-evidence registries, rollback, and explicit residual reporting. For consequential operations, permission checks and safety constraints must remain hard boundaries.

## 11. Testable Hypotheses

The following hypotheses are proposed, not established findings.

**H-FL-01 — Selective versus fixed permeability.** Under matched compute and tool budgets, adaptive boundary gating will improve performance or cost-adjusted discovery over always-open and always-closed routing on some heterogeneous task distributions.

**H-FL-02 — Weak-evidence discovery.** An exploratory gate admitting appropriately tagged partial matches will identify useful cross-domain candidates missed by strict exact-match routing, at a measurable false-positive cost.

**H-FL-03 — Two-gate reliability.** Separating hypothesis admission from validated execution will reduce consequential errors relative to a single-stage permissive routing policy while preserving some discovery benefit.

**H-FL-04 — Learned flow policy.** A routing policy trained on verified outcomes will outperform fixed hand-coded routes on held-out task families, subject to matched exploration budgets.

**H-FL-05 — Relay retention.** Provenance-aware feedback and memory will yield more durable cross-task gains than stateless relay alone, if the learning channel is effective.

Each hypothesis can fail. Negative or mixed findings should be preserved and published rather than reinterpreted as automatic support for fluidity.

## 12. Proposed Validation Program

### Experiment A — Cross-representation routing

Construct tasks with text, graphs, tabular descriptions, and executable specifications. Compare fixed representation, unrestricted conversion, and selective gating. Hold task difficulty, tool availability, and compute budget constant where feasible. Measure success, conversion error, latency, and total cost.

### Experiment B — Weak-signal opportunity search

Hide known source-to-target transfer outcomes during scoring. Compare random exploration, exact structural matching, semantic similarity, and weak-evidence directional scoring. Evaluate precision at budget, useful discoveries per unit cost, and calibration where probabilistic outputs are produced.

### Experiment C — Two-gate versus one-gate systems

Create low-stakes exploratory tasks and separately controlled consequential tasks. Test whether exploratory permeability improves hypothesis generation while validation gates prevent unsupported action. Report missed opportunities as well as false approvals.

### Experiment D — Learning where to cross

Use a family of tasks with changing capability availability and interface costs. Compare static routing with learned routing. Evaluate out-of-distribution adaptation, robustness to tool removal, and policy drift.

### Experiment E — Longitudinal relay

Run repeated tasks with and without provenance-aware memory and structural updates. Distinguish immediate performance gains from retained improvements on later unseen tasks. Include ablations for memory, scoring, and structure adaptation.

### Evaluation discipline

Pre-register primary metrics where practical; maintain held-out tasks; record failures and total exploration costs; test sensitivity to task distributions; and use independent evaluators when feasible. A result on one benchmark should not be presented as proof of general intelligence.

## 13. Implications for System-Centric Intelligence and AGI

A system-centric perspective asks not only what a single model can do in isolation, but also what capabilities a governed system can **access, coordinate, and learn to develop**. Fluidity may help such systems find relevant tools, representations, or collaborators. Selective permeability may allow exploration without surrendering execution controls.

Yet fluidity alone is neither sufficient nor necessary for AGI under all definitions. Broad competence, reliability, autonomy, grounding, learning, resource efficiency, and governance remain separate requirements. The proposed framework is a research lens for studying capability frontiers, not a forecast that open-ended growth is inevitable.

## 14. Open Questions

1. Can fluidity be measured independently of tool-use frequency and raw search breadth?
2. What constitutes a useful structural boundary, and how should its permeability be represented?
3. Which weak signals genuinely improve discovery after controlling for model scale and search budget?
4. Can a flow policy generalize to domains with unfamiliar interfaces or missing modalities?
5. How should a system balance exploratory openness against privacy, safety, and epistemic reliability?
6. What evidence distinguishes durable learning from temporary external assistance?
7. Can boundary policies themselves become reusable, portable intelligence units?
8. How do different forms of memory and relay affect long-term error propagation?
9. Which findings from biological cognition transfer to engineered systems, and which do not?
10. Under what conditions does additional permeability reduce rather than improve performance?

## 15. Collective Learning and Research Relay

This document is intended as an open invitation to investigate a set of falsifiable ideas. Researchers may contribute by refining definitions, designing counterexamples, implementing small routing systems, reporting failed transfer attempts, evaluating weak-evidence methods, or comparing biological and engineered boundary control.

A useful research relay artifact should specify: source capability, target context, proposed boundary crossing, supporting and opposing evidence, intervention or probe, observed result, resource cost, limitations, and a reproducible reference. Claims should retain their evidence status as they pass between teams.

The goal is not to establish a proprietary vocabulary, but to help different communities compare findings and build on one another's results.

## 16. Conclusion

The boundaries used to define and test an intelligent system may be narrower than the boundaries of capabilities it can mobilize. This paper proposes **intelligence fluidity** as a name for adaptive redirection of problem-solving processes across such boundaries, and **selective structural permeability** as a candidate means of regulating those crossings. The central research challenge is to discover when exploratory openness creates useful options, when validation is essential, and when repeated cross-boundary activity becomes genuine learning rather than mere motion.

A productive next step is a small, controlled experiment comparing fixed, unrestricted, and selectively gated routes under equal budgets. Evidence—not the appeal of the metaphor—should determine how far the hypothesis can be extended.

---

## Figure Placement

**Recommended primary figure:** `figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png` after Section 4 or 5.  
**Optional cross-reference:** `figures/Fig-003-Five-Characteristics-of-Intelligence-Flow.png` after Section 2.  
**Optional cross-reference:** `figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png` after Section 7.

Figures are planned conceptual illustrations, not experimental results. Paths are relative to the repository root; from this document in `docs/`, Markdown links should use `../figures/`.

## Relationship to Other ISGFTR Documents

- **ISGFTR-001:** intelligence boundaries and open capability frontiers.
- **ISGFTR-002:** definitions and distinctions among five characteristics.
- **ISGFTR-003:** folding, generalization, and reusable structural cores.
- **ISGFTR-005:** directional intuition and weak-evidence transfer.
- **ISGFTR-006:** system-centric and multi-level learning.
- **ISGFTR-007:** recursive relay and intelligence growth.
- **ISGFTR-008:** capability prospecting and opportunity evaluation.
- **SPEC-002 / SPEC-003:** evidence and validation contracts proposed for future work.

## Research Context and Attribution Note

The ideas in this document intersect with established work in cognitive control, attention and gating, transfer learning, analogical reasoning, modular systems, hierarchical reinforcement learning, multi-agent coordination, and continual learning. These neighboring fields should be consulted and cited in any later scholarly manuscript claiming empirical or historical novelty. The constructs introduced here are offered as a synthesis and research proposal; no claim of exclusive priority over related mechanisms is intended.

**License:** See the repository's `LICENSE` file (planned Apache-2.0).  
**Citation:** See repository `CITATION.cff` once finalized.  
**DOI:** To be assigned after a versioned release and archival deposit.
