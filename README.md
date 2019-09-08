## **Data Modeling with Postgres SQL**
-----------------------------------------------------------------------------------------------------------------------------------

In this project, I will build an ETL pipeline using Python. 
Define fact and dimension tables for a star schema for song play analysis 
write an ETL pipeline that transfers data from files in two local directories into the tables 

## **Motivation**
-----------------------------------------------------------------------------------------------------------------------------------

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team at Sparkify whats to know what songs users are listening to. In order to analyze songs and user activity they need to query certain data, however, the data they currently have is is JSON format.

## **Schema**
-----------------------------------------------------------------------------------------------------------------------------------

The schema will consist of four dimension tables and a fact table. The four dimension tables will be the users, songs, artists and time tables. The fact table will be the song plays table. 


### Schema for Song Play Analysis
Using the song and log datasets, you'll need to create a star schema optimized for queries on song play analysis. This includes the following tables. The columns and data for each table is listed below: 

### Fact Table
songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

### Dimension Tables

users - users in the app
user_id, first_name, last_name, gender, level

songs - songs in music database
song_id, title, artist_id, year, duration

artists - artists in music database
artist_id, name, location, latitude, longitude

time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday


## **Files**
-----------------------------------------------------------------------------------------------------------------------------------

six files included:

test.ipynb displays the first few rows of each table to let you check your database.

create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.

etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. 

etl.py reads and processes files from song_data and log_data and loads them into your tables. 

sql_queries.py contains all your sql queries, and is imported into the last three files above.

data contains JSON format song data and log data. The song data contains data about a song and its artist. The log data is data generated from an event simulator.


## **Installation**
-----------------------------------------------------------------------------------------------------------------------------------


1. Using a new terminal window the sql_queries and create_tables file should be ran first using the following commands
`python sql_queries.py`
`python create_tables.py`

2. The etl.ipynb and test.ipynb can be ran to see the output of each cell

3. In the terminal window the etl.py can be ran using the following command
`python etl.py`

*A new terminal must be ran for any changes made to the py files and the kernel for the ipynb files should be restarted to exit the connection