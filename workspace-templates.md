---
title: "Workspace Templates"
canonical: "https://dokki.one/pub/docs/workspace-templates"
source_url: "https://dokki.one/pub/docs/workspace-templates"
updated_at: "2026-07-10T04:50:02.939+00:00"
generated_by: Dokki
---

# Workspace Templates

Workspace templates start a new workspace from repeatable structure instead of rebuilding a setup by hand. Visual guide Home Workspace Map Choose a template When creating a workspace, choose Blank , a

Canonical source: [https://dokki.one/pub/docs/workspace-templates](https://dokki.one/pub/docs/workspace-templates)

Workspace templates start a new workspace from repeatable structure instead of rebuilding a setup by hand.

## Visual guide

[Home Workspace Map](home-workspace-map.md)

## Choose a template

When creating a workspace, choose **Blank**, a system template, a public custom template, or a custom template you own. Templates that are private to another person are not available to you.

The picker includes summary counts for folders, documents, and agents. A blank workspace is the only option that intentionally seeds no starter resources.

## What a template copies

A template snapshot can copy folders, documents, tables, artifacts, and supported agent configuration, including the captured structure and content. It does not copy live external credentials, personal app connections, transient agent runs, chat history, or secrets.

## Creation and seeding

Dokki creates the workspace first and makes its creator an admin. For a nonblank selection it then loads the template snapshot and seeds resources after the response has returned. The client receives a seeding status, and the new resources appear as they are created. Blank returns a blank status and creates no seed work.

This means a large template can look partially populated briefly. Do not treat the initial sidebar state as the complete seed until the structure has finished arriving.

## Save a workspace as a template

Only workspace admins can save a workspace as a reusable custom template. Remove drafts, customer material, secrets, access tokens, and private instructions before saving.

Custom templates can remain private to their creator or be made public. For a template sourced from an organization workspace, public publishing requires that organization to allow public template publishing in its organization settings.

Archiving a custom template removes it from future pickers. Changing or archiving a template never rewrites workspaces that were already created from it.

---

Published from Dokki.
