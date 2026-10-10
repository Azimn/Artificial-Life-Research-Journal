---
id: JRN-2026-10-10-03
title: "Pilot19 Reliquary: Source-Owned Episodic Detail Association and Index Exposure"
type: research-journal
status: original fictional Pretorius source experiment passed, original full archive pending
updated: 2026-10-10
projects:
  - PRJ-038
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
---

# Pilot19: detail → source event → associated detail (not semantic paraphrase)

## New question, source-provenance precondition

[Pilot18 Mirror Keys](2026-10-10-mirror-keys-cue-source-audit.md) revealed that all **450 source-cue sidecars are `unreviewed_candidate`** and most cues are short, different associated object details, e.g. `turned glove`, `millstream map`, `green tape`. The initial semantic alignment experiment recovered **0/316** third source cues without their event association. An embedding is not expected to infer that a glove and green tape occurred together solely from English phrase similarity. We therefore distinguish an event-owned **source relation** from a meaning-preserving paraphrase relation.

Relevant external methodological leads: [EventRAG, ACL 2025](https://aclanthology.org/2025.acl-long.830/) uses event-centered structures for narrative retrieval; [SEEM, ACL 2026](https://aclanthology.org/2026.acl-long.277/) explicitly anchors episodic event frames in provenance; [RippleMem, arXiv 2608.13334](https://arxiv.org/abs/2608.13334) studies cue-rich associative recollection; [EpBench, ICLR 2025](https://github.com/ahstat/episodic-memory-benchmark) compares event-level temporal, locational and participant cues; and [MAGIC, EMNLP 2025](https://aclanthology.org/2025.findings-emnlp.466/) examines conflicting and wrong source context. These are research design precedents, not evidence that our code replicates the published systems or their benchmark gains.

## Registered experiment

[Owner source PR #35](https://github.com/Azimn/Pretorius-Connectome/pull/35), [predeclared protocol](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/pilot19-reliquary-evidence-bound-episodes/docs/PILOT19_RELIQUARY_PROTOCOL.md), [implemented source model](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/pilot19-reliquary-evidence-bound-episodes/src/pretorius_connectome/reliquary19.py), and [complete measured report](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/pilot19-reliquary-evidence-bound-episodes/results/imprinting/PILOT19_ORIGINAL_SOURCE_PROVISIONAL.md).

Same original 450 fictional Pretorius reconstructed source events/27 episodes, original 317 train plus episode-isolated 62 validation absences and 71 test absences, original 159 familiar first cue, original 316 distinct third selected literal details, 31 old fourth cues, exact original source bytes and sidecar bytes SHA. Only original **317 train events** were indexed. Original absent event text, participants, locations or sidecars never enter the retrieval database. Every candidate source detail maintains `unreviewed_candidate` status; nothing auto-upgrades to verified first-person observation. This is an explicit **EXTERNAL event-ID retrieval and evidence graph**, not actual FlyWire neuron/brain computation, a cue-only neural weight store or a subject-access implementation.

Six controls:
- Original FIRST+MIDDLE candidate details only, no third cue and **no story even as hidden metadata**, so the third literal is genuinely not indexed.
- Original source narrative BM25, no sidecars anywhere in stored model.
- ALL unreviewed original sidecar details flat BM25.
- ALL sidecar details exact inverted index (with ambiguous owners abstaining).
- All the SAME sidecar details in explicit event graph detail→event→other candidate / participants / location, compared directly with exact-index results.
- ALL original sidecar cues with deterministic deliberate WRONG event ownership, preserving original true owner in emitted provenance.

The offline source truth evaluator alone uses the complete original corpus to label a query as present in its original sidecar, narrative, or ACTUAL particular arm's index. The full original source test strings and original 71 absent events may not set any model choice or threshold; only 62 validation episode absences calibrate native answer acceptance.

## Actual measured original source test

[Successful original source CI 38061091828](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38061091828) returned **4,670,137-byte original full per-case JSON SHA-256 `5f54f78625785ed3094694f40d8455cbb6cc3ff2ef24ad20f4848e385b827bc8`**, six original deterministic source-index SHA and every exact associated detail/query/evidence path. The strict no-test-cue-in-model-state fix was tested and passed, while the original case result remained byte-identical to pre-fix source run. No “learned synaptic checkpoint” was invented for deterministic indexes.

| Source-index availability and method | Correct event from original third detail /316 | Correct AND accepted /316 | Third literal ALREADY exposed inside that arm's own index | False accepted among 71 distinct absent episodes |
|---|---:|---:|---:|---:|
| FIRST+MIDDLE candidate details, no last cue | **0** | **0** | **0/316** | 3 |
| Original prose narrative BM25, NO sidecars | 121 | 69 | **75/316** third phrases verbatim | 10 |
| Full original sidecar candidate BM25 | 281 | 254 | **316/316** | 8 |
| Full sidecar candidate exact lookup | **287** | **287** | **316/316** | **6** |
| **Reliquary event graph**, exactly same original sidecars | **287** | **287** | **316/316** | **6** |
| Wrong source-owner event graph | **0** | 0 | 0/316 under rightful event ownership | 6 |

Of 316 already-indexed third candidate cue phrases in the exact and event-graph arms, **287 have a unique correct owner**; the other **29 are shared/ambiguous candidate details**, for which the system abstained rather than invent an original source event. Crucially, **the graph and simple exact index are IDENTICAL in accuracy**. The correct interpretation is that *source-bound indexing of distinct associated details* works. It is NOT evidence for complex graph reasoning, generalization to unseen wording, original fly brain memory, or validated source truth. The graph additionally preserves an auditable path to another detail and the original source's participants/location, which could be useful in a later multi-hop task—those capabilities were not shown to improve this one-hop identification task.

Wrong-owner graph makes **zero** correct original event identifications despite the original candidate detail strings being indexed, which supports the necessity of correct source ownership. Original narrative BM25 recovered 121/316 source IDs even though only 75 exact full third phrases appeared in the source prose; partial overlapping words can account for extra matches, so do not interpret it as semantic paraphrase competence without additional controls. Separately, the graph still falsely accepted 6/71 absent episode cue strings after validation-only calibration; source labeling is not sufficient for a truth/absence guard.

## Research decision and transfer guard

**Retain** provenance-bound event association as a candidate module for external historical recordkeeping: cue observation/annotation → event → other source detail. Require an explicit `unreviewed_candidate` versus independently supported field and a distinct subject-owned boundary before any cue becomes Pretorius's first-person memory.

**Do not infer** that an event graph beats BM25 when only the same cue has been supplied, or that direct all-sidecar lookup is a novel-cue competence result. A flat exact index already matches 287/316. Original source truth is a fictional reconstructive narrative, not empirically authenticated biography. An observed source detail may or may not occur literally in the narrative; absence of exact phrase is not proof detail is false.

**Separate future experiments**: (a) source-only *multi-cue ambiguity resolution* by combining participant/location/time with candidate detail, explicit wrong-owner controls and validation-only absence threshold; (b) blind independent human-written paraphrase/false-memory panel, to test meaning transfer where the paraphrase was truly unseen and not already stored as an anchor. Do not reuse old 316 third /31 fourth cue sets as independent paraphrases.

Original raw evidence is in successful source artifact; permanent Git main case archive must be verified separately before changing this journal status. Source research Issue #17 and cumulative scorecard updated/queued with exact evidence and source availability labels.
