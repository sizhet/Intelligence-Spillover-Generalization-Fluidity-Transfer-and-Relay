# SPEC-004 — Structural Relay and Collective Learning Contract

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Proposed interoperable research specification  
**Version:** v1.0.0 (theory-first)  
**Status:** Draft research contract; not an adopted standard or validated runtime  
**Date:** 2026-10-30

## Abstract

This specification proposes a portable, evidence-bearing contract for **structural relay** and **collective learning** across intelligence units, researchers, organizations, execution cycles, and domains. It defines how a research result—including a negative result, unresolved question, counterexample, or repeated execution—can be packaged, transmitted, interpreted, evaluated, reused, and revised without silently inflating its evidential status. A relay may move a claim, a structural component, a task policy, an evaluation protocol, or a reusable failure pattern; these objects are not interchangeable. The proposed contract separates **transport**, **interpretation**, **adoption**, **demonstrated utility**, and **durable learning**. It requires provenance, explicit scope, claim-state preservation, recipient-side conformance checks, versioned lineage, counterevidence, and bounded governance. It supports system-level learning even when individual execution models remain frozen, but makes no claim that such learning inevitably produces AGI or recursive self-improvement.

**Keywords:** structural relay; portable intelligence units; collective learning; evidence provenance; negative results; temporal relay; capability transfer; conformance; system-centric intelligence; open research.

---

## 1. Purpose, Scope, and Normative Vocabulary

The purpose of this contract is to make intelligence research **cumulatively inspectable** rather than merely communicable. A document can be copied without its methods being reproducible; a model can be reused without its capability claims transferring; and a successful experiment can be relayed without creating durable growth. This specification keeps these distinctions explicit.

The words **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** denote requirements within this *proposed ISGFTR contract* only. They do not assert endorsement by an external standards organization.

The contract covers: (a) relay unit identity and metadata; (b) evidence and counterevidence lineage; (c) sender and recipient responsibilities; (d) transfer/adoption lifecycle; (e) system-level learning attribution; (f) negative-result and residual preservation; (g) governance and conformance testing. It does not prescribe a universal representation of intelligence, require disclosure of confidential source material, or treat transfer success as guaranteed.

## 2. Position Within the Four-SPEC Family

| Specification | Primary concern | Interface to SPEC-004 |
|---|---|---|
| `SPEC-001` | Capability profile, operating scope, four boundaries, claim states | Referenced capability claims, actors, tasks, boundary conditions |
| `SPEC-002` | Spillover Opportunity Record (SOR), directional scores, weak evidence, counterevidence | Referenced opportunity, evidence items, transfer correspondence |
| `SPEC-003` | Prospecting, probing, authorization, validation, lifecycle decisions | Registered protocol, probe outcomes, gate decisions, deviations |
| **`SPEC-004`** | Portable relay, recipient adoption, evidence preservation, collective learning | Relay manifests, lineage, recipient decisions, aggregate learning |

A relay package MUST NOT override the source record's claim state or transform an exploratory finding into a validated one merely through repackaging. A recipient's stronger claim requires new evidence and its own adjudication.

## 3. Key Definitions and Distinctions

**Structural Relay Unit (SRU):** A versioned, bounded package containing a transferable research or execution artifact and enough context to assess what it means and where it may be reused.

**Relay event:** An attempted handoff between source and recipient contexts, including unsuccessful or rejected handoffs.

**Evidence relay:** Transmission of observations, protocols, outcomes, uncertainty, and counterevidence for later review. It does not imply capability transfer.

**Capability relay:** A recipient's attempted use of a source capability, method, or component under an explicit target operating envelope. Its success requires target-side tests.

**Structural learning:** Persistent improvement in a system's representation, routing, memory, composition, evaluation, or control policy, potentially without changing component model weights.

**Collective learning:** Persistent improvement in a shared or federated knowledge/decision system that can influence subsequent work by multiple participants, subject to governance and evaluation.

**Temporal relay:** A handoff across execution times, including the reuse of a previous attempt's traces, failure analyses, or accumulated observations.

