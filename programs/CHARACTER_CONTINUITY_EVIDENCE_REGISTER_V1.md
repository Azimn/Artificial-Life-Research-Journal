---
id: PROGRAM-CONTINUITY-EVIDENCE-001
title: Character Continuity Evidence Register v1
type: evidence-register
status: active
updated: 2026-10-08
---

# Character Continuity Evidence Register v1

The [machine-readable source pin manifest](CHARACTER_CONTINUITY_SOURCE_PINS_V1.json) records exact repository commit SHAs and Git blob SHAs for all ten evidence-register entries. Its immutable report URLs prevent later README or result edits from silently changing the evidence basis of this initial synthesis. The manifest authenticates source-file identity, not independent experiment validity.

## Reading rule

These are repository-reported exploratory findings inspected on 2026-10-08, not a pooled meta-analysis. Several studies reuse the same fictional autobiography, previously examined test prompts, correlated seeds, and author-generated labels. Do not aggregate percentages across tasks or treat them as independent replications. Follow the linked reports and exact run artifacts for source of truth. A result status of "negative" means its own tested claim was not established, not that a whole family of architectures has been falsified.

| Evidence ID | Source and result | What is directly supported | Limit and competing explanation | Program consequence |
| --- | --- | --- | --- | --- |
| CC-E01 | [NN Experiment 001, Identity Surgery](https://github.com/Azimn/Pretorius-Neural-Network/blob/main/EXPERIMENT_LOG.md): decoder-swap JS 0.8546 vs intact 0.8545; trained recurrent plus virgin decoder 0.7791 | Under default v0.3 training most measured phenotype followed learned decoder | Specific decoder, runner, reward and test distribution; says nothing universal about neural weights | Require decoder transplant and recurrent-only readout in substrate claims |
| CC-E02 | [NN Experiment 004](https://github.com/Azimn/Pretorius-Neural-Network/blob/main/EXPERIMENT_LOG.md): bounded-plasticity recurrent-only signal, full-scale example validation JS 0.7784 to 0.8009 | Direct recurrent-only phenotype signal is possible in this implementation under modified plasticity | Modest, task-specific signal; train/validation generality limited, untested continuity after long interruptions | Reject the universal claim that the network never learns; replicate under independent tasks and lesions |
| CC-E03 | [BioCircuit BC01-D6A](https://github.com/Azimn/Pretorius-Neural-Network/blob/main/results/biocircuit/BC01_D6A_RESULTS.md): output decoder 18.75% original withheld-card, 20.14% authored rephrase, four-way chance 25%; recurrent learned-W lesion unchanged | Earlier decoder-only 100% was in-sample; no measured heldout-card recurrent advantage | Tiny 16-card, transductive, unreviewed paraphrases, episode/background feature exposure | Finish source- and episode-disjoint D6 with independent review; do not transplant D5B decoder |
| CC-E04 | [Connectome Pilot 03](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT03_RESULTS.md): 77.9% IDF-trigram vs 27.1% legacy hash on word-swapped cues | Cue representation greatly changes constrained lexical identification | Not semantic paraphrase transfer; 30.6% false acceptance, external codebook | Prioritize representation and joint recall/rejection measures, not higher synapse count |
| CC-E05 | [Connectome Pilot 04](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT04_RESULTS.md): 0% correct-and-accepted on 68 authored paraphrase/contradiction challenges | Tested hashed cue-to-fingerprint conditions failed these low-overlap authored semantic probes | Not blind or human reviewed; lexical overlap about 1.87%; no narrative semantics in targets | Design independent content-grounded cues and reviewer adjudication |
| CC-E06 | [Connectome Pilot 05A](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT05_RESULTS.md): BM25 16.4% true correct-and-accepted; 62.7% contradictions falsely accepted | Full-text external retrieval improves event matching relative to tested opaque neural assay but lacks truth verification | Post-hoc reused challenge; source access differs by architecture; unfair to claim equal-resource superiority | Separate candidate retrieval, evidence finding, and claim verification |
| CC-E07 | [Connectome Pilot 07A](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/imprinting/PILOT07_RESULTS.md): NLI top-three 1.67% true correct-and-accepted; 0% contradictions accepted | Frozen local NLI reduces false acceptance chiefly through abstention | Does not establish useful recall or calibrated truth checking; reused unreviewed challenge | Report coverage as well as false-acceptance and source correctness |
| CC-E08 | [FlyWire MB trace plasticity](https://github.com/Azimn/Pretorius-Connectome/blob/main/results/associative/FLYWIRE_MB_PLASTICITY_PILOT01_RESULTS.md): trained original 7/67, frozen original 7/67 accepted-correct; learned rewired 3/67 | No isolated benefit from added learning in the tested mushroom-body topology | Post-hoc correlated challenges, lexical feature mapping, rewiring null not fully cell/weight matched | Do not claim a plasticity advantage; topology difference must be separated from learning effect |
| CC-E09 | [Attractomancy current status](https://github.com/Azimn/Attractomancy/blob/main/docs/COLLECTION_READINESS_2026-10-08.md): 444 catalog entries and 24 indexed procedures | A substantial provenance-oriented collection and intervention index exists | Neither 444 independent validated sources nor completed causal conditioning tests; capture gaps remain | Finish high-value source capture and freeze one matched intervention |
| CC-E10 | [The Doctor Lives](https://github.com/Azimn/The-Doctor-Lives/blob/main/README.md): v0.4 state-to-policy bridge and opt-in v0.5 neural convergence documented | A production subject architecture integrates recurrent policy and persistent state under explicit migration gates | Functional integration is not blinded proof of autobiographical generalization; release validation is separate | Keep production moving, make causal components auditable and opt in only |

## Cross-project synthesis

**Observed recurring limitations:** weak transfer from lexical similarity to paraphrased source meaning, failures to prove recurrent changes are causally responsible, decoder or retriever success without independent generalization, and overly aggressive false-claim abstention.

**Viable alternate explanations:** cue information loss, inappropriate synaptic credit assignment, inadequate readout, target-label weakness, evaluated-data reuse, missing semantic evidence checking, asymmetric access to narrative text, and insufficiently matched computational budgets.

**Not supported:** all continuity resides externally; biological topology can never help; weights never encode behavioral structure; current external retrieval solves identity; existing fiction proves historical autobiographical truth.

**Program conclusion:** Test the interaction among persistent record, cue representation, verifier, recurrent learning, and downstream decision policy. Preserve all legacy results unchanged and preregister fresh tests rather than retroactively grading old ones.

## Update protocol

Add a numbered CC-E identifier for a materially distinct finding, its original repository report URL, immutable commit/blob and raw-case artifact where available, measured outcome and denominator, exact claim boundary, confound, and resulting action. If a prior interpretation changes, append a correction with date and reasoning. Do not silently edit source-repo measured claims. A periodic synthesis is not a new independent experiment.

## Independent evaluation requirement

The common confirmatory test does not yet exist. Pilot 04 and BioCircuit D6A remain exploratory. The first new benchmark must be independently authored and adjudicated, frozen before any candidate tuning, and evaluated with true source support, targeted contradictions, unrelated and never-seen events, and meaningful abstention versus coverage tradeoffs.

## 2026-10-08 CC-E01 provenance audit: reproduction not yet established

The original Experiment 001 numbers in CC-E01 above remain *repository-reported narrative findings*, not independently replayed six-seed results. [Pretorius-Neural-Network commit `2f7c698b5a887325cefd52609df746112bdabd6f`](https://github.com/Azimn/Pretorius-Neural-Network/commit/2f7c698b5a887325cefd52609df746112bdabd6f) merges a pinned reconstruction runner, verified source-manifest hashes, five passing mechanical tests, and [a source-blocked run report](https://github.com/Azimn/Pretorius-Neural-Network/blob/2f7c698b5a887325cefd52609df746112bdabd6f/results/chimera_001/RUN_REPORT.md). It is **an implementation/provenance upgrade only**, not a numerical reproduction upgrade.

Canonical original v1 training (100 axis-grounded plus 30 legacy), validation (40) and adversarial (20) source files remain unavailable. A file with the historical adversarial filename in a preservation branch failed the manifest's SHA-256 and was explicitly excluded; the historical phenotype profile alone was verified byte-for-byte. The original Experiment 001 hyperparameter overrides and exact 130-item presentation order are also not fully evidenced by the narrative log. The runner's no-data preflight correctly refuses to generate per-seed metrics; the terminal battery remains sealed. **Do not write "reproduced from pinned config" for CC-E01 until six actual per-seed JSON results, the four-condition ±0.01 gate, and an immutable successful results commit exist.** The fresh-decoder control must include a matched virgin recurrent + trained fresh decoder comparator to distinguish generic supervised decoding from recurrent-specific learned representation.
