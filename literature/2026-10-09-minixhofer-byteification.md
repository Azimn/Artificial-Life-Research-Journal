---
id: LIT-2026-BYTEIFICATION-001
title: Retrofitting language models to operate over bytes
type: literature
status: source-reviewed-not-independently-replicated
updated: 2026-10-09
authors: ["Benjamin Minixhofer", "Tyler Murray", "Tomasz Limisiewicz", "Anna Korhonen", "Luke Zettlemoyer", "Noah A. Smith", "Edoardo M. Ponti", "Luca Soldaini", "Valentin Hofmann"]
year: 2026
doi: 10.1038/s41586-026-11111-4
url: https://www.nature.com/articles/s41586-026-11111-4
tags: [published-prior-art, tokenizer-transfer, byte-level-modeling, model-stitching, representation-interface, architecture-transfer, character-continuity, symbolic-cues]
research_questions: [RQ-001, RQ-003, RQ-006]
---

# Retrofitting language models to operate over bytes

## Citation and source verification

Minixhofer, B., Murray, T., Limisiewicz, T., Korhonen, A., Zettlemoyer, L., Smith, N. A., Ponti, E. M., Soldaini, L., & Hofmann, V. (2026). *Retrofitting language models to operate over bytes*. *Nature*. https://doi.org/10.1038/s41586-026-11111-4

