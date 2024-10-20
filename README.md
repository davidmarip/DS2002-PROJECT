# DS2002 - ETL data processor by Brynn Hill and David Nu

## Project Overview
This project focuses on developing a segment of an Extract, Transform, and Load (ETL) pipeline. The pipeline is designed to ingest and process raw data from various sources, transform the data as required, and output it to various formats.

## Features
- **Data Ingestion**: Supports ingesting data from local files or via URLs (or API calls).
- **Data Transformation**: Capable of converting data between formats such as JSON to CSV, CSV to JSON, and loading JSON data into a SQL database.
- **Column Modification**: Allows modifications to the data structure by adding or removing columns.
- **Data Storage**: Outputs transformed data to disk or writes directly to a SQL database.
- **Data Summary**: Generates summaries pre and post data processing to provide insights into data structure changes.

## Dependencies

This notebook requires the following Python packages:

- **Pandas**: For data manipulation and conversion.
- **Requests**: For fetching data from remote URLs.
- **SQLite3**: For database operations. Included in Python's standard library.
- **JSON**: For parsing and generating JSON formatted data. Included in Python's standard library.
- **OS**: For file and directory operations.
