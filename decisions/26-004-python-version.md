# Decision 4 -- We aim to support all Python versions from their initial release to the end of life.

## Status

* The majority of the packages in the pyiron organization support Python 3.11 to 3.14.
* Python 3.10 is currently not supported even though it only reaches end of life at the end of the month.
* Some - primarily scientific packages - lack support for Python 3.14 as dependencies are not yet updated. 

## Context

* We are restricted by the support of our dependencies.
* We can only support a new Python version once its is supported by all dependencies.
* We can only support the python version which is supported by the lower bounds of our dependencies.
* Some users use our software on computer clusters without internet access, so they have to transfer packages manual and might be forced to use the system Python version, which is typically older.

## Decision

* We define the supported Python versions in the `pyproject.toml`.
* For every supported Python version we provide a continuous integration job which is evaluated for each pull request before it is merged.
* While Python supports five different Python version at each time, we aim to support at least three different Python versions and a maximum of five Python versions. 

## Consequences

* Following the current release schedule we have to update the `pyproject.toml` and our continuous integration environment at least once a year.
* We restrict ourselves to not require the use of new features introduced in the Python language until they are supported by all active Python versions. For example we previously dropped Python 3.10 early because of the limited type hinting support. 
