
# Machine Learning Midterm Project

## Project Overview

This project compares classification and clustering methods using two datasets from scikit-learn:

- Breast Cancer Wisconsin Dataset
- Wine Dataset

The main goal is to study model performance, feature scaling, parameter selection, and clustering quality.

## Datasets

**Breast Cancer**
- 569 samples
- 30 numerical features
- 2 classes: malignant and benign

**Wine**
- 178 samples
- 13 numerical features
- 3 classes

## Methods

Classification algorithms:
- Decision Tree
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes

Clustering algorithm:
- K-Means

We tested scaled and unscaled features using three random seeds: 42, 52, and 62.

We used training and validation results to select the best classifiers. The final test sets were kept separate during model selection.

## Main Results

| Dataset | Selected Classifier | Test Accuracy |
|---|---|---|
| Breast Cancer | Scaled KNN (k=7) | 0.9737 |
| Wine | Scaled KNN (k=11) | 1.0000 |

Feature scaling improved KNN performance, especially for the Wine dataset.

## Project Files

- `breast_cancer.ipynb`: Breast Cancer analysis
- `wine.ipynb`: Wine analysis
- `comparison.ipynb`: Comparison of both datasets
- `results/`: Classification and K-Means CSV results
- `figures/`: Generated plots
- `report.docx`: Project report
- `requirements.txt`: Required Python packages
- `AI_DISCLOSURE.md`: AI assistance disclosure

## How to Run

1. Open the project folder in VS Code.
2. Create and activate a Python virtual environment.
3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Open `breast_cancer.ipynb` and `wine.ipynb`.
5. Select the Python environment as the notebook kernel.
6. Run the notebook cells in order.
7. Open `comparison.ipynb` after the two main notebooks have generated their results.

## Evaluation

The classification models were compared using macro-F1, accuracy, and other classification metrics.

K-Means clustering was evaluated using Adjusted Rand Index (ARI), silhouette scores, and class-cluster contingency tables.

## Notes

The final test results were evaluated using the selected models with random seed 42.
