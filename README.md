# Matt Laurie

**Systems administration · Automation · Service reliability**

This portfolio highlights practical systems work through my personal projects:
automating recurring operations, enforcing access boundaries, verifying releases,
and turning failures into repeatable checks.

## Featured project: TurfTrigger

[TurfTrigger](https://turftrigger.com) turns local weather and regional lawn-care
rules into application timing, season plans, and notifications.

The application combines a React interface with Python services, Firebase, and
Google Cloud. Its operational tooling covers scheduled processing, completion
monitoring, release traceability, permission checks, and historical replay.

| Area | Project example |
|---|---|
| Automation reliability | Atomic job-slot claims protect scheduled sweeps from duplicate invocations. |
| Monitoring | Completion heartbeats expose jobs that never run or never finish successfully. |
| Change management | Runtime release identifiers and served-asset checks verify deployment results. |
| Access control | Owner-scoped data and server-only fields are enforced by database rules. |
| Workflow validation | Historical replays exercise decisions, delivery, and simulated user responses. |
| Recovery planning | A recovery runbook records dependencies and rebuild steps; a complete restore exercise remains an explicit validation task. |

**[Read the TurfTrigger systems case study →](projects/turftrigger.md)**

The case study includes an architecture diagram, an incident walkthrough, a
small implementation excerpt, and the tradeoffs behind the design.
