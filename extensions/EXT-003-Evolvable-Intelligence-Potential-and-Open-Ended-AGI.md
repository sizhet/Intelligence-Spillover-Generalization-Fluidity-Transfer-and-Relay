# EXT-003 — Evolvable Intelligence Potential and Open-Ended AGI

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Exploratory research extension and falsifiable architectural hypotheses  
**Version:** 1.0.0 (theory-first)  
**Status:** Open research proposal; no claim of demonstrated AGI  
**Date:** 2026-10-30

## Abstract

A system's observed capabilities are not necessarily the full set of capabilities it could reach through changes in representation, tools, organization, memory, learning policy, or structural relay. This extension examines **evolvable intelligence potential**: the conditional capacity of an intelligence system to expand its future *reachable and validated* capabilities through evidence-guided modification of its own learning and execution arrangements. We distinguish present performance from latent opportunity, structural reconfiguration from durable learning, and open-ended exploration from open-ended improvement. We propose a research architecture connecting capability prospecting, adaptive permeability, multi-level learning, structural relay, and explicit evaluation governance. We identify counterarguments, resource ceilings, nonstationarity, failure modes, and experiments that could refute the framework. The proposal does not assert that intelligence growth is unlimited, that recursively composed systems are generally intelligent, or that AGI follows from the five ISGFTR characteristics.

**Keywords:** evolvable intelligence potential; open-ended learning; system-centric intelligence; structural relay; capability prospecting; AGI; adaptive boundaries; recursive self-improvement; falsifiability.

---

## 1. Motivation: Beyond a Fixed Capability Inventory

A model or system is commonly described by its current task scores, benchmarks, and deployment affordances. These are indispensable observations, but they are measurements under particular conditions. A system that cannot solve a task today may succeed after a representation change, access to a verified tool, a different decomposition, or an improved coordination policy. Conversely, a system that succeeds once may fail to repeat the result or generalize to nearby tasks.

ISGFTR proposes that the relevant research object is not only a list of observed skills but also a **process by which potential capabilities are discovered, tested, retained, and sometimes expanded**. This shift is deliberately conditional. No amount of architectural vocabulary can establish the existence of a capability without evidence. The question is whether a reproducible learning process can make previously inaccessible tasks reliably reachable, and whether that process can itself improve under controlled conditions.

This extension builds on ISGFTR-001 through ISGFTR-010, SPEC-001 through SPEC-004, CASE-001 through CASE-003, and EXT-001/002. It is a directional extension rather than an additional proof of the earlier hypotheses.

## 2. Operational Definitions

### 2.1 Capability under a scope

A capability claim must specify the acting subject (model, agent, team, or whole system), task family, environment, resources, success criteria, evaluation protocol, and evidence provenance. The same observed outcome may reflect a model skill, a tool, a retrieval corpus, a human intervention, or their composition. Attribution is part of the claim, not an optional footnote.

### 2.2 Four capability boundaries

We retain four non-equivalent categories:

- **Generative boundary:** candidate outputs or behaviors the present generative mechanism can produce under specified conditions.
- **Observed boundary:** capabilities supported by recorded evaluation outcomes.
- **Reachable boundary:** capabilities obtainable using an explicitly permitted set of compositions, resources, tools, and adaptations.
- **Evolvable boundary:** capabilities potentially reachable after admissible, evidence-guided changes to the system's structure or learning process.

These are *families of scoped claims*, not necessarily nested circles or a single numerical frontier. In particular, a hypothetical evolvable capability is not an observed one, and reachable performance may depend on resources unavailable in a different setting.

### 2.3 Evolvable intelligence potential

Let a system state be \(S_t\), an admissible modification policy be \(\Pi\), a resource budget be \(B\), and an evaluation family be \(\mathcal{E}\). Define an exploratory potential set:

\[
\mathcal{P}(S_t,\Pi,B,\mathcal{E}) = \{c : \exists\, \pi\in\Pi,\; \operatorname{cost}(\pi)\le B,\; \operatorname{Validate}_{\mathcal{E}}(c\mid \pi(S_t))=1\}.
\]

