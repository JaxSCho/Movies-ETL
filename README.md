# Movies - ETL
## Project Overview
In order to update the dataset daily for Amazing Prime, we helped Britta create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We created one function that takes in the three files - Wikipedia data, Kaggle metadata, and the MovieLens rating data - and performs the ETL process by adding the data to a PostgreSQL database by refactoring the code from this module. 

## Summary
The following deliverables have been created:

1. [Write an ETL Function to Read Three Data Files](ETL_function_test.ipynb) - Creates a function that reads in the three data files and creates three separate DataFrames

2. [Extract and Transform the Wikipedia Data](ETL_clean_wiki_movies.ipynb) - Extracts and transforms the Wikipedia data to merge it with the Kaggle metadata. A try-execept block is used to catch errors while extracting the IMDB IDs using a regular expression string and dropping duplicates.
    
3. [Extract and Transform the Kaggle Data](ETL_clean_kaggle_data.ipynb) - Extracts and transforms the Kaggle metadata and MovieLens rating data, then converts the transformed data into separate DataFrames. The Kaggle metadata DataFrame is then merged with the Wikipedia movies DataFrame to create the movies_df DataFrame. The MovieLens rating data DataFrame is then merged with the movies_df DataFrame to create the movies_with_ratings_df.

4. [Create the Movie Database](ETL_create_database.ipynb) - Adding the movies_df DataFrame and MovieLens rating CSV data to a SQL database.
 
## Resources
- Data Sources: wikipedia-movies.json, movies_metadata.csv, ratings.csv
- Software: Python 3.7.6, Jupyter Notebook 6.4.5