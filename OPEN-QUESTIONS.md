# Open Questions — Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Open research questions and collaborative investigation agenda  
**Version:** 1.0.0 (theory-first)  
**Status:** Open hypotheses; not empirical findings  
**Date:** 2026-10-31

## 1. Purpose and Research Discipline

This document records unresolved questions arising from the ISGFTR research program. Its purpose is not to suggest that the proposed mechanisms are already established, nor to imply that a pathway to artificial general intelligence (AGI) has been demonstrated. Instead, it offers researchers a navigable set of uncertainties, competing explanations, falsification opportunities, and potential experimental contributions.

ISGFTR investigates five potentially interacting characteristics of intelligence—**spillover, generalization, fluidity, transfer, and relay**—and their relationships to structural folding, weak-evidence prospecting, system-centric learning, and evolving capability frontiers.

Each question below should ultimately be examined under explicit task conditions, resource budgets, provenance requirements, evaluation procedures, and appropriate comparison baselines. Where possible, investigators should publish negative findings, unsuccessful transfers, and alternative explanations alongside positive results.

**Interpretive rule:** A promising opportunity is not a demonstrated capability; successful transmission is not necessarily useful transfer; improved performance is not necessarily durable learning; and open-ended exploration is not proof of AGI.

## 2. Question Map and Priorities

Priority is a proposal for research sequencing, not a statement of scientific importance or expected success.

| Cluster | Research focus | Representative question | Suggested priority |
|---|---|---|---|
| Q-BND | Capability boundaries | How can the four boundaries be measured without circular definitions? | Foundational |
| Q-SP | Spillover | When is apparent spillover more than task overlap or benchmark leakage? | Foundational |
| Q-FG | Folding and generalization | Which preserved structures actually support out-of-domain reuse? | Foundational |
| Q-FL | Fluidity and permeability | When should a system open or close a transfer boundary? | Near-term |
| Q-DI | Directional intuition | Can weak evidence discover useful transfers under a fixed probe budget? | Near-term |
| Q-TR | Transfer and relay | What constitutes faithful and useful relay across contexts? | Near-term |
| Q-ML | Multi-level learning | Can frozen execution units support durable system-level learning? | Foundational |
| Q-RG | Recursive growth | When does relay improve future learning rather than merely repeat activity? | Medium-term |
| Q-EV | Evidence and evaluation | What evidence is sufficient for a scoped capability claim? | Foundational |
| Q-AGI | AGI implications | What, if anything, follows about general intelligence? | Long-term |

## 3. Capability Boundaries (Q-BND)

ISGFTR distinguishes **Generative**, **Observed**, **Reachable**, and **Evolvable** capability boundaries. These are context-dependent research constructs, not necessarily nested geometric sets or intrinsic constants of a model.

**Q-BND-01 — Operational definitions.** Can each boundary be specified in terms of a subject, task distribution, resource budget, time horizon, allowed tools, and admissible evidence without defining the boundary by the very performance being measured?

**Q-BND-02 — Boundary identification.** How much probing is needed to estimate a reachable frontier? What confidence or uncertainty intervals can be reported when the task space is open-ended?

**Q-BND-03 — Boundary shifts.** How should we distinguish a change in observed capability caused by improved measurement from an actual change in reachable capability caused by tools, decomposition, memory, or structural reorganization?

**Q-BND-04 — Evolvability.** Can an evolvable frontier be characterized prospectively without making unverifiable claims about all future learning trajectories?

**Q-BND-05 — Non-nesting.** Under which conditions are the four boundary concepts non-nested or incomparable, and how should a capability profile represent those relationships?

**Q-BND-06 — Attribution.** When a system crosses an apparent boundary, how much of the gain belongs to the underlying model, the interface, the evaluator, external data, or the system as a whole?

*Possible study:* Register a fixed set of tasks and resources, compare direct model responses, structured decomposition, tool-augmented execution, and evidence-guided routing, then report frontier estimates separately for each condition.

