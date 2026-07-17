---
title: "Install and Customize"
canonical: "https://dokki.one/pub/docs/install-and-customize"
source_url: "https://dokki.one/pub/docs/install-and-customize"
updated_at: "2026-07-10T04:50:22.229+00:00"
generated_by: Dokki
---

# Install and Customize

Install an agent from a blueprint, then adapt its instructions and operating boundaries before relying on it for recurring work. Visual guide Agent Control Panel Map Install from Blueprints Go to Work

Canonical source: [https://dokki.one/pub/docs/install-and-customize](https://dokki.one/pub/docs/install-and-customize)

Install an agent from a blueprint, then adapt its instructions and operating boundaries before relying on it for recurring work.

## Visual guide

[Agent Control Panel Map](agent-control-panel-map.md)

## Install from Blueprints

1. Go to **Workspace → Agents → Blueprints**.
1. Open a blueprint to review its description, capabilities, instructions, included skill documents, and any suggested MCP server.
1. Choose the personal or organization tenant, give the agent a name, and select a home workspace when the setup needs a place to seed blueprint skill documents.
1. Complete the install, then open the agent's control panel to set its workspace reach, connections, and schedule.

Eligibility to create an organization agent follows that organization's agent-creation policy. The default policy allows members and above, but an organization can set a stricter requirement. Personal agents do not use an organization role check.

The home workspace is a storage location for generated setup material, not a blanket access grant. The agent's usable workspaces are derived from the owner's memberships in the same tenant and can be narrowed later in the **Workspaces** tab.

## Settings worth reviewing

In **Settings**, set the agent's name, description, model, standing instructions, maximum steps per run, and idle timeout. You can also enable or disable durable agent memory and choose whether workspace skills are loaded in addition to the agent's own skills.

Treat the standing instructions as the agent's operating brief: define its goal, output format, constraints, and escalation rules there. Keep credentials out of the prompt and memory; configure them through the relevant MCP connection instead.

## Connect only what the job needs

The **MCP** tab accepts a server URL and one of three authentication modes: none, request headers, or OAuth. For OAuth servers, add the server first and use **Connect** to finish authorization. Header values are stored as configuration and are not shown again in the panel; rotate them at the provider if exposure is suspected.

Use the **Skills** and **Pinned** tabs for stable, auditable guidance. Pin only documents, tables, and artifacts that should be considered on every run. Use a skill document for a repeatable procedure rather than duplicating the procedure in every chat prompt.

## Pause or uninstall

The owner can pause or resume an agent from its card or control panel. Pausing stops the agent's active intent; review and disable its individual schedules as appropriate. Uninstall deletes the installed agent, so review its timeline and retain any output you need before removing it.

---

Published from Dokki.
