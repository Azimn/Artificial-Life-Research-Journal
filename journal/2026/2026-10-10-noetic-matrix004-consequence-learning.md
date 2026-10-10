---
id: JOURNAL-2026-10-10-NOETIC-MATRIX004
title: Noetic MATRIX-004 consequential policy learning — narrow improvement and neural null
type: research-journal
date: 2026-10-10
status: executed-synthetic-review-pending
projects:
  - The-Noetic-Engine
  - The Doctor Lives
research_questions:
  - RQ-001
---

# MATRIX-004: outcome-driven policy becomes causally effective, but not through the neural donor

The Noetic Engine research program was extended on an isolated branch with a source-bound action-specific contextual value head, signed outcome feedback, complete decision audit, no-learning controls and strict deterministic replay.

**Executable source and research review:** [Noetic PR #18](https://github.com/Azimn/The-Noetic-Engine/pull/18). **Frozen protocol:** [MATRIX-004](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-004-consequence-learning/experiments/PROTOCOL_MATRIX_004.md). **First verified CI:** [run 38058384913](https://github.com/Azimn/The-Noetic-Engine/actions/runs/38058384913), commit `16c1ce27c8e3c5ee0989e95e8fbc73cdce875dff`. **Frozen fixture SHA-256:** `d691a6e66d2f22d71b53d7151e264669b3e0cbfa091c943fd68f049113fc1b0e`. [Full outcomes and limitations](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-004-consequence-learning/results/MATRIX_004_RESULTS.md); [durable case-level evidence](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-004-consequence-learning/results/matrix_004/cases.json.gz).

The prespecified study used twenty authored train scenes, ten authored held-out scenes, five forced-action observations per train scene, six fixed seeds, and six policy variants. All arms received identical action/outcome exposure (3,600 total training interventions, 360 held-out action choices). The external-to-agent scoring function was a **local deterministic world rule written by the implementer**, not independently human-adjudicated. Input included a strongly structured four-factor world state and no language-inference requirement.

Held-out toy-world success: full Noetic 36/60 (60%), frozen controller 24/60 (40%), non-neural signed learner **36/60 (60%)**, no-recurrent head **36/60 (60%)**, no-intention head 30/60 (50%), explicit scripted heuristic ceiling 60/60 (100%). These are ten distinct test cases repeated over six seeds, **not sixty independent evaluation samples**. On the full architecture, all accuracy gain compared with frozen came from a stable/no-action-needed category. Both models still failed every repeated confirmed-hazard and distress scene.

**Interpretation:** This is the first software-level result in the program showing signed outcome learning selecting more *world-rule-correct* actions rather than merely shifting internal values. However, the **recurrent and developmental Noetic components provide no incremental correctness advantage over the simple non-neural signed controller in this fixture**, and the hand-coded world-rule policy is much stronger. That negative matters more for the morphogenetic-identity thesis than the small positive in a synthetic classification world.

**Provenance limit:** `operator_scored` source evidence is replayable but not cryptographically authoritative. An admitted caller-provided outcome may still be misleading. The author-generated fixture and rule cannot substitute for independently designed and human-rated consequential scenes. Models did not handle ambiguous natural language, live renderer swaps, false memory, new relationships, long-horizon autonomy, consciousness or actual world physics. The historical donor E4 fresh-decoder failure remains unclosed; EGREGORE-001 still blocks production promotion of inferred social beliefs.

The archived experiment was rerun after audit improvements. A GitHub archival comparison initially failed because **wall-clock timing is nondeterministic across runs**, not because action/reward evidence changed. The archive comparator was corrected to preserve the first raw timing values while checking deterministic source, reward, policy and case records independently. This difference is documented and covered by tests; never claim the full timed JSON is byte-for-byte repeatable.

**Next:** [Noetic MATRIX-005](https://github.com/Azimn/The-Noetic-Engine/issues/17) targets independently authored interactive environments from TALES, ALFWorld or TextWorld with objective external action consequences, while the separately open [MATRIX-004 independent character-quality gate](https://github.com/Azimn/The-Noetic-Engine/issues/16) still requires human evaluation of *justified identity change*. This journal entry is additive and does not alter existing daily capture tasks. No NoeticBrainAdapter or definitive Pretorius brain modification was made.

The prior [MATRIX-001–003 journal synthesis](https://github.com/Azimn/Artificial-Life-Research-Journal/pull/13) remains a separate review submission.
