---
title: "Connected Apps"
canonical: "https://dokki.one/pub/docs/connected-apps"
source_url: "https://dokki.one/pub/docs/connected-apps"
updated_at: "2026-07-12T15:12:28.258+00:00"
generated_by: Dokki
---

# Connected Apps

Connected Apps let Copilot and agents use external services through your account. Dokki currently uses Composio for account-level integrations. Visual guide Copilot Turn Pipeline Account-level connect

Canonical source: [https://dokki.one/pub/docs/connected-apps](https://dokki.one/pub/docs/connected-apps)

Connected Apps let Copilot and agents use external services through your account. Dokki currently uses Composio for account-level integrations.

## Visual guide

[Copilot Turn Pipeline](copilot-turn-pipeline.md)

## Account-level connections

Connected Apps are tied to your Dokki user account. A workspace can use a connected app only through a user or agent acting with an access path to that account. Other workspace members do not automatically inherit your personal OAuth or API-key connection.

If Composio is not configured for the deployment, the Connected Apps screen shows a disabled/not-configured state instead of failing the page.

## Browsing apps

Open **Account -> Connected Apps** to browse available toolkits. The catalog can include hundreds of services, so the UI supports:

- Search by app name or toolkit slug.
- Category tabs, showing the most common categories first.
- A capped default grid for performance, with search/category filtering to narrow the list.
- Status badges for connected apps.

The toolkit catalog is cached for performance and can serve the last good list if Composio has a transient failure.

## Connecting

Click an app to start its connection flow. Dokki creates or reuses the toolkit's Composio auth configuration and opens a hosted Connect Link or OAuth page in a new browser tab.

Some toolkits use Composio-managed OAuth. Others collect API keys, bearer tokens, or other credentials on the hosted connection page. Dokki does not expose those credentials to other workspace members.

After a connection is created, Dokki invalidates the user's cached Composio tool session so the next Copilot turn can see the newly available tools.

## Using an app in Copilot

Connected apps appear in the Copilot `@` mention picker as MCP/toolkit targets. Mentioning one or more toolkits scopes that turn's external tools to those slugs. This is the safest way to tell Copilot which outside service it should use.

If no toolkit is mentioned, Copilot may load the acting user's available Composio tools more broadly.

## Disconnecting

Disconnecting removes the connected account through Composio and invalidates the cached tool session. Future Copilot turns cannot use that connection. Past chat messages, tool transcripts, and activity records remain as history.

## Connected Apps versus MCP Connections

Connected Apps are user-account integrations for external services like GitHub, Slack, Gmail, calendars, and issue trackers.

MCP Connections are Dokki-facing or agent-facing protocol connections: external clients can connect to Dokki through MCP, workspace admins can create workspace-scoped connector credentials, and agents can be configured with their own MCP servers.

Use Connected Apps when Copilot should act as you in a third-party service. Use MCP Connections when an external AI client needs access to Dokki or an agent needs a managed MCP server.

---

Published from Dokki.
