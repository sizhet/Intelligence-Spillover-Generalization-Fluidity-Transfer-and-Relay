# Testable Hypotheses — Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Falsifiable research hypotheses and experimental design register  
**Version:** 1.0.0 (theory-first)  
**Status:** Proposed tests; no results claimed  
**Date:** 2026-10-30

## 1. Purpose

ISGFTR proposes that intelligence can exhibit spillover beyond a narrow training objective or task specification; generalize by reusing structure; move fluidly between representations and contexts; transfer to new tasks; and relay evidence, structures, and learned policies across agents and time. None of these propositions, alone or together, demonstrates artificial general intelligence (AGI). This document converts the program's conceptual claims into **scoped, falsifiable hypotheses** with explicit baselines, outcomes, competing explanations, and conditions for revision.

The primary experimental question is not whether an architecture can produce an attractive demonstration. It is whether a precisely specified mechanism adds **reproducible, out-of-sample value** relative to credible alternatives under comparable resources.

Research claims MUST identify the tested system, tasks, data, model versions, tools, time horizon, evaluation budget, and limitations. Exploratory findings MUST NOT be described as confirmatory results. Negative evidence and failed transfers SHOULD be retained and made available for future structural relay, subject to privacy and security constraints.

## 2. Hypothesis Registry at a Glance

| ID | Domain | Main proposed effect | Principal contrast |
|---|---|---|---|
| H-BND-01 | Capability boundaries | Operationally distinct observed and reachable capabilities | Fixed-task testing vs controlled composition/tool access |
| H-SP-01 | Spillover | Novel capability beyond measured task overlap | Held-out structural tasks vs leakage/overlap controls |
| H-FG-01 | Folding/generalization | Shared core improves transfer | Structural core vs matched generic abstraction |
| H-FG-02 | Residual preservation | Residual-aware transfer reduces negative transfer | Core + residual vs core alone |
| H-FL-01 | Fluidity | Selective boundary policy improves risk-adjusted performance | Adaptive gating vs fixed/open/closed gating |
| H-DI-01 | Directional intuition | Weak-evidence prospecting increases useful discoveries per budget | Directional scoring vs random and similarity ranking |
| H-DI-02 | Counterevidence | Negative evidence improves later prospect selection | Evidence registry with vs without failures |
| H-TR-01 | Transfer | Structural transfer survives domain shift | Explicit mapping vs direct prompt/retrieval |
| H-TR-02 | Relay | Provenance-aware relay improves downstream reuse | Complete vs stripped relay package |
| H-ML-01 | System learning | Frozen units can yield durable system-level improvement | Adaptive structure vs fixed orchestration |
| H-ML-02 | Attribution | Structural gains persist without hidden unit adaptation | Frozen, audited units vs adaptive units |
| H-RG-01 | Recursive relay | Learning from prior trials improves future exploration | Recursive feedback vs independent trials |
| H-RG-02 | Repetition | Repeated execution adds value only when evidence is integrated | Repetition + update vs repetition alone |
| H-EV-01 | Governance | Two-gate process reduces unsupported capability claims | Separate exploration/claim gates vs single gate |
| H-AGI-01 | Generality limits | Broad improvement remains bounded and measurable | Multi-domain held-out evaluation and scaling tests |

**Registry rule:** Each ID denotes a research proposal, not a confirmed result. Investigators may split or refine hypotheses, but SHOULD retain stable IDs and version the revised formulations.

## 3. Common Experimental Protocol

### 3.1 Units, data, and preregistration

A **capability unit** is an identifiable model, agent, tool, or composed system evaluated under a declared context. A **trial** is one independently logged execution of a registered task instance. A **transfer opportunity** is a proposed source-to-target mapping not yet validated. A **relay unit** is a versioned package containing a claim, structure, evidence, provenance, limitations, and unresolved residuals.

Before confirmatory testing, register:

1. Target population of tasks and how instances are sampled.
2. Frozen model and tool versions; any permitted adaptive components.
3. Primary and secondary outcomes, direction of benefit, and failure thresholds.
4. Baselines, ablations, compute/token/tool budgets, and stopping rules.
5. Data-leakage checks, independent test partitions, and evaluator procedures.
6. Statistical plan, including clustering by task family and handling repeated trials.
7. Safety, privacy, and execution-permission constraints.

