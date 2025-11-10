---
id: SRC-014
source_url: https://docs.openwebui.com/features/pipelines/valves
source_type: documentation
tags:
  - pipelines
  - valves
  - configuration
summary: Describes how to define and initialize valves for pipelines, including environment variable fallbacks, optional types, and error handling considerations.
updated_at: 2025-11-10
---

# Pipeline Valves Reference

## Summary
- Pipeline documentation clarifies that valves act as per-pipeline input variables defined as subclasses of the `Pipeline` class.
- Recommends initializing valves in `__init__`, often pulling defaults from environment variables to ensure UI reconfiguration.
- Suggests using optional types to allow pipelines to load without preset values, preventing startup failures.
- Warns that missing valve configuration causes log warnings about missing `Pipeline` classes when adding pipelines to WebUI.

## Implementation Guidance
- Provide environment-variable fallbacks for each valve to support containerized deployments.
- Use Optional typing for non-critical settings to improve resilience and onboarding.
- Document valve names and expected value ranges for administrators adjusting settings in the UI.

## Key Terms
- **Pipeline.Valves** – Pydantic subclass capturing configurable pipeline inputs.
- **Optional Valve** – Field declared optional to permit missing values during initialization.
- **Warning Log** – `WARNING:root:No Pipeline class found...` message triggered by incomplete valve setup.

## Implementation Notes
- Align pipeline valve naming with function/tool valve conventions for cross-system familiarity.
- Provide guidance on where admins edit valves (Admin Panel → Settings → Pipelines).
- Pair with plugin valve best practices to deliver consistent configuration experiences.

## Related Links
- [Valves basics](./009_valves_basics.md)
- [Pipelines overview](./011_pipelines_overview.md)
- [Pipes reference](./012_pipes_reference.md)
