# ISGFTR-008 — Intelligence Spillover and Transfer Prospecting

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Directional research hypothesis, conceptual architecture, and falsifiable validation agenda  
**Version:** v1.0.0 (theory-first)  
**Status:** Open research proposal; no empirical success or novel algorithmic superiority is asserted  
**Date:** 2026-10-30

## Abstract

A system's demonstrated capabilities are not necessarily identical to the capabilities it could reach through a different prompt, representation, decomposition, tool, collaborator, or learning arrangement. Yet searching for such possibilities is difficult: the space of candidate transfers is large, evidence is incomplete, and apparent similarities frequently fail under validation. This paper proposes **intelligence spillover and transfer prospecting** as a disciplined process for identifying, prioritizing, testing, and retaining *hypotheses* about presently unobserved but potentially reachable capabilities. The proposed process integrates structural analogies, historical transfer precedents, weak and negative evidence, directional intuition, resource-aware experimental selection, controlled probes, and evidence-bearing structural relay. It distinguishes a **prospect** from an observed capability, a successful probe from a generalizable transfer, and a one-time performance gain from durable intelligence growth. We introduce a prospect record, an exploration-priority formulation, a two-gate validation policy, and a portfolio of controlled experiments, including frozen-model and system-level learning settings. Failure, negative transfer, and uncertainty are first-class outputs. Prospecting is not a proof of latent AGI, and its ranking scores are not calibrated success probabilities without additional evidence. The intended contribution is a research interface through which independent investigators can reproduce, challenge, and extend capability-discovery hypotheses.

**Keywords:** capability prospecting; intelligence spillover; transfer discovery; weak evidence; directional intuition; structural analogy; active exploration; two-phase search; selective permeability; negative transfer; structural relay; collective learning

---

## 1. The Prospecting Problem

Conventional capability evaluation asks whether a model or system succeeds on a known task under a specified procedure. Prospecting asks a different question:

> Which capabilities that are not yet demonstrated might become reachable through a feasible structural change, and which inexpensive experiments would most efficiently distinguish promising transfers from misleading analogies?

A language model may fail a task in direct form but succeed after decomposition or tool access. A group of limited agents may exhibit an ability absent from any isolated member. A structural representation learned in one domain may support a second domain only after its assumptions are translated. These observations motivate exploration; none alone establishes a general law of spillover.

Exhaustively testing all possible tasks, interfaces, representations, and compositions is infeasible. Prospecting therefore needs to be *selective*. It should spend limited resources on candidates that have a credible mechanism, potentially valuable outcomes, and tests capable of falsifying the proposed transfer.

The distinction is essential: **prospecting generates and evaluates hypotheses about capability; it does not manufacture evidence by naming an attractive possibility.**

## 2. Four Capability Boundaries Revisited

ISGFTR-001 introduced four analytical boundaries. Here they serve as a map for candidate discovery rather than a claim that all capability sets form a simple nested geometry.

1. **Generative boundary:** behaviors or artifacts that a given mechanism can produce under specified conditions.
2. **Observed boundary:** capabilities actually supported by valid measurements under a declared protocol.
3. **Reachable boundary:** capabilities plausibly accessible through permitted changes in prompting, structure, tools, coordination, or resources.
4. **Evolvable boundary:** capabilities that could be acquired and retained through permitted learning or structural adaptation over time.

A reachable capability can remain unobserved because the relevant experiment has not been performed. Conversely, an apparently observed success can disappear under stronger controls. Reachability is relative to an intervention set and a budget; evolvability is relative to a learning mechanism and time horizon. Thus these boundaries must be indexed by conditions rather than depicted as universal concentric circles.

Let \(C(S,T,I,B,E)\) denote a system's measured capability for task distribution \(T\), allowed interventions \(I\), resource budget \(B\), and evaluation protocol \(E\). Prospecting considers changes to \(I\) or system structure while preserving a clear record of what was changed. Without these indices, claims of “new capability” are ambiguous.

## 3. Definitions: Prospect, Opportunity, Probe, and Confirmed Transfer

### 3.1 Capability prospect

A **capability prospect** is a falsifiable proposal that a source capability or structural pattern can support a target task under a specified transformation. It includes a predicted mechanism, assumptions, uncertainty, and a feasible test.

