---
name: devex-golden-path
description: >
  Checklist for building frictionless local developer workflows, fast CI/CD
  pipelines, hardened containers, and reliable Kubernetes deployments.
---

# DevEx and Platform Skill

## Developer Experience
- Provide a single, documented local workflow (`justfile`, `Taskfile.yml`, `Makefile`, or Dev Container) with fast setup, lint, test, and local run targets.
- Keep local, CI, and production tooling aligned via pinned versions and lockfiles.

## Containers and CI/CD
- Use multi-stage builds, non-root users, minimal base images, `.dockerignore`, and graceful shutdown (`SIGTERM`) handling.
- Use short-lived OIDC credentials instead of static secrets, pin action/image versions, cache dependencies/layers, and fail fast on lint/security/test gates.

## Kubernetes Readiness
- Define CPU and memory requests and limits, startup/readiness/liveness probes, `PodDisruptionBudget`, `NetworkPolicy`, and externalized secrets.
- Avoid deprecated APIs and validate manifests with `helm lint`, `kubeconform`, or dry-run checks before rollout.
