# ISGFTR Validation Roadmap

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document:** `VALIDATION-ROADMAP.md`  
**Version:** 1.0.0 — theory-first research plan  
**Status:** Proposed validation program; no experimental findings are asserted  
**Date:** 2026-10-31

## 1. Purpose and epistemic commitments

This roadmap converts the ISGFTR conceptual framework into a staged, auditable research program. Its purpose is not to demonstrate artificial general intelligence (AGI) by assertion, nor to imply that every proposed mechanism will work. It is to establish what would count as evidence for or against the claims that intelligence may spill over beyond a narrow observed task boundary; that structural generalization and selective transfer may improve capability reuse; and that systems may learn through changing their organization, memory, and relay practices even when component model weights remain fixed.

A useful outcome may be a positive finding, a negative finding, a narrower claim, an improved measurement protocol, or a reusable counterexample. Exploratory scores are **not** calibrated probabilities of success unless independently calibrated. Transfer is not automatically useful; useful transfer is not automatically durable learning; durable system learning is not proof of AGI.

The program follows four commitments:

- **Specifications before implementation:** establish the object contracts, scope of claims, and conformance checks before using results to support a theory.
- **Controlled comparisons:** compare each proposed mechanism against plausible simpler explanations, including retrieval, prompting, task overlap, extra compute, and selection bias.
- **Preserved negative evidence:** retain failures, rejected prospects, mismatches, uncertainty, and adverse outcomes in the same evidence system as successes.
- **Collective reproducibility:** make methods, evaluation criteria, data provenance, versions, and resource budgets available to independent investigators where permitted.

## 2. Research questions and validation axes

| Axis | Central question | Primary observable | Key alternative explanation |
|---|---|---|---|
| Capability boundaries | Do observed, reachable, and evolvable capability estimates differ meaningfully? | Performance under prespecified changes in tools, structure, and learning policy | Benchmark undercoverage or hidden prior knowledge |
| Spillover | Can capability appear in a target task outside the original observed scope? | Held-out target success and robustness | Training contamination, task similarity, prompt leakage |
| Folding–generalization | Does an explicit shared structural core improve transfer? | Out-of-domain gain versus matched controls | Longer prompts or extra supervision |
| Fluidity and permeability | Can context-dependent gates improve safe transfer? | Utility, negative transfer, and cost across changing contexts | Hand-tuned static policy |
| Directional prospecting | Does weak-evidence guidance discover useful probes more efficiently? | Validated discoveries per budget | Candidate pool bias or hindsight scoring |
| Structural relay | Can portable evidence and structures improve later investigations? | Replication, adaptation, and preserved provenance | Simple copying or shared benchmark answers |
| System-centric learning | Can frozen components support durable system improvement? | Longitudinal gain after controller/memory updates | Hidden parameter updates or test-set memorization |
| Recursive growth | Does learning improve the *future process of learning*? | Prospective gain on novel tasks across rounds | Accumulating compute, data, or easier tasks |

These axes may interact but should be tested separately before interpreting combined effects.

## 3. Canonical experimental objects and interfaces

Every experiment should use versioned identifiers and explicit links between:

1. **Capability Profile:** actor/system identity, task distribution, allowed resources, evidence, and scoped boundary claims (`SPEC-001`).
2. **Spillover Opportunity Record:** source, target, hypothesized transfer mechanism, directional evidence, uncertainty, and potential negative transfer (`SPEC-002`).
3. **Probe Protocol and Lifecycle Record:** prespecified conditions, controls, metrics, stopping rules, authorization, observations, and adjudication (`SPEC-003`).
4. **Structural Relay Unit:** portable artifacts, provenance, successful and failed conditions, adaptations, and unresolved residuals (`SPEC-004`).

A claim should remain linked to its evidence and its counterevidence. Receiving a relay package does not automatically authorize adopting or deploying it. Conformance failures should be reported separately from hypothesis outcomes.

## 4. Phase 0 — Definitions, conformance, and measurement readiness

**Objective:** establish a common language and prevent apparent experimental gains from being produced by inconsistent definitions.

**Activities:**

