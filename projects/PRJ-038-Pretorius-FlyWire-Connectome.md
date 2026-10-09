---
id: PRJ-038
title: "Pretorius Connectome: FlyWire, Imprinting, and Vector Fly"
type: project
status: active experimental
updated: 2026-10-08
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
repos:
  - https://github.com/Azimn/Pretorius-Connectome
---

# Pretorius Connectome: FlyWire, Imprinting, and Vector Fly

## Research question

Can source-grounded autobiographical associations be learned in a synthetic or biologically inspired neural topology, and does verified fly connectivity provide value beyond shuffled, rewired or non-neural retrieval controls?

## Research components

The [Pretorius Connectome](https://github.com/Azimn/Pretorius-Connectome) owns the pinned 450-event reconstructed v12 autobiographical corpus across 27 episodes, feature caches, synthetic Hebbian imprinting experiments, real FlyWire v783 graph-constrained retrieval studies, neural plasticity overlays, and the separate Vector Fly SQLite sparse retrieval database/API. Reconstructed events are fictional evidence artifacts, not lived character memories.

Pilot 01 learned synthetic cue-to-opaque-fingerprint associations and required a decoder codebook. Pilot 02 exposed lexical fragility and absent-memory rejection problems. [Pilot 03](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT03_RESULTS.md) increased swapped-cue event identification from about 27.1% to 77.9% through lexical feature engineering, while false acceptance remained material. [Pilot 04](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT04_RESULTS.md) failed to transfer to genuinely rewritten incident questions (0% correct-and-accepted on that authored challenge). Pilots 05 through 07 tested full-text BM25 and an additional local NLI verifier; the verifier largely rejected legitimate questions along with contradictions.

[Frozen FlyWire comparisons](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/associative/README.md) tested whole-brain and mushroom-body configurations and rewired controls. Later [mushroom-body plasticity](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/associative/FLYWIRE_MB_PLASTICITY_PILOT01_RESULTS.md) produced no isolated gain from training (7/67 correct-and-accepted in both learned and frozen original MB conditions). Do not attribute differences between original and rewired graphs to training.

## Data reuse, independence, and tooling

The shared source-owned L1 450-event archive and deterministic lexical L2 v2 cache are consumed by BioCircuit through an architecture-specific feature adapter, not shared neural weights. [Vector Fly](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/VECTOR_FLY_DATABASE_V1.md) exposes local source-linked sparse retrieval and a read-only API, which is an engineering deliverable, not a demonstrated semantic autobiographical memory.

## Scientific interpretation

A recurring cue representation and claim verification bottleneck has been measured under reused, assistant-authored, unreviewed prompts. No one should report a successful synaptic identity implant, validated FlyWire plasticity advantage, source-grounded semantic recall, or independence of overlapping tests. Keep source hash, split-specific encoding and exact case-level evidence at this project's GitHub home.


## Real original-FlyWire direct synaptic imprint update (2026-10-08)

[The cumulative source-linked research journal entry](../journal/2026/2026-10-08-flywire-direct-synaptic-imprint.md) reconciles numerical learned-edge and novel-cue evidence across original real whole-brain Pilots08–11. Frozen Pilot08 synapses recalled 46/159 source events from the **trained input** but 0/159 from a distinct untrained cue; Pilot10's explicit three-source-cue imprint identified 20/159 from a last cue that was **trained**, still falsely accepting 56/71 absent events. Pilot11 reloaded unchanged Pilot10 original weights and identified **0/31** genuinely untrained source fourth cues, while a separately validated strict acceptance gate lowered absent false acceptance 56/71→5/71 but correct accepted recall 18/159→0/159. These are exploratory externally oracle-decoded 256D lexical-vector associations on actual immutable original biological FlyWire edges, **not autonomous autobiographical recollection**.

[Current Pilot12 PR #26](https://github.com/Azimn/Pretorius-Connectome/pull/26) separately compares a frozen local pretrained sentence-cue encoder against original lexical hashing on both original v783 biological wiring and binary-degree-preserving double-edge-switched readout connectivity, plus shuffled target controls. Its synthetic preliminary negative result is **not biological evidence**. The independent real original whole-FlyWire six-arm run subsequently succeeded: original BC01 **20/159** familiar trained cue event matches versus **21/159** on the binary-degree-preserving rewired original graph; frozen pretrained MiniLM input scored **0/159** vs **1/159** on corresponding real/rewired controls. **All six variants scored 0/31 on genuinely unseen fourth source cues** despite MiniLM increasing cue-feature overlap (no own-event active feature overlap dropped from 30/31 under BC01 to 5/31 under MiniLM). The [measured real-v783 Pilot12 report](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT12_REAL_V783_PROVISIONAL.md) gives the exact original workflow and source case SHA. The [journal result addendum](../journal/2026/2026-10-08-flywire-direct-synaptic-imprint.md) preserves original/rewired and false-rejection caveats. The fully permanent original-case and checkpoint archive requires a separate successful postmerge Actions pass. The [project scorecard](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/FLYWIRE_DIRECT_IMPRINT_PROGRAM_SCORECARD.md) and original source JSONs/learned checkpoint digests are held at the owning repository. Test novel cues, false acceptance, encoded prior versus learned weights, and topology-specific effects as separate, falsifiable questions.

## Vector Fly retrieval and cross-project renderer tests (2026-10-08)

The project has a source-pinned [450-reconstructed-memory SQLite lexical vector index](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/vector_fly/VECTOR_DATABASE_V1_RESULTS.md) with a separately scoped 317-event train-only index and a [read-only HTTP API](https://github.com/Azimn/Pretorius-Connectome/blob/main/docs/VECTOR_FLY_AGENT_API_V1.md). This is data interoperability and exact TF-IDF retrieval, **not a semantic embedding or biological wiring advantage**.

The API was consumed by the genuine production Pretorius brain in [The Doctor Lives Stage 01](https://github.com/Azimn/The-Doctor-Lives/blob/main/results/vector_fly/PILOT01_RETRIEVAL_INTEGRATION_RESULTS.md), then by a [twelve-response local-Ollama Stage 02 test](https://github.com/Azimn/The-Doctor-Lives/blob/main/results/vector_fly/STAGE02_REAL_OLLAMA_DIALOGUE_RESULTS.md). Four of six retrieval/no-retrieval outputs changed, but several contained fabricated or conflated facts. No real-vs-rewired FlyWire reranker was used in that dialogue test. Consult the [cumulative journal entry](../journal/2026/2026-10-08-vector-fly-to-definitive-pretorius.md); keep original topology research and the semantic/source evaluation separate.
