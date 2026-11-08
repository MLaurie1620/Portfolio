# Inventory & Vendor Automation

**Workplace · Team project**

An automation suite connecting service-management tickets, vendor files, live
asset data, database queues, and ERP processing.

## Problem and workflow

Vendor inventory movements arrived as CSV or Excel files that required manual
checks and individual asset lookups. Scheduled workers process ticket
attachments, validate records, apply defined corrections, and return readable
results to the original ticket.

Financial movements are written as JSON to ERP integration folders. Other
transactions use a platform-only destination. PostgreSQL queues on GCP VMs
are checked for duplicates and conflicting records already in flight.

## What makes it useful

- **20+ documented validation rules:** file structure, identifiers, SKU mappings,
  stockrooms, lifecycle state, and transaction requirements.
- **Efficient feedback:** early header rejection, batched lookups, and all
  failures reported together with line numbers.
- **Visible corrections:** normalization and defined data corrections are logged
  in the validation report.
- **Recoverable processing:** rate limits, timeouts, retry backoff, token refresh,
  and per-ticket locks support parallel workers.
- **Queue-aware routing:** unavailable databases leave tickets in progress for
  retry; conflicts are reported and identical in-flight records are skipped.
- **Controlled operation:** dry runs, local SQLite routing tests, environment
  configuration, and explicit flags for live purchase-order sending.

## Related tools

| Tool | Purpose |
|---|---|
| Bulk asset search | Return device, model, and location details as a CSV attached to the ticket. |
| Physical inventory | Validate uploaded counts, update the platform, and return per-row results. |
| Vendor purchase orders | Transform orders, authenticate and send through vendor APIs, and write confirmation to the platform. |

The project demonstrates service-management integration, REST APIs, data
validation, database queue controls, scheduled automation, troubleshooting,
and auditability.

[View the case study →](https://mlaurie1620.github.io/Portfolio/inventory.html)
