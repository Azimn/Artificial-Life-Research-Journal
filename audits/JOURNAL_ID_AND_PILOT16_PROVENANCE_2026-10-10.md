---
id: AUDIT-2026-10-10-ID-PROVENANCE
title: Journal identifier and Pilot16 provenance reconciliation
status: open
updated: 2026-10-10
---

# October 10, 2026: ID and provenance reconciliation

## Pilot16 provenance (pending source-level verification)

Previous portfolio review reported a successful second original FlyWire Pilot16 workflow [38028315635](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38028315635) and an archival [commit 1d08df1931370978e1d85e5a3dea08b7e80090ca](https://github.com/Azimn/Pretorius-Connectome/commit/1d08df1931370978e1d85e5a3dea08b7e80090ca), preserving raw cases and ten checkpoints. Reported aggregate outcomes matched the earlier run while raw JSON hashes differed. This audit has **not independently fetched both raw JSON files or their hash manifests**. Consequently byte-level equivalence, exact changed fields, seed/config parity and whether differences are only metadata remain **unverified**. Do not infer independent scientific replication from two successful CI executions. Before promoting a Pilot16 result, pin the two original case artifact paths, blob SHAs and SHA-256 digests; compare normalized case records and checkpoint hashes, configuration and source anatomical hashes, and document any divergences without overwriting either artifact.

## Pilot13 ledger correction

[EXP-2026-065](../EXPERIMENT_LEDGER.md) now recognizes successful original whole-v783 main replay [38024218512](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38024218512) and [permanent archive run 38024902479](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38024902479). The prior float32 parity failure, corrected numerical-tolerance policy, unchanged categorical predictions and lack of bitwise main-branch weight equivalence remain explicit. The [existing dated source note](../journal/2026/2026-10-08-flywire-pilot13-capacity.md) already documents the archival resolution; no duplicate experiment ID was created.

## Identifier audit: unresolved collisions

The preceding October 10 portfolio review reported **five groups of duplicate identifiers** across October 8–10 records. The exact conflicting files and frontmatter occurrences have **not been independently enumerated in this pass**, so the number is a prior-review lead, not a freshly validated count. No IDs have been renumbered or silently reassigned. Follow-up: enumerate every YAML `id` and experiment ledger ID on the current default branch, group by exact ID, distinguish legitimate cross-references from duplicate primary record declarations, and prepare a mapping of each conflicting path and earliest committed use. Preserve established citations and negative results; resolve collisions only with a documented alias/migration table and source verification.

## Noetic registration

[PRJ-044](../PROJECT_REGISTRY.md) records [The Noetic Engine](https://github.com/Azimn/The-Noetic-Engine) as a separate speculative architecture and deterministic engineering foundation. Its README expressly disclaims completed efficacy testing. It is not an independently validated continuity result or the definitive Pretorius production brain.

## Evidence classification

Pilot13: original exploratory computation with archived cases and known precision caveat. Pilot16: reported CI/archive evidence, provenance comparison pending. Noetic: design and engineering foundation only. ID collisions: unresolved metadata integrity audit, not experimental evidence.
