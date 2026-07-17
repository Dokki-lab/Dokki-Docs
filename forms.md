---
title: "Forms"
canonical: "https://dokki.one/pub/docs/forms"
source_url: "https://dokki.one/pub/docs/forms"
updated_at: "2026-07-10T04:50:20.328+00:00"
generated_by: Dokki
---

# Forms

A form turns a table into a public collection endpoint. Submissions append rows to the table, so you can gather intake requests, signups, feedback, lightweight surveys, or structured reports without g

Canonical source: [https://dokki.one/pub/docs/forms](https://dokki.one/pub/docs/forms)

A form turns a table into a public collection endpoint. Submissions append rows to the table, so you can gather intake requests, signups, feedback, lightweight surveys, or structured reports without giving the submitter workspace access.

## Visual guide

[Table Interaction Map](table-interaction-map.md)

## Create a form

Open a table and click the form/collection button in the table toolbar. Dokki reads the live table columns from the collaborative table document and starts with each column as a possible question.

## Configure questions

- Set the form title and optional description.
- Enable or disable each column as a question.
- Customize each question label without renaming the table column.
- Mark enabled questions as required when the row should not be accepted without a value.
- Deleted table columns are dropped from the form configuration; new table columns are appended as disabled fields when you reopen the dialog.

## Start and share collection

Saving stores the configuration. Starting collection activates a unique anonymous form token and shows a share link at `/form/<token>`. Stopping collection keeps the configuration but makes the link reject new submissions.

## Submission validation

Anonymous submissions are gated by the unguessable token and the form's active state. On submit, Dokki validates values against the live table column definitions in the same document it mutates, so select options and typed values are checked before a row is added.

## Rate limiting and errors

When Vercel KV rate-limiting environment variables are configured, anonymous submissions are limited to 30 submissions per IP per hour. Invalid values return field-level validation errors. Inactive forms return an error instead of adding a row.

## Operational notes

- A form belongs to one table resource.
- The submission counter is best-effort; the appended table rows are the source of truth.
- Use forms for collection, not for permissioned editing. Anyone with the active link can submit.
- Disable collection before sharing a table publicly if you do not want more anonymous rows.

---

Published from Dokki.
