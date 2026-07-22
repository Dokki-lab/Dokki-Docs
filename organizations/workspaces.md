---
title: "Workspaces"
canonical: "https://dokki.one/pub/docs/workspaces"
source_url: "https://dokki.one/pub/docs/workspaces"
updated_at: "2026-07-10T03:58:32.723+00:00"
generated_by: Dokki
---

# Workspaces

Organization workspaces belong to the organization account context. They share organization policies, billing context, model controls, audit scope, credit pool behavior, and storage settings. Visual g

Canonical source: [https://dokki.one/pub/docs/workspaces](https://dokki.one/pub/docs/workspaces)

Organization workspaces belong to the organization account context. They share organization policies, billing context, model controls, audit scope, credit pool behavior, and storage settings.

## Visual guide

[Organization Governance Map](../reference/visual-library/organization-governance-map.md)

## Creating workspaces

Organization policy decides the minimum role allowed to create new workspaces:

- All members
- Admins and Super Admins
- Super Admins only

The default policy allows members to create workspaces. Use a stricter policy when you want centralized workspace governance.

## Workspace inventory

Owners and admins can open the organization Workspaces tab to see every workspace in the organization, including workspaces they have not personally joined. The list shows the workspace name, icon, slug, creator, creation date, and member count. This admin inventory is broader than the sidebar switcher, which only shows workspaces the current user belongs to.

## Workspace membership

Each organization workspace has its own members and roles. Add only the people who need access. Organization membership alone is not a blanket editor role, and private resources can still restrict visibility inside a workspace.

## Templates

Organizations can allow or restrict public template publishing. Turning public template publishing off prevents templates created from organization workspaces from being published to the public marketplace. Members can still use available templates when creating workspaces if they have permission to create the workspace.

## Archive

Archive inactive organization workspaces instead of deleting them. Archived workspaces are hidden from normal lists and stop background jobs until restored.

---

Published from Dokki.
