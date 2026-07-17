---
title: "Chats"
canonical: "https://dokki.one/pub/docs/chats"
source_url: "https://dokki.one/pub/docs/chats"
updated_at: "2026-07-10T06:03:35.166+00:00"
generated_by: Dokki
---

# Chats

Chats in Dokki are part of the AI panel's unified conversation hub. The panel can show AI chats, agent threads, IM conversations, and notifications. This page covers the panel itself. For messaging pe

Canonical source: [https://dokki.one/pub/docs/chats](https://dokki.one/pub/docs/chats)

Chats in Dokki are part of the AI panel's unified conversation hub. The panel can show AI chats, agent threads, IM conversations, and notifications.

This page covers the panel itself. For messaging people and groups — direct messages, group conversations, workspace channels, and how agents reply in them — see **Messages**.

## Visual guide

[Copilot Turn Pipeline](copilot-turn-pipeline.md)

## Conversation list

The first panel level is a recent list. It combines:

| Row type | What it opens |
| --- | --- |
| **AI chats** | Saved Copilot conversations and installed-agent threads. |
| **Messages** | Direct messages and group conversations. |
| **Notifications** | A read-only notification stream. |

Rows are sorted by recency, with pinned rows floated to the top. You can group by type, sort for unread items, mark rows done, and reveal done rows from the view menu.

## Routing composer

The composer at the bottom of Home and the AI panel routes messages by target:

| Input | Route |
| --- | --- |
| Plain text | Starts a fresh Dokki Copilot chat. |
| `@agent` | Starts that agent's Copilot chat. |
| `@person` | Opens or creates an IM direct message. |
| `@group` | Posts to an IM group conversation. |

Images and supported files can be attached when the route is a Copilot or agent chat. IM routing sends text; attachments stay with Copilot routes.

## Saved and temporary chats

Normal Copilot chats create or reuse an AI session. Messages, tool calls, usage, compaction state, and memory review can be saved after the stream finishes.

Temporary chats run the turn without persisting a session or messages. They are useful for one-off questions that should not appear in chat history or feed memory review.

## Agent chats

Selecting an installed agent opens that agent's latest thread when one exists. Starting a new agent chat runs as that installed agent. The generic long-running agent mode can also run multi-step work without an installed agent identity.

## Queued turns and background streaming

If you send another message while a reply or agent run is still active, Dokki queues the turn and sends it when the current stream settles, as long as you are still in the same conversation.

## Notifications in the panel

Notifications are readable from the same panel but are not a chat. You can open, mark read, mark all read, or clear notifications; there is no composer in the notification stream.

---

Published from Dokki.
