---
title: "Custom Domains"
canonical: "https://dokki.one/pub/docs/custom-domains"
source_url: "https://dokki.one/pub/docs/custom-domains"
updated_at: "2026-07-10T05:05:04.147+00:00"
generated_by: Dokki
---

# Custom Domains

Custom domains let a published site live at a domain you own, such as docs.example.com . They change the public base URL while keeping the same Dokki publishing model: committed public snapshots, list

Canonical source: [https://dokki.one/pub/docs/custom-domains](https://dokki.one/pub/docs/custom-domains)

Custom domains let a published site live at a domain you own, such as `docs.example.com`. They change the public base URL while keeping the same Dokki publishing model: committed public snapshots, listed/unlisted controls, sitemap behavior, and translation behavior all still apply.

## Visual guide

[Publishing Snapshot Flow](publishing-snapshot-flow.md)

## Why use a custom domain

Use a custom domain when public docs should live under your brand, match your search presence, or sit beside your product website.

## Setup flow

1. Create a published site in **Workspace → Extensions → Publish**.
1. Add a custom domain in Site settings.
1. Dokki validates the domain format, checks that it is not already used by another site, and registers a Cloudflare for SaaS custom hostname.
1. Add the DNS record shown in Dokki.
1. Click **Verify DNS**, or wait for the settings page to poll while the domain is pending.
1. Once the hostname and SSL are active, Dokki marks the domain active and uses it as the public URL.

Workspace admins and editors can add, verify, or remove a custom domain.

## DNS record

For the current custom-domain flow, configure a CNAME record:

| Type | Name | Value |
| --- | --- | --- |
| CNAME | the subdomain shown in Dokki, such as `docs` | `dokki-custom-domain-proxy.naxlab.xyz` |

Dokki also exposes a lightweight verification endpoint at `/__dokki_verify`. The Cloudflare Worker returns `x-dokki-proxy: true` there, and Dokki can use that as a fallback verification signal.

## How requests resolve

There are two supported paths:

- **Cloudflare Worker proxy** — the worker resolves the host to a site slug, rewrites the request to `/pub/<slug>`, and forwards headers such as `x-custom-domain`, `x-forwarded-host`, and `x-dokki-proxy`.
- **Direct custom-domain rewrite** — Dokki's Next proxy can resolve an active `published_sites.custom_domain` directly and rewrite the request to `/pub/<slug>`.

Resolved domains are cached briefly to avoid a database lookup on every request.

## Subdirectory publishing

Dokki also shows copy-ready examples for subdirectory publishing through an upstream host rewrite. For example, a Vercel rewrite can send `/docs/:path*` to:

```json
{ "source": "/docs/:path*", "destination": "https://dokki-custom-domain-proxy.naxlab.xyz/s/<site-slug>/docs/:path*" }
```

A Netlify-style redirect can send:

```text
/docs/*  https://dokki-custom-domain-proxy.naxlab.xyz/s/<site-slug>/docs/:splat  200
```

In subdirectory mode, the Worker forwards `x-subpath-base` so public links, canonical URLs, `robots.txt`, `sitemap.xml`, and `llms.txt` use the host and base path visitors actually see.

## Canonicals and discovery

Published pages use the active custom domain, direct `/pub/<slug>` address, or proxied subpath as the public base when building links and metadata. If a site is unlisted, it still receives noindex and crawler-blocking behavior on the custom domain.

## Removing a domain

Removing a custom domain clears it from the published site and attempts to delete the Cloudflare custom hostname. The site remains available at the default `/pub/<slug>` URL if it is active.

---

Published from Dokki.
