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
Charts/genre vs ROI and T.Gross.PNG




