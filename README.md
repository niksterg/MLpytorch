# MLpytorch

PyTorch tutorials for introducing Machine Learning with Pytorch.

The first notebook uses a physics-first example: calibrating a spring force
sensor from noisy measurements. Students connect Hooke's law, least squares,
gradient descent, feature scaling, mini-batch training, scikit-learn
preprocessing, and PyTorch's `nn.Linear` API.

## Contents

- `01_linear_regression_pytorch.ipynb` - a one-hour notebook on linear
  regression with PyTorch.
- `environment.yml` - optional Conda environment for running the notebook.

## Notebook Topics

- Creating noisy experimental data with tensors
- Fitting a linear model, `y_hat = wx + b`
- Mean squared error and residuals
- Classical least squares with `torch.linalg.lstsq`
- Manual gradient descent with autograd
- Feature scaling and converting parameters back to physical units
- Static and interactive plots of the loss landscape
- Mini-batch training from scratch
- Standardizing features with scikit-learn
- The concise PyTorch implementation with:
  - `TensorDataset`
  - `DataLoader`
  - `nn.Linear`
  - `nn.MSELoss`
  - `torch.optim.SGD`
- Extending from one input feature to multiple input features

## Requirements

The notebook is intentionally lightweight.

Use Python 3.11 or newer.

You can install the dependencies with pip:

```bash
pip install torch "numpy<2" matplotlib plotly scikit-learn jupyter
```

Or create the provided Conda environment:

```bash
conda env create -f environment.yml
conda activate mlpytorch
```

When the notebook is run on Google Colab or Kaggle, it can automatically check
for missing pip packages and install only the ones that are not already present.
Local Jupyter runs skip automatic package installation.

## Usage

Start Jupyter from the repository root:

```bash
jupyter notebook
```

Then open:

```text
01_linear_regression_pytorch.ipynb
```

You can also run it with JupyterLab:

```bash
jupyter lab
```

## Suggested Lesson Flow

The notebook is designed for roughly one hour:

1. Data and model setup: 10 minutes
2. Loss function and least squares: 15 minutes
3. Gradient descent: 20 minutes
4. PyTorch implementation: 15 minutes

## Exercises

The notebook includes short exercises asking students to experiment with:

- measurement noise,
- learning rates,
- units and scaling,
- mini-batch sizes,
- extra input features.

These exercises are meant to make the numerical behavior visible, not just to
produce a final fitted line.
