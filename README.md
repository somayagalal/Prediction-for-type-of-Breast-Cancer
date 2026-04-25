# Breast Cancer Type Prediction

A project that predicts whether a breast tumor is **benign (B)** or **malignant (M)** using diagnostic measurements from a breast cancer dataset.

The project walks through the full data mining workflow: data understanding, preprocessing, outlier handling, exploratory data analysis, feature correlation analysis, model training, evaluation, and model comparison.


---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Repository Structure](#repository-structure)
- [Workflow](#workflow)
- [Models Used](#models-used)
- [Generated Visualizations](#generated-visualizations)
- [Dependencies](#dependencies)
---

## Project Overview

The goal of this project is to build and compare classification models that can predict the tumor diagnosis class:

- **B**: Benign
- **M**: Malignant

The analysis is implemented in `main.ipynb` and uses Python data science libraries to clean the data, visualize important patterns, train multiple models, and compare performance using classification metrics and ROC-AUC scores.

---

## Dataset

The dataset is stored in:

```text
data/raw/breast-cancer.csv
```

Dataset details from the notebook:

- **Rows:** 569
- **Columns:** 32 before preprocessing
- **Target column:** `diagnosis`
- **ID column:** `id`, removed before modeling
- **Missing values:** 0
- **Duplicate rows:** 0
- **Class distribution:**
  - Benign: about 62.74%
  - Malignant: about 37.26%

The feature columns include measurements such as radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, and fractal dimension. Many features are available in mean, standard error, and worst-value forms.

---

## Repository Structure

```text
Prediction-for-type-of-Breast-Cancer/
|
|-- data/
|   |-- raw/
|   |   `-- breast-cancer.csv
|   `-- processed/
|       `-- .gitkeep
|
|-- outputs/
|   |-- plots/
|   |   |-- correlation heatmaps
|   |   |-- confusion matrices
|   |   |-- ROC-AUC curves
|   |   |-- feature importance charts
|   |   `-- exploratory plots
|   `-- tables/
|       `-- .gitkeep
|
|-- main.ipynb
`-- README.md
```

---

## Workflow

The notebook follows these main steps:

1. **Data Understanding**
   - Load the dataset
   - Inspect shape, columns, data types, missing values, duplicates, and target distribution

2. **Data Cleaning and Preprocessing**
   - Drop the `id` column
   - Encode diagnosis values:
     - `M` -> 1
     - `B` -> 0
   - Detect outliers using IQR and Z-score methods
   - Remove rows containing IQR-based outliers
   - Standardize numerical features using Z-score scaling

3. **Exploratory Data Analysis**
   - Feature distributions
   - Boxplots before and after outlier removal
   - Feature spread by diagnosis
   - Scatter plots for feature relationships
   - Pairwise feature analysis

4. **Correlation Analysis**
   - Correlation matrix
   - Correlation heatmap
   - Correlation with the target variable
   - Selection of top correlated features

5. **Model Training and Evaluation**
   - Train multiple classification models
   - Use train/test split
   - Tune selected models with `GridSearchCV`
   - Evaluate using accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC

6. **Model Comparison**
   - Compare all trained models in a final performance summary table
   - Plot ROC curves for model comparison

---

## Models Used

The following machine learning models are trained and evaluated:

- Decision Tree Classifier
- Gaussian Naive Bayes
- Logistic Regression
- Random Forest Classifier
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

Hyperparameter tuning is performed for selected models such as Decision Tree, Random Forest, and SVM using `GridSearchCV`.


---

## Generated Visualizations

The notebook saves plots in:

```text
outputs/plots/
```

Examples of generated visual outputs include:

- Boxplots before and after outlier removal
- Scaling comparison plots
- Feature distribution histograms
- Feature spread by diagnosis
- Scatter plots of feature relationships
- Pairplot of top features
- Correlation heatmap
- Decision tree visualization
- Confusion matrices for multiple models
- ROC-AUC curves for individual models
- Combined ROC-AUC comparison plot
- Feature importance charts

---


---

## How to Run

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open and run:

```text
main.ipynb
```

Run the notebook cells from top to bottom. Make sure your working directory is the project root so the notebook can correctly access:

```text
data/raw/breast-cancer.csv
```

and save generated files into:

```text
outputs/plots/
```

---

## Dependencies

Main libraries used in the project:

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn
- jupyter


