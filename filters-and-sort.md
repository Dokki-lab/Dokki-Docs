---
title: "Filters and Sort"
canonical: "https://dokki.one/pub/docs/filters-and-sort"
source_url: "https://dokki.one/pub/docs/filters-and-sort"
updated_at: "2026-07-10T04:50:18.62+00:00"
generated_by: Dokki
---

# Filters and Sort

Filters and sort change the current table presentation without changing rows or columns. Visual guide Table Interaction Map Sorting Choose one column and ascending or descending order in the toolbar o

Canonical source: [https://dokki.one/pub/docs/filters-and-sort](https://dokki.one/pub/docs/filters-and-sort)

Filters and sort change the current table presentation without changing rows or columns.

## Visual guide

[Table Interaction Map](table-interaction-map.md)

## Sorting

Choose one column and ascending or descending order in the toolbar or column controls. Clearing the sort returns to the table's current row order. The current implementation has one active sort column at a time.

## Filtering

Add conditions against columns. Available operators are chosen from the column type, so text, numbers, dates, select values, and multi-select values use different comparisons. Combine active conditions with **AND** or **OR**. Empty values do not filter rows until they are filled in.

For a between condition, the second value can be omitted for an open-ended lower bound.

## Display controls

The table presentation can also hide columns, freeze columns to the left, set widths, and wrap text. These are display settings: they do not change stored cell values or table permissions.

## Saved views are local presets

Save the current presentation as a named view to return to it later in the same browser. A saved view captures its view type, filters, AND/OR mode, sort, hidden and frozen columns, widths, wrapping, and Kanban, Gantt, or Calendar settings.

Saved views are persisted in the browser's local table-view store, not in the table's collaborative Y.js data. Other people and other browsers can still see the same rows, but they do not automatically receive your saved-view list or active filter state.

Return to **Default** or clear individual settings to remove the current local presentation without deleting data.

---

Published from Dokki.
