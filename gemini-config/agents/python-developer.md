---
name: python-developer
description: >
  Modern Python engineering skill enforcing latest stable runtimes and tooling
  (Python 3.15 / 3.14, uv, Ruff, mypy, pytest), defensive programming, and
  clear, concise change summaries. Use when writing, refactoring, reviewing, or
  testing Python code.
---

# Python Developer Skill

## 1. Versions and Tooling Defaults
- Target **Python 3.15** (latest release) or **Python 3.14** (active bugfix series) unless the project `pyproject.toml` explicitly pins an older supported release. Check `python --version` and `requires-python` before writing code.
- Use **uv** for Python versions, virtual environments, and dependencies (`uv add`, `uv add --dev`, `uv sync`, `uv run`) rather than raw `pip` or manual `venv` activation.
- Use **Ruff** (`ruff check` and `ruff format`) for linting and formatting, **mypy** (`strict = true`) for static type checking, and **pytest** for testing.
- Prefer current stable library APIs; verify exact version numbers and release status before adding or upgrading dependencies.

## 2. Best Practices and Defensive Programming
- Keep modules cohesive, functions small with clear inputs/outputs, and type annotations explicit on public APIs and return values.
- Validate inputs and external boundaries early (schema/type/range checks); fail loudly with specific exceptions rather than swallowing errors in broad `except Exception:` blocks.
- Guard against edge cases: empty collections, `None`, boundary numbers, timeouts, partial writes, and non-deterministic I/O.
- Avoid mutable default arguments, implicit global state, and unpinned/unverified dependencies.

## 3. Linting and Testing Workflow
- Run checks inside the managed environment before finishing:
  ```bash
  uv run ruff check .
  uv run ruff format --check .
  uv run mypy src tests
  uv run pytest
  ```
