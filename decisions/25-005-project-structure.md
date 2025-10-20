# Decision 5 -- Adopt recommended directory structure for Python packages

## Status

Adopted in the following pull requests:
* https://github.com/pyiron/conda_subprocess/pull/155
* https://github.com/pyiron/executorlib/pull/846
* https://github.com/pyiron/pyfileindex/pull/242

## Context

* The official Python documentation provides a [recommendation how to structure a Python package](https://packaging.python.org/en/latest/tutorials/packaging-projects/).
* It recommends to store the Python package in `src/package_name` rather than `package_name` as it is currently done inside the pyiron organisation. 
* By maintaining consistency with the official Python documentation we make the pyiron project more accessible for external developers. 

## Decision

* We follow the recommendation of the official Python documentation for packaging the Python packages inside the pyiron organisation and store the Python packages in `src/package_name` rather than `package_name`.

## Consequences

* For configuration files like the `pyproject.toml` file we need less input parameters as `src/package_name` is already defined as default.
* Moving all files of a Python package can render existing pull requests incompatible, consequently it is recommended to first merge all open pull requests before changing the repository structure.
