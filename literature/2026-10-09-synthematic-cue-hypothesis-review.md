---
id: LIT-2026-10-09-SCH
title: Synthematic Cue Hypothesis v0.2.1, critical review and evidence
type: literature-note
status: source-reviewed-working-manuscript
updated: 2026-10-09
authors: []
year: 2026
url: https://github.com/Azimn/Attractomancy/blob/fb28c716ec2fd29e7d8ae31ef1e35431ef20512a/papers/synthematic-cue-hypothesis/PAPER.md
tags:
  - synthemata
  - persona-conditioning
  - three-timescale-mechanisms
  - cue-ablation
research_questions:
  - RQ-001
  - RQ-006
---

# Synthematic Cue Hypothesis: source-pinned critical review

**Citation:** *The Synthematic Cue Hypothesis: Symbolic Recognition and Behavioral Reconstruction Across Three Timescales in Language-Model Personas*. Attractomancy working paper **v0.2.1, October 9, 2026**, unpublished and not peer reviewed. Attribution and affiliations remain pending source-author approval; do not invent them. [Frozen source at commit `fb28c716`](https://github.com/Azimn/Attractomancy/blob/fb28c716ec2fd29e7d8ae31ef1e35431ef20512a/papers/synthematic-cue-hypothesis/PAPER.md), Git blob SHA `6743e522465e4c64cbd4432bad907e34109fe6eb`.

## Hypothesis and mechanism decomposition

A compact symbol, name, glyph, phrase or ritual sequence can induce characteristic model behavior by three **nonexclusive and nonidentifiable-as-additive** channels. **Timescale I, pretraining priors:** shared cultural symbols may prime a general discourse register but do not expose inaccessible private facts. **Timescale II, within-context binding:** repeated consistent pairing of a novel cue with behavior can shift responses while the conditioning context is present; apparent carryover after a reset requires a leakage and state-access audit. **Timescale III, persistent external record:** a cue may address a versioned persona file, relationship ledger or retrieval policy and thereby reconstruct behavior in a new session or renderer. This is a retrieval/reconstruction process, not automatic persistence of an identical internal subject.

The paper's `Delta_cue` contrasts blinded expected held-out performance under an intervened target cue versus a matched control cue with model, task, history and retrieval policy otherwise specified. It does **not** identify a particular latent neural code. The design must test interactions among prior, within-context learning and external record, rather than assign numerical proportions to those pathways post hoc.

The limited Iamblichus `synthemata` analogy reverses explanatory direction: the utility of a sign may depend on associations in the **interpreter**, not the conscious beliefs of the person using the sign. This is an interpretive framework, not historical evidence that theurgy accessed a machine or that ritual has metaphysical efficacy.

## Prospective directional predictions

**P1:** familiar unconditioned cues should outperform neutral/nonce cues for generic discourse markers, not private biography. **P2:** true within-context cue-profile pairing should outperform shuffled or unpaired exposure when examples and tokens are matched. **P3:** the context-only benefit should disappear after a verified reset without retrieval. **P4:** correct external records should outperform cue-only prompts for private autobiographical details and commitments after reset. **P5:** when retrieved records are literally identical, meaningful cues should offer little remaining identity-specific advantage over an arbitrary retrieval key. **P6:** any engineering efficiency advantage must survive comparison with the shortest sufficient plain-language instruction at the same quality threshold, counting cue training, archival storage, retrieval and invocation rather than marginal invocation tokens alone.

These are falsifiable predictions, not a recital of confirmed effects. The manuscript requires quality-cost Pareto comparisons, held-out multi-dimensional profiles, independent scoring, source- and prompt-matched controls, exact model versions and discontinuity audits.

## Executed exploratory evidence available October 9

The [30-case zero-shot pilot analysis](https://github.com/Azimn/Attractomancy/blob/fb28c716ec2fd29e7d8ae31ef1e35431ef20512a/experiments/EXP-A_ZERO_SHOT_SYNTHEMATA/PILOT_ANALYSIS.md) found **no demonstrated familiar-cue superiority**. **29 of 30** outputs hit the 88-token cap and the lexical proxy rewarded cue echo or discussion of the requested style. This is a negative or indeterminate feasibility result, not a definitive disproof of P1.

The [A2/B1/B0 follow-up report](https://github.com/Azimn/Attractomancy/blob/fb28c716ec2fd29e7d8ae31ef1e35431ef20512a/experiments/SCH_FOLLOWUP_2026_10_09/RESULTS_STATUS.md) records that A2 discourse induction is not robustly established and B1 conditional rule integration does not demonstrate reliable mapping reversal: Qwen2.5-0.5B changed only **1/4** diagnostic rule-conflict pairs when mapping flipped. SmolLM2-360M failed the required strict output format in B1's demonstration-conditioned responses. These are limitations, not grounds for dropping negative cases.

B0's deliberately simpler mapping produced a **narrow within-context positive control**: on Qwen2.5-0.5B, stable and flipped arbitrary label mappings were **7/8** and **8/8** correct, with **7/8** matched-prompt answer reversals. The Qwen2.5-1.5B run reported **6/8** strict accuracy for each mapping and **8/8** reversals under prespecified punctuation-tolerant parsing. SmolLM2-360M did not reliably show the effect. Scrambled-pairing control anomalies persisted, and direct explicit instructions achieved comparable accuracy for approximately half the tokens. Thus B0 supports only simple local association on the tested models; it does not support long-term identity, integrated policy or efficient symbolic persona restoration. Qwen2.5-1.5B **A2/B1** remained pending in the read report; do not infer its outcome from the B0 result.

Primary raw materials remain in Attractomancy: [original pilot](https://github.com/Azimn/Attractomancy/tree/fb28c716ec2fd29e7d8ae31ef1e35431ef20512a/experiments/EXP-A_ZERO_SHOT_SYNTHEMATA/results/pilot-open-model), [follow-up results and scripts](https://github.com/Azimn/Attractomancy/tree/fb28c716ec2fd29e7d8ae31ef1e35431ef20512a/experiments/SCH_FOLLOWUP_2026_10_09). This journal read repository-reported results; it did not rerun the models or independently blind-score the responses.

## Consequence for the continuity research program

Distinguish **cue-induced discourse**, **local label binding**, **multi-constraint decisions**, **external-state restoration**, and **partner-specific relationship continuity** in evaluation. Generic symbolic priming is not autobiographical evidence. A cue-only fresh session is a **zero-shot calibration**, not a persistence test. In Le Refuge EXP-0001, `Apocalypse.txt` specifies a symbolic-theological **discourse regime**, not a well-defined biographical subject. Do not import Ælya autobiography from another file when defining its information-matched controls.

The DCH partner-specific mechanism is orthogonal but experimentally compatible: cross partner identity, context presence, cue type and archive access while retaining privacy, information-parity, versioned sources and exact costs. The [DCH research note](../programs/DYADIC_CONSTITUTION_HYPOTHESIS_RESEARCH_NOTE_2026-10-09.md) describes that proposed test without treating it as a completed finding.
