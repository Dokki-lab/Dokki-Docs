---
title: "Organizations"
canonical: "https://dokki.one/pub/docs/organizations"
source_url: "https://dokki.one/pub/docs/organizations"
updated_at: "2026-07-10T04:49:51.722+00:00"
generated_by: Dokki
---

# Organizations

An organization groups multiple workspaces under one account context, with its own member list, workspace inventory, governance policies, AI controls, audit surface, billing, and shared credit balance

Canonical source: [https://dokki.one/pub/docs/organizations](https://dokki.one/pub/docs/organizations)

An organization groups multiple workspaces under one account context, with its own member list, workspace inventory, governance policies, AI controls, audit surface, billing, and shared credit balance.

## Visual guide

[Organization Governance Map](organization-governance-map.md)

## In this section

- **Org Members & Roles** — invite people, assign Super Admin/Admin/Member roles, and understand offboarding behavior.
- **Workspaces** — view every organization workspace, including workspaces you have not personally joined, and control who can create new ones.
- **AI Controls** — choose allowed models, review 30-day usage, set daily spending limits, and audit organization chats.
- **Billing & Credits** — manage per-member organization billing and the shared AI credit pool.

## Personal versus organization context

Your personal context contains your own workspaces, private space, personal chats, personal agents, and personal billing. An organization context contains workspaces owned by that organization. Switching contexts changes which workspaces, chats, agents, billing settings, and organization controls you see.

Organization membership does not automatically grant editor access to every workspace. Workspace roles and resource roles still decide what a member can open, edit, comment on, or share inside each workspace.

## Organization settings tabs

Open **Org settings** from the account menu while an organization is selected. Current tabs are **General**, **Members**, **Workspaces**, **AI**, **Audit**, and **Billing**. Owners and admins can manage restricted tabs; regular members can view only member-appropriate organization details.

- **General** controls organization identity, logo, URL slug, workspace-creation policy, public template publishing policy, and owner-only organization deletion.
- **Members** manages organization membership, invitations, role changes, and member removal.
- **Workspaces** lists every workspace in the organization with member count, creator, creation date, and an Open action.
- **AI** controls the model allowlist, last-30-day member usage, organization default daily spending limit, and per-member daily limit. Limits are shown in US dollars even though the backend stores credits.
- **Audit** lets owners and admins review chats created in organization workspaces. Personal chats are never shown, and opening a chat is recorded in the access log.
- **Billing** manages the organization plan, billed member seats, renewal state, and shared AI credit balance.

## Organization policies

Owners and admins can control who may create organization workspaces. The policy can be set to all members, admins and owners, or owners only. They can also decide whether templates created from organization workspaces may be published publicly.

## Shared AI governance

Organization AI controls apply on top of each member's personal plan. The organization can restrict the model catalog, set default and per-member daily spend caps, and provide a shared AI balance for organization workspace usage. If the organization pool cannot cover a request, Dokki falls back to the member's personal plan where allowed.

## Knowledge Graph

Knowledge Graph is an experimental organization-level setting. In the current UI it lives in a hidden developer section on the General tab rather than as a normal member-facing control. When enabled, it starts background extraction across the organization's workspaces and can improve search and related-entity tools.

---

Published from Dokki.
