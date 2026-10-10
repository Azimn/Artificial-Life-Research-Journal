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

## Full Victorian-text collection and later shop threshold

The character-world content milestone is [Pretorius-Laboratory PR #6](https://github.com/Azimn/Pretorius-Laboratory/pull/6), delivering a seven-volume historically curated bookshelf, rather than a row of titles whose pages are fabricated by an LLM. The books include Calvin Cutter's 1858 *Treatise on Anatomy, Physiology, and Hygiene*, William James's two 1890 *Principles of Psychology* volumes, Nicholas Culpeper's *Complete Herbal*, Reginald Scot's *Discoverie of Witchcraft*, James Frazer's **original 1890 first-edition** *Golden Bough* Volume I, and Stevenson's 1886 *Jekyll and Hyde*. The editions' primary public-domain transcriptions are referenced with immutable Git commits, blob hashes, length checks and versioned metadata; any reconstructed leaf uses the actual full text, not a paraphrase. Digital reading segments are not proof of historical print pagination or inclusion of engraved illustrations. Culpeper and Scot transcription-to-imprint equivalence still needs a physical-edition check.

The special GitHub Actions suite [38086094739](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38086094739) independently downloaded and accepted **all seven complete files**, populated the real source-backed book domain in a fresh standalone synthetic spatial-v2 fixture and uploaded an auditable SQLite backup and catalog. The first ingestion proof installed 1111 deterministic digital leaves across the seven works (118+218+219+195+237+105+19); the exact raw content hashes are in the build's ingest-report JSON. The artifact expires under GitHub retention, while the reproducible pinned source recipe remains in the repository. Neither existing character history nor Village canon was changed.

The user also specified the intended diegetic connection: Pretorius travels to reconnect with **Henry** before the film's events and leases a closed, *OPENING SOON* curiosity shop. The future shopfront is the small public face of his much larger full persistent laboratory and private sanctuary, extending into the same building. Eventually Pretorius should be able to traverse in both directions between the detailed laboratory simulator and the less granular, narrative Frankenstein Village representation. This is a **future development note only**. The Village itself pins a broadly 1890s setting with exact civil year undecided, and the Henry/Victor naming conventions warrant canon review, not unilateral game edits. No portal, avatar handoff, live shop, two-way sync or authority transfer was implemented.

The next evidence gates are additional historically sourced/physically edition-correct volumes, artwork/printed pagination, durable real-world fixture hosting, embodied reach/read behavior and a verified subject-observation adapter. Do not promote the presence of full books in a synthetic laboratory database into a claim that Pretorius has acquired, read or remembered them.

Details: [Victorian Library and Future Shop Threshold](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/VICTORIAN_LIBRARY_AND_SHOP_THRESHOLD.md), [Source-pinned bookshelf manifest](https://github.com/Azimn/Pretorius-Laboratory/blob/main/corpus/victorian_bookshelf_v1.json).

## Additional ten-volume esoteric library and protected shelf annex

On October 10 the user requested more esoteric material for Pretorius's permanent, historically situated research library. [Pretorius Laboratory PR #7](https://github.com/Azimn/Pretorius-Laboratory/pull/7) merged into main at [c118999](https://github.com/Azimn/Pretorius-Laboratory/commit/c118999a0bd2afdefc1ae751e2f8982720278259). The source-pinned corpus now adds ten full-length texts: Blavatsky's Isis Unveiled (both volumes) and Key to Theosophy, Walter Scott's Letters on Demonology and Witchcraft, Catherine Crowe's Night Side of Nature and Ghosts and Family Legends, Bulwer-Lytton's Zanoni, A Strange Story, and The Coming Race, and Cotton Mather's The Wonders of the Invisible World. First work-publication years range 1693–1889, all no later than the pinned 1890 research scenario. Early writings in the source transcriptions may represent later editions or editorial material: this program has not authenticated the exact physical imprint, engravings or printed pagination of each work.

Crucially the spatial-v2 core manifest is unchanged. An additional source-linked and hash-replay-checked physical registration ledger attaches stable IDs book:008 through book:017 to the ten previously vacant anchors of shelf one. Original books 001–007 retain their accepted shelf-three locations, event history and stored text. The existing reading/bookmark ledger checks both the original and annex registries; new book identities persist across restarts, verified backups, and research sandbox forks, and cannot overlap original world objects. Subject-facing observations expose visible book identities and source-backed titles, not full unread text or privileged millimetre coordinates.

The new complete-source workflow [run 38092706632](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38092706632) succeeded, separately rebuilding a 17-work source-backed SQLite world from pinned GITenberg bytes, asserting the 10 new esoteric books and seven original books, replay-validating the inventory, and producing an artifact with book contents, source receipts, and a complete independently verified database backup. The original basic lab acceptance tests, including targeted shelf annex tests, were also green. The additional texts are stored as digital reading leaves, not original historical book page facsimiles. The artifact's retention is limited, but pinned sources and importer permit reconstruction.

Documented caveat: existing local trusted authoring, user-presented reading offers and observed physical evidence must remain distinct from what Pretorius has personally read, recalled or experienced. No agent was actually admitted into this fixture, no claim about the truth of supernatural phenomena was made, and neither The Doctor Lives cognition nor Frankenstein Village was changed. The 1890 research fixture is a conservative publication cutoff; the Village still has not settled its exact civil year. Do not retroactively introduce translated editions first published after that year merely because the original authors wrote earlier.

Sources: [Esoteric Annex design](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/ESOTERIC_ANNEX_FULLTEXT_2026-10-10.md), [immutable esoteric source catalog](https://github.com/Azimn/Pretorius-Laboratory/blob/main/corpus/esoteric_annex_1890.json).

## Physically constrained reading: a persistent actor location

The next engineering milestone was [Pretorius-Laboratory PR #8](https://github.com/Azimn/Pretorius-Laboratory/pull/8). It adds an opt-in persistent *actor-position ledger* and local research interface (EmbodiedAccess) without changing the original world event chain, historical book contents, or frozen v2 fixture digest. A single synthetic research subject begins at the sanctum threshold, can move only between graph-adjacent stations, can look only at the nearby fixture (room features at the threshold; shelf titles at the shelf), and cannot receive host-only precise millimetre geometry from the subject port.

The separate object and book registries remain the sole authorities for physical book location and page text. For subject-scoped operations, the BookLibrary checks the actor's world/epoch-bound station against **that book's current physical shelf inside the same SQLite write transaction** that accepts open, close, single-page turn, read and bookmark operations. The accepted source event records the source world revision, book/edition identity and a referenced body event hash. A book relocated by the operator can no longer be read from its former shelf through this interface. The body's event chain is replay-verified separately, and restart/backup preserve station and offered-look receipts. A sandbox fork inherits the current pose as source-derived initial condition, **not** its parent's observations as allegedly fresh experiences.

The 76-test laboratory acceptance suite was green on [GitHub Actions run 38093617022](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38093617022), including 12 new targeted actor tests: no doorway reading, adjacent movement, source-backed nearby shelf names, denied remote reads after an object relocation, full page turn/marker persistence, book annex equivalence, source tamper detection, idempotent actor events, body history replay, backup and sandbox fork isolation. A full 17-book esoteric corpus acceptance workflow also exercises a real archived esoteric reading offer after physical approach (and denial before approaching), with its own source-backed database artifact.

**No claim of Pretorius cognizing this scene** is licensed by these engineering tests: no production The Doctor Lives cognition adapter was invoked, no memory assimilation or autonomous book selection was measured, and no human-like continuous locomotion or reach physics has been implemented. The actor's actions are trusted local research events, not cryptographically authenticated player activity. The implementation models *categorical local access* only; it cannot yet pick up and carry a volume, open a physically bounded door, model hands/light/line-of-sight or measure dimensions with instruments. The world still exists independently of a model's response.

**Behavioral next gate:** in a future real subject session, assess prior beliefs about a persistent book before any fresh external look, permit position-grounded observation or source reading, then compare revised belief/recollection and later action against the world log. Use a withheld-memory control and a deliberate book-location perturbation to distinguish knowledge from current host observation. Keep this work distinct from a claim of consciousness, and never grant the renderer the engineer-only inspect/status interface.

Design and runbook: [Embodied Subject Access v0.1](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/EMBODIED_SUBJECT_ACCESS_2026-10-10.md).

## Explicit physical book custody and surface transfer

[Pretorius-Laboratory PR #9](https://github.com/Azimn/Pretorius-Laboratory/pull/9) implements the next mechanical permanence gate: a volume taken from a shelf must **cease occupying the shelf** and remain the same physical book while carried and later placed on a different surface. An additive, world-epoch-scoped BookCustody ledger contains hash-replay-checked typed take/put actions and source references to the existing physical world, append-only shelf annex and actor-position history. The original spatial-v2 frozen genesis and old event hashes are not rewritten.

The actor must be at the book's current physical location to take it, and physically at the destination to put it down. Only one book may be carried at a time. Every effective world observation resolves a **single book location** (surface OR actor's hands); the old shelf becomes visibly empty while the same source-backed book becomes carried. The existing BookLibrary content, edition checksum, page turns and physical bookmarks stay attached to its original book ID through transfer. Subject-scoped page actions can be accepted while the book is genuinely in the actor's hands or set down on a reachable surface; they are transactionally checked against the position and custody event cursor. A bench spot initially occupied by a beaker must be cleared before a book can be placed there.

GitHub's expanded laboratory acceptance suite reported **87 passing tests** in [Actions run 38094114904](https://github.com/Azimn/Pretorius-Laboratory/actions/runs/38094114904), including core/annex book transfer, invalid distant take/put, occupied-surface denial, source-page and bookmark continuity while held or on the bench, a restart, tamper detection, backup, and independent experiment fork while holding or after putting down. The dedicated complete 17-volume integration workflow also tests carrying real archived *Isis Unveiled* text to the bench and resuming the original paper bookmark after the move, with a separate verified SQLite backup (see the PR checks for this latest run).

The experiment establishes discrete **locational permanence under accepted manipulations**, not physically simulated fingers, rigid-body dynamics, anthropometric constraints, weight/volume, accurate geometry, collision across corridors, page damage or an independently running Pretorius. In particular, the original v2 fixture anchor remains reserved to old lower-level administrative placement reducers even when an effective custody view marks it empty: consistent state is enforced for subject-facing custody operations, but full normalization of all older physical reducers still requires a source-preserving migration/versioned contract. Direct engineer APIs remain privileged, with no remote authentication claims. No cognitive architecture was invented, no first-person memory assimilation was demonstrated, and the Frankenstein Village shop remains dark and disconnected.

Next physical milestone: unify accepted effective-object occupancy across all historical reducers while preserving replay; then add genuinely measurable object handling (dimensions, mass, reach and collision) and source-grounded measuring tools. Behavioral use will require an actual production cognition adapter to test prior expected object positions, surprise after externally moved objects, and subsequent autobiographical correction, with separate delivered-observation and accessed-memory provenance.

Engineering contract: [Physical Book Handling: Persistent Custody](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/BOOK_CUSTODY_AND_PERSISTENT_HANDLING_2026-10-10.md).

## Unified effective physical occupancy and historically stable placement

The laboratory continues consolidating working physical mechanics instead of inventing another cognitive organ. [Pretorius-Laboratory PR #10](https://github.com/Azimn/Pretorius-Laboratory/pull/10) extends the existing BookCustody source ledger to handle **trusted operator placements of existing physical objects**, including the beaker, and routes new spatial-v2 operator `place` calls and shelf-annex `move` calls through one **effective physical location** authority whenever custody is activated. Original spatial-v2 and annex events, including their genesis and hash chains, remain byte-for-byte untouched and replay by the original historical reducers.

The old problem was concrete: after the actor took a book, its shelf appeared empty in the subject's real world, but the old raw physical genesis still reserved the book's original anchor, so another object could not enter. The integrated world now permits a trusted operator to place the real beaker in that actually vacant old slot; it blocks putting the carried volume back until the beaker moves away. It rejects held-book operator relocation, double occupancy, stale optional `expected_placement_revision` expectations and moving uncollected broken glass. Actions are accepted atomically in the existing SQLite world DB, with custody-domain append-only hash receipts, and replicate through backup and sandbox forks without cloning allegedly lived experience.

The new focused tests verify old pre-custody v2 event replay, original and annex book locations, visually empty and reoccupied shelf slots, source text continuity, actor permission boundaries, idempotence, collision exclusion, stale revisions, beaker condition invariants and fork isolation. The full 17-book source-backed CI exercise additionally moves the original archival *Isis Unveiled* from its shelf to a workbench, verifies source reading and a bookmark there, and then moves the physical beaker into the volume's formerly reserved first-shelf position. See [Unified Effective Occupancy](https://github.com/Azimn/Pretorius-Laboratory/blob/main/docs/UNIFIED_EFFECTIVE_OCCUPANCY_2026-10-10.md) for contract and verified acceptance evidence; numerical passing test counts are specific to the relevant CI run.

This is **not a rewrite of old history**, nor a full generic object registry migration. **Registering genuinely new physical objects** can still face the old v2 anchor reservations; only operator/annex movement for **existing** objects is unified at this gate. Dimensions, mass, reach, grasp mechanics, object collision and instrument measurement remain unimplemented. There is no production Pretorius renderer, real model-attended memory or Village runtime link demonstrated by these tests. Continue to keep source-observation receipts separate from autobiographical memory.

The next engineering priority is a versioned physical-object affordance profile (size, mass, handling requirements and actual shelf clearance) followed by empirically checkable capacity and reach tests, not another new cognition framework.

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
