---
title: "Version History"
canonical: "https://dokki.one/pub/docs/version-history"
source_url: "https://dokki.one/pub/docs/version-history"
updated_at: "2026-07-10T06:03:13.941+00:00"
generated_by: Dokki
---

# Version History

Version History is Dokki's snapshot layer for documents, tables, and artifacts. It helps you review earlier states, compare changes, and recover context when a resource has moved too far from a prior

Canonical source: [https://dokki.one/pub/docs/version-history](https://dokki.one/pub/docs/version-history)

Version History is Dokki's snapshot layer for documents, tables, and artifacts. It helps you review earlier states, compare changes, and recover context when a resource has moved too far from a prior version.

## Visual guide

[Collaboration Governance Map](collaboration-governance-map.md)

## Document snapshots

Documents store snapshots with version numbers, timestamps, snapshot type, description, character count, word count, and a preview. The document snapshot API can list recent snapshots and create a manual snapshot from the latest persisted document state.

## How long snapshots are kept

While people edit, a document saves an automatic snapshot at most every 30 minutes, and another when the last editor disconnects. Automatic snapshots are pruned over time: a document keeps at most 50 of them, and automatic snapshots older than 30 days are removed. Manual snapshots are kept until you delete them, so create one before a risky rewrite.

## Current-state caveat

Manual document snapshots read the latest persisted `documents.data` state. If a document is open and Hocuspocus still has unsaved in-memory edits, wait for the editor's idle save before creating a manual snapshot.

## Compare with current

The diff-with-current flow downloads the stored Yjs snapshot, extracts snapshot content when possible, compares it against the current document content, and returns added, removed, modified, and unchanged segments plus summary statistics.

## Tables and artifacts

Tables and artifacts also have snapshot APIs. Treat the snapshot list as a history view for the resource type you are working in, not as a single global workspace timeline.

## What snapshots are not

- They are not a replacement for workspace trash. Deleted resources live in Trash first.
- They are not a live collaborative cursor history.
- They may lag the latest keystroke until persistence catches up.
- They do not publish changes automatically. Publishing has its own frozen public snapshots.

---

Published from Dokki.
