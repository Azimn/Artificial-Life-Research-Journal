# PSL native action prediction, Stage 01A

Date: 2026-10-09. Research finding, not character-continuity evidence.

The Doctor Lives [research PR #32](https://github.com/Azimn/The-Doctor-Lives/pull/32) performed a chronological comparison on 28 native, persistently recorded Pretorius action choices: 16 adaptation cases, eight familiar-context evaluation cases and four new-context cases. [Successful CI run 38016542721](https://github.com/Azimn/The-Doctor-Lives/actions/runs/38016542721), tested commit `edf35dcaa6449bc2ed73a359c349e8be31e50f0b`. The report is [here](https://github.com/Azimn/The-Doctor-Lives/blob/research/psl-stage01a-shadow-benchmark-20261009/results/predictive_self/stage01a/STAGE_01A_EXECUTED_REPORT.md).

Familiar-case log loss was 1.126915 for episodic PSL and 1.129793 for a simple global-frequency predictor, an inconclusive difference. New-context log loss was 2.439326 for PSL versus 1.670225 for the global predictor. Case labels were researcher-authored and highly correlated; 18/28 decisions were `persist`. No external world outcomes, independent characteristic-action judgments or semantic identity revisions were measured. A deliberate context misalignment damaged familiar-case prediction, which supports context association utility within this limited setup but not genuine autobiographical understanding.

Scientific disposition: **hold**. Do not claim Game of Self efficacy from this native decision assay. A stronger, source-disjoint and world-witnessed evaluation and appropriate sparse-context backoff are the next gates. 
