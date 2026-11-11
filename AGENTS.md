# AGENTS.md

Notes for AI agents working in this repository.

## Project

`tareas` — a Python CLI (Typer) that automates repetitive file tasks from the terminal. Managed with uv; Python 3.12+ (interpreter pinned via `.python-version`).

## Commands

- `uv sync` — create/regenerate `.venv` after changing dependencies
- `uv run tareas <args>` — run the CLI
- `uv run pytest` — run tests

## Layout

- src layout: package code lives in `src/tareas/`.
- The `tareas` console script (declared in `pyproject.toml` under `[project.scripts]`) points to `tareas.cli:app`, a Typer app expected in `src/tareas/cli.py`. If `uv run tareas` fails with `ModuleNotFoundError: No module named 'tareas.cli'`, that module has not been created yet — create it there rather than renaming the entry point.
- `pytest` is not a declared dependency yet; add it as a dev dependency (`uv add --dev pytest`) before writing the first tests.

## Conventions

- Write user-facing text in Spanish: README, docstrings, comments, CLI help, and commit messages. CLI subcommand names are Spanish too (e.g. `validar`, which is pre-approved in `opencode.json`).

## Hard rules

- Never commit `.env` files (secrets — see `.gitignore`).
- `git push`, `git reset`, `rm`, and `sudo` are denied by `opencode.json` policies. Do not attempt them; ask the user to run them instead.
