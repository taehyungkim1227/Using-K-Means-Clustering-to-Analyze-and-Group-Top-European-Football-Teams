# Using K Means Clustering to Analyze and Group Top European Football Teams

## Part 1. Project Background

#### This project started with an innate, deep curiosity on how to group European football teams based on team statistics. There is no other indicator than league rank to vaguely categorize teams into "strong", "somewhat strong", "weak" etc. The k-means clustering algorithm was a perfect fit for this intention, as it naturally groups datapoints based on their Euclidean distance. For this project, I used R code (please refer to the Rmd file in this same repository folder) and used data from www.whoscored.com (all teams from the top 3 European Leagues and data collected in the mid-season of 2022-2023). Raw data sheet can be found here: https://docs.google.com/spreadsheets/d/1gpq2NdKtCitcjUuaP7FPSYnUu3GnOfxy6njsmNUOCMY/edit#gid=1726730019.

## Part 2. Data Import, Preprocessing and EDA

#### For data preprocessing, I eliminated the numbers that preceded team names (in order for clearer data manipulation and analysis) and I standardized the data (mean = 0, standard deviation = 1) using the scale() function in order to account for the varying units in the data. For instance, Shots per game, Shots on target per game, Dribbles per game, and Fouled per game are all different match statistics and in order for every variable to contribute equally to the k-means clustering model, I used standardization.

## Part 3. K-Means Clustering

#### For this part, I used the kmeans() function in R. The number of clusters ('centers' value) was set to 3 for effective analysis (too many clusters would prevent me from diving deeper into each cluster in terms of observation and analysis) and the 'nstart' variable was chosen to be 25, which is commonly used. The clusters were divided into sizes of 22, 11, and 25 teams each. The main variables of observation in this project are Goals Conceded per game (y) and Shots per game (x). 

### Part 3-1. Cluster Number 2

####

### Part 3-2. Cluster Number 3

####

### Part 3-3. Cluster Number 1

####

## Part 4. Conclusion and References

####
