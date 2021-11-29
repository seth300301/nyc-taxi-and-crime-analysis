# Predicting the Amount of Taxi Pickups in NYC Zones (2019)
This project aims to depict the relationship between the number of taxi pickups and statistics of both crime and taxi trips happening within zones across the boroughs of New York City; the Bronx, Brooklyn, Manhattan, Queens, and Staten Island, and a “sixth borough”; the EWR Airport. This project attempts to predict the amount of taxi pickups of each zone from October to December in 2019 given the corresponding zone’s crime and taxi statistics from 2019’s first nine months, specifically studying yellow and green taxi trips. The crime statistics considered regard arrests, shootings, and complaints in each zone.

Please read 'Report.pdf' to read about my methods, analyses, findings, recommendations, and conclusions.

## Dependencies
- Language: Python 3.9.5
- Packages / Libraries: Please refer to `requirements.txt`
- Note: 'raw_data' folder was omitted due to its large size, you may form it following the steps below

## Datasets
- NYC TLC: https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page
    - Yellow and Green Taxi datasets for all of 2019
    - Rename each to following format: "color_month_2019.csv" e.g. "yellow_jan_2019.csv"
    - Place all in `raw_data`
- NYC TLC Shapefile: https://s3.amazonaws.com/nyc-tlc/misc/taxi_zones.zip
    - Download zip file and unpack
    - Create folder in `raw_data`, name it `taxi_zones`, and move all items in zip there.
- NYC TLC Zone Lookup Table: https://s3.amazonaws.com/nyc-tlc/misc/taxi+_zone_lookup.csv
    - Download zip file and unpack
    - Rename to "taxi_zones_lookup.csv"
    - Place in `taxi_zones`
- NYPD Arrests Data (Historic): https://data.cityofnewyork.us/Public-Safety/NYPD-Arrests-Data-Historic-/8h9b-rp9u/data
    - Filter with the following conditions before downloading:
        - ARREST_DATE before 12/31/2018
        - ARREST_DATE after 01/01/2020
    - Rename to "arrests_2019.csv"
    - Place in `raw_data`
- NYPD Shootings Data (Historic): https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8/data
    - Filter with the following conditions before downloading:
        - OCCUR_DATE before 12/31/2018
        - OCCUR_DATE after 01/01/2020
    - Rename to "shootings_2019.csv"
    - Place in `raw_data`
- NYPD Complaints Data (Historic): https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i/data
    - Filter with the following conditions before downloading:
        - RPT_DT before 12/31/2018
        - RPT_DT after 01/01/2020
    - Rename to "complaints_2019.csv"
    - Place in `raw_data`

## Directory
- `raw_data`: Files are too large to commit. Please refer to instructions for each dataset above to download required raw data.
- `preprocessed_data`: Contains all the preprocessed data files.
- `plots`: Contains all plots, figures, and folium htmls.
- `code`:
    - Notebook 1: Preprocessing Part 1 (had to separate due to memory allocation issues)
    - Notebook 2: Preprocessing Part 2
    - Notebook 3: Analysis, Visualisation, and Outlier Detection
    - Notebook 4: Statistical Modelling
- `requirements.txt`: Contains list of all libraries used on computer project was carried out on. 

## Other
- You may encounter a memory allocation issue in Notebook 1 if you are trying to reconduct the process depending on your device. Please close all other applications and windows to allow for optimal memory allocations.
