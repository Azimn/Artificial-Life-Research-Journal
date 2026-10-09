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

[Successful synthetic six-arm provisional run 37871790784](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37871790784) found familiar cue correct event matches for original lexical vs synthetically rewired lexical **8/159 vs 9/159**, and externally pretrained MiniLM original vs rewired **2/159 vs 1/159**. **All six synthetic arms scored 0/31** genuine unseen fourth literal source cue matches. This is a negative **nonbiological synthetic** result, not yet evidence about fly topology. The real v783 publisher-verification workflow was still executing when this journal entry was authored; its result must later be appended with actual original case links and SHA, regardless of sign.

## Decisions and falsification gates

Preserve Pilots 08–11 as immutable completed exploratory evidence. Do not reinterpret known trained cue improvement as unseen semantic transfer. An external semantic encoder can be tested, but must never be credited as novel semantic knowledge learned by the fly connectome. Causal topology advantage requires original-vs-degree-matched comparisons with encoding and training held identical, then a stricter contact-weighted null and multiple seed replications. The fourth source-cue set is unreviewed, only 31 cases; independent human-authored paraphrases remain a planned confirmatory test.

Maintain the [Artificial Life Research Journal](https://github.com/Azimn/Artificial-Life-Research-Journal) as the **canonical cross-project intellectual record**, with raw evidence and runnable implementation in each experiment's owning repository. No result from this line demonstrates a finished or definitive Pretorius; that is a distinct deliverable in The Doctor Lives.
