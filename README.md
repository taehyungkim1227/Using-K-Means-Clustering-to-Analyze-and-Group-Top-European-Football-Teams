# Using K Means Clustering to Analyze and Group Top European Football Teams

## Part 1. Project Background

#### This project started with an innate, deep curiosity on how to group European football teams based on team statistics. There is no other indicator than league rank to vaguely categorize teams into "strong", "somewhat strong", "weak" etc. The k-means clustering algorithm was a perfect fit for this intention, as it naturally groups datapoints based on their Euclidean distance. For this project, I used R code (please refer to the Rmd file in this same repository folder) and used data from www.whoscored.com (all teams from the top 3 European Leagues and data collected in the mid-season of 2022-2023). Raw data sheet can be found here: https://docs.google.com/spreadsheets/d/1gpq2NdKtCitcjUuaP7FPSYnUu3GnOfxy6njsmNUOCMY/edit#gid=1726730019.

## Part 2. Data Import, Preprocessing and EDA

#### For data preprocessing, I eliminated the numbers that preceded team names (in order for clearer data manipulation and analysis) and I standardized the data (mean = 0, standard deviation = 1) using the scale() function in order to account for the varying units in the data. For instance, Shots per game, Shots on target per game, Dribbles per game, and Fouled per game are all different match statistics and in order for every variable to contribute equally to the k-means clustering model, I used standardization.

## Part 3. K-Means Clustering

#### For this part, I used the kmeans() function in R. The number of clusters ('centers' value) was set to 3 for effective analysis (too many clusters would prevent me from diving deeper into each cluster in terms of observation and analysis) and the 'nstart' variable was chosen to be 25, which is commonly used. The clusters were divided into sizes of 22, 11, and 25 teams each. The main variables of observation in this project are Goals Conceded per game (y) and Shots per game (x). 

#### - ![](Visualizations/clustering-viz1.png)

#### - ![](Visualizations/clustering-viz2.png)

### Part 3-1. Cluster Number 2 - The Strongest Teams

#### Cluster Number two has the largest values of Shots per Game (1.4461), Shots on target per game (1.4212), Dribbles per Game (0.8490) while having the lowest values of Fouled per Game (-0.7276) and Goals Conceded per game (-0.7819). Keep in mind these are all standardized values. Most of the teams in this cluster are traditionally strong and globally well known teams such as Real Madrid, Barcelona, Arsenal, Manchester City, Liverpool, and Bayern Munich. Some surprising teams in this cluster include Brighton (known for their attacking football under ex-Udinese manager De Zerbi, Brighton excitingly made it to this cluster with a high shots per game stat compared to other clusters but simultaneously with a rather large goals conceded per game within this cluster) and Manchester United (a traditionally well known big team, but has low shots per game and rather high goals conceded per game within this cluster).

#### - ![](Visualizations/clustering-viz3.png)

### Part 3-2. Cluster Number 3 - Mid to Upper-Mid Table Teams

#### Cluster Number three has the largest value of Fouled per Game (0.7594). Keep in mind this is a standardized value. It is interesting that most of these teams tend to have a high shots per game stat with high goals conceded per game. Teams in this cluster seem to have varying characteristics, which is interesting. Teams like Girona for instead, scored a lot but also conceded a lot in the last season of the La Liga. VfB Stuttgart scored a lot of goals compared to other teams in similar relegation threatened positions in the bottom of the table of the German Bundesliga, but also conceded a fair amount causing their rather poor goal difference statistic. RB Leipzig scored the most amount of goals in the Bundesliga outside of Dortmund and Bayern Munich but conceded the second most number of goals among the top five teams in the Bundesliga. On the far left corner of the graph, Spanish team Mallorca scored the sixth least amount of goals in the Spanish La Liga and conceded the 8th least amount of goals too, displaying a rather defensive yet offensively rather blunt style of football. 

#### - ![](Visualizations/clustering-viz4.png)

### Part 3-3. Cluster Number 1 - The Underdogs (but with their own Merits)

#### Cluster Number one has the lowest Shots per Game (-0.6677), Shots on target per game (-0.7380), Dribbles per Game (-0.6652), while having the largest value of Goals Conceded per Game (0.7782). Keep in mind these are all standardized values. Most teams in this cluster displayed rather poor performorances last season, such as in the case of Leicester City and Southampton, both relegated to the second tier of football in England. Some teams do stand out however, such as Union Berlin, a team that was promoted to the German Bundesliga only 4 years ago but made it to the UEFA Champions League in the 2022-2023 season. Also Fulham, although in this underdog cluster, made 10th place in the Premier League, an impressive run from a newly promoted team. 

#### - ![](Visualizations/clustering-viz5.png)

## Part 4. Reference

#### -https://uc-r.github.io/kmeans_clustering

