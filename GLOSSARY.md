# GLOSSARY — Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)

**Version:** 1.0.0 (theory-first)  
**Status:** Working research terminology, open to revision  
**Scope:** ISGFTR-001–010; SPEC-001–004; CASE-001–003; EXT-001–003

> This glossary supplies operational definitions for an open research program. Terms do not imply empirical validation. Every capability claim must specify its subject, task, resources, conditions, measurement protocol, evidence, and uncertainty.

## 1. Five characteristics of intelligence flow

### Intelligence Spillover
Useful behavior or capability observed outside the task, representation, domain, or use case for which a system was primarily trained, designed, or assessed. Spillover is a phenomenon to investigate; it does not prove that the capability was newly learned or that the system has general intelligence. Pretraining coverage, prompting, tools, and task similarity are alternative explanations.

### Generalization
Adequate performance on relevant variations beyond the evaluated examples. Specify the shift—instances, domains, tasks, constraints, or environments—and the evaluation conditions. Generalization is not automatically unlimited transfer.

### Intelligence Fluidity
The context-sensitive capacity of intelligence-related structures, information, strategies, or resources to be redirected across representations, tasks, tools, units, and boundaries. **Fluidity is not the same as utility or learning.**

### Intelligence Transfer
Attempted or evidenced reuse of knowledge, strategies, structural cores, or capabilities from a source context in a target context. Transfer can be beneficial, neutral, or harmful. Demonstrating transfer requires appropriate controls and causal attribution.

### Intelligence Relay
Transmission of intelligence-related artifacts or effects across units, subjects, systems, or time. Examples include plans, evidence, reusable structures, failure records, and questions. Successful transmission does not establish correct interpretation, adoption, utility, or durable growth.

## 2. Capability and four boundaries

### Capability
A scoped ability of an identified model or system to accomplish an outcome under stated task, resource, environment, and evaluation conditions. See [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md).

### Capability Profile
A versioned description of a subject's demonstrated and hypothesized abilities, evaluation conditions, evidence, limitations, and claim states. Hypotheses must not silently become validated capabilities.

### Generative Boundary
The behaviors or outputs that a specified generating mechanism can produce under defined conditions. This is not necessarily what an entire tool-using system can achieve.

### Observed Boundary
The capabilities actually evidenced by specified tests or observations. It depends on coverage, reliability, and the scope of evaluation.

### Reachable Boundary
The outcomes currently attainable by the whole specified system with its available tools, orchestration, memory, resources, and permissions.

### Evolvable Boundary
A hypothesis about future attainable outcomes under permitted adaptation of the system's components, organization, tools, or learning processes. **It is not a demonstrated limit or guarantee.**

### Capability Frontier
A multidimensional, evidence-dependent distinction between established capability and unverified or unreachable opportunities. The four boundaries need not be strictly nested geometric sets.

### Evolvable Intelligence Potential
The hypothesized ability of a system to expand future reachability through changes to structures, policies, tools, evidence processes, or learning organization. It must be assessed longitudinally.

### Capability Prospect
An unverified candidate capability or transfer opportunity with a rationale, uncertainty, possible counterevidence, and a proposed probe. **A prospect is a question, not an answer.**

## 3. Folding, generalization, and structural reuse

### Structural Folding
Extraction or compression of potentially reusable relations, invariants, or procedures from detailed task structures. Folding can help reuse but may lose important information.

### Structural Unfolding
Adaptation of a folded structure to a target context, restoring or adding target-specific constraints and residuals. It need not be a lossless inverse of folding.

### Folding–Generalization Duality
The hypothesis that reusable structural abstraction can facilitate generalization, while generalization results can test the adequacy of an extracted core. This is not an established mathematical equivalence.

### Shared Structural Core
A set of relations, constraints, invariants, or procedures hypothesized to remain useful across contexts. Similar language alone does not demonstrate a shared core.

### Domain-Specific Residual
Constraints, exceptions, features, or information not safely captured by the common core. Residual preservation helps prevent false analogy and negative transfer.

### Structural Reuse
Applying a previously identified structure in a new setting. Reuse is not necessarily new learning and must be tested against appropriate baselines.

### Uncertainty Preservation
Explicitly retaining confidence limits, unresolved alternatives, assumptions, and provenance during folding or relay.

### Uncertainty Recovery
Using later experiments, evidence, or calibration to reconstruct uncertainty that was not fully retained. Recovery may be imperfect or impossible.

### Two-Phase Structural Search
A process separating candidate discovery, which may use weak evidence, from independent validation with stronger evidence and predefined criteria.

## 4. Directional intuition, evidence, and scoring

### Directional Intuition
A lightweight heuristic that proposes promising transfer or exploration directions from partial structure, analogy, context, or prior outcomes. It is a discovery aid, not proof.

### Weak Evidence
Preliminary, indirect, incomplete, or uncertain information that may warrant a bounded probe but cannot independently support a strong capability claim.

### Directional Scoring
Ranking prospects using factors such as structural fit, information value, costs, risks, and uncertainty. An exploration score is **not a calibrated probability** without separate calibration evidence.

