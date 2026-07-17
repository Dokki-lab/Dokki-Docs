---
title: "Copilot"
canonical: "https://dokki.one/pub/docs/copilot"
source_url: "https://dokki.one/pub/docs/copilot"
updated_at: "2026-07-10T04:50:11.244+00:00"
generated_by: Dokki
---

# Copilot

Copilot is Dokki's AI conversation surface. It can answer questions, work with the resources you can access, create or edit workspace content through tools, use eligible connected apps, and route long

Canonical source: [https://dokki.one/pub/docs/copilot](https://dokki.one/pub/docs/copilot)

Copilot is Dokki's AI conversation surface. It can answer questions, work with the resources you can access, create or edit workspace content through tools, use eligible connected apps, and route long-running work to agents.

## Visual guide

[Copilot Turn Pipeline](copilot-turn-pipeline.md)

## In this section

- **Chats** - persistent and temporary AI chats, agent threads, queued turns, IM, and notifications in the unified panel.
- **Models & Usage** - live model catalog, Auto routing, plan and organization gates, credits, and Extra Usage.
- **Tools & Capabilities** - resource, retrieval, publishing, external-app, and agent tool boundaries.
- **Inline AI & Vibe** - editor-local Vibe and Tab completion behavior.
- **Connected Apps** - personal third-party connections used by Copilot or agents.

## Context starts from the surface

Home starts from workspace context. A document, table, or artifact surface can contribute local context. A selected agent routes the conversation through that agent's configured identity. Attached text-like files are extracted into a message part; images require a vision-capable model.

The panel distinguishes normal Copilot chats, installed-agent chats, IM conversations, and notifications. Notifications are readable and manageable there but do not have a message composer.

## Sessions and long-running work

Normal chats persist sessions and messages after a stream settles. Temporary chats run without persisting a session or messages. When another turn is sent during an active stream, it is queued for the same conversation.

For multi-step work, use an installed agent or long-running agent mode. Agent runs can use their configured memory, skills, pinned resources, schedules, MCP servers, and attention signals.

## Boundaries

Copilot and its tools do not bypass resource permissions, archived-workspace exclusion, organization scope, model allowlists, plan gates, or external-app authorization. A tool call in the transcript is an auditable operation summary, not proof that every requested action succeeded.

---

Published from Dokki.
