---
title: "Keyboard Shortcuts"
canonical: "https://dokki.one/pub/docs/keyboard-shortcuts"
source_url: "https://dokki.one/pub/docs/keyboard-shortcuts"
updated_at: "2026-07-10T06:02:02.342+00:00"
generated_by: Dokki
---

# Keyboard Shortcuts

This page documents shortcuts that are deliberately implemented in the current editor. Platform labels mean Cmd on macOS and Ctrl on Windows or Linux. Visual guide Editor Capability Map Select within

Canonical source: [https://dokki.one/pub/docs/keyboard-shortcuts](https://dokki.one/pub/docs/keyboard-shortcuts)

This page documents shortcuts that are deliberately implemented in the current editor. Platform labels mean Cmd on macOS and Ctrl on Windows or Linux.

## Visual guide

[Editor Capability Map](editor-capability-map.md)

## Select within the current block

Use Cmd/Ctrl + A while editing. When only part of the current block is selected, Dokki expands the selection to that block before the browser escalates to page-wide selection. This avoids accidentally selecting the entire document when editing a paragraph.

## Command palette behavior

Type / in an editable text block to open the document's slash menu. Use Arrow Up and Arrow Down to move through matches, Enter to run the active command, and Escape to dismiss it.

## Cmd/Ctrl + K opens search

Cmd/Ctrl + K opens Dokki's search palette, and on a published site it opens that site's search. It is not a link shortcut. To add or edit a link in a document, select text and use the link control in the floating toolbar.

## Markdown input rules

At the beginning of a block, standard editor input rules can turn common Markdown-style prefixes into headings, lists, quotes, code blocks, or horizontal rules as you type. The slash menu remains the most discoverable way to see available blocks.

## Table boundary

Standalone collaborative tables handle undo and redo at the table level when focus is not inside a cell editor or filter input. Those shortcuts apply to the table product, not to rich-text document history.

For any shortcut that is not listed here, use the relevant visible control. Dokki intentionally avoids claiming a fixed global shortcut sheet where focus and surface decide the behavior.

---

Published from Dokki.
