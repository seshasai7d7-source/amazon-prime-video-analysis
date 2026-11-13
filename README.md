# Amazon Prime Video: TV Shows and Movies Analysis

## Project Overview

This project explores movies and TV shows available on Amazon Prime Video using Exploratory Data Analysis (EDA), statistical hypothesis testing, and Machine Learning.

The main objective is to understand content characteristics, investigate rating patterns, and build a classification model to predict whether a title has an IMDb rating of 7 or higher.

## Project Structure

```text
amazon-prime-video-analysis/
|
|-- Datasets/
|   |-- titles.csv
|   |-- credits.csv
|
|-- Models/
|   |-- amazon_prime_high_rating_model.joblib
|
|-- Notebooks/
|   |-- Amazon_Prime_EDA_Colab.ipynb
|   |-- Amazon_Prime_ML_Colab.ipynb
|
|-- Submission/
|   |-- Project_Report.pdf
|
|-- README.md
|-- .gitignore
```

## Technologies Used

- Python
- Google Colab
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- SciPy
- Joblib

## Dataset Description

The project uses two datasets provided by the project coordinator:

- `titles.csv`: Contains information about movies and TV shows.
- `credits.csv`: Contains cast and crew information.

The datasets are combined for analysis and feature engineering.

## Project Workflow

1. Data loading and inspection.
2. Data cleaning and preprocessing.
3. Exploratory Data Analysis.
4. Statistical hypothesis testing.
5. Feature engineering.
6. Machine Learning model development.
7. Model comparison and hyperparameter tuning.
8. Model evaluation and feature importance analysis.
9. Saving the selected model.

## Statistical Analysis

The project investigates three statistical hypotheses:

- Welch's independent t-test to compare IMDb ratings between movies and TV shows.
- Spearman correlation to examine the relationship between IMDb and TMDb scores.
- Mann-Whitney U test to compare IMDb rating distributions across TMDb popularity groups.

The analyses found statistically significant differences or associations in all three tests.

## Machine Learning

**Prediction target:** High IMDb rating (`IMDb score >= 7`).

Three classification algorithms were evaluated:

- Random Forest
- Extra Trees
- Logistic Regression

Random Forest was selected as the final baseline model based on its test performance.

### Model Performance

| Metric | Result |
|---|---:|
| Accuracy | 83.05% |
| Precision (high-rated class) | 62.77% |
| Recall (high-rated class) | 78.18% |
| F1-score (high-rated class) | 69.64% |
| ROC-AUC | 0.8976 |

The selected model was saved as:

`Models/amazon_prime_high_rating_model.joblib`

## How to Run the Project

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `Amazon_Prime_EDA_Colab.ipynb` from the `Notebooks` folder.
3. Upload the required CSV datasets when prompted and execute the notebook cells.
4. Repeat the process with `Amazon_Prime_ML_Colab.ipynb`.
5. Follow the dataset-loading instructions included in each notebook.

To load the saved model in Python:

```python
import joblib

model = joblib.load("Models/amazon_prime_high_rating_model.joblib")
```

Use the same feature preprocessing and input structure expected by the saved pipeline.

## Limitations

- The model uses features such as TMDb scores and popularity.
- These features may not be available before a title receives audience ratings.
- Therefore, the model is not necessarily suitable for pre-release rating prediction.
- Statistical associations and feature importance do not establish causation.
- Predictions should be interpreted as analytical estimates, not guaranteed outcomes.

## Future Improvements

- Explore additional content and audience features.
- Investigate prediction approaches that do not depend on post-release rating information.
- Evaluate model performance on newer or independent datasets.
- Improve model deployment and prediction accessibility.

## Project Documentation

Refer to `Submission/Project_Report.pdf` for the project report and to the two Jupyter notebooks for implementation details and results.

## Acknowledgements

The datasets were provided by the project coordinator for this project.

---

**Project:** Amazon Prime Video TV Shows and Movies Analysis  
**Focus:** Data Analytics and Machine Learning

