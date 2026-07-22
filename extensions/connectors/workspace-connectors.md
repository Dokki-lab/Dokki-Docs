---
title: "Workspace Connectors"
canonical: "https://dokki.one/pub/docs/workspace-connectors"
source_url: "https://dokki.one/pub/docs/workspace-connectors"
updated_at: "2026-07-10T05:05:03.073+00:00"
generated_by: Dokki
---

# Workspace Connectors

Connectors are named, workspace-scoped MCP credentials. They let external clients and agents use a controlled Dokki endpoint without using your browser session. Visual guide MCP OAuth Scope Map Who ca

Canonical source: [https://dokki.one/pub/docs/workspace-connectors](https://dokki.one/pub/docs/workspace-connectors)

Connectors are named, workspace-scoped MCP credentials. They let external clients and agents use a controlled Dokki endpoint without using your browser session.

## Visual guide

[MCP OAuth Scope Map](../../reference/visual-library/mcp-oauth-scope-map.md)

## Who can manage connectors

Only workspace admins can create, list, or revoke connectors from **Workspace → Extensions → Connectors**. The settings route remains available for direct administration.

## Connector flavors

- **Documents** exposes workspace resources: documents, tables, artifacts, files, previews, search, knowledge graph, tagging, folders, sharing, and workspace channel coordination.
- **Publish** exposes publishing and custom-domain management for the workspace's public site.
- **Memory** exposes workspace-scoped long-term memory tools for adding, searching, listing, and deleting durable facts.

## Scope and auth model

Every connector URL includes the workspace id, connector id, and API key token. The token is shown once at creation time. Dokki stores only a hash and visible prefix afterward, so copy the generated token or client config before closing the dialog.

Connectors are workspace-locked. A Documents connector created for one workspace cannot read resources from another workspace. A Publish connector cannot manage another workspace's public site.

## Client snippets

After creation, Dokki can copy paste-ready snippets for MCP clients such as Claude Desktop, Codex CLI, and Codex App environment configuration. The snippet embeds the self-contained connector URL.

## Revocation and status

Revoking a connector sets it to revoked instead of deleting the row, so the workspace keeps a lightweight audit trail. The connector list shows active, expired, and revoked credentials, along with creation date and last-used date when available.

## When to create separate connectors

- Use separate connectors for different external clients or automation jobs.
- Use a Publish connector only for clients that should manage public-site state.
- Revoke credentials immediately if a token was exposed, copied into the wrong environment, or no longer needed.

---

Published from Dokki.
