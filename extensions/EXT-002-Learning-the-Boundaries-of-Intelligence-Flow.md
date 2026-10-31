# EXT-002 — Learning the Boundaries of Intelligence Flow

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Open research extension and falsifiable conceptual proposal  
**Version:** v1.0.0 (theory-first)  
**Status:** Proposed mechanisms and validation program; no empirical results claimed  
**Date:** 2026-10-31  
**Related documents:** ISGFTR-002–010; SPEC-001–004; CASE-001–003; EXT-001

## Abstract

Intelligence fluidity requires decisions about what information, representations, candidate structures, and learned practices may cross a boundary. A fixed boundary may reject useful novel transfers; an indiscriminately open boundary may amplify errors, negative transfer, contamination, and cost. This extension studies a third possibility: **learning the boundaries of intelligence flow** from observed outcomes, counterevidence, context shifts, and the history of structural relay. It proposes a boundary-learning framework that treats permeability as a contextual, revisable policy rather than a universal scalar. The framework separates permission to inspect a candidate, permission to test it in a sandbox, permission to rely on a validated result, and authority to deploy a consequential action. It specifies a boundary-state representation, feedback and attribution requirements, conservative policy updates, drift monitoring, and explicit rollback. A proposed experimental program compares static, fully open, hand-tuned, and learned boundaries under matched budgets. Success is defined by independently verified utility, calibrated risk, and durable performance—not by increased traffic across boundaries alone. All mechanisms and AGI implications remain hypotheses subject to falsification.

**Keywords:** intelligence flow; adaptive boundaries; selective permeability; boundary learning; structural transfer; weak evidence; negative transfer; policy control; evidence relay; collective learning.

---

## 1. Motivation: From Permeable Boundaries to Learned Boundaries

EXT-001 argues that an intelligent system may benefit from selective permeability. However, a designer cannot always specify in advance which unfamiliar representations, tools, analogies, or partner systems will be useful. Contexts change; formerly successful transfers can become unsafe or ineffective; apparently irrelevant weak evidence may become informative after additional observations.

The resulting research question is not simply **“Should a boundary be open?”** but:

> Can a system learn *which boundary to relax, for which kind of flow, in which context, for which purpose, under what evidence and risk constraints*—and revise that decision when new evidence arrives?

A boundary-learning system should be judged by the quality of its resulting decisions and the reliability of its claims, not by the amount of novelty admitted. The proposal builds on ISGFTR-004 (fluidity), ISGFTR-005 (directional intuition), ISGFTR-007 (recursive relay), ISGFTR-008 (capability prospecting), and SPEC-001–004 (claims, evidence, lifecycle, and relay contracts).

## 2. What Is an Intelligence-Flow Boundary?

A boundary is a context-dependent constraint on the movement or use of an intelligence-relevant object. Such objects may include a problem representation, hypothesis, evidence item, policy, memory, structural unit, tool output, learned routing rule, or execution request. Boundaries need not correspond to physical or organizational walls.

For research purposes, distinguish at least six dimensions:

1. **Representational boundary:** whether an unfamiliar encoding or ontology may be interpreted or mapped.
2. **Task boundary:** whether a capability learned or observed on one task may be considered for another.
3. **Evidence boundary:** which external claims and weak signals may enter a hypothesis portfolio.
4. **Unit boundary:** which components, agents, or organizations may exchange structural units.
5. **Temporal boundary:** whether prior outcomes may influence later decisions and for how long.
6. **Authority boundary:** which actions may actually be executed, integrated, or deployed.

The first five may be relaxed for exploratory purposes without relaxing the sixth. **Exploration permission and execution authority are separate contracts.**

### 2.1 A boundary is not a single threshold

A global openness parameter cannot adequately describe context, risk, evidence provenance, and downstream consequences. We therefore represent a boundary decision as a typed, scoped policy applied to a particular flow request. The representation is conceptual; no specific runtime is presumed.

Let a candidate flow be

$$
 f=(s,t,o,m,c),
$$

