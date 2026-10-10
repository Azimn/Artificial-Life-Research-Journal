---
id: JOURNAL-2026-10-10-NOETIC-LAB-SHADOW
date: 2026-10-10
title: Pretorius Laboratory becomes Noetic's persistent continuity host
type: research-journal
status: executed-scripted-cross-repository-integration-review-pending
projects:
  - Pretorius-Laboratory
  - The-Noetic-Engine
  - The Doctor Lives
research_questions:
  - RQ-001
---

# LAB-SHADOW-001: reuse the permanent laboratory, preserve subject/world separation

Existing [Pretorius Laboratory](https://github.com/Azimn/Pretorius-Laboratory) provides the world authority we need: persistent physical objects, book editions and pages, bookmarks, source-scoped room/object/shelf views, observation-offer receipts, event replay, controlled sandbox world epochs and backups. Its authored world is stronger as an ecologically meaningful **identity-continuity research habitat** than generic puzzle games; it is not an independent external benchmark publisher.

We deliberately reused the **exact standalone laboratory donor commit** `93d19671f7666b2996e6fcad211c5e6509336466`, without copying physics, book or object state into Noetic. [Noetic LAB-SHADOW-001 PR #22](https://github.com/Azimn/The-Noetic-Engine/pull/22) is stacked behind independent Noetic architecture reviews. The integration bridge uses an isolated local world fork plus a separate Noetic subject ID; definitive Pretorius in The Doctor Lives and the laboratory's canonical physical parent remain unchanged.

[First verified CI run](https://github.com/Azimn/The-Noetic-Engine/actions/runs/38069694129) passed **85 tests** including the actual cross-repository scenario. The source-backed scenario broke a beaker, collected fragments, placed the broken beaker in the northwest floor corner, opened a synthetic installed book, read its first page, bookmarked the second *without reading it*, then restarted both persistent world and cognitive ledgers. World physical state and bookmark survived. The shadow Noetic ledger could retrieve prior *offered and explicitly consumed* observations from memory without reinspection; the unoffered second page did not enter cognitive memory. On a later explicit read, page two was admitted from a verifiable installed edition. The parent world remained untouched; laboratory replay, backup and cognitive-ledger checks passed. The book-source admission was further hardened to verify an actual immutable book-event hash instead of trusting only a caller-chosen delivery ID.

[Complete protocol, source access limits and next study](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-pretorius-laboratory-shadow/experiments/PROTOCOL_LAB_SHADOW_001.md); [original archived result](https://github.com/Azimn/The-Noetic-Engine/blob/exp/noetic-pretorius-laboratory-shadow/results/lab_shadow/first_executed.json).

**What this does NOT establish:** no autonomous action planning, semantic autobiographical recall, first-person awareness, psychological character continuity, human-judged identity, renderer/model swap, or world synchronization with Frankenstein Village. Receipt offered to an interface is not proof of perception. The experimental action sequence was scripted, and Noetic retrieval is lexical rather than an independently judged answer. The first synthetic book is not Pretorius canon. Laboratory millimetre coordinates, private notebook material and unread book pages were excluded from subject access.

**Relevant negative context:** external TextWorldExpress [MATRIX-005](https://github.com/Azimn/The-Noetic-Engine/pull/19) found identical Noetic/full, no-recurrent and simple signed-learner world command sequences in all eight tested games. Using a more personally relevant laboratory does not erase this negative or constitute evidence of better general task ability. This next study must *compare* Noetic with strong non-neural temporal recall, graph retrieval and explicit source-ledger baselines; and it must score **actual consequential laboratory decisions**.

The next research gate is [LAB-CONTINUITY-002](https://github.com/Azimn/The-Noetic-Engine/issues/21): source-limited memory-guided autonomous object tasks, long interruptions, delayed commitments, second-actor unobserved modifications, calibrated uncertainty and reinspection, attempted false memories/foreign archives and genuine renderer swaps, using independent blind character judgments. E4 neural fresh decoder and Egregore semantic meaning/authority remain separately blocked. Production Pretorius and Village are unchanged.

This journal entry is a strictly additive proposed file; no daily research capture automation, existing studies or research registry is changed.
