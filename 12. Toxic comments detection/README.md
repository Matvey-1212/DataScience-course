# Toxic comments detection

Building a model to classify and filter out toxic comments from a platform. Aims at maintaining a positive user environment.

**What's done::**

- Models were selected for the task of detecting toxic comments.

- Data Handling:

  - Data was loaded and explored: no missing values or duplicates were found, and the index column was removed.
  - Class imbalance was identified.
  - Frequency analysis of texts was conducted.

- Data Preparation:

  - Data was prepared for training: texts were cleaned, lemmatized, and stripped of stop words. New features were added.

- Model Training:

  - Models were trained: PassiveAggressive, Logistic Regression, Random Forest, LightGBM.
  - Cross-validation was used during training.
  - Data was transformed before each fold: upsampling, TF-IDF, scaling.
  - A pipeline was used to prevent data leakage.

- Best Results:

  - Logistic Regression: F1 - 0.7582301
  - PassiveAggressive: F1 - 0.7505263

- Additionally:

  - PassiveAggressive was trained on BERT embeddings.
  - PassiveAggressiveClassifier on BERT: F1 - 0.8811035

- Best Test Result:

  - PassiveAggressiveClassifier on BERT: F1 - 0.8942
