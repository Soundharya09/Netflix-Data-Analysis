# Netflix Analysis Project
## Project Overview:
This project performs an in-depth analysis of Netflix’s movie and TV show dataset, focusing on understanding content trends, audience ratings, and genre preferences. 
The goal is to explore how different variables — such as genre, popularity, ratings, and release year — shape Netflix’s content library and viewer interests.

## Dataset:
File Used: mymoviedb.csv
- The dataset represents Netflix’s movie collection with attributes such as:
  - Movie_ID,
  - Title,
  - Genre,
  - Release_Date,
  - Popularity,
  - Vote_Average,
  - Vote_Count,
  - Revenue,
  - Runtime, etc.
- It provides a good basis to study content trends, ratings, and performance metrics.

## Data Cleaning and Preprocessing:
Key steps in your notebook include:
- Loaded the dataset using a safe line terminator (lineterminator='\n') to handle malformed rows.
- Checked for missing values and handled them appropriately.
- Converted date columns (Release_Date) into proper datetime formats.
- Removed duplicates and irrelevant columns.
- Standardized text data (titles, genres, etc.) for better grouping and analysis.
- Categorized the “Vote_Average” column into four interpretive buckets: popular, average, below_avg, not_popular using a custom function categorize_col() for descriptive clarity.
- Split the Genre column into a list and used explode() to analyze movies with multiple genres more effectively.

## Feature Engineering:
- Derived a popularity label based on Vote_Average for qualitative interpretation.
- Extracted year, month, and decade from Release_Date to observe temporal trends.
- Added features for content length buckets (short, medium, long) based on runtime.
- Calculated summary statistics (mean, median) for rating and revenue by genre.

## Exploratory Data Analysis (EDA):
The EDA section deeply examines trends and distributions across various dimensions:

a. General Distribution:
- Frequency of movies by release year shows Netflix’s growth in content over time.
- Most common genres and their counts (Drama, Comedy, Action).

b. Popularity and Ratings:
- Distribution of Vote_Average using histograms and KDE plots.
- Count plots of the popularity categories (popular, average, etc.).
- Relationship between Vote_Count and Vote_Average — to see if higher votes correlate with higher ratings.

c. Genre-Level Insights:
- Average ratings and popularity per genre.
- Top 10 genres by number of movies.
- Boxplots showing the spread of ratings and revenue for major genres.

d. Temporal Trends:
- Trend of movie releases by year and decade.
- Line plots showing change in average ratings or popularity over time.
- Seasonal trends (if monthly or quarterly analysis performed).

e. Correlation Analysis:
- Correlation heatmap between numerical variables like Vote_Average, Vote_Count, Revenue, and Popularity.
- Pair plots for quick pattern recognition between ratings, votes, and revenue.

## Data Visualization:
Your notebook uses Matplotlib and Seaborn extensively:
- Countplots, Boxplots, Heatmaps, Histograms, and Bar Charts for summarizing relationships.
- Genre-wise popularity comparisons using grouped bar charts.
- Temporal trends visualized with line charts.
- Enhanced readability using Seaborn’s set_style() and consistent color themes.
These visuals effectively communicate key findings and make storytelling intuitive.

## Insights & Findings:
From the analysis:
- The majority of Netflix content is movies rather than shows.
- Drama, Comedy, and Action are the top-performing genres.
- Most Netflix titles have moderate popularity (Vote_Average between 6–7).
- The number of releases has grown steadily after 2010, reflecting Netflix’s global expansion.
- Popularity does not always correlate directly with revenue — niche genres often have high ratings but low vote counts.
- Audience engagement tends to be higher for recent content and specific genres like thrillers or sci-fi.

## Tools and Libraries:
- Python: Core language
- Libraries: Pandas, NumPy, Matplotlib, Seaborn
- Environment: Jupyter Notebook
- Techniques: Data Cleaning, Categorization, EDA, Feature Engineering, Visualization

## Deliverables:
- Cleaned dataset ready for further ML modeling.
- Comprehensive Jupyter Notebook with step-by-step analysis.
- Clear visual insights summarizing Netflix’s content trends.

Potential use cases:
- Content recommendation insights
- Genre-based acquisition strategies
- Popularity trend prediction

## Summary:
This project demonstrates end-to-end data analysis and storytelling about transforming raw Netflix data into actionable insights through meticulous preprocessing,  
visualization, and feature engineering. It highlights your ability to handle messy real-world data, extract insights, and communicate findings effectively through visual storytelling.
