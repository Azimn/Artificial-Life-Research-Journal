# Shared Memory Across the Character Research Program

**Date:** 2026-10-09  
**Status:** Cross-project architecture and integration audit. No new runtime wiring is claimed here.  
**Research scope:** Pretorius Connectome / FlyWire, BioCircuit, The Doctor Lives, Eidolon / Noetic, Kiki Mind, Calibos Mind, Attractomancy, and Frankenstein Village.

## Decision

Reuse **memory infrastructure, provenance contracts, indexing, retrieval procedures, and evaluation harnesses**, not other subjects' autobiographical records or synaptic weights. Distinguish canonical events, derived representations, query-time candidates, policy eligibility, rendered answers, and runtime experience. Each stage has different authority and a different owner.

The shared service is presently **Vector Fly**, a CPU-local, read-only SQLite backed retrieval API for the 450-event reconstructed Pretorius v12 corpus. It is not a generic multitenant memory database and it must not be represented as one. Its fixed source, namespace, and provenance checks are a strength, not an obstacle to be removed. Future subjects can reuse a common *interface and code pattern* with **separate verified indexes**, not reach into Pretorius's autobiographical namespace. A single backend engine or daemon may eventually host multiple isolated indexes only after per-request authorization, scope enforcement, and isolation tests exist.

## Verified existing foundations

