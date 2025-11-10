---
id: S05
source_url: https://docs.openwebui.com/docs/features/tools/manifest/
source_type: documentation
tags: [Tools, Reference, Manifest]
summary: >-
  Reference specification for tool manifests detailing required fields, schema
  definitions, capability flags, and dependency declarations.
updated_at: 2025-02-14
---

# Tool Manifest Reference

## Summary
The manifest reference enumerates every configuration property available for
Open WebUI tools. It explains field types, default behaviors, and validation
rules, enabling consistent tool registration and discoverability within the UI.

## Key Points
- Documents identification metadata (name, version, author) and how they appear
  in the tool catalog.
- Describes capability flags (permissions, network access, environment needs)
  that inform security review and runtime sandboxing.
- Provides schema for inputs/outputs, including JSON Schema fragments, examples,
  and localization hints to improve prompts.

## Key Terms
- **Capability flags** — booleans controlling sensitive operations like file or
  network access.
- **Localization hints** — display strings and translations shown in the UI.
- **Schema fragment** — reusable JSON structure referenced across parameters.

## Implementation Notes
- Reuse manifest sections in internal templates to ensure new tools meet review
  criteria quickly.
- Capture example JSON in `docs/index.md` cross-references for quick copying.

## Source
- [Tool Manifest Reference](https://docs.openwebui.com/docs/features/tools/manifest/)

## Related Notes
- [S04 — Authoring Custom Tools Guide](04_tools-authoring.md)
- [S06 — Tool Runtime API Reference](06_tool-runtime-api.md)
- [S13 — Filters Overview](13_filters-overview.md)
