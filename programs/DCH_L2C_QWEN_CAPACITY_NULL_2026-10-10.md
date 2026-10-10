---
id: PROGRAM-CONTINUITY-DCH-L2C-005
title: DCH model capacity follow-up with Qwen2.5-1.5B and prompt-format ablations
type: empirical-development-result
status: capacity-calibration-negative-not-dch-test
updated: 2026-10-10
research_questions:
  - RQ-001
  - RQ-006
tags:
  - dyadic-continuity
  - negative-results
  - source-provenance
  - model-calibration
---

# DCH L2 follow-ups: 1.5B parser and 0.5B format failure

**Canonical upstream report:** [Attractomancy DCH L2C and 1.5B results](https://github.com/Azimn/Attractomancy/blob/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/L2C_AND_15B_RESULTS_2026-10-10.md). **Evidence:** [Qwen1.5B CI 38025720757](https://github.com/Azimn/Attractomancy/actions/runs/38025720757), [Qwen0.5B L2C CI 38025854993](https://github.com/Azimn/Attractomancy/actions/runs/38025854993). Read upstream raw json and independently stored targets for quantitative reuse.

Qwen2.5-1.5B on the originally frozen L2 battery yielded 32 generations, all invalid under the preregistered strict whole-response JSON parser. Twenty-three were truncated at the fixed output limit, but the other nine also failed strict full-message parsing. A post hoc recovery of the initial well-formed JSON object revealed 2/8 correct decisions in the full-oracle condition, and 0/8 in expert-auto, stale, and cold conditions. That is a *secondary diagnostic*, not a superseding primary endpoint.

Qwen2.5-0.5B on 48 L2C format conditions again did not condition decisions on memory. All 24 original-format responses answered SCHEDULE, and all 24 compact-format responses answered the malformed action FULFILL_. Strict JSON output validity was 100% across the 48 but action correctness was 25% for original format and 0% for compact format in each of expert-auto, stale and cold groups. Branch-minimal full provenance was 0% for all arms. The L2C study had zero actual expert-versus-human proxy matched pairs; an empty-array vacuous pass was corrected in code and cannot be reported as equivalence evidence.

**Interpretation:** both experiments display task and output-format limitations, with no meaningful performance differentiation attributable to curated memory. They cannot evaluate DCH, no human or dyad appears, and the oracle's increased memory budget precludes a parity inference. The primary null remains intact.

**Next gate:** [L3 staged competency ladder](https://github.com/Azimn/Attractomancy/blob/research/dch-d0-pilot-20261009/experiments/DCH_D0_SYNTHETIC_PILOT/L3_STAGED_CAPACITY_PROTOCOL.md), 64 real generations on Qwen2.5-1.5B if CI succeeds. It separates one-record lookup from chronology, conditional access, and four-record integration, and includes a cold abstention control in each task. Do not register a dyadic treatment unless accuracy and provenance sensitivity warrant it.
