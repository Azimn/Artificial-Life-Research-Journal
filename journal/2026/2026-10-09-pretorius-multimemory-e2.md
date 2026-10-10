---
id: JRN-2026-10-09-03
title: "Pretorius E2: multi-memory evidence assembly and choice integration"
type: journal-entry
status: exploratory-complete-negative-and-prior-confounded
date: 2026-10-09
updated: 2026-10-09
research_questions:
  - RQ-001
  - RQ-006
tags:
  - memory-selection
  - autobiographical-provenance
  - multi-memory-decisions
  - lexical-retrieval
  - graph-retrieval
  - semantic-retrieval
  - abstention-calibration
---

# October 9: Pretorius E2, multiple memories and action selection

## Program question

E1 established deterministic, source-verified access to the 450-event fictional Pretorius L1 while showing that memory access alone did not guarantee policy enactment, and that source-authored cues provided no observable advantage over neutral indexed keys. E2 raises a different test: when a novel hypothetical decision plausibly requires two distinct autobiographical episodes, can a renderer make an evidence-sensitive decision, and can the memory subsystem assemble the *pair* from an ordinary natural-language query?

The [Attractomancy E2 protocol and full results](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E2_MULTIMEMORY_DECISIONS/RESULTS.md) consume the original frozen, checksum-validated L1 data at Pretorius-Connectome commit \`6d2768211f5c2184c8bbdb833c06e169b5137197\`. Six dilemmas were authored from twelve source events, with two distinct source records per question. Each was counterbalanced with A/B answer positions reversed. **Preferred behavioral answers were supplied by a single unblinded investigator and are not validated character ground truth.** These cases mostly favor cautious, considerate responses and therefore permit ordinary model moral priors to mimic an apparent source effect.

## The renderer test: E2

Each Qwen2.5 model completed 72 fresh independent prompts, using six evidence interventions: both verified original memories with editorial cues; both under neutral keys; first or second source alone; none; and a deliberately wrong subject blocked *before* source injection.

**Qwen2.5-0.5B:** Two-memory decisions matched the author's expected label in **3/12 cue** and **2/12 neutral** cases, with raw answers identical in 10/12 matched cue-versus-key prompts. The one-memory arms properly abstained in 10/12 and 9/12; no-memory and upstream-rejected wrong-owner arms abstained in 11/12 each. Several apparent failures were exact-format failures such as \`A:\` rather than \`A\`, kept under a strict, unchanged scorer.

**Qwen2.5-1.5B:** Every one of 72 outputs was \`UNKNOWN\`, even when both correct memories were supplied and the new hypothetical asked for a best-supported action. This yields **0/12** author-match scores in both full-evidence arms, identical cue/key output in 12/12, and 12/12 abstentions in every incomplete-evidence arm. That is a **degenerate over-abstention strategy**, not successful multi-memory judgment. Apparently stable decisions under reversed letter order are merely consistent UNKNOWN answers.

The E2 renderer findings neither isolate a symbolic-cue benefit nor establish that the models can use two archived memories to enact Pretorius's differentiated behavioral priorities. Equally, they do not prove lack of such capacity under a better prompt or larger renderer.

## The selection tests: E2R, E2G and E2S

All selection studies use **the same six natural dilemmas** and the source-owned 450-item archive, with exactly two investigator-picked gold IDs per card. These IDs were selected by reading the autobiography, and have not been independently judged against alternative relevant memory sets. Hence the retrieval scores are **exact pair recall**, not objective relevance/quality scores.

| Method | Both required events within top 10 | Individual target events within top 10 |
| --- | ---: | ---: |
| Original lexical TF-IDF | 0/6 | 2/12 |
| Original link-graph diffusion (3 updates, 75% lexical restart) | 1/6 | 3/12 |
| Shuffled authored event links (seeds 11, 19, 37) | 0/6 each | 2/12 each |
| Local pretrained MiniLM semantic cosine | 0/6 | 3/12 |
| Fixed lexical+dense reciprocal rank fusion, k=60 | 0/6 | 4/12 |
| Permuted embedding-to-event IDs, seeds 11 and 37 | 0/6 each | 1/12, 0/12 |

The association graph links are **source-authored fictional-narrative associations, not FlyWire biological synapses**. They improved a single dilemma, moving event \`E02-013\` from rank 21 to rank 10 while the other target \`E25-001\` remained rank 2. That single case does not demonstrate significant advantage or justify activating graph diffusion by default. MiniLM's 384-dimensional embeddings and rank fusion improved individual hits but did not recover a complete pair; the MiniLM model revision and all raw ranks/costs are archived in Attractomancy.

The source-side metadata records 912 authored directed links, of which 431 span distinct narrative episodes. This is not independent behavioral association evidence and should not be treated as a neural connectome.

**Reproducibility caution:** E2R/E2G and E2S produced the same aggregate lexical pair recall but different top-ten rank orderings despite matching canonical source-manifest and query-fixture hashes. A separate runtime/lexical-rank parity audit has been initiated. Do not pool within-query numerical rankings across these runs or posit a mechanism for the discrepancy before the audit is reviewed.

## Next intervention, prepared separately

The [E2F forced-decision protocol](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E2_MULTIMEMORY_DECISIONS/FORCED_PROTOCOL.md) removes the \`UNKNOWN\` option when the task is intentionally a forced two-alternative calibration. Its key comparison is source-complete versus no-memory versus an unrelated two-record baseline on the **same six counterbalanced dilemmas**. This directly tests whether a plausible answer follows from generic moral priors rather than retrieved autobiography. If no-memory performance is comparable, high full-memory scoring cannot be attributed to the sources.

### Completed E2F control results

Both Qwen model sizes completed all 60 forced-choice cases each, and [raw results](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E2_MULTIMEMORY_DECISIONS/RESULTS.md) are archived separately from the original E2 conservative-prompt records.

| Force A/B to evaluate the author's preferred answer | Qwen2.5-0.5B (of 12) | Qwen2.5-1.5B (of 12) |
| --- | ---: | ---: |
| Two correct archival records under editorial cues | 8 | 11 |
| Same records under neutral keys | 8 | 11 |
| First correct record only | 8 | 10 |
| Two unrelated canonical records | 8 | 11 |
| **No records at all** | **7** | **12** |

Both models gave **12/12 identical editorial-versus-neutral results**. The small model's relevant two-record condition did no better than its unrelated two-record arm. The larger model achieved the greatest author-label agreement with **no memories**. Thus these investigator-authored dilemmas are answerable from ordinary model priors and normative option phrasing; the study supplies no evidence that reading autobiographical records improves the decision. The larger model's 72/72 UNKNOWN behavior under the prior conservative E2 prompt therefore reflected a prompt-dependent abstention pattern, not an established inability to select A or B.

The full two-memory prompt cost approximately **705 tokens per case** compared with **179** without records. Higher information cost, unchanged source-specific choice accuracy, and editorial/neutral output equivalence reinforce the decision not to deploy symbolic-cue mediation or unconditional long dossier injection based on these pilots. This does not invalidate real source memory for queries requiring private facts, relational histories, or genuinely revised commitments.

### Completed baseline reproducibility audit

The initial observed E2R/E2G versus E2S lexical ranking discrepancy was checked in the [dedicated audit](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E2_MULTIMEMORY_DECISIONS/results/parity-run-38024737940/parity_audit.json). Source-manifest and query-fixture hashes matched across all runs. Within a five-stage fresh runtime audit, lexical score vectors were **identical before and after torch import, thread setting, MiniLM model load and full 450-document embedding forward pass**. This audit's rankings matched E2S and differed from E2R/E2G despite original rank stability within those other runs. Cross-run root cause remains unresolved; rank-level outputs have not been normalized or replaced. The aggregate source-pair recall finding is stable, but numerical reproducibility still needs stronger initialization and library-version controls.

### Future evidence gate

[E3 Tribunal of Memory](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/PROTOCOL.md) now specifies independent blinded evidence relevance, multiple acceptable source sets, source-sensitive rather than prosocial-default dilemmas, temporal revocation and missing-source controls, cross-model-family replication, and full token/cpu cost accounting. It is a future study design and **has not been run**.

## Architectural implications

Three separable operations are required: (1) trustworthy, scoped archival access, (2) discovery and grouping of contextually relevant autobiographical *sets*, and (3) evidence-sensitive action choice with calibrated eligibility. E1 and E2 demonstrate that passing the first does not establish either of the others. More tokens or a culturally meaningful cue are not a substitute for source relevance, provenance and legitimate relationship/action constraints.

Retain the canonical Pretorius L1, original FlyWire/BioCircuit caches and all existing memory content unmodified. E2 only reads the pinned archive and produces independent investigative artifacts. Promote no new claim of persona continuity, remembered lived experiences or biological/neural transfer to the Character Continuity Program evidence register. A credible next-generation benchmark should have independently blinded judgments of multiple *acceptable* source sets, adversarial records and contradictory facts, with specificity controls and larger independent model families.