Exploratory probes may be adaptive, but their results SHOULD be labeled exploratory. Confirmation SHOULD use newly held-out task families or an independent replication cohort.

### 3.2 Primary outcome families

- **Utility:** validated task success, quality, cost-adjusted performance, or regret against a declared baseline.
- **Discovery efficiency:** independently validated useful prospects per fixed exploration budget.
- **Transfer robustness:** performance under target-domain shift and residual mismatch.
- **Negative-transfer rate:** fraction and severity of transfers that worsen the baseline.
- **Durability:** retained benefit on later, unseen tasks after the learning update.
- **Relay fidelity:** completeness of provenance, reproduction success, and semantic consistency.
- **Claim discipline:** false-positive capability claims and inappropriate deployment authorizations.

All outcomes MUST specify denominators and resource accounting. A higher score under a larger budget is not, by itself, evidence of a superior mechanism.

### 3.3 Statistical and causal safeguards

Use paired task instances where feasible; report confidence intervals or uncertainty estimates, not only point estimates. Avoid treating multiple prompts on the same task as independent evidence. Control for selection bias introduced by prospecting and multiple hypothesis searches. Prefer a preregistered primary outcome; disclose exploratory subgroup findings and corrected or hierarchical analyses where appropriate. Report effect sizes, practical significance, and failures. A null result with narrow uncertainty can meaningfully constrain a theory; an underpowered null result cannot.

## 4. Boundary and Spillover Hypotheses

### H-BND-01 — Observed and reachable capability are operationally distinct

**Hypothesis.** Under fixed task conditions, some capabilities absent from a system's direct observed performance become reproducibly reachable through declared composition, retrieval, tools, or structural routing, without changing the base model's weights.

**Design.** Freeze the model. Compare (A) direct execution, (B) matched-budget prompting, (C) static tool pipeline, and (D) structured composition with audited routing. Use tasks requiring verifiable intermediate artifacts and independent scoring. Distinguish the base model's observed capability from the composed system's reachable capability.

**Primary measure.** Incremental validated success over the strongest budget-matched baseline, with resource costs and failure rates.

**Falsifier or narrowing evidence.** Apparent gains disappear after matching tool access, token budgets, and task decomposition, or arise only on previously seen templates.

**Interpretation boundary.** This tests an operational difference between capability claims; it does not establish a metaphysical boundary or intrinsic model learning.

### H-SP-01 — Some apparent spillover survives task-overlap controls

**Hypothesis.** At least some cross-task successes reflect reusable learned structure rather than merely memorized examples, superficial lexical overlap, or benchmark contamination.

**Design.** Construct paired source/target tasks sharing an abstract relation but differing in vocabulary, surface format, and domain. Include lexical-overlap controls, adversarial near matches, contamination audits, and novel held-out combinations. Evaluate both successful and failed transfers.

**Primary measure.** Generalization gap relative to matched superficial-similarity and retrieval baselines.

**Falsifier or narrowing evidence.** The effect vanishes under controlled novelty, disappears when lexical cues are removed, or is explained by benchmark leakage.

**Interpretation boundary.** An observed out-of-domain success is evidence about the evaluated distribution, not a universal claim about capability ceilings.

## 5. Folding, Generalization, and Structural Reuse

### H-FG-01 — A preserved structural core can improve transfer

**Hypothesis.** Explicitly representing a shared relational core improves transfer efficiency and reliability on appropriately matched target domains compared with generic task instructions of equal complexity.

**Design.** Compare (A) direct target solving, (B) generic reasoning instructions, (C) source examples without structure, (D) extracted core alone, and (E) extracted core with target mapping. Match context length and source information. Include false-core controls.

**Primary measure.** Validated target-task performance and cost per successful solution.

**Falsifier or narrowing evidence.** No improvement beyond generic abstraction, or gains only on structurally identical tasks.

### H-FG-02 — Residual preservation reduces negative transfer

**Hypothesis.** Recording source–target mismatches and untransferred constraints reduces harmful overgeneralization compared with applying a folded core alone.