## 4. Intelligence Spillover (Q-SP)

**Q-SP-01 — Definition beyond coincidence.** What minimum evidence differentiates a genuine spillover effect from shared training data, prompt sensitivity, familiar task templates, or evaluator artifacts?

**Q-SP-02 — Training objective versus learned capability.** How can researchers investigate capabilities beyond a narrow training objective without implying that the objective places no meaningful constraints on the model?

**Q-SP-03 — Hidden competence versus scaffolding.** When a novel task becomes solvable through scaffolding, is the newly observed behavior evidence of latent competence, newly assembled system competence, or both?

**Q-SP-04 — Transfer asymmetry.** Why might a capability spill from domain A to domain B but not from B to A? Are the asymmetries explained by representation, available feedback, data density, or evaluator design?

**Q-SP-05 — Negative spillover.** Can one capability actively interfere with another when a shared structure is reused incorrectly? How should such failures be cataloged?

**Q-SP-06 — Replication.** How stable are observed spillover effects across models, seeds, task paraphrases, tool configurations, and independent evaluation teams?

*Falsification opportunity:* If apparent spillover disappears after controlling for task overlap, leakage, and prompt budget, the stronger spillover interpretation should be rejected or narrowed.

## 5. Folding–Generalization Duality and Structural Reuse (Q-FG)

**Q-FG-01 — Reusable cores.** Which features of a folded representation are necessary for transfer: causal relationships, constraint topology, action dependencies, semantics, or something else?

**Q-FG-02 — Compression versus generalization.** Under what conditions does folding preserve reusable structure, and when does it erase distinctions essential to the target domain?

**Q-FG-03 — Residuals.** How should target-specific and source-specific residuals be represented so that a shared core does not induce misleading equivalence?

**Q-FG-04 — Uncertainty recovery.** When is it preferable to preserve uncertainty during folding, and when can uncertainty be recovered later through independent evidence or two-phase search?

**Q-FG-05 — Transfer distance.** Is there a task-native metric that predicts structural reuse better than embedding similarity or surface lexical overlap?

**Q-FG-06 — Bidirectional reuse.** Does successful A→B transfer increase the chance of useful B→A transfer, or is structural transfer fundamentally directional in many settings?

**Q-FG-07 — Cost accounting.** Does reusable folding reduce total search and verification cost after including the cost of discovering, maintaining, and validating the core?

*Suggested controls:* Surface-similarity baselines, random analogies, deliberately corrupted cores, residual-free transfer, and full source-specific solutions.

## 6. Intelligence Fluidity and Selective Permeability (Q-FL)

**Q-FL-01 — Operational fluidity.** Can fluidity be measured as adaptive movement across representations, tasks, tools, or organizations without confusing it with general task competence?

**Q-FL-02 — Boundary types.** Which boundaries—representational, task, evidence, organizational, temporal, or authority—should be learned independently, and which require joint policies?

**Q-FL-03 — Selective openness.** When does a selective-permeability policy outperform both permanently closed and permanently open transfer policies?

**Q-FL-04 — Policy drift.** How can an adaptive flow policy avoid becoming overly permissive after a sequence of misleading successes or overly restrictive after a few failures?

**Q-FL-05 — Exploration versus authority.** How can systems accept weak-evidence hypotheses for sandbox probing without granting those hypotheses deployment privileges?

**Q-FL-06 — Context changes.** What mechanisms detect when a previously safe and useful transfer route is no longer appropriate?

**Q-FL-07 — Human governance.** Which decisions must remain under explicit human or organizational authority even when automated boundary learning appears effective?

*Minimum experiment:* Compare fixed-open, fixed-closed, hand-coded selective, and evidence-adaptive policies on changing task distributions; measure utility, unsafe promotions, negative transfer, and review cost.

## 7. Directional Intuition and Weak-Evidence Prospecting (Q-DI)

