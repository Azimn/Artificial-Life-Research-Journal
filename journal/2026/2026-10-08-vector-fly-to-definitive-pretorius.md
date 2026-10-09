---
id: JRN-2026-10-08-05
title: Vector Fly Autobiographical Retrieval to Definitive Pretorius: Real A/B and Review
type: journal-entry
status: measured preliminary and review pipeline complete
updated: 2026-10-08
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
---

# 2026-10-08: From Vector Fly retrieval to measured Pretorius dialogue

## Research decision

Connect the existing, immutable source-pinned 450-event reconstructed Pretorius autobiography to the **actual renderer-neutral production brain** in [The Doctor Lives](https://github.com/Azimn/The-Doctor-Lives), rather than write another unrelated character simulator. Keep the shared original autobiography external to the lived memory store and the recurrent neural weights.

## Evidence chain and reproducible execution

1. [Vector Fly SQLite v1](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/vector_fly/VECTOR_DATABASE_V1_RESULTS.md) created a source-verified 8,192-dimensional **lexical TF-IDF**, exact sparse index over all 450 reconstructed events (31,159 postings) and an episode-disjoint 317-record research index (24,261 postings). This is not dense learned semantics or a FlyWire synaptic engram.
2. [Source-verified agent API](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/vector_fly/VECTOR_AGENT_API_V1_RESULTS.md) provided read-only local HTTP source search and retrieval by original event ID. No insertion into canon or mutation of the biological connectome.
3. [Matched-state Stage 01](https://github.com/Azimn/The-Doctor-Lives/blob/main/results/vector_fly/PILOT01_RETRIEVAL_INTEGRATION_RESULTS.md) called the genuine Pretorius production brain. It produced six A/B packets under identical state; all five preexamined event-target questions retrieved an expected source in the top three. One absent-source probe was intentionally not counted. State digest and protected subject frame were unchanged.
4. [Real model Stage 02](https://github.com/Azimn/The-Doctor-Lives/blob/main/results/vector_fly/STAGE02_REAL_OLLAMA_DIALOGUE_RESULTS.md) executed [CI run 37873205792](https://github.com/Azimn/The-Doctor-Lives/actions/runs/37873205792) with CPU-only `qwen2.5:0.5b-instruct`, exact model digest `a8b0c51577010a279d933d14c2a8ab4b268079d44c5c8830c0a93900f1827c67`. Twelve real generated responses were preserved; four of six paired response texts changed. No blind human correctness was claimed.
5. The *complete original case-level* [104,580-byte JSON archive](https://github.com/Azimn/The-Doctor-Lives/blob/main/results/vector_fly/stage02-run37873205792/DIALOGUE_RAW_AB.json) preserves the paired actual prompts and replies, source event IDs, model metadata, and digests permanently. [Archival verification](https://github.com/Azimn/The-Doctor-Lives/actions/runs/37873701137) checked original file SHA-256 before Git commits.
6. [Stage 03 PR #27](https://github.com/Azimn/The-Doctor-Lives/pull/27) added the [masked human review rubric and scoring gate](https://github.com/Azimn/The-Doctor-Lives/blob/main/docs/VECTOR_FLY_BLINDED_REVIEW_STAGE03.md) over the real twelve replies. It balances anonymized A/B labels, keeps a private coordinator-only key, demands original-source-checked ratings, and rejects altered packets, missing ratings and false provenance. The complete production brain, migration and causal-audit tests passed.

## Directly supported findings

**Positive engineering result:** Source-verified memory retrieval can alter the language renderer's output with a fixed Pretorius brain state and without promoting reconstructed autobiography to lived experience.

**Negative or ambiguous behavioral findings:** One retrieved answer correctly mentioned the dead beetle but invented a homunculus identification; another conflated different events around Kappel's key. Two question pairs only echoed the questions. The baseline fabricated an 1982 spacecraft mission; the retrieved answer avoided that invention yet did not plainly reject the impossible premise. A changed reply is therefore not evidence of improved fact-grounding or personhood.

**Validity limit:** The six challenge prompts were exposed and previously examined by the experiment authors. Full all-450 lookup is not episode-held-out retrieval, and the small 0.5B model has obvious generation weaknesses. Human-scored supported-claim accuracy, contradiction rejection, provenance discipline and cross-turn continuity **remain unmeasured**. The masked Stage 03 presentation is a scoring tool, not genuinely independent double-blind validation; the raw public responses can still be seen.

## Competing hypotheses preserved

- **H1: External evidence loop** increases correct autobiographical specificity when a capable renderer interprets source passages accurately.
- **H2: Renderer bottleneck** masks possible retrieval advantages or misuses evidence by conflating chronology or hallucinating identity claims.
- **H3: More context can hurt** if high-similarity but mismatched episodes are injected and scored as recollection.
- **H4: Biological FlyWire topology** adds an advantage beyond matched lexical candidate retrieval only if a separate real-vs-rewired, equal-capacity controlled trial shows the effect. It was not used in the present Stage 02 experiment.

## Next confirmatory gate

Pre-register at least 30 *new*, independently written, source-adjudicated probes before inference and keep answer/source keys out of renderer prompts. Evaluate matched A/B conditions with one pinned, more capable free/local model (and preserve 0.5B as a calibration baseline), blind reviewer scores and repeated follow-up decisions. Report case-level facts, false affirmations, provenance, latency, paired confidence intervals and uncertainty; only then test real-vs-rewired FlyWire reranking on fixed candidate sets.

**Program interpretation:** Working infrastructure, measured causal influence on text, no demonstrated generalized character continuity. Keep the experiments open and treat negative outputs as findings, not failed artifacts.
