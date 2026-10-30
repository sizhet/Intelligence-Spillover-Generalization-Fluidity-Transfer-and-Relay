# Future Directions — Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Version:** 1.0.0 (theory-first)  
**Status:** Open research agenda; proposals and hypotheses, not demonstrated capabilities  
**Date:** 2026-10-30  
**License:** Apache-2.0 (repository preference; see `LICENSE` for the governing terms)

> **Research stance:** Explore widely, validate carefully, preserve counterevidence, and relay both successes and failures. Neither intelligence spillover nor recursive relay establishes artificial general intelligence (AGI).

## 1. Purpose and Scope

This document identifies research directions that could transform ISGFTR from a conceptual framework into an empirically grounded, interoperable research program. It prioritizes **discriminating experiments**, explicit contracts, and reusable evidence over speculative capability claims. It is intended for independent investigators, systems engineers, cognitive scientists, and collaborators who may challenge or refine the framework.

The central research question is not simply whether intelligence can move across tasks or systems. It is **under which conditions a capability can be discovered, transferred, verified, retained, and used to improve future learning**, and whether those effects survive rigorous baselines and distribution shifts.

The agenda draws on the ten ISGFTR papers, four specifications, three illustrative cases, and three extensions. Suggested priorities are provisional and may change as evidence accumulates.

## 2. Research Map and Priorities

| Track | Key question | Initial deliverable | Priority | Main references |
|---|---|---|---|---|
| D1. Capability boundaries | How can observed, reachable, generative, and evolvable boundaries be estimated without conflation? | Versioned capability-boundary registry | High | ISGFTR-001, SPEC-001 |
| D2. Folding and reuse | When does a shared structural core improve out-of-domain transfer? | Controlled folding/unfolding benchmark | High | ISGFTR-003, CASE-001 |
| D3. Directional prospecting | Can weak evidence find valuable transfer opportunities more efficiently than simple baselines? | Budgeted prospecting benchmark | High | ISGFTR-005, ISGFTR-008, CASE-003 |
| D4. Adaptive permeability | Can a system learn when to admit, test, reject, or adopt external structures? | Boundary-policy ablation suite | High | ISGFTR-004, EXT-001, EXT-002 |
| D5. Frozen-unit learning | Can fixed execution units support durable system-level learning? | Reproducible multi-unit study | High | ISGFTR-006, CASE-002 |
| D6. Recursive relay | When does evidence relay improve future discovery rather than merely accumulate records? | Longitudinal relay experiment | High | ISGFTR-007, SPEC-004 |
| D7. Transfer governance | How can permission, evidence, and provenance survive cross-system transfer? | Conformance tests and audit logs | High | SPEC-001–004 |
| D8. Open-ended potential | Does a system expand its future reachable capability set, and how could this be tested? | Pre-registered longitudinal protocol | Exploratory | ISGFTR-009, EXT-003 |

**Priority** indicates recommended sequencing, not a claim of importance or probability of success. Tracks D1–D7 can proceed without adopting any AGI thesis.

## 3. D1 — Empirical Capability Boundaries

### 3.1 From metaphors to scoped claims

The four proposed boundary types should be represented as **context-dependent evidence claims**, not as four nested circles of fixed size:

- **Generative boundary:** candidate outputs or behaviors that the system can produce under specified generation procedures.
- **Observed boundary:** behaviors actually measured under specified tests.
- **Reachable boundary:** behaviors accessible with a defined budget of tools, scaffolding, search, and coordination.
- **Evolvable boundary:** changes in future reachability that a specified learning or structural-update process might induce over time.

Their relationships are not automatically nested: observation depends on sampling and evaluation; reachability depends on tools and resources; evolution depends on update rules and time. An experiment must state its operational definition before measuring any boundary.

### 3.2 Research tasks

1. Develop a **Capability Boundary Profile** recording subject, model or system version, task family, resources, environment, evaluator, uncertainty, and provenance.
2. Measure how estimated boundaries change when tool access, search budget, memory, or coordination policies vary while model weights remain fixed.
3. Compare independent evaluators and test for evaluator drift, hidden task leakage, and unstable thresholds.
4. Register both **expansions and contractions** of observed reachability after system changes.

**Discriminating result:** A reproducible change in reachable performance under controlled resource conditions would support a system-level accessibility claim; it would not alone prove that the underlying model acquired an intrinsic new ability.

