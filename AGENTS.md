# Agent instructions

## Project and architecture

Expense Tracker is a Python command-line application for adding, listing,
deleting, filtering, summarizing, and exporting expenses.

- `tracker.py` contains the CLI and the `ExpenseTracker` class.
- `test_tracker.py` contains the automated tests.
- `expenses.json` is the default data file used by the CLI.
- The app uses the Python standard library. Rich is optional.

## Setup and safe commands

Run these commands from the repository root in Windows PowerShell.

```powershell
py --version
py tracker.py --help
py test_tracker.py
py -m py_compile tracker.py test_tracker.py
git status --short
git diff
```

Use synthetic data in a temporary directory when testing operations
that write, delete, or export expenses.

## Coding and verification

- Keep edits small and follow the existing Python style.
- Reuse existing functions where possible.
- Preserve CLI commands and accepted behavior unless the task explicitly changes them.
- Add a focused test for each bug fix when feasible.
- Run the test suite and compilation check after code changes.
- Report the exact commands, actual results, and any skipped checks.

## Boundaries and review

- Do not access, include, or disclose secrets, credentials, or real personal data.
- Do not deploy to production or run destructive commands.
- Do not add, remove, or upgrade dependencies without human approval.
- During a read-only review, inspect and report findings without modifying project files.
- Present the diff and verification results for human review before committing,
  pushing, merging, or deploying.