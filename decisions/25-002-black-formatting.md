# Decision 2 -- Adopt `black` for code formatting

## Status

Proposed

## Context

* Consistent code style improves readability and maintainability across contributors
* Manual style enforcement is error-prone and time-consuming
* Python lacks a universally enforced code formatting standard, but `black` has become widely accepted
* `black` enforces a strict, opinionated style which avoids bikeshedding over formatting decisions
* Other tools (e.g., `isort`, `ruff`) exist, but `black` covers a broad scope with minimal configuration
* Contributors already use varying editors/IDEs, so an automated formatter ensures consistency

## Decision

* We adopt [`black`](https://github.com/psf/black) as the official formatting tool for the codebase
* Formatting will follow `black`’s default configuration
* All code contributions must be formatted with `black` before merging
* CI will enforce this formatting via a pre-merge check

## Consequences

* Contributors must install and use `black` locally or rely on pre-commit hooks
* The initial adoption will require reformatting the codebase, possibly increasing diff noise temporarily
* Future diffs will focus on logic, not style, improving review clarity
* Tooling becomes simpler by relying on a single, robust formatter
