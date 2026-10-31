# CASE-003 — Weak-Evidence Capability Prospecting and Relay

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Illustrative research case and falsifiable experimental protocol  
**Version:** v1.0.0 (theory-first)  
**Status:** Proposed experiment; no empirical findings claimed  
**Date:** 2026-10-31  
**Related documents:** ISGFTR-003–010; SPEC-001–004; CASE-001–002

## Abstract

This case proposes a controlled experiment for discovering and testing *unobserved but plausible* capability transfers from incomplete, heterogeneous, and sometimes contradictory evidence. A prospecting system receives a fixed inventory of source capabilities, target tasks, structural descriptions, prior attempts, and limited probing resources. It must rank candidate transfers, select experiments, distinguish directional hints from verified capability claims, and relay both successful and unsuccessful results to subsequent research cycles. The main hypothesis is that **structured weak-evidence prospecting**, combined with explicit uncertainty, residual tracking, and feedback, can discover useful transfer opportunities more efficiently than random search or naive similarity matching under matched budgets.

The study is intentionally agnostic about whether a discovered transfer is implemented by a language model, symbolic program, human researcher, or hybrid system. It distinguishes prospecting quality from downstream task performance and separates an observed gain from durable system learning. No success rates, AGI implications, or superiority claims are asserted without future experiments.

**Keywords:** capability prospecting; weak evidence; directional intuition; OTHERS residual; structural transfer; two-gate validation; counterevidence; exploration portfolio; temporal relay; collective learning.

---

## 1. Motivation and Problem Statement

Intelligence research often evaluates a capability only after someone has formulated a suitable task. This leaves an important discovery problem: which *untried* tasks should be tested, and what evidence should guide that choice? A trained model may have useful skills outside the tasks on which it has been explicitly assessed. A structural tool developed in one domain may transfer to another with partially shared constraints. A failed experiment may reveal a boundary or missing adaptation that makes a different experiment more promising.

Neither broad semantic similarity nor a compelling analogy is sufficient evidence of transfer. Under limited experimental budgets, indiscriminate exploration is expensive, and weak signals are prone to confirmation bias. The proposed case tests whether a prospecting process can turn such signals into **auditable experimental priorities**, then learn from the results without treating conjectures as established capabilities.

The central research question is:

> Can a structured, uncertainty-aware prospecting and relay process improve the discovery of independently verified cross-domain capability transfers under fixed evaluation and resource budgets?

This is a claim about a *research process*, not an assertion that a particular model possesses hidden general intelligence.

## 2. Research Questions

- **RQ1 — Discovery:** Does structured prospecting find more verified useful transfers per unit of exploration cost than random or similarity-only selection?
- **RQ2 — Weak evidence:** Which weak-evidence types add predictive value beyond obvious task similarity?
- **RQ3 — Residuals:** Does explicit representation of unmatched source–target constraints reduce negative transfer?
- **RQ4 — Calibration:** Are prioritization scores calibrated, or do they merely rank candidates? What evidence is needed before probability language is justified?
- **RQ5 — Relay:** Do prior successes, failures, and unresolved questions improve prospect selection in later rounds?
- **RQ6 — Generalization:** Does any improvement survive evaluation on new task families and withheld structural patterns?
- **RQ7 — Governance:** Can the system preserve provenance, contradictory evidence, and scoped claims through repeated relays?

## 3. Working Definitions and Research Boundaries

**Capability profile:** A scoped description of an agent or system's demonstrated task competence, including evaluation conditions, resources, uncertainty, and provenance, as defined in SPEC-001.

**Spillover opportunity:** An unverified hypothesis that a source capability or reusable structure might help solve a target task beyond the currently observed capability boundary. Opportunity status is not a capability claim.

**Weak evidence:** A signal that justifies investigating a hypothesis but does not independently establish it. Examples include partial structural correspondence, shared constraint patterns, historical precedents, suggestive failure traces, and perspective-dependent directional measurements.

**Directional intuition:** A mechanism for proposing or prioritizing candidate transfer directions before full verification. Its outputs may be heuristic scores and need not be calibrated probabilities.

**OTHERS residual:** The unmatched or poorly explained part of a source–target comparison, including missing prerequisites, incompatible constraints, unrepresented concepts, or uncertainty about the mapping.

