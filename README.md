# Datheon Machine Learning & Data Science Internship

A collection of end-to-end machine learning notebooks completed during the Datheon ML/Data Science internship. Each notebook covers a full pipeline: data loading, exploratory data analysis (EDA), cleaning, feature engineering/encoding, model training, evaluation, and interpretation.

## Repository structure

```
Datheon_Machine_Learning_-_Data_Science_Internship/
├── Iris_classification_pipeline.ipynb          # Task 1 - Iris species classification
├── California_Housing_Pipeline.ipynb           # Task 2 - California housing regression
├── Telco_Churn_Pipeline.ipynb                  # Task 3 - Customer churn classification
├── Sentiment_Reviews_Pipeline.ipynb            # Task 4 - NLP sentiment classification
├── sentiment_reviews.csv                        # Labelled starter data for Task 4
├── requirements.txt                             # Python dependencies
└── README.md
```

The other datasets (`iris.csv`, `housing.csv`, `churn.csv`) are downloaded automatically by their notebooks, so they are not committed.

## Notebooks

| # | Notebook | Problem | Models |
|---|----------|---------|--------|
| 1 | `Iris_classification_pipeline.ipynb` | Classify iris species from flower measurements | Logistic Regression, Decision Tree |
| 2 | `California_Housing_Pipeline.ipynb` | Predict median house value from census features | Linear Regression, Decision Tree |
| 3 | `Telco_Churn_Pipeline.ipynb` | Predict customer churn from account/service data | Logistic Regression, Decision Tree |
| 4 | `Sentiment_Reviews_Pipeline.ipynb` | Classify customer review polarity | Multinomial Naive Bayes, Logistic Regression |

Each notebook includes evaluation metrics, visual diagnostics (confusion matrices, prediction/residual plots), feature importance, and cross-validation where applicable. Task 4 also exposes a reusable `predict_sentiment()` function and an interactive test helper.

## Running the notebooks

### Google Colab
Open any notebook in Colab using the badge at the top, then run all cells (`Runtime -> Run all`). Datasets are downloaded or read from this repository automatically.

### Local
```bash
git clone git@github.com:oumaklaus/Datheon_Machine_Learning_-_Data_Science_Internship.git
cd Datheon_Machine_Learning_-_Data_Science_Internship
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Run `Sentiment_Reviews_Pipeline.ipynb` from the repository root so it can read `sentiment_reviews.csv`; the other notebooks download their data on the first run.

## Notes

- Task 4 uses the provided 10-review starter set (5 positive, 4 negative, 1 neutral). The pipeline is complete, but metrics on such a small sample are only a smoke test; the same code scales to a larger labelled review dataset unchanged.
- All notebooks are self-contained and reproducible with `RANDOM_STATE = 42`.
