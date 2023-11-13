# Tariff recommendation

Building a classification system to analyze user behavior and suggest the most appropriate mobile tariff plan.

**Data:**

- `сalls` — Number of calls
- `minutes` — Total call duration in minutes
- `messages` — Number of SMS messages
- `mb_used` — Used internet traffic in megabytes (MB)
- `is_ultra` — Tariff used during the month ("Ultra" — 1, "Smart" — 0)

**What's done:**

- Data loading and dataset analysis.
- Splitting the dataset into training, validation, and test sets, and standardization.
- Model selection and hyperparameter tuning:
    - The following models were considered with metrics on the test set:
        - Random Forest - 0.7950310559006211
        - Logistic Regression - 0.7453416149068323
        - Decision Tree - 0.7598343685300207
        - Boosting - 0.7867494824016563
    - The best result was achieved by the Random Forest `forest_model`:
        - Accuracy on train: 0.8501556247220987
        - Accuracy on valid: 0.8132780082987552
        - f1 on valid: 0.6120689655172413
        - roc_auc on valid: 0.720601076251396
- Model adequacy assessment.
