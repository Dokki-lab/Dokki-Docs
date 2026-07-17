---
title: "Tools and Capabilities"
canonical: "https://dokki.one/pub/docs/tools-and-capabilities"
source_url: "https://dokki.one/pub/docs/tools-and-capabilities"
updated_at: "2026-07-10T04:50:09.685+00:00"
generated_by: Dokki
---

# Tools and Capabilities

Copilot is more than a chat box. It can call tools that read and change Dokki resources, search knowledge, publish content, generate media, schedule work, and use external apps. Visual guide Copilot T

Canonical source: [https://dokki.one/pub/docs/tools-and-capabilities](https://dokki.one/pub/docs/tools-and-capabilities)

Copilot is more than a chat box. It can call tools that read and change Dokki resources, search knowledge, publish content, generate media, schedule work, and use external apps.

## Visual guide

[Copilot Turn Pipeline](copilot-turn-pipeline.md)

## Tool groups

| Group | Examples |
| --- | --- |
| **Navigation and resources** | List workspaces/resources; create, rename, move, delete, tag, and untag resources. |
| **Search and retrieval** | Semantic search, exact grep, related entities, document/table/artifact reads, and web search when Exa is configured. |
| **Document editing** | Read, insert, replace, rewrite, or delete document nodes. |
| **Table editing** | Add/delete rows and columns, update columns, and update cells. |
| **Artifact editing** | Read, replace, or patch artifact source. |
| **Image tools** | Generate images and edit images when the image provider is configured. |
| **Publishing** | Create/update publish sites, publish/unpublish resources, list published resources, manage custom domains, and check domain status. |
| **Tasks and schedules** | Sync/read/clear chat todos and create/list/update/delete scheduled agent tasks. |
| **Agent-only tools** | Pinned resources, IM messaging, and attention flags when running as an agent identity. |
| **External apps** | Composio Tool Router tools for the acting user's connected apps. |

## Tool availability

Copilot can see the tool schemas it may need for the turn, but each tool still performs its own permission, resource, and provider-configuration checks before doing work.

A visible tool does not mean the model can bypass permissions. It means Copilot knows the operation exists and can request it when the current user, resource, plan, and workspace context allow it.

## Search and retrieval

Copilot can search semantically, grep exact strings, read documents, read tables, read artifacts, and use Knowledge Graph related entities when enabled. It can also use Exa-backed web search and URL crawling when `EXA_API_KEY` is configured.

## Editing and creation

Copilot can create documents, tables, artifacts, and folders. It can edit documents, tables, and artifacts with resource-specific tools. For focused resources, the relevant tool family has the strongest local context, but Copilot can still operate on other accessible resources when given IDs or search results.

## Connected apps

Composio integrations are loaded as external tools for the acting user. In the composer, `@`-mentioning a connected app/toolkit narrows the Composio tool session for that turn to the mentioned toolkit slugs. If no toolkit is mentioned, the user's connected toolkits may be available broadly.

Connected app tools are account-scoped. Other workspace members do not inherit your personal connection.

## Agent tools

Installed agents can run with extra tool families: agent schedules, pinned resources, IM tools, attention flags, and per-agent MCP servers. Agent MCP connection failures are non-fatal; Dokki records the failed server and continues with the tools that connected.

## Permission boundaries

Tools do not bypass Dokki permissions. Private resources, inaccessible organization workspaces, archived workspaces, organization model controls, and public/private visibility rules are enforced before content is shown to the assistant or changed by a tool.

---

Published from Dokki.
