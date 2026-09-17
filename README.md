# Project
test repo
this repo created by mohammad jaradat 
print("hello")
# IMDB Movie Data Analysis 🎬

## About the Project

This project analyzes movie data from the IMDB dataset using **Python, Pandas, Matplotlib, and Seaborn**. The goal is to explore the dataset and find interesting patterns related to movie genres, ratings, revenue, and popularity.

Instead of looking at the raw data only, I used different visualizations and statistical analysis to better understand the movies and identify useful insights.

## Tools and Libraries

The project uses the following Python libraries:

* **Pandas** – for loading, cleaning, and analyzing the data.
* **Matplotlib** – for creating charts and visualizations.
* **Seaborn** – for creating more detailed and attractive statistical plots.

## Dataset

The dataset used in this project is **IMDB-Movie-Data.csv**. It contains information about movies such as:

* Movie title
* Genre
* Rating
* Number of votes
* Revenue
* Release year
* And other movie-related information

## Data Preparation

Before starting the analysis, the data needs some basic cleaning.

First, missing values in the `Genre` column are replaced with empty strings. Since a movie can belong to more than one genre, the genre values are split using commas.

For example:

```text
Action, Adventure, Sci-Fi
```

becomes separate genre values:

```text
Action
Adventure
Sci-Fi
```

The `explode()` function is then used so that each genre can be analyzed individually.

The `Revenue (Millions)`, `Year`, `Rating`, and `Votes` columns are also converted to numeric values. Invalid values are changed to missing values using `errors='coerce'`.

## Analysis and Visualizations

### 1. Most Common Movie Genres

The project counts how many movies belong to each genre and displays the **top 10 most common genres** using a bar chart.

This helps us understand which types of movies appear most frequently in the dataset.

### 2. Highest-Rated Genres

Next, the average rating for each genre is calculated.

The genres are grouped together, and their average ratings are calculated using:

```python
df_genres.groupby('Genre')['Rating'].mean()
```

The three genres with the highest average ratings are then displayed in a bar chart.

This gives an idea of which genres tend to receive higher ratings in this particular dataset.

### 3. Average Revenue Over the Years

The project also looks at how movie revenue changes over time.

Movies are grouped by their release year, and the average revenue is calculated for each year.

A line chart is used to show the changes in average revenue across the years. This makes it easier to see years where the average movie revenue was particularly high or low.

### 4. Rating vs. Number of Votes

A scatter plot is created to compare **movie ratings** with the **number of votes**.

The idea is to see whether movies with more votes tend to have higher or lower ratings.

The correlation between the two variables is also calculated using:

```python
df[['Rating', 'Votes']].corr()
```

The correlation value helps describe the strength and direction of the relationship between ratings and votes.

### 5. Top 10 Movies by Revenue

Finally, the dataset is sorted according to `Revenue (Millions)`.

The project then displays the **10 movies with the highest recorded revenue**, showing their titles and revenue values.

This provides a quick look at the highest-grossing movies in the dataset.

## Main Insights

From the analysis, several observations can be made:

* **Action, Drama, and Comedy** are among the most frequently appearing genres.
* Some less common genres can have relatively high average ratings.
* Movie revenue changes considerably from year to year rather than following a constant trend.
* There is a relationship between the number of votes and movie ratings, although correlation does not necessarily mean that one directly causes the other.
* The revenue analysis highlights the movies that generated the highest recorded earnings in the dataset.

## Conclusion

This project was a practical way to use Python for **exploratory data analysis (EDA)**. By combining data cleaning, grouping, statistical calculations, and visualization, the raw IMDB dataset becomes much easier to understand.

The project also demonstrates how data analysis can be used to answer questions such as:

* Which genres are most common?
* Which genres have higher average ratings?
* How does movie revenue change over time?
* Is there a relationship between ratings and popularity?
* Which movies generated the most revenue?

Overall, the analysis provides a simple overview of movie trends in the IMDB dataset and demonstrates the use of **Pandas, Matplotlib, and Seaborn** for real-world data analysis.