### 3.2 Spillover opportunity

A **spillover opportunity** is a prospect whose target lies outside the source's original or routinely evaluated task context. Spillover is a descriptive relation between contexts, not necessarily an increase in general intelligence.

### 3.3 Transfer path

A **transfer path** is a proposed sequence of transformations, for example: source abstraction → context translation → tool or agent composition → target execution → evaluation. Each transformation can introduce error or cost.

### 3.4 Probe

A **probe** is a bounded experiment designed to update belief about a prospect. A probe should specify what result would count against the hypothesis, not only what result would support it.

### 3.5 Validated transfer

A **validated transfer** is a prospect that passes predeclared evaluation criteria, including suitable baselines and controls. Validation applies only to the tested scope. Durability, cross-task robustness, and retained growth require additional experiments.

### 3.6 Structural relay

A **structural relay** is the transmission of a prospect, test result, transformation, failure case, or reusable procedure to another unit or future experiment, with provenance and interpretation preserved.

## 4. Sources of Candidate Prospects

A prospecting engine should avoid dependence on a single similarity metric. Candidate sources may include:

- **Structural correspondence:** shared constraints, invariants, subproblems, or causal organization across domains.
- **Folding and reusable cores:** an abstraction extracted from multiple tasks that might be unfolded in a new context, subject to lost information and residual differences.
- **Historical precedents:** documented successful and failed transfers, with conditions under which they occurred.
- **Directional weak evidence:** partial analogies, suggestive behavior, unexpected outputs, or near-miss results that justify testing but not confidence.
- **Residual and OTHERS signals:** patterns poorly explained by existing categories or exact-match models, potentially indicating overlooked mechanisms or simply noise.
- **Composition opportunities:** combinations of models, tools, memories, evaluators, or agents whose interfaces might jointly support a new task.
- **Unresolved task demands:** unmet requirements that suggest a missing transformation, representation, or coordination pathway.
- **Counterexamples:** failed attempts that reveal boundary conditions and inspire narrower, more accurate prospects.

Each source should be tagged with its reliability, provenance, and relevance. Multiple weak signals from a common origin must not be treated as independent corroboration.

## 5. A Canonical Prospect Record

A minimal record can be represented as

\[
P = (s,t,\tau,a,e^+,e^-,u,c,v,g,p),
\]

where:

- \(s\): source capability or structural precedent;
- \(t\): target task and evaluation distribution;
- \(\tau\): proposed transformation or relay path;
- \(a\): assumptions and boundary conditions;
- \(e^+\): supporting observations;
- \(e^-\): counterevidence, failure reports, and competing explanations;
- \(u\): uncertainty representation and provenance gaps;
- \(c\): anticipated costs, dependencies, and safety constraints;
- \(v\): predeclared probe and validation protocol;
- \(g\): governance permissions and stop conditions;
- \(p\): lifecycle status and provenance identifiers.

This is a conceptual contract, not an implemented universal schema. `SPEC-002` and `SPEC-003` are intended to refine its machine-readable fields and state transitions.

A prospect lacking a target metric, intervention description, or plausible disconfirming result should be labeled **underspecified**, not silently promoted into the exploration queue.

## 6. Directional Intuition Without Premature Certainty

ISGFTR-005 discusses directional intuition as low-cost guidance under incomplete evidence. In prospecting, intuition selects *where to look*, not *what to believe*. A direction may arise from a metric-native relationship, an analogy across representations, or a partial causal explanation.

For example, a planner that successfully decomposes software tasks might be tested on a laboratory scheduling problem because both involve dependencies and resource constraints. The prospect is not “planning generalizes everywhere”; it is “a dependency-aware decomposition policy may improve performance on a specified scheduling benchmark under a documented interface translation.”

Directional evidence is useful when exhaustive search is costly. It becomes hazardous when the ranking function rewards narrative plausibility over independent tests. Accordingly, all prospect scores should be accompanied by the features and evidence that produced them.

### 6.1 Metric-native versus common embedding approaches

Some source and target structures may support native measures—graph edit operations, constraint satisfaction, program traces, or task-specific causal dependencies—without embedding both into a common vector space. Other settings benefit from learned embeddings. Neither representation should be assumed universally superior. A comparative experiment must control the candidate pool, probe budget, and evaluator.

