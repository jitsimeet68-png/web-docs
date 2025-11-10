---
id: S06
source_url: https://docs.openwebui.com/docs/features/tools/runtime-api/
source_type: documentation
tags: [Tools, API, Runtime]
summary: >-
  Documentation of the runtime interface exposed to tools, including context
  payloads, messaging protocol, error handling, and security constraints.
updated_at: 2025-02-14
---

# Tool Runtime API Reference

## Summary
The runtime API reference explains how Open WebUI executes tools and exchanges
data. It covers request payload formats, authentication tokens, streaming
interfaces, and how to return results or errors to the conversation thread.

## Key Points
- Defines the request envelope containing conversation state, user inputs, and
  any pipe or action metadata forwarded to the tool.
- Details synchronous versus asynchronous execution modes and how streaming
  outputs are surfaced to the chat UI.
- Clarifies sandbox limitations, network policies, and logging practices required
  to keep the system auditable.

## Key Terms
- **Execution context** — structured data passed to the tool on invocation.
- **Streaming channel** — mechanism for incremental responses from long-running
  tool operations.
- **Audit log** — persistent record of tool invocations for traceability.

## Implementation Notes
- Use the documented payload shapes when designing helper libraries for internal
  tools.
- Align error codes in custom tooling with the runtime reference to display
  consistent feedback to end-users.

## Source
- [Tool Runtime API](https://docs.openwebui.com/docs/features/tools/runtime-api/)

## Related Notes
- [S03 — Tools Feature Overview](03_tools-overview.md)
- [S04 — Authoring Custom Tools Guide](04_tools-authoring.md)
- [S08 — Building Function Handlers](08_functions-building.md)
