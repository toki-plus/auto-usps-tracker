# Auto USPS Tracker

A case study of batch shipment-status collection and reporting for cross-border e-commerce operations.

The solution combines tracking-number import, status queries, retry handling, data normalization, and Excel reporting in a desktop workflow. Its goal is to reduce repetitive record-by-record lookup and manual spreadsheet preparation.

> This repository is a sanitized public case study. It contains the solution description and interface examples, but not the complete implementation or any customer and order data.

## Problem Context

Cross-border e-commerce teams need to monitor large sets of shipment identifiers. Opening a page for every item, copying status, and maintaining spreadsheets is slow and creates missed records, duplicates, and inconsistent formats.

Auto USPS Tracker separates the process into input validation, controlled concurrency, failure recovery, status normalization, and report generation.

## Intended Users

- Cross-border e-commerce operations teams
- Customer-service and supply-chain staff following shipment exceptions
- Business users preparing recurring logistics reports

## Solution Flow

```text
Tracking-number file
    -> Input validation
    -> Controlled query queue
    -> Retry and exception handling
    -> Status normalization
    -> Excel report
    -> Manual exception review
```

## Capabilities

- Import and validate tracking numbers in batches
- Use controlled concurrency to improve throughput
- Retry timeouts, temporary failures, and unexpected responses
- Normalize status fields and timestamps
- Separate delivered, in-transit, exception, and unresolved records
- Export Excel reports designed for filtering and follow-up
- Display progress, success counts, and exception counts in a desktop interface

## Technical Approach

- Python for orchestration, data processing, and report generation
- Playwright for browser sessions and page interaction
- Pandas and Excel tooling for normalization and reporting
- PyQt5 for configuration and progress feedback
- Retry, rate-limiting, and logging controls for external-service reliability

## Interface Example

![Tracking workflow](./images/cover_software01.png)

## Project Status

This repository presents a sanitized problem statement, workflow design, and interface prototype. The full implementation and runtime configuration are not public.

## Data and Compliance

- Never commit real customer information or tracking numbers to source control, logs, or screenshots.
- Automated access must follow USPS terms and use a reasonable request rate.
- Business users should review results before customer communication or operational decisions.

## License

See [LICENSE](./LICENSE).