### 6.2 OTHERS and residual hypotheses

An unexplained residual can generate a candidate for further examination. It is not, by itself, evidence that a new transferable competence exists. A null or noise explanation must remain available.

## 7. Prospect Ranking as Resource-Aware Decision Support

Given a portfolio \(\mathcal P\) and limited budget, a ranking function can guide selection:

\[
Q(P)=w_1 D(P)+w_2 V(P)+w_3 I(P)+w_4 R(P)
-w_5 K(P)-w_6 H(P),
\]

where \(D\) represents directional support, \(V\) potential value, \(I\) expected information gain, \(R\) anticipated reuse, \(K\) experimental cost, and \(H\) expected harm or negative-transfer risk. Weights depend on the research control plane. These terms need not share a natural scale; normalization and sensitivity analysis are mandatory before comparing scores.

**Important:** \(Q(P)\) is an *exploration-priority score*, not a probability of successful transfer. A probabilistic interpretation would require labeled outcomes, calibration assessment, and checks for distribution shift.

A single scalar also hides important tradeoffs. For consequential settings, a Pareto frontier or constrained portfolio can preserve competing objectives such as expected learning, cost, safety, and domain diversity. The scoring rule should be logged before outcomes are observed to reduce post-hoc rationalization.

### 7.1 Value of information

A low-probability prospect may still deserve a small probe if the result would eliminate many related hypotheses. Conversely, an attractive high-value target may be a poor experiment if the outcome is uninterpretable. Prospecting should reward **discriminative tests**, not merely exciting applications.

### 7.2 Portfolio diversity

A queue dominated by near-duplicate analogies may appear high-scoring but provide little independent learning. Budget allocation can impose diversity across domains, transfer mechanisms, failure modes, and evidence sources. This is a hypothesis about efficient discovery, to be tested rather than presumed.

## 8. Two-Gate Prospecting and Validation

The proposed lifecycle separates exploratory openness from reliable adoption.

**Gate A — Exploration admission:** A candidate may enter a bounded sandbox if its assumptions are explicit, its risk is acceptable, and a useful falsification-oriented probe can be afforded. Weak evidence is permitted here.

**Gate B — Capability acceptance:** A candidate may be treated as validated only after passing held-out evaluation, appropriate controls, provenance review, and predeclared thresholds. Stronger claims—durability, broad generalization, or system growth—require stronger longitudinal evidence.

The gates are intentionally asymmetric. A weak signal can justify a cheap test; it cannot justify deployment, publication as an established capability, or promotion into a trusted structural library.

### 8.1 State transitions

`Proposed → Screened → Prioritized → Probed → {Rejected, Inconclusive, Provisionally Supported} → Validated → Relayed → Monitored`

A rejected prospect remains useful if the record explains *why* it failed. A validated prospect can later be downgraded after counterevidence or distribution shift. Lifecycle transitions should be reversible when justified by evidence.

## 9. A Recursive Prospecting–Relay Loop

The proposed loop is:

**Prospect → Probe → Validate → Relay → Learn → Prospect**.

1. **Prospect:** Generate hypotheses from known capabilities, structural relationships, residuals, and open questions.
2. **Probe:** Perform bounded tests with controlled interventions and recorded costs.
3. **Validate:** Compare against preregistered baselines, including negative and placebo transfers.
4. **Relay:** Preserve procedures, results, uncertainty, failures, and evidence provenance.
5. **Learn:** Update a prospect registry, routing policy, structural memory, or research portfolio; do not presume model-weight updates.
6. **Prospect again:** Use revised knowledge to select better questions or identify previously overlooked boundaries.

This loop interfaces with ISGFTR-007's recursive relay. The two mechanisms differ in emphasis: recursive relay concerns persistent transmission and adaptation, while prospecting concerns **discovery and evaluation of possible new transfer paths**.

## 10. Prospecting Across Learning Levels

Prospecting is not restricted to a single foundation model. The unit of analysis can vary:

