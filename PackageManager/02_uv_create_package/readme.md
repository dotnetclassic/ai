# Running a Python Package with `uv run --package`

This guide explains how to run a Python package using the `uv run` command with the `--package` option. This approach is especially useful if your project is structured as a package with an entry point defined in a `__main__.py` file.

---

## Command Syntax

To run a package, use the following command:

```sh
uv run --package packagename
```
This will generate the following project structure:

```
projectname/
├── src/
│   └── packagename/
│       └── __init__.py
├── .gitignore
├── pyproject.toml
└── README.md
```
Running the Project

```sh
uv run hello.py
```

pyproject.toml

```
[project]
name = "packagename"
version = "0.1.0"
description = "Add your description here"
readme = "README.md"
authors = [
    { name = "xx", email = "xx@xx.com" }
]
requires-python = ">=3.12"
dependencies = []

[project.scripts]
packagename = "packagename:main"

[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"
```