# Python Project Template
![Python Version from PEP 621 TOML](https://img.shields.io/python/required-version-toml?tomlFilePath=https%3A%2F%2Fraw.githubusercontent.com%2Fgemmadanks%2Fcoracle%2Frefs%2Fheads%2Fmain%2Fpyproject.toml)
[![codecov](https://codecov.io/gh/gemmadanks/coracle/graph/badge.svg?token=SJVFI32RHC)](https://codecov.io/gh/gemmadanks/coracle)
[![CI](https://github.com/gemmadanks/coracle/actions/workflows/ci.yaml/badge.svg?branch=main)](.github/workflows/ci.yaml)
[![release-please](https://github.com/gemmadanks/coracle/actions/workflows/release-please.yaml/badge.svg)](release-please-config.json)
[![Docs (GitHub Pages)](https://github.com/gemmadanks/coracle/actions/workflows/docs-pages.yaml/badge.svg)](https://github.com/gemmadanks/coracle/actions/workflows/docs-pages.yaml)
[![Docs (RTD)](https://app.readthedocs.org/projects/coracle/badge/?version=latest)](https://gemmadanks-coracle.readthedocs.io/en/latest/)
[![Dependabot](https://img.shields.io/github/issues-search?query=repo%3Agemmadanks%2Fcoracle%20is%3Apr%20author%3Aapp%2Fdependabot%20is%3Aopen&label=Dependabot%20PRs)](https://github.com/gemmadanks/coracle/issues?q=is%3Apr%20is%3Aopen%20author%3Aapp%2Fdependabot)
[![uv](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/uv/main/assets/badge/v0.json)](https://github.com/astral-sh/uv)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

An experimental Python package for radio astronomy data processing.

## 📦 Installation

### Working in a development container
A [Dockerfile](./devcontainer/Dockerfile) and [configuration](./devcontainer/devcontainer.json) in [./devcontainer](./devcontainer) can be used in VSCode or GitHub Codespaces to work in a pre-configured development environment. It uses a Python 3.14 base image and installs uv, just and all Python dependencies.

To open the project in the container VSCode, you will need to add the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) and download [Docker](https://docs.docker.com/get-started/get-docker/) (or [Podman](https://podman.io/docs/installation) -- and [configure VSCode to use podman instead of Docker](https://code.visualstudio.com/remote/advancedcontainers/docker-options#_podman)) -- see the [VSCode tutorial on devcontainers](https://code.visualstudio.com/docs/devcontainers/tutorial) for more details on using devcontainers. Then run:
``` bash
Dev Containers: Reopen in Container
```

### Manual installation

1. [Install uv](https://docs.astral.sh/uv/getting-started/installation/)
1. Clone and install the project using uv:
```bash
git clone https://github.com/gemmadanks/coracle
cd coracle
uv sync --all-groups
```
1. [Install just](https://just.systems/man/en/packages.html).
1. Install pre-commit hooks (only needs to be done once)
```bash
just pre-commit-install
```
Hook definitions: [.pre-commit-config.yaml](.pre-commit-config.yaml)

## 🏁 Quickstart

```python
from coracle.greet import say_hello
print(say_hello("World"))
```

## 🧪 Common Tasks

Several common tasks have been added as recipes to a [justfile](justfile) in the root of the repository:

```bash
just install               # uv sync
just test                  # run quick (non-slow) tests
just test-notebooks
just lint                  # ruff check
just format                # ruff format
just type-check            # pyright type-check
just docs-serve            # live docs
just docs-build            # build docs
just pre-commit            # run all pre-commit hooks
just clean                 # remove generated files and folders
```

## 📚 Documentation

Documentation is hosted on [Github pages](https://open-research.gemmadanks.com/coracle/).

## 🤝 Contributing

Use [conventional commit](https://www.conventionalcommits.org/) messages (feat:, fix:, docs:, etc.). Ensure:

- Lint & format clean
- Tests pass
- Docs build without warnings
- ADR drafted for architecturally significant changes

Suggestions and improvements to this template are very welcome — feel free to open an issue or pull request if you spot something that could be refined, added or removed.

## 📖 Citation

If used in research, cite via [CITATION.cff](CITATION.cff).

## 🛡 License

BSD-3-Clause – see [LICENSE](LICENSE).

Happy coding! 🚀
