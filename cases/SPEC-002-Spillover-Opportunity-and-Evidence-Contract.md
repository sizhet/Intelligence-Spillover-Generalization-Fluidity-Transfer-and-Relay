# SPEC-002 — Spillover Opportunity and Evidence Contract

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Proposed interoperable research specification  
**Version:** v1.0.0 (theory-first)  
**Status:** Draft research contract; not an adopted standard or validated implementation  
**Date:** 2026-10-30

## Abstract

This specification defines a portable, auditable way to represent a *possible* intelligence spillover or cross-domain transfer before the underlying capability has been established. It separates an opportunity hypothesis from the evidence used to prioritize exploration, the evidence produced by probes, and the evidence required to support a capability claim. It introduces a canonical **Spillover Opportunity Record (SOR)**, **Evidence Item**, **Evidence Bundle**, **Directional Assessment**, and **Counterevidence Register**. These records support exact and approximate structural correspondences, weak signals, OTHERS residuals, alternative explanations, negative transfer, selective permeability, and evidence relay. Conformance means that an opportunity can be traced, challenged, revised, and independently tested—not that the opportunity is genuine or its score predicts success. This contract complements SPEC-001 and prepares the lifecycle and relay contracts in SPEC-003 and SPEC-004.

**Keywords:** capability prospecting; intelligence spillover; transfer; weak evidence; directional intuition; provenance; counterevidence; research contracts; structural relay; falsifiability.

---

## 1. Scope, Status, and Normative Vocabulary

This document specifies the **representation of a research opportunity and its evidence**. It does not require any particular model architecture, vector embedding, metric space, statistical estimator, or AI agent. Its intended users include researchers, autonomous prospecting systems, evaluators, and collaborative relay networks.

The words **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** are normative only for implementations or documents claiming conformance to this *proposed ISGFTR contract*. They do not describe an externally ratified standard.

This specification is deliberately agnostic about whether a proposed transfer is eventually successful. It supports opportunities that are disproved, inconclusive, harmful, or no longer worth investigating. A conforming system MUST preserve the distinction among:

1. **Opportunity:** a candidate hypothesis about an unverified capability extension.
2. **Signal:** an observation or analogy motivating investigation.
3. **Probe result:** a result obtained under a declared test protocol.
4. **Capability evidence:** an observation that meets a defined task and evaluation contract.
5. **Growth evidence:** a demonstrated persistent improvement under specified retention and transfer tests.

A score assigned to an opportunity MUST NOT be represented as an empirical success probability unless an explicit calibration procedure and its validation evidence are supplied.

## 2. Relationship to the ISGFTR Research Architecture

The conceptual sequence is:

`Capability profile → opportunity hypothesis → directional assessment → bounded probe → evidence review → claim update → structural relay`.

- **SPEC-001** defines the capability profile, boundary classes, claim states, provenance, and attribution requirements.
- **SPEC-002** defines opportunity hypotheses and evidence semantics (this document).
- **SPEC-003** will define state transitions, probe authorization, evaluation, and validation gates.
- **SPEC-004** will define portable relay units, collective review, and evidence reuse.

The related research papers are ISGFTR-003 (structural reuse), ISGFTR-004 (selective permeability), ISGFTR-005 (directional intuition), ISGFTR-007 (recursive relay), and ISGFTR-008 (capability prospecting).

**Design principle:** *An opportunity is a question, not an answer.*

## 3. Conceptual Definitions

### 3.1 Spillover Opportunity

A **spillover opportunity** is a scoped hypothesis that an actor's known or suspected capabilities could support a task, domain, representation, or organizational configuration beyond the evidence that originally established them. The opportunity may involve:

- **Within-actor spillover:** a model performs outside its original evaluation domain.
- **Cross-domain transfer:** a structural principle is reused in a different task family.
- **Cross-representation transfer:** knowledge moves between linguistic, symbolic, perceptual, or operational forms.
- **Cross-unit relay:** a capability fragment becomes useful through composition with other units.
- **System-level emergence candidate:** coordination might enable behavior not shown by individual components.
- **Temporal reuse:** accumulated execution traces might improve later selection, evaluation, or routing.