- Freeze a dated protocol version and operational definitions of spillover, generalization, fluidity, transfer, relay, and durable growth.
- Specify the unit of analysis: model, agent, tool chain, organization, or system; distinguish unit-level and system-level attribution.
- Define task distributions, train/development/test partitions, target-domain novelty criteria, and prohibited information flows.
- Implement schema checks for `SPEC-001` through `SPEC-004`; test missing evidence, invalid claim transitions, orphaned provenance, and unauthorized deployment transitions.
- Establish baselines for quality, cost, latency, reliability, negative transfer, and reproducibility.
- Register anticipated confounds, data leakage checks, and failure reporting templates.

**Exit criteria:** protocol and schema version pinned; measurement scripts independently checked on synthetic positive and negative cases; all critical conformance tests pass; evaluation datasets held out from adaptation.

**Deliverables:** glossary lock, protocol registry, conformance report, baseline definitions, risk register, and a machine-readable manifest.

## 5. Phase 1 — Capability boundary and spillover baselines

**Objective:** test whether capability estimates change under controlled access to structural scaffolding and resources without conflating such changes with intrinsic model learning.

**Design:** evaluate frozen models on predeclared source and target tasks. Compare direct task execution, task-specific instructions, generic prompting, structural representations, and resource-matched tool access. Use distinct target domains and difficulty strata; report full task distributions rather than cherry-picked examples.

**Measurements:** task success, calibration where appropriate, error classes, cost per correct result, sensitivity to paraphrase and perturbation, and the difference between observed and reachable performance under specified conditions.

**Critical controls:** equal token/computation budgets where feasible; matched examples; randomized order; blinded evaluation; contamination audits; held-out tasks not used to design the transfer mapping.

**Exit criteria:** repeatable baseline estimates with uncertainty intervals and a documented account of whether apparent spillover survives leakage and resource-matching controls.

**Deliverables:** boundary profiles, source–target task matrix, negative examples, and baseline report.

**Primary case:** [CASE-001](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md).

## 6. Phase 2 — Folding, structural reuse, and transfer

**Objective:** evaluate whether an explicit reusable structural core and a preserved residual improve transfer beyond generic examples or longer instructions.

**Design:** compare at least these conditions: (A) direct baseline, (B) generic instruction, (C) irrelevant-domain analogy, (D) source example only, (E) shared-core representation, (F) shared core plus target residual, and (G) shared core plus explicit uncertainty recovery. Include deliberately false analogies.

**Measurements:** target-domain success, transfer gain, negative transfer frequency, robustness to altered domain-specific constraints, annotation burden, and representation cost.

**Decision logic:** a structural reuse claim requires improvement against matched controls on held-out target tasks. If residual preservation improves robustness, report that separately from a claim that folding alone is beneficial. If performance falls under target-domain shift, narrow the supported transfer scope.

**Exit criteria:** at least one independently repeated comparison with confidence intervals and a catalog of failure modes; null results are valid completion outcomes.

**Deliverables:** transfer mappings, residual registry, ablation results, and reproducible evaluation package.

## 7. Phase 3 — Weak-evidence prospecting and directional intuition

**Objective:** determine whether prospective directional signals improve the discovery of valid transfer opportunities per unit exploration budget.

**Design:** construct a candidate pool *before* outcomes are known. Compare random selection, surface similarity, exact structural matching, historical precedent retrieval, directional weak-evidence scoring, and residual-aware scoring. Randomize or stratify candidate assignment and keep the evaluator blind to ranking method where possible.

**Primary endpoint:** number of independently validated useful transfers per fixed cost or probe budget. Secondary endpoints include precision at k, coverage, time to discovery, information gain, false-positive burden, and rate of informative negative results.

**Critical protections:** freeze ranking before probing; prevent leakage of outcomes into scoring; report all screened candidates, not only successful ones; distinguish heuristic scores from calibrated probabilities; evaluate the marginal value of each evidence source through ablations.

**Exit criteria:** a prospecting method must outperform appropriate baselines under comparable budgets in at least one held-out candidate distribution before any general efficiency claim is made. A null or negative result should trigger re-examination of scoring features, not post hoc relabeling of success.

