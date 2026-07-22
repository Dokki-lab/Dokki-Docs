---
title: "AI Controls"
canonical: "https://dokki.one/pub/docs/ai-controls"
source_url: "https://dokki.one/pub/docs/ai-controls"
updated_at: "2026-07-10T03:58:28.468+00:00"
generated_by: Dokki
---

# AI Controls

Organization AI controls shape how members use AI across organization workspaces. They apply on top of each member's plan; they do not replace plan-tier model access, quota windows, or personal billin

Canonical source: [https://dokki.one/pub/docs/ai-controls](https://dokki.one/pub/docs/ai-controls)

Organization AI controls shape how members use AI across organization workspaces. They apply on top of each member's plan; they do not replace plan-tier model access, quota windows, or personal billing rules.

## Visual guide

[Organization Governance Map](../reference/visual-library/organization-governance-map.md)

## Allowed models

Owners and admins can choose which models are allowed in the organization. If the allowlist is empty or unset, all globally enabled models remain allowed, subject to each member's plan. If a subset is saved, only those model IDs can be used in organization workspaces and organization-scoped agents.

The model picker reads the live model catalog, so model names and availability can change without a documentation update. Use the organization AI models screen as the source of truth for the current catalog.

## Spending limits

Organizations can set a default daily AI spending limit and per-member overrides. Empty limits mean unlimited within the available organization balance and plan rules. The UI shows limits in US dollars; the backend stores them as credits, with 1,000 credits equal to $1.

## Usage review

The Usage & limits view aggregates the last 30 days of AI usage for the organization by member. It shows message counts, spend, the organization default daily limit, and each member's override. Only owners and admins can view or edit this surface.

## Shared balance and fallback

AI work in organization workspaces can draw from the organization's shared AI balance. If the organization balance cannot cover the request, Dokki falls back to the member's personal plan where allowed. For clean accounting, keep organization work inside organization workspaces.

## Audit

Owners and admins can review chats created in organization workspaces from the Audit tab. Personal chats and org-less sessions are never returned. Listing sessions and opening a specific chat are recorded in the organization access log.

## Knowledge Graph

Knowledge Graph is controlled at the organization level and is currently experimental. When enabled, it starts background extraction across the organization's workspaces and can improve search and related-entity tools.

## Good practice

Start with a smaller model allowlist for production workspaces, set a default daily spending limit, and add per-member overrides for heavy agent users or teams with stricter budgets.

---

Published from Dokki.
