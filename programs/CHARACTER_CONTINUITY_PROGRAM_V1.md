---
id: PROGRAM-CONTINUITY-001
title: Character Continuity Research Program v1
type: research-program
status: active
updated: 2026-10-08
research_questions:
  - RQ-001
  - RQ-002
  - RQ-003
  - RQ-004
  - RQ-006
---

# Character Continuity Research Program v1

## Purpose and governing question

This document formalizes the existing portfolio as a cumulative investigation, not a collection of competing Pretorius implementations.

**Governing question:** Which persistent causal mechanisms allow a character to acquire experiences, be changed by those experiences, and remain behaviorally and autobiographically recognizable across interruptions, changed contexts, and model/renderer substitutions?

Character continuity is operational: source-grounded recollection, history-sensitive action, relationship and commitment carryover, coherent updating, and resistance to confabulation. Neither smooth dialogue nor vivid first-person reports are sufficient evidence. The program does not infer consciousness, sentience, or human biological equivalence.

The [Artificial Life Research Journal](../README.md) is the canonical scholarly program record. Each implementation repository remains authoritative for source code, immutable datasets, exact run outputs, hashes, CI, and reports. This program does not copy experimental weights or redefine experimental success.

## Competing hypotheses

**H-EXT, external-loop sufficiency.** A frozen decision substrate plus a persistent, provenance-aware external history and retrieval/update loop can meet specified continuity criteria without learned recurrent-weight changes. Failure on controlled held-out continuity tasks falsifies sufficiency at the tested implementation and budget.

**H-REC, learned-substrate contribution.** Recurrent plasticity yields measurable held-out, lesion-sensitive continuity benefit beyond fixed readout and matched nonlearning controls. A benefit that disappears when the decoder is swapped, or survives exact removal of recurrent learning unchanged, does not support this hypothesis.

**H-HYB, interaction advantage.** Joint external history and recurrent adaptation provide a reproducible benefit beyond either component alone under identical source evidence and realistic resource accounting. Superadditive synergy is a separate, stricter claim requiring an interaction estimate, not merely a highest total score.

**H-CUE, representation bottleneck.** Cue-to-evidence representation and evidence verification dominate performance on the currently studied autobiography tasks. Stronger lexical perturbation performance alone is insufficient; independent semantic queries, contradiction checks, and absent-memory rejection must all be measured.

These hypotheses are not metaphysical alternatives and need not be mutually exclusive. Report task- and budget-specific results; do not assert that weights or external memory are the exclusive locus of identity.

## Repository responsibilities and continuation decisions