**Deliverables:** ranked candidate manifests, probe logs, validated/rejected opportunity records, cost accounting, and evidence relay packages.

**Primary case:** [CASE-003](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md).

## 8. Phase 4 — Selective permeability and adaptive boundary policies

**Objective:** test whether a learned, context-dependent boundary policy can outperform static policies without increasing unacceptable risk.

**Design:** separate permissions to **observe**, **probe**, **adopt**, and **deploy**. Compare closed boundaries, fully permissive boundaries in safe sandbox conditions, fixed hand-authored selective policies, and adaptive policies learned only from training-period evidence. Deploy permissions remain subject to independent authorization and cannot be self-granted by the exploration controller.

**Measurements:** utility under distribution shift, negative transfer, false admission/rejection, cost, policy stability, policy-change auditability, and recovery after a misleading evidence sequence.

**Safety and governance tests:** adversarial examples, contaminated relay packages, misleading analogies, conflicting evidence, and deliberate attempts to promote exploratory evidence into deployment authority.

**Exit criteria:** any claimed benefit must be measured on unseen contexts with fixed resource budgets and no critical permission-boundary violations. Unsafe outcomes block deployment claims even if exploratory utility rises.

**Deliverables:** policy traces, boundary decision records, safety test report, and failure/rollback documentation.

**Related extensions:** [EXT-001](extensions/EXT-001-Biomimetic-Fluidity-and-Selective-Permeability.md), [EXT-002](extensions/EXT-002-Learning-the-Boundaries-of-Intelligence-Flow.md).

## 9. Phase 5 — Frozen-unit system-centric learning

**Objective:** isolate persistent system-level learning from improvements due solely to combining capable units.

**Minimal architecture:** three to five fixed-capability execution units, a task router, a structural memory/evidence registry, a verifier, and a controller whose structural policy may change between rounds. Freeze component weights and record hashes or equivalent version identifiers throughout.

**Comparison arms:** single unit, fixed pipeline, random routing, static ensemble, retrieval-only memory, adaptive routing without persistent memory, adaptive routing with structural memory, and full evidence-aware relay. Match compute and access to training information where possible.

**Longitudinal design:** divide tasks into sequential rounds, with fresh held-out tasks in each round. Test retention after a delay and generalization to a new task family. Include ablations that remove memory, policy adaptation, and negative-evidence access separately.

**Measurements:** held-out performance over time, learning-curve slope, transfer retention, resource-normalized gain, coordination overhead, negative transfer, and attribution to system components.

**Exit criteria:** durable system learning requires a reproducible prospective improvement on fresh tasks after structural updates, relative to matched frozen-system controls. Better one-time orchestration is not sufficient.

**Deliverables:** fixed-unit manifests, policy histories, longitudinal evaluation, attribution ablations, and replication kit.

**Primary case:** [CASE-002](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md).

## 10. Phase 6 — Spatial, temporal, and recursive relay

**Objective:** determine whether reusable relay artifacts improve subsequent investigations and whether recursive feedback improves future learning efficiency.

**Design:** compare no relay, raw transcript relay, successful-results-only relay, full provenance/evidence relay, and relay including failures and unresolved residuals. Test across different agents, teams, and time periods. Use independent recipients who did not participate in producing the source artifact.

**Endpoints:** replication fidelity, adaptation cost, preservation of limitations, time to independently validated result, and future discovery rate under a fixed budget. Track error propagation and version conflicts.

**Recursive-growth criterion:** a later generation must demonstrate better *learning or prospecting performance on new problems*, not merely better task performance from a larger cache of previous answers. Control for accumulated compute, data, and tool availability.

**Exit criteria:** evidence that a relay mechanism improves at least one prospective downstream metric, with transparent costs and error rates. Open-ended growth remains unproven unless gains persist across substantially novel tasks and multiple rounds.

**Deliverables:** versioned Structural Relay Units, provenance graphs, negative-result registry, independent reproduction reports, and longitudinal growth analysis.

## 11. Phase 7 — Cross-domain and independent replication

**Objective:** establish external validity and identify the boundaries of any positive result.

**Activities:**

