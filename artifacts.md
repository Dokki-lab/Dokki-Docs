---
title: "Artifacts"
canonical: "https://dokki.one/pub/docs/artifacts"
source_url: "https://dokki.one/pub/docs/artifacts"
updated_at: "2026-07-10T04:50:25.511+00:00"
generated_by: Dokki
---

# Artifacts

Artifacts are interactive visual resources built from source code. Use them for dashboards, diagrams, widgets, calculators, visual explainers, and presentation-like experiences that need more than a d

Canonical source: [https://dokki.one/pub/docs/artifacts](https://dokki.one/pub/docs/artifacts)

Artifacts are interactive visual resources built from source code. Use them for dashboards, diagrams, widgets, calculators, visual explainers, and presentation-like experiences that need more than a document block.

## Visual guide

[Artifact Lifecycle Map](artifact-lifecycle-map.md)

## In this section

- **Generate & Edit** - create an artifact with Copilot or source code, then edit, preview, share, and publish it.

## Source formats

An artifact is either a complete HTML document or a JSX React component. JSX must default-export a component and is compiled before it previews. Dokki provides React, Framer Motion, Lucide icons, Recharts, Mermaid, and Tailwind styling in the JSX runtime.

HTML and compiled JSX render inside sandboxed iframes. That isolates the artifact from the main Dokki application. HTML links are guarded so in-page anchors scroll and other links open separately rather than navigating the editor iframe.

## Collaboration and resource controls

Artifacts are workspace resources. Editors can change source in the code view; viewers see a preview-only surface. Source changes synchronize through the artifact's collaborative Y.js text, and the preview recompiles after source changes settle.

Use the normal resource controls to rename, tag, share, set metadata, export source, publish, archive, or move the artifact. An artifact is not a separate permission system.

## Publishing

Publishing freezes the artifact source and a freshly compiled build into the public-site snapshot. Visitors interact with that frozen render but cannot edit the workspace source from the public page. Publish again after source changes when the public snapshot should change.

## Choose the right resource

Use a document for prose and long-lived writing, a table for structured rows, and an artifact for a self-contained visual or interactive experience.

---

Published from Dokki.
