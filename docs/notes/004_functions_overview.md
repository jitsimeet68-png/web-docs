---
id: SRC-004
source_url: https://docs.openwebui.com/features/plugin/functions/
source_type: documentation
tags:
  - functions
  - overview
  - governance
summary: Introduces Function types (Pipe, Filter, Action), their purposes, installation/enabling flows, and why to use Functions for platform customization.
updated_at: 2025-11-10
---

# Functions Overview

## Summary
- Defines Functions as in-process Python extensions for Open WebUI, distinct from Tools that interact with external systems.
- Breaks down three function classes: Pipes (model-like integrations), Filters (input/output modifiers), and Actions (UI buttons).
- Outlines installation via community catalog/manual import and emphasizes enabling/assignment per model or globally.
- Highlights benefits—extending providers, optimizing workflows, simplifying user interactions.

## Operational Guidance
- After enabling, map Filters/Actions to models in Workspace → Models or toggle the Global setting under Workspace → Functions.
- Use Pipes when you need responses surfaced as selectable models; treat them as first-class chat endpoints.
- Encourage admins to vet community functions and restrict enabling rights due to code execution risk.

## Key Terms
- **Pipe Function** – Custom agent/model integration appearing in the model picker.
- **Filter Function** – Hook to mutate inbound/outbound messages via inlet/outlet logic.
- **Action Function** – Chat toolbar buttons triggering custom logic.

## Implementation Notes
- Document standard operating procedures for assigning functions during environment provisioning.
- Provide training materials summarizing per-function responsibilities and UI locations.
- Cross-link to detailed guides for each function type inside runbooks.

## Related Links
- [Pipe functions](./005_pipe_functions.md)
- [Filter functions](./006_filter_functions.md)
- [Action functions](./007_action_functions.md)
