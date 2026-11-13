# Multi-Layer Perceptrons Workshop

Jasper Lim
9117038

## Overview

This workshop explores multi-layer perceptrons (MLPs), including activation
functions, forward propagation, backpropagation, and gradient-based learning.
The notebooks use NumPy and popular deep-learning frameworks to connect the
underlying mathematics with practical MNIST classification.

## Setup

1. Create and activate a virtual environment from the repository root:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

2. Install the dependencies:

   ```powershell
   python -m pip install --upgrade pip
   python -m pip install -r requirements.txt
   ```

   The PyTorch packages are required to run the PyTorch comparison in
   `lab.ipynb`. If PowerShell blocks script activation, run the notebook
   commands with the virtual environment's interpreter directly.

## How to Run

Start Jupyter from the repository root:

```powershell
jupyter lab
```

Open either notebook in the Jupyter interface:

- `MultiLayerPerceptrons_Workshop.ipynb` contains the guided workshop material
  and the completed Challenge 1 discussion.
- `lab.ipynb` contains the runnable Challenge 1 framework comparison.

Run the cells from top to bottom. The MNIST dataset is downloaded by Keras on
the first run and cached locally. The benchmark reports training time and test
accuracy for each implementation; timing results depend on the machine and
runtime configuration.

## Challenge Implementation Summary

### Challenge 1: Framework comparison

`lab.ipynb` trains comparable two-hidden-layer MNIST classifiers using:

- **Keras**, using `Sequential`, `fit`, and built-in evaluation.
- **PyTorch**, using an explicit model, loss, optimizer, and batch loop.
- **TensorFlow Core**, using `GradientTape` and a custom training step.

The notebook uses the same normalized MNIST inputs, comparable layer sizes,
optimizer settings, and epoch count for each framework. It generates a table
of training time and test accuracy, identifies the fastest and most accurate
run, and includes a short recommendation. The workshop notebook provides the
corresponding pros-and-cons comparison.

### Challenge 2: Forward and backpropagation

The workshop notebook defines the requirements for implementing a three-layer
network from scratch with NumPy, including activation experiments, gradient
updates, loss visualization, and reflection on initialization and gradient
stability.

## Learning Objectives

- Understand information flow through hidden layers.
- Implement forward propagation and compute predictions.
- Apply backpropagation and gradient descent to update parameters.
- Compare framework abstractions with explicit training loops.
- Analyze activation functions and vanishing or exploding gradients.
