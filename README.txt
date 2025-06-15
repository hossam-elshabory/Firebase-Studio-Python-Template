<h1 align="center">Firebase Studio Python Dev Template</h1>

<p align="center">
<img src="https://img.shields.io/static/v1?label=Firebase+Studio&labelColor=000000&message=Python&color=0060ff&logo=firebase&logoColor=ff6e00&style=flat" alt="firebase"/>
</p>

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Included Packages](#included-packages)
- [VS Code Extensions](#vs-code-extensions)
- [Workspace Setup (On Create Hooks)](#workspace-setup-on-create-hooks)
- [Using this Repository as a Template](#using-this-repository-as-a-template)
  - [Quick Start](#quick-start)
  - [Detailed Steps](#detailed-steps)

## Introduction

## Features
This template provides a pre-configured development environment for Python projects, powered by Nix. It includes essential tools and VS Code extensions to streamline your workflow.

### Included Packages

The following core packages are installed in your development environment:

| Package                     | Description                                                   |
| :-------------------------- | :------------------------------------------------------------ |
| `pkgs.python311`            | Python 3.11                                                   |
| `pkgs.python311Packages.pip`| Pip for Python 3.11                                           |
| `pkgs.pipx`                 | Tool to install and run Python applications in isolated environments |

### VS Code Extensions

The following VS Code extensions are highly recommended and will be installed automatically upon workspace creation to enhance your development experience:


| Extension ID                            | Description                         |
| :-------------------------------------- | :---------------------------------- |
| `mhutchie.git-graph`                    | View a Git Graph of your repository |
| `mongodb.mongodb-vscode`                | MongoDB for VS Code                 |
| `ms-azuretools.vscode-docker`           | Docker extension                    |
| `pkief.material-icon-theme`             | Material Icon Theme                 |
| `redhat.vscode-yaml`                    | YAML Language Support by Red Hat    |
| `yzhang.markdown-all-in-one`            | Markdown All in One                 |
| `ms-toolsai.jupyter`                    | Jupyter                             |
| `ms-python.python`                      | Python extension                    |
| `charliermarsh.ruff`                    | Ruff                                |
| `KevinRose.vsc-python-indent`           | Python Indent                       |
| `ms-python.debugpy`                     | Debugger for Python                 |
| `ms-toolsai.jupyter-keymap`             | Jupyter Keymap                      |
| `ms-toolsai.jupyter-renderers`          | Jupyter Renderers                   |
| `ms-toolsai.vscode-jupyter-cell-tags`   | Jupyter Cell Tags                   |
| `ms-toolsai.vscode-jupyter-slideshow`   | Jupyter Slideshow                   |
| `saoudrizwan.claude-dev`                | Claude Dev                          |
| `codezombiech.gitignore`                | .gitignore                          |
| `luma.jupyter`                          | Jupyter                             |
| `usernamehw.errorlens`                  | ErrorLens                           |
| `streetsidesoftware.code-spell-checker` | Code Spell Checker                  |
| `oderwat.indent-rainbow`                | Indent Rainbow                      |
| `aaron-bond.better-comments`            | Better Comments                     |
| `bungcip.better-toml`                   | Better TOML                         |
| `Hamza-Aziane.obsidian-dark`            | Obsidian Dark Theme                 |

> [!NOTE]
> These extensions are installed automatically using the **Workspace lifecycle hooks** `OnCreate` in the `dev.nix` file

### Workspace Setup (On Create Hooks)

When a new workspace is created from this template, the following setup steps are automatically executed to prepare your development environment:

*   **Install VS Code Extensions:** Ensures `.vscode/extensions.json` exists and installs recommended extensions.
*   **Setting up Dev Environment:** Installs `poetry` and `commitizen` (with `cz-conventional-gitmoji`) using `pipx`, and ensures `pipx` is in your PATH.
*   **Setup Virtual Environment:** Creates a Python virtual environment (`.venv`) and activates it.
*   **Add VS Code to .gitignore:** Adds `.vscode/` to your `.gitignore` file if it's not already present.
*   **Remove Template Artifacts:** Cleans up template-specific files like `.git` and `README.md`.

## Using this Repository as a Template

This repository is designed to be easily used as a template for new Firebase Studio Python workspaces. Follow these simple steps to get started:

### Quick Start

1.  **In Firebase Studio:** Create a new workspace.
2.  **Select "Import from Git":** Choose this option when prompted for a template.
3.  **Enter Repository URL:** Use `https://github.com/firebase/firebase-studio-python-template` as the source.

Firebase Studio will then automatically set up your Python development environment, including all recommended VS Code extensions and tools.

### Detailed Steps

1.  **Open Firebase Studio:** Navigate to your Firebase Studio dashboard.
2.  **Initiate New Workspace Creation:** Click on the option to create a new workspace or project.
3.  **Choose Git Import:** When presented with template options, select "Import from Git" or a similar option that allows you to specify a Git repository.
4.  **Provide Repository URL:** In the field for the repository URL, paste the following:
    `https://github.com/firebase/firebase-studio-python-template`
    (Note: This repository must be publicly accessible for Firebase Studio to clone it.)
5.  **Confirm and Create:** Follow any remaining prompts to confirm the creation of your new workspace.

Once created, Firebase Studio will clone this template, and the `OnCreate` hooks defined in `dev.nix` will automatically configure your development environment, installing necessary Python packages and VS Code extensions.