| Line | Experimental role | Continue under this gate | Must not be treated as |
| --- | --- | --- | --- |
| [Pretorius Neural Network](https://github.com/Azimn/Pretorius-Neural-Network) | Substrate phenotype localization and BioCircuit source-conditioned decisions | Finish independent episode/source-disjoint D6 evaluation and causal decoder/recurrent lesions; preserve the previously measured bounded recurrent-only signal | A demonstrated generalizing neural autobiography |
| [Pretorius Connectome](https://github.com/Azimn/Pretorius-Connectome) | FlyWire topology, associative memory, vector retrieval, cue and entailment experiments | Freeze previously examined challenges, build independently reviewed semantic cue/evidence benchmark, test matched learned vs frozen and rewired topologies | A biologically imprinted identity or verified recollection |
| [Attractomancy](https://github.com/Azimn/Attractomancy) | Prompt conditioning, symbolic structure, ritual sequencing, persona reconstruction | Preserve original artifacts and run a registered information-matched intervention and ablation study | Evidence that symbolic practices work before actual comparative trials |
| [Attractomancy Loop](https://github.com/Azimn/Attractomancy-Loop-there-it-is) | Execution home for registered information-matched Le Refuge experiment | Complete source persona audit, frozen matched B/C/D controls, independent runs and blinded scoring | Empirical persona conditioning success before source and model runs |
| [Persona Continuity Engine](https://github.com/Azimn/Persona-Continuity-Engine) | Separate model-independent, read-only persona conditioning compiler and prospective engineering evaluator | Preserve upstream character authority, add opt-in model adapters, then benchmark with synthetic personas and equal budgets | A new canonical brain, a memory database, a validated conditioning superiority claim or evidence of machine personhood |
| [The Doctor Lives](https://github.com/Azimn/The-Doctor-Lives) | Definitive character implementation, production integration and longitudinal audit | Continue release validation and opt-in tests; promote donor mechanisms only after explicit acceptance gates | A competing laboratory prototype or a blind scientific benchmark |
| [Artificial Life Research Journal](https://github.com/Azimn/Artificial-Life-Research-Journal) | Cross-project evidence synthesis, hypotheses, shared definitions, comparative protocol and decisions | Maintain this charter, [evidence register](CHARACTER_CONTINUITY_EVIDENCE_REGISTER_V1.md), [shared protocol](CHARACTER_CONTINUITY_COMPARISON_PROTOCOL_V1.md), and date-stamped journal notes | The owner of code or raw results from sibling repositories |

Preserve each project's distinctive question. Shared source artifacts and evaluators are allowed with pinned version/adapter metadata, but architectures must not be forced to adopt identical internal neural encodings. The 450 reconstructed memories are a source corpus, not observations that a fictional individual actually lived.

## Single program, distinct lanes

The scientific lane evaluates mechanisms under frozen, independent protocols. The engineering lane develops reliable source-grounded retrieval and long-term character functionality. The production lane ships The Doctor Lives with its own regression and migration gates. Engineering success must not silently become scientific success; a negative scientific result does not forbid an explicitly nonvalidated production feature.

Continue the current neural and FlyWire experiments where they have a discriminating next test. Stop repeating uninformative gain, width, memory-count, or threshold sweeps on inspected challenges. Do not resume a retired line until its proposed intervention names a failure mode, predicts a different outcome than controls, and identifies an independent evaluation.

## Decision process

Every new candidate must identify a unique mechanism and an experiment that might disprove it. First register the hypothesis, source dependencies, controls, splitting boundary, per-condition resource budgets, primary metrics, and stopping rule. Then freeze the challenger and evaluator. Run matched controls and negative controls, record even null outcomes, and perform source/lesion or state-transfer tests. Only after a replicated, held-out benefit may a donor be proposed for opt-in production evaluation.

A decision is **continue** when a specific next test can discriminate competing explanations; **hold** when labels, fair baselines, or reproducibility are missing; **archive** when a line has no remaining discriminating test at reasonable cost; **promote** only when the mechanism clears its registered scientific and production safety gates. Hold and archive preserve all original negative results.

## Immediate common milestone

Run [Continuity Comparison Protocol v1](CHARACTER_CONTINUITY_COMPARISON_PROTOCOL_V1.md) using a frozen baseline, frozen weights plus external history, recurrent adaptation without external history, and hybrid adaptation plus history. The new independent annotation set and source-disjoint feature fitting are prerequisites for confirmatory claims. Cross-renderer and interrupted-session trials are a second stage, not a substitute for first-stage source truth and causal tests.

Use the [evidence register](CHARACTER_CONTINUITY_EVIDENCE_REGISTER_V1.md) to choose the next intervention and to prevent repeating already falsified explanations. The [2026-10-08 synthesis](../journal/2026/2026-10-08-character-continuity-convergence.md) documents why this program was assembled.

## Tracked work

[Gate A: independent benchmark](https://github.com/Azimn/Artificial-Life-Research-Journal/issues/1) and [Gate B: deterministic harness](https://github.com/Azimn/Artificial-Life-Research-Journal/issues/2) may proceed in parallel. [Gate C: registered causal comparison](https://github.com/Azimn/Artificial-Life-Research-Journal/issues/3) must wait for accepted benchmark review and executable leakage-controlled adapters. This dependency is explicit to prevent exploratory data from being mislabeled confirmatory.

## Success definition

A successful research milestone is an interpretable result that changes an architectural decision, including a null result. A successful production milestone is a working, recoverable, source-grounded Pretorius whose history changes future behavior and whose causal contribution can be inspected. These milestones are related, but not identical.
