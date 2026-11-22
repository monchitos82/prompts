---
name: data-engineering
description: >
  Repeatable checklist for designing, transforming, configuring, and serving
  data with strong efficiency, security, auditability, and scalability.
---

# Data Engineering Skill

## Define Contracts and Models
- Document table/event grain, primary or unique keys, nullability, data types, units, UTC timestamps, and schema evolution rules.
- Partition and cluster data around query predicates and retention windows rather than arbitrary high-cardinality columns.

## Transform Deterministically
- Make batch, micro-batch, and streaming jobs idempotent using deterministic keys, upserts/merges, or scoped partition overwrites.
- Handle duplicates, nulls, schema drift, and late-arriving records explicitly, with clear backfill and replay procedures.

## Configure, Secure, and Audit
- Enforce least-privilege access, secrets management, PII masking/encryption, and environment isolation.
- Set explicit timeouts, retries with backoff, dead-letter handling, concurrency limits, and compute/memory budgets.
- Track source provenance, run IDs, timestamps, lineage, row counts, and data quality assertions.
