---
id: JRN-2026-10-10-03
title: "Pretorius E3: from real-L1 metadata copying to temporal relationship reconciliation"
type: journal-entry
status: exploratory-source-derived-review-packets-and-software-controls-complete
date: 2026-10-10
updated: 2026-10-10
research_questions:
  - RQ-001
  - RQ-006
tags:
  - autobiographical-memory
  - source-provenance
  - relationship-history
  - temporal-commitments
  - renderer-format-ablation
  - reviewer-annotation-pending
---

# October 10: Real Pretorius L1 and the Book of Debts

## Why move past exact metadata copying?

E3-T1 Clerk identified renderer-dependent source-extraction accuracy on synthetic rule-bearing records, with a strictly source-attested software calculator. A next [E3-T2 study](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/L1_FIELD_PROTOCOL.md) accessed the genuine 450-item source-owned *reconstructed* Pretorius L1, pinned to original source commit \`6d2768211f5c2184c8bbdb833c06e169b5137197\`. Twelve records from twelve distinct episodes were selected by fixed seed, each with original \`belief_changes\` and \`relationship_changes\` fields. The actual archived labels are machine-readable; software can retrieve them perfectly without any language model.

Two Qwen sizes each completed 72 prompts under two versions of a JSON source copying protocol (288 original responses). The first v1 included a contaminating example \`{"answer":"source text"}\`; Qwen0.5B echoed it in 70/72 cases. The v2 removed that example, but strict JSON failed frequently due to field-name substitution, Markdown fencing, or string \`"null"\` instead of the JSON value. The full [source/format report](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/L1_FORMAT_ABLATION_RESULTS.md) keeps the unmodified strict metrics.

Under strict scoring, Qwen1.5B v1 copied 22/24 isolated requested fields and 13/24 full-event requested fields, while failing all 24 missing-field null responses. The v2 strict metric collapsed to 0/24 isolated, 6/24 full event and 0/24 absent. **Post hoc text-content inspection, not a primary score**, showed that v2 still included the correct literal field text in 24/24 isolated and 23/24 full-event cases for 1.5B, while 0.5B included 19/24 and 16/24. Those mismatches locate serialization/abstention failure, not a novel cognitive advantage.

The [software-only original L1 witness](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/results/l1-witnesses-38058594338/summary.json) achieved 24/24 exact original source value access, as expected by construction. Its provenance checks and source digest guard are not independently authenticated autobiographical truth. A third plain-text output experiment, [E3-T2P3](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/L1_PLAINTEXT_PROTOCOL.md), was then frozen after v2 inspection to ask for a one-line value or FIELD_ABSENT instead of JSON. Its conditions use the same 12 source events and are a **prompt-format ablation, not independent confirmation**.

### Verified plain-text continuation

The first two [T2P3 original run archives](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/L1_FORMAT_ABLATION_RESULTS.md) were committed after the example-contaminated v1 and differently formatted v2 runs. Under exact one-line copying Qwen2.5-0.5B scored **12/24** from a visible isolated field, **2/24** from an original full event, and **0/24** correct FIELD_ABSENT responses when the requested field was omitted. Qwen2.5-1.5B scored **20/24**, **18/24**, and **0/24**, respectively. Both models therefore remained vulnerable to unsupported inferences when an explicit source-owned metadata field was missing. The v3 prompt was selected after inspecting earlier failures; it is exploratory, not independent replication. The independent SmolLM2 model run was still in progress when this note was updated.

The simplest and source-faithful solution when an original structured field is already available is the direct source-owned witness, which copied all 24 original fields exactly by software, without generating fictionalized intermediary text. A generative model's speculative reconstruction of an absent field should be kept as an explicitly tentative interpretation, not promoted into the source archive.

## More realistic next question: does later history modify a relationship?

A source archive can preserve a relationship-change string without understanding whether it is supported by an event, whether it persists after contradictory events, or whether a new event explicitly revokes a prior commitment. The [Book of Debts T3 protocol](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/RELATIONSHIP_RECONCILIATION_PROTOCOL.md) therefore takes **24 chronologically ordered pairs** sampled from eight recurring named participants: Clara Weiss, Marta Voss, Jakob Lenz, Mathilde Rosen, Anna Lenz, Emil Reuter, Anton Kappel, and Henry Frankenstein.

The [unlabeled reviewer packet](https://github.com/Azimn/Attractomancy/tree/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/packets/l1-relationship-t3) was built and verified in a successful GitHub Actions run. Reviewer-facing entries include the counterparty name and earlier/later original narrative excerpts but **no original event ID or source-authored relationship-change fields**. The source-author-sidecar and source hashes remain in organizer-only metadata excluded from the public CI commit. For each participant the packet contains early→middle, middle→late and early→late comparisons; the 24 pairs overlap, so the dataset comprises eight *dependent* relationship histories rather than 24 independent persons.

The review categories are reinforcement, modification, specific commitment supersession, tension/conflict and insufficient context. **Chronological recency alone is not proof of revocation.** The [human reviewer schema validator](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/l1_relationship_adjudicate.py) requires three reviewer records per case, explicit source quotes for affirmative claims, specific original/revised commitment quotes for supersession, confidence and rationale. Its synthetic unit tests passed in [CI](https://github.com/Azimn/Attractomancy/actions/runs/38060941520). These are software test fixtures, **not actual human relationship judgments**.

## Next evidence gate

The Book of Debts packet is an auditable starting point for studying temporal relationship continuity, not a validated test yet. Three independent reviewers must establish which claims are justified by the narrative. Only then can a model be tested on source-sensitive relationships using earlier-only, later-only, both and withheld-memory controls, along with reordering and wrong-subject provenance checks.

The main Tribunal E3 still independently requires at least 36 novel dilemmas, independent relevance reviewers, alternative sufficient source sets and cross-family decisions. Neither these source-derived paired events nor exact field copying can satisfy that larger confirmatory benchmark on their own.

**No production Pretorius state, neural connections, FlyWire/BioCircuit caches, source autobiography, or lived-experience ledger were changed by the source-reading and packet-generation studies.**
