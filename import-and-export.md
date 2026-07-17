---
title: "Import and Export"
canonical: "https://dokki.one/pub/docs/import-and-export"
source_url: "https://dokki.one/pub/docs/import-and-export"
updated_at: "2026-07-10T08:58:46.741+00:00"
generated_by: Dokki
---

# Import and Export

Your content is not locked in. Dokki supports document export from the editor and imports from nine external sources through workspace connections. Visual guide Collaboration Governance Map Export for

Canonical source: [https://dokki.one/pub/docs/import-and-export](https://dokki.one/pub/docs/import-and-export)

Your content is not locked in. Dokki supports document export from the editor and imports from nine external sources through workspace connections.

## Visual guide

[Collaboration Governance Map](collaboration-governance-map.md)

## Export formats

The document export dialog supports five formats:

- **PDF** — rendered from document content, with an embedded CJK font loaded lazily for better Chinese/Japanese/Korean output.
- **Markdown** — plain text with Markdown formatting where possible.
- **Text** — plain text without formatting.
- **Word Document (.docx)** — Microsoft Word format generated from document structure.
- **Image (.jpg)** — captures the visible editor content as a JPEG image. This option needs the document editor to be open in the browser.

## Export source

When the editor is available, export uses the live editor content. When the editor is not available, Dokki falls back to the persisted document JSON and resource title where possible.

## Import from external sources

The import dialog supports nine sources: Google Drive, Notion, Linear, Confluence, SharePoint, OneDrive, DingTalk, Feishu / Lark, and WeCom. Google Drive, Notion, Linear, Confluence, SharePoint, and OneDrive can connect with OAuth; Notion and the others also accept an API token, and DingTalk, Feishu / Lark, and WeCom are token-based. Every source supports importing a whole readable scope, not just single items.

After a workspace admin connects a source, admins and editors can pick what to import — Google Drive uses the Google file picker, while other sources take an item URL or ID — and enqueue import jobs into the selected folder.

## What gets created

Each selected item becomes one `sync_connections` job and, after the worker runs, one Dokki resource. Page-like content — Notion pages, Confluence pages, Linear issues and documents, DingTalk / Feishu / WeCom docs — is converted to Markdown and upserted as a native Dokki document. For Google Drive:

- Google Docs are exported as Markdown and upserted as native Dokki documents.
- Google Sheets are exported as CSV and stored as file resources.
- Google Slides are exported as PDF and stored as file resources.
- Other Drive files are downloaded and stored as file resources when they fit the configured file-size limit.

File imports land in workspace storage under an imports path and are eligible for file indexing. Re-imported or synced file resources overwrite the stored object and mark indexing pending again.

## One-time import versus sync

- **One-time import** queues a job that runs once and then remains done.
- **Sync mode** queues the same import but keeps the job due again on the worker's sync interval.
- Sync is one-way: external source to Dokki copy. Editing the Dokki copy does not write changes back to Google Drive.
- A sync job skips work when Google Drive reports the same modified timestamp as the last successful run.

The connection must belong to the same workspace, must match the import's provider, and must still be authorized. Imports require an admin or editor role in the destination workspace.

## Workspace-to-workspace sync

Dokki also has an internal workspace sync adapter used when copied resources are kept refreshed from their original source. This is separate from external Google Drive import, but it follows the same one-way source-to-copy model.

## Current limits

- Import is asynchronous; resources appear after the sync worker claims and finishes the queued job.
- Sync-mode refresh depends on what the source reports: sources without reliable modified timestamps may re-import on each interval.
- Export is document-focused. Tables, artifacts, and files have their own interaction surfaces.
- Image export depends on browser rendering and may require the editor content to be visible.

---

Published from Dokki.
