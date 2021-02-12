# Udacity Data Engineer Course / Project 1: Data Modeling with Postgres
## 1 Description
The data from Sparkify is available in different json files (song_data, log_data). On such files it is hard to run queries and analytics on. The goal is to make use of the data with a database. There queries and analytics could be run. The employees therefore can do more with the data they collected.  
To reach this goal an ETL process needs to be in place, to process, transform and insert the data from the json files into a database (postgres in this scenario).  
The database is using the star schema to optimize the queries on the song play analysis and contains the following fact and dimension tables:  
Fact tables:
- songplays

Dimension tables:
- users
- artist
- song
- time

For the ETL process jupyter is used at first and then the learned knowledge is transfered to a python script afterwards.

## 2 Project Setup
### 2.1 Prerequisites
The following tools/packages/frameworks have to be installed on your system
- docker and docker-compose
- python3 with psycopg2 and pandas
- jupyter (to open the jupyter notebooks) and inside psycopg2 and pandas

### 2.2 Run the project
- First run ```docker-compose up``` to fire up the postgresDB

To run the python scripts:
1. run ```python3 create_tables.py``` to create the sharkifydb and all the tables needed
2. run ```python3 etl.py``` to fill the tables with data from the json files (song_data, log_data)

Jupyter Notebooks:
1. ETL: run all commands inside the etl.ipynb. This will create the sharkifydb and all the tables needed and fill the tables with data from the json files (song_data, log_data)
2. SQL Queries: run all commands inside the test.ipynb. This will give you an short overview about the data from the database
3. Analytics: run all commands inside the analytics.ipynb. This will give you some anylitics drawn from the data in the database

## 3 ER-Diagram
![ERD-Sharkifydb](./erd-sparkifydb.png)

## 4 Jupyter Notebooks
| Name                      	| Description                                                    	|
|---------------------------	|----------------------------------------------------------------	|
| test.ipynb                   	| displays the first few rows of each table to let you check your database. |
| etl.ipynb                     | reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.  	    |
| analytics.ipynb           	| contains some analytics example queries for the data              	|
