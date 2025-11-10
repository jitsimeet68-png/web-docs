---
id: SRC-001
source_url: https://docs.openwebui.com/features/plugin/
source_type: documentation
tags:
  - overview
  - plugins
  - tools
  - functions
  - pipelines
summary: High-level orientation that distinguishes Open WebUI tools, functions, and pipelines, explaining user-facing management flows and when to choose each extension type.
updated_at: 2025-11-10
---

# Tools & Functions (Plugins) Overview

## Summary
- Defines **Tools** as abilities granted to LLMs for real-time or external data tasks, and **Functions** as extensions that modify Open WebUI itself (UI, providers, filters).
- Clarifies that **Pipelines** target advanced, API-compatible workflows meant to offload heavy processing beyond core Tools/Functions.
- Highlights installation and management UX: users import tools from the community library, while functions are administered via the Admin Panel and linked to models.
- Emphasizes low barrier to entry—features are pluggable and can be activated without code for most scenarios.

## Key Details
- Tools empower models with external capabilities like weather queries or stock retrieval, acting as plugins the model may call when relevant.
- Functions extend the platform by integrating new model providers, adding UI actions, or customizing filters; they are configured by admins and can apply globally or per model.
- Pipelines are positioned for expert use cases, converting capabilities into OpenAI API-compatible components and enabling distributed workloads.
- Management locations differ: Tools in Workspace tabs for models/prompts/knowledge; Functions in Admin Panel; Pipelines usually not required unless advanced infrastructure is needed.

## Key Terms
- **Tool** – Python-based capability exposed to the LLM during chat sessions.
- **Function** – Open WebUI extension modifying platform behavior, UI, or provider integrations.
- **Pipeline** – Externalized workflow packaged for OpenAI-compatible clients.

## Implementation Notes
- Encourage onboarding by importing curated tools/functions before attempting custom development.
- When advising teams, stress security review of community imports despite one-click install simplicity.
- Use this overview as the landing page in the knowledge index for routing stakeholders to deeper guides.

## Related Links
- [Tools usage guide](./002_tools_usage.md)
- [Functions types overview](./004_functions_overview.md)
- [Pipelines overview](./011_pipelines_overview.md)
