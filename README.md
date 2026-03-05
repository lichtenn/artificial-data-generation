# ML Method Assumptions & Behaviour — Synthetic Dataset Study

This work was part of the Machine Learning class at FCUP Porto.

An investigation into the assumptions and characteristics of classical 
machine learning methods through purpose-built synthetic datasets. 
Rather than applying models to a fixed real-world dataset, this project 
works in reverse: datasets are designed to isolate the conditions under 
which each method excels or fails.

## Project overview

### Part 1 — Method assumptions
For each of the following methods, a synthetic 2D dataset is 
constructed where that method's assumptions are met and the assumptions 
of the others are violated — i.e. a dataset where that method is 
difficult to beat:

| Method | Key assumption illustrated |
|--------|---------------------------|
| Logistic Regression | Linearly separable classes |
| LDA | Equal covariance, Gaussian classes |
| QDA | Gaussian classes, unequal covariance |
| Decision Tree (unpruned) | Complex, irregular decision boundary |
| Decision Tree (max depth 2) | Simple, low-complexity boundary |
| SVM Linear | Linear separability, large margin |
| SVM RBF | Non-linear boundary, radial structure |

Datasets are visualised with decision boundaries (if possible) and accompanied by 
an explanation of why it suits the respective method.

### Part 2 — Bias-variance tradeoff & model capacity
- Synthetic datasets with varying levels of noise are used to study 
  how the optimal pruning level (ccp_alpha) shifts as data complexity 
  changes
- Bias and variance are decomposed across three dataset versions along 
  the ccp_alpha axis
- Results are interpreted in terms of model capacity, underfitting, 
  and overfitting

### Part 3 — Ensemble methods
Using the tree dataset from Part 2, three ensemble methods are 
compared:
- **Bagging**
- **Random Forest**
- **AdaBoost** (and additional boosting variants)

Comparison includes:
- Learning curves along number of trees using Out-of-Bag (OOB) error
- Final model performance via cross-validation
- Discussion of results in terms of variance reduction and ensemble 
  diversity

## Repository structure

| File | Contents |
|------|----------|
| `Assignment 1 - CC4051 Machine Learning.ipynb` | Notebook including explanations and analysis (ipynb) |
| `Assignment 1 - CC4051 Machine Learning.pdf` | NNotebook including explanations and analysis (pdf) |
| `credit_data.csv` | Real dataset for comparison |
| `titanic.csv` | Real dataset for comparison |

## Key concepts covered
Decision Boundaries · Linear vs. Non-linear Separability · 
Bias-Variance Tradeoff · Model Capacity · Tree Pruning · 
Out-of-Bag Error · Ensemble Learning · Cross-Validation
