# Architecture

AI-Hub centralizes AI access for multiple independent applications.

## Components

### Central Gateway
Receives logical AI tasks, applies central routing/configuration, invokes the selected backend, and returns normalized results.

### Async Worker
Separates background and queue-oriented work from the request-facing gateway.

### Administration Service
Provides operational management independently from the main gateway.

## Design Principles
1. Centralize provider complexity.
2. Keep provider secrets out of client projects.
3. Prefer task-level contracts over provider-specific contracts.
4. Separate background work from request handling.
5. Make provider/model changes centrally configurable.
6. Keep client processes independent from AI-Hub service lifecycle.
