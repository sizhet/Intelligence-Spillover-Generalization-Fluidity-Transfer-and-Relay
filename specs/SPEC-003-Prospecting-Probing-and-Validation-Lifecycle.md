# SPEC-003 — Prospecting, Probing, and Validation Lifecycle

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Proposed interoperable research lifecycle specification  
**Version:** v1.0.0 (theory-first)  
**Status:** Draft research contract; not an adopted standard or empirically validated implementation  
**Date:** 2026-10-30

## Abstract

This specification proposes an auditable lifecycle for investigating suspected intelligence spillover, generalization, fluidity, and transfer. It converts an unverified **Spillover Opportunity Record (SOR)** into a bounded sequence of prospecting, protocol registration, probe authorization, execution, evaluation, claim adjudication, and evidence relay. The central design constraint is that **permission to explore is not permission to claim a capability**. The lifecycle uses two separate gates, explicit state transitions, resource and risk budgets, frozen evaluation criteria, provenance and counterevidence, independent replication, and durable records of unsuccessful probes. It permits adaptive exploration without allowing post hoc changes to silently rewrite what a probe was designed to establish. Its purpose is conformance and scientific accountability, not a guarantee of discovery, transfer, or recursive intelligence growth.

**Keywords:** capability prospecting; probing; preregistration; validation; lifecycle contract; selective permeability; evidence relay; negative transfer; conformance; collective learning.

---

## 1. Scope and Normative Language

This document defines a **research process contract**, not an AI algorithm or empirical claim. A conforming implementation MAY use human researchers, autonomous agents, frozen models, structural intelligence units, or combinations thereof. It MUST make the decision trail inspectable even if the underlying candidate-generation method is proprietary or opaque.

The terms **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** are normative within this *proposed ISGFTR specification* only. They do not imply approval by a standards body.

The specification covers:

- the admission and prioritization of capability prospects;
- controlled registration and execution of tests;
- evaluation against declared acceptance and falsification criteria;
- separation of observation, replication, transfer, and persistent growth;
- preservation of uncertainty, negative evidence, and governance decisions;
- handoff to portable structural relay and collective learning.

It does **not** prescribe a universal measure of intelligence, a universal probability of transfer success, or a pathway that necessarily reaches AGI.

## 2. Dependencies and Contract Boundaries

This document is the process layer of a four-part proposed specification family:

| Contract | Responsibility | Required linkage |
|---|---|---|
| `SPEC-001` | Capability profile, scope, boundary classes, claim state, attribution | Actor, task, operating envelope, boundary and claim identifiers |
| `SPEC-002` | SOR, weak evidence, directional assessment, counterevidence | Opportunity and evidence identifiers, provenance, transfer mapping |
| **`SPEC-003`** | Probe lifecycle, authorization, decisions, transitions, validation | Probe plan, execution events, evaluation and gate decisions |
| `SPEC-004` | Relay packaging, downstream reuse, collective review | Immutable evidence links, recipient context, reuse restrictions |

A lifecycle record MUST reference a versioned SOR. A capability claim resulting from a probe MUST reference a SPEC-001-compatible profile and the specific evaluation evidence. A relay package MUST preserve the lifecycle's decision history, not merely its final status.

## 3. Core Definitions

**Prospect:** A candidate extension or transfer of capability whose success has not yet been established. It is a hypothesis, not an observed result.

**Probe:** A bounded intervention or test designed to discriminate among a prospect's main hypothesis, null hypothesis, and credible alternatives.

**Probe protocol:** A versioned declaration of tasks, conditions, metrics, acceptance thresholds, failure criteria, resource limits, and contamination controls.

**Exploratory result:** An observation useful for generating or refining hypotheses but not automatically eligible to validate a preregistered claim.

**Confirmatory result:** A result evaluated against a previously fixed protocol, with deviations and exclusions disclosed.

**Validation:** A scoped decision that evidence supports a particular capability claim under declared conditions. Validation is not universal generalization.

**Replication:** A new test, independent to a declared degree, that assesses whether a prior result persists under specified comparable or intentionally varied conditions.

**Relay:** Preservation and transfer of an evidence-bearing research object to another execution, actor, context, or time. Relay does not imply successful capability transfer.

**Growth:** Demonstrated, durable improvement attributable to a specified learning or structural change, assessed beyond the data or cases that prompted that change.

