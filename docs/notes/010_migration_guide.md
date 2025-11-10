---
id: SRC-010
source_url: https://docs.openwebui.com/features/plugin/migration
source_type: documentation
tags:
  - migration
  - architecture
  - functions
summary: Summarizes the Open WebUI 0.4→0.5 migration guide, including architectural shifts, import path changes, unified endpoints, and updated function signatures.
updated_at: 2025-11-10
---

# Migration Guide (0.4 → 0.5)

## Summary
- Version 0.5 consolidates Open WebUI into a single FastAPI app with routers replacing the older sub-app architecture.
- Imports move from `open_webui.apps.*` to `open_webui.routers.*`, with `open_webui.main` serving as the central entry point.
- Introduces unified `chat_completion` endpoint alongside `open_webui.utils.chat.generate_chat_completion` as a lightweight successor.
- Function signatures now expect a `Request` object; guide illustrates updated `pipe` method example.

## Upgrade Steps
- Replace module imports according to the provided old/new path table, noting the special case for `webui` becoming `open_webui.main`.
- Decide between `chat_completion` (full API flow) and `generate_chat_completion` (direct POST) based on project needs.
- Update custom functions to accept `__request__` and adapt to new signature expectations.

## Key Terms
- **Router Architecture** – New layout organizing endpoints under `open_webui.routers`.
- **chat_completion** – Unified endpoint replicating `/api/chat/completions` behavior with parsing.
- **generate_chat_completion** – Lightweight helper replacing prior provider-specific functions.

## Implementation Notes
- Maintain a migration checklist capturing modules to refactor and tests to rerun.
- Flag dependencies on removed modules early to prevent runtime import errors.
- Document new request handling patterns in internal templates for Pipe/Function authors.

## Related Links
- [Pipe functions guide](./005_pipe_functions.md)
- [Functions overview](./004_functions_overview.md)
- [Tool development guide](./003_tool_development.md)
