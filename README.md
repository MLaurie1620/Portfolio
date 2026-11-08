# Matt Laurie

**Systems administration · Integration · Automation**

**[Visit the portfolio website →](https://mlaurie1620.github.io/Portfolio/)**

Selected work connecting service-management workflows, APIs, and cloud systems,
with an emphasis on data integrity, recoverable processing, and operational
visibility.

## Inventory & Vendor Automation

**Workplace · Team project**

A scheduled automation suite that takes vendor CSV/Excel files from
service-management tickets, validates them against live asset data, and routes
financial movements to ERP integration folders. Results, corrections, and
line-level errors are returned to the original ticket.

**My contribution:** I built the CSV intake, owned all validation logic,
integrated PostgreSQL tables into the checks, and implemented ticket write-backs
to explain data issues and inventory movements that conflict with the system of
record.

- **20+ documented validation rules** covering formats, identifiers, catalog
  mappings, stockrooms, lifecycle state, and transaction requirements.
- **Reliable processing:** batched lookups, shared API rate limits, retry backoff,
  token refresh, per-ticket locks, and database queue conflict checks.
- **Related tools:** bulk asset search, physical inventory updates, and vendor
  purchase-order API integrations.

[Read the integration case study →](projects/inventory-automation.md)

## FundTrace — AI Audit Triage

**Workplace · Applied AI · Sole creator and project owner**

I created an AI-assisted workflow that shortlists vendor-funding email
conversations, quotes supporting evidence, and preserves auditor corrections. Development and
testing covered seven vendor archives.

A detailed single-vendor evaluation shortlisted **506 of 1,498 conversations**
and found **162 of 198 relevant conversations (82% recall)**. The case study
explains the miss rate, review workload, and limits of that benchmark.

[Read the AI workflow case study →](projects/fundtrace.md)

## TurfTrigger

**Personal project · Sole project owner and human contributor · Since May 2026**

[TurfTrigger](https://turftrigger.com) turns local weather and regional rules into
personalized lawn-care plans and SMS alerts. Developed using AI agents across
coding, research, troubleshooting, testing, and design.

The project combines React, Python, Firebase, and Google Cloud with completion
monitoring, runtime release verification, access controls, and historical replay.
Its supporting knowledge base includes 9 grass profiles, 48 grass-by-zone plans,
265 catalog products, 65 active-ingredient records, and 25 pesticide-safety
references, counted November 7, 2026. The case study explains how those datasets
support rules, product information, and regression checks.

[Read the TurfTrigger case study →](projects/turftrigger.md)

## Website

The static HTML/CSS source is in `docs/`, with locally hosted fonts and no
JavaScript dependency or analytics. GitHub Pages publishes `master:/docs`.
