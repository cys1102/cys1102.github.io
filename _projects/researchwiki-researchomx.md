---
layout: page
title: ResearchWiki and ResearchOMX
description: Human-governed infrastructure for reproducible, agent-assisted research
permalink: /projects/researchwiki-researchomx/
importance: 1
category: work
related_publications: false
---

ResearchWiki and ResearchOMX are complementary tools for maintaining durable
research context while keeping scientific decisions with people.

## ResearchWiki

[ResearchWiki](https://github.com/cys1102/researchwiki-starter) is a Git-backed,
Obsidian-compatible Markdown workspace for research synthesis. It connects
concepts, papers, aggregate experiment evidence, claims, reviews, writing, and
the active roadmap through stable links and a chronological log.

The public starter was inspired by
[Andrej Karpathy's LLM Wiki idea](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
and turns that general pattern into a research-oriented GitHub Template. It
adds structured page metadata, aggregate-only defaults, deterministic lint,
and explicit human authority for decisions. A vector database or query-time
RAG service is not required.

## ResearchOMX

[ResearchOMX](https://github.com/cys1102/ResearchOMX) is the deterministic
control layer that can sit beside the wiki and project repositories. Its
read-only `researchctl` command validates versioned records, runs scientific
lint, traces claims to evidence, and reports blocked or unavailable evidence
without approving a claim or launching an experiment.

## How the pieces fit

```text
project repositories  ->  ResearchOMX validation  ->  ResearchWiki synthesis
code and evidence          schemas and lint            claims and decisions
```

- Project repositories own code, experiment contracts, and aggregate-safe
  results.
- ResearchOMX checks committed records and produces read-only diagnostics.
- ResearchWiki preserves the human-readable interpretation, review state, and
  roadmap.
- Explicit human records authorize execution, claim changes, review closure,
  and submission decisions.

Both public repositories use synthetic examples and exclude private research
state, participant-level data, unpublished results, credentials, and
project-specific adapters.

## Public repositories

- [Use the ResearchWiki starter](https://github.com/cys1102/researchwiki-starter)
- [Explore ResearchOMX](https://github.com/cys1102/ResearchOMX)
