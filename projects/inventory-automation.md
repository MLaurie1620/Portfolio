# Inventory & Vendor Automation

**Workplace · Team project**

A workflow connecting service-management tickets, vendor files, live inventory
data, and business systems.

## My contribution

I built file intake and validation, integrated database checks, and implemented
ticket updates that explain data-quality issues and requested movements that
conflict with the system of record.

## Workflow

Scheduled workers process submitted files, check live inventory data, apply
recorded corrections, and return actionable results to the ticket. Financial
movements enter the appropriate business integration process; operational
updates stay within the service platform.

## Engineering focus

- **Data integrity:** business rules check formats, identifiers, product mappings,
  locations, asset state, and the requested transaction.
- **Useful feedback:** early structural checks, batched lookups, and line-level
  reporting help submitters resolve issues together.
- **Recoverable operation:** rate limits, timeouts, retries, token refresh, and
  processing locks support reliable scheduled work.
- **Queue controls:** conflicting requests are reported, duplicates are skipped,
  and unavailable dependencies preserve a retry path.
- **Auditability:** corrections, outcomes, and failures are recorded in logs and
  ticket reports.

Related tools support bulk asset lookup, physical inventory updates, and vendor
purchase-order integrations.

[View the case study →](https://mlaurie1620.github.io/Portfolio/inventory.html)
