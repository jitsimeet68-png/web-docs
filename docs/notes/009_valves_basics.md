---
id: SRC-009
source_url: https://docs.openwebui.com/features/plugin/valves
source_type: documentation
tags:
  - valves
  - configuration
  - customization
summary: Explains how Valves and UserValves expose configurable settings for Tools, Filters, Pipes, and Pipelines, with annotated examples and access patterns.
updated_at: 2025-11-10
---

# Valves & UserValves Basics

## Summary
- Valves (admin-level) and UserValves (per-user) are Pydantic classes declared inside plugin classes to expose configurable options in the UI.
- Documentation illustrates typed fields, descriptions, and use of `Literal` for enumerated choices plus the optional `priority` field.
- Provides sample code showing how to access admin valves immediately and user valves via `__user__["valves"]` within runtime methods.

## Usage Guidelines
- Always declare Valves/UserValves as class attributes of the plugin to ensure UI generation.
- Use descriptive `Field` metadata to guide admins/users when filling values; include defaults when possible.
- Encourage developers to avoid direct dict indexing on `__user__["valves"]`; convert to dict or access attributes to respect Pydantic objects.

## Key Terms
- **Valve** – Admin-configured setting controlling plugin behavior.
- **UserValve** – User-adjustable option accessible in chat context.
- **Priority** – Optional field to order filters when multiple are applied.

## Implementation Notes
- Share this guide with plugin authors before publishing to ensure consistent configuration UX.
- Pair with pipeline valve documentation when standardizing environment variable fallbacks.
- Document expected valve names/types in runbooks to simplify onboarding.

## Related Links
- [Tool development guide](./003_tool_development.md)
- [Pipeline valves](./014_pipeline_valves.md)
- [Filter function guide](./006_filter_functions.md)
