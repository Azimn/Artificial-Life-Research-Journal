# Kiki Memory-Cognition v0.3: source-authorized synthetic content pilot

**Date:** 2026-10-10, America/Chicago  
**Kiki project:** [PR #9](https://github.com/Azimn/Kiki-Mind/pull/9), [Issue #8](https://github.com/Azimn/Kiki-Mind/issues/8) (independent semantic gate remains open).  
**First complete execution:** [GitHub Actions 38058221101](https://github.com/Azimn/Kiki-Mind/actions/runs/38058221101), all steps green; raw 180-case artifact [11672540015](https://github.com/Azimn/Kiki-Mind/actions/runs/38058221101/artifacts/11672540015).  
**Fixture SHA-256:** `85a6f86d237fca4d9d201748a7aeb4e484552c9951fea9e33be480e80d693e06`.  
**Shared interface exact pin:** `cc82c72167d87c19f16125ccdf9477b53c777878`.

## Design and its strict limitations

This is a **synthetic-source authority and rule-interpreter engineering pilot**, not a semantic-memory experiment. The 22 source records and 36 queries/gold answers were all assistant-authored and public; 18 cases were labelled evaluation but are **not independently blind**. The resolver receives the intended entity, relation, two-hop operation and date as structured oracle intent. It does not parse open natural language or operate a language model.

The fixture, then protocol, were committed before the implementation. The actual Kiki canonical event ledger holds synthetic source receipts; a derived content sidecar checks exact source record SHA, actor, epistemic class, claim domain, subject owner and content restriction. Non-Kiki and restricted documents are excluded *before* indexing and search. The reader provides JSON typed evidence to the same shared MemoryCognitionPort as the existing Pretorius and Kiki v0.1 adapters. No real Kiki personal memories, Calibos content, lived-write path, trained model or neural substrate is involved.

## Observed 36-question outcomes

| Condition | Correct | Correct positive answers | Correct abstentions | Incorrect affirmative answers |
| --- | ---: | ---: | ---: | ---: |
| No evidence | 8/36 | 0 | 8 | 0 |
| Uniform sample of up to six permitted source records | 13/36 | 7 | 6 | 2 |
| Direct lexical source | 36/36 | 28 | 8 | 0 |
| Same source through shared cognition port | 36/36 | 28 | 8 | 0 |
| Same retrieval, but unwisely trusting rumor | 34/36 | 26 | 8 | 2 |

The **strong same-content null** is exact agreement between direct retrieval and the shared port on all 36 answers and evidence IDs. Nothing suggests the port gives superior cognition over direct retrieval; it supplies an interoperability and provenance transport contract.

The source-eligibility ablation is more interesting: treating unverified rumors as authoritative causes two false assertions under this synthetic rule system. That is evidence that a typed provenance gate changes controlled decisions, **not** that a language model with real autobiographical memories would behave similarly.

The uniform-source arm has matched maximum source slots but not the same information or actual text budget; across cases it received 51,714 content characters versus 32,362 in direct/shared. This is **not** an information-matched causal comparison, despite the similar capacity ceilings. No scientific superiority claim may be based on that comparison.

All 5 probes passed: wrong owner denied, foreign document not indexed, restricted document not indexed, revoked token denied, stale projection denied. The canonical ledger remained unchanged during all scored trials, with a synthetic post-trial append solely to test stale-source rejection. The original Kiki test suite, old cross-project tests, and six new content safety/replay tests passed in the executed workflow.

## Evidence and promotion status

The predeclared fixture and runbook, actual synthetic-only adapter, 36-question runner, source-hash tests, GitHub Actions workflow and [full results interpretation](https://github.com/Azimn/Kiki-Mind/blob/experiment/cognition-v03-source-authorized-content/experiments/cognition_port_v03/RESULTS.md) are filed in Kiki Mind. Original case-level results are in the CI artifact. No new permanent production memory service, private content index or API has been deployed.

The follow-on [Issue #8](https://github.com/Azimn/Kiki-Mind/issues/8) should **remain open** until separate provenance/visibility review, independent authoring and sealed evaluation, a real language-query interpreter under a pinned model digest and genuinely matched information budgets have been completed. The current pilot does not meet that issue's independently validated semantic cognition gate.

**Central lesson:** a common memory interface can carry source-authorized claims into cognition, but a subject must still decide whether an event is its own history, an external fact, a hearsay report, an interpretation, or an item to abstain on. Source authority and retrieval relevance must remain separate.