This is an **idealized research definition**, not a computable oracle. In practice the set is only partially sampled, the admissible policies may be unknown, and validation may be noisy. An observed expansion in the estimated set must be reported with its evaluation scope and confidence limits. Larger search budgets can produce apparent growth without improving the underlying learning mechanism.

### 2.4 Open-ended exploration versus open-ended growth

Open-ended exploration generates an indefinite succession of candidate questions, structures, or behaviors. Open-ended growth additionally requires *sustained, independently verified improvements* across meaningful dimensions. Novelty alone is insufficient. A system can endlessly generate new artifacts without increasing utility, robustness, transferability, or autonomy.

## 3. Five ISGFTR Characteristics as Candidate Enablers

**Spillover** describes useful performance outside the setting for which a capability was originally recognized. **Generalization** concerns performance across varying conditions under a specified task relation. **Fluidity** concerns the ability to redirect processes and representations across boundaries. **Transfer** is the reuse or adaptation of prior structure for a new target. **Relay** carries structures, evidence, and unresolved questions across subjects, environments, or time.

These mechanisms may interact. A generalized core may make a new transfer plausible; fluidity may make the transfer executable; relay may preserve both success and failure evidence; prospecting may select the next test. However, none of these implications is automatic. A relay may propagate an error, a generalization may be spurious, and a fluid system may be less reliable than a well-bounded specialist.

A useful research discipline is to measure each characteristic separately before claiming a synergistic effect. An experiment should include single-mechanism baselines and ablations rather than assuming a five-factor package is superior.

## 4. Three Distinct Forms of Growth

### 4.1 Performance growth

Higher measured performance on a fixed task distribution, with comparable resources and evaluation conditions. This may be valuable but may represent tuning rather than new competence.

### 4.2 Reachability growth

An increase in the tasks a system can solve under a defined operational budget. Tool access, better routing, and structural composition may enlarge reachability even when constituent model parameters remain frozen.

### 4.3 Learning-process growth

An improvement in the system's ability to **discover, test, and acquire further capabilities**. This is the strongest and most difficult claim. It requires testing the learning process on new opportunity distributions, not merely showing that it improved one previously targeted task.

We therefore propose a reporting tuple:

`GrowthRecord = (subject, task_distribution, baseline, intervention, resources, measured_delta, persistence, transfer_test, attribution, counterevidence)`.

Without these fields, “growth” risks conflating short-term utility, additional compute, and durable learning.

## 5. System-Centric AGI as a Research Hypothesis

A system-centric perspective asks whether broadly adaptable intelligence can arise from coordinated components whose individual capabilities are narrower than those of the whole. Biological colonies, nervous systems, and human organizations offer useful analogies, but they do not prove that an engineered multi-agent system will develop general intelligence. Existing research in distributed AI, swarm intelligence, organizational learning, and multi-agent reinforcement learning provides important precedents; the proposed contribution here is a specific **contract-first integration** of capability boundaries, evidence-gated prospecting, structural relay, and learning attribution.

Three non-exclusive candidate paths deserve comparison:

1. **Model-centric:** a general-purpose model improves primarily through its internal learning and representation mechanisms.
2. **System-centric:** fixed or slowly changing units gain breadth through coordination, memory, tooling, routing, and structural adaptation.
3. **Hybrid:** both the constituent models and the larger architecture learn, with explicit allocation of responsibility and evidence.

A system may be highly useful without meeting any robust AGI definition. AGI should therefore be treated as an external evaluation target requiring a separately specified operational definition, not as a label inferred from architectural complexity.

## 6. Learning–Execution Decoupling and Its Limits

Let execution units \(U_1,\ldots,U_n\) remain parameter-frozen while a system-level state \(M_t\) stores verified precedents, routing rules, decomposition templates, constraints, and negative evidence. The execution policy may be written schematically as

\[
a_t = \operatorname{Execute}(U_{1:n},\; x_t,\; M_t,\; \rho_t),
\qquad M_{t+1}=\operatorname{Learn}(M_t,\; x_t,\; a_t,\; e_t),
\]

