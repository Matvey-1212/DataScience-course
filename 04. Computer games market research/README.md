# Computer games market research

Analyzing historical sales data from various platforms to provide insights into trends and forecasting future sales.

**data:**

- Name — Game title
- Platform — Platform
- Year_of_Release — Year of release
- Genre — Game genre
- NA_sales — Sales in North America (millions of copies sold)
- EU_sales — Sales in Europe (millions of copies sold)
- JP_sales — Sales in Japan (millions of copies sold)
- Other_sales — Sales in other countries (millions of copies sold)
- Critic_Score — Critic score (maximum 100)
- User_Score — User score (maximum 10)
- Rating — Rating by the ESRB (Entertainment Software Rating Board). This association determines the rating of computer games and assigns them an appropriate age category.


**What's done:**

- Data preprocessing: Data types were converted, missing values were removed, a column for total sales was added, and anomalies in `user_score` and `rating` were handled.

- Exploratory data analysis yielded the following insights:
    - Since 2012, there has been a decline in the annual release of new games. The period from 2012 to 2016 is considered relevant and was used for analysis in this work.
    - On average, platforms remain popular for 9-11 years.
    - The most popular platforms of all time are 'DS', 'PS', 'PS2', 'PS3', 'Wii', 'X360'.
    - By 2016, the popularity of these platforms is declining, but the popularity of platforms like PS4 and XOne is increasing. They can be considered potentially profitable.
    - The most popular games of all time were released on the PS3, X360, PS4, and 3DS platforms.
    - User and critic scores have little impact on game sales.
    - The most popular genres are `Shooter`, `Platform`, `Sports`, while the least popular are `Adventure`, `Puzzle`, and `Strategy`.

- Sales distributions for platforms and genres were compared within each region:
    - The NA and EU regions are similar in terms of platform and genre popularity, while JP differs, likely due to cultural differences and game and platform production for the domestic market.
    - In NA, games with an M rating (for mature audiences) are the most popular. It can also be said that games with a specific rating are more popular than others. In the JP region, it is difficult to determine a predominance of a specific rating, as a large number of games are not marked with a rating.

- Some hypotheses were tested, and the following conclusions were drawn:
    - It cannot be claimed that the average user scores for the Xbox One and PC platforms are unequal.
    - It can be stated that the average user scores for the Action and Sports genres are unequal.
