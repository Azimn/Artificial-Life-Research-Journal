---
id: JRN-2026-10-09-01
title: "FlyWire Pilot15: Two-Timescale Synaptic Association and Numeric Capacity Controls"
type: journal-entry
status: active; original biological source verification pending
updated: 2026-10-09
projects:
  - PRJ-038
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
---

# 2026-10-09: Pilot15 — stabilizing yesterday without preventing tomorrow

This is a **continuation of the same original source-controlled Pretorius FlyWire experiment lineage**, not a new prototype or a new independently corroborated identity. Canonical implementation and source-owned results: [Pretorius-Connectome](https://github.com/Azimn/Pretorius-Connectome), [PR #30](https://github.com/Azimn/Pretorius-Connectome/pull/30), [complete preregistered Pilot15 protocol](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/flywire-pilot15-dual-trace/docs/FLYWIRE_DIRECT_IMPRINT_PILOT15.md), and [cumulative experimental issue #17](https://github.com/Azimn/Pretorius-Connectome/issues/17).

## Predecessors and verified archival status

[Pilot13 research log](2026-10-08-flywire-pilot13-capacity.md) documented actual original full FlyWire-v783 **15/16 earliest source IDs initially correct** falling to **4/16** after 317 source events, with a constant external 317-target codebook and matching degree-rewired intervention. [Pilot14 research log](2026-10-08-flywire-pilot14-synaptic-stability.md) documented actual original original FlyWire β4 protected source-edge updates identifying **10/16** earliest source IDs at full load against β0 additive **4/16**, but identifying **0/16 newest** versus β0's **2/16**. An ordinary 50,920-scalar masked signed nonneural matrix outperformed original biological-edge learning on **newest (6/16)** and original **159 familiar source prompts (46/159)**. None recovered genuinely untrained fourth source cues (0/31); false acceptance of 71 source-episode-absent inputs remained high.

The [original Pilot14 automatic permanent Git archival workflow 37884007363](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37884007363) has **SUCCEEDED**: complete true-original full-v783 per-event case JSON and seven actual learned synaptic/masked-matrix numerical NPZ checkpoints now exist on owning project `main`, linked in [the original real Pilot14 archival report](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT14_REAL_SYNAPTIC_STABILITY_RESULTS.md). **Pilot13 does NOT have a confirmed successful permanent archive**; its original source results were measured but [PR #29](https://github.com/Azimn/Pretorius-Connectome/pull/29) separately attempts to fix source checkpoint bitwise-vs-float32 tolerance documentation. The source discrepancy was 5,602 weight entries differing by no more than 2.384185791015625e−7, including one near-zero slot; source event predictions and original anatomy were consistent. Do not conflate that bookkeeping correction with an altered memory-learning experiment.

## Prospectively fixed new mechanism

The bottleneck is increasingly visible: freezing existing associative synapses protects an older input→content mapping but suppresses plasticity for new evidence. The Pilot15 experimental hypothesis is that a **long-term stable numerical trace plus a separate fast decaying numerical trace** may preserve some early associations *while permitting adequate newly presented source cue-content acquisition*.

Predeclared fast/slow behavior: an original directed synapse's **slow trace** is the previously engineered β=1 or β=4 usage-dependent protected numerical update; an independent same-edge **fast trace** uses the original additive update. Split fixed per-literal-cue total nominal numeric rate **0.7/3** into **60% slow and 40% fast**, then decay the fast trace by **0.97 only after each fully completed source memory of three cues**. At cue-only inference, independently normalized signed 256D slow/fast responses blend 60/40 and are normalized again. There is no database of source labels, events, narratives or ID-to-content vectors inside either trace; **event classification is entirely EXTERNAL oracle-only**.

**Important experimental resource confound:** The two-trace source model doubles the eligible learned numeric synapse state from **50,920 scalar directed-edge weights to 101,840 independently writable numeric weights**, plus local exposure counters. This is not simply giving one trace a cleverer rule at equal capacity. Therefore include the previous **single-slot 50,920 numerical masked nonneural linear** and a **DOUBLE-slot 101,840 two-trace nonneural masked linear comparator**, matched in cue exposure count, 60/40 source rate allocation, fast-decay per original memory and source BC01 vectors. Comparator masks are source-independent and never hold event-IDs; they do not match fly contact weight, computational cost or numeric update norms.

Eight predeclared model conditions: real original additive; real original single-trace β4; real original dual β1; real original dual β4; binary-degree-preserving rewired original real dual β1; real original dual β1 with deliberately wrong source-content pairing; original 50,920 masked nonneural matrix; original 101,840 masked two-trace nonneural matrix. Original graph is read-only; the rewired null is separately cloned and maintains exact eligible source outdegree/readout indegree and edge-slot counts, not each target's contact-weighted incoming strength.

All arms ingest exactly the **same original 450 reconstructed Pretorius source records/27 episodes, original BC01 signed 256D lexical inputs and separately source-coded CONTENT targets**; 317 source train items, 62 validation-episode absent, 71 test-episode absent, historical 159 familiar-source prompts, and 31 eligible never-trained original fourth source literal prompts; same first/middle/last three authored cues, original seed31 source split and seed20261008 learning order. Eight arms evaluated at 0/16/32/64/128/256/317 source memories with a **fixed 317-event candidate codebook kept EXTERNAL** to all inference. Source historical Pilot10 original 159/71 event decisions must remain unchanged. Successful original real data will require actual published whole FlyWire-v783 139,255 neurons, 15,091,983 aggregate directed pairs and 54,492,922 original integer synaptic contacts, all original array hashes and source BC01 digest unchanged.

## First synthetic evidence: negative, nonbiological

[Successful synthetic-only GitHub Actions 38023927792](https://github.com/Azimn/Pretorius-Connectome/actions/runs/38023927792) has passed its local source/model integrity tests and eight-arm capacity simulation on an **artificial 8192-neuron generated numerical graph**, not original FlyWire-v783. The original dual-trace **β1 identified 5/16 early original source records after 16 learned memories, then 2/16 after all 317**; dual-trace **β4 went 4/16→3/16**. Original Pilot14 single protected β4 baseline had **4/16 after all 317**. The rewired dual β1 had 9/16→3/16. The existing single-slot and new two-trace nonneural comparators both reached 0/16 early IDs at full source memory load. This synthetic result does **not** support a dramatic dual-trace improvement in retention, but it is primarily a software/control precondition. The full biological-source run was downloading/verifying original published whole-FlyWire v783 at the time of this entry.

## Falsification and completion gates

A successful dual-trace neural result must retain early identities **AND** improve newest 16 source memories compared with Pilot14's failed β4 newest-learning result, preserve positive own-source content margins, beat shuffled/rewired and paired **101,840 numeric-slot** nonneural comparator on meaningful measures, and avoid substantially worse absent-event false acceptance. Also report 159 familiar-cue and 31 never-trained fourth source cue correctness **even if they remain poor**, without post-hoc β, rate or decay tuning.

Only the original successful, publisher-source-verified whole-v783 job counts as real fly-topology numerical evidence; an Actions synthetic job is NEVER a biological result. Exact original source case JSON, all **eight trained source numerical NPZ files**, original graph/source SHA, dual exposure counters, comparator masks, and source-ID-preserving historical parity must be permanently committed by the separate successful MAIN GitHub archive workflow. Before its completion, archive status is PENDING. Update central [PRJ-038](https://github.com/Azimn/Artificial-Life-Research-Journal/blob/main/projects/PRJ-038-Pretorius-FlyWire-Connectome.md), cumulative journal and original model evidence register with both nulls and effects.

There is no proof here of fly-like learning physiology, a conscious fictional doctor, autobiographical natural-language recall, reliable novelty rejection, cross-model identity, or reliable unseen human-semantic paraphrase transfer. Model-only inference still emits a 256D numeric signal; event identity and memory text remain absent from the network.