- Invite independent researchers to reproduce a locked protocol without private design guidance.
- Replicate on distinct task domains, model families, and execution environments.
- Publish both aggregate outcomes and disaggregated failure cases.
- Perform sensitivity analyses for budgets, baseline strength, candidate pool composition, evaluator choice, and domain novelty.
- Reconcile conflicting results without suppressing them; revise capability scopes and confidence statements as necessary.

**Exit criteria:** the claim either survives credible independent tests within a defined scope or is explicitly revised, contested, or retracted. A failed replication is a substantive result, not a process failure.

**Deliverables:** replication matrix, discrepancy log, revised claims, and versioned follow-up research questions.

## 12. Hypothesis-to-experiment traceability

The canonical hypothesis identifiers and exact formulations belong in [TESTABLE-HYPOTHESES.md](TESTABLE-HYPOTHESES.md). Rather than duplicate or silently renumber them, this roadmap maps **hypothesis families** to validation phases:

| Hypothesis family | Primary phases | Main falsification pressure |
|---|---|---|
| Boundary differentiation and spillover | 1, 7 | Gains disappear under leakage/resource controls |
| Folding and structural generalization | 2, 7 | No gain over matched generic guidance |
| Directional weak-evidence prospecting | 3, 7 | No improvement per fixed exploration budget |
| Selective permeability and flow policy | 4, 7 | Increased negative transfer or policy violations |
| Structural relay and evidence reuse | 6, 7 | No prospective downstream improvement |
| Frozen-unit system learning | 5, 7 | Gains explained by static composition or memorization |
| Recursive and evolvable growth | 6, 7 | Learning efficiency fails to improve on novel tasks |
| AGI-related interpretations | Across all | No evidence of sufficiently broad, robust generality |

Each experiment registration should include the exact hypothesis ID(s), not merely the family label.

## 13. Statistical and methodological safeguards

**Pre-registration.** Declare primary outcomes, controls, exclusion rules, analysis methods, and stopping criteria before observing final test results. Label post hoc analyses as exploratory.

**Uncertainty.** Report confidence or credible intervals appropriate to the design, effect sizes, sample counts, and the number of task families. Do not equate statistical significance with practical value.

**Multiplicity.** For large candidate pools and many endpoints, use prespecified multiple-testing controls or explicitly frame results as exploratory discovery requiring replication.

**Paired evaluation.** Prefer matched task instances and repeated independent seeds when stochastic systems are compared. Track run-to-run variance and evaluator disagreements.

**Contamination.** Maintain provenance for datasets, prompts, retrieved material, model versions, and candidate generation. Audit test-set exposure and unintended reuse of target answers.

**Cost parity.** Compare methods under equivalent or transparently accounted budgets; include tokens, tool calls, latency, human effort, compute, and failure recovery.

**Negative controls.** Include unrelated analogies, corrupted relay artifacts, and intentionally invalid transfer mappings to measure susceptibility to spurious success.

**Adverse results.** Preserve and report regressions, safety violations, invalid claims, and counterexamples, including those that are inconvenient for the preferred theory.

## 14. Evidence grading and claim adjudication

Use descriptive, non-probabilistic evidence grades unless calibration has been demonstrated:

| Grade | Meaning | Permissible statement |
|---|---|---|
| E0 — Conceptual | Mechanism proposed without an empirical probe | “A hypothesis is proposed” |
| E1 — Exploratory | Preliminary or uncontrolled observations | “An exploratory signal was observed” |
| E2 — Controlled | Prespecified controlled study supports a scoped effect | “The effect was supported under these conditions” |
| E3 — Replicated | Independent replication within a defined scope | “The scoped effect has independent support” |
| E4 — Generalized | Repeated support across distinct domains and settings | “Evidence supports broader, but still bounded, applicability” |

These grades are a proposed research convention, **not** an established universal standard. Counterevidence, methodological defects, or new information can downgrade or retract a claim at any time. A grade does not authorize deployment.

## 15. Stop, revise, and rollback conditions

Stop or revise a study when: critical provenance is missing; evaluation leakage is discovered; permission boundaries are violated; the primary outcome is no longer interpretable; the candidate pool was modified after outcomes were observed without disclosure; or risk exceeds the approved sandbox limits.