**Canonical source and memory processing:** [Pretorius-Connectome](https://github.com/Azimn/Pretorius-Connectome) owns frozen v12 source Git blob `718dcc2d5ba4feccdef1690d447edfcebaa9bfb5`, canonical L1 projection, separately versioned BC01 hashed lexical cache, and split-fitted deterministic TF-IDF L2 v2. See [consolidation](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/SHARED_MEMORY_CONSOLIDATION_20261008.md) and [L2 v2 reproducibility](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/SHARED_MEMORY_L2_V2_REPRODUCIBILITY.md). Original fly synapse counts and BioCircuit neural architecture are not shared weights.

**Query service:** [Vector Fly database](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/VECTOR_FLY_DATABASE_V1.md) is an exact sparse SQLite lexical search store, and [its agent API](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/VECTOR_FLY_AGENT_API_V1.md) provides `GET /v1/health`, `GET /v1/info`, `POST /v1/search` and `GET /v1/memories/{event_id}`. Its current API returns retrieved candidate records, source identifiers, scores, and explicitly non-entailing evidence status. Search supports provenance and episode filters, not per-user permissions or arbitrary memory ownership. It must remain loopback-only unless protected by authenticated, encrypted transport.

**Production Pretorius integration already exists:** [The Doctor Lives Vector Fly A/B protocol](https://github.com/Azimn/The-Doctor-Lives/blob/main/docs/VECTOR_FLY_PERSONA_AB_PILOT01.md) inserts externally retrieved, explicitly reconstructed source passages into the renderer evidence slot without creating `lived_runtime_memory` or changing neural state. [Actual Stage 02 local-renderer results](https://github.com/Azimn/The-Doctor-Lives/blob/main/results/vector_fly/STAGE02_REAL_OLLAMA_DIALOGUE_RESULTS.md) contain 12 nonempty outputs from six post-hoc paired prompts: four pairs differed, but false claims, temporal conflation, and nonanswers were observed. This validates the plumbing and causal possibility of different text, **not improved autobiographical accuracy**. [Stage 03](https://github.com/Azimn/The-Doctor-Lives/blob/main/docs/VECTOR_FLY_BLINDED_REVIEW_STAGE03.md) is a reviewer/evaluation infrastructure, not completed independent validation.

**Attractomancy integration already exists:** [SCH E1 integration note](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/SCH_E1_STATEFUL_MEMORY_FINDINGS_20261009.md) records that the same L1 records can be selected by editorial cues or opaque keys in a guarded SQLite sandbox. Equal supplied records produced no cue-specific reply advantage in the reported paired cases. Do not treat ritual/symbol names as causal features without ablation. The sandbox's permissions and relationships are **synthetic**, not Pretorius's lived history.

## The common contract for future consumers

The abstract interface should provide a **read-only source-owned retrieval capability** with an explicit caller, subject, collection and view. The returned candidate must carry the original source ID and version, subject/namespace, provenance classification, source hash, retrieval encoder and split/scope, access classification, excerpt/full-record reference, and retrieval score. Search results are never authoritative entailment judgments. The consumer must independently decide whether the candidate is **eligible to be perceived or used for a specific action**.

The service must not append canonical events, update relationships, mutate synapses, manufacture memories, set commitments, or make decisions. Those belong to each project's authoritative runtime and require their own verified event pathways. A query response must not be reclassified as a firsthand event merely because a language model repeated it.

When translating the architecture into a generic implementation, prefer an adapter boundary such as `search(query, subject_scope, caller_scope, top_k, source_version)` and `get_record(record_id, subject_scope, caller_scope, source_version)`. This is a proposed interface, **not** the current Vector Fly HTTP API. Never add `subject_scope` as an unvalidated client-supplied string and treat it as authorization. The host must bind identity and permissions to trusted runtime authentication or capability grants, then enforce them on retrieval, enumeration and result hydration. The existing localhost-only Pretorius service is suitable for isolated trusted experiments, not public cross-player deployment.

An illustrative reusable candidate envelope (conceptual schema, not yet shipped):

```json
{
  "schema": "portable-memory-candidate/0-proposal",
  "source_namespace": "pretorius.reconstructed.v12",
  "subject_id": "pretorius",
  "record_id": "E01-001",
  "origin_class": "reconstructed_prehistory",
  "source_git_blob": "718dcc2d5ba4feccdef1690d447edfcebaa9bfb5",
  "index_scope": "all_browse_not_holdout",
  "encoder_id": "versioned-lexical-tfidf",
  "evidence_relation": "candidate_only",
  "visibility": "subject_authorized",
  "eligible_for_lived_write": false
}
```

The source source's `provenance: reconstructed` may be mapped to a downstream `origin_class` only by an **explicit reviewed translation table**. `visibility` is an output of an authorization check, not an imported truth about the consumer. A source hash proves local data consistency against a trusted pin, not that content authored by an untrusted sender is factually authentic.

## Per-project integration candidates

### The Doctor Lives: integrate selectively, then evaluate

Its current evidence-slot adapter is already correct in its major isolation decision. Do not create a replacement memory pipeline or copy Vector Fly outputs into `brain.sqlite3`. The next work is controlled source-verification and answer-or-abstain evaluation with **new independently reviewed questions**, an adequate pinned local renderer, and separately measured attribution and temporal-confusion errors. If graph reranking is investigated, freeze the initial lexical candidate IDs and compare real FlyWire to rewired topology under identical rendering conditions. Treat the accepted v0.4 subject contract and causal-audit migration gates as authoritative.

### Eidolon / Noetic: candidate perception and action eligibility, not imported identity

The proposed cognitive architecture can consume retrieved candidate records as **external evidence entering a perception or self-binding gate**. Proposed state flow: retrieve candidate -> verify owner/source/version -> evaluate eligibility and uncertainty -> expose a bounded, provenance-tagged item to the subject workspace -> measure its influence on policy -> optionally update a runtime ledger through a separate explicitly authorized lived-event pathway. Do not turn archived Pretorius text into the controller's own memory and do not claim a working project-specific API without a verified repository and tests. Ablate the candidate gate, source label, recency, symbolic cue and policy influence independently. Attractomancy's arbitrary-key equivalence and archive-provenance failures are important negative controls.

### Kiki Mind: use only disposable retrieval projections of Kiki's ledger

[Kiki Mind](https://github.com/Azimn/Kiki-Mind) makes canonical event history authoritative and derived projections reconstructible. Its ledger and projection storage must remain physically separated, replay-equivalent, fingerprinted and freshness-checked. An optional local lexical/vector retrieval index over **Kiki's own permitted canonical events** could be rebuilt from the ledger and destroyed without losing history. Candidate relevance must never grant canonical authority; do not import Pretorius biography as Kiki autobiography. Preserve the `forbid_canonical_experience` ancestry gate and developmental-evidence semantics from the v0.3 Implementation 003 contract. Do not reuse FlyWire's source-specific manifest as Kiki's ledger authority.

### Calibos Mind: reuse mechanism and interface, never private thought contents

[Calibos Mind](https://github.com/Azimn/calibos-mind) maintains a private local `mind.db`, private thought/dream/inbox sidecars and source-specific salience/consolidation state. Its public code and schemas can inform candidate ranking, episodic recall, contradictory record handling and retention studies, but private contents remain local-only. A retrieval projection, if needed, should read from Calibos-authorized private state inside the same trusted machine boundary; the existing public Pretorius API should not be pointed at that private database. Preserve archive-never-delete, provenance, sleep isolation and explicit consent to cross-agent message sharing.

### Frankenstein Village: treat world facts, rumors and masks as distinct authorities

[Frankenstein Village](https://github.com/Azimn/frankenstein-village) has a server event ledger, authored canon, persistent world state, per-mask identity, resident-local perceptions, rumor provenance and sparse resident relationships. Proposed retrieval can support memory of **events an individual resident or player mask actually witnessed, heard, read or was told**, with separate public world knowledge and private character knowledge. Never index hidden plot material or other masks' private rooms into a globally searchable service. Access must be verified in Evennia before source retrieval, with rumor/hearsay represented as claims attributed to speakers rather than server-certified world truth.

Build the smallest opt-in adapter atop the **existing** world event/Resident Life v2 records; no continuous vectorization for every NPC and no inference call per world tick. The game rule is continuity active, cognition only when required. Retrieval should happen on player inquiry, consequential event, NPC activation, or limited local interactions, not as an always-on simulator. Protect authored-locked NPCs. This is an architecture candidate, **not a running game plugin**.

### Pretorius Neural Network / BioCircuit and FlyWire: retain controlled experimental separation

[BioCircuit](https://github.com/Azimn/Pretorius-Neural-Network) and [FlyWire](https://github.com/Azimn/Pretorius-Connectome) already reuse frozen L0/L1 and separately labeled feature encoders. Keep experiments on their original distinct neural substrates. Newly shared input or cached features must be a named experimental condition, not an unrecorded change to prior baselines. Publish lesion tests, frozen train splits, independent-process fingerprints and output reproducibility before making any memory or identity benefit claim.

### Artificial-Life-Research-Journal: archive evidence, not somebody else's mental state

[The journal](https://github.com/Azimn/Artificial-Life-Research-Journal) is the cross-repository research index. Link exact source versions, branch/merge decisions, experiment protocols, run IDs, negative results, confidence limits, adaptation proposals and evaluation status. Do not duplicate the entire autobiography, copyrighted sources, private agent stores or game player logs. This document is a navigation and methodology record, not a production state donor.

## Shared tests and acceptance gates

**Source/replay:** given the same source version, split, preprocessing version and stable seed, both independent processes reproduce identical data hashes, ordered record IDs and feature caches. Check corrupted manifests, stale source pins, mismatched `PYTHONHASHSEED` and legacy cache versions. Preserve negative drift reports such as L2 v1's non-deterministic vocabulary construction, which necessitated L2 v2.

**Provenance/identity:** make deliberately wrong-owner archives available, and prove that consumers refuse to adopt them as self history even when the passage is highly relevant. Reject nonexistent event IDs, invalid source hashes, unauthorized subjects, post-revocation access and retrieval attempts through other player masks. A successful rank-1 hit is not evidence that a subject should believe, disclose or act on the record.

**Behavior:** compare no retrieval, lexical retrieval, graph reranking with matched random/rewired controls, and provenance/eligibility gate ablations under the same source/event budgets. For neural projects, additionally perform real synapse-path interventions; for agent systems, compare decisions across model changes and restarts. Measure supported recall, false acceptance, contradiction rejection, continuity across turns, latency, memory usage and privacy violations rather than merely response difference.

**Separation:** queries and vector caches cannot write to canonical records, subject ledgers, live commitments, neural checkpoints or Evennia world state. A subsequent event writer, when separately authorized, records the actual runtime observation and source links, not a disguised copied reconstruction. Continuous synchronization between subjects is **not** the default.

## Recommended sequence

**Already achieved:** common Pretorius L1, compatible per-encoder L2 caches, read-only Vector Fly API, BioCircuit/FlyWire source reuse, and The Doctor Lives engineering A/B. Respect these as the starting point.

**First new reusable feature:** one small, tested source-adapter contract with typed provenance and subject-owner checks, developed against **synthetic** event ledgers for two fictional subjects. It should be possible to delete/rebuild the retrieval projection without changing either source ledger; wrong-owner and access-revoked tests must fail closed. It should not require a new vector model, daemon or paid API.

**First practical consumer:** a private, opt-in read-only Kiki ledger projection or a small synthetic Frankenstein Village resident fixture, whichever can satisfy source ownership and visibility tests with less code. Neither should read Pretorius's biography as its own past. Keep game deployment and network exposure outside the initial acceptance test.

**Next scientific integration:** evaluate Pretorius source evidence and self-binding decisions using matched gate ablations; retain Attractomancy neutral-key negative controls, provenance-swap guard cases, and The Doctor Lives response-quality failures as preregistered threats.

**Before promotion:** code, tests, true CPU runs, original source SHA/encoder version, permission model, publication-safe outputs and any negative results must be archived. Do not claim operational interoperability from this planning document alone.
