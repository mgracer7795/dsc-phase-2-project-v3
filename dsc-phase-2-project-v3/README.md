# Analayzing Movie Data from IMBD

# Overview

This project involves comprehensive tasks such as analyzing datasets from the IMBD that were shared in zip file. We had to unpack the tables of the sql file and then merge several tables together. Then we sorted through the data to find the best movies for each genre. Our primary objective was to be able to present these best movies to a company so they can research the best directors from the data and study how they made their mission come to fruition. 

# Business Objective

The main objective was to explore opportunities within the film industry. There were multiple datasets and one of primary focus was the IMBD as a SQL. From this SQL it was essential to filter the data for the best movies and then make recommendations to the new film company about what conclusions we can draw from the best movies we find. 

Below are the primary business questions:


# Data Understanding and Analysis

The data we worked with was from the IMBD as an SQL file.

Original data description:

The original dataset had 77452 entries from the IMBD and 17 columns.

The columns were: 

movie_id
ordering
person_id
category
job
characters
primary_name
birth_year
death_year
primary_profession
primary_title
original_title
start_year
runtime_minutes
genres
averagerating
numvotes

# Dropped Columns 

Columns that weren't needed are birth_year, death_year, ordering, and job

## Cleaned DataSet

The cleaned dataset resulted in filtering our original SQL table for multiple tables for each genre of film.

These genres are:

Drama
Comedy
Action
Thriller
Documentary
Horror
Family

The format for creating these new columns was selecting all from our principles table and joining that table with:
persons, movie_basics, and movie_ratings. All four of these are tables within the file for IMBD that were essential to the study. 
When joined it becomes clear how the person_id and movie_id variables align with the primary_title,director category within the larger category column, AND the averagerating. 

New Columns:

A new column was created for the average of the averagerating column for each director after filtering for the best directors.

# Data Analysis

The bar graphs are a visualization of the best movies for each genre mentioned above. Then from there you are able to focus on who directed those movies so the company will be able to conduct guided research. 

The x-axis on the bar graph for movies represents the primary name of the top 5 highest rated movies for that genre. The y-axis represents the averagerating for that movie according to the IMBD data.

For the movie directors, the bar graph is designed with a column created to calculate the average of the averagerating column. This created column is the y-axis for the director bar graph because it provides an average of the averagerating for all movies that specific director is credited for.

## Recommendations

Based on the results from the filtered data, created column for average of the average rating, and the bar graphs for best movies and best directors, we have found some ideal recommendations: 

The first is the best movies for each genre:

Dramas: Nicki: A Hip Hop Love Story(9.2), Nagarkirtan(9.2), Death of Love(9.1), Gwendolyn(8.9), National Theatre Live: Angels in America Part Two - Perestroika(9.0)

Produced by: Marcus Damone Henry(8.9), Kaushik Ganguly(9.0), Larry Rosen(9.0), Larry Rosen(9.0), Marianne Elliot(8.95)

--- 

Comedy: Big Weekend(9.1), Love in a Coffee Shop(8.8), Filme B - O Vampiro da Paulista(9.2), Mr Pickpocket(8.7), Yeh Suhaagraat Impossible (9.6)

Produced by: Mike Lordi(8.95), Mike Lordi(8.95), Beto Ribeiro(9.15), Pablo D'Stair(8.95), Abhinav Thakur(9.6)

-- 

## Data Analysis
The bar graphs are a visualization of the best movies for each genre mentioned above. Then from there you are able to focus on who directed those movies so the company will be able to conduct guided research.

The x-axis on the bar graph for movies represents the primary name of the top 5 highest rated movies for that genre. The y-axis represents the averagerating for that movie according to the IMBD data.

For the movie directors, the bar graph is designed with a column created to calculate the average of the averagerating column. This created column is the y-axis for the director bar graph because it provides an average of the averagerating for all movies that specific director is credited for.

We wanted to examine the most successful studios to better understand characteristics of success in order to make recommendations to our client. To do this, we used the secondary dataset of movies and box office data and calculated a new column called 'percent_profit.' From some external research, we learned that on average, movie studios keep around 50% of box office revenue, while the distributors (theaters) keep the remaining 50%. We also learned that movies incur additional print, advertising, and marketing costs when promoting a new release that are not accounted for in the production budget. For some films, these additional costs can make up to half of the films production budget.

Therefore, we filtered the secondary box office table to only include films that achieved more than 50% percent profit, and focused on films that achieved more than 75% percent profit to account for any additional marketing and advertising expenses. When we examined the distribution of studios that achieved better than 75% profits, we noticed 7 studios (and generally that smaller production companies, like IFC, A24, and Blumhouse Tilt) optimized best for percent profit while keeping production costs relatively low.

We then examined the most common genres that these 7 studios produced films in and noticed that Drama, Comedy, and Horror comprised significant proportions of their most profitable films. We also examined the spread of runtime, and noticed that the median runtime was somewhere between 90 and 105 minutes. Furthermore, when examining the distribtuon of profitability for films that were more than 50% profitable, we noticed that June, July and October saw the best performance in terms of percent profitability.

## Recommendations
Based on the results from the filtered data, created column for average of the average rating, and the bar graphs for best movies and best directors, we have found some ideal recommendations:

The first is the best movies for each genre:

Dramas: Nicki: A Hip Hop Love Story(9.2), Nagarkirtan(9.2), Death of Love(9.1), Gwendolyn(8.9), National Theatre Live: Angels in America Part Two - Perestroika(9.0)

Produced by: Marcus Damone Henry(8.9), Kaushik Ganguly(9.0), Larry Rosen(9.0), Larry Rosen(9.0), Marianne Elliot(8.95)

Comedy: Big Weekend(9.1), Love in a Coffee Shop(8.8), Filme B - O Vampiro da Paulista(9.2), Mr Pickpocket(8.7), Yeh Suhaagraat Impossible (9.6)

Produced by: Mike Lordi(8.95), Mike Lordi(8.95), Beto Ribeiro(9.15), Pablo D'Stair(8.95), Abhinav Thakur(9.6)

We also recommend that a new entrant to the film industry model their creative stuctures on A24, IFC, and Blumhouse Tilt. All of these studios produce films for less than $10 million and have a median runtime of between 92 and 106 minutes. We recommend that our client focus on Drama, Comedy, and Horror, and to target release dates between late summer and early fall (particularly October). We recommend that our clients partner with smaller, independent theaters to negotiate better box office cuts, and that they hire smaller, social-media focused marketing agencies that leverage virality to minimize marketing costs.

For future analysis, we would like to incorporate data that captures video on demand, streaming, and television revenue, investigate and incorporate retail and merchandising data to assess opportunities for future cash flow, and to look for creatives who work in the styles of the highest rated writers and directors previously identified.