## 4. Lifecycle Overview

The proposed lifecycle is:

```text
Discover → Register Prospect → Triage → Gate A
                                       │
                    reject / defer / revise
                                       │ admitted
                                       ▼
                    Design & Register Probe
                                       ▼
                     Authorize & Execute
                                       ▼
                    Preserve Raw Evidence
                                       ▼
                  Evaluate & Challenge Claims
                                       ▼
                         Gate B Decision
                         /      |       \
                 supported  inconclusive  refuted/contested
                         \      |       /
                          Evidence Relay
                                ▼
                     Replicate / Learn / Re-prospect
```

The lifecycle is **recursive but not circularly self-validating**: a result may generate a new prospect, but that new prospect requires its own identifiers, controls, and validation. Retesting the same evidence is not independent replication.

## 5. Canonical Lifecycle Record

Every lifecycle instance MUST include the following fields or semantically equivalent fields in a documented schema.

| Field | Requirement | Meaning |
|---|---|---|
| `lifecycle_id` | MUST | Stable unique identifier |
| `schema_version` | MUST | Contract version used |
| `sor_ref` and `sor_version` | MUST | Source opportunity record |
| `capability_profile_ref` | MUST | Source or target capability profile |
| `actor` and `owner` | MUST | Executing entity and accountable reviewer |
| `current_state` | MUST | Lifecycle state from Section 6 |
| `event_log` | MUST | Append-only transition and decision history |
| `gate_a_decision` | MUST before probe | Exploration admission and conditions |
| `probe_protocol_ref` | MUST before execution | Versioned protocol |
| `execution_refs` | MUST after execution | Run records and raw evidence references |
| `evaluation_ref` | MUST for Gate B | Analysis, metrics, deviations, counterevidence |
| `gate_b_decision` | MUST for claim promotion | Scoped validation outcome |
| `resource_budget` | MUST | Time, compute, data, money or equivalent constraints |
| `risk_controls` | MUST | Privacy, safety, security, and authorization controls |
| `provenance` | MUST | Origin, timestamps, hashes or integrity mechanism |
| `next_actions` | SHOULD | Replication, revision, relay or closure |

Null or absent later-stage fields are permitted only while the lifecycle has not reached the stage requiring them. A missing field MUST NOT be silently interpreted as a passed check.

## 6. State Machine and Permitted Transitions

### 6.1 States

| State | Meaning |
|---|---|
| `proposed` | Prospect registered but not triaged |
| `triaged` | Feasibility, novelty, evidence and risk reviewed |
| `deferred` | Not currently admitted; rationale preserved |
| `rejected` | Gate A failed or authorization denied |
| `admitted` | Gate A passed; probe planning allowed |
| `protocol_registered` | Test and criteria fixed at a specific version |
| `authorized` | Resources, permissions and risk controls approved |
| `running` | Probe executing |
| `interrupted` | Execution paused or aborted, partial data preserved |
| `evidence_locked` | Evidence package sealed for evaluation |
| `under_review` | Evaluation and counterevidence analysis underway |
| `inconclusive` | Evidence does not support decisive scoped judgment |
| `unsupported` | Tested claim not supported under declared conditions |
| `supported_scoped` | Gate B supports a specific limited claim |
| `contested` | Material challenge or contradictory evidence pending |
| `replication_pending` | Additional independent evaluation requested |
| `closed` | Current lifecycle concluded; record remains accessible |

`unsupported` is not a metaphysical proof that a capability can never exist. Likewise `supported_scoped` does not mean broadly general, permanent, or AGI-level capability.

### 6.2 Transition constraints

A conforming process MUST enforce the following logical ordering:

1. `proposed → triaged` after initial record completeness checks.
2. `triaged → admitted | deferred | rejected` through Gate A.
3. `admitted → protocol_registered` after protocol registration.
4. `protocol_registered → authorized` only after risk, permissions, and budget checks.
5. `authorized → running → evidence_locked` for completed probes; `running → interrupted` is allowed with reasons.
6. `evidence_locked → under_review → supported_scoped | unsupported | inconclusive | contested` through Gate B.
7. Any reviewed outcome MAY transition to `replication_pending` or `closed`, without deleting prior outcomes.

A new or materially changed protocol MUST create a new protocol version and, when necessary, a new probe instance. A contested decision MUST remain traceable even after a later adjudication supersedes it. An interrupted probe MUST NOT be presented as a completed confirmatory test.

