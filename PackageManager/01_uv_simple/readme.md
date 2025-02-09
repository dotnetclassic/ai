# Creating a UV Project with `uv init`

This guide explains how to create a new Python project using the `uv init` command. The following example will not generate a `src` folder to manage packages.

---

## Initialize the Project

Run the following command to create a new project:

```sh
uv init projectname
```

projectname/
├── hello.py
├── .gitignore
├── pyproject.toml
├── requirements.txt
└── README.md

To run the project in the terminal, use:

```sh
uv run hello.py
```


