---
id: JRN-2026-10-08-SOULSCRIPT
title: SoulScript external-prior-art comparison and Calibos critique
type: journal-entry
status: recorded-prior-art-and-proposed-test
updated: 2026-10-08
---

# 2026-10-08: SoulScript, Calibos and the necessity of load-bearing mechanisms

## Evidence event

The owner submitted an [ArtificialSentience Reddit shortlink](https://www.reddit.com/r/ArtificialSentience/s/AF5Lwgw909) for review, followed by a critical assessment from Calibos. The supplied review identified [DrTHunter/SoulScript-Engine](https://github.com/DrTHunter/SoulScript-Engine) as the candidate source, pointed out a third design-level convergence on frozen identity and mutable experience, required an equal-budget random-scheduling negative control, and proposed a bridge to the existing PEMA scarcity allocator. This entry documents those claims without attributing Calibos's statements to directly reproduced experiments.

## Verification and attribution

GitHub main tip [f299a752](https://github.com/DrTHunter/SoulScript-Engine/commit/f299a752579cefbd557c59cd00da0f9e73b30eb5) is dated September 30, 2026. Repository metadata indicates the owner is GitHub **user** `DrTHunter` and last push was September 30. The README self-attributes its creation to "Dr. Trent Hunter", which is not independent identity verification. The Reddit handle `u/OrionForgeEcosystem` is reported by Calibos; the direct shortlink was not resolved in this audit.

The [source-level literature note](../../literature/2026-10-08-orionforge-soulscript-engine.md) distinguishes implemented/documented dual-FAISS identity and life-memory stores plus an older optional autonomy tick loop from the newer claimed autonomous, surprise-driven loop. **Status of the latter: code drop pending.**

## Convergent architecture with a sharp evidence boundary

SoulScript has a read-only identity FAISS index and writable life-memory index. Calibos describes its [cartridge roots and mutable experience records](https://github.com/Azimn/calibos-mind/blob/18497706f9ada6840c1e3bc40bf121941f9332e7/README.md) and compares another reported design, SoulCore Tier 0, whose primary source still requires verification. Earlier local [Core Memories and SoulFile work](../../projects/PRJ-023-Portable-Identity-Standards-Line.md) supplies additional historical context.

Multiple teams choosing this split makes it a compelling *convergent engineering hypothesis*. Independence of discovery, necessary versus convenient structure, and advantage over a single-store or dynamic-identity variant remain unproven. This supports prioritizing causal comparison, not claiming replication.

## Critique accepted

Calibos correctly identified random scheduling as an essential negative control: surprise-dependent scheduling must beat fixed and random schedules at matched compute, and event-alignment controls should rule out mere burstiness. The corresponding [EXP-2026-064 proposed protocol](../../programs/EXP-2026-064_SURPRISE_SCHEDULING_AND_SCARCITY_V0.md) preserves the fixed, random, surprise and shuffled-surprise comparison, with frozen primary behavioral criteria.

The scarcity bridge must distinguish *urgent allocation* from *uniform throttling*, using task completion, false urgency, ordinary-task starvation, and absolute useful work as well as processing share. [EXP-2026-010](../../EXPERIMENT_LEDGER.md) measured approximately 26% abundant versus 41% scarce threat-processing share in PEMA. No OrionForge or Calibos reproduction is claimed.

## Decision

**Register prior art; register falsifiable protocol; track upstream; do not directly transplant.** A surprise-scheduler candidate in calibos-mind may proceed only as a reversible builder proposal with a critic attempting to falsify it, under existing no-trigger-proliferation and private-cognition boundaries. No agent or production project has acquired a validated continuity improvement from this note.
