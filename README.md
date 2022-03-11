# Mitiq QV

Companion repository for the paper TODO: paper link.

## Overview

There are two notebooks and a `data/` directory.

- `main.ipynb`: Run unmitigated and mitigated quantum volume experiments.
- `plot.ipynb`: Plot the results from `main.ipynb` or the data directory.

## Requirements

Each notebook has the necessary library installs. In general, `pip install mitiq qiskit qiskit-experiments` should satisfy all requirements.

An IBMQ account is needed to run on backends - see https://quantum-computing.ibm.com/. There is a place to add your credentials in the `main.ipynb` notebook. If you do not have credentials, you can run the experiments on a noisy simulator (default in the `main.ipynb` notebook).

## Notebooks

### `main.ipynb`

This notebook creates quantum volume circuits, runs them on a backend, and counts the heavy bitstrings for the unmitigated experiment. It also scales circuits, runs them on a backend, and does the extrapolation for the mitigated experiment. The unmitigated and mitigated counts are the main outputs of this notebook to be used by `plot.ipynb`. There is an option to save them at the end of the notebook.

The other main parameters of this notebook are the backend, qubits to use, number of trials, number of shots, and scale factors. These can all be set in the appropriate cell. The default values are the ones that were used for the paper results.

### `plot.ipynb`

This notebook reads in data (saved by `main.ipynb`), computes the mean and standard deviation with two methods, and plots the results. Note that `main.ipynb` only saves the unmitigated and mitigated counts, but this notebook expects files for qubits, number of trials, etc.

## Data

This directory contains the data from the paper. Each subdirectory corresponds to data from a particular computer. Use the `plot.ipynb` notebook to read it, process the results, and make the plots shown in the paper. The main parameter is the directory to load data in at the top of the notebook.

## Questions or comments

Please reach out to the paper's corresponding author or open issues on this GitHub.

