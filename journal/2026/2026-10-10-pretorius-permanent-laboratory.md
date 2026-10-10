---
id: JRN-2026-10-10-03
title: "Pretorius Laboratory: persistent external habitat, replay and offline conflict rehearsal"
type: journal-entry
status: engineering-acceptance-local-only
date: 2026-10-10
updated: 2026-10-10
projects:
  - PRJ-040
research_questions:
  - RQ-001
tags:
  - permanent-world-state
  - persistent-laboratory
  - event-sourcing
  - deterministic-replay
  - offline-reconciliation
  - provenance
---

# Permanent Pretorius Laboratory: implementation and boundaries

## What happened

The user selected a new independent repository, [Pretorius-Laboratory](https://github.com/Azimn/Pretorius-Laboratory), to hold the enduring research habitat rather than repeatedly rebuilding isolated experiment rooms. The repo initially contained only its README. The proposal was already documented in The Doctor Lives PR #45/issue #46 and Frankenstein Village PR #47/issue #48.

On October 10, the first executable laboratory [PR #1](https://github.com/Azimn/Pretorius-Laboratory/pull/1) was squash-merged into main at commit [439347c](https://github.com/Azimn/Pretorius-Laboratory/commit/439347c29bac5fe67e0e5ab76e06c8827b731da9). Runtime dependencies are confined to Python's standard library and SQLite.

## Implemented research apparatus

A persistent physical scene with stable identifiers contains a laboratory room, bench, specimen vessel, specimen, clock and notebook. Typed deterministic verbs enforce container opening/closing, movable-object containment, clock ticks and private notebook records. The clock is research-simulation time, not Village fictional time or UTC.

SQLite transactionally records laboratory changes with unique event IDs, object revision preconditions, source actor labels, base/committed revision, world epoch, schema/rules/content versions, before/after SHA-256 state digests and a chained hash cursor. Verified snapshots and SQLite-native backup/restore allow checkpoints and recovery to a fresh destination. The verifier reconstructs state from initial manifest and accepted actions, with full revision, digest and cursor checks.

A separate offline JSON branch preserves provisional local actions. Reconciliation revalidates actual latest object revisions and action physics, preserving explicit conflicts without last-write-wins. Same event ID can be retried after a lost acknowledgement without duplicating an accepted laboratory mutation. An epoch or version mismatch is quarantined. Overlapping operations against the same object within one offline queue are deliberately unsupported until causal dependency management exists.

## Grounded perception interface (same-day follow-up)

The separate [Pretorius Laboratory PR #2](https://github.com/Azimn/Pretorius-Laboratory/pull/2) was also squash-merged at [405e380](https://github.com/Azimn/Pretorius-Laboratory/commit/405e3802701cc2eb688b4f3d6731e741d46c6cd4). It adds a deterministic research-side observation port, callable from Python or the CLI, that verifies the host ledger before exposing scene objects, event cursor, world epoch, and host-eligible action candidates. Closed containers occlude their contents; private notebook contents are excluded from the view. The new observation tests, including corruption refusal and restart-stable views, passed in [Actions run 38051070419](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38051070419).

An observation response is **not** proof that Pretorius, or any cognitive model, was running or experienced the observation. It is an external environment interface awaiting an explicitly developed, provenance-preserving adapter for the subject.

## MMO comparative architecture follow-up (2026-10-10)

A separate [source-grounded comparative study](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/MMO_PERSISTENT_HABITAT_STUDY_2026-10-10.md) was merged in Pretorius-Laboratory [PR #3](https://github.com/Azimn/Pretorius-Laboratory/pull/3) at `a08a4b4`. It compares official World of Warcraft housing and sharding descriptions, the community Ryzom Core EGS/AIS/backup/mirror architecture, TrinityCore's stable spawn/instance persistence, and Evennia's database objects and time-based Scripts. It explicitly distinguishes public Blizzard product descriptions from inaccessible proprietary internals, and TrinityCore from actual Blizzard software.

**Architectural decision, not efficacy result:** preserve a permanent personalized residential **Sanctum** distinct from cloneable/resettable **Experimental Chambers**. Use source-attested laboratory history and typed semantic IDs as the interoperability boundary; allow independently implemented Evennia object views without shared storage. Explore idle/hibernation and bounded deterministic experiment catch-up rather than a permanent model/tick loop. The habitat's continued existence does not imply continued subject cognition.

**Important negative systems lesson:** current Ryzom Core documentation says its historical PDS delta-logging system became disconnected although snapshot-style character/guild saving continued through PDR/Backup Service. This reinforces our requirement to test historical event integrity separately from durable current state, particularly for claims about lived experiences. No new runtime scheduler, sanctuary partitions, Village bridge, cognition adapter or behavioral advantage was implemented by the research-only PR.

## Exact spatial permanence, identity and external-world anchoring

The user clarified the laboratory's scientific role as a strictly persistent **external reality** for character-continuity experiments, distinct from the more narrative and interpretive physical descriptions permitted in Frankenstein Village. A shattered beaker must remain shattered in the same corner after a restart; the seventh book on shelf three must retain a precise address, independently of what Pretorius's next renderer says or remembers.

[Spatial Habitat v2 PR #4](https://github.com/Azimn/Pretorius-Laboratory/pull/4) was merged into Pretorius-Laboratory at [f23656a](https://github.com/Azimn/Pretorius-Laboratory/commit/f23656a08bfeb1b337dcd26e95a205b59a19553c). It adds an **opt-in, isolated** versioned SQLite authority with named stable shelf anchors, explicit ordinals, millimetre coordinates, durable object identities, condition transitions for a beaker and grouped shards, transactional event history, replay verification, duplicate rejection, backups and sandbox forks with new world epochs. The older v0.1 host is unchanged because modifying its baked manifest would invalidate existing event histories. A real migration has **not** been performed and the new v2 initialized world is an explicitly synthetic fixture, not an already-lived Pretorius home.

Twelve dedicated continuity and integrity unit tests plus the existing laboratory suite and v2 CLI exercise passed in [Actions run 38059207447](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38059207447). Acceptance covers a book on third shelf/seventh position, a broken beaker gathered and placed in the northwest corner that remains there on reopening, occupancy exclusion, stale revision rejection, event deduplication, fork isolation, snapshots, backups, and divergence detection under record tampering. The simulation currently has **discrete spatial anchors**, not a full rigid-body physics, geometry or actor locomotion model.

The [new continuity contract](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/SPATIAL_HABITAT_V2_AND_CONTINUITY_CONTRACT.md) registers an experimental separation of internal autobiographical memory from externally verifiable world state: assess prior recall *before* the subject sees the room, then assess grounded observation and correction *after* access, including cases in which someone else changed the world during absence. This frames world permanence as a potential mechanism of expectation calibration and epistemic correction, not proof that stable selfhood or consciousness has been implemented. Model-versus-world factorial trials and any Pretorius agent habitation remain unexecuted.

## Epistemic access, actual pages and durable observation delivery

The October 10 continuation clarifies that the laboratory is intended to be a **realistic persistent external world**, not an omniscient vector database given to the renderer. Its simulation may retain millimetre-accurate anchors, while Pretorius must not receive those numeric values without a future source-grounded measuring act. He may observe qualitative shelf order and condition; beliefs and memories must remain distinct from the independent physical host.

[Pretorius-Laboratory PR #5](https://github.com/Azimn/Pretorius-Laboratory/pull/5) merged as [93d1967](https://github.com/Azimn/Pretorius-Laboratory/commit/93d19671f7666b2996e6fcad211c5e6509336466). It changes the subject-facing locate, scan and observe methods to exclude exact coordinate metadata, retaining inspect_object / inspect-geometry explicitly for engineers only. No source model has yet been given an authorized measuring instrument, actor position or line-of-sight simulation.

A same-world-epoch SQLite **book ledger** can install full source-backed ordered page content for existing physical books with immutable edition identity, declared rights/source label and content digest; open, close, single-page turn, reading offer, physical bookmark insertion/removal and reopen-at-bookmark are tracked as separately replayable events. The demonstration edition has three original synthetic pages, not a historical Pretorius source. Other physical books are not magically readable before their pages are installed. This is a bounded reading interface, not a complete material/locomotion simulation.

A distinct **observation receipt ledger** records which room, shelf or object fact payload the interface offered at which accepted physical event cursor, with a stable deduplicated receipt ID and content checksum. These records prove local delivery, **not attention, comprehension, recollection, subjectivity or demonstrated cognitive exposure**. Library installation, page requests and offered observations have distinct provenance. Books and bookmarks survive restart/backup and clone into separate experiment epochs; a cloned laboratory does not inherit its parent's observation receipts as new experiences.

The complete earlier physical event history remains untouched: the two additive domain ledgers are separate, epoch-scoped tables inside the original spatial v2 database. [CI run 38061195218](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38061195218) passed compilation, new and historical unit tests, book/marker workflow, recovery/fork and observation-receipt smoke drills.

The scientific next step is to instrument actual Pretorius subject sessions so a subject-owned cognition process can be shown only admitted perceptions, distinguish prior recollection from novel external access and produce provenance-specific belief updates. It remains wrong to infer a coherent subjective life merely because an interface logs reading offers. Physics still lacks reach, hand manipulation, paper damage, measuring instruments, and actual book import/source validation beyond operator-declared provenance. The experimental opportunity is a falsifiable difference between **the world that exists**, **the information offered**, **the information actually consumed**, and **the character's later memory and decisions**. The journal preserves this as engineering evidence and a proposed cognitive experiment, not a demonstrated improvement.

Detailed constraints: [Knowledge boundary and persistent books](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/KNOWLEDGE_BOUNDARY_AND_PERSISTENT_BOOKS_2026-10-10.md).

## Verification and limitations

[GitHub Actions run 38050736698](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38050736698) completed successfully, including Python compilation, the unittest battery and CLI init, reopen/verify, checkpoint, backup and restore exercise. The battery covers history replay, container rules, bad action rejection, duplicate event protection, tamper detection, non-conflicting offline replay, same-object conflict, epoch isolation, lost acknowledgement and concurrent optimistic writes. This is **software engineering acceptance of the local host**, not evidence of improved character cognition, a long-duration life experiment, real two-host synchronization or independent operational recovery.

All events are research-private. Local actor names are trusted command-line labels, **not** cryptographic authentication. The hash chain is for consistency, not anti-tamper proof against a filesystem operator. Neither a source-signed Stage 04 importer, external consent service, remote adapter nor Evennia shadow projection exists. No existing production cognition, player or Village game code was changed. Pretorius's dark leased shop and OPENING SOON sign remain canonically unopened.

## Decision and scientific implication

One persistent external place can now survive a model or session boundary without depending on the renderer to remember scene facts. However, the laboratory's working persistence must **not** be interpreted as demonstrated first-person experience, longitudinal agency, the causal efficacy of memories, or proof that Pretorius has inhabited the environment. Offline episodes stay provisional until locally reconciled, and even accepted local laboratory events do not become witnessed Village history.

## Next work

The next integration gate is to inspect the actual versioned Stage 04 world-host implementation, verify equivalence of clock/object/event semantics and build an explicit, provenance-preserving importer. Later work needs identity and key rotation, permission and consent checks, signed receipts, source revocation, history cursor mirroring, a nonpublic Evennia read-only projection and independent recovery/soak tests. Village entry, shop opening and story presence require a separate keeper decision.

## Provenance

Primary code and architecture: [Pretorius Laboratory main](https://github.com/Azimn/Pretorius-Laboratory/tree/main), [permanent lab technical contract](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/ARCHITECTURE.md).

Source host tracking: [The Doctor Lives issue #46](https://github.com/Azimn/The-Doctor-Lives/issues/46). Game authority constraints: [Frankenstein Village issue #48](https://github.com/Azimn/frankenstein-village/issues/48).

This entry deliberately records no new experimental efficacy claim or EXP number.
