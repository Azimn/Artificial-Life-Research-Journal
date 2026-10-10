# 2026-10-09: Empirical alternatives to Pretorius's self-binding and Predictive Self Loop

Status: **external empirical literature synthesis; not a Pretorius efficacy trial**  
Program: Character Continuity / Definitive Pretorius  
Detailed review and experimental design: https://github.com/Azimn/The-Doctor-Lives/blob/research/predictive-self-loop-20261009/docs/ARXIV_2026_TESTED_PERSONA_ARCHITECTURES_REVIEW.md

## Reason for review

The previous SelfBindingModulator Stage 01 had 0/16 changed selected actions in matched clones. The subsequent Predictive Self Loop Stage 01A (28 native policy observations) reached familiar-context mean log loss 1.1269 versus global-frequency baseline 1.1298; however its unseen-context loss 2.4393 was worse than global frequency 1.6702. These results concern *internal action-label prediction*, not enacted character or world success. Continuing to adjust scalar identity weights on inspected cases would not supply independent support.

## High-priority tested external candidate

Tang et al., **PHASE-Tree**, arXiv:2608.06975 https://arxiv.org/abs/2608.06975 ; source https://github.com/MemTensor/PHASE-Tree . Multi-timescale immutable identity and editable persona/session/moment tree. On LongEvoRoleBench long-dialogue role generation, author-reported textual-mode macros: Char 3.004 vs PAG 2.510 (+19.7%), Sem 3.697 vs RAG 3.289 (+12.4%), Emb 0.314 vs RAG 0.273 (+15.1%). Paper reports a blinded 200-response human evaluation, while the descriptive PT-vs-NR difference of +.20 is from smaller n=10 subsets; avoid overstating the human result. Code/data/evaluation and chronological later-episode splits are available, but rerunning all experiments may require GPU resources, local models and separate judge infrastructure. This is our **first replication target** because it measures *realized character state*, not only lookup.

Tong and Zou, **PersonaForge**, ACL 2026 Findings https://aclanthology.org/2026.findings-acl.386/ ; code https://github.com/fQwQf/PersonaForge . 88-character studies report +19.4% personality consistency and drift 6.3% vs 24.8% over 50 turns; external RoleBench drift 8.4% vs 20.4%, and selective deliberation 96% of full performance for 13.4% token overhead. Its conflict-oriented dual-process intervention is an attractive second independent ablation, not a reason to invent Pretorius trait ground truth.

Jiang et al., **BRIDGE**, ICML 2026 https://proceedings.mlr.press/v306/jiang26aw.html ; code https://github.com/Sunrich-HT/BRIDGE . PersonaGym 4.59, CoSER 59.5, with frozen Qwen2.5-32B plus 277M trained module parameters. Mechanistically interesting behavior/latent/memory reconciliation, but high-cost and not an appropriate full transplant to a local low-compute character.

Memory-specific supporting work: **TiMem** arXiv:2601.02845, LoCoMo 75.30% and LongMemEval-S 76.88% with 52.20% recalled-token reduction; **HippoRAG 2** arXiv:2502.14802, +7% associative memory over its strongest embedding reference; **LongMemEval-V2** arXiv:2605.12493, 451 environment-memory questions and a strong but expensive file-agent method. **MemoryArena** arXiv:2602.16313 shows why high recall does not imply multi-session world-task success. **Convomem** arXiv:2511.10523 cautions that simple exhaustive/full-context strategies often outperform elaborate retrieval for small conversation histories.

## Ruling

**Prioritize PHASE-Tree textual route for the first external reproduction** (rather than immediately adopting a new architecture). Compare its exact ablation with a flat identity profile, a static hierarchical tree, an evolving tree, and equal-evidence full-context control. Only after reproducing external behavior improvement should we adapt its state tiers to the canonical Pretorius evidence plane and test source-grounded, independently judged character-specific decisions. Compare selective PersonaForge processing separately. The outcome must be better contextual behavior and verified consequences under session/model changes, not only stylistic coherence. Preserve negative results and no-bypass UPPB/first-person constraints.

This journal entry is a research **review and recommendation**, not evidence that either technique improved Pretorius. The subject's historical canon, neural checkpoint and runtime policy remain unchanged.
