# Structure the tests folder

## Status

Already implemented in:
- https://github.com/pyiron/bagofholding
- https://github.com/pyiron/executorlib
- https://github.com/pyiron/flowrep/
- https://github.com/pyiron/pyfileindex
- https://github.com/pyiron/pyiron_module_template
- https://github.com/pyiron/pyiron_ontology
- https://github.com/pyiron/pyiron_snippets
- https://github.com/pyiron/pyiron_workflow
- https://github.com/pyiron/pysqa
- https://github.com/pyiron/semantikon

## Context

Continous Integration tests validate the functionality of a software package. In particular when a bug is itentified it is important that the barrier to add a new test is minimal. 

## Decision

For the projects in the pyiron organization we implement a standardized directory structure for the `tests` folder in alphabetical order:
* `tests/benchmark` for benchmarking the functionality of package, e.g. measuring the performance. 
* `tests/integration` for integration tests which test the functionality of the package through the user interface, ideally in the same way a user would interact with the software.
* `tests/static` for files which are required for the evaluation of the tests, this could be configuration files or example input and output files.
* `tests/unit` for unit tests, these tests validate the functionality of individual modules of the package. The structure of the unit tests should mirror the internal structure of the package.

## Consequences

With every refactoring of the package we also have to refactor the tests folder, at least the `tests/unit` folder. Still this task can be completed by LLMs. 
