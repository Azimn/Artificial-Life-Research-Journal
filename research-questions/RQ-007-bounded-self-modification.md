---
id: RQ-007
title: Bounded Self-Modification
type: research-question
status: open
updated: 2026-09-18
projects:
  - PRJ-005
  - PRJ-012
  - PRJ-013
tags:
  - self-modification
  - evolution
  - rollback
  - evaluation
---

# Bounded Self-Modification

## Question

Can a persistent artificial organism improve its own mechanisms while fixed external evaluation distinguishes genuine cognitive improvement from benchmark manipulation?

## Core difficulty

A candidate can appear better by rewriting inputs, outputs, timing, evaluator-facing behavior, or wrapper-owned state without improving the underlying organism.

## Current design response

Bicentennial Man separates Surface-Mutable Control from Mechanism-Mutable DUCK.

The Surface-Mutable condition measures how much apparent improvement can be achieved outside the organism.

The Mechanism-Mutable condition keeps scenarios, evaluators, renderer boundaries, and held-out transfer outside the mutable region.

Rollback and preserved ancestry are necessary so failed modifications do not destroy the experimental lineage.

## Stronger evidence

A modification becomes more credible if it survives unfamiliar histories, held-out scenario families, ablation, matched baselines, and replication while leaving fixed evaluation boundaries untouched.
