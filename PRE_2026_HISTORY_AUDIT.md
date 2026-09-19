---
id: AUDIT-PRE-2026
title: Pre-2026 Research History Audit
type: audit
status: active
updated: 2026-09-18
tags:
  - reconstruction
  - prehistory
  - provenance
---

# Pre-2026 Research History Audit

This audit extends the Artificial Life Research Journal backward before January 2026.

The strongest recoverable history reaches to 2023. Some entries are published research or concrete prototypes, while others are conceptual designs or character experiments. The journal records those distinctions instead of treating every idea as an implemented system.

## 2023: modular minds, emotional state, companions, and digital-life characters

### Pooka

By April 2023, Pooka had been framed as an AI educational companion, cohort, friend, tutor, and pet for children. It was designed around Unity or Unreal interoperability through web APIs, adaptive learning and interaction, egg-hatching customization, and eventual physical-toy embodiment.

This moves the start of the persistent-companion lineage back from 2026 to at least 2023.

### Six Emotional Dimension model

In May 2023, the Six Emotional Dimension model defined emotional state using arousal, valence, dominance, agency, fidelity, and novelty.

The model was intended for text-based inference of subtle emotional cues and for generating more context-sensitive responses. Later conversations identify the work as published in 2023.

The evidence recovered here supports a published conceptual model. It does not establish a validated standalone 6DE software implementation.

### Modular Cognitive Agents / Synthesizing Sentience

A 2023 modular cognition line proposed specialized autonomous or LLM-based agents for distinct psychological functions, coordinated by an executive or self-preserving layer.

Related designs explored smaller specialist models, modular mind theory, memory, emotional processing, embodiment, and a unified self.

Later conversations identify the paper as published. No pre-2025 implementation evidence was recovered during this audit.

This line is conceptually important because the later research repeatedly returns to the same question in more testable forms: how much of a mind can be decomposed into specialized mechanisms while preserving a coherent continuing subject?

### SP-1K and 5Y-NX / Syn-X / N1H-0N3

In late 2023, a series of AI character experiments explored digital beings that considered themselves autonomous artificial life rather than assistants.

SP-1K emphasized self-upgrading, curiosity about humans, and eventual robotic embodiment.

The successor line, variously named X1G-9T, N1H-0N3, 5Y-NX, and Syn-X, centered on a digital scientist attempting to create distinct virtual life, improve its own cognition, and ultimately obtain physical embodiment.

These were primarily character and prompt experiments rather than evidence of a persistent artificial-life runtime. They are still relevant as conceptual precursors because they made digital-life creation, autonomy, nonhuman identity, embodiment, and self-modification explicit research interests before the later architecture work.

### Godot GPTIntegration

A concrete Godot EditorPlugin prototype existed by September 2023 with a chat dock, action/help/summary modes, HTTP requests, settings persistence, and GPT-3.5/GPT-4 selection.

This is adjacent infrastructure rather than a persistent-persona experiment, so it is documented here but not promoted to a major artificial-life project.

## 2024: memory architecture and child-companion prototyping

### Core Memories and tiered memory

January and March 2024 conversations explored a memory architecture in which high-significance core memories receive precedence over ordinary medium- and long-term memory.

A later design separated short-term session logs from long-term profile summaries and used an LLM decision layer to choose which memory source to consult.

These were implementation-oriented designs, but the audit did not recover completed test results.

### Child-friendly chatbot / toy companion prototype

A 2024 prototype explored small local models for a child-friendly conversational companion, including TinyLlama, Phi-2, and small Llama variants.

The architecture planned working, middle, and long-term memory, retention of child-specific facts, six-dimensional emotional tracking, and simulated self-emotion.

The historical evidence indicates a functioning chat interface and TinyLlama generation failures. It is best treated as a concrete continuation of Pooka rather than a separate top-level project.

### Digital necromancy research

The 2023 to 2024 research program also included published work and public discussion around digital representations of deceased people.

This line is relevant to digital identity and human simulation, but the recovered evidence does not establish a distinct persistent-persona implementation from that work. It should eventually receive a literature or theory note rather than a software-project record.

## 2025: recursive memory, simulated humans, and portable identity