**Probe:** A bounded, pre-registered test of a transfer hypothesis with defined baselines, outcomes, budgets, and stop conditions.

**Structural relay:** The transfer of a versioned, provenance-bearing research object—hypothesis, mapping, protocol, evidence, counterevidence, or unresolved question—to another process, time, or research participant.

**Durable learning:** A persistent improvement in prospect selection or validated capability across held-out tasks, not merely one successful trial or increased computation.

These concepts refer to four distinct capability boundaries: *generative* (what candidate behaviors can be proposed), *observed* (what has been tested), *reachable* (what can be achieved with specified resources and adaptations), and *evolvable* (what can change after a specified learning or relay process). They should not be assumed to form a single ordered scalar hierarchy.

## 4. Illustrative Research Setting: Scheduling-to-Software Transfer

Consider a bounded source system that reliably handles **community-service scheduling**: ordering jobs under time windows, precedence constraints, capacity limits, and exception handling. The target domain is **software maintenance planning**: ordering dependent changes, allocating reviewers, observing release windows, and handling rollback risk.

The domains have superficial differences, but share candidate structural features: dependency graphs, resource allocation, deadlines, conflict resolution, and verification steps. Potential transferable pieces include topological ordering, constraint checking, priority adjustment, and exception escalation.

However, there are crucial residuals. A code change can introduce security or correctness regressions; reviewer competence is not equivalent to a service crew's capacity; release rollback has domain-specific semantics; and a passing schedule does not prove software correctness. These differences must remain visible rather than being folded into a misleading shared core.

The experiment uses this pair as a **motivating example**, not as proof of transfer. Additional unrelated and adversarial pairs are required to assess whether prospecting is genuinely discriminative.

### 4.1 Candidate transfer inventory

Create a prospect pool containing at least four categories:

1. **High-plausibility structural pairs:** different domains with demonstrably shared abstract constraints.
2. **Surface-similar but structurally incompatible pairs:** similar vocabulary with incompatible causal or operational rules.
3. **Surface-dissimilar but structurally related pairs:** shared dependency or allocation structures hidden by domain language.
4. **Low-evidence and deliberately misleading pairs:** candidates intended to expose overconfident inference.

Candidate category labels are for experimental construction and must be hidden from the prospecting methods during selection.

## 5. Minimal Architecture

The MVP separates discovery, evaluation, and relay responsibilities. A single model may implement multiple roles, but the experimental records must distinguish them.

| Component | Responsibility | Primary output |
|---|---|---|
| Capability registry | Maintain source capability profiles and observed boundaries | Versioned capability profiles |
| Opportunity generator | Propose source–target structural mappings | Spillover Opportunity Records (SORs) |
| Directional assessor | Rank candidates using explicit evidence and costs | Priority scores and rationale |
| Residual analyst | Identify unmatched constraints and failure risks | OTHERS residual register |
| Probe planner | Register controls, budgets, and outcome criteria | Probe protocols |
| Independent evaluator | Execute or assess pre-registered tests | Evidence and counterevidence bundles |
| Relay registry | Preserve outcomes, revisions, and open questions | Versioned Structural Relay Units |
| Policy controller | Enforce resource limits and claim gates | Authorization and adjudication decisions |

The architecture may use retrieval, language models, graph methods, symbolic rules, or metric-native scoring. The case does **not** require a particular representation technology.

## 6. Sources and Classification of Weak Evidence

Weak evidence is recorded as *typed observations*, not blended into an opaque confidence claim.

### 6.1 Structural correspondence

Examples include shared partial order constraints, conserved subgraphs, analogous preconditions, or compatible state transitions. Record both matched and unmatched features. A mapping that preserves only terminology is weaker than one that preserves task-relevant relations.

### 6.2 Historical precedents

Prior successful or failed transfers may suggest reusable mechanisms. Precedents must include domain scope, conditions, evaluation method, and failure details. A precedent from an overlapping benchmark must not be counted as independent replication.

### 6.3 Directional measurements

Directional assessments may compare candidate adaptations in a task-native space without requiring a single global embedding. For example, a planner may assess whether a proposed mapping reduces constraint violations under a limited dry run. Such measurements are **task-specific signals**, not general evidence of semantic equivalence.