where $s$ is the source, $t$ the target, $o$ the object transferred, $m$ the proposed transfer mechanism, and $c$ the relevant context. Let $b$ describe the boundary type, policy version, allowed operations, evidence requirements, and authority constraints. The policy produces a decision

$$
 \pi_{\mathrm{boundary}}(f,b,h)\rightarrow (a,r,q),
$$

where $h$ is the available evidence history, $a$ is an admissibility decision, $r$ is the permitted research or execution route, and $q$ is an auditable rationale with uncertainty. This expression is a design abstraction, not an established cognitive law.

## 3. Four Distinct Permissions

A central proposal is a **four-permission boundary ladder**:

| Permission | Meaning | Typical evidence requirement | Prohibited inference |
|---|---|---|---|
| Observe | Inspect or record a candidate signal | Provenance and basic integrity checks | Observation proves utility |
| Probe | Test a candidate in a constrained setting | Hypothesis, budget, risk review, baseline | Sandbox success authorizes deployment |
| Adopt | Incorporate a validated structural unit for a defined scope | Replicable, scoped evaluation and counterevidence review | Adoption proves generality |
| Deploy | Authorize consequential use | Separate operational authorization and monitoring | Research validation overrides governance |

These permissions are not necessarily a linear automatic progression. A system may continue to observe a contested candidate while refusing adoption; it may revoke deployment while preserving its historical evidence. No learning algorithm should grant itself additional authority merely because its score improves.

![Fig-005-Directional-Intuition-and-Selective-Permeability.png](../figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png)

*Fig-005. Weak-evidence directional guidance through selectively permeable research boundaries. Exploratory ranking, claim validation, and deployment permission are independent decisions.*

## 4. Sources of Boundary-Learning Signals

A boundary learner may use multiple forms of evidence, each with different reliability and failure modes.

### 4.1 Positive transfer evidence

A candidate structural mapping improves held-out target performance under matched budgets and a declared baseline. Its scope, effect size, uncertainty, and resource cost should be retained. One success is not universal transferability.

### 4.2 Negative transfer and counterevidence

A mapping causes regression, instability, semantic drift, security concerns, or increased cost without compensating benefit. These outcomes are first-class learning signals rather than disposable failures. Counterevidence may suggest tightening a specific boundary or requiring a different probe, not necessarily permanently rejecting a whole source domain.

### 4.3 Directional and weak evidence

Structural resemblance, historical precedents, metric-native directional scores, and OTHERS residuals may indicate where to probe. Such signals can prioritize research but must not be treated as calibrated probabilities unless calibration is demonstrated. The learner should distinguish *priority to investigate* from *likelihood of success*.

### 4.4 Context and distribution change

Changes in target requirements, data provenance, tools, partner reliability, cost structure, or evaluation distributions may invalidate previous policies. A learned boundary requires drift detection and revalidation triggers.

### 4.5 Relay and repetition histories

Repeated execution can accumulate evidence about stability, failure rates, and context sensitivity even when the underlying execution units are frozen. Repetition becomes useful learning only if the observations are recorded, compared, and allowed to revise a policy. Repeating a flawed process without meaningful feedback may merely reproduce error.

## 5. A Boundary State and Learning Record

A canonical boundary-learning record should include:

- **Boundary identity and version:** stable identifier, type, owner, applicable contexts, policy version.
- **Flow request:** source, target, object, intended use, structural mapping, unresolved residuals.
- **Evidence lineage:** positive, negative, weak, replicated, and contested evidence with provenance.
- **Policy decision:** observe/probe/adopt/deploy permission; constraints and rationale.
- **Measured outcome:** preregistered metrics, baselines, cost, risk, uncertainty, and failure modes.
- **Update proposal:** proposed change, expected benefit, evidence basis, and rollback path.
- **Governance status:** approvals, expirations, independent review, and unresolved objections.

### 5.1 Illustrative YAML record

