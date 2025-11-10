---
id: SRC-007
source_url: https://docs.openwebui.com/features/plugin/functions/action
source_type: documentation
tags:
  - functions
  - actions
  - ui
summary: Covers action functions that add chat toolbar buttons, detailing class structure, context parameters, event integration, multi-action patterns, and advanced capabilities.
updated_at: 2025-11-10
---

# Action Function Guide

## Summary
- Action functions render admin-managed buttons beneath model messages, enabling interactive workflows like confirmations, visualizations, or downloads.
- Provides class scaffold with `Valves` configuration and an `action` coroutine receiving context (`body`, `__user__`, event helpers, `__model__`, `__request__`, `__id__`).
- Explains use of `__event_emitter__` for status/notification streaming and `__event_call__` for confirmation/input dialogues.
- Describes single versus multi-action patterns, global vs model-specific enablement, and background task handling.
- Shows how to process uploaded files and return generated media in action responses.

## Design Guidelines
- Define clear naming and icons for multi-action arrays to help users differentiate actions.
- Use event calls to gate risky operations behind confirmations or to solicit extra parameters.
- For long-running tasks, emit progress updates before returning final content.

## Key Terms
- **Action Function** – Server-side routine triggered by chat toolbar button.
- **Event Call** – Bidirectional helper for requesting user input/confirmation.
- **Multi-Action** – Function exposing multiple sub-actions identified via `__id__`.

## Implementation Notes
- Align permission checks with `__user__` roles before executing privileged actions.
- Return structured `files` arrays when generating downloadable assets.
- Document dependencies or service endpoints used within the action for maintainability.

## Related Links
- [Events reference](./008_events_reference.md)
- [Functions overview](./004_functions_overview.md)
- [Tool development guide](./003_tool_development.md)