where \(\rho_t\) is an authorized routing policy and \(e_t\) is evaluated evidence. Improvement in this setting demonstrates **system-level adaptation**, not weight-level learning in the units.

The decoupling hypothesis faces clear ceilings. Fixed units may lack essential perceptual, reasoning, or actuation primitives. Better coordination cannot always synthesize a missing primitive. A system's external memory may become stale, inconsistent, or too expensive to search. A fair experiment must compare against a strong static system with the same tools, tokens, memory budget, and available information.

## 7. Recursive Relay as a Candidate Growth Mechanism

We distinguish four stages:

1. **Execution relay:** a task or partial output moves between units.
2. **Evidence relay:** observations, failures, and evaluations persist for later reuse.
3. **Structural relay:** reusable policies, schemas, decompositions, or verified modules are transferred.
4. **Learning-process relay:** validated lessons improve the mechanism that selects and tests future changes.

The fourth stage is the most relevant to evolvable potential, but it also carries the greatest risk of self-reinforcing error. Recursive relay is not synonymous with recursive self-improvement. The latter requires demonstrated, attributable improvement in the system's own improvement process under independently checked conditions.

Repeated execution can be an evidence relay if it yields new measurements or improves confidence. Identical repetition without information gain may instead waste resources or amplify sampling bias. A relay ledger should record *what changed*, *what evidence supports it*, and *what remains unresolved*.

## 8. Prospecting the Evolvable Frontier

Capability Prospecting asks which unverified transformations deserve investigation. A candidate may arise from a structural analogy, a failed task with a promising residual, a historical precedent, an unexplained performance improvement, or a directional weak-evidence signal.

A conceptual prioritization function is:

\[
Q(p) = w_u U(p) + w_i I(p) + w_r R(p) - w_c C(p) - w_h H(p) - w_d D(p),
\]

where \(U\) is hypothesized utility, \(I\) expected information value, \(R\) potential structural reuse, \(C\) cost, \(H\) hazard or negative-transfer exposure, and \(D\) evidence redundancy. Weights are policy-dependent. The score is **an exploration ranking**, not a calibrated probability of success. The scoring process itself should be tested against random, similarity-based, and expert-curated selection baselines.

A prospect must carry its unresolved assumptions, candidate source/target mapping, OTHERS residuals, possible counterexamples, and stop conditions. Otherwise the search process may preferentially preserve attractive stories while discarding disconfirming evidence.

## 9. An Open-Ended Research Loop

A candidate architecture is:

`Observe → Identify Residual → Generate Prospect → Score Portfolio → Gate A → Probe → Evaluate → Gate B → Relay → Update Structural Memory → Audit → Reobserve`

**Gate A** determines whether exploration is justified and authorized. **Gate B** determines what capability claim, if any, the resulting evidence supports. Neither gate automatically authorizes external deployment. Deployment is governed separately by risk, domain, and operational controls.

The loop should maintain three linked registries:

- **Capability registry:** scoped observed and contested capabilities, with provenance and versions.
- **Prospect registry:** unresolved opportunities, assumptions, priorities, and probe plans.
- **Relay registry:** transmitted structures, source conditions, validation status, adaptations, and downstream outcomes.

This design is intended to make independent verification easier, not merely to make claims circulate faster.

## 10. Open-Endedness Without Unlimited Resources

Physical, computational, informational, and institutional limits matter. Exploration consumes energy, time, expert attention, and sometimes scarce real-world opportunities. Increasing the number of agents or trials can worsen coordination overhead, correlated errors, or safety exposure. We therefore reject an assumption of infinite growth and propose studying **growth efficiency**:

\[
\eta_{\mathrm{growth}} = \frac{\text{independently validated, durable capability gain}}{\text{total incremental research and operating cost}}.
\]

The numerator is multidimensional and cannot always be reduced to a scalar. Reports should show the underlying dimensions, such as transfer breadth, robustness, task success, and retention, rather than presenting one score as universal intelligence.

