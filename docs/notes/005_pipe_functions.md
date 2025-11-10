---
id: SRC-005
source_url: https://docs.openwebui.com/features/plugin/functions/pipe
source_type: documentation
tags:
  - functions
  - pipes
  - agents
summary: Walks through pipe functions as custom agents/models, covering structure, workflow orchestration, and best practices for integrating external services or multiple models.
updated_at: 2025-11-10
---

# Pipe Function Guide

## Summary
- Describes Pipes as custom agent definitions that appear as models, letting authors orchestrate multiple LLMs or external APIs.
- Provides conceptual framing (pipes as ways to add new models) and step-by-step guidance on designing workflows.
- Discusses using non-AI services (e.g., search APIs, Home Assistant) and merging outputs from multiple components.
- Encourages use of Valves for configuration and highlights injection parameters available in the pipe class.

## Development Checklist
- Draft a clear `pipe` method signature that handles `body`, `__user__`, and optional context values.
- Decide whether the pipe should wrap LLM calls, external APIs, or both; plan result formatting to mimic model responses.
- Use piping to combine results from multiple inference providers when building composite agents.

## Key Terms
- **Pipe Function** – Custom workflow packaged as a selectable model.
- **Valves** – Configuration options for customizing pipe behavior per deployment.
- **Custom Agent** – Any composite pipeline orchestrated via a pipe function.

## Implementation Notes
- Standardize naming to help users differentiate pipe-backed models from native providers.
- Document dependencies and environment variables required by the pipe within the metadata docstring.
- Encourage logging inside pipes for observability, especially when chaining external services.

## Related Links
- [Pipelines pipes reference](./012_pipes_reference.md)
- [Valves basics](./009_valves_basics.md)
- [Pipeline valves](./014_pipeline_valves.md)