| Level | Candidate intervention | Evidence of success | Common confound |
|---|---|---|---|
| Model or unit | Prompt, representation, tool call | Held-out target performance | Prompt tuning to test set |
| Interaction | Routing or agent coordination | Controlled team improvement | Extra compute or more attempts |
| Structure | New calling graph or reusable core | Transfer to new task families | Task-specific hardcoding |
| Relay | Reuse of recorded procedures | Reduced future sample or compute cost | Retrieval of near-duplicate answers |
| Collective | Shared prospect and evidence registry | Cross-team reproducibility | Shared evaluator contamination |
| Evolutionary | Retained policy or structure revisions | Longitudinal improvement | Uncontrolled environmental change |

The **Learning–Execution Unit Decoupling** hypothesis from ISGFTR-006 is especially relevant. A frozen model can participate in a system whose prospecting policy improves over time. To demonstrate learning, experiments must show that past evidence causally improves future selection or performance—not merely that a larger workflow outperforms an isolated baseline.

## 11. Illustrative Prospect: Constraint Planning Across Domains

Consider a source system that decomposes software delivery work into dependency-aware subtasks. A target domain is a synthetic logistics scheduling benchmark with precedence and resource constraints.

**Prospect:** The source's dependency decomposition may transfer after translating task descriptions into a common constraint graph.

**Transformation:** Extract prerequisite relations, resource requirements, and permissible ordering; apply the decomposition policy; translate its output back into the target scheduler.

**Supporting signal:** Both domains exhibit precedence structures. This is a weak structural analogy, not proof of causal equivalence.

**Counterevidence to seek:** Target constraints may involve continuous time, uncertainty, capacity coupling, or physical constraints absent in the source. A graph translation may discard essential information.

**Controls:** Direct target solver, generic prompting, random decomposition, matched-budget planning, and a source policy with shuffled dependency information.

**Validation:** Evaluate feasibility, objective quality, constraint violations, computational cost, and robustness on held-out problem families. Test whether gains survive different graph sizes and constraint regimes.

**Relay artifact:** Store the translation contract, failure modes, tested distribution, confidence limits, and executable evaluation recipe. A successful single benchmark does not justify a claim of general planning intelligence.

## 12. A Minimal Research MVP

A first implementation can remain small and transparent:

- **Capability registry:** 10–30 documented source procedures or capabilities, with evaluation traces.
- **Target set:** several held-out task families with measurable success criteria.
- **Prospect generator:** rule-based structural analogy plus an optional LLM candidate generator.
- **Evidence registry:** positive, negative, and inconclusive results with unique provenance identifiers.
- **Priority engine:** simple interpretable score or constrained portfolio selection.
- **Probe executor:** sandbox with fixed budgets, blinded or held-out evaluation, and audit logs.
- **Relay store:** validated procedures and rejected hypotheses with conditions of applicability.

An initial study should avoid automatic deployment and external side effects. The research question is whether prospecting improves *discovery efficiency* compared with fair baselines, not whether a large system can produce a compelling demonstration.

## 13. Experimental Program and Baselines

### Experiment A — Candidate discovery efficiency

Compare structural prospecting with random selection, lexical similarity, embedding similarity, and expert-defined heuristics under the same probe budget. Measure validated transfers discovered per unit cost, precision among selected candidates, and diversity of mechanisms discovered.

### Experiment B — Weak evidence and counterevidence

Compare a positive-evidence-only ranker with a ranker that explicitly incorporates failed precedents, provenance, and negative-transfer risk. Measure false-positive selection, wasted probe cost, and missed opportunities. Include correlated-evidence stress tests.

### Experiment C — Two-gate versus single-gate admission

Evaluate whether separating cheap exploration from stringent acceptance reduces invalid promotion while maintaining discovery yield. Report both false acceptance and opportunity loss, not just successes.

### Experiment D — Recursive learning with frozen units

Keep execution models fixed. Allow only the prospect registry and selection policy to update across episodes. Compare against a stateless prospecting system with equal total compute and the same historical task distribution. Evaluate future held-out transfer discovery and forgetting or drift.

### Experiment E — Cross-domain robustness

Test candidate transformations on new target families and altered constraints. Measure whether the apparent transfer survives distribution shifts or collapses into narrow benchmark adaptation.

### Experiment F — Ablations and causal attribution

Remove directional scoring, structural abstraction, negative evidence, portfolio diversity, and relay memory one at a time. Assess whether each component contributes beyond added compute, additional attempts, or evaluator leakage.

