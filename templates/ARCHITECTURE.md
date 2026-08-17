# Architecture

## Problem and users

One sentence. Who uses this?

## High-level diagram

```mermaid
flowchart LR
    UI[UI / Browser] --> API[API]
    API --> STORE[Storage]
```

## Components

| Component | Responsibility | Tech |
|-----------|----------------|------|
| | | |

## API contract

| Method | Path | Body | Success | Errors |
|--------|------|------|---------|--------|
| | | | | |

## Data flow

1. User does X → API → storage → response

## Trade-offs (what we chose and why)

- Example: in-memory vs DB — chose X because of scope

## What we'd add at 10x scale

- PostgreSQL, auth, cache, load balancer — as a diagram, not homework to provision

## Security notes

- Secrets in env, not Git
- Input validation
- Auth: TODO / not in MVP (say so honestly)