### Metric-Native Directional Scoring
Evaluating candidate directions using meaningful domain-native metrics or relations rather than requiring a universal Euclidean embedding.

### Perspective
An explicit viewpoint specifying whose objectives, constraints, costs, and evidence determine the evaluation. Transfer value may change with perspective.

### OTHERS Residual
Unmatched, weakly matched, or unexplained factors retained outside a principal similarity assessment. Such residuals may identify crucial transfer risks or opportunities.

### Evidence Item
A traceable observation, experiment result, analysis, or counterexample with source, method, conditions, and limitations.

### Evidence Bundle
A structured collection of supporting and opposing evidence for a scoped prospect or claim, including provenance and uncertainty. See [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md).

### Counterevidence
Evidence that contradicts, weakens, or narrows a claim. It must be preserved in research and relay records.

### Negative Transfer
Measurable deterioration in target-task quality, reliability, cost, or safety attributable to attempted transfer relative to a suitable baseline.

### Provenance
Traceable origins and transformations of data, claims, evidence, and structural artifacts, supporting audit and replication.

### Claim State
The evidence-governed status of a claim, such as *hypothesized*, *under probe*, *observed*, *replicated*, *contested*, or *retracted*. Claim state does not itself authorize deployment.

## 5. Permeability and validation governance

### Structural Boundary
An interface or separation among representations, tasks, tools, subjects, systems, trust zones, or permissions.

### Selective Structural Permeability
Permitting some information or structural flows across boundaries while restricting others based on context, evidence, risk, and governance. Neither total openness nor total closure is presumed optimal.

### Permeability Controller
A proposed policy component that evaluates candidate boundary crossings and decides whether to block, observe, probe, or request authorization for adoption.

### Flow Policy
A context- and evidence-dependent mapping to permitted transfer actions. Policies may adapt through feedback but remain subject to hard constraints.

### Observe / Probe / Adopt / Deploy
Four distinct permissions: inspect information; test in a bounded experiment; integrate a supported structure into an authorized workflow; and use it operationally. **Permission at one level does not grant the next.**

### Gate A — Exploration Admissibility
A decision about whether an unverified prospect merits a controlled experiment given its relevance, evidence, cost, and risk. Gate A does not validate capability.

### Gate B — Scoped Claim Adjudication
A decision about which claims, if any, are supported by reviewed experimental evidence and under which conditions.

### Probe
A bounded experiment with specified hypothesis, controls, metrics, resources, and stopping conditions. See [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md).

### Contract Invariant
A property that must hold for valid records and transitions, such as no unsupported claim upgrade or silent deletion of counterevidence.

### Conformance Test
A check that a record, workflow, policy, or relay unit satisfies a declared contract. **Conformance before runtime** emphasizes explicit specifications and tests before operational reliance.

## 6. System-centric and multi-level learning

### System-Centric Intelligence
Capability attributable to an organized system of interacting models, tools, memory, policies, and feedback rather than a single component. This is a research perspective, not proof of AGI.

### Learning–Execution Unit Decoupling
Separation between units executing tasks and mechanisms accumulating or applying learning. For example, frozen models may be coordinated by a changing routing and evidence system.

### Frozen-Unit Structural Learning
Persistent system improvement with fixed execution-unit model parameters, potentially through updated memory, routing, structural decomposition, or evaluation. Attribution requires controls for leakage and changing resources.

### Unit Learning
Adaptation of an individual execution or decision unit.

### Interaction Learning
Improvement in communication, role allocation, coordination, or feedback among units.

### Structural Learning
Improvement through changes to task decomposition, organization, reusable components, or policies.

### Relay Learning
Improvement in later decisions due to transmitted evidence or structures from earlier units, tasks, or execution cycles.

### Collective Learning
Learning whose useful outcomes are distributed across participants through shared evidence, structures, and coordination. A shared repository alone does not prove learning.

### Evolutionary Learning
Change across generations or populations of designs through variation, selection, recombination, and retained evaluation.

### Credit Assignment
Determining which unit, policy, structural change, or evidence item caused an observed outcome, particularly in complex systems.

## 7. Relay, recursion, and growth

### Structural Relay Unit (SRU)
A portable, versioned research package containing a hypothesis, reusable structure, evidence, limits, residuals, and reproduction guidance. Receiving an SRU does not imply correctness or local suitability. See [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md).

### Spatial Relay
Transmission across units, subjects, organizations, or systems.

### Temporal Relay
Transmission across execution cycles or research generations through records, memories, and revised structures.

### Repetition as Evidence Relay
Repeated execution can accumulate observations that support future learning, even without immediate gains. **Repetition alone is not learning.**

### Recursive Relay
A feedback loop in which relay results inform future prospect selection, experimentation, structure, or policy. A loop is not automatically self-improving.

### Mobility / Utility / Durable Growth
**Mobility:** a structure can be transmitted or accessed. **Utility:** it improves an evaluated outcome. **Durable growth:** improvement persists or expands future capability under controlled assessment. These are separate claims.

### Performance Growth
Improvement on a measured task under specified conditions; it may be narrow or transient.