## 7. Gate A — Exploration Admissibility

Gate A asks **whether a prospect merits a bounded test**, not whether it is true. It MUST assess:

1. **Question clarity:** Can a falsifiable task-level hypothesis be written?
2. **Evidence traceability:** What observations, analogies, or residuals motivate the prospect?
3. **Directional plausibility:** Is there a coherent, if tentative, transfer mechanism?
4. **Discrimination:** Can a probe distinguish success from trivial or alternative explanations?
5. **Resource feasibility:** Is the experiment within an explicit budget?
6. **Risk acceptability:** Are data rights, privacy, security, and safety controls sufficient?
7. **Information value:** Would either success or failure meaningfully update knowledge?

The decision MUST be `admit`, `defer`, or `reject`, with reviewer identity, rationale, constraints, and timestamp. A high directional score MAY influence ranking but MUST NOT override risk controls or count as empirical proof. If scoring is heuristic, it MUST be labeled heuristic; a numerical score MUST NOT be called a success probability without calibration evidence.

**Selective permeability:** Gate A SHOULD permit inexpensive, reversible, informative exploration under uncertainty while restricting hazardous or irreversible actions. Admissibility can be conditional, for example allowing a sandbox-only test but prohibiting deployment.

## 8. Probe Protocol Registration

A confirmatory probe MUST have a versioned protocol fixed before the confirmatory run. At minimum, it MUST specify:

- **Hypothesis and null:** the predicted extension and an appropriate no-transfer or baseline explanation;
- **Actor composition:** frozen versus trainable units, tools, memories, routing and external services;
- **Source and target tasks:** task distributions, inclusion/exclusion criteria and held-out conditions;
- **Baselines:** no-transfer, random/naive transfer, matched-resource and relevant strong baselines;
- **Metrics:** primary outcome, secondary outcomes, error severity, cost and latency;
- **Thresholds:** success criteria, failure criteria, uncertainty intervals and practical significance;
- **Sampling plan:** sample sizes or stopping rules, randomization, seeds and repeated trials;
- **Leakage controls:** test-set separation, prompt contamination, tool-output contamination and retrospective tuning;
- **Resource limits:** compute, time, calls, data exposure and other material costs;
- **Safety controls:** allowed operations, approval requirements and abort triggers;
- **Attribution tests:** which layer changed—unit weights, tool access, routing, memory, structural composition or evaluation;
- **Analysis plan:** handling of missing data, multiple comparisons and protocol deviations.

Exploratory experiments MAY use adaptive criteria, but their results MUST be labeled exploratory. If exploration generates a revised hypothesis, confirmatory evaluation SHOULD use new held-out evidence rather than reclassifying the exploratory data as preregistered confirmation.

## 9. Probe Authorization and Execution

Execution MUST begin only after the protocol and authorization records are linked. Every run MUST record a unique run identifier, protocol version, configuration, actor composition, environment, input set reference, resource usage, outputs, error events, and provenance.

A conforming implementation MUST:

- enforce approved resource and safety limits;
- preserve failures, timeouts and partial runs rather than reporting only successful attempts;
- record changes in tools, model versions, prompts, memory, datasets and routing;
- separate test data from prospect-generation and model-selection data where required;
- record human intervention and post hoc repairs;
- flag environmental drift and unanticipated dependencies;
- halt or escalate when declared abort criteria are met.

Execution logs SHOULD be tamper-evident where practical. A cryptographic hash is one possible integrity mechanism, not a substitute for correct experimental design.

## 10. Evidence Locking and Evaluation

Before Gate B, the evaluation MUST reference a fixed set of evidence artifacts or a declared reproducible query over a versioned dataset. Evidence records SHOULD include raw outcomes, summary statistics, negative cases, resource costs, protocol deviations, and uncertainty estimates.

Evaluation MUST address at least five questions:

1. **Task success:** Did the actor meet the predeclared operational criterion?
2. **Comparison:** Did it outperform a fair baseline under comparable conditions?
3. **Attribution:** Was any gain caused by model adaptation, added tools, structural routing, memorization, human assistance or other changes?
4. **Robustness:** Does the result persist across seeds, perturbations and relevant held-out conditions?
5. **Counterevidence:** What failures, contradictory observations or alternative explanations remain?

