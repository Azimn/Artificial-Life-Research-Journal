---
id: JRN-2026-10-08-03
title: "FlyWire Pilot13: Synaptic Memory Capacity and Interference"
type: journal-entry
status: active experimental, original real FlyWire test pending
updated: 2026-10-08
projects:
  - PRJ-038
research_questions:
  - RQ-001
  - RQ-003
  - RQ-006
---

# 2026-10-08: Pilot 13 — does later memory overwrite earlier synaptic association?

This is the next falsifiable phase in the [Pretorius-Connectome](https://github.com/Azimn/Pretorius-Connectome) research lineage, not a new independent character prototype. Original FlyWire v783 synaptic imprint Pilots08–12 yielded bounded content-specific *trained-literal-cue* associations, but failed to recover genuinely novel source cues; plugging in frozen pretrained MiniLM semantics did not rescue recall, and the original fly topology did not outperform a fixed-degree rewired control in Pilot12's single-seed comparison. See the preceding [source-grounded cumulative journal entry](2026-10-08-flywire-direct-synaptic-imprint.md).

## Question and preregistered intervention

Is the repeated failure driven partly by **synaptic memory interference**, where learning additional Pretorius source memories reduces the neural readout's ability to discriminate previously learned content, or is the readout poor from the first exposure? [Pilot13 protocol](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/flywire-pilot13-capacity-interference/docs/FLYWIRE_DIRECT_IMPRINT_PILOT13.md), [implementation PR #27](https://github.com/Azimn/Pretorius-Connectome/pull/27), and [research tracker #17](https://github.com/Azimn/Pretorius-Connectome/issues/17).

Reuse the version-pinned original 450 reconstructed v12 first-person memories, 27 episodes, original BC01 256D signed lexical features and source-linked canonical L1, with exactly 317 fixed seed31 training events, 159 prior positive probes, 62 validation-absent and 71 test-episode absent cases. Learning stages are exactly **0,16,32,64,128,256,317 source autobiographical events**, three original first/middle/last cue presentations per memory at rate0.7/3. Compare four arms: original fly-directed edges correct source/target pair, degree-preserving rewired eligible synapses correct pair, original edges deranged targets, rewired edges deranged targets. The candidate memory-ID universe remains **317** at every stage, rather than getting easier when only 16 memories have been trained. The model itself accepts cue-only input and emits numerical BC01 vectors, never an event ID or autobiographical narrative.

Measure source-owned first 16 early anchor memories at every stage, newest 16 memories, not-yet-trained near-future 16 memories, currently trained intersection of prior 159 positive probes, and exactly 71 always-absent episode test probes. Track source ID, external-oracle top1, own-target cosine, highest competing target cosine, source-target margin, neural response, learned synapse count, original acceptance and diagnostic known-versus-absent AUROC. Retain source IDs *only in the offline evaluator*, not neural inference. The real-v783 terminal original arm must reproduce byte-identical entire previously learned Pilot10 delta array and original source case decisions.

## Preliminary synthetic engineering study, not biology

[Successful nonbiological synthetic CI run 37874513816](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37874513816), full synthetic [source experiment report](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/flywire-pilot13-capacity-interference/results/imprinting/PILOT13_SYNTHETIC_PROVISIONAL.md). This used an **artificial 8,192-neuron, degree-16 aggregated directed graph**, explicitly not the 139,255-neuron original FlyWire connectome.

| Training-event load | Original synthetic correct early anchor IDs (N=16) | Degree-preserving rewired synthetic (N=16) | Wrong-target original control (N=16) |
|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 |
| 16 | **5** | **10** | 0 |
| 32 | 5 | 8 | 0 |
| 64 | 5 | 5 | 0 |
| 128 | 4 | 2 | 0 |
| 256 | 0 | 2 | 0 |
| 317 | **1** | **2** | 0 |

The external 317-memory evaluation pool and original early anchor event IDs remained unchanged. Among the original biological-unrelated *synthetic* anchor memories correctly recognized after the first 16 exposures, the original synthetic arm **lost 4 of its 5 initially correct**; the rewired synthetic arm **lost 8 of its 10 initially correct** and neither arm gained new correct anchors. Mean signed correct-source target-vs-strongest competitor cosine margin fell **−0.020592 to −0.146269** for the original synthetic graph, **+0.014098 to −0.169297** for rewired. This is a direct within-event synthetic interference signal rather than a result of changing candidate pool size. However, it is NOT a claim about the real fly topology, source-grounded semantics, human forgetting, or autonomous character memory.

## Original biological source completion gates

The [original whole FlyWire v783 Pilot13 CI](https://github.com/Azimn/Pretorius-Connectome/actions/workflows/flywire-pilot13-capacity.yml) separately retrieves and verifies the publisher's 139,255 root IDs, 15,091,983 aggregate directed synapse edges, 54,492,922 integer contact counts and all original source CSR hash digests. It reruns all four arms at all seven memory loads and **fails** unless the final original real learned state is exactly the frozen Pilot10 numerical synaptic delta array and its prior 159 source-positive / 71 absent event-ID results. Full per-stage case JSON and four source-bound synaptic weight files must be archived permanently after successful real CI; the [program journal](https://github.com/Azimn/Artificial-Life-Research-Journal) gets a separately verified result addendum. Until actual whole-v783 CI passes, **only the synthetic observation is available**.

## Mechanistic interpretation and decision rule

Memory-specific target margin falling as more unrelated memory events are stored suggests overlapping feature-neuron routes, overwriting/cancellation, inadequate output separability or shared synaptic resource competition. It **does not identify a single cause on its own**. An early negative margin at the first 16 trained events would indicate baseline interference/decoding trouble before scale-up, even when later forgetting also occurs. An original-vs-rewired difference that is small, or a similar decay under shuffled targets, would limit attribution to fly-specific anatomy or learned event identity. Follow with an independently preregistered Pilot14 changing source-to-readout capacity/learning mechanism and comparing a parameter-matched non-neural supervised mapping before altering frozen Pilot13 based on its test outcomes.

No real neural fly lived the fictional narrative; all autobiographical source materials are reconstructions. The source-to-event ID is an EXTERNAL diagnostic oracle and no autonomous Pretorius identity, conscious history, semantic autobiographical recall, or definitive final character has been produced.

## Addendum: first successful actual whole-brain FlyWire-v783 result

**Actual publisher-verified original full FlyWire-v783 result (NOT synthetic):** [successful GitHub Actions run 37874735426](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37874735426) produced complete source-linked seven-stage four-arm case JSON, SHA-256 cad7e249f23e650705e412964a698395b6a262872fbbace2ee4894d16ecfe617. The [real measured source report](https://github.com/Azimn/Pretorius-Connectome/blob/experiment/flywire-pilot13-capacity-interference/results/imprinting/PILOT13_REAL_V783_PROVISIONAL.md) is committed in the owning project branch and will be integrated into main after independent verification. Original four complete biological anatomy CSR array hashes, 139,255 neurons, 15,091,983 directed neuron pairs, 54,492,922 integer synaptic counts were unchanged.

**Unlike the synthetic fixture, actual early low-load real FlyWire source association was very strong:** the same first 16 training-order source events produced **15/16 correct event IDs** after source-memory load16, but only **4/16** survived after training all 317 original reconstructed autobiographical source memories. **11 of the originally correct early source events became incorrect, with 0 gains.** The binary-degree-preserving rewired whole-brain null analogously declined **15/16 → 3/16**, losing 12 originally correct source events with no gains. The original network's mean early-event correct-target minus top competing target cosine margin fell **+0.123541 → −0.124323**, with rewired **+0.141133 → −0.100605**. The original correct-pairing model's changed source synaptic slots grew **3,382 at 16 events → 28,938 at 317 events**. At every stage, the external 317-event source target candidates and early 16 source identities were held fixed; the observed loss is not explained by a changing candidate-set denominator.

**Independent source/target pairing control:** both original and rewired deliberately deranged content-pairing neural conditions identified **0/16** original anchors at load16 and at load317, weakening a cue-collision-only explanation of early above-control source identification. Original old acceptance threshold falsely accepted **37/71** episode-absent questions at load16 and **56/71** after full 317-memory load, while the terminal original 159 known-positive probes matched prior Pilot10 **20/159** correct source event IDs. In the successful source run, the final trained original signed edge delta array and saved checkpoint bytes were **exactly identical** to the original real Pilot10 weights, with identical historical 159 known and 71 absent per-case decisions.

**Reproducibility qualification:** another original-full-v783 workflow [run 37874513816](https://github.com/Azimn/Pretorius-Connectome/actions/runs/37874513816) failed the stringent frozen Pilot10 numerical checkpoint parity check, while the independently completed 37874735426 run passed it. An instrumented real replay is testing exact edge support, source imprints and possible last-digit floating variation. The earlier failure is documented, not discarded; until validated, report this as an actual successful original v783 source run with outstanding repeatability qualification, and do not mark its permanent main archival complete.

**Mechanistic conclusion:** substantial *interference/competition between source-memory associative signals during cumulative imprinting* is supported within this cue-only source-signed BC01 one-hop synaptic model. The original fly topology does not visibly protect early associations relative to a binary-degree matched rerouting null in the same single-seed source data. This is numerical event association with an **EXTERNAL fixed 317-vector oracle evaluator**, not fly physiological forgetting, independent semantic source recollection or autobiographical subjecthood. The next separately versioned phase should isolate learned weight interference from readout bottlenecks and compare matched nonbiological learned mapping, while preserving source and prior pilot evidence.
