---
id: SRC-013
source_url: https://docs.openwebui.com/features/pipelines/filters
source_type: documentation
tags:
  - pipelines
  - filters
  - observability
summary: Covers pipeline filters, describing inlet/outlet processing, example use cases, and hosting considerations.
updated_at: 2025-11-10
---

# Pipeline Filters Reference

## Summary
- Pipeline filters operate on incoming user messages (inlet) and outgoing LLM responses (outlet) when attached to models or pipes.
- Use cases include monitoring (Langfuse/DataDog), content moderation, translation, and rate limiting.
- Filters can execute as Functions in WebUI or on a dedicated pipelines server; examples are cataloged in the pipelines GitHub repository.
- Workflow diagram illustrates message flow through the filter before/after the LLM call.

## Implementation Guidance
- Choose filter hosting (embedded vs server) based on performance needs and integration complexity.
- For monitoring/analytics, forward events to observability platforms as part of inlet/outlet logic.
- Combine pipeline filters with function filters for layered governance across environments.

## Key Terms
- **Inlet** – Pre-processing stage for user messages before requesting completions.
- **Outlet** – Post-processing stage for assistant messages before delivery to users.
- **Examples Repository** – GitHub collection of filter templates and scaffolds.

## Implementation Notes
- Document filter ordering and interplay with Valves priority to maintain deterministic processing.
- Use filters to enforce compliance controls or redaction policies prior to completion delivery.
- Link to tutorials for step-by-step monitoring setups when onboarding teams.

## Related Links
- [Filter function guide](./006_filter_functions.md)
- [Pipeline tutorials](./015_pipeline_tutorials.md)
- [Pipelines overview](./011_pipelines_overview.md)
