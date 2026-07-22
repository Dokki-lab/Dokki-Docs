---
title: "Calendar"
canonical: "https://dokki.one/pub/docs/calendar"
source_url: "https://dokki.one/pub/docs/calendar"
updated_at: "2026-07-12T15:12:25.07+00:00"
generated_by: Dokki
---

# Calendar

Calendar is a read-only schedule and run projection for agents. It is not an external calendar sync. Visual guide Calendar Schedule Map Upcoming work Enabled agent schedules expand into future occurre

Canonical source: [https://dokki.one/pub/docs/calendar](https://dokki.one/pub/docs/calendar)

Calendar is a read-only schedule and run projection for agents. It is not an external calendar sync.

## Visual guide

[Calendar Schedule Map](../reference/visual-library/calendar-schedule-map.md)

## Upcoming work

Enabled agent schedules expand into future occurrences using each schedule's cron expression and timezone. Future entries are calculated for the selected calendar window rather than stored as separate events.

## Completed work

Past entries come from agent run history. Calendar groups completed runs by local day and exposes their status so you can review what happened.

## Change a schedule

Open the agent overview to edit its name, prompt, cron expression, timezone, or enabled state. The calendar reflects the changed schedule on its next projection.

## Limits

Calendar is a Dokki view over agent schedules and runs. It does not create Google Calendar, Outlook, or other external calendar events.

---

Published from Dokki.