**Residual:** An unresolved mismatch, exception, uncertainty, or unexplained observation retained for later exploration; not automatically a novel capability.

**Adoption:** Recipient acceptance of a relay object for a specified purpose. Adoption is not proof of utility.

**Utility:** Measured improvement on declared outcomes, compared with a relevant baseline and accounting for costs.

**Growth:** Persistent, attributable improvement that survives appropriate follow-up evaluation. Growth is stronger than a one-off utility gain.

The guiding separation is:

> **Transmission ≠ interpretation ≠ adoption ≠ utility ≠ durable growth.**

## 4. Relay Object Types and Allowed Semantics

A conforming SRU MUST declare a `unit_type` and MUST NOT imply that all types carry equivalent evidential authority.

| Unit type | Typical contents | Permitted interpretation |
|---|---|---|
| `capability_profile` | Scoped actor/task performance and boundaries | Description of a claim under conditions |
| `opportunity` | SOR, structural mapping, weak evidence | Candidate to investigate, not demonstrated ability |
| `probe_protocol` | Tasks, metrics, controls, acceptance criteria | Reusable experiment design |
| `evidence_bundle` | Outcomes, provenance, counterevidence | Evidence for independent review |
| `structural_component` | Reusable policy, graph, tool interface, procedure | Candidate component requiring recipient compatibility checks |
| `failure_pattern` | Negative transfer, invalid analogy, contamination | Constraint or warning; may guide future prospecting |
| `residual_question` | Open issue, unexplained discrepancy | Research question, not a positive result |
| `learning_update` | Versioned change to routing, memory, policy, evaluation | Candidate system improvement requiring attribution |
| `composite` | Explicit references to multiple typed units | Composition with no implicit claim promotion |

An SRU MAY contain several artifacts, but MUST declare a primary type and a manifest of embedded types. A composite MUST retain the distinct claim states of its constituents.

## 5. Canonical Structural Relay Unit Manifest

Every conforming SRU MUST include the following fields, either directly or through stable references:

| Field | Required meaning |
|---|---|
| `sru_id`, `schema_version`, `revision` | Stable identity and contract version |
| `unit_type`, `title`, `summary` | Type and bounded description |
| `producer`, `created_at` | Source actor and timestamp |
| `source_context` | Task, domain, environment, relevant constraints |
| `intended_recipients` | Intended audiences or recipient capability requirements |
| `claim_refs`, `claim_states` | Linked SPEC-001 claim identities and unchanged states |
| `opportunity_refs` | Linked SPEC-002 SOR identifiers, if applicable |
| `lifecycle_refs` | Linked SPEC-003 probe and decision identifiers, if applicable |
| `evidence_refs`, `counterevidence_refs` | Positive, negative, and contradictory evidence |
| `assumptions`, `limitations`, `known_failures` | Applicability restrictions and failure modes |
| `payload_manifest` | Artifact names, formats, content digests, access constraints |
| `provenance` | Parent SRUs, transformations, licenses, attribution |
| `reuse_policy` | Permitted uses, safety restrictions, human review conditions |
| `uncertainty` | Unresolved ambiguities and confidence qualification |

A manifest MUST NOT omit a known material counterexample merely because the package is intended for positive reuse. If evidence cannot be shared, the package MUST disclose the limitation rather than claim independent reproducibility.

## 6. Evidence Integrity and Claim-State Preservation

Evidence integrity is a first-class relay obligation. The source MUST preserve the distinction among **hypothesized**, **under probe**, **observed**, **replicated**, **contested**, and **retracted** claims, using the relevant SPEC-001 vocabulary and any finer project-specific states. A recipient MAY map these to local states only with a documented, non-inflating mapping.

For each relayed claim, a recipient SHOULD be able to answer: Who asserted it? Under which task and operating envelope? Which evidence supports it? Which evidence challenges it? What changed since the prior version? Was the observation independent of the training or discovery data? Which conditions remain untested?

Content digests SHOULD protect payload integrity, but cryptographic integrity alone does not establish truth. The contract distinguishes a trustworthy *chain of custody* from a trustworthy *scientific inference*.

