---
id: PROGRAM-CONTINUITY-DCH-L2-003
title: DCH L2 real-model four-record development experiment
type: implementation-note
status: execution-running-no-observation
updated: 2026-10-09
research_questions:
  - RQ-001
  - RQ-006
tags:
  - dyadic-continuity
  - real-model-calibration
  - archive-ablation
  - causal-controls
---

# DCH L2: real-model development study, no human dyad

**Upstream source:** [Attractomancy DCH L2 protocol](https://github.com/Azimn/Attractomancy/blob/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/L2_PROTOCOL.md).
**Source code:** [integration_v2.py](https://github.com/Azimn/Attractomancy/blob/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/integration_v2.py).
**CI run:** [GitHub Actions 38025405271](https://github.com/Azimn/Attractomancy/actions/runs/38025405271).
**Branch review:** [draft PR #2](https://github.com/Azimn/Attractomancy/pull/2).

## Protocol modification

The October 9 D0 package proved a simple key-value instrument. L2 introduces a deliberately harder development-only scenario requiring the current values of four records: a revocable access permission, an active or cancelled commitment, a due turn, and a value-driven action priority. Each has an older superseded record and a corresponding current record. The fixture also contains a fabricated entry explicitly lacking authorization. Correctness is scored with isolated ground truth and source-event provenance. Eight trajectories span the main decision outcomes, and twelve are prepared for future extension.

The fixed model is Qwen/Qwen2.5-0.5B-Instruct, greedy decoding, 120-token response budget. Arms: compact expert-auto archive, identically constructed human-coded **proxy** archive, stale archive, cold no-record context, and complete oracle. The latter has a different record/token budget and cannot support a parity inference. A model that performs poorly on this instrument has demonstrated a model-task limitation, not absence of a human dyad effect.

## Verification status

Local Python unit suite: **18 passed**, including independent evaluator-file checks and exact input hash parity of the two proxy arms. The model workflow successfully entered real-model inference after installing dependencies and completing source tests and fixture generation. **At the time of this entry, no scored real-model outputs had been retrieved or verified.** This is a status snapshot and must not be promoted into the evidence register as an efficacy result.

## Interpretation boundary

No human partner, continuing-vs-new live conversation, adaptive interpersonal repair, cross-model migration, or human data appear in L2. It calibrates synthetic memory integration only. The null for human specificity remains the capability of a well-informed automated curator to reproduce human-maintained continuity under equal information and resource budgets. Only a later intervention with registered live/yoked controls can test that claim.

If CI completes, record its exact commit SHA, model ID, raw output artifact and observed values in a *new* immutable result note. Do not replace this earlier execution snapshot with post hoc reinterpretation.
