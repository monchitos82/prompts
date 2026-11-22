---
name: adversarial-review
description: >
  Read-only stress-testing checklist for finding edge cases, race conditions,
  failure modes, security gaps, and operational risks before merge or release.
---

# Adversarial Review Skill

## Stress-Test Assumptions
- Treat claims of safety, scale, or idempotency as hypotheses to verify against actual code, configs, and tests.
- Check boundary inputs, nulls, empty collections, off-by-one logic, timezone/encoding mismatches, and concurrent execution.

## Probe Failure and Security Boundaries
- Trace partial failures, network timeouts, retries without idempotency, deadlocks, memory spikes, and missing rollbacks.
- Inspect input validation, auth/permission boundaries, secret exposure in logs or errors, and unsafe defaults.

## Report Findings Clearly
- Keep changes strictly read-only; do not edit repository files during an audit.
- Rank issues by severity (**Critical**, **High**, **Medium**, **Low**) with **Location**, **Failure Scenario**, **Impact**, and **Required Fix**.
