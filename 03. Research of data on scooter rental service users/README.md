# Research of data on scooter rental service users
Analysis of user data from a scooter rental service to test hypotheses for business growth. The study also reviews different tariff plans and service costs.

**Data Used:**

- **users_go.csv**
    - `user_id` - Unique user identifier
    - `name` - User name
    - `age` - Age
    - `city` - City
    - `subscription_type` - Subscription type (`free`, `ultra`)

- **rides_go.csv**
    - `user_id` - Unique user identifier
    - `distance` - Distance traveled by the user in the current session (in meters)
    - `duration` - Session duration (in minutes) - time from when the user pressed the "Start trip" button to when they pressed the "Finish trip" button
    - `date` - Date of the trip

- **subscriptions_go.csv**
    - `subscription_type` - Subscription type
    - `minute_price` - Cost of one minute of travel under this subscription
    - `start_ride_price` - Cost of starting a trip
    - `subscription_fee` - Monthly subscription fee


**The following was done:**

- **Data preprocessing**: type conversion, missing value removal, addition of a column for months, anomaly handling.
- Various parameters were reviewed, and the following conclusions were drawn:
    - The number of users in cities where the service is available is roughly the same. However, in terms of the percentage of the city's population, **Pyatigorsk** ranks first, while **Moscow** ranks last.
    - Users with subscriptions and without subscriptions account for 45.6% and 54.4%, respectively.
    - The average age of users is 25 years. The percentage of users aged 20-30 is 77%.
    - The average trip distance is 3060 meters, but there is a slight increase in the number of trips with a length of 0-1000 meters. The average distance does not change with the season or city.
    - The average trip duration is 18 minutes. The average duration does not change with the season or city.
    - The distributions of trip times and distances for users with and without subscriptions are similar. However, subscription users take significantly fewer trips, accounting for 36% compared to 64% for non-subscription users.
- Additional tables were created to store revenue from users with and without subscriptions.
- Some hypotheses were tested.
- Work with binomial and normal distributions was conducted:
    - To ensure the success of the coupon code promotion, at least 1172 coupon codes need to be sent.
    - The probability that only 399.5 thousand out of 1 million users opened the notifications is 15%.