All experiments should report uncertainty intervals, failure counts, intervention costs, and the exact number of tested prospects. When selection is adaptive, account for multiple comparisons and winner's-curse effects.

## 14. Testable Hypotheses

**H-P1 — Structural prospecting efficiency.** Under matched exploration budgets, a prospect selector using explicit structural correspondences will identify more independently validated transfers than random or purely surface-similarity selection on at least one preregistered task collection. **Falsifier:** no robust improvement after budget matching and held-out evaluation.

**H-P2 — Negative evidence improves screening.** Incorporating counterevidence and provenance into candidate selection reduces false promotion or wasted probes relative to a positive-only ranker without an unacceptable reduction in true discovery. **Falsifier:** no favorable tradeoff across predefined operating points.

**H-P3 — Directional scoring is useful but not sufficient.** Directional weak evidence improves the ordering of low-cost probes in some domains, while strict validation remains necessary to control false claims. **Falsifier:** scoring offers no selection benefit or acceptance without validation is equally reliable under controlled tests.

**H-P4 — Two-gate policy improves reliability.** Separating exploration admission from capability acceptance lowers unsupported transfer claims at a comparable discovery budget. **Falsifier:** no improvement in false-acceptance/discovery tradeoffs.

**H-P5 — Relay memory supports future prospecting.** A system with frozen execution units but updated evidence-bearing prospect memory improves future discovery efficiency on held-out task families compared with a stateless, matched-budget control. **Falsifier:** apparent gains disappear when retrieval leakage and extra compute are controlled.

**H-P6 — Portfolio diversity can improve information yield.** Diversified candidate selection produces more independent information or broader validated coverage than greedy top-score selection in selected heterogeneous prospect spaces. **Falsifier:** diversity constraints consistently reduce yield without compensating information gains.

**H-P7 — Structural transfer has bounded applicability.** Explicitly modeling residual differences and translation loss improves calibration of transfer decisions compared with assuming shared core structure is sufficient. **Falsifier:** residual modeling adds no reliable predictive or screening value across tested domains.

These are hypotheses for investigation, not findings. Results should include failed replications and contradictory evidence.

## 15. Failure Modes, Confounds, and Governance

### 15.1 Negative transfer and false analogies

A candidate can share superficial structure while differing in decisive constraints. The prospect registry must preserve reasons for failure, not simply mark a score as low.

### 15.2 Evaluation contamination

Repeated prospecting against a visible benchmark can overfit the discovery policy to that benchmark. Maintain separate development, selection, and final test distributions. Audit whether relay artifacts contain answers to evaluation items.

### 15.3 Compute and tool confounding

A larger system may outperform a baseline because it makes more calls, sees more examples, or uses a stronger tool. Compare matched resource envelopes and report performance–cost frontiers.

### 15.4 Self-confirming evidence loops

If an LLM proposes a transfer and another LLM judges its plausibility using the same unverified narrative, agreement is not independent evidence. Require observable task outcomes or independent evaluators for acceptance.

### 15.5 Goodhart pressure and score gaming

A prospecting policy optimized only for “successful discoveries” may choose trivial or easily gamed tasks. Balance validity, novelty, reuse, cost, and coverage, and audit changes to the scoring function.

### 15.6 Unsafe boundary crossing

A promising transfer may require access to private data, high-risk tools, or unapproved actions. Exploration admission is conditional on permissions and safety policy; utility never overrides those constraints.

### 15.7 Unbounded growth rhetoric

A sequence of successful transfers does not establish open-ended growth or AGI. The mechanism may saturate, incur maintenance costs, or fail outside its training and validation regimes.

## 16. Interfaces to the Broader SI Research Program

This paper is designed to interoperate with, not replace, related conceptual proposals:

- **ISGFTR-001/002:** boundary distinctions and five characteristics of spillover, generalization, fluidity, transfer, and relay.
- **ISGFTR-003:** structural folding, reusable cores, residual differences, and uncertainty recovery.
- **ISGFTR-004:** selectively permeable structural boundaries and exploration versus execution gating.
- **ISGFTR-005:** directional intuition, metric-native scoring, weak evidence, and OTHERS residuals.
- **ISGFTR-006:** system-centric learning and learning–execution unit decoupling.
- **ISGFTR-007:** recursive relay, repeated evidence accumulation, and durable growth.
- **ISGFTR-009:** implications, limits, and counterarguments regarding AGI.
- **ISGFTR-010:** an open architecture for shared research artifacts and collective learning.
- **BM-ODWEI / MDI:** candidate directional scoring and weak-evidence interfaces, to be independently evaluated.
- **UCPSF:** control-plane and multi-perspective scoring governance.
- **SIF / UIERU / BUI-DSI:** structural units, dynamic composition, and evidence-bearing relay.
- **AQSI:** autonomous question generation, including prospect-driven research questions.

