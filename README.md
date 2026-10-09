---
id: HOME
title: Artificial Life Research Journal
type: index
status: active
updated: 2026-10-08
---

# Artificial Life Research Journal

> "To a new world of gods and monsters! Ha ha! The creation of life is enthralling, distinctly enthralling, is it not?"

This repository is the canonical research memory for an ongoing program of experiments in persistent artificial individuals, digital organisms, developmental identity, artificial-life substrates, subjective cognition, emergent ecology, and believable characters.

The code for an experiment may live in another repository. The scientific record belongs here.

## Current cross-project program

The [Character Continuity Research Program v1](programs/CHARACTER_CONTINUITY_PROGRAM_V1.md) unifies the experimental interpretation of neural substrate learning, BioCircuit, FlyWire retrieval/imprinting, Attractomancy conditioning, and the definitive The Doctor Lives character. Start with the [cross-project evidence register](programs/CHARACTER_CONTINUITY_EVIDENCE_REGISTER_V1.md) and [four-arm comparison protocol](programs/CHARACTER_CONTINUITY_COMPARISON_PROTOCOL_V1.md). Source implementations and raw case-level evidence remain authoritative in their own repositories. The comparison protocol is a preregistration draft, not an executed study.

## Portfolio and provenance audit

The [October 8 completeness audit](audits/PORTFOLIO_COMPLETENESS_AUDIT_2026-10-08.md) compares the historical journal against the current accessible Azimn repository portfolio. Its [public inventory](audits/PUBLIC_REPOSITORY_INVENTORY_2026-10-08.csv) classifies 53 public repositories, the [research lineage map](audits/RESEARCH_LINEAGE_MAP_2023_2026.md) connects historical hypotheses, the [data-assets register](audits/RESEARCH_ASSETS_2026-10-08.md) identifies canonical source owners, and the [follow-up queue](audits/PORTFOLIO_FOLLOWUP_QUEUE_2026-10-08.md) records remaining verification work. Seven missing research lines and 27 existing or proposed experiment families were added to the central indexes. All 27 indexed October report links have [fetched source-blob SHA pins](audits/OCTOBER_EXPERIMENT_SOURCE_SNAPSHOT_2026-10-08.json), which identify report versions but do not independently reproduce their measurements. Three private repositories are excluded from the public roster. Repository visibility and engineering tests do not by themselves establish authorship or scientific validation.

## Central question

**What persistent causal organization is necessary for an artificial individual to acquire a history, be changed by that history, and remain recognizably the same individual afterward?**

The program approaches that question from several directions: portable identity, first-person cognition, memory and relationships, homeostatic and motivational organization, developmental learning, recurrent neural substrates, artificial chemistry, native computational substrates, information asymmetry, embodiment, and bounded self-modification.

## Start here

Read [INDEX.md](INDEX.md) for the knowledge map.

The main registries are [PROJECT_REGISTRY.md](PROJECT_REGISTRY.md), [EXPERIMENT_LEDGER.md](EXPERIMENT_LEDGER.md), and [RESEARCH_PROGRAMS.md](RESEARCH_PROGRAMS.md).

Research questions live in [research-questions/](research-questions/). Core research project records live in [projects/](projects/). Chronological lab notes live in [journal/](journal/). Reusable record formats live in [templates/](templates/).

Work that is worth preserving but is outside the core artificial-life program lives in the separate [Other Projects Registry](OTHER_PROJECTS.md) and [other-projects/](other-projects/) archive. Those records use `OPJ-` IDs and are not treated as experimental evidence unless explicitly promoted into the core research program.

## Journal rule

A research experiment is not finished until this journal records:

1. the question,
2. the design,
3. the result,
4. the interpretation,
5. the provenance,
6. what changed because of the result.

Null results, confounds, failed hypotheses, and abandoned designs are first-class results.

## Authority model

This repository is authoritative for the intellectual history of the research program. Individual project repositories remain authoritative for their code, exact commits, machine-readable results, and implementation details.

A journal entry may summarize evidence from another repository, but it should never silently overwrite or improve the original result.

## Search

The repository is plain Markdown with YAML frontmatter, stable IDs, tags, and wikilink-compatible filenames. It can be searched directly on GitHub, opened as an Obsidian vault, indexed by ordinary text tools, or published through Quartz.

See [docs/SEARCH_AND_PUBLISHING.md](docs/SEARCH_AND_PUBLISHING.md).

## Scope

The core research journal currently reconstructs relevant work back to at least 2023 and continues through the active 2026 program. The goal is not to make the historical reconstruction look cleaner than it was. Dates, certainty, provenance, proposed designs, completed experiments, and later corrections should be recorded honestly.

The repository also contains a deliberately separate archive for game-development, creative, teaching, 3D/XR, tooling, model-training, preservation, and other projects that do not currently belong under the artificial-life research framing.

## Naming

Stable IDs are permanent. Titles are not.

Projects use `PRJ-###`.
Research questions use `RQ-###`.
Experiments use `EXP-YYYY-###`.
Journal entries use `JRN-YYYY-MM-DD-##`.
Concept notes use `CON-###`.
Literature notes use `LIT-###`.
Other-project records use `OPJ-<CATEGORY>-###`.