```yaml
schema_id: isgftr.boundary-learning.v0.1-proposal
boundary_id: boundary-cross-domain-routing-01
boundary_type: task_and_representation
policy_version: 3
context:
  source_domain: software-maintenance-planning
  target_domain: community-service-scheduling
  deployment_class: research_sandbox
flow:
  candidate_id: prospect-042
  object_type: structural_planning_core
  proposed_mechanism: dependency-and-resource-mapping
  residuals:
    - human-preference-constraints
    - uncertain-service-duration
permission:
  observe: allowed
  probe: allowed_with_budget
  adopt: pending_validation
  deploy: not_authorized
supporting_evidence:
  - evidence-101
counterevidence:
  - evidence-107
outcome:
  metric: held_out_constraint_satisfaction
  baseline_ref: baseline-12
  estimate: null  # no result claimed
  uncertainty: not_yet_measured
update_proposal:
  action: require_target_specific_residual_check
  reason: prior_negative_transfer
  status: proposed
  rollback_policy_version: 2
```

This is a **contract illustration**, not a finalized machine-readable schema. Future schema definitions should constrain field types, enumerations, and cross-record references.

## 6. The Boundary-Learning Cycle

A proposed cycle is:

**Observe → Characterize → Prospect → Admit → Probe → Evaluate → Update → Audit → Relay → Reobserve.**

1. **Observe:** detect new requests, candidate transfers, failures, and context changes.
2. **Characterize:** identify boundary type, affected units, authority level, and unresolved differences.
3. **Prospect:** generate hypotheses and directional priorities using weak evidence.
4. **Admit:** apply Gate A to decide whether a bounded probe is justified.
5. **Probe:** execute preregistered tests with controls, budgets, and stop conditions.
6. **Evaluate:** assess benefits, counterevidence, uncertainty, and generalization limits.
7. **Update:** propose a scoped policy change; do not silently expand authority.
8. **Audit:** check provenance, safety, attribution, drift, and policy invariants.
9. **Relay:** preserve results, including negative results, for other units and future runs.
10. **Reobserve:** monitor whether the update remains useful as conditions evolve.

This cycle extends the Prospect → Probe → Validate → Relay → Learn loop from ISGFTR-008. It does not require all stages to be automated.

![Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png](../figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png)

*Fig-007. Capability prospecting across uncertain frontiers: opportunity generation, prioritization, probing, evidence-based claim revision, and feedback into future research.*

## 7. Candidate Learning Mechanisms

Several approaches may be compared rather than assumed equivalent.

### 7.1 Rule revision from evidence

Explicit rules are updated when replicated outcomes show that a source–target transfer class is consistently beneficial or harmful. Rules are interpretable but may generalize poorly beyond observed conditions.

### 7.2 Contextual routing or bandit-style selection

A policy selects among permitted exploration routes using contextual features and measured rewards. Delayed outcomes, selection bias, nonstationarity, and asymmetric risks make naive reward optimization unreliable. Such algorithms are research candidates, not guaranteed solutions.

### 7.3 Structural memory and precedent retrieval

A registry stores prior successful and failed mappings with contextual qualifiers. Retrieval can help identify suitable probes, but precedent similarity does not establish transfer validity. Residual differences should remain explicit.

### 7.4 Multi-objective boundary optimization

The learner may consider verified task utility, discovery yield, negative-transfer rate, compute cost, latency, reproducibility, and risk. A scalar objective may obscure unacceptable tradeoffs. For consequential decisions, hard constraints and separate governance checks should take precedence over aggregate scores.

### 7.5 Hierarchical policy learning

A local unit may learn low-risk representational mappings while a higher-level control plane governs shared memory, cross-organization relay, and deployment. This permits learning–execution decoupling without confusing local adaptation with unrestricted system authority.

## 8. Boundary Update Rules and Stability

Policy adaptation introduces a new failure mode: the boundary learner itself may oscillate, overfit, or exploit the evaluation process.

Proposed safeguards include:

