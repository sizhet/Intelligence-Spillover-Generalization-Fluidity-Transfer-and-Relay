# START HERE — Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)

**A practical reading and research entry point**  
**Version:** v1.0.0 · **Date:** 2026-10-30  
**Status:** Theory-first, open hypotheses and proposed validation contracts; not a demonstrated AGI architecture.

Welcome. ISGFTR studies a question that is easy to ask but difficult to answer rigorously:

> When useful capabilities appear outside the contexts in which they were first observed, how can we discover, explain, test, transfer, and preserve them without overstating what has been demonstrated?

This guide helps readers navigate the repository without needing to read every document in sequence. The project welcomes independent replication, counterexamples, improved measurement, and alternative explanations.

## 1. The 90-second overview

ISGFTR uses five related lenses:

1. **Spillover:** capability is observed in a task or context beyond its initially recognized scope.
2. **Generalization:** reusable knowledge or structure continues to work across relevant variation.
3. **Fluidity:** a system adaptively redirects information, strategies, and capabilities across boundaries.
4. **Transfer:** structure or evidence from one setting helps in another, subject to target-specific constraints.
5. **Relay:** knowledge, experiments, failures, and structural units are passed across actors, systems, or time.

These terms are not claimed to be new scientific laws. They organize testable questions about *when* a capability crosses a boundary, *why* it helps, and *whether* a benefit persists.

The proposed research loop is:

**Characterize → Prospect → Probe → Validate → Relay → Learn → Reassess.**

The loop can fail at any stage. Discovery is not validation; transmission is not adoption; one-time improvement is not durable growth.

## 2. Three essential distinctions

### A. Four capability boundaries answer different questions

| Boundary | Guiding question | Caution |
| --- | --- | --- |
| **Generative** | What could the model or unit produce under specified conditions? | Not necessarily observed or useful. |
| **Observed** | What has been demonstrated by evidence? | Depends on the evaluation scope and quality. |
| **Reachable** | What can the currently configured system achieve using available components and resources? | System performance is not automatically intrinsic model capability. |
| **Evolvable** | What might become reachable through subsequent learning, reorganization, or discovery? | A hypothesis about future potential, not a measured outer limit. |

These boundaries should not be assumed to be perfectly nested circles or to admit a single universal numerical measure. See [ISGFTR-001](docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md) and [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md).

### B. Mobility is not utility, and utility is not growth

A strategy may cross domains without helping. It may help once without surviving a change of conditions. To claim **durable system-level learning**, specify the unit of analysis, baseline, evaluation distribution, persistent change, and independent evidence. See [ISGFTR-007](docs/ISGFTR-007-Recursive-Relay-and-Open-System-Intelligence-Growth.md).

### C. Exploration permission is not deployment permission

Weak evidence can justify a small, bounded probe. It does not justify a strong capability claim or unrestricted action. The project distinguishes opportunity screening, evidence adjudication, and downstream integration or deployment authorization. See [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md) and [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md).

## 3. Choose your reading path

**If you have 10–15 minutes:** Read [README](README.md), then [ISGFTR-001 — Capability Frontiers](docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md) and [ISGFTR-002 — Five Characteristics](docs/ISGFTR-002-Five-Characteristics-of-Intelligence-Spillover-and-Relay.md).

**If you study representation and generalization:** Read [ISGFTR-003 — Folding–Generalization Duality](docs/ISGFTR-003-Folding-Generalization-Duality-and-Structural-Reuse.md), [ISGFTR-004 — Intelligence Fluidity](docs/ISGFTR-004-Intelligence-Fluidity-and-Permeable-Structural-Boundaries.md), and [CASE-001 — LLM Cross-Domain Transfer](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md).

**If you study exploration and weak evidence:** Read [ISGFTR-005 — Directional Intuition](docs/ISGFTR-005-Directional-Intuition-and-Weak-Evidence-Transfer.md), [ISGFTR-008 — Capability Prospecting](docs/ISGFTR-008-Intelligence-Spillover-and-Transfer-Prospecting.md), [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md), and [CASE-003](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md).

