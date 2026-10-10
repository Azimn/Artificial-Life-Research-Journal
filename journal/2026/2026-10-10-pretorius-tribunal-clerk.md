---
id: JRN-2026-10-10-01
title: "Pretorius Tribunal of Memory: the Clerk, isolated retrieval, and source-version invalidation"
type: journal-entry
status: exploratory-model-runs-complete-with-versioned-software-gate
date: 2026-10-10
updated: 2026-10-10
research_questions:
  - RQ-001
  - RQ-006
tags:
  - typed-memory-extraction
  - provenance
  - isolated-vs-joint-context
  - versioned-memory-cache
  - causal-ablation
  - controlled-negative-results
---

# October 10: E3-T1 Clerk and Private Clerk

## Motivation from E2 and E3-C

D1 and E1 found no observed editorial-symbol benefit over information-identical neutral keys. E2 showed that a plausible "Pretorius-consistent" answer may be available **without any autobiographical memory**; E2F's 1.5B model matched author-preferred choices 12/12 with no memory and 11/12 with two selected L1 events. Corrected E3-C v2 then balanced a deterministic two-source output against counterfactual input flips, with synthetic PRETORIUS_SANDBOX records isolated from the canonical autobiography. Two Qwen sizes and independent SmolLM2-1.7B all failed 0/6 complete paired counterfactual reversals in direct forced-decision mode.

This sequence motivated separating *source fact reading* from *decision-rule execution*. The two new experiments and source-attested software module are hosted in [Attractomancy E3](https://github.com/Azimn/Attractomancy/tree/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY), with all original model outputs and pinned model revisions preserved.

## First intervention: T1 joint typed facts

[Joint Clerk protocol](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/CLERK_PROTOCOL.md) and [completed results](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/CLERK_RESULTS.md): ask the renderer to extract two fields in one strictly parsed JSON object after source admission and identity checks. Each field is checked against an exact source clause from its corresponding synthetic record. Only if both fields are source-attested does ordinary deterministic software compute the case's action.

Across **24 distinct model extraction prompts per model**, correct source-attested two-field extracts in the 12 full-record cases were: Qwen2.5-0.5B **3/12**, Qwen2.5-1.5B **9/12**, SmolLM2-1.7B **4/12**. These corresponded to the same counts of correct permitted post-gate actions and **1/6**, **3/6**, **1/6** fully correct counterfactual pairs, respectively. The 1.5B joint-extraction interface produced more correct output than its direct forced-choice 6/12, but the two tasks and prompts differ and the rule execution is software, not learned model reasoning. Failed field attestation returned UNKNOWN; perfect *software* refusal of missing evidence is not correct model abstention. Qwen1.5B correctly supplied a required \`null\` for a missing second record in 4/6 first-record-only prompts; the other two models scored 0/6.

The first model-run attempt failed before any inference because a \`save\` helper was missing. That error was fixed and the complete new workflow was run; no failed-run generations were substituted as successful research data.

## Second intervention: T1B source-isolated Private Clerk

The [Private Clerk protocol](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/ISOLATED_PROTOCOL.md) freezes each field extraction to **one distinct verified source record**. The same twelve independent local fact records (three rule families × two first values × two second values) are each read once/model; their correctly attested outputs are reused in twelve different synthetic counterfactual combinations. The policy combination requires no new model inference. Results are in [the original T1B report](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/ISOLATED_RESULTS.md).

| Model | Direct forced 12-state answer | Joint extractor + software, correct of 12 | Isolated extractor + cached software, correct of 12 | Isolated fully correct flip pairs of 6 |
| --- | ---: | ---: | ---: | ---: |
| Qwen2.5-0.5B | 5 | 3 | **10** | **5** |
| Qwen2.5-1.5B | 6 | **9** | 6 | 2 |
| SmolLM2-1.7B | 5 | 4 | **8** | 3 |

Per-record extraction achieved **11/12**, **8/12**, **10/12** strictly correct source values respectively. Qwen0.5B's only failed value was the actual correct source seal ASH output as lowercase \`ash\`, which the preregistered strict uppercase checker rightly refused; a post hoc normalization may be investigated separately but must not rewrite this score.

**Positive architectural lead, not a general improvement:** The smaller Qwen and SmolLM2 benefited from record-local field extraction, while Qwen1.5B was more successful when shown two records together. Thus a **renderer-specific, replaceable extraction interface** is more defensible than imposing one hardcoded attention/memory layout on all agents. It is inappropriate to select each model's best arm on these twelve already observed cases and report independent confirmation without held-out validation.

**Token economics:** T1B took only 12 distinct model calls per model, with exact total model tokens **3,625, 3,609, 4,163** respectively, then reconstructed 12 counterfactual decisions from cached source values. This is an artificial high-reuse fixture. If two entirely new source fields must be extracted for each real-world decision, the two isolated inference calls can cost more than one direct decision; realistic per-event reuse, cache turnover, source validation and CPU latency were not measured. The source-only deterministic regex+calculator oracle passes all fixed synthetic cases by construction and must not be counted as character cognition.

## Source-attested SQLite replay and revision invalidation

The [experimental cache](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/verified_fact_cache.py) stores derived values scoped by subject, source, event ID, record revision, source content digest, extractor ID and field schema. It rejects same-version content forks, stale rollback, unsupported extracted values, wrong owners, and mismatched extractor/schema versions. In a synthetic permission drill, a previously admitted \`ALLOW\` source and cached \`KEEP\` amendment were advanced to a new \`REVERSE\` amendment, invalidating the stale field and requiring fresh extraction before the resultant decision became \`DENY\`.

The initial cache test revealed a software bug: the fixed-fixture \`source_field\` utility assumed "record slot 2" always meant "record version 2," so it rejected a legitimate later revision. The cache's field reader was separated from that slot/version assumption; the corrected [CI run](https://github.com/Azimn/Attractomancy/actions/runs/38028840190) passed the replay and all twelve cache tests alongside existing source-guard and Clerk tests. This is ordinary tested software consistency under a trusted synthetic source, not cryptographic proof of authorship or demonstration of a cognitively persistent individual.

## What has not been demonstrated

All T1/T1B sources are artificially authored fixed text with explicit field clauses, not the 450 reconstructed Pretorius autobiography, a real relationship ledger, biological connectivity, or lived post-instantiation experience. The software computes the action whenever it has both attested values; the LLM only extracts literals. The comparisons use different prompt templates, and the factorial twelve decision states reuse only twelve independent source documents. No human-blind relevance scoring, naturalistic decision dependency, validated output-style continuity, or production character deployment has occurred.

The [E3 Tribunal protocol](https://github.com/Azimn/Attractomancy/blob/main/experiments/SCH_E3_TRIBUNAL_OF_MEMORY/PROTOCOL.md) still calls for at least 36 independently authored new dilemmas, three blinded relevance reviewers per case, multiple acceptable jointly sufficient evidence sets, temporal state updates, and cross-family evaluation. That *main* study is **not yet executed**.

**Recommendation:** Preserve immutable source IDs, versioned provenance, source-local fact validation, and a configurable renderer path; build independently labeled real-L1 field targets and measure cold and warm retrieval/decision costs before integrating into Pretorius. Do not infer autonomous personal identity from a synthetic software rule.
