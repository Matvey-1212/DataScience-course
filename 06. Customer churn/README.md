# Customer churn

Predicting if a bank's customers will leave in the near future based on historical behavioral data. The focus is on maximizing the F1-score and comparing it with the AUC-ROC value.

**Data:**

- `RowNumber` - Index of the row in the dataset
- `CustomerId` - User ID
- `Surname` - Surname
- `CreditScore` - Credit score
- `Geography` - Country of residence
- `Gender` - Gender
- `Age` - Age
- `Tenure` - How long the person has been a bank customer
- `Balance` - Account balance
- `NumOfProducts` - Number of bank products used by the user
- `HasCrCard` - Presence of a credit card
- `isActiveMember` - Customer's activity
- `EstimatedSalary` - Estimated salary
- `Exited` - Customer churn status (1 - left, 0 - retained)

**What's done::**

- Data preprocessing (removing unnecessary columns and handling missing values).

- Studied mutual correlation among columns.

- Prepared data for model training (splitting and one-hot encoding).

- Trained models without class imbalance (Logistic Regression, Decision Tree, Random Forest, CatBoost). The best result was achieved by CatBoost.

- Studied class imbalance and trained all models on different datasets:
    - Using upsampling.
    - Using downsampling.
    - Considering class weights.
- Random Forest with class weights achieved the best F1 score.

- Evaluated the final model on the test dataset.
