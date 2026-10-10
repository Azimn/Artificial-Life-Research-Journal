---
id: JOURNAL-2026-10-10-NOETIC-MATRIX005
title: Noetic external-world text-game trial and exact non-neural trace null
type: research-journal
date: 2026-10-10
status: executed_external_world_benchmark_review_pending
projects:
  - The-Noetic-Engine
  - The Doctor Lives
research_questions:
  - RQ-001
---

# Noetic MATRIX-005: real game-world interface, no incremental neural benefit

The Noetic line has advanced beyond author-coded scoring rules to an **independently developed external text-game engine**. [Noetic PR #19](https://github.com/Azimn/The-Noetic-Engine/pull/19) introduces an auditable research-only command port between the Noetic cognitive field and TextWorldExpress 1.1.0 (Java 17/Python 3.12). It drives third-party games using world-provided legal commands, natural-language scene descriptions and world-owned scoring. No privileged game state, generated gold path, paid model, language-model inference or production Pretorius autobiography was used.

**Frozen protocol and evidence:**
- [MATRIX-005 protocol](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-005-textworldexpress/experiments/PROTOCOL_MATRIX_005.md)
- [Executed results](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-005-textworldexpress/results/MATRIX_005_RESULTS.md)
- [Post-hoc full-trace diagnostic](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-005-textworldexpress/results/MATRIX_005_TRACE_AUDIT.md)
- [Permanent raw case-level archive](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-matrix-005-textworldexpress/results/matrix_005/cases.json.gz)
- [First full CI execution](https://github.com/Azimn/The-Noetic-Engine/actions/runs/38060954980), SHA `0e010c0fa961fad3824a973fbfe76f89bf8cff62`, 81 tests passed, 48 independent benchmark test-game episodes across two official TextWorldExpress game families and six conditions. Subsequent diagnostic analysis CI: https://github.com/Azimn/The-Noetic-Engine/actions/runs/38061116435.

The evaluation used three official game training seeds per family with one **common random-behavior training transcript** replayed to every policy arm. Four official test-fold seeds per game were run from versioned isolated restored checkpoints. All policies were limited to 18 actions per episode. No test-world feedback was used to update action weights.

**Observed task success (Coin Collector / TextWorld Commonsense):** full Noetic 1/4 and 0/4; no-recurrent 1/4 and 0/4; simple signed non-neural learner 1/4 and 0/4; frozen 0/4 and 0/4; lexical heuristic 3/4 and 1/4; uniform random legal policy 2/4 and 1/4. Full Noetic reached partial average score 0.50 in Commonsense but no terminal wins.

**Decisive ablation null:** the full Noetic field-plus-recurrent controller and the simple signed-only learner (and no-recurrent controller) produced **exactly identical actual command histories for all eight test games**. The field's bounded bonus may appear in scores but changed no external command choices here. This is more diagnostic than the equal aggregate win rates and does not validate morphogenetic identity.

Post-hoc data exposed important fairness limitations: the common random training histories had only **two positive reward transitions in Coin Collector** and **fourteen in Commonsense**. The frozen policy chose `inventory` for every one of its 72 test actions per game family due to default tie ordering. Its zero-win result is a particularly weak control; strong scripted lexical and uniform random baselines must remain visible.

**Research interpretation:** Noetic can now record witnessed observations and externally determined consequences across a durable replayable subject ledger, and can act in independently authored stateful worlds through a separate, candidly labeled experimental policy. **It has not shown that its exotic developmental or recurrent features improve external decisions.** The current evidence still supports no claim of consistent identity, learned Pretorius phenotype, real-world magical effects, consciousness or self-aware simulation.

This journal entry is an **additive PR only**, leaving earlier journal work and existing daily GitHub automation untouched. MATRIX-005's next replication needs a genuinely competent exploration/history baseline, more official test-fold episodes, independent environmental authority, actual language-grounded decision making, and separately blinded human adjudication of justified character change. The Doctor Lives production brain, E4 fresh-decoder gate, and Egregore provenance/semantic block remain unchanged.