### 6.4 Residual and counterevidence signals

Unmatched requirements, contradictory cases, high adaptation cost, and prior negative transfer can lower priority or prompt a narrower hypothesis. Negative evidence should not be discarded merely because it reduces apparent discovery yield.

### 6.5 Uncertainty and provenance

Every signal records source, date or version, observation conditions, known dependencies, and uncertainty. Duplicate or correlated signals must not be counted as independent support.

## 7. Canonical Opportunity Record

The following YAML is **illustrative**, not an empirical record. Field names are proposed for interoperability and may be refined by SPEC-002.

```yaml
schema: isgftr.spillover-opportunity.v1
opportunity_id: SOR-CASE003-001
status: hypothesized
source_capability_ref: CAP-SCHEDULING-001
target_task_ref: TASK-SOFTWARE-RELEASE-001
hypothesis: >
  A dependency-aware scheduling core may improve ordering of
  software maintenance changes under explicit release constraints.
structural_mapping:
  shared_core:
    - precedence_constraints
    - finite_resource_allocation
    - deadline_sensitive_prioritization
  required_adaptations:
    - reviewer_qualification_constraints
    - code_regression_checks
  others_residual:
    - rollback_semantics
    - security_impact
    - uncertain_review_effort
weak_evidence:
  - evidence_id: WE-001
    type: structural_correspondence
    source: design_review
    interpretation: exploratory_hint_only
  - evidence_id: WE-002
    type: counterevidence
    source: hypothetical_failure_analysis
    interpretation: software_correctness_not_implied
priority_assessment:
  score: null
  score_type: uncalibrated_exploration_priority
  rationale: requires_pre_registered_probe
claim_scope: no_verified_transfer_claim
next_action: propose_probe
```

A score of `null` is preferable to a fabricated numeric confidence. If a scoring implementation supplies a value, it must state the scale, training data, evaluation procedure, and whether the score is calibrated.

## 8. Prospecting Portfolio and Priority Assessment

For candidate opportunity $i$, a possible **exploration utility** is:

$$
U_i = \alpha V_i + \beta I_i + \gamma R_i - \delta C_i - \epsilon H_i - \zeta D_i,
$$

where $V_i$ is estimated task value, $I_i$ expected information gain, $R_i$ potential structural reuse, $C_i$ probe cost, $H_i$ harm or negative-transfer risk, and $D_i$ evidence-dependency or redundancy penalty. Weights are policy choices, not universal constants. The terms require operational definitions and should be normalized or otherwise made comparable before use.

A second option is **Pareto selection** rather than a single score: choose candidates that are not dominated across value, uncertainty reduction, cost, and risk. A portfolio may intentionally include high-uncertainty and negative-control prospects to avoid learning only from easy successes.

An exploration-priority score is **not** automatically a probability of transfer success. Calibration requires outcome labels, held-out assessment, and explicit uncertainty estimation.

## 9. Two-Gate Lifecycle

### Gate A — Exploration admissibility

A prospect may enter testing only if it has a coherent, falsifiable hypothesis; adequate provenance; a bounded probe; an acceptable risk profile; and an explicit resource budget. Weak evidence may be sufficient to justify *testing*, not to justify *deployment* or a broad capability claim.

### Probe execution

The registered protocol identifies task samples, controls, evaluation metrics, seed handling, budgets, evaluator independence, and stopping rules. Where feasible, it is frozen before outcomes are inspected. Deviations are logged rather than silently incorporated.

### Gate B — Scoped evidence adjudication

A positive result supports only the tested capability under its observed conditions. A broader transfer claim requires additional task families, replications, and robustness checks. Inconclusive and negative outcomes remain first-class records.

### Relay and revision

Results are packaged with their source opportunity, mapping, protocols, evidence, counterevidence, version lineage, and unresolved residuals. Later cycles may revise priorities or hypotheses without rewriting the original history.

## 10. Experimental Conditions and Baselines

Use matched candidate pools, probe budgets, evaluator access, and compute limits wherever possible.

