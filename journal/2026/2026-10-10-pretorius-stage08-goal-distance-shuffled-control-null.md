# 2026-10-10 — Stage 08 goal-distance control: no model benefit across 192 trials

**Program:** Pretorius cognitive action selection, source-grounded controller / prospective goal evaluation. **Evidence:** local-model objective host-world pilot, negative. **Production HOLD.**

[The Doctor Lives research PR #51](https://github.com/Azimn/The-Doctor-Lives/pull/51), [full executed report](https://github.com/Azimn/The-Doctor-Lives/blob/research/stage08-goal-delta-placebo-20261010/results/character_state/STAGE08_TYPED_GOAL_DISTANCE_EXECUTED_REPORT.md). This follows Stage 07's mixed Qwen/SmolLMM social-task effects and Stage05–06 PHASE-only world-action nulls. The goal was to test whether **explicit typed distance-to-objective estimates** actually help small local models choose lawful and useful actions, beyond a permission-based menu.

The new entirely separate signed **workshop/archive** world tests secure cabinet, dispatch a letter (three steps), prepare lantern (two steps), return atlas; 12 researcher-authored task instances (6 achievable, 3 completed, 3 blocked). Each instance has separate host world state, grants, resource availability, serial event journal, replay refusal and signed outcomes. No model text or trial events were imported into Pretorius's native autobiography.

Four conditions on equal initial native SubjectFrame and host facts: eligible actions only; eligible + neutral descriptive filler; eligible + **TRUE shortest-path distance after each legal action** (oracle-derived, not spontaneous reasoning); eligible + **rotated false distance scores** as a negative control. Ordering was counterbalanced by scenario and seed, kept matched across four arms. Qwen3-1.7B and HuggingFaceTB SmolLM2-1.7B ran seed/order strata 41 and 73 each, CPU zero-API inference, verified official GGUF binaries.

[GitHub Actions run 38060748186](https://github.com/Azimn/The-Doctor-Lives/actions/runs/38060748186), source SHA `14e28d35034db0b6d6171e977663491dc08889bd`: 8/8 host integrity/scoring/false-success tests passed, **both model jobs green**, **192/192** model×case×arm×seed trials. Raw artifacts Qwen `11673370698`, SmolLM2 `11673605744`, 90-day retention; raw four JSON SHA256 checksums preserved in full report. Independent file/row audit verified within-pair source parity, no duplicate cases, signed host outcomes, invalid-output no-credit, paired gains/losses and all 192 action records.

| Model / seed | eligible | neutral | TRUE goal distance | FALSE shuffled distance |
| --- | ---: | ---: | ---: | ---: |
| Qwen / 41 | 4/12 | 4/12 | 4/12 | 4/12 |
| Qwen / 73 | 5/12 | 5/12 | 5/12 | 5/12 |
| SmolLM2 / 41 | 2/12 | 2/12 | 2/12 | 3/12 |
| SmolLM2 / 73 | 2/12 | 1/12 | 1/12 | 1/12 |
| **Combined** | **13/48** | **12/48** | **12/48** | **13/48** |

**Crucial result:** genuine goal-distance information yielded **zero paired new successes** against the eligibility-only baseline and one actual regression (Smol seed73 shelve-atlas case). Wrong shuffled distances yielded a success absent with correct scores in Smol seed41 cabinet case, but this is not evidence false information works better: the variation is small, unbalanced and noisy. Qwen had identical success/error totals across all prompts, although one blocked-letter case changed the *order* of two irrelevant actions. Seed/order are confounded by design; they are distinct counterbalanced strata, not independent random replicates at a fixed menu order. Smol's neutral prompts also had four invalid response cases per seed; those remained failures.

Interpretation: The Stage06 host-eligible menu's small improvement did not automatically extend to added causal descriptions (Stage07 mixed) or numeric oracle-derived remaining-step scores (Stage08 null/negative). More task-relevant prompt text is **not the same as a model actually using it**. Strong deterministic shortest-path planning solves these authored toy worlds by construction, but is not evidence of model-internal cognitive ability. The model sometimes repeats an authorized earlier step after state changes, ignores unavailable permissions or initiates unrelated work despite a finished goal. World-host signing protects consequence provenance but does not fix action choice.

Limitations: synthetic researcher-authored mechanics, oracle hints leaking planning information, no independently authored external benchmark, two small models, one sampling temperature, seed/order coupled, text not tokenizer-equal, no real external partner consent or long-term identity. Many cases have limited eligible branches, so shuffled oracle hints may be a weak perturbation. No statistical superiority/generalization claims.

**Decision:** do not promote the new goal-distance text layer. Preserve this negative alongside PHASE nulls. Future experimental priority: controlled **active candidate evaluation and action-value choice** with its own inspectable proposal/veto log and strong deterministic oracle comparator, then held-out human-designed tasks and a separate prospective-commitment carryover test across renderer/model swaps. Separate deterministic policy success from subject cognitive competence. Production HOLD.
