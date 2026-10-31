# ISGFTR v1.0.0 — Foundational Theory and Open Research Contracts

**Project:** Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)  
**Release:** `v1.0.0` — initial theory-first research release  
**Status:** Release notes prepared for publication; not a statement that the GitHub Release or DOI already exists  
**License:** Apache-2.0, subject to the repository's `LICENSE.txt` file

## Overview

This first release introduces **Intelligence Spillover, Generalization, Fluidity, Transfer, and Relay (ISGFTR)** as an open research program for investigating how capabilities may be discovered, adapted, transmitted, and retained beyond their initially observed tasks and system configurations.

The project studies five distinguishable but potentially interacting characteristics:

- **Spillover:** useful behavior observed outside a capability's initially specified or evaluated context.
- **Generalization:** reliable performance across relevant variations, including held-out conditions.
- **Fluidity:** adaptive movement of intelligence-bearing structures, attention, methods, or resources across contexts and boundaries.
- **Transfer:** reuse or adaptation of a source capability in a target setting, with explicit attention to residual differences and negative transfer.
- **Relay:** transmission and preservation of capabilities, evidence, questions, and structural updates across units, systems, and time.

The framework connects these ideas to **structural folding and unfolding**, **directional intuition and weak evidence**, **selective permeability**, **system-centric multi-level learning**, and **recursive structural relay**. It asks whether these mechanisms can improve the discovery and durable reuse of capabilities—and under which conditions they fail.

**Scope statement:** This is a **theory-first publication** containing conceptual analyses, proposed contracts, illustrative experimental designs, falsifiable hypotheses, and a validation roadmap. It does **not** report completed empirical validation, demonstrate a functioning AGI system, or claim that open-ended intelligence growth is inevitable.

## Research Contributions

### 1. Four capability boundaries

The research distinguishes **generative**, **observed**, **reachable**, and **evolvable** capability boundaries. These are context-dependent research descriptions, not necessarily nested geometric regions or permanent limits. A capability claim must specify its subject, task distribution, available resources, evidence, and evaluation conditions.

### 2. Folding–generalization and structural reuse

The framework explores when folding a problem into reusable structural cores can support generalization and transfer, while preserving **residual differences** and recognizing that compression can discard essential information. It also distinguishes uncertainty preserved during folding from uncertainty recovered through subsequent evidence.

### 3. Directional capability prospecting

The proposed **Capability Prospecting** process uses structural analogies, historical precedents, weak evidence, directional assessments, and unresolved residuals to identify candidate transfer opportunities. Its research loop is:

**Prospect → Probe → Validate → Relay → Learn → Prospect.**

A prospect is a question, not a demonstrated capability. An exploration-priority score must not be presented as a calibrated success probability without evidence.

### 4. Selectively permeable intelligence boundaries

The research examines how systems might learn when and how to admit new information, analogies, tools, or structures. It separates permission to **observe**, **probe**, **adopt**, and **deploy**, and distinguishes exploratory admission from validated claims and execution authority.

### 5. System-centric learning and recursive relay

ISGFTR investigates whether systems composed of **fixed or limited execution units** can acquire durable improvements through routing, memory, structure, evidence, and coordination—even without updating each unit's model weights. It distinguishes:

**Transmission ≠ Interpretation ≠ Adoption ≠ Utility ≠ Durable Growth.**

Repeated execution may produce evidence that contributes to temporal relay; repetition alone is not learning. System-level improvement is not automatically intrinsic model learning, recursive self-improvement, or AGI.

## What's Included

### Ten foundational articles — `docs/`

| Document | Focus |
|---|---|
| `ISGFTR-001` | Static intelligence boundaries and open capability frontiers |
| `ISGFTR-002` | Five characteristics of intelligence spillover and relay |
| `ISGFTR-003` | Folding–generalization duality and structural reuse |
| `ISGFTR-004` | Intelligence fluidity and permeable structural boundaries |
| `ISGFTR-005` | Directional intuition and weak-evidence transfer |
| `ISGFTR-006` | System-centric intelligence and multi-level learning |
| `ISGFTR-007` | Recursive relay and open-system intelligence growth |
| `ISGFTR-008` | Intelligence spillover and transfer prospecting |
| `ISGFTR-009` | AGI implications, limits, and counterarguments |
| `ISGFTR-010` | An open research architecture for collective learning |

### Four proposed contracts — `specs/`

- `SPEC-001-Canonical-Capability-and-Boundary-Contract.md` — scoped capability and boundary records.
- `SPEC-002-Spillover-Opportunity-and-Evidence-Contract.md` — candidate opportunities, evidence, counterevidence, and directional assessments.
- `SPEC-003-Prospecting-Probing-and-Validation-Lifecycle.md` — research states, probe protocols, and validation gates.
- `SPEC-004-Structural-Relay-and-Collective-Learning-Contract.md` — provenance-preserving structural relay and evidence reuse.

These are **proposed specifications**, not an implemented machine-validated standard.

### Three illustrative cases — `cases/`