**Q-DI-01 — Weak evidence.** Which weak signals provide useful information beyond conventional similarity: partial structure, historical precedents, counterexamples, task-native metrics, or unexplained residuals?

**Q-DI-02 — Metric-native scoring.** Can candidate transfer directions be ranked in a domain-native metric without first embedding every object in a shared vector space?

**Q-DI-03 — OTHERS residual.** Can unmatched or poorly explained structure improve discovery, or does it primarily add noise and false positives?

**Q-DI-04 — Calibration.** How should prospect priority scores be evaluated when they are not calibrated probabilities of success?

**Q-DI-05 — Budget efficiency.** Under a fixed probing budget, does weak-evidence directional selection discover more validated transfers than random search, nearest-neighbor similarity, or expert heuristics?

**Q-DI-06 — Information value.** How can the value of a negative probe be measured when it improves future search without producing an immediate successful transfer?

**Q-DI-07 — Portfolio diversity.** Does choosing a diverse portfolio of candidate hypotheses outperform selecting only the highest-ranked individual candidates?

**Q-DI-08 — Selection bias.** How can researchers estimate missed opportunities when only selected prospects receive expensive validation?

*Proposed endpoint:* Validated discoveries per unit budget, with false-discovery rate, negative-transfer severity, and follow-up information value reported separately.

## 8. Transfer, Relay, and Structural Interoperability (Q-TR)

**Q-TR-01 — Relay semantics.** What information must travel with a structural unit for another system to interpret it correctly: scope, assumptions, evidence, uncertainty, counterevidence, evaluator, version, and provenance?

**Q-TR-02 — Faithful transmission.** How can we test whether a receiving system preserves the meaning of a transferred structure rather than merely accepting its syntax?

**Q-TR-03 — Adoption versus utility.** Which evaluations distinguish successful receipt, correct interpretation, authorized adoption, observed benefit, and durable improvement?

**Q-TR-04 — Spatial relay.** Under what conditions does passing structure among specialized units improve performance beyond a static pipeline with equivalent computational resources?

**Q-TR-05 — Temporal relay.** Can repeated execution yield measurable information gains even when immediate task outcomes do not improve?

**Q-TR-06 — Failure relay.** How should failed transfers and counterevidence be packaged so that future recipients can avoid repeating the same error without overgeneralizing the failure?

**Q-TR-07 — Versioning.** How should relay units be superseded, contested, or retracted without silently rewriting historical evidence?

**Q-TR-08 — Cross-system conformance.** Which minimum contracts are necessary for relay interoperability across implementations with different internal representations?

*Practical research artifact:* A versioned Structural Relay Unit with machine-checkable provenance, explicit residuals, independent reproduction links, and status transitions.

## 9. System-Centric Intelligence and Multi-Level Learning (Q-ML)

**Q-ML-01 — Frozen-unit learning.** Can a system of frozen execution units improve on future held-out tasks through persistent changes to routing, memory, task decomposition, validation, or policy?

**Q-ML-02 — Levels of learning.** Can unit, interaction, structural, relay, collective, and evolutionary learning be distinguished experimentally rather than merely named conceptually?

**Q-ML-03 — Causal attribution.** What interventions isolate gains due to structural learning from gains due to larger context windows, retrieval volume, additional inference calls, or evaluator tuning?

**Q-ML-04 — Collective credit.** How should credit be assigned among units, communication paths, learned policies, and evidence stores when system-level outcomes improve?

**Q-ML-05 — Coordination costs.** When do communication overhead, latency, inconsistency, or error propagation outweigh gains from specialized components?

**Q-ML-06 — Learning retention.** What constitutes durable system learning: improvement after a reset of transient context, across new tasks, across teams, or across changed environments?

**Q-ML-07 — Biological analogy.** Which insights from social insects, neural systems, and human organizations survive formal comparison with engineered multi-agent systems, and which analogies are misleading?

**Q-ML-08 — Novelty relative to prior work.** What does ISGFTR add beyond established work on swarm intelligence, organizational learning, multi-agent reinforcement learning, retrieval-augmented systems, and tool orchestration?

