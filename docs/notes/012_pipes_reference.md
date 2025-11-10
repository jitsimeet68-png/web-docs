---
id: SRC-012
source_url: https://docs.openwebui.com/features/pipelines/pipes
source_type: documentation
tags:
  - pipelines
  - pipes
  - architecture
summary: Summarizes pipeline-specific pipe documentation, describing standalone functions, hosting options, and UI presentation within Open WebUI.
updated_at: 2025-11-10
---

# Pipeline Pipes Reference

## Summary
- Pipes are standalone functions that process inputs, optionally call LLMs or external services, and return responses to users.
- Page positions pipes as enablers for RAG workflows, non-OpenAI providers, or in-UI function execution.
- Notes hosting flexibility—pipes can run as Functions within WebUI or on a Pipelines server; examples reside in the GitHub repository.
- Illustrates UI integration via screenshots showing pipe models labeled as "External" alongside local models.

## Implementation Guidance
- Determine hosting strategy (embedded function vs pipeline service) based on resource demands and isolation needs.
- Document dependencies when contributing examples to the pipelines repo for discoverability.
- Encourage consistent naming conventions for pipeline pipes to differentiate from function-based pipes.

## Key Terms
- **External Model** – Label used in UI for pipeline-hosted pipes.
- **RAG Pipeline** – Retrieval-augmented generation example combining knowledge sources and LLM responses.
- **Examples Directory** – GitHub location for curated pipe implementations.

## Implementation Notes
- Align pipeline pipe behavior with function-based pipe semantics to minimize user confusion.
- Provide runbooks describing when to offload pipes to separate infrastructure (e.g., heavy compute or vendor isolation).
- Pair with pipeline valves guidance when customizing input variables across deployments.

## Related Links
- [Pipelines overview](./011_pipelines_overview.md)
- [Pipe function guide](./005_pipe_functions.md)
- [Pipeline valves](./014_pipeline_valves.md)