**Design.** Create target tasks with varying degrees of structural mismatch. Compare core-only, core-plus-residual, and no-transfer conditions. Blind evaluators to the hypothesis where possible.

**Primary measure.** Negative-transfer incidence and severity at fixed average cost.

**Falsifier or narrowing evidence.** Residual-aware mapping does not improve outcomes or adds complexity without risk reduction.

**Secondary question.** Does explicit uncertainty preservation outperform later uncertainty recovery through additional evidence, and at what cost? These are competing design options, not a presumed hierarchy.

## 6. Fluidity, Selective Permeability, and Weak Evidence

### H-FL-01 — Selective permeability improves risk-adjusted adaptation

**Hypothesis.** A context-sensitive policy for observing, probing, adopting, and deploying candidate transfers achieves a better utility–risk–cost tradeoff than fully open, fully closed, or static selective policies.

**Design.** Compare four permission policies using the same candidate pool and budgets. Separate exploration authorization from claim validation and deployment authorization. Include distribution shift and misleading analogies.

**Primary measure.** Preregistered risk-adjusted utility, accompanied by raw utility, negative-transfer rate, and unauthorized-action count.

**Falsifier or narrowing evidence.** Adaptive gating performs no better than the strongest static baseline or systematically overfits prior task contexts.

**Safety constraint.** Experimental exploration MUST NOT bypass explicit deployment permissions.

### H-DI-01 — Directional intuition improves prospect discovery efficiency

**Hypothesis.** Weak-evidence directional scoring identifies more independently validated, nontrivial transfer opportunities per fixed probe budget than random selection or surface-similarity ranking.

**Design.** Construct candidate pools containing true, false, and ambiguous structural analogies. Compare random ranking, lexical similarity, embedding similarity, structure-aware ranking, and directional scoring with explicit residuals. Evaluate on unseen target domains.

**Primary measure.** Validated useful discoveries per 100 probes or per fixed cost budget; report precision at k and missed opportunities.

**Falsifier or narrowing evidence.** No gain over strong similarity baselines, or gains vanish after selection-bias correction.

**Critical caveat.** A directional priority score is **not** a calibrated probability of success unless separately calibrated and validated.

### H-DI-02 — Counterevidence improves later opportunity selection

**Hypothesis.** Preserving failed transfer attempts and reasons for failure improves later prospect ranking compared with retaining only successful precedents.

**Design.** Randomize future prospecting episodes to (A) success-only registry, (B) full evidence registry, and (C) no registry, with equal storage and retrieval budgets where possible. Measure unseen prospect selection and calibration.

**Primary measure.** Reduction in avoidable negative transfers and improved validated discoveries per budget.

**Falsifier or narrowing evidence.** Full counterevidence adds no benefit or creates persistent over-conservatism that reduces net utility.

## 7. Transfer and Structural Relay

### H-TR-01 — Explicit mappings improve robustness under domain shift

**Hypothesis.** Transfer packages that state preserved relations, required adaptations, and unresolved residuals remain more useful under target-domain shift than unstructured source examples or direct prompting.

**Design.** Evaluate structurally related domains at increasing mismatch levels. Compare explicit mapping with direct prompting, retrieval, and generic analogy instructions. Keep source exposure and budgets comparable.

**Primary measure.** Out-of-domain success, degradation slope under shift, and negative-transfer severity.

**Falsifier or narrowing evidence.** Explicit mappings do not outperform matched baselines or collapse under modest mismatch.

### H-TR-02 — Provenance-aware relay improves downstream reuse

**Hypothesis.** Relay units carrying scope, evidence, counterevidence, and provenance support more reliable downstream adoption than identical candidate structures stripped of those fields.

**Design.** Send packages to independent agents or teams under blinded conditions: complete, partial, and bare-claim relay. Measure correct interpretation, reproducibility, justified rejection, and false adoption.

**Primary measure.** Reproduced utility and reduction in unsupported adoption, net of documentation overhead.

**Falsifier or narrowing evidence.** Full packages do not improve reproducibility or impose costs exceeding the measured benefit.

**Interpretation boundary.** Successful transmission is not equivalent to correct interpretation, adoption, utility, or durable growth.

