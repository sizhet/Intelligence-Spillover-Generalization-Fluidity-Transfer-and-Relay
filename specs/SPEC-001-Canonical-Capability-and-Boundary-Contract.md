# SPEC-001 — Canonical Capability and Boundary Contract

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Proposed interoperable research specification  
**Version:** v1.0.0 (theory-first)  
**Status:** Draft research contract; not an adopted standard or validated implementation  
**Date:** 2026-10-30

## Abstract

This specification proposes a minimal, auditable contract for describing a capability, the conditions under which it has been observed, and the boundaries of what is generated, demonstrated, potentially reachable, or potentially evolvable. Its purpose is to prevent an exploratory hypothesis from silently becoming a verified capability claim. The contract accommodates individual models, composite systems, human–AI teams, and evolving relay networks without assuming that all intelligence is reducible to one scalar score or one model's parameters. It defines normative record fields, provenance and evaluation requirements, claim states, uncertainty treatment, compatibility checks, failure conditions, and illustrative conformance tests. The specification is a research proposal intended to support independent criticism, replication, negative evidence, and collective learning.

**Keywords:** capability profile; intelligence boundary; provenance; task contract; uncertainty; structural relay; evidence governance; conformance; falsifiability.

---

## 1. Scope and Normative Language

This contract describes **what a capability claim means**, **what evidence supports it**, and **which boundary interpretation is permitted**. It does not prescribe a model architecture, training method, scoring function, implementation language, or universal benchmark. It is the first of four related specifications:

- **SPEC-001:** Capability and Boundary Contract (this document).
- **SPEC-002:** Spillover Opportunity and Evidence Contract.
- **SPEC-003:** Prospecting, Probing, and Validation Lifecycle.
- **SPEC-004:** Structural Relay and Collective Learning Contract.

The terms **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** express requirements for a record that claims conformance with *this proposed contract*. They do not assert a community-wide standard. An illustrative field may be extended without changing the meaning of required fields.

A conforming record MUST NOT infer AGI, unlimited transfer, or open-ended improvement from isolated task success. It MUST distinguish measured observations from forecasts, analogies, and research hypotheses.

## 2. Core Definitions

### 2.1 Capability

A **capability** is a reproducible ability of an identified actor to perform a defined class of tasks under specified conditions, evaluated against explicit criteria. A capability claim is incomplete without its task distribution, permitted resources, evaluator, and evidence scope.

A claim is represented conceptually as:

\[
C=(A,T,K,R,M,E,P,S),
\]

where **A** is actor identity and composition, **T** is task definition and distribution, **K** is context and operating constraints, **R** is available resources and tools, **M** is measurement protocol, **E** is evidence, **P** is provenance, and **S** is claim state. This tuple is descriptive, not an assertion that capability is a single numeric quantity.

### 2.2 Actor and unit of analysis

An **actor** may be a model, agent, tool chain, collective, organization, or human–AI system. The contract MUST identify the unit of analysis. A system-level outcome MUST NOT automatically be attributed to each constituent unit. A frozen-model system can change its routing, memory, or coordination while constituent model weights remain unchanged; both facts SHOULD be recorded.

### 2.3 Task domain and evaluation envelope

A **task domain** defines the family of inputs, desired outputs, success criteria, and known exclusions. An **evaluation envelope** specifies data split, environment, tools, time, compute, human assistance, retry allowance, evaluator version, and other conditions relevant to interpreting results. Comparisons across materially different envelopes require an explicit comparability argument.

### 2.4 Structural boundary

A **boundary** is an evidence-qualified description of a capability limit or frontier under a defined evaluation envelope. It may be task-relative, resource-relative, temporal, representation-relative, or organizational. A boundary is not necessarily a geometric surface or a globally ordered threshold.

### 2.5 Gap and prospect

A **gap** identifies a desired behavior not yet established under the current evidence and conditions. A **prospect** proposes a mechanism by which the gap might be explored or bridged. Neither constitutes a verified capability. See SPEC-002 and SPEC-003 for their richer contracts.

## 3. Four Boundary Categories

| Category | Question | Evidence interpretation | Forbidden inference |
|---|---|---|---|
| **Generative** | What outputs or behaviors can the actor produce under a specified generation procedure? | Samples, coverage tests, or formal constraints on generated behavior | Generated behavior is useful, correct, or general |
| **Observed** | What has the actor demonstrably achieved under recorded conditions? | Evaluation results with provenance and uncertainty | Unmeasured tasks are solved |
| **Reachable** | What might become attainable through permitted reconfiguration, tools, representation, or coordination? | Mechanistic hypothesis, bounded probes, or established constructive pathway | Reachability is already demonstrated |
| **Evolvable** | What future capability changes might arise through allowed learning, memory, relay, or structural adaptation? | Longitudinal evidence or explicitly uncertain growth hypothesis | Improvement is unbounded or inevitable |

