---
id: JRN-2026-10-10-02
title: "Mirror Keys (Pilot18): Train-Only Cue Metric Null and Original Cue Provenance Correction"
type: research-journal
status: original source experiment passed; 6 learned states independently archive-verified; postmerge archival not yet confirmed
updated: 2026-10-10
projects:
  - PRJ-038
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
---

# 2026-10-10: Mirror Keys — the wrong hypothesis for the cue annotations

The [Pilot17 Chamber of Echoes](2026-10-10-echo-chamber-episodic-routing.md) recovered 149/159 familiar TRAINED literal source cues and retained 16/16 first source events with explicitly allocated **EXTERNAL** numerical key-value episodic memory, but identified only 1/31 previously untrained fourth cues and correctly accepted none of those 31. We proposed a TRAIN-ONLY 64D discriminant metric to increase semantic addressing. **Pilot18 tested that intervention and rejected its performance hypothesis.** More importantly, source inspection showed a design category error: old event cue annotations were never certified semantic paraphrases.

## Predeclared numerical intervention and original source

[Owning PR #34](https://github.com/Azimn/Pretorius-Connectome/pull/34), [source-frozen protocol](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/pilot18-mirror-key-holdout-metric/docs/PILOT18_MIRROR_KEYS_PROTOCOL.md), [complete measured case report](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/pilot18-mirror-key-holdout-metric/results/imprinting/PILOT18_SOURCE_PROVISIONAL.md), code `src/pretorius_connectome/mirror_keys18.py`, original source provenance audit `scripts/audit_original_source_cue_candidates18.py`.

Original source 450 reconstructed fictional first-person Pretorius events/27 episodes, old seed31 317 train + 62 validation episode absences + 71 test episode absences, original 159 familiar train-source positives and 31 already explored original fourth-source literals, immutable L0/L1 and original BC01 signed CONTENT SHA. Frozen original local MiniLM ONNX digest `6fd5d72fe4589f189f8ebc006442dbb529bb7ce38f8082112682524616046452`; no API/subscription use. Original published FlyWire-v783 anatomy is **NOT used** by this explicit numerical EXTERNAL episodic key-value store.

Changed only source-cue exposures: for each of the original 317 train memories, learn/store *FIRST plus MIDDLE* original annotated source literal cue surfaces; fit one global 256→64 semantic address projection on the 317 positive view pairs. For 316 records with distinct original last cue, **THIRD annotated cue was withheld** from both training and stored numeric keys; all third numeric key slots explicitly ZERO and excluded from key cosine retrieval, even though allocated for equal capacity. Every model stores one original 256D CONTENT codeword per event, and exactly 633,600 float32 source-episode/projection array bytes, pretrained encoder weights excluded. The projection is fit from all 317 source train records before evaluation, so only FINAL 317 memory-load metrics are interpretable; the test is not streaming metric learning. Tested same-byte random MiniLM, first/middle pair-discriminant scatter `B−2W+0.002I`, deliberately MISPAIRED source train cue-positive discriminant, unsupervised PCA, lexical BC01 random and correct metric with deliberately WRONG source CONTENT. The source original 317-target identity oracle exists only in offline scorer. Model-native key-score gate selected ONLY from 62 validation-absent episodes and cannot use 316 third, 31 fourth, 159 familiar, 71 absent source test cases.

## Real measured source result (negative)

[Original source workflow 38058153904](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38058153904) passed with complete 1,211,379-byte six-arm source-case JSON SHA `9ac8dc764718ae09d1d3ec1b7d2d8298a3ca0cf62163e4213db6e9579de8fe75` and six actually trained learned projection/episode numeric NPZs; [repeat source + descriptive cue audit workflow 38058529199](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38058529199) also passed. [Independent six trained source-state archive verification 38058371248](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38058371248) succeeded. These results are NOT full original FlyWire-v783 synaptic computations.

| Equal-633600-byte external source-memory condition | Already trained FIRST original literals correct /159 | Genuinely withheld THIRD original literals correct /316 | Third cue correctly identified and accepted /316 | Reused fourth originally untrained /31 | Episode-absent71 wrongly accepted |
|---|---:|---:|---:|---:|---:|
| Frozen semantic MiniLM, original random projection | **145** | **0** | **0** | **0** | 11 |
| MiniLM first/middle pair-discriminant learned projection | **145** | **0** | **0** | **0** | 13 |
| MiniLM deliberately incorrect positive training pair metric | 145 | 1 | 0 | 0 | 13 |
| MiniLM unsupervised PCA projection | 145 | 1 | 0 | 0 | 9 |
| Original lexical BC01 2-key random projection | 144 | 2 | 0 | 0 | 7 |
| Correct semantic learned metric but deliberately WRONG source CONTENT | 0 | 3 *chance* | 0 | 0 | 13 |

All six original memory stores correctly identified and accepted **ZERO of 316** withheld third annotated source cues and zero of the 31 reused fourth original cues. All 62 validation absences were used only for threshold, at most 6/62 false accepted validation; 71 test episode-absent false accept remained 7–13/71. Trained first original source literal recall remained 144–145/159 in every correctly bound case because those exact keys were stored; unlike semantic new-cue generalization, this is a trivial direct key-memory mechanism. Wrong-source-CONTENT control's 3/316 chance matches are larger than any proper source condition. The particular global scatter metric therefore FAILED to improve this test. These outcomes should not be retroactively optimized or described as evidence of general semantic inability.

## Post-result key discovery: all source cues unreviewed and mostly distinct OBJECT anchors

After observing the null, we independently inspected the EXISTING original [450 source annotation sidecar records](https://github.com/Azimn/Pretorius-Connectome/blob/main/memories/annotations/v12_450_sidecars.jsonl), [450 actual fictional source narrative texts](https://github.com/Azimn/Pretorius-Connectome/blob/main/memories/current/Pretorius_v12_450_Events_Complete.jsonl) and filed a [reproducible post-hoc source audit](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/pilot18-mirror-key-holdout-metric/results/imprinting/PILOT18_ORIGINAL_CUE_SOURCE_AUDIT.md).

Original file content gives **450/450 annotation_status=`unreviewed_candidate`**, **1,463** total annotated cue surface phrases, **1,453** of three words or fewer, median **two** words. Among **448 original records** with three selected distinct cues, **446/448** had no shared literal word between original first and last cue phrases; exact last cue surface was present verbatim in only **107/448** original associated narrative texts. Examples: original E09-001 source annotated cue details `turned glove`, `millstream map`, `green tape`; E09-002 `thank-you letter`, `fresh sheet`, `stove`; E01-001 `camphor`, `beetle`, `second brass key`, `cracked lens`. These are cues to DIFFERENT ASPECTS of one experience, **not independently validated semantic paraphrases**. Word overlap does not prove semantic relatedness or lack of it; annotation status is explicitly unreviewed. There is no documented independent human-written gold paraphrase panel.

**Correction to earlier broad research framing:** near-zero fourth cue matching in Pilots08–18 primarily measured failure to associate NEW SHORT EVENT-DETAIL ANCHORS with source experiences **without storing their actual association**, rather than failure to recognize independently written meaning-preserving paraphrases. We should not continue to call 31 old fourth or 316 withheld third as semantic paraphrase success/failure sets without provenance. This is a **post-hoc explanation and research-data-quality finding**, not new independently validated causal proof. It must never drive retrospective threshold or hyperparameter tuning on the current frozen tests.

## Distinct follow-on experimental research questions

**Episodic relationship binding:** Can the system use original source NARRATIVE and explicitly evidenced scene details/annotations as event-owned context to bind distinct anchors such as `green tape` and `turned glove`? Compare plain BM25, frozen pretrained dense narrative recall, event-conditioned co-occurrence graph, trust/provenance guards, and storage-matched external retrieval. If the third cue literal appears in source narrative or metadata available at episode formation, it is NOT a genuinely unseen cue—even if absent from the explicit key store. Measure and label such cases separately.

**Independent human semantic paraphrases:** Commission a new truly blinded, human-reviewed meaning-preserving paraphrase + false-memory/distractor panel based on a frozen source subset, with separate human validation of semantic equivalence and provenance before evaluating and NEVER using that panel for training, memory key storage, or threshold tuning. This is currently NOT available; cannot claim tested or generated independent human panel. Keep separate from episodic anchor associations.

No definitive Pretorius production cognition, conscious fly memory, self-authored autobiographical text or safe absence/rejection is established by these experiments. The negative results and cue source provenance correction are therefore the primary publication-quality deliverables of this pilot.


## Pilot18 permanent raw source and learned-state closure (October 10, 2026)

[Postmerge exact original source run 38058815535](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38058815535) SUCCESS, and [automatic fail-closed full-source/learned-state archive 38058864875](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38058864875) SUCCESS. The original **1,211,379-byte full per-case JSON** SHA256 `9ac8dc764718ae09d1d3ec1b7d2d8298a3ca0cf62163e4213db6e9579de8fe75` now exists permanently in [Connectome main results/imprinting/runs](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/runs/pilot18-two-view-source-run38058815535.json), together with [the measured original source report](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT18_SOURCE_MIRROR_KEYS_RESULTS.md) and all **SIX** actually learned original two-view metric projection and numeric episode key/value NPZ states in artifacts/imprinting/checkpoints, confirmed by independent main-tree listing. [Source experiment PR #34](https://github.com/Azimn/Pretorius-Connectome/pull/34) and [journal PR #16](https://github.com/Azimn/Artificial-Life-Research-Journal/pull/16) are MERGED.

The permanent results preserve the negative source metric finding **without retuning**: train-only paired discriminant **0/316** genuine distinct original third-annotated source cue recoveries, random source projection **0/316**, and all six arms **0/316 correct AND accepted** after the validation-only not-known gate. Wrong source CONTENT target control accidentally matched 3/316. This is **a within-original-corpus anchor-cue binding test**, not a new validated human-written paraphrase test. The reproducible post-hoc source-cue sidecar audit separately shows 450 `unreviewed_candidate` annotation statuses and mainly distinct short event-detail anchors. Future work must not relabel these as verified semantic paraphrases.
