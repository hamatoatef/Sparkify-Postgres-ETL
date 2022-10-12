# Sparkify ETL with Postgres and Python
In this project, we'll apply data modeling with Postgres and build an ETL pipeline using Python. we will need to 
> define fact and dimension tables for a star schema for a particular analytic focus,
> write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL. 

## Project Description
This project is to create a SQL analytics database for a music streaming startup called Sparkify. 
A Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app.The analytics team is particularly interested in understanding what songs users are listening to, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

## How to run the Python scripts
1. Run create_tables.py to create your database and tables.
2. Run etl.py to process for extract, transform , load
3. Run test.ipynb to confirm the creation of your tables with the correct columns

## Project Template


1.  test.ipynb displays the first few rows of each table to let you check your database.

2. create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.

3. etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains  detailed instructions on the ETL process for each of the tables.

4. etl.py reads and processes files from song_data and log_data and loads them into your tables. You can fill this out based on your work in the ETL notebook.

5. sql_queries.py contains all your sql queries, and is imported into the last three files above.

## Data Modeling 

### fact Table

songplays - records in log data associated with song plays i.e. records with page NextSong
        (songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent)

### Dimension Tables

users - users in the app
        (user_id, first_name, last_name, gender, level)
songs - songs in music database
        (song_id, title, artist_id, year, duration)
artists - artists in music database
        (artist_id, name, location, latitude, longitude)
time - timestamps of records in songplays broken down into specific units
        (start_time, hour, day, week, month, year, weekday)
        
        
![drawSQL-export-2022-10-12_03_32](https://user-images.githubusercontent.com/88297240/195228854-11273b41-d2b0-4e32-a6a8-bea3657cb7f2.png)
