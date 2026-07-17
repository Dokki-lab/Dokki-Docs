---
title: "Embeds and Math"
canonical: "https://dokki.one/pub/docs/embeds-and-math"
source_url: "https://dokki.one/pub/docs/embeds-and-math"
updated_at: "2026-07-10T04:50:12.906+00:00"
generated_by: Dokki
---

# Embeds and Math

Use document embeds to bring context into a page while keeping the source resource authoritative. Visual guide Editor Capability Map External embeds Use the slash menu or paste a supported URL to add

Canonical source: [https://dokki.one/pub/docs/embeds-and-math](https://dokki.one/pub/docs/embeds-and-math)

Use document embeds to bring context into a page while keeping the source resource authoritative.

## Visual guide

[Editor Capability Map](editor-capability-map.md)

## External embeds

Use the slash menu or paste a supported URL to add YouTube, X, Figma, GitHub, Google Docs/Sheets/Slides, or a generic web embed. Generic embeds can display a bookmark-style preview or an iframe when the source permits it.

External services control their own access and embedding rules. A private Figma design, Google file, or GitHub item may ask the viewer to sign in, refuse to render in an iframe, or show no content.

## Embed a Dokki resource

**Embed Resource** inserts a live card for a workspace document, table, artifact, file, or folder. It uses the current resource identity rather than a copied snapshot, so renamed items keep their reference. The preview remains permission-aware: an unavailable card replaces private, archived, deleted, or inaccessible content.

## Images and SVG

Add images by dragging an image into the editor, pasting one, or using the Image command to choose a local file. Images are uploaded to workspace storage and can be resized while preserving their aspect ratio.

Use the SVG command for vector markup. Dokki sanitizes SVG before rendering, removing unsafe content rather than treating SVG as unrestricted HTML.

## Inline math

Dokki's math extension renders a selected LaTeX expression as an inline KaTeX node. Select the inline node to edit it back to its LaTeX source. Invalid notation is displayed without throwing a document-level error.

The current editor does not expose a separate slash-menu math block or dollar-sign auto-conversion workflow. Keep large equations in normal document structure around inline math, or use a code block when the source notation itself is what readers need.

## Code blocks

Code blocks are syntax highlighted and have a language selector. They are separate from inline code formatting and are the appropriate place for multi-line source snippets.

---

Published from Dokki.
