# Breast Cancer Type Prediction

Data Mining project for analyzing breast cancer data and preparing a full pipeline to support classification of tumor diagnosis as:
- B: Benign
- M: Malignant

## Project Overview
This repository contains the Phase 1 workflow:
- Data understanding
- Data cleaning
- Preprocessing
- Outlier analysis
- Visualization
- Insights and findings

The analysis is organized as sequential notebooks so the workflow is easy to follow and reproduce.

## Repository Structure
```text
Prediction-for-type-of-Breast-Cancer/
|-- data/
|   |-- raw/
|   |   `-- breast-cancer.csv
|   `-- processed/
|
|-- outputs/
|   |-- plots/
|   `-- tables/
|-- main.ipynb
`-- README.md
```

## Tools and Libraries
- Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Notebook Workflow
steps:
1. `data_understanding`
2. ` Outlier detection , removal & visualization`
3. ..

## Setup and Run
1. Clone the repository:
```bash
git clone https://github.com/somayagalal/Prediction-for-type-of-Breast-Cancer.git
```

2. Open the project in VS Code or Jupyter.

3. Install required packages in your Python environment.

4. Run the notebooks in order from the previous section.

## Expected Outputs
- Cleaned and prepared dataset versions in `data/processed/`
- Charts and plots in `outputs/plots/`
- Summary tables in `outputs/tables/`
- Final insights from exploratory and preprocessing steps


## Notes
- Keep notebook outputs and generated artifacts organized in the `outputs/` folder.
- Include short explanations in each notebook cell for reproducibility.
