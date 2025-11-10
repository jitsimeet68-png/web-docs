---
id: SRC-003
source_url: https://docs.openwebui.com/features/plugin/tools/development
source_type: documentation
tags:
  - tools
  - development
  - python
  - valves
summary: Details how to author custom Toolkits, including required class structure, metadata, valves configuration, optional injection arguments, and event emitter compatibility considerations.
updated_at: 2025-11-10
---

# Building Custom Tools

## Summary
- Toolkits live in single Python files with a metadata docstring and a `Tools` class containing callable methods.
- Methods require type hints to generate JSON schemas; optional nested types supported.
- Explains `Valves`/`UserValves` patterns for admin and user-configurable settings.
- Lists optional injection parameters (event emitters, user context, metadata, files, OAuth tokens) and demonstrates secure OAuth usage.
- Provides compatibility matrix showing how event emitters behave under Default vs Native function calling modes.

## Design Guidelines
- Always supply a descriptive docstring (title, author, git_url, requirements, version) to surface in catalogs.
- Use Pydantic-based `Valves` classes to expose configuration; recommend enumerated options via `Field` metadata.
- For interactive tools, prefer Default function-calling mode to retain full event emitter support.
- Document fallback behavior when function calling mode is incompatible to set user expectations.

## Key Terms
- **Valves/UserValves** – Admin/user configuration objects for customizing tool behavior.
- **Event Emitter** – Async helper enabling UI updates (`status`, `message`, `notification`, etc.).
- **OAuth Token Injection** – Secure pattern for accessing user OAuth credentials via `__oauth_token__`.

## Implementation Notes
- Include guardrails when relying on optional injections (e.g., verify event emitter is available before streaming updates).
- Provide compatibility notes inside tool descriptions for operations requiring Default mode.
- Encourage modular code to support both Default and Native modes by branching on `function_calling` configuration.

## Related Links
- [Events reference](./008_events_reference.md)
- [Valves & UserValves primer](./009_valves_basics.md)
- [Pipeline valves](./014_pipeline_valves.md)
