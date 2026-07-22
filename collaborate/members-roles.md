---
title: "Members & Roles"
canonical: "https://dokki.one/pub/docs/members-roles"
source_url: "https://dokki.one/pub/docs/members-roles"
updated_at: "2026-07-10T04:50:00.226+00:00"
generated_by: Dokki
---

# Members & Roles

Add people to a workspace and choose the baseline access they need. Visual guide Permission Resolution Map Invite members Open Settings -> Members and invite a person by email, then choose a workspace

Canonical source: [https://dokki.one/pub/docs/members-roles](https://dokki.one/pub/docs/members-roles)

Add people to a workspace and choose the baseline access they need.

## Visual guide

[Permission Resolution Map](../reference/visual-library/permission-resolution-map.md)

## Invite members

Open **Settings -> Members** and invite a person by email, then choose a workspace role. Existing Dokki users can be added directly; a new person receives an invitation and joins after creating an account.

Removing a member removes their workspace-level access immediately, but does not delete content they created. Review any direct resource roles separately, because those roles can remain after membership changes.

## Workspace roles

| Role | What it can do |
| --- | --- |
| Viewer | View normal workspace resources. |
| Editor | View and edit normal workspace resources; create and manage workspace tags. |
| Admin | Manage members, workspace settings, shared pins, and normal workspace content. |

Some older workspaces may contain a **manager** role. Dokki treats it as admin-equivalent in permission checks.

## Direct resource roles

Use the share dialog when one person needs access different from their workspace baseline. Direct roles are **Viewer**, **Commenter**, **Editor**, and **Admin**. The resource creator is also an owner for permission purposes.

On a normal resource, Dokki considers applicable direct roles, workspace membership, creator status, and public access. A direct Viewer role does not reduce an Editor's normal workspace permission. Use a private resource when a smaller audience must be enforced.

## Private-resource exception

Workspace membership alone does not reveal a private resource. It remains available to its creator, people with a direct resource role, workspace admins (and legacy managers), and people whose access request has been approved.

## Plans and organization policy

Plan limits can affect available workspaces, collaborators, storage, and AI credits. In organization workspaces, organization membership and workspace-creation policy can add another governance layer. See **Organizations** and **Pricing & Plans** for those settings.

---

Published from Dokki.
