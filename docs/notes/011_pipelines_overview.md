---
id: SRC-011
source_url: https://docs.openwebui.com/features/pipelines/
source_type: documentation
tags:
  - pipelines
  - deployment
  - architecture
summary: Provides an overview of Open WebUI Pipelines, highlighting their purpose, setup workflow, Docker quick start, and integration with OpenAI-compatible clients.
updated_at: 2025-11-10
---

# Pipelines Overview

## Summary
- Pipelines are an Open WebUI initiative delivering modular workflows compatible with OpenAI API clients, aimed at heavy or externalized processing.
- Page warns not to use pipelines for basic provider support—Functions suffice; pipelines target distributed/custom logic scenarios.
- Lists example pipelines (function calling, RAG, monitoring, rate limiting, translation, toxicity filtering) sourced from the GitHub examples directory.
- Explains workflow diagrams and how to connect clients by pointing the OpenAI URL to the pipelines server.

## Deployment Guidance
- Docker quick start includes running the `ghcr.io/open-webui/pipelines:main` image, configuring connections via Admin Panel → Settings → Connections, and verifying pipeline activation.
- Highlights security warning about arbitrary code execution when importing pipelines.
- Provides fallback instructions for custom dependency pipelines using `PIPELINES_URLS` environment variable and direct admin install.

## Key Terms
- **Pipelines Server** – Separate service hosting Python workflows accessible via OpenAI-compatible endpoints.
- **PIPELINES_URLS** – Environment variable for preloading pipeline scripts.
- **Pipelines Tab** – Admin UI location for configuring valves per pipeline.

## Implementation Notes
- Ensure Docker networking between Open WebUI and pipeline container; use `host.docker.internal` when necessary.
- Document Python version requirements (3.11) and repository setup for on-prem installations.
- Encourage teams to maintain curated pipeline directories and follow security best practices.

## Related Links
- [Pipes reference](./012_pipes_reference.md)
- [Pipeline filters](./013_pipeline_filters.md)
- [Pipeline valves](./014_pipeline_valves.md)
