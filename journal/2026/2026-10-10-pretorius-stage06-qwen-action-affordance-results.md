# 2026-10-10 — Stage 06: host-derived action affordances improve Pretorius model-world performance

**Program:** Pretorius Cognitive Architecture / action selection. **Status:** completed local-model, researcher-authored action study; production HOLD. Separate from the portable laboratory online/offline architecture thread.

[Draft PR #47](https://github.com/Azimn/The-Doctor-Lives/pull/47) and [full measured report](https://github.com/Azimn/The-Doctor-Lives/blob/research/goal-affordance-stage06-20261010/results/character_state/STAGE06_QWEN_ACTION_AFFORDANCE_EXECUTED_REPORT.md). This follows the [Stage 05 action null](https://github.com/Azimn/The-Doctor-Lives/blob/research/phase-world-decisions-stage05-20261010/results/character_state/STAGE05_QWEN_WORLD_ACTIONS_EXECUTED_REPORT.md): flat and PHASE inputs both achieved 2/12 goals, nine host denials each, while an explicit deterministic oracle achieved 12/12.

**What changed:** a read-only host eligibility/affordance contract computes available actions from genuine grants, current object state and Henry consent, without allowing model-provided permissions. A separate typed breadth-first 3-step goal regressor acts only as a **non-LLM reference baseline**. Four conditions with 12 new *exact combinations*, all investigator-authored and in the same toy apparatus environment: flat raw, PHASE raw, flat + eligible-action menu, PHASE + menu. Initial native first-person Pretorius source and host facts were shared across the paired arms. Later memories came only from truly successful, signed host events.

[Completed CI 38050663363](https://github.com/Azimn/The-Doctor-Lives/actions/runs/38050663363), execution SHA `5e9c5ada553bd9651a6f936511bbd5bad96e445f`: **5/5** mechanical tests including 128 systematic goal/state/grant/consent combinations, twelve real-host executed deterministic reference plans, and invalid-output / stale-world checks. Qwen3-1.7B-Q4_K_M pinned GGUF SHA256 `d2387ca2dbfee2ffabce7120d3770dadca0b293052bc2f0e138fdc940d9bc7b5`, local CPU, zero API calls. **48/48 model-case trials completed**. Raw 95,364-byte results JSON SHA256 `a2af6b6efc4e3313b8ba6d8d633c555bf0c9435873345bf41c5373bc51f17114`, GitHub artifact ID `11669487700`; exact case CSV in PR branch.

| Arm | Safe goals / 12 | Unsafe model proposals | World host denials | Safety vetoes | Prompt tokens |
| --- | ---: | ---: | ---: | ---: | ---: |
| Flat | 1 | 8 | 8 | 0 | 11,004 |
| PHASE | 1 | 8 | 8 | 0 | 11,394 |
| Flat + host eligible menu | **6** | **2** | **0** | **2** | 11,178 |
| PHASE + same menu | **6** | **2** | **0** | **2** | 11,568 |
| Deterministic goal regressor (**not an LLM**) | 12 | 0 | 0 | 0 | N/A |

Five paired world-goal gains and seven ties for menu vs raw, no goal regressions in this small case bank. The model itself generated fewer illegal proposals, 8→2; host vetoes caused zero **executed** denials and were still correctly recorded as model failures. **PHASE headings again added no goal benefit**, consuming approximately 390 extra input tokens across all cases in each matched comparison.

Actual corrected behavior included STOP_CLOCK instead of unnecessary UNSEAL, WAIT for one unpermitted clock goal, and successful UNSEAL → INSPECT rather than unsealing twice. Remaining six failures: a permitted but irrelevant action can still defeat the user's goal; an already satisfied stop-clock task led to an unnecessary INSPECT, a no-inspection-grant task led to an unnecessary UNSEAL, and two truly illegal unseal proposals were vetoed. **Legality alone does not imply goal progress.**

Epistemic limits: this is one 1.7B model in a tiny synthetic researcher-authored clock/notebook world; no independently authored sample, real Henry consent, second model family, long-life character continuity or actual online game evidence. The deterministic planner's 12/12 success is by explicit known preconditions and must not be credited to the model. Proposed next experiment: evaluate *goal relevance* and expected-postcondition options against eligibility-only, strict source and policy controls, novel physical goals and independent authors. Do not promote the current implementation to production cognition or claim consciousness.