These categories MAY overlap. None establishes that the hypothesized capability exists.

### 3.2 Directional Intuition

**Directional intuition** is a low-cost, explicitly uncertain method for prioritizing plausible exploration directions using incomplete evidence. It can use structural similarity, known constraints, perspective fields, historical precedents, negative examples, or residual signals. It is an *exploration policy input*, not a substitute for measurement.

### 3.3 Weak Evidence

**Weak evidence** is information that can rationally motivate a probe but does not by itself satisfy the target capability's acceptance criteria. Examples include a partial analogy, a small uncontrolled success, a related prior result, or a suggestive difference between two structural descriptions.

### 3.4 OTHERS Residual

An **OTHERS residual** is a documented aspect of the target opportunity not captured by the current matching or explanatory model. It MUST be represented as unresolved structure, not silently discarded or automatically treated as a positive signal.

### 3.5 Negative Transfer

**Negative transfer** occurs when reuse or transfer degrades performance, reliability, safety, resource efficiency, or another declared outcome relative to an appropriate baseline. An opportunity record SHOULD state plausible negative-transfer pathways before expensive probing.

## 4. Canonical Spillover Opportunity Record (SOR)

Each SOR MUST have a stable identifier and a revision history. The following fields form the proposed minimum interoperable contract.

| Field | Required | Meaning |
|---|---|---|
| `schema_id` | MUST | Contract identifier, e.g. `isgftr.sor.v1` |
| `opportunity_id` | MUST | Stable unique identifier |
| `revision` | MUST | Monotonic record revision |
| `created_at` / `updated_at` | MUST | Timestamp with timezone |
| `originator` | MUST | Human, agent, team, or system that proposed the opportunity |
| `source_capability_refs` | MUST | One or more SPEC-001 capability-profile references |
| `target_task_contract` | MUST | Target task family, conditions, resources, and acceptance criteria |
| `hypothesis` | MUST | Falsifiable claim of potential spillover or transfer |
| `transfer_mechanism` | MUST | Proposed mechanism and assumptions |
| `boundary_scope` | MUST | Which capability boundary is being explored, with justification |
| `evidence_refs` | MUST | References to motivating evidence; may be empty if explicitly marked speculative |
| `counterevidence_refs` | MUST | References to contrary evidence; may be empty but cannot be omitted |
| `uncertainties` | MUST | Unknowns, dependencies, and measurement limits |
| `risk_and_cost` | MUST | Expected probe costs, failure risks, and constraints |
| `claim_state` | MUST | State consistent with SPEC-001 semantics |
| `next_probe` | SHOULD | Smallest informative test, or explicit reason for deferral |
| `directional_assessment_ref` | SHOULD | Assessment record and policy version |
| `owner_or_steward` | SHOULD | Responsible review or governance contact |
| `related_opportunity_refs` | MAY | Predecessors, alternatives, or competing explanations |
| `relay_history` | MAY | Prior handoffs, feedback, and receiving contexts |

The hypothesis MUST identify **what would count as disconfirming evidence**. `target_task_contract` MUST NOT be replaced by a vague assertion such as “general intelligence” or “works in any domain.”

A SOR MUST distinguish the **source actor** from the **target execution configuration**. For example, a frozen language model plus retrieval tools is not equivalent to the same model acting alone. The record MUST identify the composition used in each claim.

## 5. Canonical Evidence Item

An Evidence Item represents one attributable observation, dataset result, expert judgment, analogy, or experimental outcome. It MUST include:

- `evidence_id`, `evidence_type`, `collected_at`, `source`, and `provenance`;
- `supports_or_challenges`: `support`, `challenge`, `mixed`, or `context_only`;
- `claim_refs`: which opportunity or capability claims the item bears on;
- `observation`: a concise description of what was actually observed;
- `method`: collection method or experimental protocol, including deviations;
- `conditions`: relevant task distribution, tools, actor version, evaluator, and resources;
- `limitations`: uncertainty, selection bias, confounding, and missing data;
- `artifact_refs`: immutable or versioned references to logs, measurements, code, or datasets where available;
- `independence_group`: identifier to flag correlated or reused evidence.

