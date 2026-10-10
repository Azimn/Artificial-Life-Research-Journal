# Memory-to-Cognition Port v0.1: executable shared interface

**Research date:** 2026-10-09 (America/Chicago)  
**Implementation repository:** [Azimn/Pretorius-Connectome](https://github.com/Azimn/Pretorius-Connectome)  
**Merged PR:** [#31](https://github.com/Azimn/Pretorius-Connectome/pull/31)  
**Verified merge commit:** `cc82c72167d87c19f16125ccdf9477b53c777878`  
**Research status:** an implemented, source-aware, read-only transport boundary, not a demonstrated improvement in character cognition.

## Purpose

Implement the first executable common memory-to-cognition interface without altering canonical memories, biological FlyWire topology, BioCircuit weights, or The Doctor Lives lived experience. Preserve distinct subject ledgers and let each cognitive engine consume source-verified candidates through its own perception, self-binding, belief and action policies. Do not build another vector database.

## Code and documentation

- [MemoryCognitionPort implementation](https://github.com/Azimn/Pretorius-Connectome/blob/main/src/pretorius_connectome/cognition_port.py): standard-library-only, immutable typed evidence packets, versioned source descriptors, two-subject namespace and source verification, revocable ephemeral in-process capabilities and explicit `eligible_for_lived_write=False`.
- [Existing Vector Fly adapter](https://github.com/Azimn/Pretorius-Connectome/blob/main/src/pretorius_connectome/vector_cognition_adapter.py): wraps the already pinned `VectorFlyStore`, maps reconstructed Pretorius entries to externally sourced evidence, and validates result excerpts against the original source records.
- [Runnable demonstration](https://github.com/Azimn/Pretorius-Connectome/blob/main/scripts/demo_cognition_port.py): uses existing deterministic L2/SQLite cache and emits real structured JSON without invoking an LLM or altering a character.
- [Contract, security and future adapters](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/MEMORY_COGNITION_PORT_V0_1.md): describes source ownership, trust boundary, unsupported multi-tenant and per-record authorization cases, scientific limits and next experimental stages.

## Measured engineering evidence

- [First green PR port workflow](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38025374837): 8 synthetic two-subject unit tests, actual 450-memory Vector Fly adapter tests, withheld episode isolation, original-source validation, actual cache/database regeneration, JSON demonstration and provenance/scope invariants passed.
- [First green PR foundation workflow](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38025374814): existing foundation regression workflow passed against the same feature branch head `4d1517d1a106dc59d75a82e6ff217f5cfa2d6113`.
- Independent local run of the standalone synthetic tests also passed all eight before commit. Workflow evidence is authoritative for the canonical source integration.
- The real retrieval behavior remains lexical TF-IDF, not semantic entailment, stored neural autobiography, transferable phenotype, or proof of personhood. A source hit does not imply a correct answer.

## Key boundaries

The capability issuer is controlled by a **trusted Python host**. This is in-process scoping, not authentication of hostile processes or remote users; if an attacker can directly call `grant_self`, it is outside this prototype's security model. Source adapters must independently verify their own data; a provided hash does not authenticate an untrusted origin. The implementation intentionally does not allow cross-subject grants or host private multi-tenant databases.

For production Pretorius, continue using the existing safe read-only Vector Fly evidence-slot path pending an explicit [Doctor Lives authority migration gate](https://github.com/Azimn/The-Doctor-Lives/blob/main/ARCHITECTURE_CONTRACT.md). Do not import reconstructed archival text as `lived_runtime_memory`. Kiki and Calibos retain their own private/canonical stores, and Frankenstein Village must implement Event/Evennia-authorized visibility before searching any resident or mask memory. None of those production adapters were installed by PR #31.

## Next falsifiable research step

Port the interface to a second **synthetic** ledger with a different backend, then verify process restart, source edits, access revocation, actor/owner swap and retrieval-versus-no-retrieval policy outcomes. Freeze an independently reviewed challenge before claiming cognitive benefit. Distinguish differences caused by supplying more text from differences caused by actual neural or self-binding architecture. The first stage deliberately establishes a common boundary, not a common mind.

This follows [the cross-project integration assessment](CROSS_PROJECT_SHARED_MEMORY_INTEGRATION_2026-10-09.md), without duplicating any private thought content, unrelated project data or canonical source archives.
