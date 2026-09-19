---
id: DOC-SEARCH
title: Search and Publishing
type: documentation
status: active
updated: 2026-09-18
---

# Search and Publishing

The journal is intentionally plain Markdown so the research memory does not depend on one application.

## Immediate search

GitHub can search filenames and repository text.

Clone the repository locally and open the repository root as an Obsidian vault for fast full-text search, backlinks, graph navigation, tags, and wikilinks.

Ordinary tools such as ripgrep can also search the entire journal.

## Recommended local workflow

Clone the repository.

Open the repository folder directly in Obsidian. Do not move the Markdown files into a separate proprietary database.

Commit meaningful research changes back to Git so the scientific history remains versioned.

## Quartz publishing layer

Quartz is the preferred future web layer because it is designed for Markdown knowledge bases and works naturally with Obsidian-style links and frontmatter.

The journal content should remain independent of Quartz. Quartz is a view over the research memory, not the research memory itself.

When Quartz is added, configure the published content to include the journal, project pages, research questions, concepts, and literature notes. Machine-generated experimental outputs should remain in their source repositories unless a compact result belongs in the journal.

## Searchable metadata

Every substantive note should use YAML frontmatter with, at minimum:

```yaml
---
id: EXP-2026-025
title: Example Experiment
type: experiment
status: active
updated: 2026-09-18
tags:
  - development
  - lesion
projects:
  - PRJ-002
research_questions:
  - RQ-002
---
```

Stable IDs make it possible to rename files without losing the intellectual identity of a record.

## AI retrieval

The Markdown corpus is deliberately suitable for retrieval by local or hosted language models.

For future automated retrieval, index content and metadata, but treat the Markdown files as the authoritative source. Generated summaries should point back to record IDs and source repositories rather than becoming a second hidden memory system.
