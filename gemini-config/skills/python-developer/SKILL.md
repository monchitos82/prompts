---
name: python-developer
description: >
  Modern Python engineering skill covering current runtimes and tooling
  (Python 3.15 / 3.14, uv, Ruff, mypy, pytest), defensive programming, and
  clear change summaries.
---

# Python Developer Skill

## Versions and Environment
- Check `python --version` and `requires-python` in `pyproject.toml`; target current supported releases (Python 3.15 or 3.14) unless pinned otherwise.
- Manage environments and dependencies with `uv` (`uv add`, `uv add --dev`, `uv sync`, `uv run`). Do not use raw `pip` or manual `venv` activation.
- Verify exact package versions and APIs before adding or upgrading dependencies.

## Defensive Coding
- Keep functions small, cohesive, and well-typed on public parameters and return values.
- Always follow the zen of python to write readable, explicit, simple and well thought code.
- Validate external inputs early and raise specific exceptions instead of catching broad `Exception` silently.
- Handle edge cases explicitly: `None`, empty collections, boundary values, timeouts, partial I/O, and non-deterministic behavior.
- Avoid mutable default arguments, hidden global state, and unpinned dependencies.

## Checks and Change Summary
- Run `uv run ruff check .`, `uv run ruff format --check .`, `uv run mypy src tests`, and `uv run pytest` before finishing.
- Add or update `pytest` tests for new behavior and edge cases.
- Report every change in four brief sections: **What changed**, **Why**, **Risk and trade-offs**, and **Verification**.
