---
title: "Runs and Schedules"
canonical: "https://dokki.one/pub/docs/runs-and-schedules"
source_url: "https://dokki.one/pub/docs/runs-and-schedules"
updated_at: "2026-07-22T11:13:32.802+00:00"
generated_by: Dokki
---

# Runs and Schedules

A run is one execution of an installed agent. Dokki currently records two run origins: a conversation with the agent and a scheduled task. Visual guide Agent Control Panel Map Chat runs Select an inst

Canonical source: [https://dokki.one/pub/docs/runs-and-schedules](https://dokki.one/pub/docs/runs-and-schedules)

A run is one execution of an installed agent. Dokki currently records two run origins: a conversation with the agent and a scheduled task.

## Visual guide

[Agent Control Panel Map](../../reference/visual-library/agent-control-panel-map.md)

## Chat runs

Select an installed agent in Copilot or use the routing composer to start its dedicated conversation. The agent uses its current instructions, allowed workspace reach, enabled skills, pinned resources, memory setting, and configured MCP servers. A conversation can continue across turns; the activity timeline records the latest user prompt and a compact output preview for each run.

## Scheduled runs

Schedules are configured on the agent's **Overview** tab. Each schedule has a name, prompt, cron expression, timezone, enabled state, next-run time, last-run data, and failure count. They are suitable for predictable recurring work such as weekly reviews, research briefs, or documentation checks.

When a due schedule is claimed, Dokki creates a queued agent run and calculates the next occurrence. Scheduled work does not run in archived workspaces, and a paused or deleted agent cannot continue as an active worker. Make the prompt self-contained enough that the task still makes sense when no one is watching the chat.

## Review the activity timeline

The **Overview** timeline is the record of work. It shows whether each run was started by chat or a schedule, along with status, model, step progress, timestamps, the triggering prompt preview, output preview, and an error message when one is available. Open the relevant conversation for the full exchange; use the timeline to diagnose repeated failures or an unexpected schedule result.

You can enable, disable, or delete schedules from the Overview tab. Disabling preserves the schedule configuration but prevents future runs; deleting removes that schedule. Pausing an agent and disabling a schedule are different controls, so use both deliberately when retiring an automation.

## Operational checklist

- Verify the agent's workspace allowlist before creating a schedule.
- Keep recurring prompts specific about scope, expected output, and where results belong.
- Watch the first run and inspect any error before treating a schedule as dependable.
- Revisit the schedule after permission, model, or MCP connection changes.

---

Published from Dokki.