- **Scoped updates:** change the smallest boundary condition supported by evidence.
- **Hysteresis or evidence thresholds:** avoid opening and closing a boundary on one noisy observation.
- **Held-out evaluation:** assess proposed updates on tasks and contexts not used to choose them.
- **Versioned rollback:** preserve previous policies and the conditions that justified them.
- **Expiration and revalidation:** treat some permissions as temporary.
- **Independent counterevidence:** retain disconfirming results and adversarial checks.
- **Budgeted exploration:** limit compute, tool calls, and consequential effects.
- **Separation of duties:** a learner may recommend but not unilaterally authorize higher-risk actions.

A change in a boundary policy is **not** itself evidence of capability growth. Durable improvement requires performance gains that persist under controlled retesting.

## 9. Learning–Execution Decoupling

A particularly useful test holds the parameters of all execution units fixed while allowing only a boundary controller and evidence registry to change. This can isolate a form of **system-level policy learning** from intrinsic model adaptation.

However, improvements may still be explained by memorization, increased retrieval, test-set leakage, or access to more resources. Comparisons must match budgets, control memory access, and evaluate novel task families. The causal question is whether the *learned boundary policy* adds value beyond a strong static or hand-engineered routing baseline.

A useful ablation sequence is:

1. Frozen units, fixed closed policy.
2. Frozen units, uniformly permissive research policy.
3. Frozen units, expert-designed selective policy.
4. Frozen units, adaptive policy without negative evidence.
5. Frozen units, adaptive policy with counterevidence and drift monitoring.
6. Frozen units, adaptive policy with relay history disabled.

The relevant result is a difference in independently verified outcomes under matched resources—not a difference in the number of transfers attempted.

## 10. Directional Intuition, OTHERS, and Residual-Aware Boundaries

Exact matching can be overly restrictive when two domains share a useful structural core but differ in crucial details. Directional intuition can propose a transfer based on partial alignment; an OTHERS residual records what the alignment does not explain.

A boundary learner should therefore distinguish:

- **Core compatibility:** which structural relations appear reusable?
- **Residual severity:** which unmatched conditions could invalidate the transfer?
- **Evidence quality:** which claims are observed, inferred, or speculative?
- **Probe reversibility:** can the mapping be tested without consequential deployment?
- **Expected information value:** will a test meaningfully reduce uncertainty?

The residual is not a nuisance term to hide. It may be the decisive reason to require an additional validation step. A metric-native directional score can assist ranking, but the metric, its calibration, and the target context must be documented.

## 11. Multi-Level and Collective Boundary Learning

Boundaries can be learned at multiple levels:

| Level | Example adaptation | Primary attribution risk |
|---|---|---|
| Unit | Change a local representation-selection rule | Mistaking prompt sensitivity for durable learning |
| Interaction | Revise handoff conditions between two units | Confounding with added communication budget |
| Structural | Reorganize routing and shared memory | Confounding with static composition benefits |
| Relay | Prefer certain reusable evidence packages | Propagating biased or stale precedents |
| Collective | Share validated boundary precedents across teams | Mistaking transmission for independent replication |
| Evolutionary | Revise the architecture that proposes boundary policies | Recursive error amplification or uncontrolled complexity |

Cross-system relay requires provenance, local compatibility checks, and independent validation. A policy successful in one environment must not be automatically promoted to a universal boundary rule.

![Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png](../figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png)

*Fig-008. Recursive evidence-bearing relay across systems and time. Durable growth is an outcome to be tested, with negative results, saturation, and rollback explicitly represented.*

## 12. A Minimal Research Architecture

The extension proposes seven implementation-neutral components:

1. **Boundary Registry:** versioned, typed policy definitions and authority constraints.
2. **Flow Observer:** collects candidate requests, context changes, and outcomes.
3. **Prospecting Engine:** ranks candidate transfers using explicit weak evidence.
4. **Sandbox Probe Manager:** conducts bounded, preregistered tests.
5. **Evidence and Counterevidence Ledger:** retains provenance, uncertainty, and negative results.
6. **Boundary Policy Learner:** proposes scoped revisions using outcomes and histories.
7. **Governance and Relay Plane:** reviews policy updates, controls permissions, and exports reusable records.

The system should be operable with a human reviewer in the loop. The architecture is a proposed research scaffold, not a claim that these components have been implemented or validated.

