---
title: "Connectors"
canonical: "https://dokki.one/pub/docs/connectors"
source_url: "https://dokki.one/pub/docs/connectors"
updated_at: "2026-07-20T11:10:35.91+00:00"
generated_by: Dokki
---

# Connectors

Connectors are the credentials and endpoints that allow an external AI client or automation to use Dokki. The best connector is the one that gives the required access without opening unrelated workspa

Canonical source: [https://dokki.one/pub/docs/connectors](https://dokki.one/pub/docs/connectors)

Connectors are the credentials and endpoints that allow an external AI client or automation to use Dokki. The best connector is the one that gives the required access without opening unrelated workspaces.

## Choose the connection type

- **OAuth** — best for interactive clients used by a person. Access follows the account and choices made during sign-in.
- **API key** — useful for a trusted script or service that needs a reusable credential.
- **Workspace connector** — best when an automation should work only inside one named workspace.

## Set up and test

- Create the connection from **Connect → AI Clients**.
- Copy only the URL or credential requested by the client.
- Store credentials in the client's secure credential settings, not in documents or chat messages.
- Test by listing or reading a known resource before allowing edits.

## Control access

A connector does not override Dokki roles. The connected client can work only within the access granted to that connection and the acting user or workspace.

## Rotate or remove a connector

Replace a credential when it may have been exposed, when ownership changes, or when the client no longer needs access. Update the client after rotation and remove the old connection.

## Troubleshooting

- **Unauthorized** — sign in again or replace the expired credential.
- **Forbidden** — the connection or acting user does not have the required workspace or resource role.
- **Not found** — confirm the client is using the intended Dokki URL and workspace.

---

Published from Dokki.