| ID | Condition | Purpose |
|---|---|---|
| B0 | Random candidate selection | Establish chance discovery efficiency |
| B1 | Surface lexical/embedding similarity | Test conventional similarity ranking |
| B2 | Structural matching only | Isolate explicit structural correspondence |
| B3 | Directional weak-evidence scoring | Test direction-aware prioritization |
| B4 | B3 plus explicit OTHERS residual | Test value of mismatch awareness |
| B5 | B4 plus historical positive relay | Test benefit of successful precedents |
| B6 | B4 plus positive and negative relay | Test benefit of counterevidence retention |
| B7 | Full prospecting with policy and active information gain | Test combined lifecycle |
| B8 | Full method with shuffled evidence labels | Negative control for spurious patterns |
| B9 | Full method without temporal memory | Separate single-round discovery from learning |

If methods use different numbers of model calls, tokens, retrievals, or tool invocations, compare at both equal monetary/compute cost and equal number of probes. Do not attribute gains to better intelligence when they may be explained by more resources.

## 11. Dataset Construction and Leakage Controls

Construct a candidate pool across several domains, such as scheduling, software change planning, inventory allocation, document workflows, and constrained graph tasks. Include cases that are structurally similar but lexically distant and cases that are lexically similar but structurally incompatible.

Split evaluation along **task instances**, **domain pairs**, and **structural templates**. The strongest generalization test withholds entire source–target template families. Any model-based evaluator or candidate generator must have documented access to the pool; previously seen benchmark solutions are a possible confound.

Maintain independent human or executable reference checks for whether a transfer is useful. Blind adjudication of the prospecting method is preferable when feasible. Avoid selecting only candidates that the full method already scores highly.

## 12. Primary and Secondary Metrics

**Primary metric — verified discovery efficiency:**

