---
title: "Notifications"
canonical: "https://dokki.one/pub/docs/notifications"
source_url: "https://dokki.one/pub/docs/notifications"
updated_at: "2026-07-10T04:49:57.417+00:00"
generated_by: Dokki
---

# Notifications

Notifications collect items that need your attention across Dokki. They are durable database rows, not local-only UI state. Visual guide Collaboration Governance Map Where notifications appear Notific

Canonical source: [https://dokki.one/pub/docs/notifications](https://dokki.one/pub/docs/notifications)

Notifications collect items that need your attention across Dokki. They are durable database rows, not local-only UI state.

## Visual guide

[Collaboration Governance Map](../reference/visual-library/collaboration-governance-map.md)

## Where notifications appear

Notifications appear in the topbar notification center and in the AI panel's **Notifications** view. The AI panel view is read-only: you can open and manage notifications there, but it has no message composer.

Dokki loads recent notifications from the server, keeps them live with Supabase realtime, and refetches when the browser tab regains focus.

## What appears in notifications

Notification categories include:

- **Mentions** — user mentions in documents, comments, or other supported surfaces.
- **Invites** — workspace invites, organization invites, and access-request decisions.
- **Agent runs** — background work that completed, failed, or needs attention.
- **Agent attention** — items an agent or workflow wants a human to notice.
- **Automation** — automation-related status or failure notifications.
- **System** — fallback category for anything that does not fit another type.

Each notification can include a title, message, actor, workspace id, resource link, and metadata.

## Access requests

Private-resource access requests appear as invite-category notifications with inline **Approve** and **Deny** actions. Approval grants the requested direct resource role. Denial closes the request and notifies the requester.

The same pending requests can also appear inside the resource share dialog for people who can manage that resource.

## Reading and clearing

You can mark one notification as read, mark all as read, clear one notification, or clear all notifications. Read state and deletion are synced back to the server on a best-effort basis.

Unread counts come from notifications without `read_at`. The message center keeps the local view responsive by applying optimistic updates before the server reply returns.

## Home reminders

Notifications carry workspace context when available. Home can use that workspace context to surface reminders and agent attention items for the active workspace.

## Good practice

Use notifications as an operational inbox, not long-term storage. Once a decision is made, capture the outcome in the relevant document, table, chat, resource, or task.

---

Published from Dokki.
