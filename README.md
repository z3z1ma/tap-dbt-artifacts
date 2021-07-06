# tap-dbt-artifacts
[![test](https://github.com/prratek/tap-dbt-artifacts/actions/workflows/test.yml/badge.svg)](https://github.com/prratek/tap-dbt-artifacts/actions/workflows/test.yml)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![PyPI Version](https://img.shields.io/pypi/v/tap-dbt-artifacts?style=flat)](https://pypi.org/project/tap-dbt-artifacts/)
[![License](https://img.shields.io/pypi/l/tap-dbt-artifacts)](LICENSE.md)
[![Python](https://img.shields.io/pypi/pyversions/tap-dbt-artifacts)](https://pypi.org/project/tap-dbt-artifacts/)

`tap-dbt-artifacts` is a Singer tap for dbtArtifacts.

Built with the Meltano [SDK](https://gitlab.com/meltano/singer-sdk) for Singer Taps.

## Installation

- [ ] `Developer TODO:` Update the below as needed to correctly describe the install procedure. For instance, if you do not have a PyPi repo, or if you want users to directly install from your git repo, you can modify this step as appropriate.

```bash
pipx install tap-dbt-artifacts
```

## Configuration

### Accepted Config Options

- [ ] `Developer TODO:` Provide a list of config options accepted by the tap.

A full list of supported settings and capabilities for this
tap is available by running:

```bash
tap-dbt-artifacts --about
```

### Source Authentication and Authorization

- [ ] `Developer TODO:` If your tap requires special access on the source system, or any special authentication requirements, provide those here.

## Usage

You can easily run `tap-dbt-artifacts` by itself or in a pipeline using [Meltano](www.meltano.com).

### Executing the Tap Directly

```bash
tap-dbt-artifacts --version
tap-dbt-artifacts --help
tap-dbt-artifacts --config CONFIG --discover > ./catalog.json
```

## Developer Resources

- [ ] `Developer TODO:` As a first step, scan the entire project for the text "`TODO:`" and complete any recommended steps, deleting the "TODO" references once completed.

### Initialize your Development Environment

```bash
pipx install poetry
poetry install
```

### Create and Run Tests

Create tests within the `tap_dbt_artifacts/tests` subfolder and
  then run:

```bash
poetry run pytest
```

You can also test the `tap-dbt-artifacts` CLI interface directly using `poetry run`:

```bash
poetry run tap-dbt-artifacts --help
```

### Testing with [Meltano](https://www.meltano.com)

_**Note:** This tap will work in any Singer environment and does not require Meltano.
Examples here are for convenience and to streamline end-to-end orchestration scenarios._

Your project comes with a custom `meltano.yml` project file already created. Open the `meltano.yml` and follow any _"TODO"_ items listed in
the file.

Next, install Meltano (if you haven't already) and any needed plugins:

```bash
# Install meltano
pipx install meltano
# Initialize meltano within this directory
cd tap-dbt-artifacts
meltano install
```

Now you can test and orchestrate using Meltano:

```bash
# Test invocation:
meltano invoke tap-dbt-artifacts --version
# OR run a test `elt` pipeline:
meltano elt tap-dbt-artifacts target-jsonl
```

### SDK Dev Guide

See the [dev guide](https://gitlab.com/meltano/singer-sdk/-/blob/main/docs/dev_guide.md) for more instructions on how to use the SDK to 
develop your own taps and targets.