## 4. D2 — Folding–Generalization Duality and Structural Reuse

### 4.1 The hypothesis

A representation that preserves a transferable **shared structural core** while explicitly retaining task-specific **residuals** may improve cross-domain performance compared with direct prompting, generic abstraction, or superficial similarity matching.

A possible decomposition is:

\[
X_d \longrightarrow (C,\Delta_d,U_d),
\]

where \(X_d\) is a domain-specific task representation, \(C\) a proposed reusable core, \(\Delta_d\) a domain-specific residual, and \(U_d\) a description of unresolved uncertainty. This is a conceptual interface, not a proven canonical decomposition.

### 4.2 Experiment families

- **Core fidelity:** Test whether essential constraints survive folding.
- **Residual sensitivity:** Remove or corrupt residual information to quantify negative transfer.
- **Uncertainty recovery:** Compare uncertainty retained during folding with uncertainty reconstructed using later evidence.
- **Unfolding quality:** Measure adaptation to a genuinely new target domain without giving the target answer in the abstraction.
- **Cost-aware reuse:** Compare accuracy, calibration, runtime, tokens, human effort, and error severity.

Baselines should include direct solutions, no-transfer controls, generic templates, similarity retrieval, and randomly paired source domains. Use held-out domains and pre-specified evaluation rubrics.

**Failure condition:** If folded representations consistently underperform strong baselines, or if apparent gains disappear after leakage controls, narrow or reject the claimed duality for those task families.

## 5. D3 — Directional Intuition and Capability Prospecting

The prospecting program should investigate **discovery efficiency**, not merely eventual task success. A useful system may rank speculative cross-domain opportunities before expensive experiments, but the ranking must not be presented as a calibrated probability without independent calibration.

### 5.1 Candidate signals

Candidate features include structural overlap, historical precedents, perspective-dependent distance, metric-native directionality, weak counterevidence, residual novelty, expected information value, and test cost. These features are **hypotheses about useful predictors** and should be individually ablated.

### 5.2 Budgeted evaluation

Under a fixed exploration budget \(B\), compare selection policies on:

- Verified useful transfers per unit cost;
- Time to first independently validated transfer;
- Negative-transfer rate and severity;
- Calibration and ranking stability;
- Diversity of discovered opportunities;
- Information gained from failed probes;
- Generalization to unseen task families.

Suggested baselines: random search, lexical similarity, embedding similarity, human-curated heuristics, structural-only scoring, and full weak-evidence scoring.

### 5.3 Prospecting loop

**Prospect → Admit → Probe → Validate → Relay → Learn → Re-prospect.**

Every candidate should have a durable identifier, scope, proposed transfer mechanism, alternative explanations, explicit disconfirmation criteria, budget, and evidence links. A candidate that fails validation remains valuable as negative evidence if it is well documented.

## 6. D4 — Learning Selective Structural Permeability

**Selective permeability** asks which external structures a system should observe, explore, adopt, or deploy. These are different permissions:

| Permission | Meaning | Minimum evidence expectation |
|---|---|---|
| Observe | Inspect a candidate structure | Provenance and basic safety checks |
| Probe | Test in a bounded environment | Explicit hypothesis, budget, stop conditions |
| Adopt | Incorporate into a reusable workflow | Scoped validation and rollback plan |
| Deploy | Permit operational use | Separate authorization and deployment-specific controls |

The boundary policy may adapt from outcomes, but **policy learning must not grant itself broader operational authority**. Human or institutional governance remains a separate control plane.

### 6.1 Experimental comparisons

Compare fixed-closed, fixed-open, manually gated, heuristic-gated, and evidence-adaptive policies. Hold task distribution and execution budget constant where feasible. Include adversarial examples, out-of-domain analogies, stale precedents, and conflicting evidence.

### 6.2 Measurements

Measure transfer utility, false admissions, missed opportunities, rollback frequency, auditability, human review burden, and policy stability under distribution shift. Explicitly examine whether a learned boundary merely overfits historical approval decisions.

**Failure condition:** If adaptive gating increases contamination or negative transfer without measurable discovery gains, prefer a simpler or more restrictive policy.

## 7. D5 — System-Centric Learning with Frozen Execution Units

