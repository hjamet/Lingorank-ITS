# Lingorank_LLM

## Description

This repository contains the code needed to reproduce the experiences of the paper **Difficulty Estimation and Simplification of French Text Using LLMs** submitted to the [ITS 2024] conference (https://iis-international.org/its2024-generative-intelligence-and-its/#). The aim of this paper is to propose a method for estimating the difficulty of French texts and simplifying them using generative language models.

## Installation 🐼

### Requirements 🐨

This project uses the following tools:
- [Pyenv](https://github.com/pyenv/pyenv-installer) : Python version manager
- [Poetry](https://python-poetry.org/docs/#installation) : Python package manager
Tools that you can install using the following commands:
```bash
> curl https://pyenv.run | bash
> curl -sSL https://install.python-poetry.org | python3 -
```

These tools are not necessary to carry out the project, but they are recommended to guarantee the reproducibility of the experiments.

### Installation 🐻

Once you have installed the above tools, you can install the project using the following commands:
```bash
> pyenv install 3.9.7 # Installs the version of Python used in the project
> pyenv local 3.9.7 # Defines the version of Python used in the project
> poetry install # Installs project dependencies
```

Or, if you don't want to use the above tools, you can install the project using the following commands (assuming you have Python 3.9.7 or equivalent installed):
```bash
> python -m venv .venv
> source .venv/bin/activate
> pip install -r requirements.txt
```

## Architecture 🐯

The project is organized as follows:
- `data/` : Contains the data used in the project