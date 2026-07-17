---
title: "Real-time Editing"
canonical: "https://dokki.one/pub/docs/real-time-editing"
source_url: "https://dokki.one/pub/docs/real-time-editing"
updated_at: "2026-07-10T04:50:19.916+00:00"
generated_by: Dokki
---

# Real-time Editing

Tables in Dokki are collaborative resources backed by Y.js and the Hocuspocus collaboration server. People can edit rows, columns, cells, and view settings while others are in the same table. Visual g

Canonical source: [https://dokki.one/pub/docs/real-time-editing](https://dokki.one/pub/docs/real-time-editing)

Tables in Dokki are collaborative resources backed by Y.js and the Hocuspocus collaboration server. People can edit rows, columns, cells, and view settings while others are in the same table.

## Visual guide

[Table Interaction Map](table-interaction-map.md)

## What live editing feels like

- Cell, row, and column changes sync through the collaborative table document.
- There is no manual save button for table edits.
- Connected collaborators see table changes after the update reaches the collaboration server.
- Refreshing the table reloads the persisted collaborative state.

## Presence and selection

Dokki tracks collaborator presence for tables. The table UI can show active collaborators and selection state so teammates can see that someone else is working in the same table.

Presence is session-based: it appears while a collaborator is connected and disappears after the tab or connection closes.

## Conflict behavior

Y.js handles concurrent structural updates without locking the table. Practical outcomes are straightforward:

- if two people edit the same cell, the final cell value reflects the resolved collaborative update order;
- if a row or column is deleted while someone else is editing it, the deletion removes that target;
- if a column type or option list changes, later edits and public form submissions are validated against the current column definition;
- Copilot and bulk operations can update many cells in one action, and those updates sync through the same table document.

## Persistence

The collaboration server persists table state to Dokki's table storage. Public forms, Copilot tools, and server-side table mutations use the same table document path so appended rows and generated edits land in the live collaborative table instead of a separate copy.

## Scale guidance

Dokki tables are designed for human-scale collaborative work: project trackers, content calendars, CRM-style lists, research logs, intake queues, and lightweight operational tables. Very large analytical datasets should stay in a data warehouse or spreadsheet/database system, with the summary or working subset brought into Dokki.

---

Published from Dokki.