## 8. System-Centric and Multi-Level Learning

### H-ML-01 — Frozen execution units can support durable system learning

**Hypothesis.** A system with frozen execution-unit parameters can improve on later unseen tasks through learned routing, structural memory, verification policies, or relay organization.

**Design.** Use identical frozen worker units across (A) single-unit baseline, (B) static orchestration, (C) history retrieval, (D) adaptive routing, and (E) adaptive routing plus structured evidence memory. Hold out future task families and audit all updates.

**Primary measure.** Post-update performance on unseen tasks, retention after delay, and resource-normalized gain.

**Falsifier or narrowing evidence.** Improvements disappear when task exposure, retrieval budget, and orchestration complexity are controlled, or fail to persist on unseen tasks.

### H-ML-02 — Attribution audits can isolate structural learning

**Hypothesis.** A substantial portion of measured improvement, when present, can be causally attributed to system-level state updates rather than covert changes to workers, tools, prompts, or evaluation criteria.

**Design.** Hash or otherwise verify worker versions, freeze tool interfaces, log policy updates, and use counterfactual replay or component ablation. Compare updated and reverted structural states on identical held-out tasks.

**Primary measure.** Difference attributable to structural-state intervention with confidence intervals.

**Falsifier or narrowing evidence.** Gains cannot be isolated from hidden adaptation, task contamination, or evaluation drift.

**Interpretation boundary.** System learning is not evidence of intrinsic model-weight learning, and neither is sufficient to establish AGI.

## 9. Recursive Relay, Repetition, and Growth

### H-RG-01 — Recursive evidence relay improves future exploration

**Hypothesis.** Prospecting systems that use validated outcomes and counterevidence from earlier cycles discover useful new capabilities more efficiently than independent one-shot search under the same cumulative budget.

**Design.** Compare independent prospecting, success-only feedback, full evidence feedback, and full evidence plus structural-policy updates over multiple rounds. Use fresh held-out task pools for final evaluation.

**Primary measure.** Slope of validated discoveries per cumulative budget, along with held-out performance and regression frequency.

**Falsifier or narrowing evidence.** Improvements reflect only larger cumulative search, duplicate tasks, or memorization; no persistent advantage remains under matched-budget testing.

### H-RG-02 — Repetition is useful only with a learning channel

**Hypothesis.** Repeated executions improve future capability only when their observations are captured, evaluated, and incorporated into a reusable system state.

**Design.** Compare (A) repeated execution without retention, (B) raw-log retention, (C) structured evidence aggregation, and (D) structured evidence plus adaptive policy updates. Use identical numbers of trials.

**Primary measure.** Generalization to later unseen tasks and improvement in decision quality.

**Falsifier or narrowing evidence.** Repetition alone matches structured relay, or structured relay produces no transferable improvement.

**Nuance.** Repetition can still constitute **data accumulation relay** even when it does not yet cause measurable growth. Record this as an intermediate outcome, not a success claim.

## 10. Evaluation Governance and AGI Boundaries

### H-EV-01 — Separate exploration and claim gates reduce false claims

**Hypothesis.** Explicit Gate A (permission to explore) and Gate B (evidence-based scoped claim) reduce false capability assertions compared with a single undifferentiated approval process, without unacceptable loss of useful discovery.

**Design.** Present evaluators with mixed-quality opportunity and evidence packages. Randomize review workflows. Include deliberately misleading high-priority candidates and cases with partial replication.

**Primary measure.** False-positive claim rate and time/cost per justified claim; secondary measure is false-negative rejection of valid prospects.

**Falsifier or narrowing evidence.** No reduction in unsupported claims or excessive suppression of legitimate research opportunities.

### H-AGI-01 — Generality claims must survive increasingly broad held-out tests

**Hypothesis under examination.** Structural transfer, relay, and adaptive boundaries may expand the breadth of tasks a composed system can solve, but the degree and persistence of that expansion are empirical questions.

**Design.** Evaluate on independently selected task families with new constraints, unseen tools, varied resource ceilings, and delayed follow-up. Compare model-centric, static-system, adaptive-system, and hybrid variants. Audit whether gains depend on external human intervention or specialized tools.

