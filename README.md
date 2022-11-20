# Microsoft-Movie-Studio-Project
# Introduction

![tyson-moultrie-BQTHOGNHo08-unsplash](https://user-images.githubusercontent.com/71209567/202917440-7c16dfac-d4ae-4936-9081-788e61af0293.jpg)

Photo by <a href="https://unsplash.com/@tysonmoultrie?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Tyson Moultrie</a> on <a href="https://unsplash.com/s/photos/movies?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
  

This project will use exploratory data analysis to generate insights for a Microsoft Stakeholder.
# Business Understanding
## Real World Problem:

Microsoft has seen all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. The task at hand is exploring what types of films are currently doing the best at the box office. 

## Aim of the project:

The data will be used by the head of Microsoft's new movie studio to help decide what type of films to create.
## Objectives:
In order to make recommendations, this analysis is going to explore some questions which are:
1. What types of films are doing the best at the box office?

2. Which languages are doing the best at the box office?

3. Does Release month affect profit?

4. Is there a correlation between runtime minutes and the other variables?

# Data Understanding
## 1. Sources and Properties of Data :
The folder containing the data is called "zippedData" which contains movie datasets from:

1. Box Office Mojo

2. IMDB

3. Rotten Tomatoes

4. TheMovieDB

5. The Numbers 

The data files used in the analysis are:

1. im.db.zip which is a Zipped SQLite database (It needs to be unziped then queried using SQLite). The relevant tables are movie_basics and movie_ratings.

2. bom.movie_gross.csv.gz - a compressed CSV file

3. tn.movie_budgets.csv.gz - a compressed CSV file

4. tmdb.movies.csv.gz - a compressed CSV file

We will not use the data from the TSV files because they don't have the data we need in analysing. We will only use the compressed CSV files and unzipped IMDB file.

Our final dataset to be used in the analysis is named "movies_df". The size of the dataset is 1001 by 10 (1001 rows by 10 columns). The columns are:

1. movie - name of film

2. runtime_minutes - total minutes of a film

3. genres - types of films

4. averagerating - average rating of individual films

5. production_budget - total production budget for the film

6. month - release month of the film

7. profit - total amount remainint production budget from total gross

8. original_language - film language

9. popularity - how popular a film is

10. year - release year of film

These columns are relevant in analysing what impact genres, language and release month have on films in order to make conclusions and recommendations.
## 2. Loading libraries
Load the libraries required for the analysis
## 3. Loading datasets
Load the compressed CSV files and the IMDB zippedfile. Unpack the IMDB file then query it using SQLite. Convert the movie basics tables and movie ratings tables into dataframes.
# Data Cleaning
Here we will do data cleaning. Data cleaning is the process of preparing data for analysis by weeding out information that is irrelevant or incorrect.This is generally data that can have a negative impact on the model or algorithm it is fed into by reinforcing a wrong notion. 

We will analyse each dataset separately because we have 5 datasets to start with. The steps for our data cleaning is:

1. Completeness - Ensure the datasets has no missing values.

2. Uniformity - The datatypes for the datasets are correct.

3. Consistency - Ensure there are no duplicates in the data.
# Results
## Genres
![Most Profitable Genres](https://user-images.githubusercontent.com/71209567/202910256-1cf6b4a5-b1ea-4105-839d-37dc590145b1.png)

The top 5 most profitable genres are Adventure, Action, Comedy, Drama and Animation.

## Languages
![Most Profitable Languages](https://user-images.githubusercontent.com/71209567/202910283-653e45a5-e24b-45b6-a001-268a0c9b6e80.png)

The top 5 most profitable languages are Thai, Telugu, English, Hungarian and Hindi

## Release Month
![Months With Highest Profit](https://user-images.githubusercontent.com/71209567/202910326-89c317a0-a569-46ff-bb7d-70e04a6b3694.png)

The top 3 most profitable months are June, May, July, November and December.

## Correlation
![Correlation Representation Using a Heatmap](https://user-images.githubusercontent.com/71209567/202910469-88669fd8-1ef0-4a01-ba1a-1b32b6770a32.png)

We have positive correlation between all the variables but varying in terms of strength. A positive correlation is a relationship between two variables that tend to move in the same direction. In this case one variable tends to increase when the other increases.

# Conclusions
## 1. What types of films are doing the best at the box office?
Genre was analysed based on profit, budget, popularity and rating. The top genres (types of films) are Adventure, Action Comedy and Drama.
## 2. Which languages are doing the best at the box office?
Languages were analysed based on profit, popularity , budget and rating. The top languages are Thai, Telugu, English, Danish, Greek Mordern, Germany  and Spanish.
## 3. Does Release month affect profit?
Yes The Release Month with the highest profit are June, May, July, November and December. School breaks and work vacations fall within these months hence attributing for the profitability of movies on these months. 
## 4. Is there a correlation between runtime minutes and the other variables?
No, runtime minutes for a film has a weak positive correlation on the quantitative variables. Runtime minutes for the film do not affect its profitability or popularity strongly hence the minutes can vary.
# Recommendations
1. The best types of films to create are Adventure, Action and Comedy
2. The best languages for this films are Thai, Telugu and English
3. The best months to release the films are June, May and July.
# Repository Guide

The data used for the project can be found here https://github.com/Glo-riah/Microsoft-Movie-Studio-Project/tree/main/Data

The images from EDA can be found here https://github.com/Glo-riah/Microsoft-Movie-Studio-Project/tree/main/MS%20EDA%20images

The notebook that contains the project can be found here https://github.com/Glo-riah/Microsoft-Movie-Studio-Project/blob/main/microsoft_movie_studio.ipynb

The presentation for this project can be found here https://github.com/Glo-riah/Microsoft-Movie-Studio-Project/blob/main/Microsoft%20Movie%20Studio%20Presentation.pdf
