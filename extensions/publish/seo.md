---
title: "SEO"
canonical: "https://dokki.one/pub/docs/seo"
source_url: "https://dokki.one/pub/docs/seo"
updated_at: "2026-07-12T15:12:22.985+00:00"
generated_by: Dokki
---

# SEO

Dokki gives each published site explicit controls for whether search engines and AI crawlers should discover it. Discovery behavior is controlled at the site level through the listed/unlisted setting.

Canonical source: [https://dokki.one/pub/docs/seo](https://dokki.one/pub/docs/seo)

Dokki gives each published site explicit controls for whether search engines and AI crawlers should discover it. Discovery behavior is controlled at the site level through the listed/unlisted setting.

## Visual guide

[Publishing Snapshot Flow](../../reference/visual-library/publishing-snapshot-flow.md)

## Listed sites

When a site is listed, Dokki serves crawl-friendly public pages with normal links between published resources. Published pages include metadata built from the frozen resource, workspace/site context, and resource tags.

Document pages include:

- canonical URLs;
- Open Graph and Twitter metadata;
- article or web-page JSON-LD;
- breadcrumb JSON-LD;
- tag keywords when tags exist;
- hreflang alternates when multiple published languages are enabled.

## Unlisted sites

When a site is unlisted, pages remain reachable by direct link but are marked `noindex` and `nofollow`. Dokki also returns crawler-blocking or empty discovery surfaces:

- `robots.txt` returns `Disallow: /`;
- `sitemap.xml` returns 404;
- `llms.txt` returns 404.

Use unlisted for drafts, internal previews, customer-specific docs, or anything you want shareable by link but not indexed.

## Sitemap

`sitemap.xml` includes the published site home and every committed published resource. It uses the active public base URL: default `/pub/<slug>`, custom domain, or subdirectory proxy base.

For each page, the sitemap uses `frozen_at` when available, falling back to the published row or site timestamp. Commit changes after editing a published resource so the public snapshot and sitemap timestamp match the version you want crawled.

## robots.txt

For listed sites, `robots.txt` allows crawling and points to the site's sitemap URL. For unlisted sites, it disallows all crawling. The route is served from the same public base as the site, including custom domains and subdirectory proxies.

## llms.txt

`llms.txt` summarizes the published site for AI crawlers and assistants. It includes:

- the site name;
- a short summary from the home description, or a generated fallback;
- a hierarchical Markdown map of committed public pages.

Folder labels preserve the information architecture, but only published resources receive links and count as readable pages.

## Custom domains and subpaths

Custom domains and subdirectory proxies should keep public links, canonical URLs, robots.txt, sitemap.xml, and page routes aligned. If you change domain routing, verify the live public URL directly and check the discovery files from that same host and path.

---

Published from Dokki.
