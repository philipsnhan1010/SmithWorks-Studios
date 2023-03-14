# SmithWorks-Studios
Aanalyze data on previous movies from IMDb , a popular source for movie ratings, to get ideas of the types of movies it should produce to maximize its profit

# About the Project
1. Overview of IMDb movie ratings.
2. Import the Movies Data set into a Pandas DataFrame: movie_df = pd.read_csv(r'Movie Assignment Data.csv')

3. Generate descriptive statistics for the budget of all the movies: movie_df[["budget"]].describe().applymap(lambda x: f"{x:,.0f}")

4. Find out how many of the top-rated movies produced in the United States have a PG-13 rating.
5. Find out whether any of the top-rated movies produced in 2014 were not produced in the United States.
6. Find the percentage of the top-rated movies that are in:
- 1 genre only
- 2 genres only
- 3 genres only
7. Convert the budget and gross values from “dollars” to “dollars in millions” for all top-rated movies. Round the converted values down to 3 decimal places. For example, a value of 192,345,273 should be converted to 192.345.
8. List all details for the top 10 movies with the highest profit, sorted from highest to lowest. Hint: Profit is not a column in the DataFrame. You will need to calculate it.
9. Generate a list of all the actors, in alphabetical order by the first name, that have starred in a top-rated movie. If an actor has starred in multiple movies, their name should appear only once on the list. Assume that all actors’ names are in the format <first_name> <last_name>.
10. The movie studio wants to determine who it should approach to act in its next movie production. Find the top 3 actors who appeared in the most top-rated movies.
11. Create a data visualization that shows each country and the number of top-rated movies produced in it. Find the country that produced the most top-rated movies.
movie_stats_df = movie_df['Country'].value_counts().to_frame()

![image](https://user-images.githubusercontent.com/43742200/224871526-3c8e8a00-7c33-4c0e-bf79-4a87a780272b.png)
movie_stats_df.plot(kind='bar', y='Country', figsize=(5, 5));
plt.title('Number of top-rated movies produced by country')
plt.xlabel('Country')
plt.ylabel('Count')
plt.show()

![image](https://user-images.githubusercontent.com/43742200/224871585-da029c09-2f62-48b4-89c1-368b2e6a3b67.png)


# Tech
- Python: Numpy, Pandas, Matplotlib
- Jupyter Notebook.

# Containing files
1. Movie Data.csv: movies data set
2. Movie Data Dictionary.xlsx: movies data dictionary
3. SmithWorks_Analysis.ipynb: Jupyter Notebook solution file
