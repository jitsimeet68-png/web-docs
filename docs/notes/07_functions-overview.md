---
id: S07
source_url: https://docs.openwebui.com/docs/features/functions/
source_type: documentation
tags: [Functions, OpenAI, Integration]
summary: >-
  Overview describing Open WebUI's compatibility with OpenAI-style function
  calling, including schema alignment and invocation flow.
updated_at: 2025-02-14
---

# Functions Support Overview

## Summary
The functions overview explains how Open WebUI interprets tool metadata through
an OpenAI-compatible function calling layer. It shows how developers can expose
structured functions to the assistant, allowing deterministic code-generation
support while keeping prompts concise.

## Key Points
- Illustrates the mapping between tool manifests and OpenAI function descriptors,
  enabling cross-compatibility with existing agent frameworks.
- Covers enabling function calling per model, specifying available functions, and
  handling multi-step dialogues where the assistant requests function execution.
- Discusses best practices for designing argument schemas and enumerations so the
  assistant reliably picks the correct function.

## Key Terms
- **Function descriptor** — JSON schema describing callable arguments.
- **Call/response loop** — iteration where the assistant proposes invoking a function
  before finalizing an answer.
- **Model binding** — configuration connecting models to sets of available functions.

## Implementation Notes
- Reference this overview when mapping legacy OpenAI function libraries into Open
  WebUI tools.
- Align naming conventions and descriptions with OpenAI guidelines to maintain
  compatibility across orchestrators.

## Source
- [Functions Overview](https://docs.openwebui.com/docs/features/functions/)

## Related Notes
- [S08 — Building Function Handlers](08_functions-building.md)
- [S03 — Tools Feature Overview](03_tools-overview.md)
- [S06 — Tool Runtime API Reference](06_tool-runtime-api.md)
