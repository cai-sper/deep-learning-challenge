# Alphabet Soup Funding Success Prediction: Neural Network Model Analysis

## Overview

The goal of this project is to assist Alphabet Soup, a nonprofit foundation, in identifying the most promising funding applicants. Using machine learning techniques, specifically neural networks, we aim to predict the success of various organizations based on historical data.

## Data Preprocessing

### Target and Features

* **Target Variable**: `IS_SUCCESSFUL`
* **Feature Variables**: `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, `ASK_AMT`
* **Non-useful Variables**: `EIN` and `NAME` were removed.

### Binning Cutoff Changes Across Optimizations

* **Baseline Model**: The cutoff for `APPLICATION_TYPE` was set at 500 and for `CLASSIFICATION` at 200.
* **Optimization 1**: No change in binning cutoffs.
* **Optimization 2**: Modified cutoffs; `APPLICATION_TYPE` changed to 1000 and `CLASSIFICATION` changed to 1500.
* **Optimization 3**: No noticeable change in binning cutoffs.

## Models and Optimizations

### Baseline Model

* **Architecture**: Neural network with hyperparameter optimization.
* **Training**: Data scaled using StandardScaler.
* **Evaluation**: Loss of 0.5513 and accuracy of 72.59%.

### Optimization 1

* **Data Preprocessing**: Consistent with the baseline.
* **Architecture**: Similar to baseline with hyperparameter optimization.
* **Training**: Data scaled using StandardScaler.
* **Evaluation**: Loss of 0.5564 and accuracy of 72.70%.

### Optimization 2

* **Data Preprocessing**: Modified cutoffs for binning.
* **Architecture**: Expanded neuron count.
* **Training**: Data scaled using StandardScaler.
* **Evaluation**: Loss of 0.5598 and accuracy of 72.72%.

### Optimization 3

* **Data Preprocessing**: Consistent with the baseline.
* **Architecture**: Similar to the previous optimizations.
* **Training**: Data scaled using StandardScaler.
* **Evaluation**: Loss of 0.5599 and accuracy of 72.61%.

## Summary

Despite numerous attempts to optimize the neural network model, the desired accuracy of 75% was not achieved. Even after adjustments to binning cutoffs and model tuning, the models hovered around an accuracy of 72-73%.

## Recommendations

1. **Feature Engineering**: Experiment with different feature sets to possibly improve the model.
2. **Other Algorithms**: Consider using other machine learning algorithms like Random Forest or SVM for better performance.
3. **Advanced Techniques**: Using ensemble methods or more advanced algorithms might provide the needed boost in model performance.