**Primary measure.** Breadth of independently validated capabilities at fixed resource ceilings, robustness under shift, and persistence of system learning.

**Falsifier or narrowing evidence.** Improvements concentrate in narrow families, disappear under transfer, or rely on unaccounted resources. Such outcomes should narrow claims about generality.

**Interpretation boundary.** No finite benchmark suite establishes unrestricted general intelligence. Open-ended exploration, recursive relay, and open-ended growth are different propositions.

## 11. Recommended Cross-Hypothesis Experiments

### Experiment A — Shared-Core Transfer Matrix

Cross source and target domains with structural similarity, superficial similarity, and residual mismatch varied independently. Test H-SP-01, H-FG-01, H-FG-02, and H-TR-01. This design helps separate genuine relational transfer from surface pattern matching.

### Experiment B — Prospecting Budget Challenge

Provide all methods with identical candidate pools and fixed probe budgets. Compare random, embedding, structural, and weak-evidence directional ranking. Repeat with and without counterevidence. Test H-DI-01 and H-DI-02. Publish all candidate selections, including failures, to reduce winner's-curse bias.

### Experiment C — Frozen-Unit Collective Learning Laboratory

Use three to five fixed workers and a replaceable structural controller. Measure static coordination, adaptive routing, evidence retention, and long-horizon learning under identical budgets. Test H-BND-01, H-ML-01, H-ML-02, H-RG-01, and H-RG-02.

### Experiment D — Relay Package Reproduction Challenge

Give independent teams complete versus incomplete evidence-bearing relay packages. Score replication, correct rejection, semantic fidelity, and cost. Test H-TR-02 and H-EV-01.

### Experiment E — Boundary Policy Stress Test

Inject distribution shifts, adversarial analogies, misleading weak evidence, and permission-sensitive operations. Compare open, closed, static selective, and adaptive selective permeability. Test H-FL-01 and H-EV-01. Ensure all risky actions remain sandboxed or simulated.

### Experiment F — Longitudinal Capability Frontier Audit

Track observed and reachable capability profiles over multiple cycles with independent holdout tasks and resource accounting. Test H-BND-01, H-RG-01, and H-AGI-01. Record both expansions and contractions of supported claims.

## 12. Minimal Machine-Readable Hypothesis Record

The following YAML is illustrative, not a finalized schema. The canonical contracts in `specs/` govern authoritative field definitions and validation behavior.

```yaml
hypothesis_id: H-DI-01
version: 1.0.0
status: proposed
claim: >
  Directional weak-evidence ranking increases independently validated
  useful transfer discoveries per fixed probe budget.
scope:
  source_domains: [software_planning]
  target_domains: [service_scheduling]
  system: frozen_model_plus_prospecting_controller
  budget:
    max_probes: 100
    max_total_compute: declared_before_trial
intervention: directional_scoring_with_explicit_residuals
baselines:
  - random_selection
  - lexical_similarity
  - embedding_similarity
  - structural_similarity
primary_outcome: validated_useful_discoveries_per_100_probes
secondary_outcomes:
  - negative_transfer_rate
  - cost_per_validated_discovery
  - precision_at_k
pre_registration: required_for_confirmatory_claim
counterevidence:
  - no_improvement_over_strongest_budget_matched_baseline
  - effect_disappears_on_unseen_target_domains
provenance:
  data_split_manifest: pending
  model_and_tool_versions: pending
  evaluator_protocol: pending
claim_gate: not_evaluated
relay_status: hypothesis_only
```

An experiment result SHOULD additionally include a stable experiment ID, registered protocol hash, execution environment, data provenance, uncertainty estimates, deviations from the protocol, negative results, and links to independently reproducible artifacts. Do not infer a calibrated success probability from an ordinal ranking score.

## 13. Claim-State and Evidence Discipline

Use the following progression as a conceptual guide; refer to [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md), [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md), and [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md) for the actual contracts:

| State | Evidence expectation | Allowed interpretation |
|---|---|---|
| Proposed | Mechanism and falsifier articulated | Research hypothesis |
| Exploratory | Initial probes with disclosed selection | Candidate finding, not confirmation |
| Supported in scope | Preregistered result and appropriate controls | Scoped empirical support |
| Replicated in scope | Independent repetition under documented conditions | Stronger scoped support |
| Contested | Contradictory or limiting evidence | Unresolved; scope requires review |
| Retracted or narrowed | Failed checks or revised interpretation | Historical record retained |

