---
id: S03
source_url: https://docs.openwebui.com/docs/features/tools/
source_type: documentation
tags: [Tools, Extensions, Overview]
summary: >-
  Overview of the Tools feature explaining how scripted utilities can be
  registered with Open WebUI to extend the assistant with deterministic
  capabilities during coding sessions.
updated_at: 2025-02-14
---

# Tools Feature Overview

## Summary
This guide introduces the Tools system as the foundation for connecting Open
WebUI conversations to deterministic back-end capabilities. It covers tool
registration, permission management, invocation from prompts, and how tools
integrate with other extensibility layers such as pipes and filters.

## Key Points
- Defines tools as executable adapters that can be implemented in Python or via
  HTTP endpoints, exposing metadata such as name, description, input schema, and
  authentication requirements.
- Details the runtime lifecycle: discovery, validation, availability toggles, and
  invocation through natural language triggers when the assistant determines a
  tool is appropriate.
- Explains interplay with functions and actions—tools can be orchestrated by
  pipeline nodes or filtered responses to maintain reliable automation flows.

## Key Terms
- **Tool registry** — the configuration store enumerating all installed tools.
- **Invocation policy** — rules and heuristics controlling when a tool may run.
- **Schema validation** — JSON schema used to validate tool parameters.

## Implementation Notes
- Document each tool with consistent metadata to simplify indexing and discovery.
- Align tool descriptions with the naming conventions recommended in Open WebUI
  so they surface cleanly in the UI tool picker.

## Source
- [Tools Feature Overview](https://docs.openwebui.com/docs/features/tools/)

## Related Notes
- [S04 — Authoring Custom Tools Guide](04_tools-authoring.md)
- [S05 — Tool Manifest Reference](05_tool-manifest.md)
- [S09 — Pipes Architecture Overview](09_pipes-overview.md)
