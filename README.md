# Remote-jobs-api-to-postgre
 # EXTRACTING DATA FROM A REST API AND LOADING INTO POSTGRESQL DATABASE

This project demonstrates how to extract data from a REST API using Python, perform basic eda and or cleaning, and store it in a SQL database for analysis.
It’s a one-time data extraction project, ideal for data analysis or analytics engineering tasks.



# PROJECT OVERVIEW

The goal of this project was to connect to a public REST API, extract structured data (in JSON format), and load it into a SQL database for further querying and analysis.

The project focuses on:

Data extraction using Python’s requests library

Data cleaning and transformation using pandas

Data loading into a SQL database using SQLAlchemy



# Tools and Libraries

Purpose	                   Tool / Library
API Connection	              requests
Data Manipulation   	         pandas
Database Connection	          SQLAlchemy
Environment management          OS
JSON handling                  JSON
PostgreSQL connection          psycopg2
Environment variable loading    dotenv
pprint                          Debugging & formatting




# FOLDER STRUCTURE

Remote-jobs-api-to-postgre/
│
├── data/
│   └── remote_jobs_raw.csv        # raw API data saved as csv
│
├── src/
└── test.ipynb        # script to extract  and clean data from the API



# SETUP AND USAGE
1. Install dependencies
    pip install -r requirements.txt

2. Run the scripts

import os
import json
import pandas as pd
import psycopg2
import requests
from dotenv import load_dotenv
from pprint import pprint
from sqlalchemy import create_engine
import matplotlib.pyplot as plt


3. Example Steps
   EXTRACT
   load_dotenv() ## Load environment variables from a .env file
   
   API_KEY = os.getenv("API_KEY")
  API_HOST=os.getenv("API_HOST")
  COUNTRY = 'us'
  EMPLOYMENT_TYPE= 'fulltime'
    print(payload)

    CLEAN
cols_to_drop=[  "slug","url","dateDeleted",
    "company.slug","company.website","company.linkedinUrl",
    "company.linkedinSize","company.linkedinFounded",
    "company.linkedinTagline",
    "company.linkedinDescription","company.linkedinSpecialties","company.linkedinLocations"]

df.drop(columns=[c for c in cols_to_drop if c in df.columns],errors="ignore", inplace=True)
print("Dropped columns (if present).Remaining columns:",df.columns.tolist())


  LOAD TO POSTGRESQL



# KEY LEARNINGS

How to work with REST APIs in Python

Basic data wrangling and cleaning

Writing data into SQL databases

Structuring a small data project professionally


# AUTHOR

Author

Frank Ohene-Darkoh
📧 ohenedarkohfrank@gmail.com




