# Alphabet Soup Funding Success Prediction

## Project Overview

This project aims to assist Alphabet Soup, a nonprofit foundation, in identifying the most promising funding applicants. Using machine learning techniques, specifically neural networks, we aim to predict the success of various organizations based on historical data.

## Table of Contents

1. [Usage](#usage)
2. [Data Preprocessing](#data-preprocessing)
3. [Modeling and Optimizations](#modeling-and-optimizations)
4. [Results](#results)

## Usage

The project includes Jupyter Notebooks that walk through data preprocessing, model building, and optimizations. Run these notebooks to understand the modeling approach and to build your own models.

## Data Preprocessing

* **Target Variable**: `IS_SUCCESSFUL`
* **Feature Variables**: Various organization-related attributes.
* **Non-useful Variables**: `EIN` and `NAME` were removed.

### Binning Cutoff Changes Across Optimizations

* **Baseline Model**: Cutoff for `APPLICATION_TYPE` at 500 and `CLASSIFICATION` at 200.
* **Optimization 1**: No change in binning cutoffs.
* **Optimization 2**: `APPLICATION_TYPE` changed to 1000 and `CLASSIFICATION` to 1500.
* **Optimization 3**: No noticeable change in binning cutoffs.

## Modeling and Optimizations

### Baseline Model

* **Function**: `create_model`
* **Hyperparameter Tuning**: KerasTuner used for activation functions and neuron counts.
* **Hidden Layers**: Up to 6 hidden layers allowed.

### Optimization 1

* **Function**: `create_model`
* **Changes**: None; same as the baseline model.

### Optimization 2

* **Function**: `create_model`
* **Changes**: Increased the `min_value`, `max_value`, and `step` values for neurons in hidden layers to range from 5 to 25 with steps of 5.

### Optimization 3

* **Function**: `create_model`
* **Changes**: Increased the `min_value`, `max_value`, and `step` values for neurons in the first layer to range from 10 to 90 with steps of 5. Neurons in hidden layers range from 5 to 30 with steps of 5.

## Results

All models achieved an accuracy rate of around 72-73%, falling short of the desired 75% accuracy.