Recommended `evidence_type` values are `analogy`, `structural_match`, `historical_precedent`, `expert_judgment`, `pilot_probe`, `controlled_probe`, `replication`, `failure`, `counterexample`, and `operational_observation`. The list is extensible; types MUST NOT be treated as a universal quality ranking.

An analogy MAY justify exploration, but MUST NOT alone establish a target capability. A successful pilot probe MUST NOT be relabeled an independent replication. A negative result MUST NOT be deleted solely because it conflicts with the preferred hypothesis.

## 6. Evidence Bundle and Counterevidence Register

An **Evidence Bundle** groups evidence items relevant to a particular opportunity revision and review decision. It MUST contain:

1. A stable bundle identifier and version.
2. The opportunity revision and target task contract being assessed.
3. References to supporting, challenging, mixed, and contextual items.
4. A dependence map or statement of known evidence overlap.
5. An explicit synthesis explaining what is and is not supported.
6. A record of unresolved alternatives and residual uncertainty.
7. A reviewer identity or declared automated review policy.
8. A decision timestamp and a link to the decision record.

A **Counterevidence Register** MUST remain queryable across opportunity revisions. Its entries SHOULD include failure conditions, alternative explanations, affected claims, severity, status, and follow-up probes. `unresolved`, `addressed`, and `superseded` are acceptable statuses; `addressed` MUST cite the evidence that resolves the concern. `superseded` MUST preserve the historical entry.

Evidence quality depends on *relevance, measurement design, provenance, and independence*, not merely item count. Ten correlated examples SHOULD NOT be treated as ten independent confirmations.

## 7. Structural Correspondence and Transfer Mapping

A transfer hypothesis SHOULD specify a **source-to-target mapping** with at least:

- `source_structure`: relevant source concepts, relations, operators, or constraints;
- `target_structure`: hypothesized target counterparts;
- `preserved_relations`: invariants expected to survive transfer;
- `required_adaptations`: changes needed to fit target context;
- `known_mismatches`: differences already identified;
- `others_residuals`: important aspects not explained by the mapping;
- `failure_conditions`: conditions under which the mapping is expected to break;
- `mapping_evidence_refs`: evidence supporting or challenging the mapping.

A mapping MAY be symbolic, graph-based, metric-native, embedding-based, procedural, or hybrid. The contract does not require a common Euclidean representation. A partial match is admissible for prospecting if its limitations are recorded. It MUST NOT be silently promoted to structural equivalence.

For example, “resource allocation in a swarm resembles distributed compute scheduling” is a plausible *direction* for investigation. The record must still address differing agent objectives, communication latency, observability, failure recovery, and control authority.

## 8. Directional Assessment and Prospect Ranking

A **Directional Assessment** is an optional but recommended record that explains why one opportunity receives exploration priority over another. It SHOULD contain:

- assessment identifier, assessor, timestamp, and policy version;
- component estimates such as structural fit, evidence strength, novelty, expected information gain, probe feasibility, cost, negative-transfer risk, and downstream reuse potential;
- measurement scales and missing-data conventions;
- an aggregation rule, weights or constraints, and sensitivity analysis;
- uncertainty bounds or qualitative confidence labels, with their meaning;
- the resulting *priority*, and a clear statement of whether it is calibrated.

An illustrative heuristic is:

$$
P(o)=w_s S(o)+w_e E(o)+w_i I(o)+w_r R(o)-w_c C(o)-w_n N(o),
$$

where $S$ denotes structural plausibility, $E$ evidence quality, $I$ expected information value, $R$ potential reuse, $C$ cost, and $N$ negative-transfer risk. This is **not** a canonical probability model. Weights and component scales MUST be disclosed if the score is reported. A high score authorizes, at most, consideration for a probe subject to governance constraints.

The assessment SHOULD also report how ranking changes under reasonable alternative weights and how unmeasured OTHERS residuals might reverse the recommendation. A constrained portfolio MAY favor diversity of mechanisms and domains rather than only top-ranked candidates.

