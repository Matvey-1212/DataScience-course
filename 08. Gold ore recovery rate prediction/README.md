#  Gold ore recovery rate prediction

Creating a model to predict the gold recovery rate from gold-bearing ore using production data. Aims at optimizing the production process.

**What's done:**

- Performed Actions:

  - Trained models to predict the efficiency of gold recovery from ore.

- Data Loading and Exploration:

  - Loaded and examined the data:
      - The data consists of three datasets (training, test sets, and full dataset).
      - There were missing values in the data.
      - The test set lacks some features that were present in the training data.

- Data Preprocessing:

  - Filled 1.5% of the missing values using neighboring values, as similar adjacent values were observed (interpolation was done considering time intervals).
  - Removed the remaining missing values.
  - Removed anomalies near zero in the 'air' features.

- Data Analysis:

  - Examined how the metal contents change at different stages.
  - Studied the particle sizes in the test and training datasets.
  - Investigated the total metal concentration at different stages.

- Model Selection:

  - Predicted two features as per the task requirements: `rougher.output.recovery` and `final.output.recovery`.
  - Best model for the first feature (`rougher.output.recovery`) - CatBoost:

    | Metric  | Value  |
    |:----------:|:----------:|
    | RMSE  | 4.7970  | 
    | MAE | 3.4131  | 
    | R2  | 0.4792 | 
    | **sMAPE**  | **4.0957**  |

  - Best model for the second feature (`final.output.recovery`) - CatBoost:

    | Metric  | Value  |
    |:----------:|:----------:|
    | RMSE  | 7.4923  | 
    | MAE | 5.1753  | 
    | R2  | 0.2070  | 
    | **sMAPE**  | **7.9257**  |

- Final Metric:

  - Final sMAPE: **6.97**
