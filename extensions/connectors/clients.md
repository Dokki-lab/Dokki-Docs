---
title: "Clients"
canonical: "https://dokki.one/pub/docs/clients"
source_url: "https://dokki.one/pub/docs/clients"
updated_at: "2026-07-20T11:10:34.707+00:00"
generated_by: Dokki
---

# Clients

AI Clients let supported external assistants and tools work with Dokki. Connect only clients you trust, and give each one the smallest access needed for its job. Set up an AI client Open Connect → AI

Canonical source: [https://dokki.one/pub/docs/clients](https://dokki.one/pub/docs/clients)

AI Clients let supported external assistants and tools work with Dokki. Connect only clients you trust, and give each one the smallest access needed for its job.

## Set up an AI client

- Open **Connect → AI Clients**.
- Choose the client or connection method you want to use.
- Follow the displayed instructions to sign in or add the connection details to the client.
- Select the organization or workspace access the client needs.
- Start with a read request to confirm that the connection reaches the expected workspace.

## Choose a connection method

- Use **OAuth** when the client supports browser sign-in and you want access tied to your Dokki account.
- Use an **API key** for a trusted tool that requires a key and has a clearly defined scope.
- Use a **workspace connector** when an automation should be limited to one workspace.

## Review recent activity

The AI Clients page can show recent use observed from connected clients. Use this to find clients that are active or unexpectedly quiet. An activity entry does not mean a connection still has permission; review the connection itself when access needs to change.

## Remove access

Revoke or delete a connection when a device, tool, or owner changes. Removing one client connection does not remove the underlying Dokki resources.

## Troubleshooting

- If sign-in fails, restart the setup from the AI Clients page.
- If the client reaches the wrong workspace, remove the connection and create one with the correct scope.
- If a write is denied, confirm both the connection scope and your role on the target resource.

---

Published from Dokki.
