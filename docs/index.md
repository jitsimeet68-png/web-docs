# Open WebUI Extension Knowledge Index

## 1. Foundational Overview
- [Tools & Functions (Plugins) orientation](./notes/001_plugins_overview.md)
- [Migration guide for 0.4 → 0.5 architecture changes](./notes/010_migration_guide.md)

## 2. Tools — Extending LLM Capabilities
- [Operational guide to installing and enabling tools](./notes/002_tools_usage.md)
- [Authoring custom toolkits with valves and events](./notes/003_tool_development.md)
- [Real-time events reference for tool-driven UX](./notes/008_events_reference.md)
- [Valves & UserValves configuration primer](./notes/009_valves_basics.md)

## 3. Functions — Customizing Open WebUI
- [Functions overview and enablement workflow](./notes/004_functions_overview.md)
- [Pipe function guide for agent-style workflows](./notes/005_pipe_functions.md)
- [Filter function guide for message mutation](./notes/006_filter_functions.md)
- [Action function guide for interactive buttons](./notes/007_action_functions.md)
- Cross-cutting references:
  - [Events reference](./notes/008_events_reference.md)
  - [Valves & UserValves basics](./notes/009_valves_basics.md)

## 4. Pipelines — Externalized Workflows
- [Pipelines overview and deployment checklist](./notes/011_pipelines_overview.md)
- [Pipeline pipes reference](./notes/012_pipes_reference.md)
- [Pipeline filters reference](./notes/013_pipeline_filters.md)
- [Pipeline valves configuration](./notes/014_pipeline_valves.md)
- [Pipeline tutorials digest (community resources)](./notes/015_pipeline_tutorials.md)

## 5. Community Catalog
- [Curated open-webui/functions repository](./notes/016_functions_repo.md)

### Cross-Domain Links
- Tool authors transitioning to pipelines should review [Pipeline valves](./notes/014_pipeline_valves.md) after [Valves basics](./notes/009_valves_basics.md).
- For UI-rich experiences, pair [Action functions](./notes/007_action_functions.md) with [Events reference](./notes/008_events_reference.md).
- To align pipeline filters with in-app filters, compare [Filter function guide](./notes/006_filter_functions.md) and [Pipeline filters reference](./notes/013_pipeline_filters.md).
