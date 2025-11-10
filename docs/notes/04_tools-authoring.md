---
id: S04
source_url: https://docs.openwebui.com/docs/features/tools/creating-tools/
source_type: documentation
tags: [Tools, Development, HowTo]
summary: >-
  Step-by-step instructions for creating new tools, covering scaffolding,
  manifest metadata, runtime handler implementation, and testing inside Open
  WebUI.
updated_at: 2025-02-14
---

# Authoring Custom Tools

## Summary
The authoring guide walks developers through scaffolding a new tool package. It
covers required directory layout, manifest fields, handler entry points, and
local debugging. The guide emphasizes how to validate input/output schemas and
register the tool through the admin console.

## Key Points
- Provides recommended project layout including `tool.yaml`, handler scripts,
  and assets for UI representation.
- Demonstrates how to annotate functions with metadata (parameters, response
  schema, rate limits) so Open WebUI can surface the tool reliably.
- Offers testing workflow: local invocation via CLI, sandbox execution, and
  verifying the tool within a sample pipe before publishing.

## Key Terms
- **tool.yaml** — manifest describing the tool for registration.
- **Handler entry point** — Python async function or HTTP endpoint executed when
  the tool is triggered.
- **Sandbox** — controlled environment for validating tool behavior safely.

## Implementation Notes
- Capture manifest snippets and CLI commands in our knowledge base to accelerate
  future tool development.
- Map testing recommendations to quality checklists for new tool contributions.

## Source
- [Creating Tools](https://docs.openwebui.com/docs/features/tools/creating-tools/)

## Related Notes
- [S05 — Tool Manifest Reference](05_tool-manifest.md)
- [S06 — Tool Runtime API Reference](06_tool-runtime-api.md)
- [S10 — Pipe Designer Walkthrough](10_pipe-designer.md)
