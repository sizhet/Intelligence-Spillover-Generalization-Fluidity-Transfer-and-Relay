# EXT-001 — Biomimetic Fluidity and Selective Permeability

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Open research extension and falsifiable conceptual proposal  
**Version:** v1.0.0 (theory-first)  
**Status:** Hypotheses and proposed experiments; no empirical validation claimed  
**Date:** 2026-10-31  
**Related documents:** ISGFTR-002, ISGFTR-003, ISGFTR-004, ISGFTR-005, ISGFTR-006, ISGFTR-007, ISGFTR-008, ISGFTR-009, ISGFTR-010; SPEC-001–004; CASE-001–003

## Abstract

Biological organisms routinely adapt their problem-solving behavior under incomplete information, limited energy, noisy perception, and changing environments. They may redirect attention, exploit analogies, recruit other individuals, preserve useful habits, or temporarily explore unfamiliar alternatives. These observations motivate—but do not establish—a possible design principle for artificial intelligence: **intelligence fluidity may benefit from boundaries that are neither uniformly closed nor indiscriminately open, but selectively permeable to information, candidate structures, and actions under different evidence requirements**.

This extension proposes a biomimetically informed, implementation-neutral research framework for **selective permeability**. It distinguishes exploratory information flow from consequential execution, separates rapid adaptation from durable learning, and identifies possible mechanisms including contextual gating, novelty-sensitive exploration, structural analogy, memory-mediated transfer, distributed coordination, and reversible sandbox probing. A staged architecture and experimental program test whether such mechanisms improve verified transfer, adaptation, and resilience relative to fixed routing and unrestricted exploration under matched budgets. Biological examples are treated as sources of hypotheses rather than proof of engineered superiority. The document also addresses negative transfer, excessive permeability, information contamination, coordination costs, and the possibility that simple fixed policies outperform elaborate fluid architectures.

**Keywords:** biomimetic intelligence; intelligence fluidity; selective permeability; adaptive boundaries; structural analogy; exploratory gating; cognitive control; collective learning; evidence relay; negative transfer.

---

## 1. Purpose and Research Boundary

The ISGFTR program asks how capabilities can spill over, generalize, flow, transfer, and relay beyond their initially observed settings. ISGFTR-004 introduces intelligence fluidity and selectively permeable structural boundaries; ISGFTR-005 examines directional intuition and weak-evidence transfer; ISGFTR-006 develops system-centric learning. This extension considers a specific inspiration: living systems often function with flexible, context-sensitive interactions rather than relying exclusively on rigidly preassigned task routes.

The central question is:

> Under what conditions can biologically inspired, selectively permeable boundaries improve an artificial system's ability to discover and verify useful structural transfers without increasing unacceptable error, cost, or risk?

This is not a claim that biological intelligence uses one universal mechanism, nor that an artificial system should imitate biological anatomy. Biological examples differ greatly across species and scales; engineering value must be demonstrated in controlled comparisons.

### 1.1 Scope

This extension concerns: (a) representation and strategy switching; (b) exploratory admission of weak evidence; (c) context-dependent routing across units; (d) reversible testing and evidence preservation; and (e) multi-level adaptation and relay. It does **not** assert consciousness, subjective experience, autonomous AGI, or a biologically faithful brain model. It also does not claim that every boundary should become permeable.

## 2. Working Definitions

**Intelligence fluidity** is the context-sensitive capacity of a problem-solving system to redirect its representations, strategies, tools, collaborators, or computational pathways while maintaining appropriate constraints and evaluation.

**Structural boundary** is an interface or rule that separates tasks, representations, execution rights, evidence scopes, organizational roles, or learning states.

**Permeability** is the conditional ability of specified objects—signals, candidate mappings, evidence, policies, or actions—to cross a structural boundary. It is a property of an interface under conditions, not a global score of intelligence.

**Selective permeability** is the governance of such crossings according to their object type, uncertainty, reversibility, resource cost, provenance, and potential consequences.

**Biomimetic hypothesis** is a proposed engineering mechanism motivated by biological observations and requiring independent evaluation.

**Durable growth** means an improvement that persists across suitable future evaluations and is attributable to a retained learning or structural change, rather than one-off luck or increased resources alone.

These definitions preserve the ISGFTR distinction **Mobility ≠ Utility ≠ Growth**. A system may move information freely without solving tasks better; it may improve one task without retaining the improvement; and it may retain an adaptation that fails outside a narrow environment.

