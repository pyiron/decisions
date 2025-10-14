# Decision 4 -- Adopt `pyproject.toml` as python project manager with `hatch` as build backend

## Status

Adopted in the following pull requests:
* https://github.com/pyiron/atomistics/pull/521
* https://github.com/pyiron/conda_subprocess/pull/113
* https://github.com/pyiron/executorlib/pull/657
* https://github.com/pyiron/pyfileindex/pull/203
* https://github.com/pyiron/pyiron_atomistics/pull/1793
* https://github.com/pyiron/pyiron_base/pull/1862
* https://github.com/pyiron/pyiron_lammps/pull/239
* https://github.com/pyiron/pyiron_vasp/pull/75
* https://github.com/pyiron/pylammpsmpi/pull/360
* https://github.com/pyiron/pysqa/pull/410
* https://github.com/pyiron/structuretoolkit/pull/379

## Context

* Consistent mapping of release versions distributed on pypi and conda to git tags to simplify debugging. 
* The python community is transitioning from `setuptools` to the more modern python project manager `hatch`. Read more in [why hatch](https://hatch.pypa.io/latest/why/).
* Embrace `pyproject.toml` files as standard configuration files, as those become the [python standard](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/).

## Decision

* We use `hatchling` as default build backend defined in our `pyproject.toml` files.
* We use `hatch-vcs` to map the git tag `<package name>-0.0.1` to the version number `0.0.1`. 

## Consequences

* With this change the outdated `setup.py` and `setup.cfg` files are no longer required, so remove those from all our repositories.
* Every release receives a git tag - we do not release versions with manually defined version numbers.
* While `versioneer` was a great tool which provided the same functionality, we no longer use it and replace it with `hatch-vcs` instead. 