No hypothesis should be promoted because of narrative appeal, number of experiments attempted, or success on a single cherry-picked example. Governance and deployment permission are separate from research claim status.

## 14. Priorities and Dependencies

**Foundational first:** H-BND-01, H-SP-01, H-FG-01, H-ML-01, and H-EV-01 establish measurement validity, leakage controls, structural transfer baselines, and claim discipline.

**Near-term mechanisms:** H-FG-02, H-FL-01, H-DI-01, H-DI-02, H-TR-01, and H-TR-02 test whether residuals, weak evidence, adaptive boundaries, and evidence-rich relay improve outcomes.

**Longitudinal and higher-order:** H-ML-02, H-RG-01, H-RG-02, and H-AGI-01 require longer observation windows, audited state changes, and broader independent testing.

These priorities are pragmatic and may change as counterevidence accumulates. They are not estimates of the probability that each hypothesis is true.

## 15. How to Report a Negative or Mixed Result

A useful negative-result report SHOULD answer: Which exact claim was tested? Which baseline was strongest? Was the test adequately powered? Did the intervention fail outright, or only under particular residual mismatch, task shift, budget, or policy conditions? What was learned about the boundary of applicability? What reusable experiment protocol, counterexample, or residual question can be relayed?

Mixed results should be disaggregated by prespecified task families and difficulty strata where possible. Do not suppress a harmful transfer because other tasks improved. Do not interpret a null result as universal impossibility. Update the hypothesis version and preserve the original wording and evidence lineage.

## 16. Interfaces to the ISGFTR Repository

- **Theory:** [ISGFTR-001](docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md), [ISGFTR-002](docs/ISGFTR-002-Five-Characteristics-of-Intelligence-Spillover-and-Relay.md), [ISGFTR-003](docs/ISGFTR-003-Folding-Generalization-Duality-and-Structural-Reuse.md), [ISGFTR-004](docs/ISGFTR-004-Intelligence-Fluidity-and-Permeable-Structural-Boundaries.md), [ISGFTR-005](docs/ISGFTR-005-Directional-Intuition-and-Weak-Evidence-Transfer.md).
- **System learning and growth:** [ISGFTR-006](docs/ISGFTR-006-System-Centric-Intelligence-and-Multi-Level-Learning.md), [ISGFTR-007](docs/ISGFTR-007-Recursive-Relay-and-Open-System-Intelligence-Growth.md), [ISGFTR-008](docs/ISGFTR-008-Intelligence-Spillover-and-Transfer-Prospecting.md), [ISGFTR-009](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md), [ISGFTR-010](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md).
- **Contracts:** [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md), [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md), [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md), [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md).
- **Illustrative studies:** [CASE-001](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md), [CASE-002](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md), [CASE-003](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md).
- **Extensions:** [EXT-001](extensions/EXT-001-Biomimetic-Fluidity-and-Selective-Permeability.md), [EXT-002](extensions/EXT-002-Learning-the-Boundaries-of-Intelligence-Flow.md), [EXT-003](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md).
- **Research agenda:** [OPEN-QUESTIONS.md](OPEN-QUESTIONS.md), [FUTURE-DIRECTIONS.md](FUTURE-DIRECTIONS.md), and [VALIDATION-ROADMAP.md](VALIDATION-ROADMAP.md) (planned).

## 17. Open Collaboration and Closing Principle

The strongest contribution to ISGFTR may be a clean counterexample, a better-matched baseline, a clarified definition, or a reproducible failure—not necessarily a positive demonstration. Researchers are encouraged to publish protocol details, data partition logic, cost accounting, evidence lineage, and explicit limitations so that findings can be examined and relayed without overstating their implications.

**Discover possibilities broadly; validate claims narrowly; preserve counterevidence; attribute learning correctly; and treat AGI implications as questions to investigate rather than conclusions to announce.**

---

*Document status: Proposed, falsifiable research agenda. No experiments or empirical outcomes are asserted in this document.*
