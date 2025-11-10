---
id: SRC-002
source_url: https://docs.openwebui.com/features/plugin/tools/
source_type: documentation
tags:
  - tools
  - onboarding
  - function-calling
summary: Explains what Tools are, how to install and enable them for models, and how Default versus Native function-calling modes impact tool invocation.
updated_at: 2025-11-10
---

# Using Tools in Open WebUI

## Summary
- Tools are Python scripts that augment LLM chats with capabilities like web search, image generation, or text-to-speech.
- Installation flows include importing from the community library with one-click connectivity to an Open WebUI instance.
- Enables two activation paths: in-chat quick enable or model-level defaults via Workspace → Models configuration.
- Describes Default (prompt-based) versus Native (model-driven function calling) modes and when to use each.

## Operational Guidance
- Encourage curation of trusted tools; warn admins about executing unverified Python code.
- Remind users that AutoTool filters still require enabling underlying tools in model settings.
- Document the UI path for toggling function calling mode (Chat Controls → Advanced Params).

## Key Terms
- **Default Mode** – Tool prompting strategy for models without native function calling support.
- **Native Mode** – Direct function call support for models like GPT-4o with multi-tool chaining.
- **Tool Showcase** – Community catalog at https://openwebui.com/tools for discovering scripts.

## Implementation Notes
- Provide teams with checklists to review tool permissions and ensure persistent defaults for mission-critical flows.
- When training staff, highlight screenshot references for locating Chat Controls and Advanced Params.
- Capture AutoTool filter dependencies as part of knowledge index cross-links.

## Related Links
- [Tool development deep dive](./003_tool_development.md)
- [Events reference](./008_events_reference.md)
- [Pipeline filters for cross-environment execution](./013_pipeline_filters.md)