**If you study multi-agent or system-centric learning:** Read [ISGFTR-006 — Multi-Level Learning](docs/ISGFTR-006-System-Centric-Intelligence-and-Multi-Level-Learning.md), [ISGFTR-007 — Recursive Relay](docs/ISGFTR-007-Recursive-Relay-and-Open-System-Intelligence-Growth.md), [CASE-002 — Minimal Collective Learning](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md), and [SPEC-004 — Relay Contract](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md).

**If you assess AGI claims or governance:** Start with [ISGFTR-009 — AGI Implications, Limits, and Counterarguments](docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md), then [EXT-003 — Evolvable Intelligence Potential](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md).

**If you want an integration architecture:** Read [ISGFTR-010 — Open Research Architecture](docs/ISGFTR-010-An-Open-Research-Architecture-for-Collective-Learning.md), then the four [SPEC contracts](CONTENTS.md).

For a full file-by-file map, use [CONTENTS.md](CONTENTS.md); for terminology, use [GLOSSARY.md](GLOSSARY.md).

## 4. Repository map

```text
Intelligence-Spillover-Generalization-Fluidity-Transfer-and-Relay/
├── README.md                 # Project overview
├── START-HERE.md             # This reading guide
├── CONTENTS.md               # Full navigation
├── GLOSSARY.md               # Definitions and distinctions
├── FIGURE-INDEX.md           # Eight planned research figures
├── FUTURE-DIRECTIONS.md      # Next research directions
├── OPEN-QUESTIONS.md         # Unresolved questions
├── TESTABLE-HYPOTHESES.md    # Falsifiable propositions
├── VALIDATION-ROADMAP.md     # Empirical research plan
├── CHANGELOG.md
├── CITATION.cff
├── .zenodo.json
├── LICENSE
├── docs/                     # ISGFTR-001 through ISGFTR-010
├── specs/                    # SPEC-001 through SPEC-004
├── cases/                    # CASE-001 through CASE-003
├── extensions/               # EXT-001 through EXT-003
├── figures/                  # Fig-001 through Fig-008
└── release/                  # Release notes and ResearchGate assets
```

This is the **intended repository layout**; check the repository for which assets have actually been committed. The documents are proposed research artifacts, not reports of completed experiments.

## 5. Eight visual entry points

When the images are available under `figures/`, the figures provide a quick conceptual tour:

| Figure | Theme |
| --- | --- |
| [Fig-001](figures/Fig-001-ISGFTR-Grand-Architecture.png) | Overall research architecture |
| [Fig-002](figures/Fig-002-Four-Intelligence-Boundaries.png) | Four distinct boundary questions |
| [Fig-003](figures/Fig-003-Five-Characteristics-of-Intelligence-Flow.png) | Five intelligence-flow characteristics |
| [Fig-004](figures/Fig-004-Folding-Generalization-and-Structural-Transfer.png) | Shared structural cores and residuals |
| [Fig-005](figures/Fig-005-Directional-Intuition-and-Selective-Permeability.png) | Weak-evidence guidance and gated exploration |
| [Fig-006](figures/Fig-006-System-Centric-Multi-Level-Learning.png) | Multi-level learning with fixed units |
| [Fig-007](figures/Fig-007-Spillover-Prospecting-and-Capability-Frontiers.png) | Capability discovery and probing |
| [Fig-008](figures/Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png) | Evidence-bearing recursive relay |

**Diagram caveat:** figures are explanatory schematics, not empirical results; any depicted boundary geometry or progression should be read conceptually.

## 6. How to evaluate the claims

For each proposed mechanism, ask:

- **Scope:** What system, task distribution, resources, and evaluation conditions are specified?
- **Baseline:** What would a simpler explanation or nonadaptive control achieve?
- **Attribution:** Did the model change, did the system configuration change, or did only the prompt or task selection change?
- **Evidence:** Are observations reproducible, independently checked, and accompanied by uncertainty estimates?
- **Counterevidence:** Which failures, negative transfers, and confounders have been preserved?
- **Durability:** Does the benefit persist on held-out tasks and after the immediate episode?
- **Cost and risk:** Does improvement remain after accounting for tokens, tools, compute, coordination, and failure costs?

Consult [TESTABLE-HYPOTHESES.md](TESTABLE-HYPOTHESES.md) and [VALIDATION-ROADMAP.md](VALIDATION-ROADMAP.md) as the research program develops.

