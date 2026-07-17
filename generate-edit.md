---
title: "Generate & Edit"
canonical: "https://dokki.one/pub/docs/generate-edit"
source_url: "https://dokki.one/pub/docs/generate-edit"
updated_at: "2026-07-10T04:50:26.244+00:00"
generated_by: Dokki
---

# Generate & Edit

Create an Artifact from a Copilot request or from source code, then refine it in the workspace. Visual guide Artifact Lifecycle Map Start with a clear outcome Ask Copilot for a concrete visual or inte

Canonical source: [https://dokki.one/pub/docs/generate-edit](https://dokki.one/pub/docs/generate-edit)

Create an Artifact from a Copilot request or from source code, then refine it in the workspace.

## Visual guide

[Artifact Lifecycle Map](artifact-lifecycle-map.md)

## Start with a clear outcome

Ask Copilot for a concrete visual or interaction: a KPI dashboard, timeline, decision map, calculator, quiz, or a presentation-shaped explainer. Copilot creates an artifact resource with source code; you can then continue the conversation or open the artifact directly.

## Choose HTML or JSX

Use a complete HTML document when the artifact should be self-contained. Use JSX when you want a React component. JSX must default-export a component and can use React, Framer Motion, Lucide, Recharts, Mermaid, and Tailwind classes.

Dokki detects a full HTML document or plain HTML markup as HTML. Source containing imports, exports, React-style expressions, className, event props, or JSX-only syntax is treated as JSX and must compile.

## Edit and preview

Open an editable artifact to switch between **Preview** and **Code**. Press Tab outside the CodeMirror editor and form controls to toggle those modes. Changes synchronize through the shared source text; JSX compilation is debounced, so the preview can briefly show Compiling while you type.

Compilation or render errors appear in the preview instead of silently replacing the last source with a false success. HTML renders directly in its sandboxed iframe; JSX is compiled and dry-run validated before API writes succeed.

## Collaborate safely

People with view access see preview only. People with edit access can change source collaboratively. Use the resource share controls for the intended audience; embedding an artifact in a document does not grant access beyond the artifact's own permission.

## Publish and export

The settings menu can export the source as a JSX text file and manage tags or metadata. Publishing creates a frozen public snapshot. Public visitors can interact with that snapshot, but source edits remain governed by the workspace resource permissions and require a new publish to update the public page.

---

Published from Dokki.
