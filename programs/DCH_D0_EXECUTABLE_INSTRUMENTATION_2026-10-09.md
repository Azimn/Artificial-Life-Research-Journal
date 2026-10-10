---
id: PROGRAM-CONTINUITY-DCH-D0-002
title: DCH D0 executable synthetic pilot implementation and evidence gate
type: implementation-note
status: instrumentation-verified-no-efficacy
updated: 2026-10-09
research_questions:
  - RQ-001
  - RQ-006
tags:
  - dyadic-continuity
  - partner-replay
  - expert-curation
  - methodological-null
---

# DCH D0: executable instrumentation, not a dyad finding

**Upstream protocol:** [DCH working prospectus v0.2](DYADIC_CONSTITUTION_HYPOTHESIS_V0_2_2026-10-09.md). [Attractomancy draft PR #2](https://github.com/Azimn/Attractomancy/pull/2). **Code snapshot:** [commit e1f1ce62197cfd6d66e0305dc1de2822fd129690](https://github.com/Azimn/Attractomancy/commit/e1f1ce62197cfd6d66e0305dc1de2822fd129690). [Offline CI run 38024933325](https://github.com/Azimn/Attractomancy/actions/runs/38024933325) completed successfully. These references pin the implementation, not the status of the DCH theory.

## Research boundary

The experimental unit proposed by DCH is a distributed historical partner-plus-agent feedback system. A comparison of human-curated memory against a sufficiently capable automatic controller is the crucial challenger. If a well-informed automatic controller reproduces the relevant future behavior under fair budgets, the claim of uniquely human constitution is not supported in that regime, while a general distributed feedback-and-memory claim may survive. A replacement partner's natural dialogue differing from the incumbent's is not a causal result without a matched tape and perturbation-adjusted comparison.

## Executed methods and observations

The upstream package now contains a deterministic 12-case fixture generator, 40 synthetic events per case, twelve conditional-value metadata cards, eight revocable permissions, twelve commitment metadata cards and thirty questions per case, with eight terminal prompts separated into an evaluator-owned JSON file. Four of the eight terminal questions require a permission value plus a domain record; the cards are not all tested as conditional or long-horizon behavior.

Fifteen Python unit tests passed locally. The offline workflow also completed successfully on GitHub Actions. A model-agnostic runner now supports **local Ollama** and optional **Transformers**, alongside a clearly labeled test-only fake renderer. There is a post-intervention evaluator, provenance/authorization checks, transcript capture, no-overwrite behavior and a separate token/record-budget audit.

The deterministic lookup fixture scored oracle 1.00 and cold 0.00 by construction; investigator-coded curators scored 1.00 and 1.00, passive append 0.50, ceremonial no-update 0.25. These numbers arise from the programmed policy and are **not observations of AI partner persistence**. Exact scripted tape replay produced matching hashes; a three-turn synthetic revocation made a scripted adaptive repair score 3/3 against a taped nonadaptive 2/3. This is **engineered fixture sensitivity**, not a measured human, dyad or real LLM effect.

## Open gates

No actual model generation, human Scribe, continuing/live partner, replacement partner, genuine cross-yoked model trajectory, blinded rater, independent corpus of persona histories or full-value/long-horizon commitment trial has yet been executed. Human-coded is merely a controller name for script logic. G1 and G2 succeed only under the mock oracle; G5 is incomplete in real-model conditions; G6 mock replay passes; G3 and G4 remain untested. The preset advancement decision remains **NO-GO**.

The public code and template generator make the initial terminal battery operationally sealed from inference inputs, not statistically immune to researcher iteration or model-training contamination. Never use these scores to endorse consciousness, dyadic essence, a unique human causal contribution, or any other substrate claim.

## Next handoff

Run a limited development-phase real local model first, preserving exact model version, raw generations, prompt/output token counts, source citations, and timeout/failure traces. Upgrade independently authored, action-grounded conditional and prospective commitment cases before inferential tests. Precommit source authority and blinded scoring, verify matched-budget automated curation, then execute a registered continuing/newcomer cross-yoked trial. New findings, positive or null, require a separate immutable evidence-register entry with raw results; this note is not CC-E efficacy evidence.
