# TurfTrigger — Operating a Weather-Driven Application

[← Portfolio](../README.md) · [Application](https://turftrigger.com)

**Personal project · Sole project owner and human contributor**

TurfTrigger turns local conditions and regional rules into personalized plans
and SMS alerts, with email delivery also supported.

## My role and approach

I own the requirements, service integration, validation, release decisions, and
ongoing operation. I used AI agents throughout coding, research, troubleshooting,
testing, and design, directing the work around the product's needs.

Development combines documented requirements, review notes, automated checks,
and investigation of actual behavior.

## How the project developed

The project grew from a local lookup into a connected service through ongoing
iteration:

- **Foundation:** interface, external data, identity, storage, and scheduled updates.
- **Consistency:** shared rules and checks that plans agree with alerts.
- **Operations:** release verification, completion monitoring, and permission tests.
- **Validation:** replay of decisions, messages, and simulated user responses.
- **Refinement:** incident investigation and focused regression coverage.

## The knowledge behind SMS alerts

The engine combines local conditions, regional context, user preferences, and
recorded activity with shared decision rules.

| Supporting data | Purpose |
|---|---|
| Regional profiles | Inform advice using grass characteristics and local conditions. |
| Seasonal plans | Supply structured, climate-appropriate plan content. |
| Product information | Support product-selection surfaces. |
| Safety references | Support regression checks on the advice. |

These datasets serve different roles. Profiles and rules inform live decisions;
plan content, product information, and safety checks support other parts of the
experience. SMS delivery also checks consent, local timing, and delivery state.

## Keeping decisions consistent

A rule change can affect a plan, a display, a message, and a follow-up. Shared
decision functions reduce drift, while historical replay checks how those
surfaces behave together and respond to recorded user activity.

## Protecting scheduled work

A scheduler retry exposed a duplicate-delivery risk during startup. An atomic
claim now reserves a job's time slot so competing workers skip it. A raised
failure attempts to release the claim for retry.

Regression checks cover duplicate suppression, independent work, and retry
behavior. Partial delivery and unexpected termination still require recovery
procedures and recipient-level state.

## Monitoring and release verification

Scheduled stages record successful completion. Health checks detect missing or
stale signals, covering failures that error logs alone can miss.

Runtime release identifiers and hosted-content checks help verify what actually
runs after deployment. The release baseline advances only after verification
succeeds.

## Access, recovery, and testing

Data rules distinguish public information, owner-scoped records, administrative
access, and server-only fields. Permission tests check those boundaries.

Recovery documentation records backup and configuration dependencies. A complete
restore exercise remains an outstanding validation task.

Workflow replay follows decisions through delivery and simulated user actions.
Its limits are documented: historical hindsight differs from a real forecast,
and internal consistency does not establish field accuracy.

[View the product screenshots and case study →](https://mlaurie1620.github.io/Portfolio/turftrigger.html)
