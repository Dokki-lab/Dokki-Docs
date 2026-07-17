---
title: "Sharing & Public Access"
canonical: "https://dokki.one/pub/docs/sharing-public-access"
source_url: "https://dokki.one/pub/docs/sharing-public-access"
updated_at: "2026-07-10T04:49:59.667+00:00"
generated_by: Dokki
---

# Sharing & Public Access

Share one resource with a defined person, open it to anyone with a link, or keep it private. Publishing to a public site is a separate workflow. Visual guide Permission Resolution Map Direct sharing O

Canonical source: [https://dokki.one/pub/docs/sharing-public-access](https://dokki.one/pub/docs/sharing-public-access)

Share one resource with a defined person, open it to anyone with a link, or keep it private. Publishing to a public site is a separate workflow.

## Visual guide

[Permission Resolution Map](permission-resolution-map.md)

## Direct sharing

Open the share dialog and choose **Viewer**, **Commenter**, **Editor**, or **Admin** for a person. The resource creator, a direct resource admin, or a workspace admin can manage direct sharing.

For an existing Dokki user, Dokki sends an email and an in-app notification. For a new person, it sends an invitation email; after they accept it, the chosen resource and role are available to them.

Direct roles add access. On a normal resource, they do not reduce a stronger applicable workspace role. Use **Private** when direct sharing must be the main access path.

## General access and link sharing

General access controls a broader audience:

| Setting | Effect |
| --- | --- |
| Private | Only the creator, direct role holders, workspace admins, and approved requesters can open it. |
| Link: view | Anyone with the link can view the source resource. |
| Link: comment | Anyone with the link can view and comment. |
| Link: edit | Anyone with the link can view and edit. |

Private access and a public link are mutually exclusive. Enabling a link clears the private setting; making the resource private clears its public link.

## Access requests

When a signed-in person opens a private resource without access, Dokki offers **Request access**. The request can ask for Viewer, Commenter, or Editor access; Viewer is the default. Resource managers can approve or decline from the notification center or the share dialog. Approval creates the requested direct role, and Dokki notifies the requester of either outcome.

## Publishing is different

Publishing freezes a document, table, or artifact into a public site snapshot. A published page does not grant edit access to the source resource, and source link-sharing does not update an already-published snapshot.

---

Published from Dokki.
