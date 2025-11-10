---
id: SRC-006
source_url: https://docs.openwebui.com/features/plugin/functions/filter
source_type: documentation
tags:
  - functions
  - filters
  - message-processing
summary: Describes filter functions for modifying inputs/outputs, outlines skeleton structure, toggleable UI features, and advanced valve configuration patterns.
updated_at: 2025-11-10
---

# Filter Function Guide

## Summary
- Filters act as checkpoints that adjust user inputs (inlet), streamed outputs, and final responses (outlet).
- Provides canonical class skeleton with `Valves`, `inlet`, `stream`, and `outlet` methods.
- Introduces toggleable filters with UI switches and icon support, plus event emitter notifications.
- Demonstrates using Pydantic fields with enums and metadata to expose dropdown configuration options.

## Design Guidelines
- Determine which stages need transformation (pre, streaming, post) and implement only the required methods.
- Use `toggle` and `icon` attributes to improve UX for optional filters.
- Capture advanced configuration via `json_schema_extra` enumerations so admins select validated choices.

## Key Terms
- **Inlet** – Hook for mutating inbound user messages.
- **Stream** – Interceptor for chunked model output while streaming.
- **Outlet** – Final post-processing step before sending responses to the user.

## Implementation Notes
- Combine event emitter notifications with toggle state to deliver instant feedback during filter execution.
- Document default values and use-case-driven Valve structures to encourage reuse across teams.
- Align filter naming with pipeline filter terminology to ease mental mapping between functions and pipelines.

## Related Links
- [Pipeline filters reference](./013_pipeline_filters.md)
- [Valves primer](./009_valves_basics.md)
- [Events reference](./008_events_reference.md)
