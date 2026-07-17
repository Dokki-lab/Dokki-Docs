---
title: "Connectors"
canonical: "https://dokki.one/pub/docs/connectors"
source_url: "https://dokki.one/pub/docs/connectors"
updated_at: "2026-07-12T15:12:26.905+00:00"
generated_by: Dokki
---

# Connectors

Model Context Protocol (MCP) lets an external AI client work with Dokki, and lets a Dokki agent use an external MCP server. These are separate directions: this section covers exposing Dokki's own MCP

Canonical source: [https://dokki.one/pub/docs/connectors](https://dokki.one/pub/docs/connectors)

Model Context Protocol (MCP) lets an external AI client work with Dokki, and lets a Dokki agent use an external MCP server. These are separate directions: this section covers exposing Dokki's own MCP servers to a client such as Codex, Claude, Cursor, or a custom automation.

## Visual guide

[MCP OAuth Scope Map](mcp-oauth-scope-map.md)

## Dokki's MCP surfaces

The unified **Documents MCP** endpoint can list and search workspace content; read documents, tables, artifacts, and files; request rendered previews; create and update supported resources; manage tags and folders; share resources; and use workspace channel tools. Knowledge-graph tools appear only where the organization has enabled Knowledge Graph.

Dokki also has focused **Publish** and **Memory** MCP surfaces. Publish covers site, published-resource, and custom-domain operations. Memory provides durable workspace-scoped fact operations. Which surface a client receives depends on its credential type.

## Choose the credential model

### OAuth for interactive clients

Remote OAuth is the best default for a person connecting a supported MCP client. During the Dokki consent screen, choose one or more allowed contexts: Personal, organizations, and/or specific non-archived workspaces. The selected scope is enforced on subsequent tool calls and can be narrowed without relying on a client-side convention.

### API key for a single tenant

An API key begins with `dk_` and is tied to either Personal or one organization. Create and revoke keys in **Account settings**, or open **Workspace → Extensions** and select **Set up a client...**. It is appropriate for a client configuration that must not require an interactive OAuth grant, but it cannot be limited to an individual workspace. The raw key is shown only at creation time.

### Workspace connector for automation

A connector is an admin-managed credential locked to exactly one workspace. Its generated URL carries the workspace, connector, and token information, and Dokki rejects a different workspace, resource, or publish site even if a caller supplies one. Use it for a CI job, a shared local configuration, or a client that needs a fixed workspace endpoint.

## Permission and scope checks

Scope determines the tenant or workspace that a credential may address. Dokki then applies the relevant resource and workspace checks for the acting identity. Do not treat an OAuth grant, API key, or connector as a universal bypass: choose the smallest scope and revoke it when the client, machine, or automation is no longer trusted.

See **Clients** for external MCP client setup, **Workspace Connectors** for the three workspace connector flavors, **Connected Apps** for services that Copilot can use, and **Chat Channels** for talking to your Dokki Agent from Weixin.

---

Published from Dokki.
