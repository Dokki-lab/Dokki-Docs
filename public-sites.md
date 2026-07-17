---
title: "Public Sites"
canonical: "https://dokki.one/pub/docs/public-sites"
source_url: "https://dokki.one/pub/docs/public-sites"
updated_at: "2026-07-10T05:05:03.606+00:00"
generated_by: Dokki
---

# Public Sites

A public site is the workspace-level container for resources you choose to publish. A site is separate from normal resource sharing: workspace content stays private until a document, table, or artifac

Canonical source: [https://dokki.one/pub/docs/public-sites](https://dokki.one/pub/docs/public-sites)

A public site is the workspace-level container for resources you choose to publish. A site is separate from normal resource sharing: workspace content stays private until a document, table, or artifact is explicitly committed into `published_resources`.

## Visual guide

[Publishing Snapshot Flow](publishing-snapshot-flow.md)

## Create and configure a site

Open **Workspace → Extensions → Publish**. The publishing area has three working areas:

- **Site settings** — create the site, choose the `/pub/<slug>` address, turn the site live/offline, set listed/unlisted behavior, configure language settings, set a site URL, and manage custom domain or subdirectory proxy options.
- **Navigation tabs** — choose up to five workspace tags as public top-level tabs. Tabs can be reordered or removed.
- **Resources** — publish, commit, or unpublish individual resources from the workspace tree.

Workspace admins and editors can manage publishing. Viewers cannot create sites or commit public snapshots.

## Public URL and slug

The default public URL is `https://dokki.one/pub/<site-slug>`. Slugs are normalized to lowercase letters, numbers, and hyphens. If a slug is already taken, Dokki rejects the change instead of silently moving the site.

If an active custom domain is configured, Dokki shows the custom-domain URL as the public URL. Subdirectory proxy setups keep their own host and base path through proxy headers.

## Publish a resource

Use the Resources tab, or a resource's publish action, to publish a document, table, or artifact. Publishing freezes the current source into a public snapshot and assigns a resource slug. Files are not currently published as standalone public pages.

What is frozen depends on the resource type:

- **Documents** freeze their persisted document JSON, plus public-safe resource embeds.
- **Tables** freeze their publishable table JSON and description.
- **Artifacts** freeze source and compiled output; JSX artifacts are recompiled from source at freeze time when possible.

## Commit changes

After a resource is published, workspace edits remain private until committed again. Dokki compares the source resource's `updated_at` with the public snapshot's `frozen_at`:

- **Unpublished** — no public snapshot exists.
- **Published** — the public snapshot is current.
- **Updated** — the source changed after the last public snapshot.

Use **Commit** on an Updated resource to refresh the public page.

## Unpublish

Unpublish deletes the resource from the public site. The original resource remains in the workspace, and normal workspace permissions continue to apply.

## Navigation and home behavior

Published navigation is built from committed resources plus ancestor folders needed to preserve the tree structure. Folders help structure the sidebar but are not readable pages.

The site can also store a `site_url` used by the public header/logo navigation. Navigation tabs are tag filters: a public tab points readers to pages with that workspace tag.

## Active and listed

An inactive site is not served publicly. An unlisted site remains reachable by direct link but is marked `noindex`, disallows crawlers in `robots.txt`, and does not expose `sitemap.xml` or `llms.txt`.

---

Published from Dokki.
