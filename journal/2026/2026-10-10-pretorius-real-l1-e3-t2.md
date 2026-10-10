---
id: JRN-2026-10-10-02
title: "E3-T2: Source-owned belief and relationship fields versus narrative interpretation"
type: journal-entry
status: real-l1-copy-inference-running-narrative-review-unlabeled
date: 2026-10-10
updated: 2026-10-10
research_questions:
  - RQ-001
  - RQ-006
tags:
  - real-autobiographical-archive
  - source-provenance
  - explicit-belief-changes
  - relationship-history
  - model-data-extraction
  - blinded-review-pending
---

# October 10: L1 source metadata and narrative semantics

The earlier [E3-T1 Clerk study](2026-10-10-pretorius-tribunal-clerk.md) demonstrated an important renderer-specific result on *synthetic* two-bit source records: Qwen2.5-0.5B and SmolLM2-1.7B extracted more accurate cached source facts from isolated records, while Qwen2.5-1.5B was stronger when two records appeared together. The software calculator, not the model, computed final authorization. Because such synthetic record fields are exceptionally simple, the next question is whether that same interface can even copy two realistic *existing source-owned belief and relationship fields* from the canonical Pretorius reconstruction.

## Real-source E3-T2 protocol

The [preregistered E3-T2 study](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/L1_FIELD_PROTOCOL.md) reads only the existing [Pretorius-Connectome 450-record L1](https://github.com/Azimn/Pretorius-Connectome) at pinned source commit \`6d2768211f5c2184c8bbdb833c06e169b5137197\` and verifies the original L1 manifest. It selects twelve event IDs from twelve distinct narrative episodes using an explicit deterministic seed. For each original event, the source already has two author-written structured string fields: \`belief_changes\` and \`relationship_changes\`. Those give 24 **machine-checkable source metadata copying** targets.

Each target is tested under three presentations: only the selected field, full original episode record with both source-authored change fields, and a narrative/other-field condition that withholds the requested explicit field. There are 72 independent source-field extraction prompts per model, scored for strict JSON, exact text reproduction, confusion between belief and relationship text, and justified null abstention when the field label is absent. Correct field values originate from the original archived source structure; the researcher does not add interpretive gold answers to the model prompt.

**Limitation:** These metadata are already explicit source fields. Ordinary software access can retrieve them *exactly by construction* without an LLM. Any copying metric measures model input-processing loss and source-label discipline, not autonomous semantic memory or greater character consistency. The narrative may support or contradict an author-written field, but exact text matching cannot determine that.

## Distinct review task and uncollected evidence

A separate [actual-L1 narrative assessment packet](https://github.com/Azimn/Attractomancy/tree/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/packets/l1-semantic-calibration) has passed GitHub CI. It contains **24 reviewer narrative tasks and 72 candidate interpretations**, mixing the event's original sidecar statement with within-episode and remote-event comparator statements. Candidate source origins and event IDs are hidden in the reviewer-facing document. The public archive remains reconstructible, so this is procedural masking, not cryptographically guaranteed blinding.

The three required independent reviewers have not supplied any judgments. The packet must not be reported as a validated relevance benchmark. Candidate statements from another event could genuinely fit the excerpt, so none is automatically "false," and the original author sidecar is not automatically "true." Reviewers will need to supply labels, confidence, direct textual support or contradiction quotes, and disagreements. This source-semantic calibration also does not satisfy the main E3 requirement for at least 36 newly authored natural dilemmas, independently validated multi-record sufficiency, temporal updates, and source-dependent actions.

## Production boundary and reporting status

No original autobiographical record, FlyWire/BioCircuit cache, state ledger, or production cognition was modified. The experimental pipeline reads the pinned source in GitHub Actions and stores any model generations in the Attractomancy repository only. At this note's creation, the 0.5B and 1.5B Qwen inference jobs were running; **no scores from those jobs are asserted here until raw outputs are committed and checked**.

The important engineering choice is between **direct trusted structured source access** (preferable whenever the needed field already exists), **model extraction from nonstandard unstructured source narrative**, and **reasoned integration of competing source records**. Only the latter two require new cognition experiments, and neither is proven by exact copying of preexisting labels.
