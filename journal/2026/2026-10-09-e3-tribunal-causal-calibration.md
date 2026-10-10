---
id: JRN-2026-10-09-04
title: "E3 Tribunal of Memory: factorial source-necessity controls and blinded annotation infrastructure"
type: journal-entry
status: exploratory-qwen-calibration-complete-independent-family-active
date: 2026-10-09
updated: 2026-10-09
research_questions:
  - RQ-001
  - RQ-006
tags:
  - source-evidence
  - counterfactual-calibration
  - provenance-gate
  - reviewer-blinding
  - experiment-validity
---

# E3 research development: The Tribunal of Memory

The E2 source-grounded Pretorius results gave no evidence that selected autobiographical records improved decisions over model priors: in the forced-choice test, Qwen2.5-1.5B agreed with the author-preferred responses **12/12 without memory** and only **11/12 with the relevant two records**. A new benchmark must make the correct answer depend *causally* on the supplied evidence, instead of rewarding generic cautious or prosocial wording.

## Two deliberately separated tracks

**Synthetic prerequisite calibration:** [E3-C Counterfactual Chamber](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/CALIBRATION_PROTOCOL.md) defines three two-source reasoning mechanisms, all four combinations of two input bits, a balanced output code, editorial/opaque keys, one-source and no-source baselines, and identity-guarded false-owner controls. Each Qwen size runs 84 fresh prompts with original generations, hashes and tokenizer costs retained. This is *not* Pretorius autobiography, and success or failure would demonstrate only literal use of task facts in a small synthetic decision rule.

**Validity discovery:** The first synthetic fixture, **v1**, mistakenly encoded both bits in each source event ID. That allowed the supposedly absent second bit to be inferred from first-record metadata. The original output is preserved and is **not** a valid test of two-record necessity. [A corrected v2 runner](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/counterfactual_calibration_v2.py) hashes each record ID solely from its *own* input bit and checks that the one-source prompt stays byte-identical when the hidden second value flips. New model runs are separately labeled; no v1-v2 results should be silently pooled.

**Reviewer infrastructure:** The [E3 candidate packet tool](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/blinded_packet.py) uses the existing checksum-verified 450-memory Pretorius L1 source and the owner-provided lexical and source-link retrieval to build candidate pools. A calibration workflow successfully produced **127 unlabeled passages across six known E2 dilemmas**. The reviewer file withholds candidate source IDs and retrieval-method labels and does not publicly commit the organizer mapping. These prompts were originally source-informed and are **not** a valid independently authored E3 trial. No human review labels were collected.

A [reviewer schema validator](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/adjudicate.py) requires at least three distinct reviewers per case, complete passage-level judgments, written rationales, explicit minimum evidence sets containing multiple records, and agreement reporting. It refuses incomplete or knowingly source-informed calibration cases. Its ten *synthetic unit tests* passed in CI. This is a validity gate, not an automatic source relevance judge.

## Research context and nonclaims

[LongMemEval](https://arxiv.org/abs/2410.10813) separates extraction, multi-session reasoning, temporal updates and abstention. [EverMemBench](https://arxiv.org/abs/2602.01313) emphasizes multi-party and evolving memory scope. [RFEval](https://arxiv.org/abs/2602.17053) distinguishes apparent correctness from counterfactual causal influence. [TiMem](https://arxiv.org/abs/2601.02845) motivates optional complexity-aware temporal recall. These are design references and have not been tested against Pretorius in the new phase.

The [full E3 Tribunal protocol](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/PROTOCOL.md) still requires 36 independently authored dilemma candidates, at least three independent blinded source-relevance reviewers, multiple acceptable evidence sets, and an independent model-family replication. **It has not been executed.** No canonical Pretorius records, internal neural/connectome state, production memory settings, or real relationship commitments have been modified by these experiments.

## Verified corrected E3-C v2 findings

The corrected [E3-C v2 results](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/CALIBRATION_RESULTS.md) now have original, distinct-run archives from **both Qwen2.5-0.5B and Qwen2.5-1.5B**. Every model generated 84 independent-context responses, and the v2 anti-leak invariance assertions passed before inference. The 0.5B model matched the strictly computed two-bit output in **5/12** complete-source cases under either editorial cues or neutral keys; 1.5B matched **6/12** under either form. Both earned **6/12** with no records at all. Neither model obtained even one of the **six fully correct paired counterfactual flips**. Both produced identical symbolic/neutral responses for **12/12 matched inputs**. These results constitute a negative, corrected-fixture finding for the specific toy conditional inference, not a claim about a full real-world agent's abilities.

The upstream identity guard rejected **12/12** deliberately mismatched synthetic records per model, but their independent language response rules were poor: required UNKNOWN abstention on a one-record-only evidence input succeeded in **0/12** cases for both models; wrong-subject empty-evidence abstention succeeded **0/12** for 0.5B and **4/12** for 1.5B. A typed deterministic authorization gate and a generative explanation/decision renderer therefore remain distinct components.

An [independent SmolLM2-1.7B calibration](https://github.com/Azimn/Attractomancy/blob/main/.github/workflows/sch-e3c-v2-smollm.yml) was scheduled as a real GitHub Actions run, using the same fixed v2 fixture and CPU inference without any paid API. It has **no reported result** until its own data commit and verification are complete.

## Pending update boundary

The original v1 outputs remain preserved but are methodologically invalid for the two-record necessity claim due to cross-bit event-ID leakage. The independent cross-family SmolLM2 extension still awaits source-specific output verification. Do not pool versioned results or substitute the synthetic calibration for E3's unexecuted, human-blinded source relevance experiment.
