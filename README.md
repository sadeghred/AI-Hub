# AI-Hub

**Central AI Gateway & Orchestration Layer for Multi-Project AI Workloads**

[فارسی](README.fa.md) · [Architecture](docs/en/ARCHITECTURE.md) · [Security](docs/en/SECURITY.md) · [Integrations](docs/en/INTEGRATIONS.md) · [Roadmap](docs/en/ROADMAP.md)

> **Public repository:** Project presentation and documentation only. Private source code, deployable packages, credentials, provider keys, production backups, and application downloads are not published here.

## Overview

AI-Hub is a centralized AI service that allows multiple independent applications to use AI through one controlled gateway instead of embedding provider-specific SDKs, credentials, routing rules, and fallback logic in every project.

## Core Capabilities

- **One AI gateway for multiple projects**
- Central provider and model configuration
- Task-oriented routing instead of hard-coded provider calls
- Provider/model fallback and credential rotation architecture
- Provider credentials isolated from client applications
- Independent asynchronous worker
- Independent administration service
- Central PostgreSQL-backed state/configuration
- Independent Linux service control

## Architecture

```text
Client Projects
      |
      v
AI-Hub Gateway
      |
      +----> Task Routing ----> Provider / Model ----> AI Provider(s)
      |
      +----> Async Worker
      |
      v
Structured Result -> Client Project

Administration Service
```

The confirmed deployment separates the platform into three services:

| Component | Purpose |
|---|---|
| Central Gateway | Receives and routes AI tasks |
| Async Worker | Processes background/asynchronous jobs |
| Administration Service | Operational management |

## Integration Model

`Client Project → AI-Hub → Provider / Model → Structured Result → Client Project`

A confirmed integration is **Tel-News**, a multi-source news processing and publishing system. AI-Hub provides the central AI layer for selected semantic operations while Tel-News remains independent of a specific AI provider.

## Security by Design

Client applications do not need direct access to external AI-provider credentials. Public documentation intentionally excludes API keys, tokens, passwords, private server details, database credentials, internal authentication secrets, and deployable private implementation.

## Operational Profile

In one measured stabilized near-idle deployment, the three AI-Hub processes together used approximately **210–220 MiB RSS**. This is an observed deployment figure, not a formal hardware requirement.

## Project Status

AI-Hub is operational central infrastructure and is being integrated progressively with other projects. This repository documents the architecture and capabilities without distributing the private implementation.

## Contact

- Telegram: [@Sadeghred](https://t.me/Sadeghred)
- Email: **Public email will be added after confirmation.**

---
© 2026 AI-Hub Project
