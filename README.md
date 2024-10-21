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

## Tests (FILE PATHS VARIES BY OS! MAKE SURE TO PASTE FILEPATH ACCORDINGLY FOR CODE TO WORK!)

### 1. **Test JSON to CSV Conversion (`test_json_to_csv`)**
   - **Purpose**: Converts a JSON file (`Airports.json`) into a CSV file and verifies if the conversion is successful.
   - **Outcome**: Checks if the CSV file is created at the specified path.

### 2. **Test API Data Ingestion (`test_api_to_csv`)**
   - **Purpose**: Fetches data from a remote API, saves the JSON response to a file, and then converts it to CSV format.
   - **Outcome**: Verifies that the CSV file is correctly generated from the API data.

### 3. **Test Summarizing Data (`test_generate_summary`)**
   - **Purpose**: Summarizes the number of records and columns before and after transforming a CSV file (`New_Market_Tax_Credit_Eligible_Area_2015.csv`).
   - **Outcome**: Prints the summary (number of rows and columns) and checks if the column modification is correct after transformation.

### 4. **Test for Missing File Handling (`test_missing_file`)**
   - **Purpose**: Checks if the ETL pipeline handles missing files properly by attempting to load a non-existent CSV file.
   - **Outcome**: The test passes if a `FileNotFoundError` is raised as expected.

### 5. **Test for Unsupported Format Handling (`test_unsupported_format`)**
   - **Purpose**: Ensures that the pipeline raises an appropriate error when attempting to output data in an unsupported format (in this case, `xml`).
   - **Outcome**: The test passes if a `ValueError` is raised for the unsupported format.

### 6. **Test CSV to SQLite Conversion (`test_save_to_sqlite`)**
   - **Purpose**: Loads a CSV file (`US_Census_Tract_Area_2010.csv`), converts it to an SQLite database, and verifies that the data is written to the SQLite table.
   - **Outcome**: The test checks if the SQLite table is populated and contains records.

# Datasets

Below are the datasets we used in this project along with their respective links:

### 1. **Census Dataset**
   - **Description**: The Charlottesville Census dataset contains information about demographics within the area.
   - **Link**: [Census Dataset](https://opendata.charlottesville.org/datasets/63f965c73ddf46429befe1132f7f06e2_15/explore?location=38.040076%2C-78.485000%2C13.45)

### 2. **Market Tax Credit Eligible Area Dataset**
   - **Description**: This dataset contains information about areas eligible for the New Market Tax Credit in Charlottesville.
   - **Link**: [Market Tax Credit Eligible Area Dataset](https://opendata.charlottesville.org/datasets/f820db54f19e478bbcccce35916a5caa_41/explore?location=38.040098%2C-78.490850%2C12.86)

### 3. **NASA Meteorite Landings Dataset**
   - **Description**: This dataset includes information on meteorite landings worldwide, made available by NASA.
   - **Link**: [NASA Meteorite Landings Dataset](https://data.nasa.gov/api/views/gh4g-9sfh/rows.json?accessType=DOWNLOAD)

### 4. **Airports Dataset**
   - **Description**: A dataset containing information on airports across various locations.
   - **Link**: [Airports Dataset](https://catalog.data.gov/dataset/airports-5e97a)

### 5. **Popular Baby Names Dataset**
   - **Description**: This dataset contains information on the most popular baby names over the years.
   - **Link**: [Popular Baby Names Dataset](https://catalog.data.gov/dataset/popular-baby-names)


