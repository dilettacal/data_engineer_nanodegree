# Introduction
The first project of the Udacity's Data Engineering Nanodegree is about Data Modeling with PostgreSQL.

# Overview
Sparkify is a music streaming service. Currently all information about the streamed music, users and usage of the service are stored into log files in JSON format.
The goal of this task is to improve the data storage and analytics by creating a PostgreSQL database. 

# Datasets
There are two JSON datasets:
1. Song Dataset - Complete details and metadata about the song
2. Log Dataset - User activity log

# STAR Schema 
Relational databases allow data modeling and querying. Here PostgreSQL is used, especially tables are designed based on the STAR schema.

The STAR schema consists of one or more FACT tables referencing any number of DIMENSION tables. 
In Sparkify the schema is implemented as follows:
* FACT table `songplays` which contains the metadata of the complete information about each user activity. 
* DIMENSION tables: `users`, `songs`, `artists` and `time table` contain relevant information about users, songs, artists and time of use 

# ETL Pipeline
An ETL pipeline is built to extract and process data from the available datasets. 
Further fact and dimention tables are created.

# Files
The repository contains following data:
1. `create_tables.py` creates the tables in the database. This script should be used in advance, in order to drop existing tables and create new ones.
2. `sql_queries.py` contains the queries to select and insert entries into the database
3. `etl.ipynb` is a IPython notebook displaying the database functionality
4. `etl.py` is a script that reads and processes files, in order to store them into the database
5. `test.ipynb` is notebook to test the program functionality

# How to run the code
To run the pipeline, you need to run following scripts:
1. Create tables with `create_tables.py`
   $ python3 create_tables.py   
2. Run ETL pipeline with `etl.py`
   $ python3 etl.py 
  
   