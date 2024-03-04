# Lingorank_LLM

## Description

This repository contains the code needed to reproduce the experiences of the paper **Difficulty Estimation and Simplification of French Text Using LLMs** submitted to the [ITS 2024 conference](https://iis-international.org/its2024-generative-intelligence-and-its/#). The aim of this paper is to propose a method for estimating the difficulty of French texts and simplifying them using generative language models.

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

## Repository Architecture 🦥

The project is structured as follows:
```
.
├── notebooks
| ├── difficulty_estimation (7 notebooks for difficulty estimation)
| ├── text_simplification (8 notebooks for text simplification)
├── src (Some frequently used functions and classes)
├── figures (The figures generated by the notebooks and used in the article)
├── README.md
├── requirements.txt
├── pyproject.toml
└── poetry.lock
```

Notebooks are intended to be executed in alphabetical order. Notebooks in the **difficulty_estimation** section are to be executed first, then those in the **text_simplification** section.

*Note that executing certain notebooks may cause the following folders to appear:*
```
.
├── data (For data storage)
│ ├── raw
│ ├── processed
├── results (For storing results)
├── scratch (For storing temporary data)
├── .slogs (If using Slurmray)
```

### Difficulty Estimation 🐳

1. `a_Datasets` : This notebook allows you to download the data used to train the models. It also prepares the json files needed to train the **OpenAI** models and provides a cost estimate.
2. `b_OpenAiModelsTraining` : This notebook allows you to train the **OpenAI** models.
3. `c_OpenAiEvaluation` : This generates the results and metrics for the **OpenAI** models.
4. `d_OpenSourceModelsTraining` : This notebook is responsible for training the **CamemBERT** and **Mistral** models.
5. `e_OpenSourceEvaluation` : This generates the results and metrics for the **CamemBERT** and **Mistral** models.
6. `f_PairwiseMismatch` : This notebook trains and evaluates the performance of the **ARI**, **GFI** and **FKGL** Readability Indices. It also introduces the **Pairwise Mismatch** metric and evaluates the performance of all previous models on this metric.
7. `g_CreateFigures` : This notebook generates the figures used in the article.

### Text Simplification 🐬

1. `a_DatasetCreation.ipynb` : This notebook allows you to download the data used to train the models
2. `b_FineTuningMistral.ipynb` : This notebook is responsible for fine-tuning the **Mistral** model
3. `c_MistralEvaluation.ipynb` : This notebook generates the predictions for the **Mistral** model
4. `d_Metrics.ipynb` : This notebook defines and evaluates the metrics used to evaluate the performance of the models
5. `e_OpenAIFineTuning.ipynb` : This notebook is responsible for fine-tuning the **OpenAI** models
6. `f_OpenAIEvaluation.ipynb` : This notebook generates the predictions for the **OpenAI** models
7. `g_IterativeSimplification.ipynb` : This notebook explores the iterative simplification of texts
8. `h_CreateFigures.ipynb` : This notebook generates the figures used in the article