The categories MUST be separately labeled. They **MUST NOT** be treated as universally nested sets: a generated output may fail evaluation; a reachable result may depend on an external tool not available to the baseline actor; an evolvable possibility may never be realized. Boundaries MAY overlap, change with context, and be only partially comparable.

For each boundary assertion, the record MUST state: (1) category, (2) actor and task scope, (3) operating envelope, (4) evidence or hypothesis basis, (5) known exclusions, and (6) uncertainty or confidence rationale. If the evidence is insufficient, the state MUST be `unknown` or `hypothesized`, not `verified`.

## 4. Canonical Capability Profile

A **Capability Profile** is the primary interoperable object. The following is a *proposed logical schema*, not a published JSON Schema or a guarantee of executable interoperability.

| Field | Required | Meaning |
|---|---|---|
| `schema_id` | MUST | `ISGFTR-SPEC-001` |
| `schema_version` | MUST | Version of this record contract |
| `capability_id` | MUST | Stable identifier within a declared namespace |
| `record_version` | MUST | Immutable revision label |
| `actor` | MUST | Identity, type, composition, relevant versions |
| `task_contract` | MUST | Input class, desired outputs, exclusions, success criteria |
| `evaluation_envelope` | MUST | Data, tools, compute, budget, human involvement, environment |
| `claim` | MUST | Precise capability statement and claim state |
| `boundary_assertions` | MUST | Zero or more typed boundary records; empty list allowed if explicitly unknown |
| `evidence_refs` | MUST | References to supporting and contradicting evidence; may be empty for hypotheses |
| `provenance` | MUST | Author/source, date, artifact origin, transformations, disclosure limits |
| `uncertainty` | MUST | Sources of uncertainty and method of estimation or explanation of absence |
| `limitations` | MUST | Known failure cases, exclusions, and interpretation limits |
| `dependencies` | SHOULD | Tools, memory, services, external models, people |
| `baseline_refs` | SHOULD | Comparable reference actors and protocols |
| `cost_profile` | SHOULD | Latency, compute, energy, monetary, human costs when measured |
| `governance` | SHOULD | Permissions, risk tier, evaluator independence, review status |
| `related_relay_refs` | MAY | Linked structural or evidence relay artifacts |
| `supersedes` | MAY | Prior record revisions, never silently overwritten |

Required fields may explicitly contain `unknown`, `not_measured`, or an empty collection when appropriate, but MUST NOT fabricate a value. A missing observation is not evidence of inability; a missing counterexample is not evidence of robustness.

## 5. Canonical Boundary Record

Each `boundary_assertions` entry SHOULD contain:

- `boundary_id`, `boundary_type`, and `claim_state`;
- `scope`: task slice, representation, actor, resources, and temporal horizon;
- `statement`: an operationally testable boundary description;
- `basis`: observation, formal result, probe, analogy, or conjecture;
- `evidence_refs` and `counterevidence_refs`;
- `uncertainty`: sampling, distribution shift, measurement error, evaluator limitations;
- `conditions_for_revision`: a test or observation that would change the assessment;
- `owner_or_reviewer`, `created_at`, and `record_version`.

A boundary record SHOULD distinguish **empirical failure under a test** from **proved impossibility**. The former does not establish the latter. For reachable and evolvable categories, a mechanism and explicit probe plan SHOULD accompany any optimistic assertion.

## 6. Claim States and Permitted Transitions

The contract proposes these states:

| State | Meaning |
|---|---|
| `hypothesized` | Proposed mechanism or capability, not established by a qualifying test |
| `under_probe` | Bounded exploratory tests are in progress |
| `observed` | Reported success under a documented evaluation envelope |
| `replicated` | Independently repeated under stated comparability criteria |
| `contested` | Material counterevidence, methodological dispute, or unresolved contradiction |
| `retracted` | Claim withdrawn or superseded as unsupported |
| `unknown` | Insufficient information to characterize a capability or boundary |

`observed` is **not** equivalent to `replicated`; neither is equivalent to broad generalization. Transition from `hypothesized` to `observed` MUST cite qualifying evidence. Transition to `replicated` MUST identify independent replication and differences in conditions. A claim MAY transition from any evidence-bearing state to `contested` or `retracted`. No state transition SHOULD erase previous versions or negative evidence.

A conforming registry MUST preserve the historical trail of transitions or an equivalent append-only audit history. This is an evidence-governance requirement, not a demand for any particular database technology.

## 7. Evaluation Envelope and Comparability

Capability comparisons MUST state the conditions that may explain differences:

1. **Task and sampling:** task population, selection criteria, difficulty, held-out status, contamination risk.
2. **Execution resources:** time, compute, context, tools, retries, external memory, human intervention.
3. **Actor configuration:** model and system versions, routing, prompts, policies, retrieval sources.
4. **Evaluation:** metric, evaluator identity, blind review where appropriate, confidence intervals or uncertainty explanation.
5. **Costs and risks:** whether improved success requires disproportionate resources or unacceptable side effects.

A purported spillover or generalization gain SHOULD compare against strong, resource-matched baselines. If a new system gains access to an external solver, the record SHOULD attribute the gain to **system-level access and orchestration** unless independent evidence establishes a change in the original unit's intrinsic competence.

For stochastic results, the record SHOULD report sample size, variance or interval estimates, and failed trials. A single demonstration MAY justify `observed` only for the narrowly defined event it demonstrates; it MUST NOT support an unqualified distribution-wide claim.

## 8. Provenance, Evidence, and Counterevidence

A capability claim MUST identify the origin of evidence and the evaluation procedure. Evidence references SHOULD resolve to versioned artifacts or reproducible descriptions. Each reference SHOULD include:

- evidence ID, kind (measurement, trace, formal argument, replication, counterexample), and timestamp;
- dataset/protocol version and evaluator;
- relationship to the claim (`supports`, `limits`, `contradicts`, or `inconclusive`);
- access restrictions, license, and reproduction instructions where possible.

The contract MUST NOT require public disclosure of private, proprietary, or dangerous data. Where evidence cannot be shared, the record MUST describe the restriction and reduce its verification claims accordingly. An evidence package can be **well documented but not independently reproducible**; these are distinct properties.

Negative results and failed probes SHOULD remain addressable, even when the research team changes direction. A later successful relay MUST NOT retroactively relabel earlier failures as successes.

## 9. Uncertainty and Confidence Discipline

The contract distinguishes at least four uncertainties: **aleatoric** (task variability), **epistemic** (limited knowledge), **structural** (uncertain mapping between domains or representations), and **evaluation** (metric, reviewer, or benchmark limitations). Authors MAY use other taxonomies if explicitly defined.

A directional prospect score is a **ranking signal**, not a calibrated probability of success unless calibration is empirically established. Confidence labels MUST include their derivation or be explicitly qualitative. Claims of boundary expansion SHOULD distinguish the measured gain from uncertainty about its portability to new tasks or environments.

## 10. Minimal Example (Illustrative YAML)

```yaml
schema_id: ISGFTR-SPEC-001
schema_version: '1.0.0'
capability_id: 'example:route-and-check-v1'
record_version: '1'
actor:
  id: 'example:composite-system'
  type: 'composite-system'
  components:
    - 'example:frozen-model-v1'
    - 'example:external-verifier-v1'
task_contract:
  domain: 'synthetic-rule-checking'
  input_class: 'held-out rule instances'
  success_criterion: 'exact agreement with an independent oracle'
  exclusions: ['unseen rule families']
evaluation_envelope:
  dataset_version: 'synthetic-heldout-1'
  tools: ['external-verifier-v1']
  retry_budget: 1
  human_assistance: 'none during evaluation'
claim:
  statement: 'The composite system completed a subset of held-out instances.'
  state: observed
boundary_assertions:
  - boundary_id: 'example:observed-subset'
    boundary_type: observed
    claim_state: observed
    scope: 'synthetic-heldout-1 only'
    statement: 'Success is limited to the reported evaluation subset.'
    basis: 'documented evaluation'
    evidence_refs: ['example:eval-report-1']
    counterevidence_refs: ['example:failed-cases-1']
    uncertainty: 'Sampling and transfer beyond this subset not established.'
    conditions_for_revision: 'Independent held-out replication'
evidence_refs: ['example:eval-report-1', 'example:failed-cases-1']
provenance:
  origin: 'illustrative example, not actual measured results'
  created_at: '2026-10-30'
uncertainty:
  note: 'No quantitative performance figures are asserted.'
limitations:
  - 'No evidence of improvement to frozen model weights.'
  - 'No claim about broad transfer or AGI.'
```

This is deliberately **not an empirical result**. A conforming implementation would need to define the serialization profile, identifier resolution, and field-level validation rules before claiming machine-checked interoperability.

## 11. Validation Rules and Invariants

A proposed conformance checker SHOULD enforce the following invariants:

**INV-001 — Identity:** Every record has a unique, versioned capability ID and declared actor.

**INV-002 — Scope:** Every capability statement is bound to a task contract and evaluation envelope.

**INV-003 — Boundary typing:** Every boundary assertion uses one of the four defined categories, or a declared extension type.

**INV-004 — Evidence honesty:** `observed` and `replicated` claims have traceable supporting evidence; `replicated` identifies independence criteria.

**INV-005 — No silent promotion:** A hypothesis or prospect cannot become a verified capability merely by being relayed, copied, scored, or cited.

**INV-006 — Counterevidence retention:** Material contradictory evidence remains linked, even after record revision.