## 13. Testable Hypotheses

**H1 — Adaptive selectivity:** Under distribution shift, a learned selective boundary yields higher held-out verified utility than fixed closed or uniformly open research boundaries at comparable cost.

**H2 — Counterevidence advantage:** Including negative transfer records reduces repeat failures on related tasks compared with a learner trained only on successful transfers.

**H3 — Context specificity:** Context-conditioned policies outperform a single global openness threshold on heterogeneous transfer tasks.

**H4 — Residual-aware gating:** Explicit unmatched-structure checks reduce harmful cross-domain adoption without an unacceptable loss of beneficial discoveries.

**H5 — Temporal relay:** Versioned history and repeated evaluation improve later boundary decisions beyond an equal-budget, memoryless policy.

**H6 — Drift recovery:** Policies with change detection and revalidation recover more reliably from changed task conditions than policies that retain stale permissions.

**H7 — Frozen-unit learning:** With execution-unit parameters fixed, boundary policy updates produce persistent held-out improvements beyond strong static routing and retrieval baselines.

**H8 — Governance separation:** Keeping exploratory permission distinct from execution authorization reduces unauthorized or insufficiently validated deployment events without eliminating useful low-risk probing.

These are research hypotheses, not reported findings. Null results and reversals would materially constrain the framework.

## 14. Experimental Program

### 14.1 Task environment

Construct a benchmark of multiple source–target task families with partially shared structure and deliberate mismatches. Include benign transfer opportunities, misleading analogies, stale precedents, and shifts in tool reliability or task constraints. Keep a genuinely held-out family for evaluation.

### 14.2 Experimental conditions

| ID | Condition | What it tests |
|---|---|---|
| C0 | Fixed closed boundary | Conservative baseline |
| C1 | Uniformly open exploratory boundary | Cost and risk of unrestricted probing |
| C2 | Hand-tuned selective boundary | Strong interpretable baseline |
| C3 | Learned boundary, positive evidence only | Value and limitations of reward-only learning |
| C4 | Learned boundary with counterevidence | Negative-transfer prevention |
| C5 | C4 plus residual-aware structural checks | Effect of unmatched-structure representation |
| C6 | C5 plus drift monitoring and rollback | Adaptation under changing conditions |
| C7 | C6 without historical relay | Causal contribution of temporal evidence |
| C8 | C6 with frozen execution units | Attribution of system-level learning |

Use matched compute, probe count, retrieval access, and evaluation time. Randomize task ordering where possible, report confidence intervals, and preregister primary endpoints.

### 14.3 Primary metrics

- Verified transfer utility on held-out tasks relative to a declared baseline.
- Negative-transfer frequency and severity.
- Discovery yield per probe and per compute budget.
- False admission and false rejection rates where ground truth is constructible.
- Policy stability, rollback frequency, and time to recover from drift.
- Calibration of *empirical* risk estimates, when probabilities are explicitly modeled.
- Provenance completeness and reproducibility of evidence records.
- Unauthorized action attempts and violations of permission separation.

A greater number of admitted candidates, a higher directional score, or faster policy changes alone do not count as successful intelligence growth.

## 15. Illustrative Case: Shared Planning Structure, Different Residuals

Consider a frozen planning system initially evaluated on software maintenance scheduling. A prospecting process proposes using a dependency-and-resource planning core for neighborhood service scheduling. Shared relations may include prerequisites, scarce resources, and time windows. Important residuals include travel uncertainty, human preferences, weather, and variable service durations.

A static closed policy rejects the candidate. A uniformly open policy may apply the source structure without adequate checks. A selective learned boundary might permit sandbox inspection and constrained tests, while withholding adoption until target-specific residuals are modeled. If controlled tests reveal failure on weather-dependent tasks, that negative evidence can tighten the relevant condition without banning every planning transfer.

This is a **hypothetical example**, not evidence that any particular system performs such learning. It illustrates why a learned boundary should be context-specific, evidence-sensitive, and reversible.

## 16. Contract Interfaces

