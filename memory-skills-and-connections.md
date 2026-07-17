---
title: "Memory, Skills and Connections"
canonical: "https://dokki.one/pub/docs/memory-skills-and-connections"
source_url: "https://dokki.one/pub/docs/memory-skills-and-connections"
updated_at: "2026-07-10T04:50:22.805+00:00"
generated_by: Dokki
---

# Memory, Skills and Connections

Three things make an agent more than a one-off chat: what it remembers, what it knows how to do, and what it can connect to. Visual guide Agent Control Panel Map Memory Agent memory stores durable fac

Canonical source: [https://dokki.one/pub/docs/memory-skills-and-connections](https://dokki.one/pub/docs/memory-skills-and-connections)

Three things make an agent more than a one-off chat: what it remembers, what it knows how to do, and what it can connect to.

## Visual guide

[Agent Control Panel Map](agent-control-panel-map.md)

## Memory

Agent memory stores durable facts and preferences that should carry across runs. Use it for stable context such as team conventions, product names, writing style, recurring workflows, or long-lived project facts.

Do not put secrets in memory. Use managed connections or environment configuration for credentials.

## Skills

Skills package instructions for a repeatable kind of work. A skill can define how the agent should review a document, triage updates, prepare a report, use a tool, or follow a workspace-specific process.

Good skills are narrow, explicit, and easy to audit.

## Workspace resources

Agents can use pinned resources, documents, tables, artifacts, files, and search results as context when permissions allow it. Private resources remain private unless the agent and current run have access.

## Connections

Agents can use MCP connections and connected apps. MCP connections are managed at the workspace or agent level. Connected Apps are account-level integrations that let an assistant act through an authorized user.

## Attention flags

Agents can flag a resource for attention. These flags show up as reminders on Home and as notifications so a human can review the result.

---

Published from Dokki.