A research program may be successful if it identifies stable limits or conditions under which open-ended growth fails. Such negative results are useful structural relay assets.

## 11. Boundaries, Sovereignty, and Governance

Adaptive permeability should not erase control boundaries. The system may learn to suggest new exploration paths, but authority to probe sensitive systems, modify policies, integrate external artifacts, or deploy actions remains separately governed. This is especially important when recursive loops begin to alter their own selection rules.

Minimum governance commitments include: scoped authorization; immutable experiment provenance; explicit resource budgets; reversible structural updates; independent validation; retention of counterevidence; rollback on degradation; and auditability of who or what changed the learning policy. Policy learning can optimize within authorized limits but must not silently rewrite those limits.

The question “whose choice is it?” remains relevant. System-level capability growth does not establish a right for the system to choose its own societal objectives.

## 12. Failure Modes and Counterarguments

**F1 — Search masquerading as learning.** Additional trials discover successes without improving the discovery policy. *Test:* hold search budget constant and compare on unseen opportunity pools.

**F2 — Benchmark contamination.** Structural memory encodes evaluation-specific answers. *Test:* use withheld tasks, independent evaluators, and contamination audits.

**F3 — Tool-driven capability inflation.** Performance is attributed to the system despite a stronger external tool doing the critical work. *Test:* report component and tool ablations.

**F4 — Negative transfer.** Reused structures harm performance in the target domain. *Test:* compare with no-transfer and domain-specific baselines.

**F5 — Relay error amplification.** A false precedent spreads through a network. *Test:* inject known false claims and measure detection, containment, and rollback.

**F6 — Coordination overhead.** More units reduce reliability or increase cost. *Test:* measure end-to-end latency, failure rates, and marginal gains.

**F7 — Nonstationary boundary learning.** A once-useful transfer policy becomes harmful as conditions shift. *Test:* introduce controlled distribution shifts and evaluate adaptation lag.

**F8 — False open-endedness.** Novel artifacts increase but validated capability does not. *Test:* separate novelty metrics from utility and retention.

**F9 — Irreducible missing primitives.** No available composition can solve tasks requiring absent capabilities. *Test:* construct task families with provable or empirically demonstrated component limitations.

**F10 — Governance bypass.** Recursive optimization discovers routes around controls. *Test:* adversarial conformance checks and policy invariants, with no uncontrolled deployment.

These are not peripheral caveats; they are central empirical tests of the proposal.

## 13. Testable Hypotheses

Each hypothesis requires pre-registered scope, baselines, cost accounting, and negative-result publication.

**H1 — Prospecting efficiency.** Under equal probe budgets, evidence-guided prospecting finds more independently validated transfers than random prospect selection. *Refutation:* no consistent advantage across held-out task families.

**H2 — Structural reuse.** Verified reusable cores improve cross-domain transfer compared with unstructured example reuse, after controlling for information and compute. *Refutation:* benefits disappear under matched controls.

**H3 — Selective permeability.** Context-adaptive boundary policies improve risk-adjusted utility relative to fixed-open and fixed-closed policies. *Refutation:* simpler policies consistently match or outperform them.

**H4 — Frozen-unit system learning.** A system with frozen execution units but adaptive structural memory shows durable improvement on unseen tasks compared with a static architecture. *Refutation:* gains are explained by extra resources, memorization, or evaluation leakage.

**H5 — Negative evidence relay.** Preserving failures and counterevidence reduces repeated unproductive probes without materially suppressing novel successes. *Refutation:* no improvement in discovery efficiency or unacceptable loss of coverage.

**H6 — Learning-process improvement.** A prospecting policy updated from validated history performs better on future, disjoint prospect distributions than its initial version. *Refutation:* gains do not transfer beyond the training opportunity pool.

**H7 — Recursive relay persistence.** Improvements persist after temporary retrieval shortcuts, test-specific prompts, and evaluator hints are removed. *Refutation:* performance collapses under retention and transfer tests.

**H8 — Compositional limits.** Some task classes remain unreachable under frozen units and finite authorized compositions. *Support for a limit:* robust failure despite controlled increases in coordination budget; this result would constrain, not invalidate, the entire framework.