### Reachability Growth
Expansion of outcomes currently attainable by a system under specified resource and organizational conditions.

### Learning-Process Growth
Improvement in the system's ability to discover, test, retain, or transfer future capabilities.

### Recursive Self-Improvement (RSI)
A process where changes to a system's own improvement mechanisms enable further improvements. Recursive relay does not prove RSI without causal evidence.

### Residual-Based Growth
Growth motivated by explicitly retained failures, unmet requirements, exceptions, or unresolved questions.

### Open-Ended Growth
A research possibility that useful new structures and capabilities may continue emerging through exploration and adaptation. It does not mean unlimited resources or inevitable AGI.

## 8. Capability prospecting and collective research

### Capability Prospecting
Systematic discovery and prioritization of unverified spillover or transfer opportunities. The proposed cycle is **Prospect → Probe → Validate → Relay → Learn → Prospect**.

### Prospect Portfolio
A set of candidates selected under shared constraints on budget, diversity, uncertainty, risk, and expected information value.

### Information Value
The expected decision-relevant reduction in uncertainty from an experiment, including informative negative outcomes.

### Research Residual
An unresolved discrepancy, failure, untested assumption, or open question preserved for future study.

### Collective Evidence Registry
A proposed shared index of claims, experiments, evidence, replications, counterevidence, and relay artifacts, with provenance and versioning.

### Research Governance
Policies controlling authorization, experimental conduct, claim strength, evidence handling, adoption, deployment, and revision.

### Open Research Architecture
A proposed organization of prospecting, experiment, evidence, structural relay, and governance planes. See [ISGFTR-010](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md).

## 9. AGI interpretations and limits

### Artificial General Intelligence (AGI)
A contested concept concerning broadly capable intelligence across varied tasks and contexts. ISGFTR does not assume a universally accepted operational definition or claim that its mechanisms suffice for AGI.

### Model-Centric AGI Hypothesis
A pathway emphasizing broad competence arising primarily from individual models.

### System-Centric AGI Hypothesis
A pathway investigating whether broad adaptive competence can emerge through organized and learning systems of individually limited components.

### Hybrid AGI Hypothesis
A pathway combining strong individual models with adaptive tools, memory, organization, and system-level learning.

### Biological Analogy
A comparison to cognition, nervous systems, animal groups, or human organizations used to generate testable ideas, **not** to establish algorithmic equivalence.

### Falsifiable Hypothesis
A proposition specifying observable outcomes that could weaken or reject it, with baselines, scope, alternative explanations, and counterexamples.

## 10. Essential distinctions

| Do not conflate | Reason |
|---|---|
| Spillover vs. new learning | The ability may already be latent or supported by tools |
| Similarity vs. structural equivalence | Crucial constraints may differ |
| Folding vs. generalization | Compression may lose necessary structure |
| Directional score vs. probability | Ranking need not be calibrated |
| Weak evidence vs. validated capability | Discovery is not confirmation |
| Permeability vs. authorization | Information access is not deployment permission |
| Relay vs. successful adoption | Recipients may misinterpret or reject artifacts |
| Repetition vs. learning | Accumulation need not change future behavior |
| System learning vs. model learning | Improvements may arise outside model weights |
| Performance vs. durable growth | A benchmark gain may not persist or transfer |
| Recursive relay vs. RSI | Feedback need not improve the improvement process |
| Open-ended exploration vs. AGI | Generating possibilities does not establish broad competence |

## 11. Reading and cross-reference guide

- **Boundaries and five characteristics:** [ISGFTR-001](docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md), [ISGFTR-002](docs/ISGFTR-002-Five-Characteristics-of-Intelligence-Spillover-and-Relay.md).
- **Folding and fluidity:** [ISGFTR-003](docs/ISGFTR-003-Folding-Generalization-Duality-and-Structural-Reuse.md), [ISGFTR-004](docs/ISGFTR-004-Intelligence-Fluidity-and-Permeable-Structural-Boundaries.md).
- **Directional evidence and prospecting:** [ISGFTR-005](docs/ISGFTR-005-Directional-Intuition-and-Weak-Evidence-Transfer.md), [ISGFTR-008](docs/ISGFTR-008-Intelligence-Spillover-and-Transfer-Prospecting.md), [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md).
- **System learning and relay:** [ISGFTR-006](docs/ISGFTR-006-System-Centric-Intelligence-and-Multi-Level-Learning.md), [ISGFTR-007](docs/ISGFTR-007-Recursive-Relay-and-Open-System-Intelligence-Growth.md), [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md).
- **Governance and validation:** [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md), [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md).
- **AGI limits and research architecture:** [ISGFTR-009](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md), [ISGFTR-010](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md), [EXT-003](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md).

## 12. Revision and collective learning

Definitions here are provisional and may be contested. Contributors are encouraged to supply counterexamples, clearer operational criteria, alternative terminology, and evidence-based revisions. Updates should preserve provenance and identify any consequences for existing contracts or prior claims.

**Working principle:** *Name the boundary, state the evidence, preserve the residual, and keep the claim revisable.*
