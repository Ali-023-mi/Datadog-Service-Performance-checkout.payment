
# Checkout Service — Datadog Performance Report

## Overview

This report documents observed request durations for the
`checkout-service`, monitored using Datadog APM.

## Service Details

- Service: checkout-service
- Framework shown in traces: FastAPI
- Endpoint: GET /api/v1/checkout
- Operation: checkout.process_payment
- Data source: Datadog trace list

## Observed Results

| Metric | Result |
|---|---:|
| Trace entries reviewed | 9 |
| Average displayed duration | 310.7 ms |
| Minimum displayed duration | 302 ms |
| Maximum displayed duration | 343 ms |

## Individual Trace Durations

| Trace timestamp (Oct 04) | Duration |
|---|---:|
| 16:36:23.893 | 303 ms |
| 16:36:21.063 | 305 ms |
| 16:36:18.231 | 309 ms |
| 16:29:41.588 | 305 ms |
| 16:29:38.767 | 302 ms |
| 16:29:35.927 | 321 ms |
| 15:55:44.474 | 304 ms |
| 15:55:41.626 | 304 ms |
| 15:55:38.791 | 343 ms |

## Notes

These statistics are calculated from the nine trace entries
visible in the Datadog trace list provided for this report.
They do not represent all requests during the monitoring period.

The year and timezone of the displayed timestamps have not
been independently verified.

## Monitoring Platform

Datadog APM

[Open Datadog](https://app.datadoghq.eu/)
