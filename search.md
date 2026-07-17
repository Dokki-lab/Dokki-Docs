---
title: "Search"
canonical: "https://dokki.one/pub/docs/search"
source_url: "https://dokki.one/pub/docs/search"
updated_at: "2026-07-12T15:12:30.32+00:00"
generated_by: Dokki
---

# Search

Search combines backend retrieval with local navigation matches. It is scoped to workspaces you can access and excludes archived workspaces. Visual guide Search Coverage Map Resource coverage by retri

Canonical source: [https://dokki.one/pub/docs/search](https://dokki.one/pub/docs/search)

Search combines backend retrieval with local navigation matches. It is scoped to workspaces you can access and excludes archived workspaces.

## Visual guide

[Search Coverage Map](search-coverage-map.md)

## Resource coverage by retrieval path

- **Semantic search** uses document embeddings. It is strongest when you remember an idea but not the exact words, and currently returns document content rather than embedding tables or Artifact source.
- **Keyword search** matches document content and titles, table content, Artifact source, and indexed file text. Use it for exact phrases, identifiers, names, error strings, and source terms.
- **Hybrid search** fuses keyword and document-semantic results. It can rerank when a caller enables reranking.
- **Folders** have no backend embeddings. The search dialog adds title matches from the loaded workspace tree.

Files only contribute content after extraction and indexing. A new file can preview immediately but remain absent from content search until its extracted text is ready.

## Search dialog scope

The dialog also appends local navigation matches for agents, Copilot chat titles, and message or channel names. These are navigation results, not a claim that every message or chat body is full-text indexed.

By default, search uses the active workspace. The all-workspaces control searches the non-archived workspaces the signed-in person belongs to. Guest users receive tree-title matches only.

## Deep Search and graph signals

Deep Search expands a question into focused sub-queries, runs graph-boosted hybrid retrieval, de-duplicates resources, and attempts a short grounded answer. If answer generation or graph retrieval is unavailable, it still returns the raw retrieval results.

Knowledge Graph is optional and organization-scoped. It can boost ranking but does not inject inaccessible resource content or replace normal keyword and semantic retrieval.

## Access and freshness

Normal in-app search uses the caller's RLS-scoped access. Search and MCP paths that deliberately surface restricted items can redact their excerpts and mark them restricted, pointing the caller to request access rather than leaking content.

Edits and uploads may need background indexing before text retrieval reflects them. Clear local recent searches when you want to remove only your browser's search history.

---

Published from Dokki.
