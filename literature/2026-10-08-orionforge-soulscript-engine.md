---
id: LIT-2026-ORIONFORGE-001
title: OrionForge SoulScript Engine, dual-store identity and life memory
type: literature
status: source-reviewed-code-loop-pending
updated: 2026-10-08
authors: ["DrTHunter (GitHub author; name not independently verified)"]
year: 2026
url: https://github.com/DrTHunter/SoulScript-Engine
tags: [prior-art, persona-continuity, memory, retrieval, adaptive-scheduling]
research_questions: [RQ-001, RQ-003, RQ-006]
---

# OrionForge SoulScript Engine: identity versus mutable life memory

## Citation and attribution chain

- Community post: https://www.reddit.com/r/ArtificialSentience/s/AF5Lwgw909
- Reddit handle reported in the 2026-10-08 Calibos review: `u/OrionForgeEcosystem`. The shortened Reddit URL was not directly resolved in the present source inspection, so the handle-to-post link remains attributed to that review, not independently verified by this entry.
- Code host and exact repository: https://github.com/DrTHunter/SoulScript-Engine
- GitHub owner: `DrTHunter` is a GitHub **user account**, not a GitHub organization, according to repository metadata.
- Repository self-attribution: "Dr. Trent Hunter" in the README. Personal/legal identity and any claimed doctoral credential have **not** been independently verified. Do not conflate self-attribution with verified authorship identity.
- Verified published main-branch tip at review: [f299a752579cefbd557c59cd00da0f9e73b30eb5](https://github.com/DrTHunter/SoulScript-Engine/commit/f299a752579cefbd557c59cd00da0f9e73b30eb5), dated 2026-09-30T15:53:38Z. Public repo metadata reports last push 2026-09-30T15:54:41Z.
- Author-controlled sources: [README](https://github.com/DrTHunter/SoulScript-Engine/blob/f299a752579cefbd557c59cd00da0f9e73b30eb5/README.md), [code tree](https://github.com/DrTHunter/SoulScript-Engine/tree/f299a752579cefbd557c59cd00da0f9e73b30eb5), and [last commit](https://github.com/DrTHunter/SoulScript-Engine/commit/f299a752579cefbd557c59cd00da0f9e73b30eb5).

## Claim or contribution

The README describes a stable, read-only identity FAISS index for personality/directives and a mutable life-memory FAISS index for recorded experience. A prompt assembly layer retrieves relevant identity and memory segments on each turn rather than making the model weights themselves the durable source of identity. The README also describes an **optional autonomy loop** with configurable ticks/steps/intervals.

The Reddit discussion, as characterized in the supplied Calibos review and prior discussion, separately proposes a richer endogenous cycle with sensing, prediction error/surprise, attention, energy budgeting, fatigue and reflection. **Do not treat that newer loop as a verified code release** merely because an older optional tick loop is documented in the README.

## Methods or implementation reviewed

The publicly documented implementation uses profiles, system prompts, soul-script chunks, always-on notes, FAISS retrieval, a mutable vault, and a model-call context assembler. The README specifies `sentence-transformers/all-mpnet-base-v2` embeddings (768 dimensions), a read-only identity store, and mutable memory writeback. The embedded UI example is an implementation, but this review did not execute, benchmark, or audit its full runtime and did not independently reproduce the newer Reddit loop.

## Findings and current verification status

**Verified published artifact:** A public repository, dual-store architectural documentation, configurable older autonomy feature, and exact September 30 head commit exist.

**Author claims not independently validated:** stable identity without drift, 25,000+ memory retrieval performance, longevity, continuous cognition effects, or superior coherence. The novel prediction-error/energy-regulated scheduling cycle is **code drop pending**, not an evaluated outcome. A future commit can change this status only after direct inspection of the released implementation, runnable configuration, and relevant test artifacts.

## Relevance to our program

Three described systems appear to distinguish a protected identity substrate from writable experiential state: SoulScript's immutable identity index/mutable life index; a reported SoulCore "Tier 0" separation, whose primary source remains to be pinned; and [Calibos's cartridge versus experience records](https://github.com/Azimn/calibos-mind/blob/18497706f9ada6840c1e3bc40bf121941f9332e7/README.md). The [2024 Core Memories/SoulFile lineage](../projects/PRJ-023-Persona-Engine.md) may provide older related antecedents, subject to link validation.

This is **convergent engineering design**, not three independent experimental replications. The systems share broad conceptual antecedents, may have been exposed to similar ideas, and do not yet supply matched causal tests showing that the division is necessary or sufficient. It is nevertheless a concrete, plausible architecture hypothesis worth ablating.

The surprise scheduler suggests a test of whether prediction-error-triggered sampling improves decisions beyond equal-budget fixed and *random* schedules. Energy budgets suggest a separate test of allocation: uniform slowing versus urgency-sensitive redistribution, anchored to the program's [EXP-2026-010 PEMA scarcity allocator](../EXPERIMENT_LEDGER.md). That earlier record reports threat-processing share near 41% under scarcity versus 26% in abundance; it is evidence for PEMA, **not** SoulScript.

## What should not be inferred

A persona prompt's vivid affect language is not proof of subjective feeling or sentience. A scalar energy meter is not itself functional urgency prioritization. A surprise-responsive loop is not causally necessary merely because it produces interesting narratives. A README or promotional benchmark is not an independently replicated scientific result. Identity-store read-only semantics do not automatically establish stability under misleading memories, missing cue retrieval or model changes.

## Experiments influenced and release watch

See [EXP-2026-064 proposed scheduling and scarcity protocol](../programs/EXP-2026-064_SURPRISE_SCHEDULING_AND_SCARCITY_V0.md) and [dated synthesis note](../journal/2026/2026-10-08-soulscript-convergence.md). Monitor the upstream repository for substantive autonomous-cycle source code, tests, configuration, benchmark artifacts, and provenance. Compare new commits against the pinned September 30 baseline before updating this note. No code import into Calibos or Pretorius is authorized by this literature review.