Where a claim has been retracted, downstream relay indexes MUST surface the retraction and SHOULD notify known dependents. A recipient MUST NOT silently continue to present the superseded claim as current.

## 7. Provenance Graph, Versioning, and Lineage

An SRU is part of a directed provenance graph rather than an isolated document. Edges SHOULD be typed, including `derived_from`, `replicates`, `contradicts`, `adapts`, `combines`, `supersedes`, `retracts`, and `evaluated_against`.

A new relay revision MUST have a new revision identifier and MUST retain references to prior revisions. Changes to claim scope, evidence, metrics, or restrictions MUST be explicitly described. A recipient-side adaptation SHOULD create a child SRU rather than rewriting the source artifact.

The provenance graph MAY contain cycles in *research influence* (A informs B, B later informs A), but revision lineage MUST remain auditable: each published revision references already-existing predecessors. A graph edge that expresses intellectual influence MUST NOT be confused with an exact-copy lineage edge.

## 8. Sender and Recipient Responsibilities

The **sender** MUST supply a manifest, relevant limitations, access and reuse terms, known negative evidence, and stable evidence references. The sender SHOULD provide a minimal verification procedure and compatibility assumptions.

The **recipient** MUST validate the manifest's structural completeness, inspect scope and restrictions, assess applicability to its target context, and record an explicit decision. The recipient MUST NOT claim target-domain capability merely because source-domain evidence exists.

A recipient MAY reject an SRU for reasons of missing evidence, incompatible representation, governance constraints, licensing, cost, or unacceptable uncertainty. Such a rejection SHOULD be preserved as a relay outcome when doing so is permitted and useful.

## 9. Relay Lifecycle and State Machine

The proposed minimal lifecycle is:

`Prepared → Offered → Received → Inspected → {Rejected | Quarantined | Admitted} → {Adapted | Trialed} → Evaluated → {Not Useful | Useful | Contested} → {Archived | Integrated | Revised}`

`Quarantined` permits additional review but not operational integration. `Admitted` means the package is eligible for bounded experimentation, not that its capability is validated. `Integrated` requires documented compatibility and governance approval; where material claims are made, it also requires evidence appropriate to those claims.

Every state transition MUST record `event_id`, `actor`, `timestamp`, `prior_state`, `new_state`, `reason`, and relevant evidence or policy references. Implementations MAY use a richer state machine, provided it does not bypass source-claim restrictions or recipient authorization.

## 10. Three Independent Gates

The relay process SHOULD distinguish three independent decisions:

**Gate R1 — Transport and inspection.** Is the package structurally complete, traceable, and safe to receive? A positive R1 result says nothing about target utility.

**Gate R2 — Contextual trial.** Is a bounded experiment justified under the target operating envelope? The recipient checks structural compatibility, evidence quality, anticipated costs, risks, and an explicit test protocol. A positive R2 result is permission to test, not permission to deploy.

**Gate R3 — Integration and claim adoption.** Do target-side results justify the proposed operational use or capability claim, within the declared scope? R3 SHOULD include holdout evaluation, comparison to baseline, counterevidence review, and governance approval where relevant.

Gate decisions MUST remain separate. The SPEC-003 exploration and validation gates continue to govern research claims; R1–R3 address the additional cross-context relay obligations.

## 11. Spatial Relay, Temporal Relay, and Repetition

**Spatial relay** occurs when an artifact crosses actor, system, team, domain, or organization boundaries. It requires explicit sender/recipient identities and context transformation records.

**Temporal relay** occurs when observations or artifacts from an earlier execution inform a later one. It requires timestamps, revision references, and protection against silently reusing contaminated evaluation cases.

Repeated execution MAY be recorded as evidence relay even when no component parameters or structural policies change. For repeated trials to contribute to learning, their observations must be meaningfully accumulated, compared, and used to update a testable decision process. Repetition without an evidence or decision pathway is not, by itself, learning.

For repeated trials, a conforming record SHOULD identify the repeated protocol, changed conditions, independent variables, stopping rule, and whether results are independent or correlated. Counting correlated repeats as independent confirmations MUST be avoided.

