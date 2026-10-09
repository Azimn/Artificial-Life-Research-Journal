---
id: PROGRAM-CONTINUITY-COMPARE-001
title: Character Continuity Comparison Protocol v1
type: protocol
status: preregistration-draft
updated: 2026-10-08
---

# Character Continuity Comparison Protocol v1

**Status:** registered experimental design proposal, NOT a frozen confirmatory preregistration and NOT experimental data. No run, green CI, participant blinding, or approved reviewer labels is claimed. Exact source splits and metric thresholds must be sealed before confirmatory execution.

## Hypothesis test

Does external persistent history, recurrent adaptation, or their interaction cause improved recall and history-sensitive action while retaining reliable refutation and abstention?

### Conditions

| Arm | Recurrent weights after initial checkpoint | Durable autobiography available during recall/action | Scientific function |
| --- | --- | --- | --- |
| A, frozen control | Frozen | No growing autobiographical record, only matched initial character specification | Lower-bound default and shortcut detector |
| B, external loop | Frozen | Yes, source-linked growing record, retrieval and persistence | Test external record contribution |
| C, recurrent only | May learn | No growing readable record, only same precommitted initial state and training experiences | Test causal learned-substrate contribution |
| D, hybrid | May learn | Same record and retrieval as B | Test added value and interaction |

A is not a capacity-matched substitute for B, C or D. B and D must match access to sources and retrieval; A and C lack that store by design. Report compute, memory bytes, parameter count, retrieval access, number of training neural updates, test-time context tokens, model calls, index size, and other side information per arm. Include a strong independent full-text lexical or BM25 retrieval reference for retrieval subtests, not as a fifth persona architecture.

## Fixed inputs, inference boundaries, and replay

Use an immutable versioned Pretorius archive with original memory IDs, provenance, narrative content and episode boundaries. For studies requiring 450 source events, pin v12 source and the deterministic shared L2 v2 feature encoder manifest. Architecture-specific adapters remain separate and versioned. No event's source identity, answer, action label, or hidden evaluation category may leak through test prompts, feature fitting, teacher channels or renderer metadata.

Create distinct evaluation axes:

**Stored-event recall:** model experiences a source event during the common development history, then answers a new independently written paraphrase about it. Measure target-event candidate recall at K, correct-and-accepted grounded claims, contradiction false confirmations, episode confusion, and coverage.

**Generalization to untrained source events:** exclude target source episodes from learning, background curriculum and feature fitting, then test an explicitly registered ability such as evidence recognition when those unseen episodes are presented as new input. Do not pretend a subject should remember an event it has never encountered.

**Longitudinal continuity:** across controlled history sequences, ask new decision scenarios about carried commitments, relationships, revisions of belief, and prospective tasks. Pre-author independent expected evidence and scoring rules. Compare identical-history repeats and counterfactual histories.

**Perturbation:** restart the process with identical persisted arm-appropriate state, replace only the language renderer when technically supported, scramble surface wording, and interrupt context. Do not reset stored history in B/D without marking the intervention.

**Causal localization:** on matched checkpoints lesion the learned recurrent delta while retaining all other state; remove or swap the external record while retaining weights; test policy readout transplantation and fixed-decoder control. For D use a 2 x 2 factorial interpretation, holding history and recurrent treatment consistent.

## Outcome metrics

Primary endpoint 1: correctly sourced AND accepted true claims divided by all adjudicated answerable true prompts, with numerator and denominator. Report retrieval candidate recall separately from evidence verification.

Primary endpoint 2: contradictions incorrectly confirmed divided by adjudicated contradictions; absent-event false acceptance; answer coverage and risk-versus-coverage curves. Reject-all achieves perfect rejection but zero useful recall and cannot be declared successful.

Primary endpoint 3: correct history-conditioned choices on sealed, independently reviewed situations with paired counterfactual histories. Measure whether lesioning learned weights or replacing the record changes the predicted action in the expected direction; raw policy variance alone does not prove correct causal learning.

Secondary metrics: event-ID accuracy at K, source citation correctness, temporal order, relationship continuity, commitment retention, calibration, renderer-swap degradation, persistence after restart, runtime, memory/storage and inference cost. Never combine unlike outcome metrics into a single "identity" score without a frozen weighting rule.

## Dataset separation and independent review gate

Development cases may use the existing 450 reconstructed events and published Pilot 04 or D6A items, but those published test prompts MUST NOT serve as final independent evidence. The confirmatory set needs new authoring by someone not adjusting the candidate, independent factual reviews of the fictional source by at least two reviewers, resolution of disagreement, paraphrase-equivalence checks and contradiction verification. Freeze hashes, seed splits, source episodes, model checkpoints, budget rules, thresholds and evaluation script before testing. Annotate ambiguous prompts and exclude or pre-specify handling before unblinding. If that review is unavailable, run only a clearly labeled exploratory pilot.

Use independent narrative-cluster splits where necessary because episode separation alone may not remove related paraphrases. Freeze a negative family that includes unseen episodes, nearby but unsupported incidents, genuinely contradictory variants, and insufficient-evidence questions. Keep positive and negative families balanced or report class-specific denominators and use prevalence-aware scoring.

## Stopping and admission gates

The first stage stops after registered arms, seeds, and challenge partitions are evaluated without adaptive retuning on the frozen set. A positive recurrence claim needs consistent correctly grounded task improvement over its matched W-lesion and wrong-label controls; a positive topology claim requires improvement over a topology-rewired control that matches relevant graph statistics. A positive external-loop claim needs useful supported recall and transfer, not retrieval on identical surface cues alone. A hybrid claim needs measured incremental benefit beyond B and C, with ablations demonstrating each contribution; a genuine interaction claim requires an explicit factorial interaction test.

Statistical inference, minimum effect size and replication counts must be fixed after independent dataset sizing, before scores are observed. Until then all v1 results are exploratory. Negative or inconclusive outcomes must be recorded unchanged.

## Ownership and implementation

Shared benchmark definitions, blinded-review manifests, frozen protocol, comparison summary, and independent findings belong in this journal with version-pinned references. Original event source and L2 encoder stay in Pretorius Connectome. BioCircuit and FlyWire keep their own neural runners. The Doctor Lives is the target for optional production evaluation, not an automatic test winner and not a replacement for independent control code.

First engineering deliverable: a deterministic, source-ID-driven evaluation contract with adapters for a record-only baseline, a frozen recurrent baseline, learned recurrence and a hybrid. The contract must be able to replay paired histories without requiring an API subscription.

## Tracked implementation gates

Independent benchmark and review: [Gate A](https://github.com/Azimn/Artificial-Life-Research-Journal/issues/1). Deterministic four-arm evaluator with contamination and lesion checks: [Gate B](https://github.com/Azimn/Artificial-Life-Research-Journal/issues/2). Registered experiment and architectural decision after both gates: [Gate C](https://github.com/Azimn/Artificial-Life-Research-Journal/issues/3).

## Required report structure

Every executed report states the question, frozen environment, source/git hashes, actual train/inference budgets, reviewer status, train-test leakage audit, condition and seed denominators, raw per-case outputs, paired ablations, failures, uncertainty, interpretation and next architectural decision.