Published 2026-10-07. Version of record 2026-10-07. Source: [Nature article](https://www.nature.com/articles/s41586-026-11111-4). Author-released [training/inference implementation](https://github.com/allenai/bolmo-core); [training mix](https://huggingface.co/datasets/allenai/bolmo_mix); [evaluation suite](https://github.com/allenai/olmes). These are source-owned assets, not artifacts created or independently reproduced by this journal.

**Review scope, 2026-10-09:** Source-level inspection of the published article, including its method description, results, ablations, and availability statements. No local model runs, dataset audit, checkpoint reproduction, or independent statistical reanalysis. Claims below are attributed to the paper except where explicitly labeled program interpretation or proposed testing.

## Claim or contribution

The authors introduce **byteification**, a procedure to retrofit existing pretrained subword-tokenized LLMs for byte-level language modeling without training a comparably capable Transformer from scratch. The architecture retains the original large global Transformer and learns a new byte-facing interface around it. The authors call this family of architectures latent tokenizer language models (LTLMs).

The relevant architectural principle is **functional preservation under a change of input/output representation**, not direct evidence that a model's personality, autobiographical memory, or identity can be transferred.

## Methods and controls reported

The byte stream passes through an mLSTM-based local encoder, a neural boundary predictor, variable-length patch pooling, the retained global Transformer, patch depooling, and an mLSTM-based local decoder that predicts bytes and patch boundaries.

A two-stage conversion trains (1) the interface, with the global Transformer frozen, to approximate the source subword model's behavior, then (2) the full byteified model. The first stage includes boundary supervision and an activation-matching objective using the first layers of the frozen global model, rather than only matching static embedding vectors. The published configuration used 9.8 billion tokens in stage 1 and 39.3 billion in stage 2 (49.1 billion total).

Models include Bolmo 1B and 7B (OLMo-derived), Bwen 8B (Qwen3-derived), and Blama 8B (Llama-derived). The experiments compare source subword models, prior byte-level models, and an Olmo 3 continued-training control on the authors' data mix. Ablations examine staged versus direct training, patch boundaries, and compression. The paper additionally demonstrates reuse of a source-model instruction-tuning weight delta through task arithmetic in the byteified backbone.

## Findings actually reported

Bolmo 7B outperformed BLT 7B, a previous byte-level model trained from scratch, by **16.5 percentage points** on the article's aggregated STEM tasks. The byteified models approached the performance of their respective pretrained source LLMs and markedly improved character-level understanding in the study's evaluations. Results did not improve uniformly: the authors report weaker first-attempt coding for some converted models, even alongside stronger multi-sample coding and character-level performance.

The authors found a practical compression/performance trade-off by changing the average number of bytes per patch. Their task-arithmetic demonstration transferred instruction-following behavior from a post-trained Olmo 3 checkpoint to its byteified relative without repeating that post-training process.

**Interpretation boundary:** The work supports a viable representation-interface retrofit with substantial preservation of pretrained capability. It does **not** show unchanged latent states, unchanged internal connectivity, broad task superiority, preserved autobiographical identity, or successful persona continuity under arbitrary model swaps.

## Critical limitations for our purposes

The architecture changes alongside an additional nontrivial training intervention. Although Olmo continued training and other ablations help isolate the architecture's contribution, they do not prove an architecture-only effect for every capability. The training mixture includes synthetic character-understanding examples. Improved character-level scores can therefore arise from the interface, task-specific training, or their interaction.

Cross-model numbers are benchmark- and implementation-dependent. The authors discuss sampling-dependent code-diversity effects, which should not be confused with evidence of a generally better reasoning model. The inference results do not establish similar performance on our specific low-resource local CPU/Ollama deployment targets.

The demonstration of transferring a task-tuning weight delta between **related checkpoints sharing an aligned pretrained Transformer** is not evidence that autobiographical identity transfers between unrelated models. That distinction matters for Pretorius.

## Relevance to the research program

**Pretorius neural phenotype / model stitching:** The trained interface can change while the central pretrained computation is initially frozen. This is a published engineering precedent for studying whether a decoder, perception interface, or intermediate representation layer is responsible for observable phenotype, as opposed to the underlying recurrent or global substrate. Link to [Pretorius Neural Network](../projects/PRJ-002-Pretorius-Neural-Network.md), [RQ-001 persistent identity](../research-questions/RQ-001-persistent-artificial-identity.md), and the [Character Continuity Program](../programs/CHARACTER_CONTINUITY_PROGRAM_V1.md).

**Cue representation and Attractomancy:** Nonordinary glyphs, arbitrary labels, invented words, and meaningful names can change their representation when passing from subword tokenization to byte-level processing. That supplies a new intervention on the **cue encoding pathway** for symbolic-persona experiments. It does not establish any special property of ritual glyphs or prove symbolic identity restoration. Link to [Attractomancy project](../projects/PRJ-039-Attractomancy-Persona-Conditioning.md).

**SelfBindingModulator / perceptual gate:** An interface layer is a plausible place to instrument what is admitted to, aggregated for, or released from downstream processing. This is an architectural analogy only. The paper does not study an integrated self-model, conscious access, or any consciousness gate.

## Proposed discriminating experiment, NOT executed

**Question:** When the persona specification and external memory evidence are held fixed, does switching between the original subword model and its byteified descendant change symbolic cue sensitivity or character continuity?

**Candidate pair:** Source Qwen3 8B Base and its byteified descendant Bwen 8B, with exact upstream revisions and checkpoint availability pinned before any testing. Because these are base-model derivatives, use identical completion-compatible evaluation instructions. If instruction-tuned versions are introduced, explicitly document their different post-training and separate the comparison.

**Factorial design:** Representation (subword vs byteified) x cue (arbitrary identifier vs meaningful name vs unusual glyph) x persistence support (no external memory vs identical source-grounded memory). Maintain the same persona specification, independent memory facts, retrieval outputs, and probe set in each matched comparison. Include a no-cue calibration arm and a text-normalized/glyph-escaped control to disentangle symbolic interpretation from byte sequence/tokenization quirks.

**Primary measures:** Held-out behavioral decision agreement against a frozen character specification, correctly sourced autobiographical claims, contradiction false-acceptance rate, absent-memory abstention, and relationship/commitment consistency following interruption. Secondary: literal cue recovery, sensitivity to Unicode normalization and corruption, generic language performance, latency, and actual byte/token/context budgets.

**Controls and separation:** Blind-score independently authored probes; keep source-disjoint training and evaluation assets; pair random seeds and sampling settings where sampling semantics are comparable; report source model quality differences separately from the cue interaction; fix retrieved evidence and available information rather than equalizing only token counts; preserve exact prompts, outputs, hashes, model revisions, temperature and decoding configuration. Run adequate repeated trials and report uncertainty, including null results. Do not describe any observation as a validated identity transfer without causal memory/state ablation.

**Falsifiable hypothesis:** Byteification may improve *literal glyph/character sensitivity*, but it is not predicted to restore autobiographical information in the absence of memory support. If either model appears to recall nonexistent or held-out personal history with the cue alone, classify this initially as reconstruction or confabulation, not persistent identity. If improved cue fidelity fails to improve evidence-grounded character decisions, it weakens a simple cue-representation bottleneck account.

**Status:** Proposed literature-inspired test only. No new EXP ID, run, score, or implementation is claimed. Promote to a formal experiment only after the continuity program's benchmark and preregistration gates are satisfied.

## Decision recorded on 2026-10-09

Preserve this article as **strong published prior art for representation-interface retrofitting**, with **no direct empirical support for persistent AI identity**. Candidate use: controlled source-versus-byteified comparisons of cue representations and decoder/interface contributions. Do not replace the current memory or recurrent architecture on the strength of this paper alone.
