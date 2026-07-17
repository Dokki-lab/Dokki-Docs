---
title: "Column Types"
canonical: "https://dokki.one/pub/docs/column-types"
source_url: "https://dokki.one/pub/docs/column-types"
updated_at: "2026-07-10T06:02:26.847+00:00"
generated_by: Dokki
---

# Column Types

Every column in a Dokki table has a type. The type controls the editor shown in the cell, how filter operators are chosen, how form submissions are validated, and how values are displayed. Visual guid

Canonical source: [https://dokki.one/pub/docs/column-types](https://dokki.one/pub/docs/column-types)

Every column in a Dokki table has a type. The type controls the editor shown in the cell, how filter operators are chosen, how form submissions are validated, and how values are displayed.

## Visual guide

[Table Interaction Map](table-interaction-map.md)

## Available types

| Type | What it stores | Current editor / behavior |
| --- | --- | --- |
| Text | Any string, including multiline text | Inline text editor |
| Number | Numeric values or blank | Numeric editor; blanks stay blank instead of becoming 0 |
| Boolean | True / false | Checkbox |
| Date | One date value | Date editor and local-date display |
| Date range | Start date and end date | Range value used by Gantt and date-range filters |
| Select | One option from the column's option list | Dropdown-style single choice |
| Multi-select | Multiple values from the option list | Multi-choice editor; stored as a comma-separated value internally |
| Tags | Workspace tags applied to that row | Tag picker backed by the workspace tag list |
| Member | One workspace member | Member picker listing current workspace members |
| URL | Link-like text | Text editor with URL-oriented rendering where available |
| Email | Email-like text | Text editor with email-oriented rendering where available |

## Setting a column type

Open the column menu from the header, choose the type action, and pick the new type. Column definitions are stored in the table's collaborative Y.js document, so collaborators see the new type as soon as the table syncs.

Changing a type affects new edits, filters, views, and public form validation. Existing values are not a substitute for a database migration: review important columns after changing their type, especially when moving between free text and structured types such as number, date, select, or multi-select.

## Select and multi-select options

Select and multi-select columns use the column's option list as the source of truth. Those options drive:

- the cell editor choices;
- Kanban grouping, because Kanban groups by a select-style column;
- public form validation, because anonymous submitters cannot invent new select options;
- filter operators such as `is`, `is not`, `includes any`, and `includes all`.

If you need free-form values, use a Text column instead of Select.

## Date and date range columns

Date columns power Calendar views and date filters. Date range columns can power Gantt views directly. Gantt can also use separate start and end Date columns when a date-range column is not available.

Date filters compare by local calendar day for equality-style checks. For date ranges, Dokki treats a range as matching when the target day or filter range overlaps the stored range.

## Public form validation

Forms validate against live column definitions at submit time:

- required non-boolean fields must be present;
- number fields must parse as numbers;
- date and date-range fields must parse as dates;
- select and multi-select values must already exist in the column options;
- email fields must match a basic email format;
- disabled fields and deleted columns are ignored.

## Current limits

Dokki tables currently do not provide formulas, relational links between tables, or a dedicated file/attachment column type. Use documents, files, or separate tables for those workflows.

---

Published from Dokki.