## 3. Biological Inspirations: Analogies, Not Evidence of Transfer

### 3.1 Attention and behavioral switching

Animals frequently shift attention or behavior when stimuli, needs, or risks change. The engineering analogy is a controller that can redirect resources from an ineffective route to an alternative representation or tool. The testable proposition is not that such switching is always beneficial, but that *context-sensitive switching* may outperform a fixed route when task regimes vary and the switching overhead is bounded.

### 3.2 Associative memory and partial similarity

Biological cognition can exploit incomplete cues and remembered associations. An artificial counterpart might retrieve a partially matching precedent, preserve its mismatches, and propose a low-cost test. This suggests candidate discovery beyond exact matching. However, apparent analogy may be spurious; a good analogy generator is not necessarily a good validator.

### 3.3 Exploration and exploitation

Organisms face a tradeoff between exploiting familiar opportunities and exploring uncertain alternatives. The proposed AI analogue is a policy that budgets probes according to expected information value, risk, and cost. The exploration–exploitation problem is already well studied; ISGFTR's contribution is to connect it explicitly to **structural transfer opportunities and evidence relay**, not to claim the tradeoff itself as novel.

### 3.4 Social coordination and distributed adaptation

Social insects and human organizations provide examples of useful behavior emerging through interactions among individually limited participants. They motivate a distinction between learning inside an individual and adaptation of a coordination system. But collective behavior can also amplify mistakes, create congestion, or suppress diversity. System-level improvement must therefore be compared against single-unit and static multi-unit baselines.

### 3.5 Memory, habit, and repeated experience

Repeated experience may modify subsequent choices even when an individual component's internal parameters remain fixed. For engineered systems, an external evidence registry, routing table, or precedent store can carry this temporal relay. The analogy is informative only if experiments distinguish genuine feedback-based adaptation from simple accumulation of more context or computing resources.

## 4. A Taxonomy of Permeable Boundaries

Permeability should be indexed by **what crosses** and **what the receiving side may do with it**.

| Boundary | Admitted object | Potential benefit | Principal risk | Example control |
|---|---|---|---|---|
| Representational | Analogies, alternative encodings | New solution perspectives | Semantic distortion | Typed mapping and residual record |
| Task/domain | Reusable methods or subroutines | Cross-domain transfer | Negative transfer | Target-specific probe |
| Evidential | Weak hints, precedents, counterexamples | Better candidate discovery | Confirmation bias | Provenance and uncertainty labels |
| Organizational | Requests, specialist outputs, proposals | Complementary capabilities | Coordination failure | Role-scoped interfaces |
| Temporal | Memories, outcomes, failed attempts | Persistent learning | Stale or contaminated memory | Versioning and expiry review |
| Execution/authority | Tools, actions, policy changes | Real-world utility | Harm or unauthorized behavior | Explicit authorization and safety gate |

The same candidate may cross an evidential boundary as a hypothesis but must not automatically cross an execution boundary as an approved action.

## 5. The Two-Gate Principle and a Third Authorization Layer

The framework retains the two-gate separation developed in ISGFTR and SPEC-003:

- **Gate A — Exploration admissibility:** Is there sufficient rationale, budget, and safety clearance to investigate a candidate?
- **Gate B — Scoped claim validation:** Does the collected evidence justify a narrowly defined capability claim under stated conditions?

A further **deployment authorization** layer may be required before consequential execution. It is distinct from evidence validation: a capability can be demonstrated in a sandbox without being authorized for production use.

This separation makes permeability asymmetric. Weak signals may enter a *candidate workspace* with relatively low evidential thresholds; verified outputs may enter a *reusable capability registry* only after validation; high-impact actions remain behind independent permissions. A fluid system should therefore be more permissive in **reversible reasoning** than in **irreversible action**.

## 6. Proposed Architecture: Selective Permeability Controller

The proposed architecture has seven logical components:

