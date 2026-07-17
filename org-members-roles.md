---
title: "Org Members & Roles"
canonical: "https://dokki.one/pub/docs/org-members-roles"
source_url: "https://dokki.one/pub/docs/org-members-roles"
updated_at: "2026-07-10T03:58:30.32+00:00"
generated_by: Dokki
---

# Org Members & Roles

An organization has its own member list, separate from each workspace's member list. Organization roles govern account-level administration; workspace and resource roles still govern day-to-day conten

Canonical source: [https://dokki.one/pub/docs/org-members-roles](https://dokki.one/pub/docs/org-members-roles)

An organization has its own member list, separate from each workspace's member list. Organization roles govern account-level administration; workspace and resource roles still govern day-to-day content access.

## Visual guide

[Organization Governance Map](organization-governance-map.md)

## Organization roles

- **Super Admin** is stored as the owner role. Super Admins can manage every organization setting, invite admins, change privileged roles, remove admins, manage billing, and delete the organization. An organization must always keep at least one Super Admin.
- **Admin** can manage most organization operations, including members, workspaces, policies, AI controls, usage limits, audit access, and billing. Admins cannot grant or remove Admin/Super Admin privileges.
- **Member** belongs to the organization but does not manage organization settings. Members need workspace membership or explicit resource access to work inside organization workspaces.
- **Guest** is a legacy role. New invitations use Admin or Member; existing guest rows can be changed to current roles.

## Workspace roles still matter

Being an organization member does not automatically make someone an editor in every organization workspace. Workspace roles decide whether they are an admin, editor, or viewer in that workspace. Resource roles and private-resource settings can further narrow access.

## Invitations

Owners and admins invite people from organization settings. Invitable roles are Admin and Member, but only a Super Admin can invite another Admin. If the email belongs to an existing Dokki user, Dokki sends an organization invite notification. If it is new, Dokki uses Supabase's invite flow and creates the profile row needed for membership.

## Role changes and safeguards

Only Super Admins can grant, demote, or remove Super Admin/Admin tiers. Admins can manage ordinary members. Dokki blocks changes that would leave the organization without a Super Admin, and members cannot remove themselves through the remove-member endpoint.

## Offboarding

When an owner or admin removes a member, Dokki removes that user's memberships from the organization's workspaces. Resources, agents, and agent schedules created by the removed user inside those organization workspaces are transferred to the admin performing the removal. Personal work and work in other organizations are not touched.

## Account context

Organization members see the organization as a separate context from personal work. This keeps personal workspaces, personal chats, and organization workspaces from blending together.

---

Published from Dokki.
