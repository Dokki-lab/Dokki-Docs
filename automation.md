---
title: "Automation"
canonical: "https://dokki.one/pub/docs/automation"
source_url: "https://dokki.one/pub/docs/automation"
updated_at: "2026-07-10T04:54:25.713+00:00"
generated_by: Dokki
---

# Automation

Automation is the code-backed routine capability inside Extensions. Use it for repeatable workspace work that needs a visible handler, a defined trigger, and reviewable run history. Visual guide Autom

Canonical source: [https://dokki.one/pub/docs/automation](https://dokki.one/pub/docs/automation)

Automation is the code-backed routine capability inside Extensions. Use it for repeatable workspace work that needs a visible handler, a defined trigger, and reviewable run history.

## Visual guide

[Automation Lifecycle Diagram](automation-lifecycle-diagram.md)

## Open Automation

Open **Workspace → Extensions → Automation**. Create a routine, describe the outcome to the built-in AI assistant, then review or edit the generated JavaScript before saving it.

## What an automation contains

- A name and optional description.
- An enabled or draft state.
- A trigger type with its configuration.
- A JavaScript handler.
- A reviewable run history.

## Trigger support

Manual runs and scheduled cron runs are the supported production triggers. Event and webhook trigger types can be stored in the editor, but the current product does not expose a workspace event dispatcher or public webhook receiver. Do not rely on them as live triggers.

## Runtime boundary

Handlers run in a QuickJS sandbox. They cannot use the DOM, Node APIs, raw fetch, imports, require, or npm packages. Use the provided ctx APIs for workspace resources, document reads, tagging, AI calls, logs, skip, and explicit failure.

```ts
ctx.trigger\nctx.workspace\nctx.resources.query(...)\nctx.resources.get(...)\nctx.resources.tag(...)\nctx.resources.untag(...)\nctx.doc.read(...)\nctx.ai.run(...)\nctx.log(...)\nctx.skip(...)\nctx.fail(...)
```

## Run safely

Save before running. Review the handler before enabling a schedule. The default run cap is 30 seconds; the sandbox has a 64 MB memory limit, a 1 MB stack limit, and retains up to 500 log entries per run.

## Connector relationship

Automations work inside the workspace. Connectors expose Dokki capabilities to external AI clients or provide agents with external MCP access. Use a connector when the initiating system is outside Dokki.

---

Published from Dokki.
