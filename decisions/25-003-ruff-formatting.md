# Decision 2 -- Adopt `ruff` for code formatting

## Status

[Adopted V1](https://github.com/pyiron/decisions/pull/13)

## Context

* Consistent code style improves readability and maintainability across contributors
* Manual style enforcement is error-prone and time-consuming
* Python lacks a universally enforced code formatting standard, but `ruff` has become widely accepted
* `ruff` requires more configuration than `black`, but correspondingly comes with more power and scope
* Contributors already use varying editors/IDEs, so an automated formatter ensures consistency

## Decision

* We adopt [`ruff`](https://github.com/astral-sh/ruff) as an official formatting tool for the codebase
* All code contributions will be formatted with `ruff` before merging
* CI will enforce this formatting via a pre-merge check
* A minimal set of `ruff` selections we activate is:
  * `"E"`, pycodestyle
  * `"F"`, Pyflakes
  * `"UP"`, pyupgrade
  * `"B"`, flake8-bugbear
  * `"SIM"`, flake8-simplify
  * `"I"`, isort
  * `"C4"`, flake8-comprehensions
  * `"ERA"`, eradicate
  * `"PL"`, pylint
* We supply no maximal set of `ruff` ignores, but these should be minimized according to common sense and available developer time

## Consequences

* Contributors must install and use `ruff` locally or rely on pre-commit hooks
* The initial adoption will require reformatting the codebase, possibly increasing diff noise temporarily
* Future diffs will focus on logic, not style, improving review clarity
* Long-term code readability will improve