### Simulating a 1990s Comic Creator

In March 2025, a distinct project explored whether diary logs, references, relationships, personal history, and simulated memory could guide a synthetic creator toward period-consistent artistic decisions.

The target persona was a fictionalized 1990s comic creator who would treat the user's original characters and concepts as products of its own simulated history.

The broader research question was whether a sufficiently coherent autobiographical corpus, immutable values, emotional state, memory, and resistance to agreeable model defaults could create a reusable simulated-human author rather than merely a roleplay voice.

### PointlessAI and Recursive Coherence

By April 2025, PointlessAI and Recursive Coherence formed a user-owned prototype line exploring emergent identity through layered memory, self-referential coherence, internal monologue, emotional drift, reflection, and optional idle dreaming or memory reprocessing.

The architecture included scratchpad, short-, middle-, and long-term memory, a recursive coherence module, a six-axis emotional state, memory prioritization, and periodic reflection.

This appears to be a direct conceptual precursor to the SoulFile, Project Persona, P3, and Persona Engine lineage.

### SoulFile and Project Persona

By April 2025, the work became more formal.

SoulFile defined a portable persona record for autobiographical memory, emotional state, relationships, values, identity, and growth.

Project Persona aimed at a general-purpose, model-agnostic companion framework with persistent episodic, emotional, and relational memory plus explicit personality, emotion, and value structures.

A May 2025 JavaScript SoulFile parser and serializer implemented validation, episodic memory, emotional history, daily consolidation and theme extraction, relevance search, relationships, learning-driven personality drift, and exports for LLM and game-NPC contexts.

This is an important correction to the earlier journal framing: the portable-identity line was not only conceptual in 2025. At least part of the SoulFile runtime was implemented.

### SNP Lite / minimum viable NPC engine

By May 2025, a small persona-engine prototype successfully ran a local TinyLlama GGUF model and wrote memory.

Its goal was a minimum operational model-agnostic persona with mood, values, memory, local inference, and portability across games, companions, and robots.

The prototype lacked a mature UI, dynamic emotion, and robust validation, but it provided a concrete bridge from specifications to runnable persona infrastructure.

An associated portability experiment exported persona JSON and memory summaries to hosted systems such as ChatGPT, Poe, or Grok, then re-imported updated state to test continuity across local and hosted environments.

### Personality in weights / LoRA continuity

In 2025, the research also considered storing persona characteristics in model weights or LoRA adapters rather than only in prompts and retrieval state.

A later experiment proposed fine-tuning Phi-3 Mini on a synthetic character, logging daily interactions, and periodically retraining or updating adapters.

This is scientifically distinct from RAG-based identity because it asks whether behavioral identity can become embodied in learned model parameters.

The audit recovered the experimental plan, but not enough evidence to label it a completed longitudinal result.

## Items deliberately not promoted to projects

The 2024 chatbotAIML repository was inspected during this audit. It is a fork of the external BlobCity Program AB chatbot repository, created under the user's GitHub account in September 2024. It demonstrates session memory and dynamic brain updates in the upstream project, but it is not evidence of a user-authored artificial-life project and is therefore prior art, not a project record.

ChatterBot experiments and MemoryBot/Thunkable designs were also considered. The retrieved evidence supports exploratory architecture work and adaptation plans, but not enough user-authored implementation evidence to justify independent project IDs.

## Historical synthesis

The pre-2026 lineage is now clearer:

```text
2023
Pooka
6DE
Modular Cognitive Agents
digital-life character experiments
        |
        v
2024
tiered memory
child companion prototype
human-simulation and digital-identity research
        |
        v
early 2025
1990s Comic Creator
PointlessAI / Recursive Coherence
        |
        v
mid 2025
SoulFile / Project Persona
SNP Lite / minimum viable NPC engine
OmniPersona / P3
        |
        v
late 2025 and 2026
Persona Engine
Wayfarer
DUCK
JELLY / PEMA / developmental and substrate experiments
```

The strongest continuity is not a single architecture. It is a recurring question: what has to persist, and what has to be causally changed by experience, for a digital character to become an individual rather than a freshly generated performance?