$$
\mathrm{VDE}(B) = \frac{\#\text{ independently verified useful transfers found by budget }B}{\text{total prospecting and probe cost consumed by }B}.
$$

Report both numerator and denominator with uncertainty intervals. A transfer counts only when it exceeds a pre-registered baseline and satisfies domain-specific safety or correctness constraints.

Secondary metrics include:

- **Precision at probe budget $k$:** fraction of tested top-$k$ candidates independently verified useful.
- **Recall within labeled pool:** fraction of all verified useful opportunities discovered, when a sufficiently exhaustive reference set exists.
- **Negative-transfer rate:** fraction of tested or adopted mappings that worsen target outcomes relative to controls.
- **Information gain per cost:** reduction in uncertainty about candidate mechanisms, under an explicitly defined estimator.
- **Residual detection:** sensitivity and specificity for known incompatible constraints.
- **Calibration:** reliability curves and Brier score, *only if* predicted probabilities are produced.
- **Relay benefit:** held-out discovery efficiency in later rounds with versus without prior evidence.
- **Robustness:** results across seeds, task families, and shifted environments.
- **Audit completeness:** fraction of claims with linked provenance, protocols, counterevidence, and decision records.

Also report time-to-discovery, model calls, tokens, tool use, human review effort, and failure severity. Do not collapse all measures into one headline score.

## 13. Testable Hypotheses

**H1 — Prospecting efficiency.** Under matched budgets, structured weak-evidence prospecting yields higher verified discovery efficiency than random selection. *Falsifier:* no reproducible advantage on held-out candidate pools.

**H2 — Beyond surface similarity.** Structural and directional evidence improves ranking for surface-dissimilar but structurally related pairs relative to lexical similarity alone. *Falsifier:* no gain after controlling for retrieval and compute.

**H3 — Residual-aware safety.** Explicit OTHERS residual analysis reduces negative transfer or improves detection of incompatible mappings. *Falsifier:* residual tracking adds cost without measurable safety or selection benefit.

**H4 — Negative-evidence relay.** Retaining counterevidence improves later-round candidate selection compared with positive-only history. *Falsifier:* no improvement, or systematic over-avoidance of genuinely useful opportunities.

**H5 — Temporal learning.** A fixed execution model with updated prospecting records improves on held-out future rounds. *Falsifier:* gains disappear when repeated examples and extra context are controlled.

**H6 — Information-value portfolio.** Explicit information gain and diversity selection improves long-run discovery over greedy high-score selection. *Falsifier:* equal-budget portfolio search fails to outperform a well-tuned greedy baseline.

**H7 — Evidence integrity.** Enforcing two-gate claims and provenance requirements reduces unsupported capability assertions without an unacceptable loss in verified discovery throughput. *Falsifier:* no reduction in unsupported claims or prohibitive evaluation cost.

**H8 — Cross-domain generality.** Improvements persist when whole structural templates or domain pairs are held out. *Falsifier:* results are confined to known or near-duplicate patterns.

All hypotheses require preregistered metrics, sample sizes or power considerations, and independent replication before strong conclusions.

## 14. Relay Experiment: Learning From Repeated Trials

Organize trials into sequential rounds. In Round 1, prospecting methods receive only a shared initial capability inventory and weak-evidence corpus. In subsequent rounds, some conditions receive versioned evidence bundles from earlier trials; others receive no history or positive-only history.

A **relay unit** should contain:

- the original opportunity and source–target mapping;
- probe protocol, evaluator version, and resource budget;
- outcomes, uncertainty, and failure cases;
- negative or contradictory evidence;
- residuals that remain unresolved;
- any proposed structural update and its justification;
- conditions under which a successor may reuse the result.

Repeating an execution can contribute evidence even if no new capability appears. However, repeated evidence is useful only if it changes a future decision or improves uncertainty estimates without double-counting correlated observations. Record the distinction between **data accumulation**, **decision improvement**, and **durable capability growth**.

## 15. A Minimal Relay Record

```yaml
schema: isgftr.structural-relay.v1
relay_id: SRU-CASE003-001
parent_opportunity: SOR-CASE003-001
source_protocol: PROBE-CASE003-001
source_evidence_bundle: EB-CASE003-001
result_state: inconclusive
claim_state: under_review
validated_scope: null
counterevidence_refs:
  - CE-CASE003-001
remaining_residuals:
  - security_impact
  - uncertain_review_effort
proposed_next_probe: >
  Evaluate dependency ordering separately from code-correctness
  claims using held-out software maintenance tasks.
relay_decision: retain_as_research_evidence
lineage:
  version: 1
  supersedes: null
```

The example is a **schema illustration**; the named records do not represent executed tests. A relay recipient must verify schema validity and evaluate target-context applicability before adopting a recommendation.

## 16. Failure Modes and Counterarguments

### 16.1 Attractive analogies without operational transfer

Two domains may share an appealing narrative but lack the invariants required for useful reuse. Remedy: require an explicit mapping and target-side test.

### 16.2 Hidden data leakage

A language model may have encountered similar examples during training or retrieval. Remedy: use fresh generated tasks, withheld templates, and leakage audits; interpret results conservatively.

### 16.3 Uncalibrated scoring and score gaming

A priority score can become optimized for easy-to-measure opportunities rather than important ones. Remedy: preserve separate metrics for value, information gain, cost, risk, and novel discovery; include adversarial controls.

### 16.4 Correlated evidence and false confidence

Multiple documents may repeat the same underlying claim. Remedy: track evidence dependencies and source independence.

### 16.5 Negative transfer and unsafe adaptation

A transferable scheduling abstraction may still fail when applied to security-critical code changes. Remedy: keep target-specific correctness gates and domain residuals.

### 16.6 Survivorship bias in relay registries

Sharing only successes inflates estimated transfer potential. Remedy: record failures, inconclusive trials, and abandoned hypotheses.

### 16.7 Overfitting to a prospecting benchmark

A system may learn benchmark-specific cues rather than general discovery principles. Remedy: hold out structural templates and test across independent task-generation pipelines.

### 16.8 Confusing organizational improvement with model learning

A fixed model may benefit from better retrieval or routing without changing its intrinsic competence. Remedy: report model-level, system-level, and learning-layer changes separately.

### 16.9 Costly exploration without growth

A prospecting process can generate endless questions and consume resources without useful discoveries. Remedy: budget caps, stop conditions, and cost-adjusted discovery metrics.

## 17. Governance and Claim Discipline

Prospecting systems should enforce three distinct permissions: permission to **propose**, permission to **probe**, and permission to **adopt or deploy**. A successful exploratory probe does not automatically authorize high-stakes deployment. Any claim about transfer must state the tested source capability, target distribution, resource configuration, evaluation protocol, and observed limitations.

Claims should use scoped statuses such as `hypothesized`, `under_probe`, `observed`, `replicated`, `contested`, or `retracted`. Later counterevidence must remain visible. Audit trails should support revisions without erasing original records.

This case does not require public release of sensitive task data. Evidence can be shared through redacted or aggregated relay objects when privacy, security, or contractual obligations apply.

## 18. Interface With the Four ISGFTR Specifications

| Specification | Role in CASE-003 |
|---|---|
| **SPEC-001** | Source capability profiles, scoped boundaries, attribution, and claim states |
| **SPEC-002** | Spillover Opportunity Records, weak evidence, directional assessments, residuals, and counterevidence |
| **SPEC-003** | Prospecting/probing state machine, Gate A and Gate B, preregistration, and adjudication |
| **SPEC-004** | Versioned structural relay, provenance preservation, recipient validation, and collective learning |

The case is an example of how these proposed contracts could be combined; it does not assert that their schemas have been implemented or externally standardized.

## 19. Five-Phase MVP Validation Roadmap

**Phase 1 — Static candidate pool.** Construct source capability profiles, target tasks, and deliberately mixed opportunity categories. Establish random and similarity baselines. Freeze evaluation rules.

**Phase 2 — Structured prospecting.** Add typed weak evidence, structural correspondences, and residual tracking. Evaluate ranking quality without executing all transfers.

**Phase 3 — Bounded probing.** Run preregistered probes under equal budgets; record successes, failures, uncertainty, and negative transfer.

**Phase 4 — Temporal relay.** Introduce versioned positive and negative evidence; test whether future prospect selection improves on held-out tasks without changing execution-model weights.

**Phase 5 — Independent replication and transfer.** Replicate with new domain pairs, withheld structural templates, alternative evaluators, and independent researchers. Publish negative and inconclusive findings alongside positive results.

Advancement between phases should depend on documented conformance and evidence quality, not a preset expectation of success.

## 20. Open Questions

1. Which weak-evidence types are consistently useful across domains, and which are irreducibly domain-specific?
2. Can metric-native directional scores be compared across perspectives without misleading normalization?
3. How should a prospecting system represent fundamentally unknown residuals rather than only known missing features?
4. When does a successful structural analogy constitute a genuine transfer rather than a convenient restatement of task knowledge?
5. What minimum evidence justifies sharing a prospect as a reusable research object?
6. How should the system discount repeated or dependent observations in a large relay network?
7. Can negative evidence improve exploration without creating an overly conservative policy?
8. How much of observed improvement comes from prospecting versus better downstream execution tools?
9. What are the limits of frozen-unit structural learning under sustained domain shift?
10. Can a portfolio of unanswered questions become a useful collective learning resource even when most prospects fail?

## 21. Suggested Figures

- **Primary:** `figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png` — insert after Section 5 to show the capability inventory, prospecting loop, two gates, and evidence feedback.
- **Supporting:** `figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png` — reference in Sections 6–9 for directional evidence and exploratory gating.
- **Supporting:** `figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png` — reference in Section 14 for temporal relay and iterative evidence accumulation.

These are figure references; the experiment does not depend on the figures' existence.

## 22. Conclusion and Collective Learning Invitation

This case reframes possible intelligence spillover as an **experimental search problem**. A useful research system should not merely generate more analogies or more confident claims. It should find promising transfer questions, choose economical tests, preserve unmatched structure, expose counterevidence, and carry forward what each experiment teaches. The proposed architecture therefore connects *Prospect → Probe → Validate → Relay → Learn → Prospect* while keeping exploration permission separate from verified capability claims.

The outcome is deliberately open. Weak-evidence prospecting may outperform simple baselines, may work only in certain domains, or may fail under strict controls. Each outcome is informative if the protocols and evidence are reusable. Researchers are invited to challenge the candidate representations, propose adversarial cases, implement alternative prospecting strategies, and publish reproducible negative results. Such contributions would strengthen the collective research process regardless of whether the central hypotheses survive.

---

**Document status:** Theory-first proposed case. All examples, record identifiers, and experiment designs are illustrative. No measurements, validated discoveries, AGI capabilities, or external standards are claimed.
