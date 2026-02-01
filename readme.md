# SCIT: Learning Causal-Consistent Imputation for Multivariate Time Series

## Overview

SCIT (Self-supervised Causality-guided Imputation for Time Series) is a novel framework for imputing missing values in multivariate time series (MTS) data. Traditional imputation methods often fail when the underlying causal relationships among the variables are ignored. SCIT addresses this gap by introducing a causal-guided framework that enforces imputation consistency with the inferred causal graph, ensuring both numerical accuracy and structural integrity.

The SCIT framework consists of two key components:
1. **Similarity-Driven Structural Learning**: Starts with an initial imputation and iteratively refines a global causal graph by clustering similar samples and aggregating their local causal subgraphs.
2. **Structure-Informed Imputation**: Performs imputation based solely on causally relevant features rather than all observed variables.

We evaluate SCIT on several datasets from diverse domains, comparing its performance against 12 competitive baseline models, demonstrating superior or competitive performance across multiple tasks.

## Key Features
- **Causality-guided imputation**: Considers temporal causal relationships for accurate imputation.
- **Self-supervised learning**: Reduces dependency on ground truth labels during training.
- **Scalable framework**: Efficient for large datasets, such as those found in healthcare and finance.

## Appendix
Hyperparameters used in experiments is in Appendix__Hyperparameters.pdf

## Datasets
SCIT is evaluated on five popular datasets from various domains:
1. **Lorenz-96**: Synthetic dataset based on a nonlinear climate model.
2. **Linear VAR**: Synthetic dataset using a linear vector autoregression process.
3. **Finance**: Simulated financial data using the Fama-French Three-Factor Model.
4. **MIMIC-III**: Real-world healthcare dataset containing time-series data from ICU patients.
5. **Beijing Air Quality**: Real-world environmental dataset with hourly pollution measurements.

## Evaluation Metrics
SCIT's performance is assessed using several evaluation tasks:
- **Missingness Imputation**: Evaluated with Mean Squared Error (MSE) and Normalized Root Mean Squared Error (NRMSE).
- **Downstream Prediction**: Indirectly evaluates imputation quality through classification tasks (e.g., mortality, sepsis, acute kidney injury).
- **Causal Graph Recovery**: Evaluates the alignment between the recovered causal structure and ground truth causal graphs.
- **Computational Efficiency**: Assesses the runtime performance on large-scale datasets.

## Installation
To run SCIT, clone this repository and install the dependencies:
```bash
git clone https://github.com/yourusername/SCIT.git

```bash
# Example command
python main.py

