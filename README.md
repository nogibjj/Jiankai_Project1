# Project 1

## Overview
This project build a microservice, command line tool that links to a big data system. Azure Databricks is used to operate data and handle queries.

## Setup
Use make to install required packages.
```bash
make
```
## Microsoft Azure and Databricks
The Databricks service is hold on Microsoft Azure. 

We need the following four secrests to connect and communicate with our Databrick cluster.
```DATABRICKS_HOST```
```DATABRICKS_HTTP_PATH```
```DATABRICKS_SERVER_HOSTNAME```
```DATABRICKS_TOKEN```


## Test Databricks Connections
We can run this line of code to see if Databricks is successfully connected and configured.
```
databricks clusters list --output JSON
```

## CLI interface
```click``` is used to build a CLI interface 
To execute default query:
```
python3 ./query.py cli-query
```

## Web Interface using FastAPI
```FastAPI``` to build a microservice that enables users to query in a RESTful way. Use the following command to start the service.

```
python3 ./fastapi-app.py
```
A simple welcome message will be displayed.

Add ```/query``` at the end of the url, the default query will be executed and the return value will be displayed.
