# From Script to Screen: Data-Backed Decisions for a Profitable Film Studio
![filmmaking_process](https://github.com/user-attachments/assets/3506d8a1-a4e0-462d-811d-e77e47e4f778)
## Project Overview
This project focuses on analyzing movies data from Rotten Tomatoes,IMDB and The Number DB dentify the types of films that are most successful, using insights from genres, budgets, ratings, and revenue data. These findings will guide decisions on what types of films to create, ensuring a profitable and competitive entry into the film industry.

## Business Problem
Your company now sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of your company's new movie studio can use to help decide what type of films to create.

### Key Business Questions:
1.Which genres and themes consistently lead to high box office performance?

2.How do production budgets influence profitability and ROI?

3.What impact do ratings and audience engagement have on revenue and success?

4.How does the balance between domestic and international revenue vary across genres and film types?

5.What are the most profitable times of the year to release films?

Our ultimate goal is to ensure that the company  is able to make informed, risk-averse and profitable choices when expanding into this industry.

# Data
You can find the data used for this analysis in our data folder:https://github.com/Day-hue/phase-2-project/tree/main/Data

### Data Description:
####  IMDb: Movie Basics
This table provides foundational information about movies, critical for understanding trends in genres, runtime, and release years.
*Columns:*

**movie_id:** Unique identifier for each movie (joins with movie_ratings).

**primary_title:** Official title of the movie (used for identification in analysis).

**original_title:** Native language title, useful for analyzing the influence of language on commercial success.

**start_year:** Year of release, enabling exploration of time-based trends (e.g., genre popularity, seasonal releases).

**runtime_minutes:** Movie length, used to determine if runtime influences audience engagement and box office performance.

**genres:** Genres of the movie, critical for identifying commercially successful themes and trends.

####  IMDb: Movie Ratings

This table offers insights into audience reception and engagement metrics, which are critical for understanding the role of ratings and votes in a movie's financial performance.
*Columns:*

**movie_id:** Unique identifier for each movie (joins with movie_basics).

**averagerating:** Average IMDb rating, useful for gauging critical acclaim and audience satisfaction.

**numvotes:** Number of votes received, indicating audience engagement and popularity.


####  The Numbers: Budget Data

This table provides production budget details and global revenue, essential for ROI and profitability analysis.
*Columns:*

**movie:** Name of the movie.

**production_budget:** Cost of production, enabling the evaluation of budget-performance relationships.

**domestic_gross:** Domestic revenue.

**worldwide_gross:** Total revenue globally.

#### . TMDb: Additional Metadata

This dataset supplements IMDb data with information about popularity and audience ratings.
*Columns:*

**original_language:** Language of the film, supporting analysis of language preferences.

**genre_ids:** Genre categorization (used alongside IMDb genres).

**vote_average and vote_count:** Audience ratings and engagement metrics.

**release_date:** Exact release date, supporting seasonal and trend analysis.
These multiple dataset will enable us to do our analysis with no problems

we'd then combine the dataset to one
# Results
## Top 10 Genres by Total Gross and Average ROI

![Genre vs ROI](https://github.com/Day-hue/phase-2-project/blob/main/Charts/genrevsGrossandROI.PNG)

**1. Budget Recommendation**

Focus on production budgets between 10 million usd  and 40 million usd , aligning with the 25th to 75th percentile, to capture consistent ROI opportunities while occasionally considering high-budget films ($100M+) to capitalize on blockbuster trends, but prioritize efficient mid-budget films for stability

**2. Genre's Recommendation** 

Focus on producing high-revenue films in Adventure, Action, and Drama genres to target global audiences, incorporating occasional high-budget blockbusters for significant market impact, while leveraging Horror and Animation genres for low-risk, high-ROI projects to ensure a balanced and profitable portfolio.

## ROI vs Production Budget

![ ROI vs Production Budget](https://github.com/Day-hue/phase-2-project/blob/main/Charts/roivsbudget.PNG)

**Key Observations:** 

**Negative Correlation Between Budget and ROI**

As the production budget increases (moving right along the X-axis), the ROI generally decreases, clustering near zero.
High-budget movies (above 100 million) show lower ROI, meaning they do not always generate proportionally high profits.

**High ROI for Low-Budget Films**

Some low-budget films (left side of the plot) show extremely high ROI, suggesting that low-budget films can be highly profitable.

**Wide ROI Variability in Low-Budget Films**

The leftmost side of the plot (low-budget films) has a large spread in ROI, meaning some films generate very high returns while others fail.

**Stable ROI for High-Budget Films**

The right side (high-budget films) has a narrower spread in ROI, suggesting that blockbuster movies have more predictable but lower returns.

**Insights & Implications:**

 * Higher budgets do not guarantee high ROI. Studios should carefully analyze the risk of large investments.
 * Low-budget films have higher profit potential but higher risk. Some achieve massive ROI, while others fail entirely.
 * Medium-budget films might offer a balance. Further analysis of budget categories is needed to determine an optimal investment range.

## Relationship between Ratings and Revenue 

![Ratings vs Revenue](https://github.com/Day-hue/phase-2-project/blob/main/Charts/ratingsvsrevenue.PNG)

Variance in Revenue: While higher-rated movies tend to earn more, the spread of revenue is wide at each rating level, meaning other factors (e.g., budget, marketing) also influence earnings.

High Revenue Outliers: Some movies with ratings around 6-8 have exceptionally high revenues (over 1 billion), likely representing blockbuster hits.

Interpretation:

Movies with higher ratings generally earn more revenue, but ratings alone are not a strong predictor of box office success.

Other factors such as franchise value, marketing, and production budget significantly impact earnings.

## Audience Engagement and Box Office Performance

![Audience Engagement vs Revenue](https://github.com/Day-hue/phase-2-project/blob/main/Charts/audienceengagementvsrevenue.PNG)

Interpretation and Insights: Stronger Correlation Than Ratings vs. Revenue

Unlike average ratings (which had a weak effect on revenue), the number of votes shows a clearer upward trend.
More engagement often means a larger audience, leading to higher revenue.
Popular Movies Are More Profitable

Movies with a high number of votes tend to generate more revenue.
This suggests that audience size (engagement) is a better predictor of box office success than just the rating score.
Outliers Exist

Some movies with low votes still have high revenue (possibly due to marketing, franchise popularity, or blockbuster status).
Some movies with high votes but lower revenue might have gained popularity post-theatrical release (e.g., cult classics or streaming success).
Causation vs. Correlation

High engagement likely leads to higher revenue, but marketing, production budget, and franchise status also contribute significantly.


## **Key Takeaways**
 * High-rated movies generally earn more revenue, but the advantage is not absolute.
   * While median revenue increases with rating, the presence of high-revenue outliers in both average- and low-rated films suggests that other factors (e.g., budget, marketing, franchise strength) play a critical role.

* Some low-rated films can still perform well.
   * The presence of outliers in the "Low" category suggests that certain movies succeed despite poor reviews—possibly due to strong marketing, established fan bases, or niche appeal.

* The “Average” rating category has the highest variation.
   * Many blockbusters fall into this category, showing that critical reception is not the only predictor of financial success.

## **Recommendations for the Film Industry**
1. Invest in High-Quality Productions (But Don't Ignore Other Factors)
 * Since higher-rated movies tend to perform better on average, studios should prioritize quality storytelling, strong scripts, and production value.
 * However, high ratings do not guarantee high revenue, so marketing and distribution strategies remain crucial.

2. Focus on Marketing and Franchise Potential
 * Some low-rated movies (outliers) achieve high revenue, likely due to franchise popularity or strong branding (e.g., superhero movies, action franchises).
 * Marketing campaigns, strategic release timing, and audience engagement play a crucial role in box office performance.

3. Target Broad Audiences for Mid-Tier Movies
 * Mid-rated films (5-7/10 range) still have strong revenue potential.
 * Instead of focusing only on critic scores, studios should leverage audience preferences, genre appeal, and accessibility to maximize profits.

4. Utilize Streaming and Digital Platforms
* Movies that do not perform well in theaters can gain popularity post-release through streaming services, leading to increased revenue over time.
 * Investing in alternative revenue streams (digital rentals, merchandise, special editions) can boost profitability for movies that underperform in theaters.

**Final Thoughts**

While higher ratings generally lead to better revenue, there is no absolute guarantee of success. Successful films often rely on a combination of quality, marketing, franchise value, and audience reach. Studios should adopt a balanced strategy, focusing not just on critic scores but also on audience preferences, effective distribution, and strong marketing efforts.

# Modeling 

![modeling results](https://github.com/Day-hue/phase-2-project/blob/main/Charts/modeling.PNG)

**The table above compares the performance of different regression models based on several evaluation metrics.** 

**Metrics:**

 * **MAE (Mean Absolute Error):**
   * Represents the average absolute difference between the predicted and actual values. Lower MAE indicates better accuracy.

 * **MSE (Mean Squared Error):**
   * Measures the average squared difference between the predicted and actual values. MSE gives higher weight to larger errors.

 * **RMSE (Root Mean Squared Error):**
   * The square root of MSE, providing an interpretable metric in the same units as the target variable. Lower RMSE indicates better accuracy.

 * **MAPE (Mean Absolute Percentage Error):**
   * Represents the average percentage difference between the predicted and actual values. Lower MAPE indicates better accuracy.

 * **R2 (R-squared):**
   * Measures the proportion of variance in the target variable that is explained by the model. Higher R2 indicates a better fit.

 * **Training Time (s):**
   * The time taken by the model to train on the data.

 * **Prediction Time (s):**
   * The time taken by the model to make predictions on new data.

**Interpretation:**

 * **CatBoost Regressor:**
   * Achieves the lowest MAE, MSE, RMSE, and MAPE, indicating the best overall performance in terms of accuracy. However, it has the longest training time.

 * **LGBM Regressor:**
   * Performs well across all metrics, with a slightly higher MAE and RMSE compared to CatBoost. It has a faster training time than CatBoost but slower than XGBoost.

 * **XGBoost Regressor:**
   * Performs similarly to LGBM Regressor, with slightly higher errors. It has the fastest training time among the three.

 * **Linear Regressor:**
   * Has the highest errors across all metrics, indicating the least accurate performance. It has a relatively fast training time.

## Visualization of the best model

![Visualization of the best model](https://github.com/Day-hue/phase-2-project/blob/main/Charts/bestmodel.PNG)

## prediction vs actual for all the models

![Prediction vs actual for the models](https://github.com/Day-hue/phase-2-project/blob/main/Charts/predictionvsactualvalues.PNG)

**The graph showcases the performance of four different regression models by comparing their predicted values to the actual values.**

**Interpretation:**

 * **Ideal Scenario:**
   * The red dashed line represents the perfect prediction where predicted values equal actual values. The closer the data points are to this line, the better the model's performance.

 * **Model Performance:**
   * All four models demonstrate good performance, with the data points closely aligned with the diagonal line. This suggests that the models are accurately predicting the target variable.

 * **Comparison:**
   * Among the four, the XGB Regressor seems to have the tightest clustering of points around the diagonal line, indicating it might be the most accurate model in this comparison.

Overall, the graph illustrates the accuracy of the regression models in predicting the target variable.

## Residuals








