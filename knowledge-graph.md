---
title: "Knowledge Graph"
canonical: "https://dokki.one/pub/docs/knowledge-graph"
source_url: "https://dokki.one/pub/docs/knowledge-graph"
updated_at: "2026-07-10T04:49:55.694+00:00"
generated_by: Dokki
---

# Knowledge Graph

Knowledge Graph is an optional organization-scoped relationship layer. It is not enabled for personal workspaces and does not replace ordinary search. Visual guide Search Coverage Map When it is avail

Canonical source: [https://dokki.one/pub/docs/knowledge-graph](https://dokki.one/pub/docs/knowledge-graph)

Knowledge Graph is an optional organization-scoped relationship layer. It is not enabled for personal workspaces and does not replace ordinary search.

## Visual guide

[Search Coverage Map](search-coverage-map.md)

## When it is available

A workspace must belong to an organization, and that organization must have its Knowledge Graph flag enabled. When either condition is missing, the Home graph card hides itself and graph-assisted retrieval safely falls back to normal keyword and semantic search.

## What it contributes

The graph models entities, relationships, and connected resources across organization content. Hybrid and Deep Search can use graph results as a ranking boost for resources that are already surfaced by ordinary retrieval. The graph arm improves ordering; it is not an unrestricted source of new hidden content.

Copilot, agents, and compatible MCP clients can use relationship-aware discovery when their configured scope allows it.

## Access boundary

Graph data is organization partitioned, but resource permissions still apply. People see only resources they can view. In contexts that intentionally expose a restricted item's existence, Dokki removes excerpts and content and directs the person to request access.

## Home overview

Enabled organization workspaces can show an overview of top entities and edges on Home. It is an orientation view, not a full graph editor or proof that every workspace resource has been indexed.

## Expected behavior

Graph availability is best-effort. A graph error or disabled feature should not make search empty: the search path continues with the keyword and semantic arms.

---

Published from Dokki.
