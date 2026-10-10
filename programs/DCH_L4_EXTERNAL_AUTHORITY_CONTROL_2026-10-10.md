---
id: PROGRAM-CONTINUITY-DCH-L4-006
title: DCH source-authority gate implementation and null separation
type: implementation-and-engineering-result
status: control-law-verified-dch-untested
updated: 2026-10-10
research_questions:
  - RQ-001
  - RQ-006
tags:
  - dyadic-continuity
  - memory-authority
  - source-provenance
  - nonclaim
---

# DCH L4: making the cognitive control law independent of the language renderer

**Canonical experimental home:** [Attractomancy L4 report](https://github.com/Azimn/Attractomancy/blob/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/L4_AUTHORITY_RESULT_2026-10-10.md). **Runnable audit:** [CI 38058117852](https://github.com/Azimn/Attractomancy/actions/runs/38058117852). **Raw evidence:** [L4 result folder](https://github.com/Azimn/Attractomancy/tree/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/results/l4-authority-38058117852). **Draft integration PR:** [Attractomancy #2](https://github.com/Azimn/Attractomancy/pull/2).

The L3 Qwen2.5-1.5B-Instruct competency ladder produced poor model-derived decisions even with archived relevant records: available S1 0/8, S2 0/8, S3 4/8, S4 0/8 strict correctness. Some failure was output formatting; others were stale-record use, conditional rule violations and unsupported decisions with no archive. The fixed four-stage task did not satisfy advancement thresholds.

L4 implements an explicit external authority gate, separating provenance checks and action preconditions from natural-language generation. It rejects duplicate identifiers, cross-subject records, conflicting equal-time updates, unauthorized evidence, bad value types and invalid time information. Its unit tests exposed an initial error in conflict detection for superseded history, which was repaired before the successful CI run.

On the pre-existing development fixture, the deterministic gate achieves 96/96 target actions and 96/96 exact source certificates, including cold controls. The result is an **engineered reference control** whose rules are programmed to match the fixture, not experimental evidence that this architecture is intrinsically more capable than a model, that a persona is persistent, or that a human dyad performs a unique causal function. A 64-item matched descriptive comparison against archived Qwen generations is preserved for auditing. Different computation and token budgets forbid a fair performance-efficiency conclusion.

**Research program implication:** Because the gate can hold source authority and policy execution fixed, subsequent DCH tests can manipulate the upstream intervention and memory-curation policy separately from the renderer. The strongest null, expert automated curation being sufficient under information and budget parity, remains central. The next eligible experiment is a precommitted curator-policy benchmark with true cross-yoked continuing and replacement partners, synthetic histories first and actual consented human partners only after reliable blinded scoring and privacy review. A toy imitation of a continuing human is sensitivity calibration, not the treatment.

This is an instrumentation pass; DCH causal hypotheses and preregistered G1–G6 remain untested/NO-GO.
