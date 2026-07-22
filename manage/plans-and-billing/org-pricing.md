---
title: "Org Pricing"
canonical: "https://dokki.one/pub/docs/org-pricing"
source_url: "https://dokki.one/pub/docs/org-pricing"
updated_at: "2026-07-10T04:49:52.207+00:00"
generated_by: Dokki
---

# Org Pricing

Organization pricing is managed from organization billing settings. The billing screen and Stripe checkout are authoritative for exact price, renewal state, cancellation timing, and availability. Visu

Canonical source: [https://dokki.one/pub/docs/org-pricing](https://dokki.one/pub/docs/org-pricing)

Organization pricing is managed from organization billing settings. The billing screen and Stripe checkout are authoritative for exact price, renewal state, cancellation timing, and availability.

## Visual guide

[Home Workspace Map](../../reference/visual-library/home-workspace-map.md)

## What organization billing covers

Organization billing covers the organization account context: members, organization workspaces, model controls, spending limits, audit access, and a shared AI balance. It is designed for company-level governance rather than for a single workspace.

## Per-member subscription

The organization Team plan is billed per member. Checkout creates one Stripe subscription item with quantity equal to the current organization member count. After members are added or removed, Dokki syncs the Stripe item quantity to the new member count with prorations.

This is not the same as workspace Team pricing. Organization billing does not use a workspace base price or sponsored-seat concept.

## Credits

Organizations can buy shared AI credit bundles. Organization-scoped AI usage attempts to debit the organization pool first, then falls back according to the member's available personal plan rules.

Credit bundles are one-time purchases:

- $10 adds 10,000 credits.
- $50 adds 50,000 credits.
- $200 adds 200,000 credits.

The UI shows the pool as dollars, and the backend stores credits at 1,000 credits per $1.

## Limits and controls

Owners and admins can configure model availability and daily usage limits. These controls sit above workspace usage and help prevent unexpected spend across teams. The usage view aggregates the last 30 days of organization AI usage by member.

## Who can manage billing

Any organization member can view billing status. Owners and admins can start checkout, manage billing in Stripe, and buy organization credits.

## Pricing source of truth

The organization seat price is read live from Stripe. If the price is not configured or Stripe is unavailable, the app may hide the amount and still show member count and plan state. Treat the billing screen, Stripe checkout, and plan-specific notices shown in the app as authoritative.

---

Published from Dokki.
