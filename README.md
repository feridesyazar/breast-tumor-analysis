# 🎗️ Breast Cancer Classification

This project uses measurements from cell images to classify breast tumor samples as **benign (B)** or **malignant (M)**. We explore the data, train a **Random Forest** classifier, and evaluate its predictions with simple Python code.

> **Educational project only.** The model is not a medical screening or diagnosis tool.

## Dataset

- **Source:** [Breast Cancer Wisconsin (Diagnostic) – Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- **File:** `data.csv`
- **Samples:** 569 (357 benign, 212 malignant)
- **Raw columns:** 33, including the target, sample ID, and one empty column
- **Model features:** 30 numeric measurements
- **Target:** `diagnosis` (`B = 0`, `M = 1`)

The `id` and empty `Unnamed: 32` columns are excluded from the model.

## Project Steps

1. Import libraries and load the CSV file
2. Explore the data and check missing values
3. Visualize class counts, cell measurements, and correlations
4. Prepare the 30 numeric features and encode the target
5. Split the data into 80% training and 20% testing
6. Train a Random Forest classifier
7. Evaluate predictions and visualize feature importance

## Results

Results from the test split (`random_state=42`, `stratify=y`):

| Metric | Result |
|---|---:|
| Accuracy | 0.974 |
| Precision (malignant) | 1.000 |
| Recall (malignant) | 0.929 |
| F1-Score (malignant) | 0.963 |

The test set contains 114 samples. The model correctly predicted 111; **3 malignant samples were classified as benign**. These results are specific to this dataset and split.

## Run Locally

1. Download `data.csv` from the Kaggle source above.
2. Place it in the same folder as `Breast_Cancer_Classification.ipynb`.
3. Install the libraries if needed:

```bash
pip install notebook pandas matplotlib seaborn scikit-learn
```

4. Open the notebook in Jupyter and run the cells in order.

```python
import pandas as pd

df = pd.read_csv('data.csv')
```

## Limitations

The dataset is small and the model is evaluated on only one train/test split. Performance may change on other data. Feature importance does not establish causality. **Do not use this educational model to make medical decisions.**

## Tools

Python · Pandas · Matplotlib · Seaborn · Scikit-learn · Jupyter Notebook

## Data Source

[Breast Cancer Wisconsin (Diagnostic) on Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data). Check the dataset's redistribution terms before uploading the CSV to a public repository.
