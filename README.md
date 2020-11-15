# Movies-ETL
Data Analytics course, Module 8

## Overview of project

This is an Extraction / Processing / Loading exercise, to get raw data from various sources into a form that can be processed in a database.

For this project, I collected movie data from
- wikipedia, as JSON files
- kaggle
- MovieLens ratings

The data, especially the wikipedia data, required a fair deal of scrubbing to get into a readable DataFrame, and from there into a database table. 


# Extracting
- data came in as both as CSV's and JSON files. These were converted to dictionaries and/or dataframes.

# Processing examples

- combining data that had slightly different lables, e.g. one movie might have show "Director", another showes "Directed by". Python set up a dictionary structure with both fields - this process aimed to combine those fields and other similar pieces of data.
- There were fields for many different languages - this process created on field for alternate language
- monetary amounts was presented in many different formats - this project used standard expressions to figure out what format was being used, convert to a consistent layout. Same for date fields.
- individual movie reviews were grouped and counted by movie and rating, and the results stored in an easy-to-read table.

# Loading
- the clean data was stored in Pandas DataFrames in python, and then exported to a PostGreSQL database.
- as a quick check on the integrity of the process, I counted the rows of movie data and review data in PostGreSQL. Screenshots of this validation are stored as

[Movie_Count](/Resources/movies_query.png)

[Ratings_Count](/Resources/ratings_query.png)



