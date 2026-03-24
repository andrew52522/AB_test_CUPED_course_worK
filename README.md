# A/B Testing and CUPED Framework Simulation

## Description
This project provides a comprehensive simulation environment for evaluating A/B testing methodologies, with a strong focus on variance reduction using the CUPED (Controlled Experiments Using Pre-Experiment Data) framework. The simulation compares ordinary A/B testing against standard CUPED and advanced Multi-CUPED approaches (both Independent and Iterative). The primary goal is to demonstrate how leveraging multiple covariates can significantly reduce metric variance, lower the Type II error rate, and allow for faster experiments without requiring a larger sample size.

## File Overview

* `final_simulation_ab_tests.ipynb`
  This Jupyter Notebook contains the complete simulation code. The workflow is divided into the following key stages:
  
  - **A/A Testing Validation:** Ensures the foundational statistical engine (using Welch's t-test) works correctly across different continuous and discrete data distributions (Normal, Binomial, Exponential). It verifies that the False Positive Rate remains at the expected alpha level.
  - **Error Rate Analysis:** Analyzes how the Type II error (Beta) depends on data noise and sample size.
  - **Covariate Generation:** Simulates realistic experimental data by building custom covariance matrices to generate correlated features.
  - **CUPED Implementations:** Applies and compares four distinct methods: Standard A/B, Standard CUPED, Multi-CUPED (Independent), and Multi-CUPED (Iterative).
  - **Results Evaluation:** Compares the variance reduction efficiency and visualizes the results to prove the superiority of the Multi-CUPED approach in increasing test sensitivity.

## Installation

To run the notebook, you will need to install the necessary Python dependencies. You can install them using pip:

```bash
pip install numpy pandas scipy matplotlib seaborn tqdm
```

## How to Run
Open the final_simulation_ab_tests.ipynb file in your preferred environment (Jupyter Notebook, JupyterLab, or Google Colab).

Run the first cell to load all required libraries and initialize the environment.

Execute the data generation and A/A testing cells to validate the statistical distributions and view the empirical error rates.

Proceed to the CUPED sections. Run the cells to generate the covariance matrices and apply the variance reduction algorithms.

Run the final cells to view the comparative plots and conclusions regarding test sensitivity and the effectiveness of the Multi-CUPED algorithms.