A mechanism should be narrowed or abandoned when repeated well-controlled experiments show no advantage over simpler alternatives, or when its negative-transfer burden outweighs its demonstrated benefit. Report such outcomes and relay the informative failure conditions.

## 16. Suggested minimal implementation sequence

A lightweight, contract-first program can begin without a full autonomous runtime:

1. **Registry first:** structured records for capability, prospect, protocol, evidence, and relay, with stable IDs and immutable result references.
2. **One narrow transfer benchmark:** a source/target task pair with a clean held-out evaluation and strong baselines.
3. **One prospecting comparison:** random selection versus structural and weak-evidence ranking at the same probe budget.
4. **One frozen-unit study:** a small collection of fixed agents with static and adaptive routing controls.
5. **One independent relay test:** a second investigator uses the evidence package to reproduce or refute a result.

Only expand complexity when the preceding phase yields interpretable evidence. Avoid building a large architecture that makes causal attribution impossible.

## 17. Deliverable manifest and publication checkpoints

For each phase, maintain:

- `protocol.md` or equivalent, with date, authorship, hypothesis IDs, and preregistered outcomes;
- `manifest.yaml` with software/model versions, task splits, resources, and provenance;
- conformance results against applicable SPEC contracts;
- baseline and intervention outputs, including all excluded runs with reasons;
- a negative-evidence and residual register;
- analysis code or reproducible procedures where legally and technically possible;
- a claim-adjudication note specifying evidence grade, scope, uncertainty, and limitations;
- a relay package for future independent researchers.

For **v1.0.0**, publication of this roadmap and the theory/specification documents is a **research proposal release**, not a completed empirical validation milestone. Any future empirical release should identify the phase, protocol version, dataset provenance, and replication status explicitly.

## 18. Governance, ethics, and scope of AGI conclusions

The program should be conducted in authorized, bounded experimental environments. Exploratory permeability must not bypass data access controls, privacy obligations, deployment review, or human governance. System-level optimization can create coordination failures and misleadingly strong aggregate results; evaluation should include worst-case and subgroup/task-family failures, not only mean scores.

Even a successful sequence of experiments would support particular claims about transfer, prospecting, relay, and system learning. It would **not by itself establish AGI**, unlimited scalability, consciousness, autonomy, or inevitable open-ended improvement. Model-centric, system-centric, and hybrid explanations should remain open to comparison.

## 19. Collective learning invitation

Researchers are invited to contribute rigorous replications, counterexamples, alternative metrics, simplified baselines, and formal analyses. Especially valuable contributions include demonstrations that a claimed gain is explained by a confound; studies that identify when weak-evidence prospecting fails; and evidence that a simpler architecture matches a proposed system. Such contributions improve the research frontier even when they weaken an original hypothesis.

The intended loop is:

**Question → Prospect → Protocol → Probe → Evidence → Adjudication → Relay → Revised Question.**

A successful collective-learning program should make claims easier to challenge and reproduce, not merely easier to propagate.

## 20. Related ISGFTR documents

- [README.md](README.md) and [START-HERE.md](START-HERE.md) — project orientation.
- [OPEN-QUESTIONS.md](OPEN-QUESTIONS.md) — unresolved research questions.
- [TESTABLE-HYPOTHESES.md](TESTABLE-HYPOTHESES.md) — canonical hypothesis formulations.
- [FUTURE-DIRECTIONS.md](FUTURE-DIRECTIONS.md) — longer-term research directions.
- [ISGFTR-008](docs/ISGFTR-008-Intelligence-Spillover-and-Transfer-Prospecting.md) — prospecting mechanisms.
- [ISGFTR-009](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md) — limits and counterarguments.
- [ISGFTR-010](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md) — research architecture.
- [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md), [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md), [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md), and [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md) — canonical contracts.
- [CASE-001](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md), [CASE-002](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md), and [CASE-003](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md) — candidate experimental settings.

---

**Research status:** Open, directional, falsifiable. This roadmap proposes a validation process; it does not report completed experimental evidence.  
**Release philosophy:** Theory first; conformance before runtime; preserve counterevidence; invite collective learning.
