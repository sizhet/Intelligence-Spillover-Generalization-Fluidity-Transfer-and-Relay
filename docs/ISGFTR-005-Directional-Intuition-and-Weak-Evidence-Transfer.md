# ISGFTR-005 — Directional Intuition and Weak-Evidence Transfer

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Document type:** Directional research hypothesis, conceptual mechanisms, and testable research agenda  
**Version:** v1.0.0  
**Status:** Open research proposal; hypotheses and illustrative mechanisms are not established experimental findings

## Abstract

Intelligence transfer is often recognized only after a system has demonstrated competence in a new task. This retrospective view can miss promising transfers whose evidence is incomplete, non-isomorphic, or difficult to express formally. This paper examines **directional intuition** as a proposed, low-cost mechanism for generating *testable* cross-domain transfer hypotheses from weak, partial, and heterogeneous evidence. It distinguishes the discovery of a potentially useful direction from the verification of a transferable capability. Building on the ISGFTR framework and connecting to the earlier Beyond Matching: OTHERS and Directional Weak Evidence Intelligence (BM-ODWEI) and Metric-Directional Intuition (MDI) research proposals, it outlines evidence types, directional scoring, selective structural permeability, two-phase search, counter-evidence, and relay of validated results. The paper does not assert that human intuition follows a single algorithm, that weak signals imply successful transfer, or that these mechanisms establish AGI. Its purpose is to make an attractive but uncertain hypothesis explicit enough for controlled comparison and collective refinement.

**Keywords:** directional intuition; weak evidence; transfer learning; structural analogy; intelligence fluidity; OTHERS; metric-native scoring; two-phase search; negative transfer; capability prospecting; structural relay

## 1. Motivation: The Discovery Problem Before Transfer

Transfer is often studied after source and target tasks have been identified. Yet the selection of a target is itself a difficult intelligence problem. A model, agent, or structural unit may have capabilities that are not obvious from its original task description. A human researcher can notice a vague resemblance between two domains and investigate it without first proving a complete structural mapping. A machine system may similarly benefit from a *hypothesis-generating* stage that tolerates incomplete evidence.

The motivating question is not, “Can weak evidence prove that a transfer will succeed?” It cannot. The question is: **Can weak, directionally informative evidence improve the allocation of limited experiments to previously untested transfers?**

A useful distinction is between three events:

1. **Candidate discovery:** a possible source–target connection is proposed.
2. **Transfer verification:** an intervention shows that source knowledge or a reusable structure improves a target outcome relative to an appropriate baseline.
3. **Capability retention:** the improvement persists, generalizes, or can be reliably relayed to subsequent tasks.

Only the first event is directly addressed by directional intuition. The other two require experiments and evidence governance.

## 2. Position in the ISGFTR Framework

ISGFTR identifies spillover, generalization, fluidity, transfer, and relay as related but distinct properties. Directional intuition is proposed as a *front-end discovery mechanism* that may help a system identify where to attempt transfer. It is not a sixth property and does not replace the five-part framework.

- **Spillover:** an existing capability proves useful beyond its original intended purpose.
- **Generalization:** competence survives changes in task conditions or distributions.
- **Fluidity:** a system adaptively redirects problem-solving activity across available boundaries.
- **Transfer:** knowledge or structure from a source makes a measurable contribution to a target.
- **Relay:** a task, result, representation, or experience is passed across units or time.

Directional intuition may propose a crossing; selective permeability may admit it into an exploratory sandbox; a transfer test determines whether it is useful; relay can preserve the resulting evidence. This sequence must not be collapsed into a claim that every plausible analogy constitutes intelligence growth.

## 3. Working Definitions

### 3.1 Directional Intuition

> **Directional intuition** is a provisional, resource-bounded process that ranks possible next exploration directions using incomplete structural, contextual, historical, or relational evidence, without requiring a fully verified source–target equivalence in advance.

“Intuition” is an engineering metaphor here, not a claim of consciousness or a complete neuroscientific model. Its defining output is a *candidate direction with uncertainty*, not a certified answer.

### 3.2 Weak Evidence

> **Weak evidence** is information that is potentially relevant to a transfer hypothesis but insufficient on its own to establish that the transfer will succeed.

