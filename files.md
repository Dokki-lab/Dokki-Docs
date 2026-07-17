---
title: "Files"
canonical: "https://dokki.one/pub/docs/files"
source_url: "https://dokki.one/pub/docs/files"
updated_at: "2026-07-12T15:12:17.821+00:00"
generated_by: Dokki
---

# Files

Files are workspace resources for original uploaded assets that should remain files rather than become native documents. Visual guide Home Workspace Map Upload a file File uploads use a direct-to-stor

Canonical source: [https://dokki.one/pub/docs/files](https://dokki.one/pub/docs/files)

Files are workspace resources for original uploaded assets that should remain files rather than become native documents.

## Visual guide

[Home Workspace Map](home-workspace-map.md)

## Upload a file

File uploads use a direct-to-storage flow:

1. An Editor or Admin requests a one-time signed upload URL. Dokki checks membership, the declared size, the per-file limit, and remaining pooled storage.
1. The browser uploads the object directly to workspace storage.
1. Dokki finalizes the upload, verifies the object's actual size, repeats the quota checks, and creates the file resource.

If finalization fails after upload, Dokki attempts to remove the orphaned storage object. The second check matters because the declared client size is not trusted.

## Storage limits

Personal workspaces share their creator's account-wide storage pool across that person's personal workspaces. Organization workspaces share the organization's pooled storage. The default organization pool is 100 GB, unless its policy overrides it; organizations have no per-file cap unless a policy sets one.

Personal limits follow the current user plan: Free 1 GB total and 25 MB per file; Pro 100 GB and 500 MB; Max 5x 500 GB and 2 GB; Max 20x 1 TB and 2 GB. These limits can change with plan policy, so check **Billing & Credits** for the current entitlement.

## Preview and actions

Images render inline, PDFs use an embedded viewer, video and audio use browser media controls, and text-like formats can open inline. Other formats show metadata plus signed open or download actions.

From the file menu, people with edit access can rename the resource, change its icon, and manage tags. People with manage access can move it to Trash. Download uses a short-lived signed URL and preserves the original filename.

## Indexing and search

New files begin with an indexing state such as queued, indexing, done, failed, skipped, or unsupported. The file menu shows status, text and chunk counts, and lets an eligible user queue reindexing. Preview availability and indexing are separate: a PDF can render before extraction is finished.

After content is extracted and indexed, files can contribute to workspace search and Copilot context. Google Drive imports that create or refresh file resources also mark them for indexing.

## Files and publishing

Files can be shared inside a workspace but are not standalone published-site pages. Published documents, tables, and artifacts may refer to files only when the public rendering rules allow it.

---

Published from Dokki.
