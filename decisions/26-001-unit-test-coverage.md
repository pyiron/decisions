# Require 90% unit test coverage - before 1.0 release

## Status

A number of packages in the pyiron organisation already achieved 90% unit test coverage, namely:
- https://github.com/pyiron/bagofholding
- https://github.com/pyiron/conda_subprocess
- https://github.com/pyiron/executorlib
- https://github.com/pyiron/pyfileindex
- https://github.com/pyiron/pyiron_snippets
- https://github.com/pyiron/pyiron_vasp
- https://github.com/pyiron/pyiron_workflow
- https://github.com/pyiron/pysqa
- https://github.com/pyiron/semantikon

## Context

For the 1.0 release which indicates a software is ready for production use, our users expect our software to be stable. 
This means especially successive versions should not break existing functionality unless indicated with a corresponding version change. 
Unit tests help us to maintain backwards compatibility and do not accidentally break existing functionality. 
Basically, everytime the unit tests have to change, this means functionality changed which means the next release should be a major release. 

Ideally, we would require 100% unit test coverage, still as this is challenging with increasing complexity the closer we get to 100% we restrict ourselves to 90% which has been achieved by a number of packages in the pyiron organization already. 

## Decision

A 1.0 release without 90% unit test coverage cannot be approved. 

## Consequences

Packages with more than 80% but less than 90% unit test coverage, which is currently the second largest group after the packages with >90% unit test coverage, cannot be released as 1.0 version without additional unit tests being added. 