Weakness may arise from small samples, indirect relevance, noisy measurements, incomplete mappings, uncertain provenance, or untested causal assumptions. A signal can be weak but useful for prioritization; it can also be misleading.

### 3.3 Directional Transfer Hypothesis

A directional transfer hypothesis specifies a source capability, target task, proposed relationship, expected gain, uncertainty, and a feasible falsification probe. For example: “A planner trained for route constraints might help schedule constrained laboratory workflows because both require resource-aware sequencing.” This is a candidate, not evidence that the planner works on the laboratory task.

### 3.4 Non-Equivalence as a Design Condition

The source and target need not be formally identical to warrant exploration. However, a transfer that works must ultimately show a defensible mechanism and measurable improvement. **Exploratory non-equivalence is permitted; unverified operational equivalence is not.**

## 4. Sources of Directional Evidence

A candidate may draw on several distinct signals:

| Evidence family | Example signal | Common failure mode | Suggested check |
|---|---|---|---|
| Shared structural core | similar dependency or constraint pattern | superficial analogy | map decisive relations |
| Functional or goal affinity | similar optimization pressure | different objective semantics | compare target outcomes |
| Perspective transformation | a new view exposes a useful correspondence | cherry-picked perspective | evaluate competing views |
| Historical precedents | similar transfers worked previously | selection and survivorship bias | retain failed trials |
| Directional or metric-native cues | locally useful gradients, rankings, orderings | incompatible geometry or scale | probe under target metric |
| Residual compatibility | source fills a known target gap | missing prerequisite capability | isolate residual and intervention |
| Relay accessibility | tools, memory, or peers make transfer feasible | interface or provenance mismatch | test contract and handoff |
| OTHERS / unexplained residual | recurring weak anomaly not captured by existing features | noise disguised as novelty | require cheap discriminating probe |

The **OTHERS** category should never be treated as a free bonus. Each residual signal needs a provenance record, a proposed interpretation, an uncertainty annotation, and a path to counter-evidence. Unexplained observations are a reason to investigate, not to believe.

## 5. From Matching to Directional Guidance

Exact matching and complete structural isomorphism are useful when available, but they can be too restrictive at the candidate-discovery stage. Directional guidance asks a weaker question: **If we invest one more experiment, which transfer hypothesis is worth testing next?**

The proposed shift is:

`Exact match required → partial correspondence admitted → directional candidate ranked → targeted probe → validated or rejected transfer`

This is compatible with formal methods. The formal gate moves from *before candidate generation* to *before consequential deployment or durable capability claims*.

### 5.1 Metric-Native Rather Than Mandatory Euclidean Embedding

Not every transfer direction needs a common vector embedding. Some tasks have native structures—graphs, partial orders, programs, symbolic constraints, causal relations, or domain-specific distances. A candidate can be evaluated using the metric or ordering appropriate to its representation, provided that the score is interpretable and testable.

This does **not** imply that a metric-native score is always better than an embedding-based one. It proposes a comparison: when does preserving the native structure produce more useful discovery rankings than projecting all candidates into a shared vector space?

### 5.2 Perspective-Indexed Directions

A candidate's apparent transferability may change with perspective: semantic, operational, causal, temporal, cost-sensitive, or safety-sensitive. The evaluator should retain perspective identifiers rather than average away disagreements prematurely. A promising semantic analogy may fail an operational compatibility check.

## 6. A Minimal Directional Transfer Opportunity Record

A candidate opportunity can be represented as:

\[
O=(I_s,T_t,P,M,E^+,E^-,R,C,V)
\]

where:

- \(I_s\): source intelligence unit or capability;
- \(T_t\): target task or capability gap;
- \(P\): evaluation perspective;
- \(M\): proposed source–target mapping or transformation;
- \(E^+\): supporting evidence;
- \(E^-\): counter-evidence and known failure cases;
- \(R\): accessible relay resources and interfaces;
- \(C\): cost, safety, and execution constraints;
- \(V\): a specified probe and validation criterion.

The record should also contain provenance, timestamp or version, status (`proposed`, `probed`, `validated`, `rejected`, `inconclusive`), and a **leftover** field for unresolved residuals. This is a conceptual contract, not a mandated runtime schema. The canonical interface is deferred to `SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md`.

## 7. Directional Scoring: Priority Is Not Probability

