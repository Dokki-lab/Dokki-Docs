---
title: "Billing & Credits"
canonical: "https://dokki.one/pub/docs/billing-credits"
source_url: "https://dokki.one/pub/docs/billing-credits"
updated_at: "2026-07-10T02:09:44.608+00:00"
generated_by: Dokki
---

# Billing & Credits

Organization billing keeps company usage separate from personal plans. It combines per-member organization billing with a shared AI credit pool. Shared billing An organization can stay on Free or upgr

Canonical source: [https://dokki.one/pub/docs/billing-credits](https://dokki.one/pub/docs/billing-credits)

Organization billing keeps company usage separate from personal plans. It combines per-member organization billing with a shared AI credit pool.

## Shared billing

An organization can stay on Free or upgrade to the organization Team plan from the Billing tab. The organization Team plan is billed per member: one Stripe subscription item tracks the current organization member count. Seats sync automatically after members are added or removed.

Any organization member can view the billing state. Only owners and admins can start checkout, open the billing portal, or buy organization credits.

## Per-member seats

Organization billing is pure per-head billing. It is different from workspace Team billing, which uses a workspace base price and sponsored-seat budget. In organization billing, every organization member counts toward the billed headcount shown on the Billing tab.

The exact per-member price is read from Stripe and displayed in the app when configured. Treat the billing screen and Stripe checkout as authoritative for current price, renewal, cancellation, and taxes.

## Shared AI balance

The Billing tab shows the organization's shared AI balance in dollars. Internally the balance is stored as credits, where 1,000 credits equals $1. Organization AI usage in organization workspaces draws from this pool first. When it runs out, members fall back to their personal plans where allowed.

## Credit bundles

Owners and admins can add one-time credit bundles to the organization pool:

- $10 adds 10,000 credits.
- $50 adds 50,000 credits.
- $200 adds 200,000 credits.

These are shared Stripe credit products routed to the organization pool by checkout metadata.

## Member limits

Use the AI tab to set a default daily organization spending limit and per-member overrides. Limits are shown in dollars in the UI and stored as credits in the backend. Empty limits mean unlimited within the organization's available balance and plan rules.

## Personal plan fallback

If the organization pool cannot cover an AI request, Dokki may fall back to the member's personal plan. For clean accounting, keep company work inside organization workspaces and keep the organization balance funded.

---

Published from Dokki.
