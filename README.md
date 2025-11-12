# Chastain_appliedML_midterm

## Introduction:

The following contains instructions on setting up a project to perform model testing.

Author: Megan Chastain
Notebook: http://localhost:8888/notebooks/HeartDisease_Chastain.ipynb



## 1. Set Up Project

After creating a repository, run the following to ensure all dependencies are working


```shell
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version
```
Activate the virtual environment

**Windows (PowerShell):**

```shell
.\.venv\Scripts\activate
```


---

## 2. Daily Workflow

At the start of each working session pull any changes from the reposiory


```shell
git pull
```


1. Use `git add .` to stage all changes.
2. Use 'git commit -m 'message' to commit changes
3. Use pit push -u origin main to put changes on the repository

 
### 3. Open notebooks

Run 'jupyter notebooks' in a terminal 

Start the project with a title and introduction

Import programs at the top of the project

### 4. Import and Inspect the Data

Load the dataset and display the first 10 rows.

Check for missing values and display summary statistics.

### 5. Data Exploration and Preparation
Explore data patterns and distributions

Create histograms, boxplots, and count plots for categorical variables (as applicable).

Identify patterns, outliers, and anomalies in feature distributions.

Check for class imbalance in the target variable (as applicable).

Handle missing values and clean data

Impute or drop missing values (as applicable).

Remove or transform outliers (as applicable).

Convert categorical data to numerical format using encoding (as applicable).

Feature selection and engineering

Create new features (as applicable).

Transform or combine existing features to improve model performance (as applicable).

Scale or normalize data (as applicable).

### 6. Feature Selection and Justification
Choose features and target

Select two or more input features (numerical for regression, numerical and/or categorical for classification)

Select a target variable (as applicable)
Regression: Continuous target variable (e.g., price, temperature).
Classification: Categorical target variable (e.g., gender, species).
Clustering: No target variable.

Justify your selection with reasoning.

Define X and y
Assign input features to X
Assign target variable to y (as applicable)

### 7. Train a Model (Classification: Choose 1: Decision Tree, Random Forest, Logistic Regression)
Split the data into training and test sets using train_test_split (or StratifiedShuffleSplit if class imbalance is an issue).

Train model using Scikit-Learn model.fit() method.

Evalulate performance, for example:
Regression: R^2, MAE, RMSE (RMSE has been recently updated)
Classification: Accuracy, Precision, Recall, F1-score, Confusion Matrix
Clustering: Inertia, Silhouette Score

### 8. Improve the Model or Try Alternates (Implement a Second Option)
Train an alternative classifier (e.g., Decision Tree, Random Forest, Logistic Regression) OR adjust hyperparameters on the original model.

Compare performance of all models across the same performance metrics.

### 9. Final Thoughts & Insights
For my project I found that a logistical regression model works decently well at predicting heart disease. The future of healthcare can be improved with the use of model based early detection systems. Even though there may be false positives, it's better to include too many than miss one.