*Decisive control:* Hold execution models, tools, inference budgets, and evaluation data fixed while randomizing or ablating the learned structural policy and evidence registry.

## 10. Recursive Relay and Open-System Growth (Q-RG)

**Q-RG-01 — Recursion versus repetition.** What observable criterion distinguishes a repeated workflow from a relay loop that changes future search or learning capability?

**Q-RG-02 — Three growth types.** Can performance growth, reachability growth, and improvement of the learning process be measured independently?

**Q-RG-03 — Meta-learning without weight updates.** Can structural changes make later capability acquisition systematically cheaper, more reliable, or more general?

**Q-RG-04 — Stability.** Does recursive relay converge, oscillate, accumulate brittle complexity, or collapse under distribution shift?

**Q-RG-05 — Open-endedness.** How can claims of open-ended growth be tested under finite observation windows and finite resource budgets?

**Q-RG-06 — Anti-Goodhart safeguards.** How can a system detect when improving its evaluator score no longer corresponds to improving real-world task competence?

**Q-RG-07 — Evidence accumulation.** When does the value of repeated execution saturate, and how should a system decide to stop gathering redundant evidence?

**Q-RG-08 — Recursive self-improvement.** What additional evidence would be required to classify an observed relay cycle as genuine recursive self-improvement rather than workflow optimization?

*Failure condition:* If a system's apparent growth vanishes after controlling for memory size, evaluation leakage, and compute budget, claims of recursive capability growth must be revised.

## 11. Evidence, Evaluation, and Conformance (Q-EV)

**Q-EV-01 — Claim granularity.** How narrow should a capability claim be to remain informative and reproducible without becoming trivially specific?

**Q-EV-02 — Two-gate governance.** What evidence suffices for exploratory admission, and what stronger evidence is necessary to support a scoped capability claim?

**Q-EV-03 — Deployment gate.** Why should deployment authorization remain separate from scientific validation, and how should this separation be enforced?

**Q-EV-04 — Counterevidence.** How should contradictory observations affect claim status, exploration priority, and relay eligibility?

**Q-EV-05 — Independent replication.** How can independent teams reproduce a transfer claim when proprietary models, changing APIs, or private datasets are involved?

**Q-EV-06 — Measurement validity.** Which metrics reflect real transfer utility rather than benchmark familiarity, output style, or evaluator preferences?

**Q-EV-07 — Uncertainty reporting.** How should uncalibrated rankings, empirical success rates, confidence intervals, and subjective assessments be kept distinct?

**Q-EV-08 — Contract interoperability.** Can the four ISGFTR specifications support machine-checkable conformance without prematurely fixing one implementation architecture?

**Q-EV-09 — Negative results.** What incentives and formats make it practical to publish failed probes and abandoned hypotheses?

**Q-EV-10 — Auditability.** Can an external reviewer reconstruct why a prospect was admitted, why a claim was promoted, and which evidence was available at each decision point?

The corresponding contracts are [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md), [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md), [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md), and [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md).

## 12. AGI Implications and Theoretical Limits (Q-AGI)

**Q-AGI-01 — Necessary versus sufficient.** Are spillover, generalization, fluidity, transfer, and relay necessary, sufficient, or merely useful for some operational definitions of general intelligence?

**Q-AGI-02 — Model-centric versus system-centric.** Can a system of specialized units achieve broad general competence without any individually general unit, and under what resource and autonomy constraints?

**Q-AGI-03 — Hybrid architectures.** When do model-level learning and system-level structural learning complement one another, and when are they redundant?

**Q-AGI-04 — Capability coverage.** How should breadth, depth, robustness, adaptation speed, and autonomy be combined without hiding severe failures in aggregate scores?

**Q-AGI-05 — Agency and sovereignty.** Which kinds of self-directed prospecting and structural evolution are compatible with meaningful human oversight?

