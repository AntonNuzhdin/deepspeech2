# PyTorch Template for DL projects

<p align="center">
  <a href="#about">About</a> •
  <a href="#examples">Examples</a> •
  <a href="#installation">Installation</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#useful-links">Useful Links</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a>
</p>

## About

This repository contains a template for [PyTorch](https://pytorch.org/)-based Deep Learning projects.

The template utilizes different python-dev techniques to improve code readability. Configuration methods enhance reproducibility and experiments control.

Repository is released as a part of [HSE DLA course](https://github.com/markovka17/dla), however, can easily be adopted for any DL-task.

## Examples

> [!IMPORTANT]
> The main branch leaves some of the code parts empty or fills them with dummy examples, showing just the base structure. The final users can add code required for their own tasks.

You can find examples of this template completed for different tasks in other branches:

- [Image classification](https://github.com/Blinorot/pytorch_project_template/tree/example/image-classification): simple classification problem on [MNIST](https://yann.lecun.com/exdb/mnist/) and [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) datasets.

- [ASR](todo): template for the automatic speech recognition (ASR) task. Some of the parts (for example, `collate_fn`) are missing for studying purposes of [HSE DLA course](https://github.com/markovka17/dla).

## Installation

Installation may depend on your task. The general steps are the following:

0. (Optional) Create and activate new environment using [`conda`](https://conda.io/projects/conda/en/latest/user-guide/getting-started.html) or `venv` ([`+pyenv`](https://github.com/pyenv/pyenv)).

   a. `conda` version:

   ```bash
   # create env
   conda create -n project_env python=PYTHON_VERSION

   # activate env
   conda activate project_env
   ```

   b. `venv` (`+pyenv`) version:

   ```bash
   # create env
   ~/.pyenv/versions/PYTHON_VERSION/bin/python3 -m venv project_env

   # alternatively, using default python version
   python3 -m venv project_env

   # activate env
   source project_env
   ```

1. Install all required packages

   ```bash
   pip install -r requirements.txt
   ```

2. Install `pre-commit`:
   ```bash
   pre-commit install
   ```

## How To Use

To train a model, run the following command:

```bash
python3 train.py -cn=CONFIG_NAME HYDRA_CONFIG_ARGUMENTS
```

Where `CONFIG_NAME` is a config from `src/configs` and `HYDRA_CONFIG_ARGUMENTS` are optional arguments.

To run inference (evaluate the model or save predictions):

```bash
python3 inference.py HYDRA_CONFIG_ARGUMENTS
```

## Useful Links:

You may find the following links useful:

- [Python Dev Tips](https://github.com/ebezzam/python-dev-tips): information about [pre-commits](https://pre-commit.com/), [Hydra](https://hydra.cc/docs/intro/), and other stuff for better python code development.

- [CLAIRE Template](https://github.com/CLAIRE-Labo/python-ml-research-template): additional template by [EPFL CLAIRE Laboratory](https://www.epfl.ch/labs/claire/) that can be combined with ours to enhance experiments reproducibility via [Docker](https://www.docker.com/).

- [Mamba](https://github.com/mamba-org/mamba) and [Poetry](https://python-poetry.org/): alternatives to [Conda](https://conda.io/projects/conda/en/latest/user-guide/getting-started.html) and [pip](https://pip.pypa.io/en/stable/installation/) package managers given above.

- [Awesome README](https://github.com/matiassingers/awesome-readme): a list of awesome README files for inspiration. Check the basics [here](https://github.com/PurpleBooth/a-good-readme-template).

- [Report branch](https://github.com/Blinorot/pytorch_project_template/tree/report): Guidelines for writing a scientific report/paper (with an emphasis on DL projects).

- [Seminar on R&D Coding](https://youtu.be/sEA-Js5ZHxU): Seminar from the [LauzHack Deep Learning Bootcamp](https://github.com/LauzHack/deep-learning-bootcamp/) with template discussion and reasoning.

## Credits

This repository is based on a heavily modified fork of [pytorch-template](https://github.com/victoresque/pytorch-template) and [asr_project_template](https://github.com/WrathOfGrapes/asr_project_template) repositories.

## License

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)
