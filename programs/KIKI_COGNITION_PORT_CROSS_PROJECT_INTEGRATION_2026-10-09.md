# Kiki Ledger to Memory-Cognition Port: First Independent Consumer

**Research date:** 2026-10-09, America/Chicago  
**Kiki code:** [Kiki-Mind PR #5](https://github.com/Azimn/Kiki-Mind/pull/5)  
**Common interface:** [Pretorius-Connectome, merged PR #31](https://github.com/Azimn/Pretorius-Connectome/pull/31), pinned commit `cc82c72167d87c19f16125ccdf9477b53c777878`  
**Research status:** merged and verified on both the existing Kiki tests and cross-repository integration suite. **Kiki main merge commit:** `5f4940d1003e4746bbd16a8951455732a7ba5f2e`. Original shared-interface pin remains `cc82c72167d87c19f16125ccdf9477b53c777878`.

## Question

Can the same external, source-scoped memory-to-cognition contract consume the independently designed Kiki Mind canonical event ledger without importing Pretorius biographical contents, bypassing Kiki's transition gate, creating new canonical events, copying private thoughts or letting returned retrieval candidates become automatically accepted lived memories?

## Implementation

`runtime/kiki_mind/cognition_adapter.py` imports the **existing upstream** `pretorius_connectome.cognition_port` classes, not a private reimplementation. The adapter receives an existing validated `EventLedger`, verifies its canonical SHA-256 chain, and snapshots the latest head. The source descriptor binds subject `kiki`, namespace `kiki.canonical.events`, metadata-token index version, and the exact canonical head hash.

The optional disposable in-memory index includes only fixed type labels and recognized metadata categories of already canonical receipts (source evidence ingested, recorded encounters, recorded interpretations, and developmental observations). It does **not** expose underlying source title, message, report content, relationship private text, autobiographical passages, raw payloads, or restricted records. `observed_runtime` labels the existence of a logged receipt only. Its truth interpretation is separate.

Any canonical append invalidates the source snapshot; the consumer must rebuild from the authoritative ledger before retrieval resumes. Source capabilities are issued only by the trusted in-process host and can be revoked. The subject ID is checked by the upstream port before any lookup. The adapter creates no new SQLite tables and writes no canonical state.

The [cross-project test suite](https://github.com/Azimn/Kiki-Mind/blob/feature/cognition-port-ledger-adapter-v01/tests_integration/test_memory_cognition_port.py) uses **synthetic data** in real Kiki `EventLedger` instances, not Kiki's private/live account. It exercises provenance, subject-swap rejection, fake memory lookup, restrictions, unchanged canonical head, rebuild/restart, revocation and independent process determinism. The GitHub workflow checks out the exact pinned upstream common interface and runs both these tests and the existing Kiki regressions.

## Initial failure and correction

The first CI job executed all eight new integration tests and passed seven. One failed because the test incorrectly expected an empty Python list for no matches, while `MemoryCognitionPort.search` correctly returns an immutable empty tuple. This was a **test expectation error**, not incorrect record retrieval. The test was corrected in commit `bcf88ac0303d30571b17184956801a392ed111cb`. Both final-head CI workflows passed: [cross-project interoperability run 38025840323](https://github.com/Azimn/Kiki-Mind/actions/runs/38025840323), [full Kiki regression run 38025840269](https://github.com/Azimn/Kiki-Mind/actions/runs/38025840269). A second pair on the same exact head also passed ([cross-project run 38025837197](https://github.com/Azimn/Kiki-Mind/actions/runs/38025837197), [Kiki regression run 38025837212](https://github.com/Azimn/Kiki-Mind/actions/runs/38025837212)). The PR was squash-merged at `5f4940d1003e4746bbd16a8951455732a7ba5f2e`. Retain the original failure and correction as audit evidence.

## Scientific boundaries

This is an **interoperability test**, not a finding that the character improves cognitively. The metadata-only retrieval deliberately lacks episodic content recall and cannot justify adding source titles, private records, a production renderer, psychological conclusions, or shared personal memories. The familiar words in its bounded metadata relevance index are not validated semantic embeddings.

Kiki's own ledger and deterministic projector remain authoritative, as do the developmental evidence and `forbid_canonical_experience` restrictions. A trusted host must verify real user permissions separately; in-process capabilities are not public-user authentication. Pretorius's canonical prehistory, FlyWire neuron IDs, BioCircuit trained weights, and all Calibos private cognition remain entirely separate.

## Next gate

The completed green two-project CI and preserved Kiki baseline tests authorize the completed narrow merge. The next work is a second-stage **synthetic** character task requiring retrieval of safe event receipt metadata. Real content retrieval must wait for a separately reviewed content-visibility scheme, attacker/owner-swap controls and no-memory comparator. No live subject migration is authorized by this implementation.