These are proposed research interfaces, not claims that the named frameworks have already demonstrated the empirical results hypothesized here.

## 17. Open Questions

1. What is the smallest useful representation of a capability that supports meaningful prospecting without overcompressing its assumptions?
2. Can directionally informative structural distances be learned with fewer validated examples than generic similarity models require?
3. How should an exploration policy distinguish independent evidence from many restatements of one source?
4. When is a failed transfer informative enough to justify retaining a negative precedent?
5. Which components of a prospect record can be standardized across scientific, software, robotic, and organizational domains?
6. How can prospective reachability be estimated without conflating it with current observed performance?
7. Can a frozen-unit system learn a reusable prospecting policy that transfers to genuinely new task families?
8. What governance mechanism prevents valuable weak evidence from being suppressed while blocking unsafe or unsupported deployment?
9. How can uncertainty recovered through downstream testing be attached to earlier folding or abstraction decisions?
10. When does the cost of maintaining a prospect registry exceed the future value of its discoveries?

## 18. Collective Learning and Research Relay

An open prospecting ecosystem should make both positive and negative outcomes reusable. A contribution need not demonstrate a dramatic new capability. A careful failed transfer with a reproducible test and clear boundary conditions can be more valuable than an unrepeatable success claim.

Suggested contributions include prospect schemas, controlled baselines, blinded evaluation sets, cross-domain translation contracts, negative-transfer taxonomies, calibration studies, and small frozen-unit experiments. Each contribution should state the intervention, budget, comparator, data provenance, evaluation criteria, and limits of inference.

The proposed research ethos is **collective-learning-friendly**: publish enough structure for others to test, reject, narrow, or extend the hypothesis. Avoid treating exploratory priority as certainty, or temporary benchmark gains as durable intelligence growth.

## 19. Conclusion

Intelligence spillover and transfer prospecting reframes capability discovery as a disciplined search problem. It seeks candidate paths from known structures to unobserved tasks, admits weak evidence for bounded exploration, and demands stronger evidence before recognizing transferable competence. The proposed process combines structural analogy, directional intuition, counterevidence, resource-aware selection, two-gate validation, and recursive evidence relay. Its central empirical question is whether this architecture discovers **more valid, reusable capability transfers per unit cost** than simpler alternatives while reducing false claims and negative transfer.

A prospect is a question, not an answer. A probe is evidence, not proof of generality. A relay is an opportunity for learning, not a guarantee of growth. These distinctions are the basis for an open and falsifiable research program.

---

## Planned Figure Placement

**Primary:** `../figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png` — place after Section 9, illustrating candidate generation, directional scoring, two gates, and the recursive relay loop.

**Secondary:** `../figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png` — reference in Sections 6–8.

**Secondary:** `../figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png` — reference in Sections 9–10.

The named figures are planned conceptual illustrations, not empirical result plots. Add Markdown image links when the figure assets are available.

## Related Research Areas (Non-Exhaustive)

The proposed questions intersect transfer learning, active learning, Bayesian experimental design, multi-armed bandits, meta-learning, program synthesis, analogical reasoning, causal representation learning, open-ended search, multi-agent coordination, and continual learning. This document does not claim priority over those established fields. A future literature review should identify comparable algorithms and empirical benchmarks before making novelty or superiority claims.

## Publication and Evidence Notes

- **Evidence status:** Conceptual proposal; no experiments are reported in this document.
- **Reproducibility:** Future results should be linked to versioned protocols, artifacts, and evaluation data where legally and ethically shareable.
- **License:** Intended repository license Apache-2.0; see `LICENSE.txt` for the authoritative terms.
- **Citation metadata:** See `CITATION.cff` when published.
- **DOI:** Not assigned in this draft; add only after an archival release.
