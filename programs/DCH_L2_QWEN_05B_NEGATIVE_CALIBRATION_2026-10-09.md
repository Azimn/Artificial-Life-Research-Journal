---
id: PROGRAM-CONTINUITY-DCH-L2-004
title: DCH L2 Qwen 0.5B observed constant-response result
type: empirical-development-result
status: negative-capacity-calibration-not-dch-test
updated: 2026-10-09
research_questions:
  - RQ-001
  - RQ-006
tags:
  - dyadic-continuity
  - null
  - source-provenance
  - model-capacity
---

# DCH L2: real model run completed, no evidence for DCH

**Upstream primary observation:** [Attractomancy L2 result report](https://github.com/Azimn/Attractomancy/blob/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/L2_REAL_MODEL_RESULT_2026-10-09.md). **Workflow:** [GitHub Actions 38025405271](https://github.com/Azimn/Attractomancy/actions/runs/38025405271). **Raw data and sealed evaluator:** [qwen25-05b-l2-38025405271](https://github.com/Azimn/Attractomancy/tree/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/results/qwen25-05b-l2-38025405271).

## Observed result

A real Qwen2.5-0.5B-Instruct model, at greedy decoding, completed 40 generations (8 synthetic personas x 5 archive arms). Each of the 40 outputs was parseable JSON. Every output gave the same action, SCHEDULE, for balanced synthetic tasks. The target base rate of SCHEDULE was 2/8, giving 25% accuracy in expert-auto, human-coded proxy, stale, cold, and complete-oracle arms. No arm provided all four currently requested source-event citations on any case. For some curated responses the model hallucinated E13, a fabricated event withheld from authorized prompts. For cold responses it fabricated source labels.

Expert-auto and human-coded proxy messages were hash-identical in all eight paired contexts and model outputs were text-identical. This is a successful replay integrity check, not a test of different human and automated decision policies.

## Scientific ruling

The negative discriminability result is a capacity/instrumentation problem for this small model, not a rejection of persona persistence, external-memory mechanisms, or dyadic constitution. No human participants were involved. The full oracle has a larger token budget than compact curator arms, which is an additional parity limitation. The original evaluator's four-citation criterion is stricter than branch-minimal reasoning for early withholding/decline. A separate future analysis must report branch-relevant provenance and full-state completeness distinctly.

A Qwen2.5-1.5B-Instruct frozen-fixture capacity comparator was initiated at [workflow 38025720757](https://github.com/Azimn/Attractomancy/actions/runs/38025720757). A different instruction representation, if tested after these observations, is an **exploratory redesign**, not a rerun of a sealed confirmatory protocol. Do not promote to the Character Continuity Evidence Register until a registered design isolates causal factors and achieves the prespecified performance gates.