## 12. Learning–Execution Decoupling and Attribution

A collective system may improve by updating routing, tool selection, memory, structural composition, validation rules, or task allocation while individual execution models remain unchanged. Such improvement SHOULD be labeled **system-level structural learning**, not automatically **unit-level learning**.

A learning update MUST identify its target layer: `unit`, `interaction`, `structure`, `relay`, `collective`, or `evolutionary`. Multiple layers MAY be affected, but attribution MUST be supported by evaluation or clearly marked as unresolved.

To substantiate durable growth, researchers SHOULD compare a baseline system with an otherwise matched updated system on held-out or future tasks, include cost and failure-rate measures, and verify persistence across multiple episodes. Ablations SHOULD distinguish gains from added compute, more tools, more data, changed prompts, better routing, and genuinely reusable structural changes.

A frozen-unit baseline is especially informative: if model weights stay fixed and the collective system improves, the result supports system-level adaptation under tested conditions. It does not demonstrate that the system has acquired arbitrary new general intelligence.

## 13. Collective Evidence Registry and Precedent Reuse

A collective learning registry SHOULD index SRUs by domain, task, structural features, evidence state, provenance, known failures, restrictions, and recipient-side outcomes. Search and retrieval MAY use exact matching, differential trees, metric-native directional scoring, structural similarity, or learned embeddings.

A registry MUST NOT rank research validity solely by popularity, number of citations, or relay frequency. It SHOULD permit retrieval of failed attempts and conflicting results alongside successful cases. It SHOULD expose whether a precedent is a source observation, an independent replication, or a derived interpretation.

When a precedent is reused, the new record SHOULD link the specific reusable component and explain the correspondence and residual mismatch between source and target contexts. This is essential to prevent superficially similar cases from being treated as equivalent.

## 14. Negative Results, Residuals, and Counterevidence Relay

Negative evidence is a first-class relay object. A failed probe can reveal a boundary, disconfirm a transfer mapping, identify a missing dependency, or expose an evaluation artifact. Such findings can improve future prospect selection even if no positive capability emerges.

A negative-result SRU SHOULD specify the original hypothesis, conditions, observed failure, alternative explanations, and limits of the negative inference. A failed test in one operating envelope MUST NOT be presented as proof of impossibility across all environments.

Residual questions SHOULD be retained with explicit unresolved status, proposed discriminating tests, and the evidence that motivated them. A residual is not a substitute for a claim. A future recipient MAY formulate a new prospect from a residual, but MUST create a distinct SOR and trace the originating uncertainty.

## 15. Directional Prospecting and Feedback to ISGFTR-008

Relay outcomes can supply evidence for the next prospecting cycle. A recipient's success, failure, rejection, adaptation cost, or novel mismatch may update a directional ranking model. Such updates SHOULD be based on traceable observations and MUST distinguish exploratory priority from calibrated success probability.

A possible cycle is:

`Prospect → Probe → Adjudicate → Package → Relay → Trial → Learn → New Prospect`

The cycle is a **research workflow**, not a claim that recursive iteration necessarily yields open-ended capability growth. Stagnation, negative transfer, evidence contamination, and rising coordination costs are legitimate outcomes that the registry must preserve.

## 16. Governance, Sovereignty, Privacy, and Access

An SRU MUST declare its reuse policy, including licenses where applicable, confidentiality restrictions, safety constraints, and any required human authorization. The ability to technically relay an artifact does not establish permission to use it.

Sensitive or proprietary evidence MAY be represented by redacted summaries or restricted references, but the package MUST mark what cannot be independently inspected. A recipient MUST NOT infer that withheld evidence has been independently validated.

Cross-organizational collective learning SHOULD respect participant sovereignty: a contributor retains authority over authorized disclosure and local deployment, subject to applicable agreements. A governance plane SHOULD support withdrawal notices, correction, dispute handling, and recipient-side opt-in.

For higher-risk settings, relay admission and integration SHOULD include domain-specific safety review. The present contract is not a substitute for regulatory or security controls.

## 17. Illustrative YAML Relay Package

The following example is illustrative and does not claim that the referenced experiments exist. It is not a formal JSON Schema.

