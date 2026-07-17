---
title: "Private Documents"
canonical: "https://dokki.one/pub/docs/private-documents"
source_url: "https://dokki.one/pub/docs/private-documents"
updated_at: "2026-07-10T04:49:59.201+00:00"
generated_by: Dokki
---

# Private Documents

Private resources are hidden from the broader workspace unless someone has direct access or admin authority. The feature applies across resource types, even if an older label in the UI still says "doc

Canonical source: [https://dokki.one/pub/docs/private-documents](https://dokki.one/pub/docs/private-documents)

Private resources are hidden from the broader workspace unless someone has direct access or admin authority.

The feature applies across resource types, even if an older label in the UI still says "document" in a few places.

## Visual guide

[Permission Resolution Map](permission-resolution-map.md)

## What private means

A private resource does not appear in the normal sidebar, search results, Copilot context, or MCP results for workspace members who are not allowed to see it.

A private resource remains visible to:

- Its creator.
- Users with a direct resource role.
- Workspace admins and legacy managers.
- Users whose access request was approved.

A plain workspace viewer or editor role is not enough for a private resource. That is the key difference from normal workspace resources.

## Requesting access

If someone opens a private resource link without access, Dokki shows a request access screen. The same compact request flow appears for embedded resources that the viewer cannot open.

The requester can ask for viewer, commenter, or editor access. If no role is specified, Dokki requests viewer access.

## Approving access

Approvers can act from the notification center or the share dialog's access request section. Approval grants the requested direct resource role. Denial closes the request and sends a notification back to the requester.

## Sharing a private resource

Open sharing controls and add people directly. You can grant view, comment, edit, or admin/full-access roles.

Changing general access away from private makes the resource visible to the selected broader audience. Enabling a public link also clears the private flag.

## Private versus archived

Private controls who can see one resource. Archive controls whether an entire workspace is active. Archived workspaces are hidden from normal switching, excluded from MCP OAuth consent pickers, and background jobs stop; private resources can still live inside active workspaces.

---

Published from Dokki.
