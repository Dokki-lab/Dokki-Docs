---
title: "Agents"
canonical: "https://dokki.one/pub/docs/agents"
source_url: "https://dokki.one/pub/docs/agents"
updated_at: "2026-07-12T15:12:21.518+00:00"
generated_by: Dokki
---

# Agents

Agents are persistent AI teammates created from blueprints. Unlike a one-off Copilot prompt, an agent can keep its own instructions, optional memories, reusable skills, pinned context, MCP servers, wo

Canonical source: [https://dokki.one/pub/docs/agents](https://dokki.one/pub/docs/agents)

Agents are persistent AI teammates created from blueprints. Unlike a one-off Copilot prompt, an agent can keep its own instructions, optional memories, reusable skills, pinned context, MCP servers, workspace access rules, and recurring schedules.

## Visual guide

[Agent Control Panel Map](agent-control-panel-map.md)

## Start with a blueprint

Open **Workspace → Agents → Blueprints**, choose a blueprint, then install a personal or organization-tenant agent. The built-in catalog currently includes Research Analyst, Technical Writer, Knowledge Curator, Data Analyst, Project Coordinator, Meeting Scribe, and SEO Agent. A blueprint is a starting configuration: its instructions, capabilities, suggested skills, and optional MCP server defaults can all be reviewed and adjusted after installation.

## Ownership and tenant boundary

Agents are **private to their owner**. Selecting an organization changes the tenant in which the agent operates; it does not make that agent visible or editable by every organization member. The Agents dashboard lists the signed-in user's agents for the current personal or organization context.

An agent acts with its owner's workspace reach inside the matching tenant. In the **Workspaces** tab, the owner can keep that full reach or turn on an allowlist and grant a smaller set of workspaces read or write access. Archived workspaces are excluded. This is the practical boundary to review before assigning an agent recurring work.

## Control panel

Open an installed agent to manage:

- **Overview**: schedules and a paginated activity history with trigger, prompt/output previews, status, model, and errors.
- **Settings**: identity, description, model, standing instructions, maximum steps, idle timeout, memory, and workspace-skill loading.
- **Memory**: explicit durable facts for this agent when memory is enabled.
- **Skills**: reusable instruction documents attached to the agent.
- **Pinned**: up to 20 documents, tables, or artifacts supplied as persistent context, each with an optional note.
- **MCP**: external MCP servers, using no authentication, request headers, or OAuth where the server supports it.
- **Workspaces**: the effective owner-derived reach and the optional allowlist restriction.

Only the owner can open and manage an installed agent's control panel. Pause an agent to stop its active intent; its schedules remain visible and can be enabled, disabled, or removed separately.

## How work starts

Use the Copilot's agent selector or routing composer to begin an agent conversation. Scheduled tasks create their own queued runs at the configured time. The activity timeline distinguishes chat and scheduled runs, so it is the authoritative place to inspect the result of a task instead of assuming that an agent changed a resource.

See **Install & Customize**, **Memory, Skills & Connections**, and **Runs & Schedules** for the operational details.

---

Published from Dokki.
