# Determining the place for a new oil well

Model to determine the best region for oil drilling based on oil quality and volume metrics. Uses bootstrap technique for risk and profit analysis.

Steps for Selecting Oil Well Locations:

1. In the preferred region, search for oil fields and determine the values of features for each field.
2. Build a model and estimate the volume of oil reserves.
3. Choose the oil fields with the highest estimated values. The number of selected fields depends on the company's budget and the cost of drilling a single well.
4. Profit is equal to the total profit from the selected oil fields.

**Data:**

- `id` — Unique well identifier.
- `f0`, `f1`, `f2` — Three features of the data points.
- `product` — Volume of oil reserves in the well (thousand barrels).


**What's done:**

The following steps were taken:

- Examined the provided data: no data preprocessing was required.

- Trained linear regression models for three regions and compared the results:

| Region      | Mean     | RMSE     |
|:-----------:|:--------:|:-------:|
| geo_data_0  | 92.078597 | 37.579422 |
| geo_data_1  | 68.723136 | 0.889737  |
| geo_data_2  | 94.884233 | 39.958042 |

- Prepared constants and functions for calculating the expected profit.

- Used the Bootstrap technique to select the best region.

- **Final Region: geo_data_1**

  - Average Profit: 501.33 million rubles.
  - 95% Confidence Interval: (100.15, 925.05) million rubles.
  - Risk of Loss: 1.3%

