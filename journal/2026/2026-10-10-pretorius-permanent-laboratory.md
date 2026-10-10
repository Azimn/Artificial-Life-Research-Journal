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
