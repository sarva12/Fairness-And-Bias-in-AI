# AI Hiring Fairness Analysis

This project explores different definitions of candidate success and their impact on efficiency and fairness outcomes in an AI hiring model. It uses the UCI Adult Income dataset to demonstrate how varying success definitions and decision thresholds influence model performance and group-based disparities.

## Table of Contents

- [Setup Instructions](#setup-instructions)
- [Dependencies](#dependencies)
- [Dataset](#dataset)
- [Replication Instructions](#replication-instructions)

## Setup Instructions

To run this notebook, you will need a Python environment with the necessary libraries installed. You can set up your environment by executing the following commands in your notebook or terminal:

```bash
!pip install ucimlrepo pandas numpy matplotlib scikit-learn
```

## Dependencies

This project relies on the following Python libraries:

- `ucimlrepo`: For easily fetching the UCI Adult Income dataset.
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib`: For creating static, interactive, and animated visualizations.
- `seaborn`: (Implicitly used for plotting in `run_experiment` function's visualization calls, though not explicitly in the `!pip install` or direct import list in the provided `5tw3VBfO3GJa` cell, it's good practice to include it if plots use it.)
- `scikit-learn`: For machine learning tasks, including model training, preprocessing, and evaluation metrics.

## Dataset

The project utilizes the **Adult Income Dataset** from the UCI Machine Learning Repository. This dataset contains demographic and employment-related information, used to predict whether an individual earns over 50K USD per year. 

**Link to Dataset:** [Adult Data Set - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/2/adult)

## Replication Instructions

To replicate the analysis and results presented in this notebook, follow these steps:

1.  **Open the Notebook:** Ensure you have access to this Jupyter/Colab notebook.
2.  **Install Dependencies:** Run the setup instructions provided in the [Setup Instructions](#setup-instructions) section. This will install all required libraries.
3.  **Execute Cells Sequentially:** Run all code cells in the notebook from top to bottom. The notebook is structured to perform the following steps:
    *   **Data Loading and Initial Cleaning:** Loads the UCI Adult dataset and performs initial cleaning, including handling missing values and converting income labels.
    *   **Defining Alternative Success Metrics:** Creates a 'composite success' score based on work-readiness criteria.
    *   **`detailed_metrics` Function:** Defines a helper function to calculate fairness metrics by group.
    *   **`run_experiment` Function:** Defines the core experiment function, which trains a logistic regression model, applies hiring policies, computes fairness metrics, and generates various plots for a given success definition.
    *   **Running Experiments (A, B, C):** Executes the `run_experiment` function for three different scenarios:
        *   **Experiment A:** Original income >50K success definition.
        *   **Experiment B:** Composite work-readiness success definition.
        *   **Experiment C:** Income >50K without wealth-related features.
    *   **Composite Analysis and Marginalization Visuals:** Combines and normalizes results from all experiments, calculates a composite score across thresholds, and visualizes marginalized groups.

By following these steps, you will generate all the model training results, fairness metric tables, and visualizations presented in this analysis.