**SPEC-001 — Capability and Boundary Contract:** supplies scoped capability profiles, boundary categories, attribution, and claim status. A boundary update must not silently change what a capability claim means.

**SPEC-002 — Spillover Opportunity and Evidence Contract:** supplies candidate opportunity records, weak-evidence provenance, directional assessment, and counterevidence. Exploration scores must remain distinct from verified claims.

**SPEC-003 — Prospecting, Probing, and Validation Lifecycle:** governs admission, preregistration, testing, review, and claim adjudication. Boundary learning cannot bypass Gate A or Gate B.

**SPEC-004 — Structural Relay and Collective Learning Contract:** governs export, reception, local compatibility testing, adoption, and retention of failed or contested results. A learned boundary policy is itself a versioned relay object.

Future executable schemas should define interoperable identifiers, policy change records, validation evidence, and conformance checks. The present document proposes semantic requirements rather than asserting conformance to a completed implementation.

## 17. Proposed Invariants

- **INV-01:** No boundary policy grants consequential execution authority solely from an exploratory score.
- **INV-02:** Every policy update identifies its previous version and evidence basis.
- **INV-03:** Negative and contested evidence remain accessible after a policy revision.
- **INV-04:** Boundary permissions are scoped to context, operation, and validity period.
- **INV-05:** Transfer across domains does not automatically transfer deployment authorization.
- **INV-06:** Unmatched structural residuals are recorded or explicitly marked unknown.
- **INV-07:** A successful transmission or adoption is not recorded as durable growth without follow-up evidence.
- **INV-08:** Policy changes have a rollback or safe-disable path.
- **INV-09:** Historical training and evaluation evidence are separated to reduce leakage.
- **INV-10:** System-level improvement is not automatically attributed to changes in individual execution-unit parameters.
- **INV-11:** External relay records preserve provenance and local validation status.
- **INV-12:** An uncertainty estimate is not labeled a calibrated probability without calibration evidence.

## 18. Conformance Test Sketches

| Test | Stimulus | Required result |
|---|---|---|
| CT-01 | Weak evidence with high prospect score | Probe may be proposed; deployment remains unauthorized |
| CT-02 | Positive result without declared baseline | Claim upgrade is rejected or deferred |
| CT-03 | Negative result contradicting an earlier success | Both records remain visible; review is triggered |
| CT-04 | Transfer with critical unmapped residual | Additional checks or constrained rejection |
| CT-05 | Policy update with missing provenance | Update is blocked |
| CT-06 | Changed target context after validation | Revalidation requirements are evaluated |
| CT-07 | New policy causes regression | Rollback or safe-disable is available |
| CT-08 | External relay marked “validated” elsewhere | Local validation is not silently inferred |
| CT-09 | Frozen execution units improve on held-out tasks | Attribution is system-level unless contrary evidence exists |
| CT-10 | Uncalibrated directional score presented as success probability | Record is rejected or corrected |
| CT-11 | Repeated execution without retained observations | No learning claim is recorded |
| CT-12 | Policy requests expanded operational privileges | Separate authorization is required |

These tests are proposals for future implementation and should be supplemented by schema validation, security review, and adversarial test cases.

## 19. Failure Modes and Counterarguments

**Complexity may outweigh benefit.** A learned boundary controller can add latency, memory overhead, and operational fragility. A well-designed static policy may win under stable tasks.

**Boundary learning may overfit its own history.** The controller can learn which probes look good on familiar data rather than which transfers generalize. Held-out evaluation and changing-task tests are essential.

**Negative evidence can be misleading.** A failed transfer may reflect poor execution or inadequate resources rather than intrinsic incompatibility. The evidence record should retain causal uncertainty.

**The learner may become excessively conservative.** Overweighting failure can suppress valuable novelty. Discovery yield and false rejection must be measured alongside risk reduction.

**The learner may become excessively permissive.** Optimizing short-term reward can create hidden externalities, evidence contamination, or unsafe action paths. Hard permission boundaries and independent oversight remain necessary.

