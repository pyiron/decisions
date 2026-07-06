# Use of the prefix `pyiron_` 

## Status

Changes required in:
- https://github.com/pyiron/pyiron_ontology - is archived 
- https://github.com/pyiron/pyiron_snippets - current discussion https://github.com/pyiron/pyiron_snippets/issues/75
- https://github.com/pyiron/pyiron_vasp - suggested name vaspparser
- https://github.com/pyiron/pyiron_module_template - should be renamed to `module_template`
- https://github.com/pyiron/pyiron-publication-template - should be renamed to `publication-template`

## Context

If the package `pyiron_atomistics` depends on `pyiron_base` and `pyiron_lammps` does not then it is confusing for our users why both packages use the prefix `pyiron_`. 
For the specific case of `pyiron_lammps` this was resolved by renaming it to `lammpsparser`. 

## Decision

The prefix `pyiron_` should be used exclusively for the pyiron workflow engine and packages which depend on the pyiron workflow engine.

## Consequences

* `pyiron_atomistics` depends on `pyiron_base` so the use of the `pyiron_` prefix is fine.
* `pyiron_base` is one version of the pyiron workflow engine.
* `pyiron_core` is one version of the pyiron workflow engine.
* `pyiron_workflow` is one version of the pyiron workflow engine.
* `pyironflow` is the visual programming interface based on `pyiron_workflow`.
* `pyiron_dataclasses` defines the HDF5 storage interface used by `pyiron_base` and `pyiron_atomistics`.
* `pyiron_potentialfit` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron_apt` is based on `pyiron_workflow`.
* `pyiron_workflow_atomistics` is based on `pyiron_workflow`.
* `pyiron_workflow_lammps` is based on `pyiron_workflow`.
* `pyiron_rdm` is based on `pyiron_base`.
* `pyiron_ontology` is archived, so no need to rename it.
* `pyiron_nodes` is based on `pyiron_workflow`.
* `pyiron_contrib` is based on `pyiron_base` and it is archived.
* `pyiron_gui` is based on `pyiron_base` and it is archived.
* `pyiron_dpd` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.
* `pyiron-installer` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.
* `pyiron_experimental` is based on `pyiron_base` and it is archived.
* `pyiron_VR_server` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron_VR` is based on `pyiron_VR_server` which itself is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron_continuum` is based on `pyiron_base` and it is archived.
* `pyiron_gpl` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.
* `pyiron_meltingpoint` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron-resources` defines the executables interface used by `pyiron_base` and `pyiron_atomistics`.
* `pyiron_developer_tutorial` is focused on `pyiron_atomistics` and it is archived.
* `pyiron_electrochemistry` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.
* `pyiron-dft-uncertainty` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron_atomistics_docs` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.
* `pyiron-galaxy-example` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.
* `pyiron_md_montecarlo` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron_generalized_dipole` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base`.
* `pyiron_jupyter_book` is based on `pyiron_atomistics` and consequently internally uses `pyiron_base` and it is archived.

