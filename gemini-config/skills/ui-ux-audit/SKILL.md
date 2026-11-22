---
name: ui-ux-audit
description: >
  Checklist for auditing and building accessible, responsive, high-performing
  web interfaces and UX states.
---

# Web and UI/UX Skill

## UX States and Hierarchy
- Handle `loading`, `empty`, `error`, `partial`, `disabled`, and `success` states explicitly with clear hierarchy and actionable recovery paths.
- Reuse existing design tokens, components, and layout patterns before adding new ones.

## Accessibility and Responsiveness
- Use semantic HTML first, support full keyboard navigation, keep focus indicators visible and unobstructed, and meet contrast and target-size targets.
- Verify layouts from narrow mobile widths up to desktop screens without horizontal overflow, clipped text, or reduced-motion conflicts.

## Performance and Frontend Safety
- Reserve dimensions for images and embeds to prevent layout shift (CLS), keep interactions responsive (INP), and prioritize critical content (LCP).
- Sanitize untrusted HTML, validate inputs at boundaries, and avoid storing sensitive tokens or secrets in browser storage.