A first-generation evaluator should produce an **exploration priority**, not an unearned claim of transfer-success probability. One possible abstract ranking is:

\[
S_{\mathrm{dir}}(O)=F\bigl(A_s,D_p,H,R_b,G_r,U,C,K\bigr)
\]

where \(A_s\) is structural affinity, \(D_p\) directional compatibility under perspective \(P\), \(H\) historical precedent, \(R_b\) relay feasibility, \(G_r\) residual-bridging potential, \(U\) uncertainty, \(C\) cost, and \(K\) risk or governance constraints. The aggregation function \(F\) is deliberately unspecified: linear weighted sums, Pareto ranking, constrained policies, and learned ranking models are competing hypotheses.

For experiments with calibrated probabilities and comparable utility units, a decision-theoretic expression may be tested:

\[
\operatorname{EVI}(O)=p_{\mathrm{success}}(O)\,G(O)-C(O)-R(O)+\lambda\,IG(O)
\]

Here \(G\) is expected gain conditional on success, \(R\) expected risk cost, and \(IG\) expected information gain. The expression is *illustrative*, not a validated estimator; terms must be measured consistently and double-counting avoided. Without calibration, report rank or score only—not a percentage probability.

### 7.1 Multi-Strategy Scoring

A single similarity function risks reproducing its own blind spots. A portfolio may combine conservative structural matching, directional weak-evidence ranking, historical precedent retrieval, and an explicit exploration allocation for high-uncertainty candidates. A control plane should record which policy selected each probe and why.

### 7.2 Uncertainty and Abstention

The evaluator should be able to say “insufficient evidence,” decline to rank incomparable opportunities, and request a discriminating test. A high novelty score is not a substitute for safety or evidence quality.

## 8. Two-Phase Search and Selective Permeability

**Phase I — Exploratory Guidance:** generate and cheaply rank candidates using weak evidence, analogies, partial structures, native metrics, and OTHERS residuals. Keep the sandbox low-cost, reversible, and appropriately permissioned.

**Phase II — Verification and Relay:** perform controlled tests against baselines; check source–target compatibility, provenance, constraints, and negative transfer; promote only supported claims to reusable capability records.

This separation is a proposed **two-gate principle**:

1. **Exploration gate:** low threshold for considering a hypothesis, with strict budget and risk controls.
2. **Operational gate:** evidence- and contract-based threshold before consequential execution, deployment, or persistent claims.

A hypothesis can remain interesting without passing the second gate. Its failure should still be recorded as informative evidence.

## 9. Connection to Intelligence Fluidity

ISGFTR-004 proposes that adaptive systems may benefit from selectively permeable boundaries. Directional intuition supplies a candidate route for crossing a boundary; permeability policy determines whether exploratory information may pass; validation determines whether the resulting operation is acceptable.

A useful abstraction is a flow policy:

\[
\pi_{\mathrm{flow}}(a\mid x,O,\mathcal{B})
\]

where \(a\) is a possible next action (probe, transform, request help, abstain), \(x\) the context, \(O\) the opportunity record, and \(\mathcal{B}\) the applicable boundaries and permissions. Whether such a policy can be learned better than fixed routing is an empirical question.

**Boundary openness is not itself a virtue.** Too little permeability misses useful transfers; too much produces distraction, negative transfer, unsafe execution, and evidence contamination.

## 10. Connection to Biological Intuition: Inspiration, Not Equivalence

Human cognition can generate analogies and action tendencies from partial cues before explicit explanation is available. Distributed representations, associative retrieval, attention, and cognitive control provide plausible inspirations for artificial directional guidance. Yet human intuition is also prone to confirmation bias, false analogy, and overconfidence.

This paper does not claim that a specific neural circuit implements BM-ODWEI, metric-native scoring, or the proposed two-gate procedure. A biomimetic comparison should identify measurable functional correspondences rather than infer algorithmic identity from surface resemblance.

A productive research question is whether **low-formality candidate generation followed by disciplined testing** can capture some of the exploration advantages of intuition without inheriting its most costly errors.

## 11. From Directional Transfer to Structural Relay

When a probe yields useful evidence, the outcome should become a portable research artifact:

`source + target + perspective + mapping + probe + baseline + result + uncertainty + counter-evidence + next questions`