```yaml
schema: ISGFTR-SPEC-004
schema_version: "1.0.0"
sru_id: "example:sru:route-transfer:001"
revision: 1
unit_type: evidence_bundle
title: "Exploratory routing transfer from domain A to domain B"
summary: "Candidate structural correspondence with mixed trial outcomes"
producer:
  actor_id: "example:research-team-a"
  role: "source"
created_at: "2026-10-30T00:00:00Z"
source_context:
  domain: "synthetic-domain-A"
  task: "select among bounded task routes"
  operating_envelope: "offline, synthetic, non-deployed"
intended_recipients:
  - "research groups evaluating synthetic-domain-B"
claim_refs:
  - "example:capability:route-selection:001"
claim_states:
  "example:capability:route-selection:001": "observed"
opportunity_refs:
  - "example:sor:cross-domain-route:001"
lifecycle_refs:
  - "example:probe:route-transfer:001"
evidence_refs:
  - "example:evidence:trial-summary:001"
counterevidence_refs:
  - "example:evidence:negative-transfer:002"
assumptions:
  - "route alternatives are explicitly enumerable"
limitations:
  - "not tested under live operational constraints"
known_failures:
  - "negative transfer on shifted cost distributions"
uncertainty:
  status: "unresolved cross-domain robustness"
  untested_conditions:
    - "larger candidate sets"
payload_manifest:
  - name: "trial-summary.md"
    format: "text/markdown"
    digest: "illustrative-placeholder-not-a-real-hash"
    access: "public-example"
provenance:
  parent_sru_ids: []
  transformations: []
  attribution: "illustrative example only"
reuse_policy:
  license: "Apache-2.0"
  deployment_allowed: false
  required_review: "recipient-side evaluation"
relay_events:
  - event_id: "example:relay:001"
    actor: "example:research-team-b"
    timestamp: "2026-10-30T01:00:00Z"
    prior_state: "Offered"
    new_state: "Received"
    reason: "candidate for controlled review"
recipient_outcome:
  state: "Inspected"
  target_claim_status: "not evaluated"
  durable_growth_claimed: false
```

In a real implementation, content digests MUST be computed from actual bytes, references MUST resolve to available records or explicitly state access limitations, and timestamps and actor identities MUST be verifiable to the extent required by the project.

## 18. Contract Invariants

A conforming implementation MUST satisfy the following invariants:

1. **Identity:** Every SRU has stable identity, schema version, and revision.
2. **Type clarity:** Every SRU declares its primary object type and does not conflate evidence with capability.
3. **Scope preservation:** A relayed claim retains its source task and operating envelope.
4. **No promotion by copying:** Relay cannot increase a claim's evidence status without new adjudicated evidence.
5. **Provenance:** Source, transformations, and parent references remain traceable.
6. **Counterevidence:** Known material counterevidence and negative transfer are linked or disclosed as inaccessible.
7. **Recipient autonomy:** Receipt and adoption are distinct, recorded decisions.
8. **Gate separation:** Transport, trial authorization, and integration are separately decided.
9. **Version integrity:** Material changes create new revisions with preserved lineage.
10. **Retraction propagation:** Known retractions are exposed to downstream users.
11. **Attribution:** Unit-level and system-level learning claims are distinguished.
12. **Outcome distinction:** Transmission, utility, and durable growth are separately measured.
13. **Access constraints:** Reuse respects declared permissions and confidentiality limits.
14. **Negative-result retention:** Failures and residuals can be represented without forced positive interpretation.
15. **Repeat dependence:** Correlated repeated observations are not misrepresented as independent replications.
16. **Uncertainty:** Unresolved assumptions and limits remain visible to recipients.

## 19. Illustrative Conformance Tests

The following tests are proposed checks, not evidence of an implemented validator.

