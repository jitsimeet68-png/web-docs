---
id: SRC-008
source_url: https://docs.openwebui.com/features/plugin/events/
source_type: documentation
tags:
  - events
  - realtime
  - ux
summary: Documents the event system for Tools and Functions, including emitter/call usage patterns, payload structure, and supported event types.
updated_at: 2025-11-10
---

# Events Reference

## Summary
- Events enable real-time UI communication from Tools/Functions using `__event_emitter__` for one-way updates and `__event_call__` for interactive flows.
- Provides sample payloads showing `type` and `data` schema and stresses that routing metadata is auto-managed.
- Enumerates event types (`status`, `chat:message`, `files`, `chat:title`, `notification`, `confirmation`, `input`, `execute`, etc.) with usage notes.
- Highlights advanced behaviors, including creating custom event types and implications for streaming content replacement.

## Usage Guidelines
- Use `status` events to surface progress, `chat:message:delta` for streaming, and `replace` when finalizing content.
- Reserve `__event_call__` for operations requiring user confirmation or data entry; handle returned responses gracefully.
- Keep payloads minimal—Open WebUI populates chat identifiers automatically.

## Key Terms
- **Event Emitter** – Async callback broadcasting UI updates without expecting a response.
- **Event Call** – Awaitable helper for dialog-style interactions requiring user input.
- **Event Type Catalog** – Reference table describing when to apply each supported `type` string.

## Implementation Notes
- Combine this reference with the tool development compatibility matrix to choose safe event types per function-calling mode.
- Document any custom event types in team guidelines to ensure frontend handling exists.
- When chaining streaming events, ensure final `chat:message` or `replace` event consolidates output to avoid flicker.

## Related Links
- [Tool development guide](./003_tool_development.md)
- [Action function guide](./007_action_functions.md)
- [Filter function guide](./006_filter_functions.md)