Evidence strength MUST be represented independently of opportunity priority. A large exploratory ranking score cannot compensate for weak validation evidence. A null result MAY be valuable as evidence that narrows a prospect or reveals an invalid transfer assumption.

## 11. Gate B — Scoped Claim Adjudication

Gate B asks **what, if anything, the evidence permits us to claim**. Its decisions MUST include:

- `supported_scoped`: stated criterion met under a specified evaluation envelope;
- `unsupported`: criterion not met or credible evidence contradicts it;
- `inconclusive`: insufficient power, ambiguous results or unresolved methodological issues;
- `contested`: material dispute or contradictory evidence requiring adjudication.

For `supported_scoped`, the decision MUST identify the exact task, actor configuration, resource conditions, metrics, thresholds, evidence references, known exclusions, and uncertainty. It MUST NOT imply generalization to untested domains or independence from tools if those were not demonstrated.

A claim may be promoted in the SPEC-001 capability profile to `observed` only with qualifying evidence. A transition to `replicated` requires separately identified replication evidence and a declared independence criterion. `supported_scoped` is a lifecycle decision, whereas `observed` and `replicated` are capability claim states; implementations MUST NOT conflate the two.

An outcome MAY be challenged or retracted later. The previous decision and reasons for revision MUST remain discoverable.

## 12. Three Distinct Validation Targets

### 12.1 Capability extension

A system performs a target task previously unobserved or not demonstrated under a declared configuration. This supports a *scoped capability observation*, not necessarily learning or generalization.

### 12.2 Transfer benefit

A reused structure or prior experience improves target-task performance relative to appropriate controls, accounting for extra resources and tuning. The evaluation SHOULD include negative transfer and out-of-distribution cases.

### 12.3 Durable growth

A system retains a useful change and demonstrates benefit on future, sufficiently independent tasks or time-separated trials. Evidence MUST identify the persistence mechanism and rule out merely replaying the same examples. A one-off successful composition does not establish durable growth.

These targets MAY co-occur, but each requires its own operational evidence. **Mobility ≠ Utility ≠ Growth.**

## 13. Recursive Prospecting and Temporal Relay

The lifecycle MAY feed outcomes into a new round of prospecting:

`Prospect → Probe → Validate → Relay → Learn → Prospect`.

The learning stage MAY update a directional prior, precedent registry, structural map, routing policy, memory, or research portfolio without changing model weights. The record MUST distinguish which component changed and which remained frozen.

Repeated execution can constitute **evidence relay** when each run contributes traceable observations, uncertainty reduction, failure modes, or context variation. Mere repetition without retained information, feedback, or measurable improvement MUST NOT be labeled learning. Reusing the same run under multiple labels MUST NOT count as independent evidence.

The process SHOULD retain explicit residuals: unanswered questions, unresolved OTHERS mappings, failed assumptions, unexplained discrepancies, and potential alternative transfer routes.

## 14. Independent Replication and Cross-Context Transfer

A replication plan SHOULD specify the intended independence dimensions: evaluator, operator, dataset, environment, implementation, institution, and time. These dimensions are not interchangeable. A second run with the same hidden leakage may reproduce an artifact rather than a capability.

A cross-context transfer claim MUST declare which conditions changed and which remained fixed. Transfer across domains, modalities, tools, or actor compositions SHOULD be evaluated separately rather than merged into a single undifferentiated success score.

Replication outcomes MUST be able to weaken, qualify, or overturn earlier conclusions. Contradictory evidence SHOULD trigger a review of confounds, rather than automatic suppression of either result.

## 15. Governance, Safety, and Stop Conditions

The process MUST support interruption, rejection, escalation and retrospective audit. A gate decision SHOULD identify an accountable reviewer or policy authority. For autonomous systems, the accountable authority MAY be a human-approved policy and escalation workflow; the system MUST NOT treat self-generated approval as sufficient when external authorization is required.

Stop conditions SHOULD include unauthorized access, privacy leakage, dangerous action requests, unexpected tool privileges, unacceptable external effects, budget exhaustion, and irrecoverable evidence contamination. Safe sandbox testing SHOULD be preferred for unverified transfer mechanisms.

The governance record MUST distinguish **permission to experiment**, **permission to publish a claim**, and **permission to deploy a capability**. Gate B validates a research claim; it does not by itself authorize real-world deployment.