**Q-AGI-06 — Bounded resources.** What limits do finite compute, memory, data, time, energy, and coordination impose on purported open-ended intelligence growth?

**Q-AGI-07 — Counterexamples.** What systems show impressive relay and generalization yet remain narrow, brittle, or incapable of independent adaptation?

**Q-AGI-08 — Evidence threshold.** What empirical results would materially change our assessment of the plausibility of system-centric or hybrid AGI pathways?

ISGFTR makes no claim that its proposed mechanisms guarantee AGI. The appropriate research posture is comparative, empirical, and open to disconfirmation. See [ISGFTR-009](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md) and [EXT-003](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md).

## 13. Cross-Cutting Questions

Several problems recur across clusters and should be treated as shared research infrastructure rather than isolated topics:

- **Causal identification:** Can improvements be attributed to the proposed mechanism rather than increased computation, data, tool access, or human intervention?
- **Distribution shift:** Do observed gains persist when task families, evaluators, interfaces, and environments change?
- **Negative transfer:** How can harmful transfer be detected early and preserved as informative counterevidence?
- **Uncertainty:** Can a system express what remains unknown without converting every directional score into a misleading probability?
- **Resource accounting:** What is the complete cost of discovering, probing, validating, maintaining, and relaying a structural unit?
- **Provenance and reproducibility:** Can claims be reconstructed and challenged by researchers who did not design the original system?
- **Human authority:** Can exploratory intelligence remain broad while adoption and deployment are governed by explicit authorization?
- **Open research:** Can useful structural knowledge be shared without requiring identical runtime implementations or exposing sensitive information?

## 14. Suggested First Research Portfolio

A modest first portfolio is preferable to attempting to validate the entire framework at once.

| Study | Central question | Experimental comparison | Primary outcome |
|---|---|---|---|
| P-01: Structural Core | Does folding improve cross-domain transfer? | Shared-core mapping vs surface analogy and direct baseline | Held-out target success and negative transfer |
| P-02: Weak-Evidence Prospecting | Does directional ranking improve discovery efficiency? | Directional portfolio vs random and similarity ranking | Validated transfers per probe budget |
| P-03: Selective Permeability | Can adaptive gating outperform fixed policies? | Learned vs fixed-open, fixed-closed, and hand-coded gates | Utility under shift, unsafe promotion rate |
| P-04: Frozen-Unit Learning | Does system-level structural learning persist? | Adaptive structure vs static orchestration under equal compute | Post-reset held-out performance |
| P-05: Evidence Relay | Do negative results improve later exploration? | Full evidence registry vs positive-only and no-history registry | Future discovery efficiency and error reduction |
| P-06: Recursive Growth | Does relay improve the future learning process? | Recursive policy updates vs repetition-only controls | Improvement in learning efficiency across rounds |

For each study, preregister the task distribution, hypotheses, baselines, budget, evaluation criteria, stop rules, and expected failure modes. Use multiple seeds or independent replications where appropriate. Record null and negative outcomes.

## 15. A Minimal Open-Question Record

To make these questions actionable and portable, contributors may use the following lightweight record. This is an illustrative format, not a finalized machine schema.

```yaml
question_id: Q-DI-05
version: "1.0"
title: "Does weak-evidence prospecting improve discovery per budget?"
status: open
scope:
  subjects: ["frozen-model systems"]
  task_families: ["cross-domain structural transfer"]
  resource_limit: "fixed number of probe calls"
competing_explanations:
  - "directional evidence predicts useful transfer"
  - "simple similarity or task frequency explains the gains"
proposed_baselines:
  - random_selection
  - surface_similarity
  - structural_similarity
primary_metrics:
  - validated_transfers_per_budget
  - false_discovery_rate
  - negative_transfer_severity
required_evidence:
  - registered_protocol
  - held_out_tasks
  - reproducible_probe_log
  - counterevidence
links:
  specification: "specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md"
  case: "cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md"
notes: "Exploration scores are not presumed to be calibrated probabilities."
```

