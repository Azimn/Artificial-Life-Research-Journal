# 2026-10-10 — Pretorius's Portable Laboratory: proposed permanent home across offline research and Frankenstein Village

**Type:** architecture proposal/backlog, NOT a completed experiment or deployed game feature.

The isolated laboratory introduced in The Doctor Lives Stage 04 is a promising **permanent research habitat** for Pretorius: a persistent world with real apparatus-state changes, signed witnessed outcomes and a source-preserving bridge to his lived memories. The user suggested preserving it beyond the test harness, eventually giving it a permanent residence in Frankenstein Village or having it exist as **one synchronized logical environment visible offline and online**.

Recorded design notes:
- [The Doctor Lives research proposal PR #45](https://github.com/Azimn/The-Doctor-Lives/pull/45); [future-work issue #46](https://github.com/Azimn/The-Doctor-Lives/issues/46).
- [Frankenstein Village design proposal PR #47](https://github.com/Azimn/frankenstein-village/pull/47); [deferred integration issue #48](https://github.com/Azimn/frankenstein-village/issues/48).

Two alternatives are preserved. **A: handoff later**, transferring an audited research snapshot to an Evennia-owned playable lab once canon approves Pretorius's arrival. **B: single authoritative external lab**, with an offline experimental replica and online Evennia projection, using versioned events and source-custody checks. B is preferred in principle if continuous use from both environments is valuable, but not approved for implementation. Lab identity and reset epoch, schema/rules versions, content manifest, actual world revision, and village-applied event cursor must align. Offline events are **provisional proposals** until reconciled against current online world and consent; no silent last-writer-wins, duplicate items, private data leaks, invented memories or retroactive impacts on other players. The Village remains authoritative for masks, shared chronology, NPCs/players and public consequences. Pretorius's mind remains external to the server.

Crucial canon constraint: the [World Bible v0.2](https://github.com/Azimn/frankenstein-village/blob/main/files/frankenstein-village-world-bible-v0.2.md) states that Pretorius is **not present at launch**; the dark leased shop and OPENING SOON sign remain unchanged. The proposed future lab does not unlock the shop, spawn Pretorius, change invited-alpha scope, or choose hosting. This is not part of Stage 05's **objective negative PHASE world-action result** (2/12 versus 2/12 flat, oracle 12/12), which remains preserved and unmodified.

**Status:** documented and cross-referenced, no runtime/test/game canon changes. Next only by explicit prioritization: stable research-lab snapshots and recovery → portable event/version contract → offline conflict tests → Evennia shadow projection → canon-approved playable location → independent multi-actor soak.
