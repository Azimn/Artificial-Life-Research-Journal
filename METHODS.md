---
id: METHODS
title: Research Methods
type: reference
status: active
updated: 2026-09-18
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
