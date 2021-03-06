# MedSal (SQL) & Enhydris (Timeseries) Database command line client

This project provides the connection and tools to query the [database](https://www.uhydro.de/medsaldba/) and the [enhydris](http://enhydris.de/) for the [MedSal](https://medsal.eu/) project on salinization of critical groundwater reserves in coastal Mediterranean areas: Identification, Risk Assessment, and Sustainable Management with the use of integrated modeling and smart ICT tools.

The MEDSAL Project aims to secure the availability and quality of groundwater reserves in Mediterranean coastal areas, which are amongst the most vulnerable regions in the world to water scarcity and quality degradation. 

## MedSal (SQL) Database

The database is designed in MySQL ans is available on the [web](https://www.uhydro.de/medsaldba/). Nevertherless, a set up is designed to query the database with Python enabling the extraction of data directly into dataframes, for further processing of the data.

The database consists of the following entities with data from Rhodope (Greece), Salento (Italy) and Samos (Greece) (more data will be uploaded):

* Climatic_data
* Gauging_characteristics
* Geochemical
* ICPMS_and_ASS_data
* Isotopes
* Lithostratigraphic_data
* Pumping_test_data
* Rainfall_data
* Runoff_data
* Soil_data_physicochemical
* Stage_data
* Well_chemical_analysis
* Well_data
* XRD_Mineralogy
* XRF_Geochemical
* borehole
* characteristics

### Functions

* Print all entities and their attributes

* Query the database in raw sql commands 

* Export queried data to a Pandas dataframe

* Export queried data to a csv file at the working directory

## Enhydris (Timeseries) Database

Enhydris is an open-source database system that stores and manages hydrological and 
meteorological data. Data can be raw, processed time series, model parameters and curves. It can also enable the storage of metadata, such as measurement instruments, events etc. The database is accessible through a web interface where data can be queried spatially. A map indicates the location of the station, while under each station one or more sensors are stored.

### Functions

* Print all stations and their attributes

* Query the database in Python

* Export queried data to a Pandas dataframe

* Export queried data to a csv file at the working directory



## Scripts


You can either open the [Jupyter notebook](Connect_and_query_the_MedSal_database.ipynb) or run the [script](medsal_db.py) as following:

```
python2 medsal_db.py
```

### Requirements:

#### Jupyter Notebook

`Connect_and_query_the_MedSal_database.ipynb` was developed using Python 3.8.6 on Ubuntu 20.04.1 LTS (Focal Fossa).

#### Script

`medsal_db.py` was developed using Python 2.7.16 on Debian 10.7 (buster).

#### Google Colab

Access and use the notebook online via [Google Colab](https://colab.research.google.com/drive/15pGMyIJjjsWgmheDL7A_uYIMxwlXUeg-?usp=sharing).

It has been tested with the following package versions:

* mysql-connector-python == 8.0.23

* pandas == 0.24.2   

* SQLAlchemy == 1.2.18

To install them run in a shell:

```
pip install -r requirements.txt
```