One of the clearest falsifiable paths is to test whether **fixed-weight execution units** can participate in a system that learns through changes in memory, routing, workflow structure, evaluation, and coordination.

### 7.1 Minimal architecture

A candidate system contains:

1. Several limited execution units with frozen weights and documented capabilities;
2. A task decomposition and routing layer;
3. An evaluator with independent test data;
4. A versioned structural-memory and precedent registry;
5. A controller that proposes bounded updates to routing or composition;
6. A governance layer that approves updates and records their provenance.

### 7.2 Causal baselines

Compare single-unit execution, static pipelines, random routing, retrieval-only memory, adaptive routing, adaptive composition, and full structural learning. Apply memory resets and frozen-policy tests to isolate where gains originate.

**Primary endpoint:** sustained improvement on held-out future tasks after a controlled learning phase, measured under matched compute and tool budgets.

**Attribution rule:** A better system outcome does not imply any component's model weights learned. Report unit-level, interaction-level, and system-level effects separately.

## 8. D6 — Recursive Relay and Longitudinal Evidence Learning

Relay is not one event. It may involve passing a method between units, accumulating repeated execution traces over time, transmitting counterexamples, or adapting a structure for a new environment.

A minimal relay record should distinguish:

- **Transmission:** Was the artifact delivered intact?
- **Interpretation:** Was its meaning correctly understood?
- **Adoption:** Was it actually incorporated into a workflow?
- **Utility:** Did it help on a defined evaluation?
- **Durability:** Did benefits persist across later tasks or conditions?
- **Growth:** Did the system's ability to discover or learn future capabilities improve?

These stages must not be treated as equivalent.

### 8.1 Repetition as evidence relay

Repeated execution can accumulate useful traces, including failures, but repetition without analysis or memory is not learning. Compare identical repeated trials with and without evidence capture, evaluation, precedent updates, and later retrieval.

### 8.2 Recursive experiments

Run multi-round studies with pre-registered update windows, held-out test sets, periodic policy freezes, and controlled resets. Record error propagation, evidence contamination, strategy churn, and storage/coordination cost.

**Discriminating result:** Improvement in future discovery efficiency after previous relay cycles, beyond what a static archive or increased compute budget explains, would support a narrow recursive-learning claim.

## 9. D7 — Contracts, Provenance, and Independent Conformance

The four specifications should evolve toward **machine-checkable contracts** without prematurely presenting the conceptual YAML examples as final schemas.

| Specification | Next engineering deliverable | Critical invariant |
|---|---|---|
| [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md) | Capability profile schema and validator | Every capability claim has a scope and attributable evidence |
| [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md) | Opportunity and evidence-bundle schemas | Prospecting scores are not automatically success probabilities |
| [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md) | State machine and transition tests | Exploration admission cannot substitute for validation |
| [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md) | Relay unit schema and provenance graph | Transmission cannot be promoted directly to durable growth |

### 9.1 Conformance priorities

- Immutable or append-only experiment provenance;
- Explicit versioning of task definitions, evaluation criteria, and artifacts;
- Separate positive evidence, negative evidence, and unresolved claims;
- Reproducible state transitions with authorization checks;
- Counterevidence-triggered review or claim downgrades;
- Cross-team portability tests and schema evolution rules;
- Clear distinction between *syntactic conformance* and *empirical validity*.

A record that conforms to a schema is not thereby scientifically correct.

## 10. D8 — Evolvable Potential and Open-Ended AGI: A Cautious Program

This track should begin only after narrower mechanisms have been independently tested. The **evolvable boundary** concerns possible future reachability under a specified adaptation process; it is not an observable universal ceiling or proof of unlimited growth.

Three separate hypotheses deserve testing:

1. **Performance growth:** A system improves on a defined task distribution.
2. **Reachability growth:** A system reliably accesses task classes that were previously inaccessible under matched conditions.
3. **Learning-process growth:** A system becomes better at discovering, validating, and retaining *future* capabilities.

Even the third result would not establish AGI. Stronger claims require broad transfer, robust autonomy under appropriate oversight, sustained reliability, calibrated uncertainty, and carefully designed cross-domain evaluations.

### 10.1 Counterarguments to investigate

