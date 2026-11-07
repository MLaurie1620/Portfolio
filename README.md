# Matt Laurie

**Systems administration · Automation · Service reliability**

**[Visit the portfolio website →](https://mlaurie1620.github.io/Portfolio/)**

This portfolio highlights practical systems work through my personal projects:
automating recurring operations, enforcing access boundaries, verifying releases,
and turning failures into repeatable checks.

## Featured project: TurfTrigger

[TurfTrigger](https://turftrigger.com) turns local weather and regional lawn-care
rules into application timing, season plans, and notifications.

**Solo project · Development recorded since May 15, 2026**

I am the sole project owner and human contributor. My responsibility spans the
product's requirements, its cloud services and integrations, validation, release
decisions, and ongoing operation. Over nearly six months of recorded development,
the project grew from a ZIP-code lookup into a service with regional decision
rules, personalized plans, notifications, and operational checks.

**Development approach: agentic engineering.** I used AI agents throughout
coding, research, troubleshooting, testing, and design. My role is directing
that work around the product's requirements and owning the resulting service,
its decisions, and its operation.

The application combines a React interface with Python services, Firebase, and
Google Cloud. Its operational tooling covers scheduled processing, completion
monitoring, release traceability, permission checks, and historical replay.

| Area | Project example |
|---|---|
| Agentic engineering | Applying AI agents across development, supported by documented requirements, tests, replay checks, and deployment verification. |
| Automation reliability | Atomic job-slot claims protect scheduled sweeps from duplicate invocations. |
| Monitoring | Completion heartbeats expose jobs that never run or never finish successfully. |
| Change management | Runtime release identifiers and served-asset checks verify deployment results. |
| Access control | Owner-scoped data and server-only fields are enforced by database rules. |
| Workflow validation | Historical replays exercise decisions, delivery, and simulated user responses. |
| Recovery planning | A recovery runbook records dependencies and rebuild steps; a complete restore exercise remains an explicit validation task. |

**[Read the TurfTrigger systems case study →](projects/turftrigger.md)**

The case study follows that development through dated milestones, difficult
technical decisions, an architecture diagram, and an incident walkthrough. It
connects the implementation to the skills involved and explains the limits of
the checks.

## Portfolio website

The GitHub Pages site presents the project overview and a dedicated TurfTrigger
case study. It also includes a high-level overview of a workplace project
integrating vendor hardware movement records, validation, PostgreSQL on GCP VMs,
and SAP APIs.

Website source lives in `docs/`. It is a static HTML/CSS site with locally hosted
fonts, no JavaScript dependency, and no analytics. GitHub Pages publishes the
`master` branch's `/docs` directory.