**INV-007 — Actor attribution:** System-level improvements are not automatically attributed to frozen constituent models.

**INV-008 — Comparability:** Cross-system improvement claims identify changed resources, tools, tasks, and evaluation protocols.

**INV-009 — Version preservation:** Revisions do not silently overwrite the historical claim and evidence trail.

**INV-010 — Safety and disclosure:** Sensitive evidence may be access-controlled; unsupported verification claims must be qualified.

## 12. Conformance Test Matrix

| Test | Input condition | Expected result |
|---|---|---|
| CT-001 | Fully scoped hypothesis with no observations | Accept as `hypothesized`; not verified |
| CT-002 | `observed` claim with no evidence reference | Reject or downgrade pending evidence |
| CT-003 | `replicated` claim with only same-run reruns | Reject replication status |
| CT-004 | Boundary category omitted | Reject boundary assertion |
| CT-005 | New tool improves composite system; claim says base model learned | Flag attribution mismatch |
| CT-006 | Negative evidence omitted from revised record | Flag provenance integrity failure |
| CT-007 | Transfer score described as 90% success probability without calibration | Reject probability interpretation |
| CT-008 | Two benchmarks use unequal retry budgets | Require qualification of comparison |
| CT-009 | Failed trial reported with explicit limitations | Accept as valuable evidence |
| CT-010 | `evolvable` hypothesis asserted as guaranteed AGI | Reject unsupported conclusion |

The test matrix is a design target, not a report that a validator has already been implemented or run.

## 13. Worked Boundary Interpretation

Suppose a frozen language model cannot reliably solve a synthetic verification task on its own. A composite system adds a structured parser and external verifier, and succeeds on a held-out subset. Three statements are possible:

- **Supported, if measured:** The *composite system* demonstrated success under the specified envelope.
- **Potentially testable:** The architecture may transfer to another task family after appropriate adaptation and evaluation.
- **Unsupported without further evidence:** The original frozen model acquired a new intrinsic general capability or the composite system achieved AGI.

A second experiment adds a persistent routing memory that improves task selection across weeks. The resulting gain may be **system-level structural learning** even if component weights remain fixed. To establish *durable growth*, researchers must show retention, improvement against resource-matched baselines, and generalization beyond the feedback cases. Repetition that only replays identical answers is not sufficient.

## 14. Relationship to the ISGFTR Research Program

This specification operationalizes the four boundaries introduced in **ISGFTR-001**, the five-characteristic distinction of **ISGFTR-002**, structural reuse in **ISGFTR-003**, selective permeability in **ISGFTR-004**, directional weak evidence in **ISGFTR-005**, multi-level learning in **ISGFTR-006**, recursive relay in **ISGFTR-007**, prospecting in **ISGFTR-008**, AGI limits in **ISGFTR-009**, and the open research architecture in **ISGFTR-010**.

It is particularly important for the five-plane architecture: the **Prospecting Plane** may create hypothetical boundary assertions; the **Experiment Plane** generates observations; the **Evidence Plane** assesses quality and contradictions; the **Relay Plane** transports versioned records; and the **Governance Plane** controls permissible promotion and use. These planes are logical responsibilities, not mandatory software services.

**Suggested figure references:** `figures/Fig-002-Four-Intelligence-Boundaries.png` after Section 3; `figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png` after Section 13. Figures are planned explanatory aids, not evidence.

## 15. Open Questions and Proposed Extensions

1. Can boundary records remain meaningful when task distributions evolve faster than evaluations can be replicated?
2. What is the smallest common capability schema that preserves useful uncertainty without burdening lightweight experiments?
3. How should human participation and tool contributions be attributed in a composite actor?
4. Which measures distinguish genuine structural learning from caching, benchmark contamination, or added compute?
5. Can boundary comparisons be expressed as partial orders rather than misleading universal scores?
6. How can confidential evidence support limited independent audits without disclosing protected data?
7. Which claims require domain-specific safety review before relay into operational systems?
8. How should a record represent conflicting independent replications without collapsing them into a single confidence number?

Researchers are invited to challenge the four-boundary taxonomy, propose simpler representations, supply counterexamples, and test whether the contract improves reproducibility relative to ordinary benchmark reports. Failure of this schema to support meaningful comparison would be a valuable negative result.

## 16. Research Status and Next Contracts

**Current status:** Conceptual contract and proposed conformance criteria. No reference implementation, interoperability certification, benchmark performance, or empirical validation is claimed.

**Next:** `SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md` will define the evidence-bearing prospect objects linked to this capability profile. `SPEC-003` will specify state transitions for probing and validation. `SPEC-004` will define preservation and exchange of these records through structural relay and collective learning.

**Research principle:** *A capability boundary is a scoped, revisable claim about evidence—not a permanent verdict about what intelligence can become.*