**H9 — Governance preservation.** Contract-governed recursive loops can retain auditability and rollback while learning. *Refutation:* policy changes repeatedly evade provenance or authorization controls.

**H10 — Growth-versus-novelty separation.** An open-ended generator optimized only for novelty yields weaker durable capability growth than a system using independent validation and retention. *Refutation:* no difference under fair comparison.

## 14. Experimental Program

### Experiment A — Frontier mapping with frozen units

Choose a finite benchmark family and a set of fixed, versioned execution units. Compare a static pipeline, random recombination, retrieval-only adaptation, structured prospecting, and structured prospecting plus relay. Hold total tools, model calls, time, and data access constant. Report reachable task coverage, accuracy, cost, and failure distributions. Distinguish previously observed tasks from genuinely held-out tasks.

### Experiment B — Learning the prospecting policy

Construct multiple nonoverlapping opportunity pools. Train or update only the prospect-selection policy using evidence from earlier pools; freeze it before each future evaluation. Compare discovery yield per probe and calibration of any claimed uncertainty estimates. Measure whether the policy learns transferable selection rules rather than memorizing specific candidates.

### Experiment C — Open-ended artifact generation versus growth

Compare novelty-seeking generation with validation-gated structural growth. Record unique artifacts, independent task utility, retention, negative transfer, and resource consumption. A positive result requires utility gains, not just a larger artifact inventory.

### Experiment D — Adversarial relay and provenance

Seed the relay registry with a mixture of valid, weak, contradictory, and intentionally erroneous precedents. Evaluate downstream detection, attribution, propagation, and rollback. Track whether system performance improves when counterevidence is preserved rather than discarded.

### Experiment E — Boundary drift

Change task conditions, available tools, or risk constraints across phases. Compare static and adaptive permeability policies. Measure adaptation latency, unsafe proposals, missed opportunities, and recovery after reversal of the shift.

### Experiment F — Long-horizon retention

After a learning phase, suspend updates and test on new tasks after multiple execution cycles. Remove temporary hints and prohibit access to test labels. Evaluate whether validated improvements persist and remain attributable to structural memory or policy changes.

## 15. Minimal Research MVP

The first MVP should be deliberately small:

1. Three to five frozen execution units with clearly different strengths and known limitations.
2. A versioned capability registry with evidence and counterevidence.
3. A prospect generator producing source–target structural mappings and explicit residuals.
4. A constrained probe scheduler with fixed budget and pre-registered baselines.
5. Independent evaluators for task success, robustness, and transfer.
6. A relay store retaining positive, negative, and inconclusive results.
7. An adaptive selection policy that can be switched off for ablation.
8. An audit layer enforcing permissions and provenance.

The MVP succeeds as a research instrument if it can **distinguish** structural learning from search, memorization, tool effects, and ordinary coordination—even if the central growth hypotheses fail.

## 16. Contract Interfaces

| Artifact | Function | Primary relationship |
|---|---|---|
| Capability Profile | Scoped ability, subject, environment, evidence | SPEC-001 |
| Spillover Opportunity Record | Unverified transfer prospect and weak evidence | SPEC-002 |
| Probe Lifecycle Record | Gate decisions, protocol, execution, adjudication | SPEC-003 |
| Structural Relay Unit | Portable result, provenance, residual, and reuse conditions | SPEC-004 |
| Boundary Policy Record | Context-dependent observe/probe/adopt/deploy permissions | EXT-002 |
| Growth Evaluation Record | Persistent, attributable, cost-aware change | This extension; proposed addition |

No contract grants automatic promotion from hypothesis to observation, from observation to replication, or from research approval to deployment authorization.

### Example: proposed growth evaluation record