## 7. A minimal reproducible study

A small study can test whether structural evidence relay improves transfer selection **without updating execution-model weights**:

1. Select two related but meaningfully different task families; document overlap and domain-specific residuals.
2. Freeze the execution model(s), prompts where applicable, and tool permissions for each comparison condition.
3. Register evaluation criteria, budgets, stopping rules, and held-out tasks before probing.
4. Compare random candidate selection, similarity-based selection, and a weak-evidence prospecting method.
5. Log each proposed transfer, source evidence, uncertainty, experiment, failure, and outcome.
6. Repeat on new tasks with and without access to the accumulated evidence registry.
7. Evaluate not just task success, but discovery cost, false positives, negative transfer, calibration, and persistence.
8. Report alternative explanations and share unsuccessful probes, not only successful examples.

**What would count as evidence?** A controlled, reproducible advantage on pre-specified measures under comparable budgets. **What would not?** A persuasive anecdote, a cherry-picked demonstration, or a score improvement that disappears under proper controls.

Relevant concrete designs: [CASE-001](cases/CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md), [CASE-002](cases/CASE-002-Minimal-System-Centric-Collective-Learning.md), and [CASE-003](cases/CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md).

## 8. The contract-first route

The four proposed specifications form a sequence:

| Contract | Purpose |
| --- | --- |
| [SPEC-001](specs/SPEC-001-Canonical-Capability-and-Boundary-Contract.md) | Identify scoped capability claims and boundary types. |
| [SPEC-002](specs/SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md) | Record opportunities, weak evidence, provenance, residuals, and counterevidence. |
| [SPEC-003](specs/SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md) | Govern probe registration, lifecycle states, evaluation, and claim decisions. |
| [SPEC-004](specs/SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md) | Package, transfer, independently assess, and reuse evidence-bearing structural units. |

These are **proposed contracts**. A YAML illustration is not, by itself, an implemented validator or a formally verified schema. The intended engineering direction is **specification → conformance tests → experimental runtime**, not the reverse.

## 9. Where to extend or challenge the project

The three exploratory extensions ask progressively harder questions:

- [EXT-001 — Biomimetic Fluidity and Selective Permeability](extensions/EXT-001-Biomimetic-Fluidity-and-Selective-Permeability.md): Can biological analogies suggest better gated transfer mechanisms, and where do the analogies break?
- [EXT-002 — Learning the Boundaries of Intelligence Flow](extensions/EXT-002-Learning-the-Boundaries-of-Intelligence-Flow.md): Can evidence improve a boundary policy without weakening governance?
- [EXT-003 — Evolvable Intelligence Potential and Open-Ended AGI](extensions/EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md): What would constitute evidence of expanding future capability rather than repeated recombination or benchmark exploitation?

Valuable contributions include independent baselines, carefully scoped counterexamples, better measurement, failure taxonomies, alternative mathematical models, schema proposals, and reproducible negative results.

## 10. Research boundaries and responsible interpretation

ISGFTR **does not claim** that spillover proves general intelligence, that all useful knowledge can be folded into a common core, that weak evidence is sufficient for deployment, that recursive relay guarantees self-improvement, or that AGI necessarily follows from system-level learning.

The research is open-ended in *questions*, not unlimited in its evidentiary claims. Its most important discipline is to separate:

**Hypothesis → Probe → Observation → Replication → Scoped Claim → Relay.**

Claims should remain revisable as new evidence and counterevidence arrive.

## 11. Continue from here

- **Big picture:** [README.md](README.md)
- **Full reading index:** [CONTENTS.md](CONTENTS.md)
- **Concepts:** [GLOSSARY.md](GLOSSARY.md)
- **Open challenges:** [OPEN-QUESTIONS.md](OPEN-QUESTIONS.md)
- **Research tests:** [TESTABLE-HYPOTHESES.md](TESTABLE-HYPOTHESES.md)
- **Experimental roadmap:** [VALIDATION-ROADMAP.md](VALIDATION-ROADMAP.md)

**Invitation:** Explore broadly, test carefully, preserve uncertainty and counterevidence, and make useful research structure easier for others to reproduce, challenge, and relay.

---

*ISGFTR v1.0.0 · Theory-first open research guide · Apache-2.0 where applicable under the repository license.*