1. **Context and Boundary Descriptor:** records the current task, domain, permissions, constraints, resources, and uncertainty.
2. **Candidate Inflow Interface:** accepts analogies, weak evidence, prior cases, tools, and requests from external units with provenance.
3. **Directional Opportunity Assessor:** estimates structural relevance, potential value, residual mismatch, and information gain without pretending that heuristic scores are calibrated probabilities.
4. **Permeability Policy Controller:** chooses which candidate objects may cross which boundaries and at what level of trust.
5. **Reversible Probe Sandbox:** tests mappings under bounded costs, controlled inputs, and explicit stopping rules.
6. **Evidence and Counterevidence Registry:** stores results, failures, scope restrictions, and lineage.
7. **Relay and Policy Revision Unit:** transmits validated or unresolved findings and updates future routing or exploration policies under governance.

The architecture is conceptual. A single program may implement several components, or a distributed system may allocate them across agents. The design does not require neural networks, online weight updates, or a particular orchestration platform.

### 6.1 A minimal decision model

For candidate crossing $c$ under context $x$, consider an illustrative policy:

$$
\pi_{\mathrm{perm}}(c,x) \in \{\text{reject},\text{observe},\text{sandbox},\text{validate},\text{authorize}\}.
$$

An exploration priority may be represented as:

$$
Q(c\mid x)=w_v V(c,x)+w_i I(c,x)+w_r R(c,x)-w_k K(c,x)-w_h H(c,x)-w_u U(c,x),
$$

where $V$ is estimated task value, $I$ information value, $R$ structural reuse potential, $K$ cost, $H$ harm or failure exposure, and $U$ unresolved mismatch or uncertainty burden. Weights are policy parameters, not universal constants. These quantities may be ordinal, heterogeneous, or uncertain; naive weighted sums can conceal incomparable criteria. A practical implementation may instead use constrained ranking, Pareto selection, or hard safety exclusions.

**Important:** $Q$ is an exploratory ranking aid, not a calibrated probability of successful transfer and not evidence that a capability exists.

## 7. Selective Permeability as a Dynamic Policy

A fixed boundary policy may be too restrictive in unfamiliar contexts or too permissive in risky ones. The research hypothesis is that boundary policies can adapt using **observed performance, explicit counterevidence, and contextual shifts**.

A dynamic policy should specify:

- **Trigger:** what changed—task distribution, failure signal, new evidence, resource availability, or policy revision?
- **Object type:** what may cross—information, candidate mapping, executable component, or authority?
- **Trust tier:** is the item untested, partially supported, independently replicated, or contested?
- **Scope:** in which contexts and target tasks is the crossing permitted?
- **Reversibility:** can the effects be undone, isolated, or rolled back?
- **Review condition:** what event or time limit causes the policy to be reconsidered?

An adaptive controller must not silently promote exploratory objects into execution rights. The relevant invariant is that **new evidence can update confidence and scope, but cannot bypass an independent authorization requirement**.

## 8. Directional Intuition and Residual-Aware Analogy

Biomimetic flexibility motivates searching beyond exact structural matches. A source domain may share causal or operational relations with a target while differing in units, semantics, constraints, or failure costs. The candidate mapping should therefore retain both a proposed shared core and a residual mismatch:

$$
M_{s\to t}=(C_{\mathrm{shared}},\Delta_{s\to t},\mathcal{R}_{\mathrm{unresolved}}).
$$

Here $C_{\mathrm{shared}}$ denotes hypothesized reusable relations, $\Delta_{s\to t}$ required adaptations, and $\mathcal{R}_{\mathrm{unresolved}}$ the explicitly unmodeled differences. This is a representation proposal, not a proof that a canonical decomposition exists.

An OTHERS residual can be valuable as a *search direction* when standard similarity scores fail. But high novelty can also indicate irrelevance. A useful system should test whether residual-aware candidate selection yields more verified discoveries than novelty-only, similarity-only, or random baselines.

## 9. Fluidity Across Learning Levels

Biomimetic ideas should be assessed at several distinct levels:

| Learning level | Potential adaptive change | What remains fixed in a frozen-unit experiment? |
|---|---|---|
| Unit | Internal model parameters or rules | Model parameters and executable logic |
| Interaction | Communication order and coordination | Underlying unit capabilities |
| Structural | Task decomposition, routing, tool composition | Unit internals |
| Relay | Evidence packaging and reuse | Historical observations are immutable |
| Collective | Shared precedent selection and governance | Individual unit parameters |
| Evolutionary | Population or architecture selection across generations | May require a separate experiment |

The key hypothesis is **learning–execution decoupling**: a system may improve through changes to interaction, structural, or relay policies while its execution units remain unchanged. To support this claim, experiments must freeze unit versions, control tool access and compute budgets, and demonstrate persistent improvements on held-out tasks.