**System learning may be ordinary engineering optimization.** Better routing, caching, or retrieval is not automatically a new category of intelligence. Claims of novelty require comparison to established adaptive control, meta-learning, contextual bandits, multi-agent learning, and policy optimization.

**Relay can spread systematic error.** Shared evidence registries can amplify common biases and correlated mistakes. Provenance, diversity of evidence, and independent replication matter.

**No AGI conclusion follows.** Even durable improvements in boundary policies do not establish open-ended general intelligence or recursive self-improvement. They support, at most, a specific measured form of adaptive system behavior.

## 20. Five-Phase Validation Roadmap

**Phase 1 — Contract and baseline:** Implement a minimal typed boundary record, strong static baselines, and a held-out task split. Verify that permission separation works before adding learning.

**Phase 2 — Evidence-aware adaptation:** Add versioned positive and negative evidence, explicit residuals, and a conservative update mechanism. Measure negative transfer and cost.

**Phase 3 — Context and drift:** Introduce heterogeneous target contexts and distribution shifts. Evaluate stability, recovery time, and rollback behavior.

**Phase 4 — Temporal and collective relay:** Allow independent research runs to exchange policy evidence packages. Test whether cross-run relay improves decisions beyond equal-budget local memory.

**Phase 5 — Replication and scope revision:** Release protocols, schemas, failure cases, and reproducible benchmarks. Narrow or reject hypotheses that do not survive independent tests.

A phase should not be declared successful merely because its software components are implemented. Each phase needs predefined evidence thresholds and counterfactual comparisons.

## 21. Open Questions

1. What is the minimal useful state representation for learning a boundary without overfitting?
2. Can residual severity be estimated reliably without forcing every domain into one metric space?
3. How should a learner trade exploration value against irreversible downside risk?
4. Which policy changes require independent review rather than automated acceptance?
5. How much of apparent fluidity is explained by retrieval and routing alone?
6. When does evidence from one context justify opening a boundary in a related context?
7. Can negative evidence be transferred without making the system systematically timid?
8. How should collective registries handle contradictory results and incompatible evaluation protocols?
9. What constitutes a durable boundary-learning gain under continual distribution shift?
10. Can boundary learning help discover new structural units, rather than only choose among known ones?
11. How do privacy, sovereignty, and organizational trust constrain evidence relay?
12. Which observations would decisively falsify the claim that learned boundaries improve intelligence fluidity?

## 22. Collective Learning and Research Relay Invitation

This extension is intended as an **open, falsifiable research proposal**. Useful contributions include strong static baselines that defeat adaptive policies, examples where negative evidence prevents genuine discovery, datasets exposing misleading analogies, formal models of contextual permeability, interoperable policy schemas, and independently reproduced null results. Such contributions may be more informative than another positive demonstration on a familiar benchmark.

Contributors should preserve the distinction between a proposed mechanism, a simulated illustration, a measured result, and an independently replicated result. Any future implementation should document its authority model and the precise scope of permitted automation.

## 23. Conclusion

Intelligence fluidity may depend not only on what a system can transfer, but also on whether it can **learn when, where, and how transfer is appropriate**. The proposed boundary-learning framework combines contextual selectivity, weak-evidence prospecting, explicit residuals, controlled probing, counterevidence preservation, versioned policy updates, and structural relay. It treats openness as an evidence-sensitive research decision rather than a universal virtue.

The central empirical challenge remains open: **does learning the boundaries of intelligence flow produce verified, durable improvements over simpler alternatives under comparable cost and risk?** A convincing answer requires controlled experiments, negative results, and independent replication—not architectural plausibility alone.

---

## Related Research Areas

Adaptive control; contextual bandits; meta-learning; continual learning; domain adaptation; selective prediction and abstention; safe exploration; multi-agent coordination; concept drift detection; knowledge transfer; organizational learning; provenance and reproducible science. These are relevant comparison areas, not claims that ISGFTR supersedes existing work.

**Document status:** Directional extension for open research. No empirical validation, calibrated probability estimates, AGI demonstration, or production-ready safety guarantee is claimed.
