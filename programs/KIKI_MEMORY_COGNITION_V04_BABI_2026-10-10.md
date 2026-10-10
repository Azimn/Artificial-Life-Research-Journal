# Kiki Memory-to-Cognition v0.4: public bAbI QA and the multi-hop retrieval null

**Research date:** 2026-10-10  
**Implementation:** [Azimn/Kiki-Mind PR #10](https://github.com/Azimn/Kiki-Mind/pull/10), **merged** into Kiki Mind `main` at exact commit `bfc283bc9fd5ba6896a2bef835093606e30f63bb`.  
**Completed CI:** [original run 38060905490](https://github.com/Azimn/Kiki-Mind/actions/runs/38060905490), [final-head benchmark 38061113629](https://github.com/Azimn/Kiki-Mind/actions/runs/38061113629), and [final-head original Kiki regression 38061113654](https://github.com/Azimn/Kiki-Mind/actions/runs/38061113654) all passed. Full original Kiki regression, prior v0.1-v0.3 integration gates and new v0.4 unit tests passed. Final verified PR head was `0471efecdb86c7c612c01007889fbc7a8cb69896`.  
**Original benchmark:** Weston et al. (2015), [Meta's bAbI tasks](https://github.com/facebookarchive/bAbI-tasks), CC BY 3.0 [HF dataset card](https://huggingface.co/datasets/facebook/babi_qa).  
**Exact public source:** [azreasoners/LLM-ASP revision `642a9ade9c92677b970b1bc9921cafb0764d2ed7`](https://github.com/azreasoners/LLM-ASP/tree/642a9ade9c92677b970b1bc9921cafb0764d2ed7/bAbI/data), qa1 Git blob `8f9586848f7b0afdccb25328feeb04d561c31756`, qa2 `6deccd0cf07947ff525839a7b4643c6e0afe1b92`, qa6 `da25e9fd5bb7d69c7150b208051b1413fd91ff2b`. Source bytes and upstream commits are verified before any test results are calculated.  
**Shared port pinned source:** Pretorius-Connectome `cc82c72167d87c19f16125ccdf9477b53c777878`.

## Hypothesis and design

The prior synthetic v0.3 trial scored 36/36 on self-authored structured questions with a supplied oracle intent. This v0.4 trial removes oracle-structured question intent and uses 120 **externally authored** public benchmark questions (first 40 test questions in each task qa1, qa2 and qa6), no model/API call and no precomputed parser hints. Questions are still from a narrow, publicly familiar template dataset and evaluated by fixed hand-coded English movement, possession and yes/no rules, **not independent blind language understanding**.

Each test question has a disposable real Kiki EventLedger containing *only prior story facts* as synthetic external **source receipts**. Source owner, source blob, event ID, temporal prefix, version and hash are pinned. The bridge returns candidate-only external evidence, never a newly lived memory. Gold answers/supporting IDs are read only in scoring after the answer and citations are fixed.

Compare original full prior context, no context, random five preceding facts, native lexical ranked top five, and the identical ranked facts through shared MemoryCognitionPort.

## Actual fixed-slice findings

| Condition | QA1 single fact /40 | QA2 two-fact /40 | QA6 yes/no /40 | All /120 |
| --- | ---: | ---: | ---: | ---: |
| No context | 0 | 0 | 0 | 0 |
| Full story prefix | 40 | 40 | 40 | 120 |
| Random five source facts | 34 | 9 | 32 | 75 |
| Native source top-five lexical | 40 | **0** | 40 | 80 |
| Same candidates through port | 40 | **0** | 40 | 80 |

Mean official required-support recall for the shared port was qa1 1.00, **qa2 0.50**, qa6 1.00; the reader abstained on all 40 qa2 cases. The **full-context** condition succeeded on all QA2 cases *with the same parser*, locating the failure at the insufficient memory selection step rather than a demonstrated inability of this narrow rule interpreter to track objects across two observed facts. Candidate relevance is not enough when the support spans linked events about two different entities. A controlled first-hop lexical retriever primarily matching the object does not necessarily include later movement by its human carrier. This last causal explanation is plausible, not separately experimentally proven; the trace-level empirical evidence is the required-support recall failure.

**Strong port null:** native ranked and shared-port ranked predictions, candidate IDs and cited record IDs were **identical for all 120**. The port provides an invariant provenance/source interface, not better reasoning. Random five facts answered 9/40 QA2 questions despite single-hop ranking obtaining 0, underscoring the ranking failure rather than supporting a simple `more retrieval` claim.

**Source safety:** all six recorded source/identity/temporal checks passed: wrong-owner rejected, revoked token rejected, future line absent, scope restricted to current story prefix, stale source rejected after a post-scoring synthetic append, and the isolated append modified only the scratch database after the scored interval. No private Kiki data, real canonical history, Calibos thoughts, Pretorius autobiographies or neural weights touched. Default Kiki tests and prior cognition-port tests passed in the full CI job.

## Reproducibility

[Fixed source and question protocol](https://github.com/Azimn/Kiki-Mind/blob/experiment/cognition-v04-external-babi-qa/experiments/cognition_port_v04/PROTOCOL.md), [public source adapter](https://github.com/Azimn/Kiki-Mind/blob/experiment/cognition-v04-external-babi-qa/experiments/cognition_port_v04/source.py), [non-oracle reader](https://github.com/Azimn/Kiki-Mind/blob/experiment/cognition-v04-external-babi-qa/experiments/cognition_port_v04/reader.py), [runner](https://github.com/Azimn/Kiki-Mind/blob/experiment/cognition-v04-external-babi-qa/experiments/cognition_port_v04/run.py) and [report](https://github.com/Azimn/Kiki-Mind/blob/experiment/cognition-v04-external-babi-qa/experiments/cognition_port_v04/RESULTS.md) remain executable in CI without downloading a neural model. Full per-case machine output is archived by the Actions workflow; timing and candidate budgets are reported but must not be used as evidence of a speed or semantic gain.

## Scientific next step

Do not change v0.4's already observed outcome. Create a separate preregistered **two-hop evidence-chain retrieval v0.5** on a fresh, uninspected external benchmark slice (e.g., test ordinals **201-240** at the same upstream pin). Infer a holder from retrieved object evidence, then retrieve the holder's movements with a fixed overall source budget, comparing the original one-shot ranking, native vs port identical-evidence, random fixed-budget and full-context conditions. Include owner-swap/rumor provenance failures and all case-level citations.

**Interpretation boundary:** even successful learned or rule-based retrieval on bAbI is not equivalent to character identity continuity or human autobiographical cognition. Issue [Kiki Mind #8](https://github.com/Azimn/Kiki-Mind/issues/8) remains open for independent authoring/grading and more naturalistic language/continuity tasks.

**Follow-on tracking:** [Kiki Mind Issue #11](https://github.com/Azimn/Kiki-Mind/issues/11) freezes new public benchmark ordinals 201–240 for bounded evidence-chain retrieval; [Issue #8](https://github.com/Azimn/Kiki-Mind/issues/8) stays open for independent semantic validation.
