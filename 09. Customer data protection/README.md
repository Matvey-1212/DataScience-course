# Customer data protection

Designing a method to protect personal data by transforming them in such a way that the quality of machine learning models remains unchanged.

**Data:**

- Features:
  - Gender: Gender of the insured individual.
  - Age: Age of the insured individual.
  - Salary: Salary of the insured individual.
  - Family Members: Number of family members of the insured individual.
  
- Target Variable:
  - Insurance Claims: Number of insurance claims made by the client in the last 5 years.
 
**What's done:**

- Selected a method for protecting user data.

- Data Loading and Exploration:

  - Loaded and examined the data: No missing values or anomalies found.
  - Removed 153 duplicates.
  - Renamed columns.

- Analysis:

  - Answered the question: "Does multiplying the feature matrix by a reversible matrix affect the model's quality?" - It does not affect the quality.

- Proposed Data Protection Method:

  - The data protection method involves multiplying the feature matrix by a randomly generated reversible matrix.

$$B = XP $$

  - Used linear regression to minimize the Mean Squared Error (MSE) with the modified feature matrix.

$$w_1 = \arg\min_{w_1} MSE(Bw_1, y)$$

Where:

  $X$ — Feature matrix (with a column of ones as the zeroth column).
  
  $y$ — Target feature vector.

  $P$ — Matrix used for feature multiplication.
  
  $w$ — Linear regression weights vector (with the zeroth element as the bias).

- Model Validation:

  - Checked the performance of the linear regression model on both the original and modified data: The result remained unchanged.


