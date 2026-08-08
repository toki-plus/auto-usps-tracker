# Auto USPS Tracker

[简体中文](./README.md) | [English](./README_en.md)

A case study of batch shipment-status collection and reporting for cross-border e-commerce operations.

The solution combines tracking-number import, status queries, retry handling, data normalization, and Excel reporting in a desktop workflow. Its goal is to reduce repetitive record-by-record lookup and manual spreadsheet preparation.

> This repository is a sanitized public case study. It contains the solution description and interface examples, but not the complete implementation or any customer and order data.

## Problem Context

Cross-border e-commerce teams need to monitor large sets of shipment identifiers. In peak season a single operator may need to check hundreds or thousands of USPS packages a day: open the tracking page for each one, copy the status, paste it back into a spreadsheet. A full reconciliation can take hours, and it produces missed records, duplicates, and inconsistent formats — exceptions such as delays, failed deliveries, and unknown numbers often surface only when a customer complains.

Auto USPS Tracker separates the process into input validation, controlled concurrency, failure recovery, status normalization, and report generation, turning record-by-record lookup into a single import that produces one report.

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

- **Batch import and validation**: import thousands of tracking numbers at once, with automatic de-duplication and format checks; invalid numbers are flagged before they enter the query queue
- **Batch status queries at compliant request rates**: Playwright drives real browser sessions with controlled concurrency and request throttling, improving throughput while respecting the target site's terms of service — not circumventing any access controls
- **Failure recovery**: timeouts, temporary failures, and unexpected responses are retried automatically; records that still fail are flagged explicitly in the report instead of being silently dropped
- **Detailed status extraction**: captures not only the latest status (Delivered, In Transit, etc.) but also the full status description and complete tracking history for exception tracing
- **Status normalization**: unifies status fields and timestamp formats, separating delivered, in-transit, exception, and unresolved records
- **Formatted Excel reports**: exports `.xlsx` reports with colored headers, wrapped text, borders, and auto-sized columns, grouped by status and ready for filtering and follow-up
- **Desktop progress feedback**: shows query progress, success counts, and exception counts in a PyQt5 interface, with optional HTTP proxy configuration for different network environments

## Technical Approach

- Python for orchestration, data processing, and report generation
- Playwright for browser sessions and page interaction
- Pandas and Excel tooling for normalization and reporting
- PyQt5 for configuration and progress feedback
- Retry, rate-limiting, and logging mechanisms that keep request pressure on the external service under control and make every record traceable

## 📸 Screenshots

<p align="center">
  <img src="./images/cover_software01.png" alt="Main interface" width="800"/>
  <br>
  <em>Main interface: import tracking numbers, configure parameters, and follow query progress.</em>
</p>
<p align="center">
  <img src="./images/cover_software02.png" alt="Exported report" width="800"/>
  <br>
  <em>The exported Excel report: grouped by status, consistently formatted, ready for follow-up.</em>
</p>

## Project Status

This repository presents a sanitized problem statement, workflow design, and interface prototype. The full implementation and runtime configuration are not public.

## Data and Compliance

- Never commit real customer information or tracking numbers to source control, logs, or screenshots; all interface screenshots in this repository are sanitized.
- Automated access must follow USPS terms of service and use a reasonable request rate; this solution controls request pressure through throttling and controlled concurrency, and neither includes nor encourages any circumvention of access controls.
- Business users should review results before customer communication or operational decisions.

## 📂 More Projects

- [video-mover](https://github.com/toki-plus/video-mover) — Automated multi-platform content distribution pipeline: media processing, metadata generation, scheduling, platform adapters
- [ai-highlight-clip](https://github.com/toki-plus/ai-highlight-clip) — Long-video smart triage: Whisper transcription + LLM scoring + human review
- [ai-ttv-workflow](https://github.com/toki-plus/ai-ttv-workflow) — Desktop text-to-video workflow with human-in-the-loop checkpoints
- [ai-video-workflow](https://github.com/toki-plus/ai-video-workflow) — Multi-model AIGC video pipeline orchestrating image, video and music services
- [ai-mixed-cut](https://github.com/toki-plus/ai-mixed-cut) — Video re-creation workflow via structured asset library and script reassembly
- [ai-trader-for-mt4](https://github.com/toki-plus/ai-trader-for-mt4) — LLM×MT4 controlled-execution framework: constrained tools, risk rules, state management
- [ai-trader-for-mt5](https://github.com/toki-plus/ai-trader-for-mt5) — AI trading assistant and EA engineering framework for MetaTrader 5
- [AB-Video-Deduplicator](https://github.com/toki-plus/AB-Video-Deduplicator) — Experimental video re-creation tool based on high-frame-rate blending
- [netease-downloader](https://github.com/toki-plus/netease-downloader) — Netease Cloud Music desktop downloader: QR login, queue, ID3 tagging

## License

See [LICENSE](./LICENSE).
