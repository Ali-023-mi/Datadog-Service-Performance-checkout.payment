
# FastAPI Service Performance Report

## Overview

This report documents observed request durations and HTTP
status codes from Datadog APM for the FastAPI service.

## Service Details

- Service: fastapi
- Framework: FastAPI
- Operation: fastapi.request
- Span kind: server
- Environment: none (as displayed in Datadog)
- Monitoring period: Historical Search, 1 month
- Timestamp timezone: UTC+02:00

## Observed Endpoint Results

| Endpoint | Displayed Requests | HTTP Status |
|---|---:|---|
| GET /api/v1/user/{user_id} | 3 | 500 |
| GET /api/v1/checkout | 9 | 200 |
| GET / | 6 | 200 |
| GET /favicon.ico | 5 | 404 |

These counts represent the trace entries included in this report,
not necessarily all requests during the monitoring period.

## User Endpoint — Error Observations

| Timestamp (Oct 04) | Duration | HTTP Status |
|---|---:|---:|
| 16:36:26.502 | 55.3 ms | 500 |
| 16:29:44.210 | 71.0 ms | 500 |
| 15:55:47.057 | 56.1 ms | 500 |

Average duration of these three displayed requests: 60.8 ms.

The HTTP 500 responses indicate server errors. Further
investigation is needed to identify their cause.

## Checkout Endpoint — Successful Observations

| Timestamp (Oct 04) | Duration | HTTP Status |
|---|---:|---:|
| 16:36:23.893 | 303 ms | 200 |
| 16:36:21.063 | 305 ms | 200 |
| 16:36:18.231 | 309 ms | 200 |
| 16:29:41.588 | 305 ms | 200 |
| 16:29:38.767 | 302 ms | 200 |
| 16:29:35.927 | 321 ms | 200 |
| 15:55:44.474 | 304 ms | 200 |
| 15:55:41.626 | 304 ms | 200 |
| 15:55:38.791 | 343 ms | 200 |

Average duration of these nine displayed requests: 310.7 ms.

## Additional Endpoint Observations

The root endpoint (GET /) returned HTTP 200 in the displayed
traces. The favicon endpoint (GET /favicon.ico) returned
HTTP 404 in the displayed traces. The significance of these
404 responses should be checked against the application's
expected behavior.

## Summary

The displayed traces show successful checkout and root
requests, server errors on the user endpoint, and missing
favicon responses. These observations provide a starting
point for further service-performance investigation.

## Monitoring Source

Datadog APM

[Open Datadog EU](https://app.datadoghq.eu/)
