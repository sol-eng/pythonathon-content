# FastAPI

This demo serves two purposes:

* Explore using ODBC connections from Python via `pyodbc`
* Build out an example FastAPI API and deploy it to RStudio Connect

## Outline
* Data is pulled from [this API](https://dev.socrata.com/foundry/data.seattle.gov/4xy5-26gy) and includes details about bikes crossign teh Fremont Bridge in Seattle.
* The data is initially loaded into the database using a Jupyter notebook
* A separate Jupyter notebook is published RStudio Connect to perform periodic updates of the data stored in the DB
* A FastAPI is built to provide a way of querying the underlying data in the DB

## ODBC
Snowflake is used for the backend of the ODBC piece.

## FastAPI
