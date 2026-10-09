---
id: JRN-2026-10-08-02
title: "Real FlyWire Synaptic Imprint: Memory Cues, Decoder Reliance, and Biological Wiring Controls"
type: journal-entry
status: active research, real Pilot12 pending
updated: 2026-10-08
projects:
  - PRJ-038
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
---

# 2026-10-08: Real FlyWire direct synaptic imprinting, from trained cue success to unseen cue failure

## Research question and chain of custody

Does a character-specific source-cue/content association live in numerical weights on actual original fly connectome synaptic connections, does it generalize to never-imprinted cues, and does the fly-derived directed topology matter beyond a degree-matched sparse network?

This record is a **cumulative source-linked continuation**, not six independent successful experiments. The source is [Pretorius-Connectome](https://github.com/Azimn/Pretorius-Connectome). The original 450-event, 27-episode Pretorius biography is explicitly **reconstructed fiction**. The original full-brain FlyWire v783 graph has 139,255 identified neurons, 15,091,983 aggregated directed neuron-to-neuron connections and 54,492,922 integer synaptic contacts. A [completed original-array audit](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/shared_memory/flywire-v783-real-csr-invariance-run37847525950.json) proves the biology-source arrays remain unchanged when source-linked features are consumed.

A **separate signed numeric learned overlay** was restricted to existing original directed synaptic slots. Model-only inference accepts a cue and outputs 256D signed lexical-feature coordinates. It cannot return narrative memories or event labels without an **external oracle target-content codebook** in a diagnostic evaluator. This distinction must remain in every interpretation.

## Real biological-topology computational measurements

| Pilot | Neural training intervention / test | Observed original full-FlyWire results | Key limitation |
|---|---|---|---|
| [Pilot08](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT08_REAL_V783_RESULTS.md) | Train 317 reconstructed source event associations, then probe 159 separate *untrained* literal recall cues | **0/159** correct source event matches versus **0/159** shuffled-content; 25,780 updated source-edge entries; 55/71 absent events falsely accepted | Narrow lexical representation and one-hop cue inputs |
| [Pilot09](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT09_REAL_CUE_TRANSFER_RESULTS.md) | Freeze original Pilot08 learned weights; replay *original training cue* against same-event different literal cue | **46/159** training-cue correct vs **1/159** shuffled; **0/159** different cue; 143/159 paired cues share no selected active lexical coordinate | Weight-specific cue association exists, but novel input lacks a route to its memory |
| [Pilot10](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT10_REAL_MULTICUE_RESULTS.md) | Three **explicitly trained** first/middle/last source cues per event, same 317 source records | First trained cue **25/159**, last trained cue **20/159**, mechanically shortened last cue **10/159**; last cue zero for exposure-matched concatenated and shuffled controls; **56/71** absent false accepts | A last cue taught during training cannot count as semantic or truly unseen retrieval |
| [Pilot11](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT11_REAL_UNSEEN_CUE_REJECTION_RESULTS.md) | Freeze actual original Pilot10 state; test first genuinely untrained source fourth cue on eligible paired cases; calibrate external acceptance only on source-disjoint validation | **0/31** unseen fourth literal cues correctly identified vs **4/31** trained cues for same 31. **30/31** untrained source cues share zero own-event active lexical features. Calibrated rejection reduced false accepts **56/71→5/71**, but correct accepted familiar source memories **18/159→0/159** | Input semantics and correct-versus-absent discrimination remain unresolved |

The above all use the **same underlying authored fiction, related source cues, heldout event IDs and source-aligned external oracle targets**. They must not be pooled as independent efficacy or replicated biology. They do not establish fly learning physiology, first-person Pretorius identity, semantic autobiographical recall or a claim about consciousness.

Actual original Pilot08 and Pilot10 learned sparse synaptic weights, rather than only their SHA hashes, were subsequently committed under [artifacts/imprinting/checkpoints](https://github.com/Azimn/Pretorius-Connectome/tree/main/artifacts/imprinting/checkpoints). The full original case-level JSON for Pilots 08–11 and experiment handoffs also live in permanent versioned Git evidence.

## What failed, what was learned, and where information resides

The learned overlay can yield **content-specific source cue associations above shuffled-content baselines on original FlyWire-directed connections** when its fixed input encoder activates coordinates that were actually trained. However, the BC01 input is a deterministic signed *lexical hash*, not a semantic embedding. One-hop training updates cannot contribute the intended event-specific weights when a new cue activates none of its source-event training coordinates. Pilots 09 and 11 empirically quantified this bottleneck. Multi-cue exposure helps familiar trained cues, while high absent-event false acceptance remains. A much stricter offline threshold can suppress false accepts only by rejecting real memories as well.

A positive result with an **external source content codebook** measures numerical association and externally decoded memory IDs; it cannot be called autonomous source recollection. Neither source-selected neuron mapping nor provenance of connectivity alone proves fly-specific causal advantage, because an ordinary network may provide the same learnable parameter resources.

## Next explicit intervention: Pilot12 (designed, synthetic passed, original biological result pending)

[Original Pilot12 preregistration](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/flywire-pilot12-semantic-rewired-null/docs/FLYWIRE_DIRECT_IMPRINT_PILOT12.md), [PR #26](https://github.com/Azimn/Pretorius-Connectome/pull/26), and [cumulative project scorecard](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/FLYWIRE_DIRECT_IMPRINT_PROGRAM_SCORECARD.md).

A six-condition factorial control holds original 317 source memories, three cue exposures, **original BC01 narrative-content target vectors**, signed synaptic update rule and external event scorer constant. It varies only **cue input encoder** (the original 256D lexical hash versus a pretrained local frozen MiniLM-L6-v2 sentence embedding projected into 256D signed coordinates), **wiring** (original full biological FlyWire versus double-edge-swapped degree-preserving rewired original eligible source→readout support), and in two conditions **correct versus shuffled target pairing**. The output neurons, input neurons, original synaptic-contact counts and learnable slot counts remain fixed. The rewired null preserves each source's eligible binary out-degree and each postsynaptic readout neuron's eligible binary in-degree, but does **not** fully preserve each destination's contact-weighted strength or posttraining nonzero weights.

Frozen pretrained language ability is an **external semantic prior**, not learned in fly-derived synaptic weights. MiniLM ONNX is pinned to Hugging Face revision `1110a243fdf4706b3f48f1d95db1a4f5529b4d41`, with a fixed 384→256 projection seed20261008, and executes locally without a paid inference API. Candidate ranking remains explicitly oracle-only.

[Successful synthetic six-arm provisional run 37871790784](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37871790784) found familiar cue correct event matches for original lexical vs synthetically rewired lexical **8/159 vs 9/159**, and externally pretrained MiniLM original vs rewired **2/159 vs 1/159**. **All six synthetic arms scored 0/31** genuine unseen fourth literal source cue matches. This is a negative **nonbiological synthetic** result, not evidence about fly topology. The original v783 whole-brain source-verification and six-condition benchmark subsequently succeeded and were recorded separately below; the synthetic results remain visible to prevent hindsight rewriting.

## Decisions and falsification gates

Preserve Pilots 08–11 as immutable completed exploratory evidence. Do not reinterpret known trained cue improvement as unseen semantic transfer. An external semantic encoder can be tested, but must never be credited as novel semantic knowledge learned by the fly connectome. Causal topology advantage requires original-vs-degree-matched comparisons with encoding and training held identical, then a stricter contact-weighted null and multiple seed replications. The fourth source-cue set is unreviewed, only 31 cases; independent human-authored paraphrases remain a planned confirmatory test.

Maintain the [Artificial Life Research Journal](https://github.com/Azimn/Artificial-Life-Research-Journal) as the **canonical cross-project intellectual record**, with raw evidence and runnable implementation in each experiment's owning repository. No result from this line demonstrates a finished or definitive Pretorius; that is a distinct deliverable in The Doctor Lives.

## Addendum: actual verified original full FlyWire Pilot12 result

**The separate original whole-brain biological-topology experiment PASSED**, [GitHub Actions run 37871790784](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37871790784), with source-checksummed 139,255 original root IDs, 15,091,983 aggregated directed pairs, all 54,492,922 integer synaptic contacts and source-aligned 450 fictional first-person memories unchanged. Original full machine-readable JSON **SHA-256 `bd005cce4cf74ab8f7854388375d7cc1d839974fa2caac26a3cf29033a71dfed`**. [Measured biological Pilot12 report](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT12_REAL_V783_PROVISIONAL.md) in now-merged [PR #26](https://github.com/Azimn/Pretorius-Connectome/pull/26). Per-run original learned weight files and cases remain in the successful Actions artifact; independent main-branch permanent archival is a separate completion gate.

The effective fixed feature-neuron population had **50,920 original eligible directed synaptic slots**. The deterministic binary-degree-preserving double-edge-switch null accepted **101,840 swaps**, changing 49,962 destinations while preserving each selected presynaptic source's eligible outgoing binary degree, each output target's eligible incoming binary degree, original per-edge contact counts and total trainable slots. The null was an isolated *control copy*; it does not preserve each target's contact-weighted total incoming strength or each trained model's number of nonzero weight deltas. The original biology remained unmodified.

| Real v783 condition, 951 source-cue exposures for 317 trained source events | Correct familiar trained literal cue, N=159 | Correct genuinely unseen fourth source cue, N=31 | Correct familiar and accepted using per-arm validation-only threshold, N=159 | False accepted truly absent test episode, N=71 |
|---|---:|---:|---:|---:|
| Original FlyWire / original BC01 cue | **20** | **0** | **0** | **5** |
| Degree-rewired FlyWire / BC01 cue | **21** | **0** | **2** | **6** |
| Original FlyWire / frozen pretrained MiniLM cue | **0** | **0** | **0** | **6** |
| Degree-rewired FlyWire / MiniLM cue | **1** | **0** | **0** | **13** |
| Original FlyWire / MiniLM, source-content shuffled | **0** | **0** | **0** | **5** |
| Degree-rewired FlyWire / MiniLM, content shuffled | **0** | **0** | **0** | **10** |

**Key causal finding:** Pretrained MiniLM cue input increased *overlap* of active signed input coordinates between unseen source fourth cues and their own originally trained source cue fields: the original lexical BC01 had **30/31** unseen cues with no overlap, whereas MiniLM had **5/31** with no overlap. However **every single original and rewired MiniLM condition still identified 0/31 source events**. Thus, cue-feature overlap is not sufficient for this one-hop synaptic-write/output-readout model to discriminate individual source memories. An input semantic encoder by itself did not rescue learned memory. The no-gain result must be interpreted as specific to frozen MiniLM→256D random projection→top-8 sparse features and fixed source target BC01 vectors; it does not show sentence embeddings generally cannot work.

**Topology interpretation:** Under identical original BC01 input conditions and source cases, original whole-FlyWire **20/159** vs rewired **21/159** produced no measurable advantage of the original fly wiring, despite matching binary eligible in/out degrees and source contact totals. In the pretrained-input arms the results were original **0/159** vs rewired **1/159**. No unique biological advantage can be claimed; these are correlated source cases and a single seed, with incomplete strength-matching in the rewired null.

**Rejection interpretation:** Validation-optimized oracle similarity gates gave an acceptable-looking low absent false-positive rate in some arms but nearly zero correctly accepted source memories. This repeats Pilot11's actual signal-versus-absence separation failure. The neural network itself still does not implement an internal absent-memory decision; any accepted event is assigned by an external source codebook.

This is a **negative controlled biological-topology result worth retaining**, not an unsuccessful prototype to hide. No demonstration of autonomous autobiographical content reconstruction, source-grounded cross-model identity, biophysical fly learning, generalized semantic recollection or the definitive Pretorius is warranted. The next discriminating intervention should isolate synaptic content capacity/readout separability from input geometry, preserve all external-oracle leakage gates, add contact-weighted topology nulls and evaluate independently written cues across multiple random seeds.
