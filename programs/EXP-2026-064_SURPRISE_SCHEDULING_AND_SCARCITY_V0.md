---
id: EXP-2026-064
title: Surprise Scheduling and Scarcity Allocation, preregistration candidate v0
type: experimental-protocol
status: proposed-not-run
updated: 2026-10-08
program: PROGRAM-CONTINUITY-001
---

# EXP-2026-064: Is prediction-error scheduling causally useful?

**Status: proposed, not executed, not independently reviewed.** This protocol records a candidate comparison inspired by [SoulScript prior art](../literature/2026-10-08-orionforge-soulscript-engine.md). Nothing in this document establishes that SoulScript's newer autonomous-cycle code has been released or run, or that Calibos has adopted the mechanism.

## Distinct hypotheses

**H-SCHED:** Given identical observations, model, memory, prompt budget, action set, environment, total decision opportunities, and inference capacity, a surprise-responsive scheduler produces better held-out prospective behavior than both fixed-period and random-timed scheduling. A gain over fixed alone is insufficient.

**H-ALLOC:** Under scarce processing resources, urgency-sensitive allocation improves time-critical correct action relative to uniform throttling at equal total budget, without intolerable neglected-work or false-alarm cost. Mere proportional slowdown does not support the functional allocation claim.

**H-IDENT:** Independently of scheduling, a protected identity store and mutable experience store causally outperform a matched single writable store on specifically defined continuity metrics. Architectural resemblance across repositories is prior art, not evidence for this hypothesis. Test separately to avoid factorial ambiguity.

## Scheduling experiment, primary causal comparison

Use a frozen deterministic event stream with surprise-relevant and neutral episodes, including genuine prediction violations, distractors, absent-event probes, delayed obligations, and periods with no external input. Run multiple predeclared independent histories, seeds, and renderer configurations; split development from held-out histories. Store a canonical snapshot and replay all exogenous events identically.

| Arm | Trigger or schedule | Matching principle |
| --- | --- | --- |
| F: fixed | Regular decision slots | Same total eligible cognition calls, token ceiling, observations and cumulative budget |
| R: random | Seeded randomized slot placement independent of event significance | Match F and S count, active window, minimum spacing and slot-count distribution |
| S: surprise responsive | Precommitted predictor computes prediction error and schedules or reprioritizes eligible slots | Equal realized decision-call, token and time/opportunity budgets |
| S-shuffled diagnostic | Replay the empirical distribution of S slots but permute their alignment to prediction errors | Tests whether specific event alignment matters beyond burstiness and nonuniform timing |

To avoid timing leakage, measure the predictor's CPU, data access, tokens and memory overhead, and either charge it to S or give the other arms budget-matched dummy computation without new information. Decide up front whether a triggered intervention **moves** a previously allocated slot or receives an incremental call. Prefer moved slots for the causal budget test. A run must not see more external event data merely because it wakes earlier. Record actual context bytes presented, since nominally equal tokens can contain different information.

Random schedules must not be allowed to collect more episodes through extra observation windows. Use a common read-only sensory event log with timestamps and immutable event IDs, explicitly reporting observation-to-response latency. Replay paired seeds, include no-surprise null streams, and instrument cases where prediction error is high but action is irrelevant. If S wins only because it observes different information or uses extra calls, the scheduling-specific claim fails.

**Primary outcome (freeze before execution):** proportion of held-out time-bounded commitments and external-world obligations satisfied correctly by their deadlines, with full denominator and missed-opportunity accounting. **Co-primary or separately declared secondary outcomes:** event-appropriate response latency, false urgent interventions, correct belief revision after unexpected evidence, missed neutral obligations, source-grounded recall with absent-event rejection, identity-drift probes, and normalized compute. Do not promote a post-hoc "felt alive" rating to a primary measure.

**Decision rule:** an S-over-F effect without S-over-R (and without improved alignment versus S-shuffled) cannot be called surprise-specific. Require repeated paired-seed evidence and effect-size intervals established under a later sealed pre-registration. No p-values or superiority claims are asserted here. Preserve negative results.

## Scarcity-allocation bridge to EXP-2026-010

The journal's [EXP-2026-010](../EXPERIMENT_LEDGER.md) recorded threat-processing share of approximately 41% under scarcity and 26% under abundance in the PEMA allocator. This is a **separate experimental system**. The bridge is a candidate replication of the *functional distinction*, not an export of PEMA's effect size to SoulScript.

Hold task demands, deadlines, reward stakes and event traces constant while crossing resource budget (abundant versus scarce) with allocator policy:

| Policy | Functional definition | Null concern |
| --- | --- | --- |
| Uniform throttling | Reduce processing rate or call count proportionally without reprioritizing categories | Models scalar fatigue only |
| Urgency-sensitive reallocation | Reassign bounded capacity toward high-cost, time-sensitive evidence or actions | Must improve urgent outcomes at a measured cost to other work |
| Random reallocation | Reassign capacity to categories with the same overall distribution but independent of urgency | Rules out reallocation or variability alone |
| Demand-only diagnostic | Change task mix without actual budget scarcity where feasible | Rules out need/demand explanations already considered in PEMA |

Track *absolute* useful urgent work in addition to percentage share. A rising share due only to the collapse of background processing is not a genuine prioritization benefit. Measure urgent task completion, ordinary-task starvation, wrong urgent classification, total capacity, latency, memory integrity, resource conservation, and deterministic replay. Match work opportunities and charge all predictor/allocator overhead to the appropriate condition.

## Calibos candidate gate, not an integration instruction

The source-owned [calibos-mind](https://github.com/Azimn/calibos-mind) explicitly prohibits trigger proliferation, bulky wake-ups, identity rewriting by an outside review, and unverified cognitive narration. A scheduling mutation is an optional proposal through its own builder/critic selection process. It is not approval to change heartbeat semantics, the cartridge, private memory, queue policy or dream isolation.

**Builder submission** must include the exact base commit, one reversible scheduler-only modification, objective fitness, resource ledger, no-input traces, null/random schedule controls, and a protected baseline replay.

**Critic challenge** attempts to kill the mechanism by removing event-prediction alignment, permuting surprise labels, isolating the predictor, observing repeated rumination triggers, testing starvation and quiet periods, and checking full separation of private records and renderer behavior. The critic must report a concrete failure condition before any run.

**Promotion gate:** only a predeclared held-out, resource-matched benefit, with no trigger proliferation or authority regression, can justify a later production proposal. Negative or null results must remain in the journal. Do not install the mechanism merely because source architectures resemble one another.

## Provenance and next step

Upstream source: [SoulScript head f299a752](https://github.com/DrTHunter/SoulScript-Engine/commit/f299a752579cefbd557c59cd00da0f9e73b30eb5). Calibos inspected public head at time of registration: [18497706f](https://github.com/Azimn/calibos-mind/commit/18497706f9ada6840c1e3bc40bf121941f9332e7). Prior evidence record: [EXP-2026-010 and 011](../EXPERIMENT_LEDGER.md). Proposed protocol requires source-owner review, sealed test scenarios, exact cost matching, and a named critic before execution. **Results: none.**
