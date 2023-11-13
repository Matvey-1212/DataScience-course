# Determining the cost of cars

Developing a model to determine the market value of used cars based on various technical specifications and features.

Priorities:

- Prediction quality.
- Prediction speed.
- Training time.

**Data:**
- DateCrawled: Date of the ad being crawled from the database.
- VehicleType: Type of the vehicle body.
- RegistrationYear: Year of registration of the vehicle.
- Gearbox: Type of gearbox.
- Power: Engine power in horsepower (hp).
- Model: Vehicle model.
- Kilometer: Mileage in kilometers (km).
- RegistrationMonth: Month of vehicle registration.
- FuelType: Type of fuel.
- Brand: Vehicle brand.
- Repaired: Whether the car has been repaired or not.
- DateCreated: Date of ad creation.
- NumberOfPictures: Number of pictures of the vehicle.
- PostalCode: Postal code of the ad owner (user).
- LastSeen: Date of the user's last activity.
- Price: Price of the vehicle in euros (€).



**What's done:**

- Data preprocessing was carried out:
    - Removal of duplicates.
    - Identification and removal of outliers and anomalies.
    - Detection and removal of uninformative columns.
    - Replacing missing values with placeholders in categorical data.

- Model selection and hyperparameter tuning were performed:
    - LightGBM
    - CatBoost
    - Linear Regression

- Comparison was made with a constant model.

The best result was achieved by the **LightGBM** model.
