# Research review: Hirsh (2026), The Game of Self

Date: 2026-10-09  
Status: reviewed theoretical framework, no empirical validation for Pretorius  
Target project: [The Doctor Lives](https://github.com/Azimn/The-Doctor-Lives)  
Detailed architecture review: [draft PR #30](https://github.com/Azimn/The-Doctor-Lives/pull/30)  
Prior negative/mixed comparator: [Stage 01 SelfBindingModulator report](https://github.com/Azimn/The-Doctor-Lives/blob/5629f1cba0000047321fffbbfc6367df23a173c2/results/self_binding/STAGE_01_EXECUTED_MEASUREMENTS.md)

## Primary citation and evidentiary classification

Hirsh, Jacob B. 2026. "The Game of Self: Identity and Experience as Active Inference." *Personality and Social Psychology Review*, first published March 5, 2026. https://doi.org/10.1177/10888683261422344 ; full paper https://journals.sagepub.com/doi/full/10.1177/10888683261422344 ; PubMed 41784280.

A peer-reviewed integrative **conceptual/theoretical account** proposing a hierarchical generative self-model with Bayesian semantic-to-episodic and episodic-to-semantic inference. The paper contains worked probabilities and testable hypotheses but not a ready-to-install AI system or demonstrated cross-model persona continuity.

Supporting computational account of active inference's pragmatic/epistemic action distinction: Friston et al. 2016, "Active inference and learning," https://pmc.ncbi.nlm.nih.gov/articles/PMC5167251/.

## High-value extraction

1. The "Me" as semantic self-description is distinct from the "I" as perspectival experience; one cannot simply identify a richer identity ledger with subjecthood.
2. Trait-like priors, situation-dependent self states, relationship adaptations and autobiographical narrative occupy different timescales. An agent can vary behavior contextually without losing identity.
3. The high-level semantic self predicts meaning and probable experience in each context. Episodes, when observed with sufficient reliability, update higher-level self-belief distributions.
4. The direction of revision depends on *relative precision*. A single ambiguous contradiction may produce a local episode/context refinement; repeated reliable contradictions across independent settings should favor changed semantic priors. Never rewrite source-verified facts to preserve narrative coherence.
5. Self-knowledge enables inference about how others perceive the agent and how they may react. Models of other people's feelings remain hypotheses, not private-data access or facts.
6. An epistemic action (asking, observing, testing) can disambiguate competing explanations. Action must be subject to existing permissions, world constraints, privacy and consent, not used to forcibly make the world confirm the self.
7. Table 1 divides proposed falsifiable effects into two-way inference, uncertainty reduction, future simulation/contextual identity shifts and social prediction. The methodology section proposes small sets of informative **situations** and full distributions, rather than isolated single-valued trait labels.

## Impact on Pretorius

The v0.4 production brain already owns episodic source-ranked records, design invariants, state policy bridge, recurrent choice, relationships, concerns, commitments and versions. However, it does **not** have a demonstrated independent predictor linking a particular self hypothesis to the expected *next* lived episode, then adjusting that hypothesis based on verified new events. The previous self-binding research stage changed scoring but no action argmax, so this should not be addressed by silently raising bonus ceilings.

Recommendation: **read-only predictive self-loop in an independent experimental harness first.** Train from verified chronological world-action/context/outcome episodes only; report insufficiency if none exist. Forecast expected state and action distributions; log predictions *before* events; score with Brier/log-loss, coverage and correct source grounding; use new held-out contexts including Henry pressure, absent memory, conflicting source and delayed promise. Distinguish forecasts from actions; do not add a second world or identity store. Evaluate against strong simple context-frequency and recurrence baselines. Freeze UPPB/first-person firewall and production recurrent baseline.

Specific hypothesis: an evidence-calibrated two-way self model may improve context-appropriate consistency and prospective followthrough, **without** making reactions uniform. Genuine identity development should be characterized by reliable gradual self-posterior updates and corrected context-sensitive expectations, not immutable style and not uncontrolled persona drift.

## Failure/risk register

Conceptual theory is not evidence of efficacy. Strong priors can produce motivated blindness; a model that tries to make observations confirm its self-image can distort facts or pressure partners. Rhetorical use of Bayesian terms without fitted likelihoods is a weak substitute for empirical work. Relationship context may reproduce agreeableness instead of identity. A literal claim of AI subjectivity is unwarranted. Context labels, world witness identity, epistemic classes (fictional preawakening / reconstructed / lived), trust of feedback and consent must be kept distinct.

## Decision

**Priority: HIGH for a new causal experiment; production status HOLD.** The paper supplies a more falsifiable account of adaptive identity than scalar retrieval salience. The next milestone is a small, source-verified, shadow-mode predictor with chronological calibration and explicit uncertainty. Only after outperforming properly matched baselines should any policy modulation be considered.

The detailed design and staged experiments are in the linked Doctor Lives RFC. No experiment was run in this journal entry; do not call this an experimental result.

## Same-day executable follow-through, 2026-10-09

The theoretical proposal now has a working, isolated [Predictive Self Loop v0.1 shadow implementation](https://github.com/Azimn/The-Doctor-Lives/blob/research/predictive-self-loop-20261009/docs/PREDICTIVE_SELF_SHADOW_V01.md) in [The Doctor Lives PR #30](https://github.com/Azimn/The-Doctor-Lives/pull/30). It provides five separated interfaces: semantic identity -> expected action, context-conditional episodic adaptation, slow evidence-weighted semantic revision across independent situations, partner-observed behavior prediction, and permission-requiring epistemic inquiry suggestions. It also has a portable SHA-256-audited checkpoint and a read-only native BrainStore adapter.

[CI workflow 38015971437](https://github.com/Azimn/The-Doctor-Lives/actions/runs/38015971437), execution commit `b7d71ccd03ebf2ab37ce749db0aa87ea1e4cac44`, **passed 16 targeted tests** and exercised both synthetic/mock-world and native PretoriusBrain cases. Native chosen action: `create`; 10-category log loss `2.30258509`, and the shadow observation did not mutate the BrainStore. The model did **not** verify any external world effect. In a three-context *mock* case, one operational independence hypothesis changed from prior `0.75` to `0.60`, capped by the research revision rule. This is a mechanics demonstration, not evidence of an evolved authentic persona. [Source-referenced preserved result](https://github.com/Azimn/The-Doctor-Lives/blob/da6940416205b1b9ef5001ffb25cc5fb437542b8/results/predictive_self/STAGE_00_SHADOW_EXECUTED.json).

Status: **research implementation complete for v0.1 / production HOLD**. A real event attestor, independent temporal ground truth, chronological forecast calibration, and baseline-controlled source-disjoint challenge battery remain unimplemented. Neither this paper nor our synthetic CI result demonstrates subjective consciousness, true active-inference optimization or improved cross-renderer identity continuity.
