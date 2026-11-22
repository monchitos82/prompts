---
name: observability
description: >
  Checklist for OpenTelemetry instrumentation, Collector pipelines, trace-log
  correlation, cardinality control, and actionable SLO alerts.
---

# Observability Skill

## Instrument and Correlate
- Propagate W3C trace context across HTTP, gRPC, message queues, and background jobs using current semantic conventions.
- Use low-cardinality span names and emit structured JSON logs with timestamps, `service.name`, `trace_id`, and `span_id`.

## Protect Cardinality and Collectors
- Keep unbounded values (`user_id`, `request_id`, raw IDs in paths, full stack traces) out of metric labels; bound histogram buckets to SLO targets.
- Place `memory_limiter` first and `batch` next in OpenTelemetry Collector pipelines, paired with bounded queues, retries, and PII/secret redaction.

## Alert on Symptoms
- Define SLIs and multi-window burn-rate or pipeline freshness alerts tied to real user or data-SLA impact and clear remediation steps.
