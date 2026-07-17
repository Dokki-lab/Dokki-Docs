---
title: "Models and Usage"
canonical: "https://dokki.one/pub/docs/models-and-usage"
source_url: "https://dokki.one/pub/docs/models-and-usage"
updated_at: "2026-07-10T04:50:10.415+00:00"
generated_by: Dokki
---

# Models and Usage

Dokki uses a live model catalog for Copilot, agents, and generation workflows. The active catalog is stored in Dokki's ai_models settings and served to the client from /api/models ; code carries a boo

Canonical source: [https://dokki.one/pub/docs/models-and-usage](https://dokki.one/pub/docs/models-and-usage)

Dokki uses a live model catalog for Copilot, agents, and generation workflows. The active catalog is stored in Dokki's `ai_models` settings and served to the client from `/api/models`; code carries a bootstrap fallback so the picker is never empty during startup or a catalog read failure.

## Visual guide

[Copilot Turn Pipeline](copilot-turn-pipeline.md)

## Model catalog

The current bootstrap catalog includes providers such as MiniMax, DeepSeek, Z.ai, Alibaba Qwen, Google Gemini, OpenAI, Anthropic Claude, StepFun, and xAI.

The database catalog is authoritative for enabled state, tier, display order, default model, and credit rates. The server caches it for 24 hours per runtime instance; operators can invalidate a local cache through the protected model-cache endpoint.

## Auto routing

The model picker includes **Auto**. Auto is not sent to a provider. It is a sentinel that the chat API resolves to a concrete in-plan model for each request.

Auto routing looks at the latest user turn:

| Signal | Effect |
| --- | --- |
| Short/simple text | Prefer a fast low-cost model. |
| Longer text | Move toward a mid-strength model. |
| Code, debugging, architecture, analysis, or complex reasoning keywords | Prefer a stronger model. |
| Image attachment | Prefer a vision-capable model when the plan and org allow it. |

Auto also respects organization model allowlists. If no allowed pool exists, the normal model-tier gate still decides whether the fallback can run.

## Model tiers

Models have a minimum access tier: free, pro, or max. The plan gate is enforced server-side even if the client picker has stale data.

The client picker shows locked models when they are above the user's plan. In organization context, it also filters the picker by the organization's allowed model list when one is configured.

## Vision models

Image understanding is limited to models marked as vision-capable in code. If a user attaches an image while using a non-vision model, Dokki recommends a vision model, with Gemini Pro as the default recommendation when available.

## Credits and limits

Each completed turn calculates credits from input/output tokens and the active model's catalog rates. If the catalog lookup fails during billing, Dokki uses a conservative fallback rate rather than treating the turn as free.

Plans can impose daily and weekly usage windows. Extra Usage can continue after included limits when enabled, until credits or the configured cap runs out.

## Organization controls

Organizations can restrict available models with an allowlist. An empty allowlist means members may use any model their plan permits. A non-empty allowlist narrows the model pool for organization workspaces and also constrains Auto routing.

---

Published from Dokki.