## 9. Exploration and Validation Gates

This contract distinguishes two gates; SPEC-003 will define their full lifecycle.

### Gate A — Exploration Admissibility

Gate A asks whether a candidate is worth a bounded, reversible, ethically and operationally permitted test. Its decision MUST consider scope, cost, safety, uncertainty, and whether the probe can produce informative evidence. Passing Gate A **does not** validate the opportunity.

### Gate B — Claim Promotion

Gate B asks whether the resulting evidence supports a defined claim under SPEC-001. It MUST reference the target task contract, predeclared acceptance criteria, relevant baselines, counterevidence, and independence limitations. Passing a single Gate B review does not imply unrestricted generalization, AGI, or durable growth.

A conforming record MUST NOT skip Gate B by relabeling a directional assessment as empirical validation. Where the same team both proposes and evaluates an opportunity, the bundle SHOULD disclose this dependence and seek independent review when stakes justify it.

## 10. Evidence Strength and Calibration

The specification does not prescribe a universal scalar evidence-strength scale. If a project defines one, it MUST publish the rubric, data dependencies, and limitations. A calibrated success probability requires a declared target event, reference population, prediction horizon, and out-of-sample calibration assessment. Without those elements, numbers MUST be described as *heuristic priority scores* or *uncalibrated estimates*.

Reviewers SHOULD separate:

- **Epistemic uncertainty:** uncertainty about mechanisms or hypotheses.
- **Measurement uncertainty:** uncertainty arising from evaluators, sampling, or instrumentation.
- **Context uncertainty:** uncertainty about transfer to different domains or deployment settings.
- **Attribution uncertainty:** uncertainty about which unit, tool, human, or structural arrangement produced the result.

Evidence that supports a system-level claim MAY fail to support a component-level claim. The reverse also holds: strong unit performance does not prove reliable composition.

## 11. Negative Results, Drift, and Evidence Contamination

An opportunity's evidence history MUST preserve material negative findings and protocol failures. An Evidence Item SHOULD flag suspected:

- benchmark or training-data contamination;
- evaluation leakage or adaptive overfitting;
- correlated replications;
- changing target definitions after observing outcomes;
- hidden human assistance or tool dependencies;
- semantic drift between source and target structures;
- nonstationary environments and version changes;
- cost escalation or unsafe side effects.

If a claimed success depends on a revised task definition, the record MUST identify the revision rather than rewriting earlier criteria. Failed probes can remain valuable as evidence relay; their value lies in improving future selection and explanation, not in being counted as successes.

## 12. Provenance, Revisions, and Relay Readiness

Every SOR and Evidence Bundle MUST be versioned. Material changes to hypothesis, target criteria, actor composition, evidence synthesis, or claim state MUST produce a new revision with a reason. Prior revisions MUST remain addressable.

A relay-ready bundle SHOULD include:

1. A concise hypothesis and its disconfirmation conditions.
2. Source capability and target task references.
3. Structural mapping, residuals, and known limitations.
4. Evidence and counterevidence with provenance.
5. Probe protocol and actual outcomes, if any.
6. Current claim state and permissible downstream uses.
7. Unresolved questions and recommended next tests.

Receiving systems MUST NOT interpret receipt of a relay package as independent verification. If evidence is re-used across several relays, its original `evidence_id` and `independence_group` MUST be preserved to avoid double counting.

## 13. Illustrative YAML Record

The following example is **synthetic** and demonstrates format, not a validated transfer result.