A receiving unit can repeat the test, adapt the mapping, or reject the result. Relay may be **spatial** (between agents, teams, tools, or domains) or **temporal** (across repeated trials, revisions, and accumulated memory). Repeated execution can itself generate evidence, even when no new structure is created.

But the relay must not silently upgrade an exploratory score into a validated capability. A provenance-preserving chain distinguishes *candidate*, *tested transfer*, and *retained improvement*.

## 12. Failure Modes and Adversarial Cases

1. **False analogy:** shared vocabulary masks incompatible causal or operational structure.
2. **Negative transfer:** a source capability degrades target performance relative to a no-transfer baseline.
3. **Selection bias:** only successful transfer stories enter historical memory.
4. **Evidence laundering:** repeated relay makes an unverified hypothesis appear established.
5. **Metric gaming:** the evaluator optimizes proxy similarity rather than useful target outcomes.
6. **OTHERS inflation:** unexplained residuals become a universal excuse to pursue arbitrary ideas.
7. **Search-cost explosion:** too many candidate directions exhaust exploration budgets.
8. **Boundary violation:** a speculative direction triggers unauthorized or irreversible actions.
9. **Distribution shift:** a score calibrated in one domain fails elsewhere.
10. **False growth claims:** one-off success is reported as durable new intelligence.

Every study should report failed probes, abstentions, and cost-adjusted outcomes, not only impressive examples.

## 13. Testable Hypotheses

**H005-1 — Weak-evidence discovery gain.** Under matched budgets, a directional evaluator using weak structural evidence discovers more *validated, previously unobserved* useful transfers than random candidate selection.

**H005-2 — Complementarity.** A diversified portfolio of exact-match and weak-evidence strategies outperforms either alone on a mixture of near and distant transfers.

**H005-3 — Native-structure advantage in selected domains.** Metric-native or graph-native guidance improves discovery efficiency relative to a shared embedding baseline on tasks where critical relations are poorly preserved by that embedding.

**H005-4 — Two-gate reliability.** Exploratory admission plus independent validation produces fewer unsupported operational transfers than a single permissive gate at comparable discovery budgets.

**H005-5 — Counter-evidence benefit.** Explicitly storing failed mappings and counter-evidence reduces repeated negative-transfer probes over successive evaluation rounds.

**H005-6 — Relay learning benefit.** Provenance-preserving evidence relay improves future candidate ranking or reduces duplicated exploration cost relative to a system that discards probe history.

Each hypothesis may fail. Null results should narrow the applicable conditions rather than be reclassified as success.

## 14. Controlled Experimental Design

### 14.1 Candidate Space

Construct a suite of source capabilities and target tasks spanning near, moderate, and distant structural relations. Include intentionally deceptive analogies and targets with no useful source transfer. Freeze task splits before scoring where feasible.

### 14.2 Baselines

Compare at least: random selection; lexical or embedding similarity; exact structural matching; historical precedent retrieval; directional weak-evidence scoring; and a combined multi-strategy policy. Match compute, number of probes, access to task metadata, and human assistance.

### 14.3 Measurements

- **Validated discovery yield:** confirmed useful transfers per fixed probe budget.
- **Precision among selected probes:** fraction meeting a preregistered improvement threshold.
- **Negative-transfer rate:** fraction that harm target performance.
- **Cost per validated discovery:** total search and evaluation cost divided by successes.
- **Calibration:** proper scoring metrics only if probabilities are explicitly predicted.
- **Information value:** reduction in uncertainty or improved later ranking after failures and successes.
- **Relay retention:** repeatability and reuse of the validated improvement across time or new tasks.

### 14.4 Controls and Leakage Prevention

Separate candidate-generation data from held-out transfer tests; audit retrieval for target answers; control model versions and prompting; distinguish tool-assisted gains from source-capability transfer; report variance across seeds, tasks, and evaluator policies. Where feasible, preregister success criteria and use blinded target labels.

### 14.5 Minimal MVP

Begin with a small capability inventory and 20–50 candidate source–target pairs, including known negative controls. Use a fixed probe budget and simple ranking functions. Test whether weak-evidence guidance finds additional validated transfers without unacceptable false positives or cost. The number of pairs is illustrative, not a statistical power claim; sample size should be justified for the intended inference.

## 15. Relationship to Capability Prospecting and AGI