Recommended lifecycle for a question: **Open → Protocol Proposed → Under Test → Evidence Available → Supported / Contested / Unresolved → Revised or Retired**. A status change should preserve the original question and its evidence history rather than silently overwrite it.

## 16. How Researchers Can Contribute

Contributions need not support ISGFTR. Useful contributions include:

1. A sharper operational definition that eliminates ambiguity.
2. A concrete counterexample or negative-transfer case.
3. An experimental protocol with a credible baseline and matched budget.
4. A replication or independent evaluation of a reported effect.
5. A machine-checkable contract or conformance test.
6. A structural relay unit that includes assumptions, provenance, residuals, and failure conditions.
7. A connection to established literature that narrows or challenges novelty claims.
8. A carefully scoped new hypothesis that makes a distinct, falsifiable prediction.

The most valuable outcome may be a better question, a more precise boundary, or an informative failure rather than a positive result.

## 17. Research Navigation

**Core conceptual articles**

- [ISGFTR-001 — Static Boundaries and Capability Frontiers](docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md)
- [ISGFTR-002 — Five Characteristics](docs/ISGFTR-002-Five-Characteristics-of-Intelligence-Spillover-and-Relay.md)
- [ISGFTR-003 — Folding–Generalization Duality](docs/ISGFTR-003-Folding-Generalization-Duality-and-Structural-Reuse.md)
- [ISGFTR-004 — Intelligence Fluidity](docs/ISGFTR-004-Intelligence-Fluidity-and-Permeable-Structural-Boundaries.md)
- [ISGFTR-005 — Directional Intuition](docs/ISGFTR-005-Directional-Intuition-and-Weak-Evidence-Transfer.md)
- [ISGFTR-006 — System-Centric Learning](docs/ISGFTR-006-System-Centric-Intelligence-and-Multi-Level-Learning.md)
- [ISGFTR-007 — Recursive Relay](docs/ISGFTR-007-Recursive-Relay-and-Open-System-Intelligence-Growth.md)
- [ISGFTR-008 — Capability Prospecting](docs/ISGFTR-008-Intelligence-Spillover-and-Transfer-Prospecting.md)
- [ISGFTR-009 — AGI Limits and Counterarguments](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md)
- [ISGFTR-010 — Open Research Architecture](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md)

**Illustrative studies**

- [CASE-001 — LLM Spillover and Cross-Domain Transfer](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md)
- [CASE-002 — Minimal System-Centric Collective Learning](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md)
- [CASE-003 — Weak-Evidence Prospecting and Relay](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md)

**Extensions**

- [EXT-001 — Biomimetic Fluidity](extensions/EXT-001-Biomimetic-Fluidity-and-Selective-Permeability.md)
- [EXT-002 — Learning Flow Boundaries](extensions/EXT-002-Learning-the-Boundaries-of-Intelligence-Flow.md)
- [EXT-003 — Evolvable Potential and Open-Ended AGI](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md)

See also [TESTABLE-HYPOTHESES.md](TESTABLE-HYPOTHESES.md), [VALIDATION-ROADMAP.md](VALIDATION-ROADMAP.md), [FUTURE-DIRECTIONS.md](FUTURE-DIRECTIONS.md), and [GLOSSARY.md](GLOSSARY.md).

## 18. Closing Perspective

ISGFTR is most useful if it encourages researchers to distinguish **what a system appears able to do**, **what it can reach under stated conditions**, **what can be transferred or relayed reliably**, and **what can improve over time through validated learning**.

These questions should remain open to competing explanations and revision. A healthy collective-learning program preserves uncertainty, documents failures, and makes both claims and counterclaims easier to test.

**Explore broadly. Validate carefully. Preserve counterevidence. Relay what others can inspect and reproduce.**

---

*This document is a theory-first research agenda. The listed questions, mechanisms, and example protocols are proposals for investigation, not claims of demonstrated empirical success or AGI.*
