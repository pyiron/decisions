# Documentation Website 

## Status

Already implemented in:
- https://github.com/pyiron/atomistics
- https://github.com/pyiron/bagofholding
- https://github.com/pyiron/conda_subprocess
- https://github.com/pyiron/executorlib
- https://github.com/pyiron/flowrep/
- https://github.com/pyiron/lammpsparser
- https://github.com/pyiron/pyfileindex
- https://github.com/pyiron/pyiron_base
- https://github.com/pyiron/pyiron_core
- https://github.com/pyiron/pyiron_snippets
- https://github.com/pyiron/pyiron_workflow
- https://github.com/pyiron/pylammpsmpi
- https://github.com/pyiron/pysqa
- https://github.com/pyiron/structuretoolkit

## Context

Every package should have a short documentation website for new users to inform themselves about the functionality of the package before the release of version 1.0. 

## Decision

To keep the barrier for creating the documentation low, the minimal documentation only consists of three parts:
- `README.md` - to give a general high level introduction to the package.
- `example.ipynb` - A jupyter notebook to demonstrate the functionality of the package. This jupyter notebook has three usecases:
  - The jupyter notebook is rendered as a website to document the functionality of the package.
  - The jupyter notebook is executed as integration test to validate that the documentation is compatible to the latest version of the package.
  - The jupyter notebook can be tested live in interactive environments like mybinder to allow the users to test the software directly in their webbrowser.
- A rendered version of the docstrings for users to search for a specific function and understand how to use it,  

## Consequences

While creating documentation in addition to inline docstrings is additional work, it hopefully helps to attract more users for the packages we develop as part of the pyiron organization. 
