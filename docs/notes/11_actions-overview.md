---
id: S11
source_url: https://docs.openwebui.com/docs/features/actions/
source_type: documentation
tags: [Actions, Automation, Overview]
summary: >-
  Overview describing the Actions framework for triggering workflows based on
  events within Open WebUI conversations or external systems.
updated_at: 2025-02-14
---

# Actions Framework Overview

## Summary
The actions overview introduces event-driven automation inside Open WebUI. It
explains how actions listen to triggers, execute defined steps (tools, functions,
pipes), and deliver results back into conversations or external services.

## Key Points
- Enumerates built-in triggers such as conversation events, schedule timers, and
  webhooks.
- Discusses action composition: condition checks, tool invocations, and output
  routing.
- Highlights security considerations including authentication for outbound calls
  and permission scopes for sensitive actions.

## Key Terms
- **Trigger** — event initiating an action workflow.
- **Action handler** — the logic executed when a trigger fires.
- **Output channel** — destination for the action result (chat, notification, API).

## Implementation Notes
- Align action naming and descriptions with triggers so they are easily indexed.
- Document dependencies (tools, pipes) referenced by each action to maintain a
  traceable automation catalog.

## Source
- [Actions Overview](https://docs.openwebui.com/docs/features/actions/)

## Related Notes
- [S12 — Action Triggers Reference](12_action-triggers.md)
- [S09 — Pipes Architecture Overview](09_pipes-overview.md)
- [S13 — Filters Overview](13_filters-overview.md)