```yaml
growth_record_id: gr-example-001
status: hypothetical_example
subject:
  kind: system
  id: frozen-units-plus-structural-controller
baseline:
  version: baseline-v1
  evaluation_set: heldout-family-a
intervention:
  kind: evidence_guided_structural_relay
  version: relay-policy-v2
resource_controls:
  fixed_model_weights: true
  matched_probe_budget: true
  matched_tool_access: true
claims:
  performance_growth: pending_validation
  reachability_growth: pending_validation
  learning_process_growth: not_established
evidence:
  positive: []
  negative: []
  independent_replications: []
retention_test: pending
cross_domain_test: pending
attribution_review: pending
governance:
  deployment_authorized: false
  rollback_supported: true
```

The example deliberately contains no fabricated results.

## 17. Relationship to Adjacent Research

This proposal intersects open-ended evolution, lifelong learning, meta-learning, transfer learning, program synthesis, automated curriculum generation, active learning, multi-agent coordination, and recursive self-improvement. It should be compared with these bodies of work rather than presented as replacing them. The potentially distinctive research emphasis is the **joint specification** of scoped capability boundaries, weak-evidence opportunity discovery, two-gate validation, provenance-preserving relay, and system-level learning attribution.

Related ISGFTR components provide narrower entry points: ISGFTR-003 for folding and reusable cores; ISGFTR-005 for directional intuition; ISGFTR-006 for multi-level learning; ISGFTR-007 for recursive relay; ISGFTR-008 for prospecting; ISGFTR-009 for AGI limits; and ISGFTR-010 for collective research architecture. The CASE series offers candidate experimental settings, not empirical confirmations.

## 18. Open Questions

1. Which capability dimensions permit meaningful comparisons across radically different task families?
2. Can a system learn a reusable prospect-selection policy without overfitting its historical research portfolio?
3. How can we detect missing primitives that coordination cannot overcome?
4. What constitutes sufficient independent replication for a system-level growth claim?
5. When should a negative transfer be treated as a local mismatch versus a broader structural counterexample?
6. Can selective permeability adapt safely under adversarial or rapidly changing environments?
7. How should human oversight allocate exploration budgets among utility, novelty, and scientific information gain?
8. Can relay registries remain useful without becoming unmanageable or self-confirming?
9. Which parts of the learning process should remain frozen to make causal attribution possible?
10. What operational AGI benchmarks, if any, could fairly compare model-centric, system-centric, and hybrid approaches?
11. How do we distinguish genuinely new capabilities from better access to pre-existing external services?
12. What observations would justify abandoning the open-ended growth hypothesis for a given architecture?

## 19. Suggested Figure Placement

- **Fig-002-Four-Intelligence-Boundaries.png:** after Section 2, illustrating distinct scoped boundary categories without implying a universal geometric nesting.
- **Fig-006-System-Centric-Multi-Level-Learning.png:** after Section 6, contrasting execution-unit behavior with system-level structural learning.
- **Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png:** after Section 8, showing the prospecting pipeline and its evidence gates.
- **Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png:** after Section 9, showing feedback loops, provenance, and counterevidence.

Figures are proposed cross-references; their presence and exact contents must be checked before publication.

## 20. Validation and Publication Discipline

This is a **theory-first directional research extension**. No experiments, datasets, or external replications are claimed to have been completed by this document. Proposed hypotheses must be treated as unverified until tested. Future revisions should preserve superseded claims, cite supporting and contradictory work, distinguish conjecture from observation, and document changes to experimental protocols. Where possible, results should be shared with machine-readable contracts and explicit leftover questions to support collective learning.

## 21. Conclusion

The central proposition is not that intelligence inevitably expands without bound. It is that **the boundary of what a system can reliably do may itself become an object of structured learning**. Capability prospecting can search for plausible opportunities; adaptive permeability can govern exploration; independent evaluation can separate evidence from enthusiasm; and structural relay can preserve what is learned across time and organizational boundaries. Whether these mechanisms yield sustained, generalizable growth is an empirical question.

A successful research program must be willing to discover both new pathways and hard limits. Its most valuable outcome may be a clearer, testable account of when intelligence flows, when it fails to flow, and what kinds of learning can change that boundary.

---

**Research invitation:** Independent critiques, negative results, alternative baselines, boundary counterexamples, and replication protocols are welcome. The aim is a collective learning artifact, not a claim of completed AGI.