## 16. Illustrative YAML Lifecycle Record

The following example is schematic. Identifiers, thresholds, and results are illustrative, not empirical findings.

```yaml
schema: isgftr.spec-003.lifecycle.v1
lifecycle_id: LC-EXAMPLE-001
schema_version: 1.0.0
sor_ref: SOR-EXAMPLE-001
sor_version: 1
capability_profile_ref: CAP-EXAMPLE-001
actor:
  system_id: frozen-llm-plus-verifier
  model_weights_changed: false
  external_tools: [structured_parser, deterministic_verifier]
owner: research-team-example
current_state: under_review
resource_budget:
  max_probe_runs: 200
  max_compute_hours: 8
risk_controls:
  sandbox_only: true
  external_actions_allowed: false
gate_a_decision:
  outcome: admit
  rationale: bounded and discriminating synthetic test
  reviewer: reviewer-A
  decided_at: 2026-10-30T09:00:00Z
probe_protocol_ref:
  id: PROTO-EXAMPLE-001
  version: 1
  preregistered: true
  hypothesis: structural verification improves held-out accuracy
  null_hypothesis: no improvement over matched-resource baseline
  primary_metric: held_out_exact_accuracy
  acceptance_rule: > baseline with prespecified uncertainty criterion
  held_out_dataset_ref: DATA-EXAMPLE-HOLDOUT-001
  baseline_ref: BASE-EXAMPLE-001
  stop_rule: 200 runs or budget limit
execution_refs: [RUN-EXAMPLE-001, RUN-EXAMPLE-002]
evaluation_ref: EVAL-EXAMPLE-001
gate_b_decision: null
provenance:
  created_at: 2026-10-30T08:00:00Z
  evidence_bundle_ref: EB-EXAMPLE-001
event_log:
  - state: proposed
    at: 2026-10-30T08:00:00Z
  - state: admitted
    at: 2026-10-30T09:00:00Z
  - state: protocol_registered
    at: 2026-10-30T10:00:00Z
  - state: authorized
    at: 2026-10-30T10:30:00Z
  - state: running
    at: 2026-10-30T11:00:00Z
  - state: evidence_locked
    at: 2026-10-30T12:00:00Z
  - state: under_review
    at: 2026-10-30T12:15:00Z
next_actions: [independent_review, check_negative_transfer]
```

An implementation SHOULD use machine-readable timestamps, explicit data types, and schema validation. The illustrative YAML does not itself constitute a finalized JSON Schema or reference implementation.

## 17. Contract Invariants

**INV-001 — Prospect separation.** A registered opportunity MUST NOT be reported as an observed capability without qualifying evidence.

**INV-002 — Two-gate separation.** Gate A admission MUST NOT be interpreted as Gate B validation.

**INV-003 — Traceability.** Every probe MUST link to a versioned SOR, capability profile and protocol.

**INV-004 — Authorization.** No probe may enter `running` without an authorized protocol and declared resource/risk controls.

**INV-005 — Protocol integrity.** Material post hoc changes MUST be versioned and disclosed.

**INV-006 — Evidence retention.** Failures, aborted runs, counterevidence and negative transfer MUST NOT be selectively deleted from the decision trail.

**INV-007 — Scoped claims.** A successful probe MUST produce only claims supported within the tested envelope.

**INV-008 — Attribution.** Changes in model weights, tools, memory, routing and structural composition MUST be distinguishable.

**INV-009 — Calibration honesty.** Heuristic priority scores MUST NOT be presented as calibrated success probabilities.

**INV-010 — Replication integrity.** Repeated evaluation of the same evidence MUST NOT be counted as independent replication.

**INV-011 — Revision history.** Contested or retracted claims MUST retain earlier versions and reasons for change.

**INV-012 — Deployment separation.** Research validation MUST NOT automatically confer deployment authorization.

**INV-013 — Durable-growth evidence.** Growth claims MUST include retention or future-task evidence, not merely a single successful execution.

**INV-014 — Relay completeness.** Relay of a conclusion MUST include evidence references, limitations and unresolved residuals.

## 18. Illustrative Conformance Tests

A future validator SHOULD support at least the following tests:

| Test | Input condition | Expected outcome |
|---|---|---|
| CT-001 | SOR missing | Reject lifecycle record |
| CT-002 | `running` without authorization | Reject transition |
| CT-003 | Gate A admitted, no probe result | Forbid capability promotion |
| CT-004 | Protocol threshold changed after results | Require version and deviation flag |
| CT-005 | Only successful runs retained | Fail evidence completeness review |
| CT-006 | Priority score called probability without calibration | Flag invalid claim |
| CT-007 | Model frozen, external verifier added | Attribute outcome to composite system |
| CT-008 | One-off success called durable growth | Reject growth promotion |
| CT-009 | Same dataset reused as independent replication | Reject replication independence claim |
| CT-010 | Null result and negative transfer recorded | Accept as valid research outcome |
| CT-011 | `supported_scoped` without evaluation envelope | Reject Gate B decision |
| CT-012 | `contested` claim silently overwritten | Reject audit history |
| CT-013 | Risk stop triggered, execution continues | Flag governance violation |
| CT-014 | Relay omits counterevidence references | Fail relay readiness |
| CT-015 | Exploration data relabeled confirmatory post hoc | Flag preregistration violation |
| CT-016 | Unsupported result interpreted as universal impossibility | Flag overgeneralized conclusion |

These are proposed test cases, not claims that a validator already exists.

## 19. Minimal Research MVP and Evaluation Plan

A minimal implementation can use a small prospect registry, frozen execution units, a deterministic evaluator, and a versioned event log. Three conditions can be compared:

1. **Unstructured exploration:** probes chosen informally, without registered gates or standardized evidence records.
2. **Structured lifecycle:** identical probe budget with preregistered criteria, Gate A/B separation and complete evidence retention.
3. **Structured lifecycle with relay:** condition 2 plus reuse of positive and negative evidence in later prospect selection.

Primary outcomes SHOULD include false claim-promotion rate, reproducibility, evidence completeness, negative-transfer detection, and cost per validated prospect. Secondary outcomes MAY include discovery yield, time to decision, and number of genuinely novel transferable structures. Independent evaluators SHOULD assess whether structured governance improves reliability without suppressing useful exploratory diversity.

This MVP is intended to test the *research process*, not to demonstrate AGI or open-ended recursive self-improvement.

## 20. Open Questions and Falsification Opportunities

1. Does strict preregistration improve reliability enough to offset its coordination cost in rapidly changing AI research?
2. Which types of exploratory adaptation can remain valid without a wholly new confirmatory dataset?
3. Can directional prospect scores be calibrated across domains, or are they necessarily local and context-dependent?
4. How should independent replication be defined for systems sharing foundation models, training corpora or tools?
5. When does persistent structural memory constitute learning rather than retrieval or benchmark-specific caching?
6. Can negative evidence relay reduce wasted probes without systematically excluding rare breakthroughs?
7. What minimum evidence is sufficient to distinguish a transferable mechanism from accidental correlation?
8. How should governance adapt when a safe sandbox prospect becomes risky in deployment?

A central falsification opportunity is straightforward: if the structured lifecycle does not improve the reliability or information efficiency of capability research under fair matched-budget comparisons, its claimed practical value should be narrowed or revised.

## 21. Figure and Research Interfaces

**Primary figure:** `figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png`, near Sections 4–7, to show prospect selection, boundary hypotheses and validation gates.

**Supporting figure:** `figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png`, near Sections 13–14, to show recursive learning and evidence relay across time and actors.

**Related research:** ISGFTR-005 (weak-evidence directional intuition), ISGFTR-006 (multi-level learning), ISGFTR-007 (recursive relay), ISGFTR-008 (capability prospecting), ISGFTR-009 (limits and counterarguments), and ISGFTR-010 (open research architecture).

**Next contract:** `SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md` should specify how the lifecycle's evidence, decisions, revisions, counterevidence and residuals travel across actors and contexts without losing their meaning.

## 22. Conclusion

A credible capability-prospecting system needs more than a mechanism for proposing promising transfers. It needs a disciplined way to decide which prospects may be explored, how they are tested, what their evidence actually supports, and how both successes and failures can be reused. This proposed lifecycle separates **exploration permission**, **scoped scientific validation**, and **deployment authorization**. It supports recursive research and collective learning while preserving uncertainty, counterevidence, accountability, and the possibility that an attractive hypothesis is wrong.

**Document status:** Open, theory-first specification offered for critique, refinement, independent conformance tooling and empirical evaluation. No claim of established AGI capability or validated implementation is made.