ISGFTR-008 develops the broader idea of **Intelligence Spillover and Transfer Prospecting**: actively searching for capabilities that have not yet been demonstrated. Directional intuition is one candidate front-end for such prospecting, while controlled probes establish the observed frontier.

Even a successful prospecting system does not establish an unlimited capability frontier or guarantee AGI. It may simply make better use of existing capabilities. Claims about *growth* require evidence of durable new competence beyond temporary routing or tool access; claims about *generality* require broad, diverse evaluation.

The distinction among **intrinsic**, **accessible**, and **evolvable** intelligence remains a research proposal, not a set of directly additive quantities.

## 16. Open Questions for Collective Learning

1. What evidence types reliably indicate transfer beyond lexical or embedding similarity?
2. Can directional guidance work with incomparable native metrics without hiding arbitrary normalization choices?
3. How should weak evidence, counter-evidence, and unexplained residuals be weighted under scarce data?
4. What is the smallest useful transfer-opportunity contract for independent research groups?
5. Can a system learn when to abstain, request a probe, or escalate to a more formal verification gate?
6. Which domains benefit from weak-evidence exploration, and which require strong formal constraints from the outset?
7. Does the value of directional intuition persist when all candidate-generation and validation costs are counted?
8. Can evidence relay reduce repeated errors without locking the community into early mistaken assumptions?
9. What would falsify the claim that a distinct directional-intuition mechanism is useful beyond standard retrieval and active learning?
10. How can independent teams contribute negative results and preserve comparability across versions?

## 17. Research Context, Scope, and Attribution

This proposal intersects with established research in analogical reasoning, transfer learning, active learning, Bayesian experimental design, meta-learning, representation learning, information retrieval, hierarchical decision-making, causal transfer, and cognitive control. It should be read as a proposed synthesis and experimental agenda, **not** as a claim that weak-evidence search or transfer prioritization was invented here.

The terminology and architectural suggestions also connect to earlier open Structural Intelligence research proposals, especially **Beyond Matching: OTHERS and Directional Weak Evidence Intelligence (BM-ODWEI)** and its **Metric-Directional Intuition (MDI)** extension. Those connections are conceptual; they do not constitute independent experimental validation. A later scholarly version should add verified bibliographic references and direct empirical comparisons to adjacent work.

## 18. Conclusion

Directional intuition is proposed as a disciplined way to **ask where intelligence might transfer next** without demanding complete formal equivalence before exploration. Weak evidence can justify a cheap probe, but not a capability claim. Selective permeability admits candidate directions; two-phase search separates discovery from verification; counter-evidence and provenance keep the resulting relay honest. If controlled experiments show improved cost-adjusted discovery of valid transfers, this mechanism may become a useful component of capability prospecting and system-centric learning. If they do not, the hypothesis should be narrowed or rejected.

The intended contribution is a clear research question, a modest candidate architecture, and a set of tests that others can reproduce, criticize, or extend.

---

## Figure Placement

**Primary planned figure:** `figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png`, recommended after Section 8.  
**Secondary cross-reference:** `figures/Fig-004-Folding-Generalization-and-Structural-Transfer.png`, recommended after Section 4 or 5.  
**Optional cross-reference:** `figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png`, recommended after Section 15.

All figures are conceptual proposals rather than measured results. Because this file belongs in `docs/`, links to figures should use `../figures/` once the assets are available.

## Relationship to Other ISGFTR Documents

- **ISGFTR-001:** intelligence boundaries and open capability frontiers.
- **ISGFTR-002:** five properties and their conceptual distinctions.
- **ISGFTR-003:** folding–generalization duality, structural reuse, and uncertainty.
- **ISGFTR-004:** intelligence fluidity and selectively permeable boundaries.
- **ISGFTR-006:** system-centric intelligence and multi-level learning.
- **ISGFTR-007:** recursive relay and durable structural growth.
- **ISGFTR-008:** capability prospecting, ranking, and exploration value.
- **SPEC-002 / SPEC-003:** proposed evidence records and validation lifecycle.
- **CASE-003:** proposed controlled weak-evidence prospecting experiment.

**License:** See the repository's planned `LICENSE` file (Apache-2.0).  
**Citation:** See `CITATION.cff` after publication metadata is finalized.  
**DOI:** To be assigned after a versioned release and archival deposit.
