---
title: "Publish"
canonical: "https://dokki.one/pub/docs/publish"
source_url: "https://dokki.one/pub/docs/publish"
updated_at: "2026-07-10T04:54:26.009+00:00"
generated_by: Dokki
---

# Publish

Publishing turns selected documents, tables, and artifacts into a public website for a workspace. The publishing app now has three working areas: site settings, navigation tabs, and the resource tree.

Canonical source: [https://dokki.one/pub/docs/publish](https://dokki.one/pub/docs/publish)

Publishing turns selected documents, tables, and artifacts into a public website for a workspace. The publishing app now has three working areas: site settings, navigation tabs, and the resource tree.

## Visual guide

[Publishing Snapshot Flow](publishing-snapshot-flow.md)

## In this section

- **Public Sites** — create the workspace site, choose the slug, turn the site on or off, and understand resource publish states.
- **Custom Domains** — attach a custom domain and verify DNS.
- **SEO & Discoverability** — control whether the site is listed, plus robots.txt, sitemap.xml, and llms.txt behavior.
- **Translations** — choose the default public language and additional translated languages.

## Publishing app layout

Open **Workspace → Extensions → Publish**. The page contains:

- **Site settings** — slug, active/offline switch, listed/unlisted switch, language settings, default public URL, and custom domain controls.
- **Navigation tabs** — optional tag-based top navigation for the published site. You can add up to five workspace tags as tabs and reorder or remove them.
- **Resources** — a publish tree showing every publishable resource and its current status.

## Publishing is snapshot-based

When you publish a resource, Dokki freezes the current content into the public site. Later workspace edits do not automatically change the public page. The publish status becomes **Updated** when the source has changed, and you commit again when the public version should refresh.

## Resource states

- **Unpublished** — the resource is private to the workspace or available only through its normal sharing settings. It is not on the public site.
- **Published** — the frozen public snapshot is current.
- **Updated** — the workspace resource changed after the last frozen public snapshot. Use **Commit** to publish the new version.

## What can be published

Documents, tables, and artifacts can be published. Files are shared through resource permissions and links, but are not currently published as standalone docs pages.

## Embedded resources

Published documents can include resource embeds. At publish time, Dokki only bakes in embedded resources that the public audience can see: resources already published on the same site, or resources with public link access. Private or unpublished embeds become unavailable in the public snapshot and do not leak titles.

For embedded tables, Dokki freezes a public-safe preview rather than leaving the page to fetch live table data.

## Site-level controls

- Turning a site inactive takes the whole public site offline without deleting its settings.
- Changing the slug changes the `dokki.one/pub/<slug>` address, unless the new slug is already taken.
- The listed switch controls search-engine discoverability behavior. Keep private or early sites unlisted.
- The default language is always enabled. Additional languages can be enabled for translated public pages.
- Custom domains start as pending, poll for DNS verification, then become active once the domain is configured correctly.

---

Published from Dokki.
