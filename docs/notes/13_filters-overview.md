---
id: S13
source_url: https://docs.openwebui.com/docs/features/filters/
source_type: documentation
tags: [Filters, Moderation, Overview]
summary: >-
  Overview describing Open WebUI filters that sanitize, transform, or reroute
  model responses before presenting them to users or downstream systems.
updated_at: 2025-02-14
---

# Filters Overview

## Summary
The filters overview presents filters as middleware for post-processing model
responses. It covers types of filters (sanitization, transformations, routing),
configuration patterns, and their role in quality control when generating code or
running automations.

## Key Points
- Defines filter categories: pre-processing (prompt shaping), response filters,
  moderation checks, and custom transformers for formatting output.
- Details configuration parameters, including priorities, chaining order, and
  fallback behaviors.
- Explains integration with actions and pipes to ensure filters run consistently
  across automated workflows.

## Key Terms
- **Filter chain** — ordered list of filters applied to a response.
- **Priority** — numeric weight determining filter execution order.
- **Transformation** — modifications (formatting, annotation) applied to responses.

## Implementation Notes
- Document filter ordering guidelines to maintain deterministic outputs.
- Provide reusable code-formatting filter examples for teams building coding
  assistants.

## Source
- [Filters Overview](https://docs.openwebui.com/docs/features/filters/)

## Related Notes
- [S14 — Custom Filter Development](14_filters-custom.md)
- [S11 — Actions Framework Overview](11_actions-overview.md)
- [S09 — Pipes Architecture Overview](09_pipes-overview.md)
