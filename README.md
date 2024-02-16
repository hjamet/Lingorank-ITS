# Lingorank_LLM

## Description

The aim of this project is to reproduce, study and improve the results presented in the article [**Large Language Models for Difficulty Estimation of Foreign Language Content with Application to Language Learning**](pdf/1%20Original%20Paper.pdf). It consists in the creation of a tool to assist French language learning by recommending content to be read according to the learner's language level.

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

### Installation 🐻

Once you have installed the above tools, you can install the project using the following commands:
```bash
> pyenv install 3.9.7 # Installs the version of Python used in the project
> pyenv local 3.9.7 # Defines the version of Python used in the project
> poetry install # Installs project dependencies
```

## Repository Convention & Architecture 🦥

### Architecture 🦜

* The notebooks folder contains the notebooks that we will return with our results
* All algorithms performing complex or persistent operations must be implemented in the src folder, one file per feature. Give preference to object-oriented programming. These objects will then be called in the notebooks.
* We use Poetry for managing virtual environments & installing dependencies. See
    * https://python-poetry.org/
    * https://github.com/pyenv/pyenv
* All files other than source files are numbered to facilitate reading. Source files are named according to their functionality.

### Convention 🦦

* **[DOCSTRING]** : We use typed google docstrings for all functions and methods. See https://www.python.org/dev/peps/pep-0484/ and https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html . Docstring and notebooks should be written in English.
* **[TEST]** : All files in src should be summarily tested. Ideally, leave a simplistic example of use commented out at the bottom of each file to demonstrate its use. No need to use PyTest absolutely, we're not monsters either :D
* **[GIT]** : We use the the commit convention described here: https://www.conventionalcommits.org/en/v1.0.0/ . You should never work on master, but on a branch named after the feature you are working after opening an issue to let other members know what you are working on so that you can discuss it. When you are done, you can open a pull request to merge your branch into master. We will then review your code and merge it if everything is ok. Issues and pull requests can be written in French.

> Of course, anyone who doesn't follow these rules, arbitrarily written by a tyrannical mind, is subject to judgmental looks, cookie embargoes and denunciatory messages with angry animal emojis.