- Apparent novelty may be interpolation or benchmark contamination.
- Larger orchestration systems may merely trade cost for performance.
- A static collection of tools may simulate learning without persistent adaptation.
- Cross-domain gains may rely on hidden human expertise or hand-designed scaffolding.
- Recursive loops may amplify errors, reward hacking, or evaluator weaknesses.
- Open-ended search may be bounded by finite resources, representations, or governance constraints.
- Biological metaphors may be misleading at algorithmic or causal levels.

The research program should publish findings that contradict its motivating hypotheses.

## 11. Cross-Cutting Measurement and Statistical Discipline

Across all tracks, prefer **pre-registered primary endpoints**, held-out evaluation tasks, fixed resource budgets, multiple random seeds where appropriate, and independent replication. Report confidence intervals or uncertainty estimates alongside point estimates. Avoid treating repeated trials on correlated tasks as independent observations.

Minimum recommended measures include:

| Dimension | Example operational measure | Common confound |
|---|---|---|
| Transfer success | Held-out task success under a scoped rubric | Prompt leakage or evaluator drift |
| Discovery efficiency | Validated opportunities per exploration cost | Unequal search budgets |
| Negative transfer | Performance decline relative to no-transfer baseline | Unequal task difficulty |
| Structural durability | Retained benefit after policy freeze and delay | Persistent hidden memory |
| Learning attribution | Change with fixed execution weights | Uncontrolled tools or external data |
| Relay fidelity | Reproduction of source claims and constraints | Missing provenance |
| Calibration | Agreement of forecasts with observed outcomes | Uncalibrated directional scores |
| Governance | Unauthorized transition rate | Incomplete event logging |

Distinguish **exploratory findings** from **confirmatory evidence** in every report. Report both gains and losses, including resource overhead.

## 12. Research Infrastructure and Shared Artifacts

An open collective-learning ecosystem could maintain:

- **Capability Registry:** scoped, versioned capability profiles and evaluations;
- **Opportunity Registry:** proposed transfers, hypotheses, costs, and statuses;
- **Evidence Registry:** raw results, evaluator versions, negative findings, and replications;
- **Structural Relay Registry:** reusable procedures, mappings, residuals, and adaptation histories;
- **Precedent and Counterexample Registry:** prior successes, failures, and known boundary violations;
- **Conformance Suite:** contract validators, lifecycle tests, and reference fixtures;
- **Governance Log:** approvals, revocations, audits, and policy changes.

The first implementation should be small and inspectable. A versioned repository with structured records and reproducible scripts may be more informative than a complex distributed platform built before the research questions are settled.

## 13. Proposed Phased Roadmap

### Phase 0 — Definition and baseline audit

Freeze initial terminology, evaluation protocols, resource accounting, and negative controls. Identify potential leakage and unsupported claims in existing examples.

**Exit criterion:** independent readers can reproduce the definitions and understand what would falsify each hypothesis.

### Phase 1 — Contract-first research MVP

Implement minimal schemas for capability profiles, opportunities, probes, evidence bundles, and relay records. Run syntactic and lifecycle conformance tests.

**Exit criterion:** every research result can be traced to a specific protocol, evaluator, and artifact version.

### Phase 2 — Three controlled case studies

Implement the studies proposed in [CASE-001](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md), [CASE-002](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md), and [CASE-003](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md). Include strong baselines and explicit failure thresholds.

**Exit criterion:** at least one independent, interpretable comparison per case, including null results where applicable.

### Phase 3 — Longitudinal relay and boundary learning

Study adaptive gating, evidence reuse, and recursive relay across multiple rounds. Freeze evaluation tasks before system updates and perform ablations.

**Exit criterion:** distinguish mere accumulation of records from durable, causally attributable learning.

### Phase 4 — Cross-domain and cross-team replication

Invite independent groups to reproduce experiments and exchange portable evidence units. Record disagreements, schema incompatibilities, and environment-specific failures.

**Exit criterion:** verified reproducibility claims, not just successful artifact exchange.

### Phase 5 — Revising the theory

Update the conceptual framework, contract definitions, and claims based on observed evidence. Retire hypotheses that fail and document alternatives.

**Exit criterion:** an auditable theory revision that incorporates both supportive and disconfirming results.

No phase requires a claim that AGI has been achieved.

## 14. Suggested Near-Term Research Questions