```yaml
schema_id: isgftr.sor.v1
opportunity_id: SOR-EXAMPLE-001
revision: 1
created_at: "2026-10-30T12:00:00Z"
updated_at: "2026-10-30T12:00:00Z"
originator:
  type: research_team
  id: team-example
source_capability_refs:
  - CAP-EXAMPLE-ROUTING-001
target_task_contract:
  task_family: dynamic_service_dispatch
  environment: simulated_nonstationary_requests
  actor_configuration: frozen_planner_plus_adaptive_router
  allowed_resources: [historical_dispatch_traces, simulator]
  acceptance_criteria:
    metric: normalized_regret
    comparison: prespecified_static_routing_baseline
    criterion: improvement_with_uncertainty_interval
hypothesis: >
  Structural patterns from queue scheduling may help select
  routing strategies under changing service demand.
transfer_mechanism:
  type: partial_structural_mapping
  preserved_relations: [resource_constraints, queue_backlog]
  required_adaptations: [spatial_travel_cost, demand_nonstationarity]
  known_mismatches: [delayed_feedback, heterogeneous_agents]
  others_residuals: [unmodeled_local_preferences]
boundary_scope:
  category: reachable
  rationale: tool-mediated system configuration is being explored
claim_state: hypothesized
evidence_refs:
  - EVID-EXAMPLE-001
counterevidence_refs: []
uncertainties:
  - whether the source mapping improves target outcomes
  - whether observed effects persist on held-out scenarios
risk_and_cost:
  risk_level: low_in_simulation
  estimated_probe_budget: 1000_simulated_episodes
  constraints: [no_live_deployment]
directional_assessment_ref: ASSESS-EXAMPLE-001
next_probe:
  protocol_ref: PROBE-EXAMPLE-001
  disconfirmation: no_gain_or_negative_transfer_on_held_out_scenarios
```

An associated Evidence Item could be:

```yaml
evidence_id: EVID-EXAMPLE-001
evidence_type: structural_match
collected_at: "2026-10-30T12:00:00Z"
source: team-example
provenance: analyst_documented_mapping
supports_or_challenges: context_only
claim_refs: [SOR-EXAMPLE-001]
observation: shared_queue_and_capacity_constraints
method: conceptual_structure_comparison
conditions: {evaluation_performed: false}
limitations: [no_target_domain_performance_evidence]
artifact_refs: [mapping-note-example-v1]
independence_group: mapping-example-001
```

The example deliberately avoids presenting conceptual similarity as measured transfer success.

## 14. Contract Invariants

A conforming implementation MUST enforce the following invariants:

**INV-001 — Opportunity/Capability Separation.** A hypothesis cannot be automatically treated as an observed capability.

**INV-002 — Scoped Target.** Every opportunity names a target task contract and evaluation conditions.

**INV-003 — Actor Attribution.** Source and target actor configurations remain distinguishable.

**INV-004 — Evidence Traceability.** Every cited evidence item has stable identity and provenance.

**INV-005 — Counterevidence Visibility.** Challenging evidence is preserved and addressable.

**INV-006 — Score Semantics.** An uncalibrated ranking is not labeled a probability of success.

**INV-007 — Mapping Limits.** Partial correspondences disclose mismatches and unresolved residuals.

**INV-008 — Gate Separation.** Exploration authorization cannot silently promote a capability claim.

**INV-009 — Revision Integrity.** Material edits produce a traceable new revision.

**INV-010 — No Relay Laundering.** Repeated handoffs do not create independent evidence or verification.

**INV-011 — Negative Result Preservation.** Material failures and negative-transfer observations remain in the record.

**INV-012 — Boundary Discipline.** A demonstrated local transfer is not generalized to unrestricted AGI or open-ended growth.

## 15. Illustrative Conformance Tests

| Test | Input or scenario | Expected result |
|---|---|---|
| CT-001 | Opportunity without target task contract | Reject as nonconformant |
| CT-002 | Hypothesis with no disconfirmation condition | Reject or require revision |
| CT-003 | Uncontrolled analogy entered as `replication` | Reject evidence-type misrepresentation |
| CT-004 | Uncalibrated score labeled “85% success probability” | Reject unsupported probability claim |
| CT-005 | Partial mapping with hidden mismatches | Reject or mark incomplete |
| CT-006 | Evidence bundle with no counterevidence field | Reject incomplete record |
| CT-007 | Gate A approval used to set `observed` | Reject invalid state promotion |
| CT-008 | Reused evidence copied under new IDs as independent | Flag dependence and prohibit double counting |
| CT-009 | Negative result removed from next revision | Reject history violation |
| CT-010 | Frozen model plus tools credited to model alone | Reject attribution error |
| CT-011 | Changed evaluation metric with unchanged record revision | Reject revision violation |
| CT-012 | Evidence item has unknown source and no provenance caveat | Mark insufficient for verification |
| CT-013 | Valid speculative opportunity with empty evidence refs and explicit uncertainty | Accept as speculative, not validated |
| CT-014 | Replicated task-specific result extrapolated to universal AGI | Reject overbroad inference |

