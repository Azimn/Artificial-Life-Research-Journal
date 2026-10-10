# Kiki Memory-Cognition Port v0.2: synthetic behavioral gate

**Experiment date:** 2026-10-10, America/Chicago.
**Engineering owner:** [Kiki-Mind](https://github.com/Azimn/Kiki-Mind), [PR #7](https://github.com/Azimn/Kiki-Mind/pull/7), [Issue #6](https://github.com/Azimn/Kiki-Mind/issues/6).
**Measured complete run:** [GitHub Actions 38028146504](https://github.com/Azimn/Kiki-Mind/actions/runs/38028146504), green; full original Kiki regression, six new behavior acceptance tests, eight existing cross-port adapter tests, and actual offline synthetic run.
**Frozen test fixture SHA-256:** `bcb86434da97ba0fbb5876a22f342b6cac8b930161f985c786a28bcbcee2cff7`.
**Common port version:** [Pretorius-Connectome commit `cc82c72167d87c19f16125ccdf9477b53c777878`](https://github.com/Azimn/Pretorius-Connectome/commit/cc82c72167d87c19f16125ccdf9477b53c777878).

## Research question

When Kiki's independently designed hash-chained canonical ledger is queried for metadata-only receipt IDs, does the verified cross-project memory-to-cognition port produce better *source identification and abstention decisions* than no retrieval? Does it add any advantage over direct source access with the same information?

The protocol and frozen synthetic fixture were committed **before the runner**. All twelve cases were authored by an assistant and are publicly visible. Six were labeled development and six labeled heldout, but this is **not independent blind testing**. No genuine Kiki mind data or player records were accessed. No renderer, trained embedding or neural network ran in this experiment.

## Recorded primary outcomes

| Condition | Correct total / 12 | Unique event IDs / 6 | Correct abstentions / 6 |
| --- | ---: | ---: | ---: |
| No retrieval | 6 | 0 | 6 |
| Always abstain | 6 | 0 | 6 |
| Direct read-only source | 12 | 6 | 6 |
| Shared memory-cognition port | 12 | 6 | 6 |

The development and development-sequestered case halves each scored 6/6 under the two retrieval conditions and 3/6 without retrieval. The existing source and shared port returned exactly the same decisions. The four gate probes passed: **wrong subject denied; revoked token denied; stale snapshot denied; restricted source record inaccessible**. The canonical hash-chain head was unchanged during the matched tasks, and payload titles/self-reports were absent from machine output.

CPU timing from this one workflow's twelve decisions: no-retrieval 0.071 ms, always-abstain 0.006 ms, direct adapter 39.421 ms, shared port 40.530 ms. These are order-dependent, tiny-sample engineering numbers, **not** reliable performance comparisons.

## What these data support

**Engineering positive:** the same verified memory contract works with both Pretorius's Vector Fly index and Kiki's independent canonical event ledger, returning source-linked evidence without copying histories, altering Kiki's TransitionGate, or promoting retrieved evidence to lived autobiography. A bounded synthetic decision task can use that evidence to cite a unique record while rejecting missing/ambiguous cases.

**Important negative/null:** the common port adds no outcome-quality advantage over direct access to the same Kiki receipt index. The 12/12 versus 6/12 difference against no-retrieval is strictly an **information availability effect** in an exact-label task. It says nothing about neural cognition, model-swap continuity, semantic memory, selfhood or personality stability. The explicit always-abstain control demonstrates that six of the twelve gold cases were abstentions.

**Validity limitation:** both positive queries and matching policy were developer-authored; no human/independent assessor, no withheld unknown narratives, no out-of-distribution language and no real behavioral agent were tested. Semantic ambiguity remains untouched.

## Durable documentation / replication

- [Predeclared fixture](https://github.com/Azimn/Kiki-Mind/blob/main/experiments/cognition_port_v02/fixture_v1.json)
- [Protocol](https://github.com/Azimn/Kiki-Mind/blob/main/experiments/cognition_port_v02/PROTOCOL.md)
- [Real ledger/port runner](https://github.com/Azimn/Kiki-Mind/blob/main/experiments/cognition_port_v02/run.py)
- [Permanent results interpretation](https://github.com/Azimn/Kiki-Mind/blob/main/experiments/cognition_port_v02/RESULTS.md)
- [CI original run and downloadable raw 48 case decisions](https://github.com/Azimn/Kiki-Mind/actions/runs/38028146504), workflow artifact `kiki-cognition-port-v02-fixed-battery` (90-day retention)
- [Acceptance tests](https://github.com/Azimn/Kiki-Mind/blob/main/tests_integration/test_cognition_port_v02.py)

PR #7 must still be confirmed merged before any link to `main` is taken as a main-branch guarantee. This note reports the **completed original CI**, not preemptive approval of unreviewed future changes.

## Recommended next gate

Do not add Kiki's private content to the current publicly testable retrieval surface. The next experiment should use **synthetic source-authored content** with an explicitly reviewed visibility/owner-provenance policy. Compare a source-indexed retrieval + source-gating decision to an information-matched baseline, not just no memory. Include independently written multi-hop, paraphrase, false-premise, wrong-owner and source-revocation questions. Preserve the strict separation of canonical event receipts, derived semantic hypotheses, lived experiences and model-rendered explanations.

Cross-reference [Kiki implementation integration note](KIKI_COGNITION_PORT_CROSS_PROJECT_INTEGRATION_2026-10-09.md) and [Cross Project Shared Memory Integration](CROSS_PROJECT_SHARED_MEMORY_INTEGRATION_2026-10-09.md).
