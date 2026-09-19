---
id: PRJ-012
title: Integration Harness
type: project
status: active
updated: 2026-09-18
repos:
  - https://github.com/Azimn/integration-harness
research_questions:
  - RQ-006
  - RQ-007
tags:
  - methodology
  - ablation
  - provenance
---

# Integration Harness

## Core research question

Can persistent-agent mechanisms be integrated only after they demonstrate measurable causal value under controlled tests?

## Principle

Do not begin by designing a new mind.

Begin by auditing existing implementations, preserving provenance, wrapping mechanisms behind small interfaces, and testing whether each mechanism produces a longitudinal behavioral effect.

New cognitive mechanisms require an explicit gap finding before implementation.

## Experimental loop

Proposal, donor and reuse check, adapter or wrapper, deterministic tests, adversarial review, behavioral and ablation tests, revision, second review, and merge decision.

## Importance

The harness converts software reuse into experimental discipline and helps prevent the research program from continually adding plausible mechanisms without evidence that they matter.