## 10. Three Illustrative Research Scenarios

### Scenario A — Representation switching under ambiguity

A planning system initially treats a problem as sequence optimization. An external hint suggests that a dependency graph better captures the constraints. A permeability controller admits the hint as a candidate, constructs a graph representation in a sandbox, and compares solutions against a fixed baseline. The graph approach is adopted only if target-task evidence supports it. **Failure case:** graph construction overhead exceeds gains or misrepresents dependencies.

### Scenario B — Weak-evidence cross-domain analogy

A software incident-response workflow suggests a possible analogy to community service dispatch: prioritization, resource constraints, escalation, and handoff. The controller admits the analogy for exploration, records nonmatching legal and operational constraints, and runs controlled tests. **Failure case:** the analogy overlooks domain-specific safety requirements; apparent transfer collapses on realistic data.

### Scenario C — Collective adaptation with frozen units

Several specialized fixed units process changing tasks. A shared registry records which routes succeeded, failed, or required intervention. The controller updates its routing and evidence retrieval policies across rounds without changing unit weights. **Failure case:** observed gains disappear when registry size, compute, and task order are controlled; or feedback causes premature convergence to a brittle route.

These scenarios are proposals, not reported experiments or empirical demonstrations.

## 11. Falsifiable Hypotheses

**H-BF1 — Adaptive permeability:** Under controlled distribution shifts, a context-sensitive permeability policy yields higher held-out task utility per fixed cost than static routing, provided that candidate diversity is meaningful. *Falsifier:* no gain or consistent degradation across representative shifts.

**H-BF2 — Asymmetric gates:** Separating exploratory admission from capability validation reduces unsupported capability promotion relative to a single-threshold policy, at comparable discovery recall. *Falsifier:* no reduction or a prohibitive loss of useful discoveries.

**H-BF3 — Residual preservation:** Explicitly tracking unmapped structural differences reduces negative transfer relative to analogy selection without residual records. *Falsifier:* no improvement after matched model and compute controls.

**H-BF4 — Reversible probing:** Sandboxed low-cost tests improve verified useful transfers per exploration budget compared with direct adoption of high-scoring candidates. *Falsifier:* probes provide insufficient information or cost more than they save.

**H-BF5 — Frozen-unit learning:** External routing and evidence-policy updates yield persistent gains on held-out tasks while unit parameters remain frozen. *Falsifier:* gains vanish under proper baseline and memory controls.

**H-BF6 — Counterevidence relay:** Retaining failed analogies and negative outcomes improves future candidate selection versus positive-only memory. *Falsifier:* no measurable benefit, or systematic over-avoidance of productive directions.

**H-BF7 — Permeability calibration:** Policies conditioned on risk, reversibility, and uncertainty outperform uniformly open or uniformly closed policies on a predeclared utility–risk frontier. *Falsifier:* fixed policies dominate under relevant conditions.

**H-BF8 — Boundary drift control:** Versioned provenance and periodic revalidation reduce stale or contaminated transfer reuse compared with an unreviewed memory store. *Falsifier:* no detectable benefit under controlled drift.

Each hypothesis is conditional. Failure in one domain may limit its scope rather than refute every possible implementation; repeated failures across representative domains should nevertheless motivate substantive revision.

## 12. Experimental Design and Baselines

### 12.1 Task environments

Use at least three classes of controlled tasks: (i) representation-switching problems with multiple valid encodings; (ii) cross-domain structural transfer problems with known partial analogies and deliberate mismatches; and (iii) sequential multi-unit tasks with changing task distributions. Split training/design, tuning, and held-out evaluation by *problem family*, not merely by surface wording, to reduce leakage.

### 12.2 Comparison conditions

| Condition | Boundary policy | Evidence handling | Adaptation |
|---|---|---|---|
| B0: Single fixed route | Closed | No transfer candidates | None |
| B1: Static multi-route | Preassigned | No dynamic gating | None |
| B2: Uniformly open | All candidates admitted to sandbox | Minimal filtering | Limited |
| B3: Similarity-only | Threshold on similarity | Positive evidence | Static |
| B4: Novelty-only | Prioritize unfamiliar candidates | Weak evidence | Static |
| B5: Dynamic gating | Contextual admission | Positive and negative evidence | Routing updates |
| B6: Dynamic + residual | Contextual admission | Explicit mismatches and provenance | Routing updates |
| B7: Full proposed architecture | Separate gates and authorization | Auditable evidence relay | Governed policy updates |

