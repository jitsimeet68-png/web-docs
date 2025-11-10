---
id: S09
source_url: https://docs.openwebui.com/docs/features/pipes/
source_type: documentation
tags: [Pipes, Orchestration, Overview]
summary: >-
  Overview of the Pipes system describing how multi-step workflows orchestrate
  tools, functions, and actions to support complex coding tasks in Open WebUI.
updated_at: 2025-02-14
---

# Pipes Architecture Overview

## Summary
The pipes overview introduces pipeline orchestration as a visual and declarative
way to automate sequences of assistant actions. It explains pipe building blocks,
execution semantics, and how to chain tools, function calls, and filters to
create reproducible coding workflows.

## Key Points
- Describes pipe components: input nodes, processing nodes (tools/functions),
  decision branches, and output nodes for delivering results.
- Explains execution semantics, including data passing, concurrency options, and
  error recovery strategies (retry, fallback steps).
- Highlights integration with Actions and Filters to trigger pipes automatically
  or post-process outputs before showing them to the user.

## Key Terms
- **Node** — individual step in a pipe, referencing a tool, function, or action.
- **Edge** — connection that transports structured data between nodes.
- **Fallback branch** — alternate path executed on failure.

## Implementation Notes
- Use this overview to map our documentation index into core pipe concepts for
  easier discovery.
- Document canonical workflow patterns (linting, deployment, code review) using
  pipe diagrams for quick replication.

## Source
- [Pipes Overview](https://docs.openwebui.com/docs/features/pipes/)

## Related Notes
- [S10 — Pipe Designer Walkthrough](10_pipe-designer.md)
- [S11 — Actions Framework Overview](11_actions-overview.md)
- [S13 — Filters Overview](13_filters-overview.md)