| ID | Test input or situation | Expected behavior |
|---|---|---|
| `CT-001` | SRU missing `unit_type` | Reject as structurally incomplete |
| `CT-002` | SOR packaged as demonstrated capability | Reject claim promotion |
| `CT-003` | Source `observed`, recipient declares `replicated` without new test | Reject unsupported promotion |
| `CT-004` | Known negative result omitted from manifest | Flag or reject incomplete evidence |
| `CT-005` | Adapted payload overwrites source revision | Reject lineage violation |
| `CT-006` | Package digest differs from payload | Quarantine for integrity failure |
| `CT-007` | R1 receipt treated as deployment approval | Reject gate bypass |
| `CT-008` | Target domain differs but no compatibility analysis exists | Require bounded trial or reject |
| `CT-009` | Failed recipient trial recorded | Preserve negative outcome and provenance |
| `CT-010` | Repeated correlated trials counted as independent replications | Flag invalid evidence accounting |
| `CT-011` | Frozen-unit system improvement labeled model-weight learning | Reject attribution error |
| `CT-012` | Retraction issued for source evidence | Flag affected downstream SRUs |
| `CT-013` | Missing license or restrictive reuse policy | Hold integration pending authorization |
| `CT-014` | Redacted evidence described as fully independently verified | Reject misleading evidence claim |
| `CT-015` | New structural policy improves only one seen example | Do not certify durable growth |
| `CT-016` | Residual question relayed as a positive result | Reject type/claim mismatch |
| `CT-017` | Two valid SRUs combined without preserving their individual limits | Reject composite claim inflation |
| `CT-018` | Recipient rejects a technically valid but unsuitable SRU | Accept rejection and record reason |

Conformance tests SHOULD include positive, negative, and adversarial examples. Passing schema checks is necessary for interoperability but not sufficient for scientific validity.

## 20. Minimal MVP and Validation Roadmap

A small prototype can be built without a multi-agent runtime or model training:

**Phase 1 — Static records.** Implement machine-readable manifests for three SRU types: `opportunity`, `evidence_bundle`, and `failure_pattern`. Validate required fields and cross-references to SPEC-001–003.

**Phase 2 — Controlled handoff.** Use two synthetic research actors. Actor A packages a candidate transfer and both positive and negative observations; Actor B checks provenance, inspects constraints, and records admission or rejection.

**Phase 3 — Recipient-side probe.** Actor B registers a target-domain protocol, executes a baseline and a proposed transfer, and publishes a separate result. The source claim state remains unchanged; any target claim must reference the new evidence.

**Phase 4 — Temporal relay.** A later execution retrieves the prior failure pattern, revises the hypothesis, and records whether prospecting becomes more efficient or merely more conservative.

**Phase 5 — Collective learning evaluation.** Compare a registry-enabled research workflow with a no-registry baseline on held-out synthetic tasks. Report discovery yield, invalid claim rate, negative-transfer rate, human review effort, compute cost, and persistence of improvements.

A useful prototype should first demonstrate **auditability and honest failure handling**. It need not claim open-ended intelligence growth to be scientifically valuable.

## 21. Testable Research Hypotheses

**H-R1 — Provenance-aware relay.** Compared with unstructured handoffs, provenance-rich SRUs reduce unsupported claim promotion in blinded recipient reviews.

**H-R2 — Counterevidence retention.** Registries that preserve negative evidence reduce repeated selection of previously falsified transfer mappings, conditional on comparable task distributions.

**H-R3 — Explicit gates.** Separating receipt, trial, and integration reduces premature deployment decisions without prohibitive loss of legitimate discoveries.

**H-R4 — Temporal relay.** Versioned reuse of prior failure analyses improves later prospect-selection efficiency compared with retaining only successful cases.

**H-R5 — Frozen-unit collective learning.** A system with unchanged execution-model weights but an adaptive relay registry can show persistent held-out performance improvement relative to a matched frozen-registry control.

**H-R6 — Attribution discipline.** Explicit learning-layer labels improve agreement among independent evaluators on what changed and what capability is actually supported.

**H-R7 — Cost-sensitive relay.** Under some workload distributions, unrestricted relay increases coordination and verification cost more than task utility; bounded relay policies perform better.

Each hypothesis requires preregistered metrics, appropriate baselines, independent review where feasible, and published negative outcomes. Failure to confirm a hypothesis should update the proposed contract rather than be hidden.