All conditions should use matched task sets, model versions, tool availability, and resource budgets. If a method uses more probes or tokens, report that difference rather than attributing gains solely to architecture.

### 12.3 Metrics

Primary outcomes: **held-out task utility**, **verified transfer discovery per unit cost**, **negative-transfer rate**, and **unsupported claim promotion rate**. Secondary outcomes: adaptation latency, probe information gain, calibration of *separately calibrated* confidence estimates, robustness to drift, memory contamination rate, relay reuse success, and reversibility of failed experiments. Report confidence intervals and uncertainty, not only point estimates.

### 12.4 Ablations and adversarial checks

Remove counterevidence, residual tracking, sandboxing, dynamic routing, and provenance separately. Introduce misleading analogies, contradictory sources, stale precedents, domain shifts, and resource constraints. Use independent evaluators and predeclared stopping rules where feasible. Test whether the proposed architecture still helps when fixed baselines are well tuned.

## 13. Evidence, Claims, and Contract Alignment

The extension inherits the contract discipline of the four ISGFTR specifications:

- **SPEC-001:** every capability statement must identify actor, scope, conditions, evidence, and boundary type.
- **SPEC-002:** every opportunity and weak-evidence signal must retain source, uncertainty, proposed mapping, and counterevidence.
- **SPEC-003:** candidate admission, probe authorization, and evidence adjudication must be distinguishable in the lifecycle.
- **SPEC-004:** relay packages must preserve lineage, limitations, negative results, and recipient-specific validation needs.

A useful biomimetic analogy is an **opportunity record**, not a validated capability. An improvement observed in a multi-unit system must be attributed at the appropriate level; it cannot automatically be described as new learning inside its constituent models.

## 14. Minimal Illustrative Contract

The following YAML is a *conceptual example*, not a published machine-validated schema:

```yaml
permeability_candidate:
  id: BF-CAND-001
  status: proposed
  source_context: software-incident-triage
  target_context: community-service-dispatch
  object_type: structural_analogy
  proposed_shared_core:
    - constrained_prioritization
    - dependency_aware_handoff
  unresolved_residuals:
    - domain_specific_safety_rules
    - service_equity_requirements
  evidence:
    strength: weak
    provenance: illustrative_hypothesis
    counterevidence_required: true
  exploration:
    gate_a: pending
    sandbox_only: true
    max_probe_budget: predefined
  validation:
    gate_b: not_evaluated
    held_out_target_tasks: required
  deployment:
    authorization: prohibited_until_separate_review
  relay:
    preserve_negative_results: true
    require_scope_and_version: true
```

The example deliberately prevents an untested analogy from acquiring operational authority.

## 15. Failure Modes and Counterarguments

**Biological analogy fallacy.** The existence of flexible biological behavior does not imply that the proposed computational mechanism is correct. Response: evaluate engineered mechanisms directly; remove biological terminology if it adds no predictive value.

**Excessive openness.** A system may admit too many low-value signals, leading to noise, distraction, and compute inflation. Response: enforce bounded portfolios, explicit information-value tests, and hard risk constraints.

**Excessive closure.** A conservative policy may miss rare but valuable transfers. Response: reserve a measured exploration budget and evaluate discovery recall, not just precision.

**Negative transfer and semantic drift.** Analogies can hide crucial differences. Response: preserve residuals, use target-domain checks, and disallow unsupported promotion.

**Policy Goodhart effects.** Optimizing a proxy for discovery may generate easy-to-validate but trivial candidates. Response: use independent downstream utility, novelty-adjusted value, and adversarial audits.

**Memory contamination.** Repeated relay can amplify mistaken precedents. Response: immutable provenance, contradiction records, expiry/revalidation, and source diversity checks.

**Coordination overhead.** Multi-unit fluidity may be slower and less reliable than a single competent model. Response: measure end-to-end cost and compare with strong fixed baselines.

**Unclear learning attribution.** A larger memory or tool inventory can look like learning. Response: control context, resources, unit versions, and exposure; test persistence and transfer to held-out tasks.

