---
id: METHODS
title: Research Methods
type: reference
status: active
updated: 2026-10-08
---

# Research Methods

The program is exploratory, but the journal should make exploratory work progressively more falsifiable.

## Experimental discipline

Prefer causal comparisons over demonstrations. When possible, change one mechanism while holding founder state, scenario family, evaluation boundary, random seeds, and compute budget constant.

Separate training, validation, adversarial, and terminal evaluation when an experiment can overfit.

Preserve failed hypotheses and confounds. A result that invalidates an architectural assumption is scientifically useful.

Match the true causal budget. In neural experiments, "ticks" are not interchangeable with actual neural update calls. In agent experiments, wall-clock time is not interchangeable with decision opportunities.

Use identical-history replicates when claiming experience-driven divergence.

Use intact, virgin, lesion, graft, and ablation controls when asking where a learned function resides.

Do not allow a language model to manufacture the phenomenon being measured when the experiment is intended to evaluate nonlinguistic substrate, identity, memory, or motivation.

## Evidence hierarchy

Strongest evidence usually comes from replicated causal interventions that survive held-out evaluation.

Useful but weaker evidence includes deterministic traces, longitudinal behavioral comparisons, and controlled simulation outcomes.

Demonstrations, compelling transcripts, and subjective impressions can motivate an experiment but should not be promoted into causal evidence.

## Provenance

Every completed experiment should record the source repository, branch, commit, configuration, seeds, evaluation set, and location of machine-readable results when available.

If a historical result is reconstructed from conversation rather than directly from code or preserved artifacts, mark it as reconstructed.

## Interpretation discipline

Distinguish:

- what was measured,
- what changed,
- what interpretation is supported,
- what alternative explanations remain,
- what the result changed about the next experiment.

Avoid claims of consciousness, sentience, biological equivalence, or human psychological fidelity unless a future project explicitly develops valid evidence for those claims.

## Cross-project comparison and cumulative evidence

For the active [Character Continuity Program](programs/CHARACTER_CONTINUITY_PROGRAM_V1.md), every reported finding needs a stable evidence ID, its source-repository report, original raw result and commit references when available, an explicit task and denominator, known reuse of cases/seeds, competing explanations, and the next architectural decision. The [evidence register](programs/CHARACTER_CONTINUITY_EVIDENCE_REGISTER_V1.md) is a finding index, not a statistical meta-analysis.

Distinguish cue-match top-1 accuracy from correct-and-accepted sourced recall, from contradiction and never-seen false acceptance, from history-sensitive decisions. Always report answer coverage: reject-all is not robust recollection. A language model's rendered fluency cannot substitute for source truth or a causal lesion of the claimed mechanism.

A fair comparison must document which arm has access to readable event text, learned weights, mutable history, external indices, renderer context, additional pretrained parameters and training supervision. Equal random seeds alone do not make arm costs or available information equivalent. Match the resources appropriate to the causal question and report remaining asymmetry explicitly.

Reuse of published authored prompts is exploratory. Independent confirmatory claims require a new reviewer-adjudicated sealed benchmark, source- and episode-disjoint fitting where relevant, registered stopping rules, pre-frozen thresholds and no post-hoc tuning on test cases. Production release gates for The Doctor Lives remain independent of research significance.