- `CASE-001-LLM-Capability-Spillover-and-Cross-Domain-Transfer.md`
- `CASE-002-Minimal-System-Centric-Collective-Learning.md`
- `CASE-003-Weak-Evidence-Capability-Prospecting-and-Relay.md`

The cases are **research designs**, not reports of executed or successful experiments.

### Three extensions — `extensions/`

- `EXT-001-Biomimetic-Fluidity-and-Selective-Permeability.md`
- `EXT-002-Learning-the-Boundaries-of-Intelligence-Flow.md`
- `EXT-003-Evolvable-Intelligence-Potential-and-Open-Ended-AGI.md`

### Navigation, research governance, and publication metadata

The repository is organized around `README.md`, `START-HERE.md`, `CONTENTS.md`, `GLOSSARY.md`, `FIGURE-INDEX.md`, `FUTURE-DIRECTIONS.md`, `OPEN-QUESTIONS.md`, `TESTABLE-HYPOTHESES.md`, `VALIDATION-ROADMAP.md`, `CHANGELOG.md`, `CITATION.cff`, and `.zenodo.json`.

The visual sequence consists of eight figures, from `Fig-001-ISGFTR-Grand-Architecture.png` to `Fig-008-Recursive-Relay-and-Collective-Intelligence-Growth.png`. **Verify that all eight exist as separate correctly named files in `figures/` before publishing links to them.**

## How to Read This Release

- **New readers:** start with [`README.md`](../README.md) and [`START-HERE.md`](../START-HERE.md).
- **Theory and scope:** read [`ISGFTR-001`](../docs/ISGFTR-001-From-Static-Intelligence-Boundaries-to-Open-Capability-Frontiers.md), [`ISGFTR-002`](../docs/ISGFTR-002-Five-Characteristics-of-Intelligence-Spillover-and-Relay.md), and [`ISGFTR-009`](../docs/ISGFTR-009-AGI-Implications-Limits-and-Counterarguments.md).
- **Engineering and conformance:** consult the four documents in [`specs/`](../specs/) and the experimental designs in [`cases/`](../cases/).
- **Reproducibility and critique:** begin with [`TESTABLE-HYPOTHESES.md`](../TESTABLE-HYPOTHESES.md), [`OPEN-QUESTIONS.md`](../OPEN-QUESTIONS.md), and [`VALIDATION-ROADMAP.md`](../VALIDATION-ROADMAP.md).

## Scientific Boundaries and Known Limitations

1. **No AGI claim.** Neither capability spillover nor recursive relay establishes general intelligence.
2. **No experimental results asserted.** Proposed tests, example schemas, and case studies must not be interpreted as completed validations.
3. **Negative transfer is possible.** Structural similarity can be misleading; residuals, distribution shift, and counterevidence matter.
4. **System-level attribution matters.** Improved performance may result from tools, orchestration, retrieval, memory, or additional compute rather than intrinsic changes in model capabilities.
5. **Evidence must travel with claims.** Source conditions, failed attempts, uncertainty, and independent replication status should remain available through relay.
6. **Governance remains explicit.** Permission to explore is not permission to deploy; safety and authorization boundaries are not inferred from performance.

## Validation and Next Steps

The immediate research priorities are to: (i) implement minimal machine-readable schemas and conformance checks for the proposed contracts; (ii) establish leakage-resistant, budget-matched baselines; (iii) run controlled cross-domain transfer and frozen-unit structural-learning studies; (iv) compare prospecting policies against random, similarity-based, and other relevant baselines; and (v) publish negative results and independent replication reports alongside positive findings.

These activities are **future work**, not part of the validated deliverables of v1.0.0.

## Citation, License, and DOI

Please use the repository's [`CITATION.cff`](../CITATION.cff) for citation metadata and cite the **version consulted**. A version-specific DOI may be added after a successful Zenodo archive; **no DOI is claimed in these release notes**.

The intended license is **Apache License 2.0**; confirm that the repository contains the corresponding `LICENSE.txt` file before publication.

## Open Research Invitation

ISGFTR is offered as a **collective-learning-friendly** research framework. Critical comparisons with existing work, stronger baselines, failed replications, formal counterexamples, alternative formulations, and interoperable evidence records are all valuable contributions.

**Explore widely. Validate carefully. Preserve counterevidence. Relay what can be checked.**

---

### Pre-publication checklist (remove or retain as internal release guidance)

- [ ] All 20 research documents are present under the `docs/`, `specs/`, `cases/`, and `extensions/` paths.
- [ ] Root navigation files and internal links have been checked.
- [ ] All eight figures are separately exported, correctly named, and legible.
- [ ] `LICENSE.txt` contains the intended Apache-2.0 text.
- [ ] `CITATION.cff` and `.zenodo.json` agree on title, authors, license, and version.
- [ ] The Git tag and GitHub Release are both named `v1.0.0`.
- [ ] Any release date and DOI are confirmed before being stated as facts.
- [ ] No proposed experiment is described as completed.