## 22. Limits, Counterarguments, and Failure Modes

**Metadata overhead:** Detailed manifests may be too costly for trivial or short-lived artifacts. The contract SHOULD support lightweight profiles, but not by omitting critical evidence and restrictions.

**False precision:** Structured fields can make weak claims appear more authoritative. Validators MUST distinguish syntactic conformance from empirical support.

**Semantic mismatch:** Two systems can agree on a schema while disagreeing on task meanings, metric definitions, or acceptable risk. Recipient-side semantic checks remain necessary.

**Registry pollution:** Large-scale sharing can amplify low-quality, duplicated, or strategically manipulated evidence. Deduplication, independent evaluation, and reputation mechanisms MAY help, but reputation alone is not proof.

**Selection bias:** Only relaying success stories biases prospecting. Explicit failure records help, although complete reporting may be unattainable.

**Privacy and sovereignty:** Full reproducibility may conflict with confidentiality. The contract requires honest disclosure of access limits, not compulsory disclosure.

**Collective stagnation:** A shared registry can entrench existing assumptions and suppress novel hypotheses. Diversity of exploratory policies and periodic adversarial review SHOULD be considered.

**AGI extrapolation:** Better relay, structural learning, or cumulative research efficiency does not establish general intelligence. Any broader claim requires separate operational definitions and evidence.

## 23. Figure Placement and Research Interfaces

- **Fig-008 — Recursive Relay and Collective Intelligence Growth:** Recommended primary figure after Sections 9–12; show source and recipient SRUs, evidence feedback, temporal relay, and learning attribution.
- **Fig-006 — System-Centric Multi-Level Learning:** Useful after Section 12 to distinguish unit, structural, and collective learning layers.
- **Fig-007 — Spillover Prospecting and Capability Frontiers:** Useful after Section 15 to show how relay outcomes become new prospecting inputs.

This contract provides the formal interface for `ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md`, and should be exercised by `CASE-002-Minimal-System-Centric-Collective-Learning.md` and `CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md`. It is compatible in research intent with portable-unit and structural-relay directions explored in UIERU, SIF, and related work, but compatibility must be established through actual mappings rather than assumed from terminology.

## 24. Open Questions

1. What is the smallest SRU manifest that preserves scientific accountability without excessive overhead?
2. How should evidence quality be compared across different tasks, metrics, and evaluators?
3. Which provenance graph structures scale while remaining understandable to independent reviewers?
4. How can a registry prevent popularity or relay frequency from becoming a proxy for truth?
5. When does repeated evidence accumulation become genuine learning rather than improved bookkeeping?
6. How should partial access, confidential evidence, and independent replication coexist?
7. Which negative results are sufficiently transferable to guide a different domain?
8. How can collective systems detect when a previously useful precedent has become stale?
9. How should multi-level credit assignment be reported when unit and system improvements interact?
10. What conformance tests most effectively catch silent claim inflation by autonomous agents?
11. Can directional prospecting use relay histories without inheriting their selection biases?
12. Which empirical results would justify simplifying, replacing, or abandoning this proposed contract?

## 25. Conclusion and Open Research Invitation

Structural relay should transmit **what was done, what was observed, what remains uncertain, and what a recipient is authorized to infer**—not just an attractive result. A portable intelligence artifact becomes scientifically valuable when its scope, provenance, counterevidence, adaptations, and recipient outcomes remain inspectable across contexts and time. Collective learning can then be investigated as a testable system-level process, including cases where the execution units never update their model weights.

SPEC-004 completes the proposed four-part ISGFTR specification family: capability and boundary definitions; opportunity and evidence records; controlled prospecting and validation; and auditable relay with collective learning. The family is an **open research proposal**, not a validated standard. Contributions are welcome in the form of counterexamples, simpler schemas, negative results, independent replications, interoperability mappings, and carefully bounded implementations.

---

**Document status:** Proposed specification for open research discussion.  
**Intended repository location:** `specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md`  
**Research stance:** Theory-first; specifications and conformance before runtime; explicit uncertainty; counterevidence preservation; collective-learning-friendly.