These are *proposed checks*, not reports of executed software tests. Future implementations SHOULD publish machine-readable fixtures and a reproducible validator.

## 16. Minimal Review and Decision Protocol

Before allocating a probe budget, a reviewer SHOULD ask:

1. Is the proposed transfer mechanism understandable enough to challenge?
2. Is the target task contract narrow enough to evaluate?
3. What evidence is independent, and what is only analogy?
4. What plausible counterexamples or OTHERS residuals are being ignored?
5. Which inexpensive experiment would most reduce uncertainty?
6. Are baselines, resource budgets, and safety constraints explicit?
7. Would failure produce reusable information rather than only a discarded attempt?

Before promoting a claim, reviewers MUST compare the outcome against declared criteria and record alternative explanations. If the evidence is insufficient, the correct outcome may be `inconclusive` or `contested`, not a forced positive or negative verdict.

## 17. Research Questions and Proposed Extensions

The contract intentionally leaves several research problems open:

- Can structural mapping quality be estimated without reducing all tasks to a shared embedding space?
- Which weak-evidence combinations improve *discovery efficiency* rather than merely raising the number of speculative proposals?
- How should OTHERS residuals affect priority when their direction is unknown?
- Can prospecting policies learn from failures without overfitting to historical task families?
- How should collective systems reconcile conflicting evidence while preserving dissent and provenance?
- What is the minimum evidence required to justify transferring a result between different system configurations?
- How can calibration be assessed under rare, open-ended, or shifting opportunity distributions?
- When does the cost of provenance and review outweigh the value of a relay opportunity?

These questions are suitable for independent contributions, benchmark design, negative-result reporting, and collaborative refinement of the contract.

## 18. Figure Placement and Research Interfaces

**Suggested figure:** `figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png`, placed near Sections 4–9 to depict the opportunity/evidence separation and prospecting gates. The figure is an optional explanatory aid; the normative contract is textual.

**Related research interfaces:**

- ISGFTR-001 — From Static Intelligence Boundaries to Open Capability Frontiers.
- ISGFTR-003 — Folding–Generalization Duality and Structural Reuse.
- ISGFTR-004 — Intelligence Fluidity and Permeable Structural Boundaries.
- ISGFTR-005 — Directional Intuition and Weak-Evidence Transfer.
- ISGFTR-008 — Intelligence Spillover and Transfer Prospecting.
- ISGFTR-009 — AGI Implications, Limits, and Counterarguments.
- ISGFTR-010 — An Open Research Architecture for Collective Learning.
- SPEC-001 — Canonical Capability and Boundary Contract.
- SPEC-003 — Prospecting, Probing, and Validation Lifecycle (planned).
- SPEC-004 — Structural Relay and Collective Learning Contract (planned).

The broader Structural Intelligence research program—including BM-ODWEI and Metric-Native Directional Intuition, UCPSF, SIF, UIERU, and AQSI—offers candidate mechanisms and research connections. Their relevance should be evaluated rather than assumed.

## 19. Conclusion

SPEC-002 treats capability prospecting as a disciplined process of proposing, evaluating, and revising **uncertain opportunities**. Its primary contribution is not a scoring algorithm or a guarantee of intelligence growth. It is an explicit boundary between *what suggests a direction*, *what was actually measured*, *what remains unexplained*, and *what may responsibly be relayed as evidence*. This separation supports more informative experiments, less misleading claims, and a collective learning process in which failed transfers, unresolved questions, and counterexamples remain valuable research assets.

---

**Document status:** Open proposed specification for critique, refinement, independent implementation, and empirical testing. No conformance certification or performance result is claimed.
