---
title: "Translations"
canonical: "https://dokki.one/pub/docs/translations"
source_url: "https://dokki.one/pub/docs/translations"
updated_at: "2026-07-12T15:12:26.42+00:00"
generated_by: Dokki
---

# Translations

Published sites can offer translated public pages. Translation is asynchronous: publishing queues work, and the public site uses cached translations only after the worker has generated them. Visual gu

Canonical source: [https://dokki.one/pub/docs/translations](https://dokki.one/pub/docs/translations)

Published sites can offer translated public pages. Translation is asynchronous: publishing queues work, and the public site uses cached translations only after the worker has generated them.

## Visual guide

[Publishing Snapshot Flow](publishing-snapshot-flow.md)

## Configure languages

In publishing settings, choose the content's original language and any additional languages to offer. The original language is the default language and is never machine-translated.

The current language list includes English, Simplified Chinese, Traditional Chinese, Spanish, French, German, Japanese, Korean, Portuguese, Russian, Italian, Dutch, Arabic, Hindi, Indonesian, Turkish, Vietnamese, Thai, Polish, and Ukrainian.

Changing the default language removes that language from the additional-language set, because it becomes the source language.

## Reader experience

Visitors can switch languages from the public site. Dokki uses `?lang=<code>` as the language selector and carries it through internal published-site links so readers do not lose their language while navigating.

If a requested language is not enabled, unknown, or equal to the default language, Dokki renders the original content.

## How translation updates

When you publish or commit a resource, Dokki queues translation jobs for enabled non-default languages. When a new language is enabled at the site level, Dokki queues translation work for already-published documents.

Translation jobs are stored in `translation_jobs` and claimed by a worker with lock/retry behavior. Queued jobs for the same site, language, kind, and source are replaced before insertion so stale queued work is superseded by the latest publish.

## Cached translations

Dokki stores translated output in `published_translations` with content hashes:

- document translations cache the translated title and document JSON;
- string translations cache site-level strings such as home copy and navigation labels.

At render time, Dokki reads cached translations. A cache miss renders the original language instead of blocking the page request.

## What gets translated

Documents receive body translation. Site home strings and navigation strings are translated so page titles, excerpts, breadcrumbs, and nav labels can appear in the selected language when cached.

Tables and artifacts can appear in navigation and published pages, but their internal structured content is not translated the same way document body text is.

## SEO behavior

When multiple languages are enabled, document metadata includes hreflang alternates. The default language uses the canonical page URL; translated variants use the same URL with `?lang=<code>`.

---

Published from Dokki.