**Risk of unauthorized action.** Flexible exploration may be mistaken for permission to act. Response: keep action authorization independent of candidate ranking and evidential support.

## 16. A Five-Phase Research Roadmap

**Phase 1 — Boundary inventory.** Define candidate object types, permissions, task families, baselines, and outcome metrics. Publish a compact threat and failure model.

**Phase 2 — Controlled analogy probes.** Test representation switching and cross-domain mappings in a sandbox, with explicit residuals and held-out targets.

**Phase 3 — Adaptive permeability.** Compare fixed, open, closed, and context-sensitive gating under matched budgets and domain shifts.

**Phase 4 — Temporal and collective relay.** Add versioned evidence memory and frozen execution units; measure persistent system-level adaptation and negative-evidence reuse.

**Phase 5 — Independent replication and revision.** Release protocols, anonymized or synthetic tasks, negative results, and contract conformance checks; revise or narrow claims based on replication.

Progression between phases should depend on evidence quality, not an assumed inevitable trajectory toward more general intelligence.

## 17. Open Research Questions

1. Which forms of permeability are most valuable: representational, evidential, organizational, temporal, or execution-related?
2. Can a controller learn when to *close* a boundary as effectively as when to open it?
3. What minimal evidence is sufficient to justify a reversible probe without overloading the system?
4. How should heterogeneous costs, uncertainty, and risk be compared without hiding hard constraints inside one scalar score?
5. When does a partial analogy help despite a large residual, and when does it become misleading?
6. How can the system distinguish an adaptive policy from an ever-growing collection of ad hoc exceptions?
7. Can collective memory improve adaptation without creating correlated group errors?
8. Which biological inspirations generate novel, testable predictions beyond established adaptive control and multi-agent learning?
9. How should permeability policies differ between low-risk research sandboxes and high-stakes deployments?
10. What evidence would show that fluidity contributes to durable, transferable system-level growth rather than temporary routing efficiency?

## 18. Relation to Other ISGFTR Research

This extension elaborates **ISGFTR-004** by converting selective permeability into candidate object types, conditional gates, and a testable controller. It draws on **ISGFTR-003** for structural reuse and residual preservation; **ISGFTR-005** for directional intuition; **ISGFTR-006** for system-centric and frozen-unit learning; **ISGFTR-007** for temporal relay; and **ISGFTR-008** for capability prospecting. **ISGFTR-009** supplies the caution that improved transfer or system adaptation does not demonstrate AGI. **ISGFTR-010** supplies the open research architecture and collective validation perspective.

Related research traditions include adaptive control, attention and cognitive flexibility, reinforcement learning, hierarchical planning, transfer learning, multi-agent coordination, organizational learning, and biological collective behavior. These are established areas with substantial prior work. ISGFTR proposes a *cross-cutting research organization* for their interactions; novelty and empirical advantage remain to be established.

## 19. Suggested Figure Placement

- **Primary:** `figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png` — insert after Section 6 to illustrate candidate inflow, gating, sandbox validation, and relay.
- **Supporting:** `figures/Fig-003-Five-Characteristics-of-Intelligence-Flow.png` — reference near Section 2 for the relation between fluidity, transfer, and relay.
- **Supporting:** `figures/Fig-006-System-Centric-Multi-Level-Learning.png` — reference near Section 9 for the learning–execution distinction.
- **Supporting:** `figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png` — reference near Section 16 for evidence feedback and temporal relay.

Figure filenames indicate assets; the present document does not imply that the figures have been empirically validated.

## 20. Conclusion and Collective Learning Invitation

Biological adaptability offers useful prompts for asking how intelligence can move across structural boundaries. The actionable research proposal is **selective permeability**: admit uncertain ideas for bounded exploration, demand target-specific evidence before capability claims, and require independent authorization before consequential actions. This preserves the value of weak evidence without treating it as proof, and it connects exploratory fluidity to structural relay and collective learning.

The hypothesis may fail. Static routing may prove sufficient; adaptive gates may cost more than they save; biological metaphors may add little beyond existing control theory. These outcomes would still be informative if experiments preserve their methods, evidence, and counterexamples. Researchers are invited to test the mechanisms independently, contribute negative findings, compare against strong baselines, and revise the architecture through transparent structural relay.

**Research stance:** Theory-first; specification and conformance before runtime; explicit uncertainty and counterevidence; no AGI achievement claim; collective-learning-friendly.
