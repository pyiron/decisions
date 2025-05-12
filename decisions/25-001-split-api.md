# Decision 1 -- Split the API to user and dev sections

## Status

[Adopted](https://github.com/pyiron/decisions/pull/1)
- https://github.com/pyiron/executorlib/pull/644

[Amended](https://github.com/pyiron/decisions/pull/10)
- https://github.com/pyiron/executorlib/pull/644
- https://github.com/pyiron/pyiron_workflow/pull/643

## Context

- Tab-completability/simple exposure of tools is a `pyiron` goal
- Many users of our tools are scientists, not programmers
- Some users of our tools are deeply knowledgeable programmers
- Effectively using [semantic versioning](https://semver.org/) is a `pyiron` goal, but python provides no universal guidance on how
- Python provides no universal guidance on API management

## Decision

- `pyiron` packages should provide a concise user-facing API directly in the topmost `__init__.py` file; if appropriate for the package, they should provide a second API for power-users of the package under `api.py`.
- Objects included in both these APIs are what we consider for evaluating how to update the semantic versioning of new releases.

## Consequences

- Standard users should see a shorter tab-completion list 
- Power users consistently know where to look for an extended list of tools
- Users of all types get increased clarity of what is protected by our semantic versioning and what they use at their own risk
- Package maintainers may (but are not required to) use the `api.py` to manage deprecation cycles from tools exposed in `__init__.py`
