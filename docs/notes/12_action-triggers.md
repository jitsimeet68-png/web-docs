---
id: S12
source_url: https://docs.openwebui.com/docs/features/actions/triggers/
source_type: documentation
tags: [Actions, Triggers, Reference]
summary: >-
  Detailed reference of available action triggers, payload formats, and
  configuration options for binding triggers to workflows.
updated_at: 2025-02-14
---

# Action Triggers Reference

## Summary
The triggers reference documents each event source that can launch an action.
It outlines payload structures, filtering options, and chaining capabilities so
teams can automate precise workflows based on conversation context or external
signals.

## Key Points
- Catalogues built-in triggers: message received, tool finished, schedule, HTTP
  webhook, model response filters, and custom events.
- Provides configuration snippets showing how to specify conditions and map
  trigger data into action parameters.
- Describes sequencing strategies to ensure idempotency and prevent duplicate
  action runs.

## Key Terms
- **Payload mapping** — transformation from trigger data to action inputs.
- **Condition expression** — declarative filters controlling when a trigger fires.
- **Idempotency key** — unique identifier preventing repeated executions.

## Implementation Notes
- Standardize naming conventions for triggers to ease catalog search.
- Include payload examples in internal documentation to accelerate onboarding.

## Source
- [Action Triggers Reference](https://docs.openwebui.com/docs/features/actions/triggers/)

## Related Notes
- [S11 — Actions Framework Overview](11_actions-overview.md)
- [S09 — Pipes Architecture Overview](09_pipes-overview.md)
- [S08 — Building Function Handlers](08_functions-building.md)
