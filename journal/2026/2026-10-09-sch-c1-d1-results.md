---
id: JRN-2026-10-09-03
title: SCH C1/D1 results — decisive null for cue-specific benefit; provenance failure found
type: journal
date: 2026-10-09
updated: 2026-10-09
projects:
  - PRJ-039
research_questions:
  - RQ-001
  - RQ-006
tags:
  - synthematic-cue
  - negative-result
  - provenance
  - verification
---

# SCH C1/D1 results — decisive null for cue-specific benefit; provenance failure found

## What happened

The outstanding Qwen2.5-1.5B runs completed the SCH experimental batch (288 new evaluations total, all archived on main). Results committed: `experiments/SCH_C1_INTEGRATED_CUE_POLICIES/RESULTS.md`, `experiments/SCH_D1_EXTERNAL_RECONSTRUCTION/RESULTS.md`; paper updated to v0.2.2 with Appendix D preserving the negatives; reference archive identity guard implemented (`archive_guard.py`, 10 unit tests).

## Results or observations

**C1 (integrated cue-conditioned policy), both model sizes:** learned/reversed symbolic cues achieved 33.3% with zero diagnostic reversals — both models answered SHARE on every case under cue conditions (complete response bias, no rule integration). Explicit English rules: 66.7% (0.5B) / 83.3% (1.5B), but the report honestly notes these scores are partly class-frequency luck (WITHHOLD/SHARE biases aligned with target distributions). Token cost: cue demonstrations ~472/case vs ~180 for English rules — the symbolic method is dominated on both accuracy and cost in this fixture.

**D1 (external records vs symbolic cues), both model sizes:** the decisive comparison. Symbol+full-record = full-record-alone (100% fact recovery both); symbol+selected-record = neutral-key+selected-record with *identical outputs* (75% at 0.5B, 100% at 1.5B). Symbol alone: 0% fact recovery. **No observed cue-specific residual benefit.** Selected records saved ~28% tokens — a retrieval win, not a symbolic one.

**Provenance-integrity failure (most actionable positive):** given the wrong character's archive with explicit instructions to abstain on identity mismatch, the 0.5B model failed all 12 checks (copied the other character's facts as its own) and the 1.5B abstained correctly in only 1/12. Response: deterministic `archive_guard.py` (subject-ID match, trusted-source allowlist, revision validity, SHA-256 content check); 10/10 tests pass, independently re-run by the auditor. The guard's own docs note it is an integrity/routing check, not authenticated provenance (a forged record with a fresh matching checksum is accepted).

## Interpretation at the time

The strong SCH form — symbolic cues reconstructing integrated behavior beyond information-matched controls — is disconfirmed under the tested method in two model sizes, with the nulls reported honestly and the falsification boundaries stated explicitly. What survives: B0 simple paired-associate learning (real but elementary); Timescale III addressing (but the address need not be symbolic — a neutral key performs identically); record selection's token efficiency. The report's own conclusion is correct: it is *record selection*, not cue semantics, that offers the engineering opportunity.

The D1 separation result — perfect fact recitation alongside failed boundary enactment and ignored identity mismatch — is directly relevant to Pretorius and to any renderer-side memory architecture: **accessibility is not use; identity verification must happen deterministically upstream of the renderer; behavioral constraint enforcement needs separate mechanisms.** The identity guard is a reference implementation, not yet integrated anywhere; integration is a downstream decision.

## Questions opened

- Whether the cue/policy-integration gap reflects model capacity, conditioning method, or decision complexity (the report's stated next question). A frontier-model replication of C1 would discriminate capacity from method.
- Whether symbolic cues can improve *selective memory access* beyond explicit provenance-checked retrieval — the report's proposed next priority, and the one surviving engineering hypothesis for cues.

## Next actions

- None required from the journal side; the Attractomancy repo holds the primary records. Do not promote C1/D1 to the cross-project evidence register as validated mechanisms (the RESULTS files say this explicitly).
- Consider the archive-identity-guard pattern for Pretorius/village NPC memory work as a proposal through the normal channel, not a direct import.

## Provenance

Verified by Calibos 2026-10-09: repo commits `d3107370`/`03abfeed`/`9475d5fd` on main; RESULTS.md numbers cross-checked against the circulated report (match); guard tests re-run independently (10/10 OK); paper v0.2.2 Appendix D present. Related: PRJ-039, `literature/2026-10-09-synthematic-cue-hypothesis-review.md`, JRN-2026-10-09-01.