1. Can an explicitly represented shared core outperform direct prompting on genuinely unseen domains after accounting for extra compute?
2. Which residual types most often predict harmful transfer?
3. Does directional scoring outperform simple similarity ranking under equal exploration budgets?
4. When does weak counterevidence improve candidate selection rather than suppress useful novelty?
5. Can adaptive permeability policies generalize to unseen boundary conditions without granting unauthorized execution rights?
6. What is the smallest frozen-unit system that exhibits persistent structural learning under rigorous controls?
7. Does repeated execution improve future decisions when only evidence capture—not model parameters—changes?
8. Which relay artifacts are most portable across teams: prompts, structural mappings, evaluator contracts, or counterexample sets?
9. How should a system distinguish failure to discover a capability from evidence that the capability is absent?
10. What empirical result would justify updating the estimated evolvable boundary rather than merely the observed boundary?
11. Can independent evaluators detect misleading capability claims produced by optimistic relay summaries?
12. At what coordination cost does a multi-unit system cease to outperform a strong single-unit baseline?

These questions are invitations to experiments, not assertions that the proposed mechanisms work.

## 15. Collective Learning and Contribution Protocol

Contributors are encouraged to submit small, independently useful research pieces rather than broad endorsements. A useful contribution should state:

1. **Question and scope:** Which claim or mechanism is being examined?
2. **Method and baseline:** What was held constant, and what was compared?
3. **Evidence and provenance:** Where are the data, protocol, code, and evaluator definitions?
4. **Results and uncertainty:** What improved, failed, or remained unresolved?
5. **Counterarguments:** What competing explanations remain plausible?
6. **Relay value:** What reusable structure, negative finding, or open question should others inherit?

Contributions should be marked **hypothesis**, **exploratory observation**, **replicated result**, **contested claim**, or **retracted claim** as appropriate. The project should welcome carefully documented failures and alternative architectures.

## 16. Related ISGFTR Documents

**Conceptual foundation:** [ISGFTR-001](docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md), [ISGFTR-002](docs/ISGFTR-002-Five-Characteristics-of-Intelligence-Spillover-and-Relay.md), [ISGFTR-003](docs/ISGFTR-003-Folding-Generalization-Duality-and-Structural-Reuse.md), [ISGFTR-004](docs/ISGFTR-004-Intelligence-Fluidity-and-Permeable-Structural-Boundaries.md).

**Discovery and system learning:** [ISGFTR-005](docs/ISGFTR-005-Directional-Intuition-and-Weak-Evidence-Transfer.md), [ISGFTR-006](docs/ISGFTR-006-System-Centric-Intelligence-and-Multi-Level-Learning.md), [ISGFTR-007](docs/ISGFTR-007-Recursive-Relay-and-Open-System-Intelligence-Growth.md), [ISGFTR-008](docs/ISGFTR-008-Intelligence-Spillover-and-Transfer-Prospecting.md).

**Boundaries and research architecture:** [ISGFTR-009](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md), [ISGFTR-010](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md).

**Extensions:** [EXT-001](extensions/EXT-001-Biomimetic-Fluidity-and-Selective-Permeability.md), [EXT-002](extensions/EXT-002-Learning-the-Boundaries-of-Intelligence-Flow.md), [EXT-003](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md).

**Companion research assets:** [OPEN-QUESTIONS.md](OPEN-QUESTIONS.md), [TESTABLE-HYPOTHESES.md](TESTABLE-HYPOTHESES.md), [VALIDATION-ROADMAP.md](VALIDATION-ROADMAP.md), [GLOSSARY.md](GLOSSARY.md), and [CONTENTS.md](CONTENTS.md).

## 17. Closing Perspective

The most valuable future result may not be evidence of an expanding intelligence frontier. It may be a precise account of **where transfer fails, why a boundary remains resistant, and what information would change that conclusion**. A theory of intelligence flow becomes useful when it makes both opportunities and limitations more visible, testable, and shareable.

ISGFTR therefore treats open-ended growth as a research question, not a destination guaranteed by architecture. The immediate goal is an evidence-disciplined process through which independent researchers can **prospect, test, challenge, revise, and relay** structural intelligence claims.

---

*Document status: Forward-looking research agenda. No experiments are represented here as completed or independently validated. All proposed mechanisms remain subject to falsification and revision.*
