# Company Merger Data Cleaning

## Project Overview
This notebook contains the data cleaning process for the company acquisitions dataset. The cleaning process transforms raw acquisition data into a structured format suitable for analysis.

## Data Cleaning Steps

### 1. Initial Data Loading
- Loaded raw data from `acquisitions_update_2021.csv`
- Initial dataset contained 10 columns including company information, acquisition details, and categorization

### 2. Missing Value Treatment
- Converted "-" entries to proper NULL values
- Analyzed missing value patterns using missingno visualization
- Made informed decisions about column retention based on missing value percentages

### 3. Column Modifications
#### Removed Columns
- Category (99.31% missing)
- Country (76.56% missing)
- Derived Products (72.30% missing)
- Acquisition Price (64.95% missing)

#### Date Processing
- Combined 'Acquisition Year' and 'Acquisition Month' into a single 'Acquisition Date' column
- Converted to proper datetime format

### 4. Final Dataset Structure
The cleaned dataset contains 1455 rows and 5 columns:
- ID (int64)
- Parent Company (object)
- Acquired Company (object)
- Business (object)
- Acquisition Date (datetime64[ns])

## Output
- Cleaned dataset saved as `acquisitions_cleaned.csv`
- All datetime values formatted as YYYY-MM-DD
- No index column included in the output file

## Dependencies
- pandas
- numpy
- matplotlib
- seaborn
- plotly.express
- missingno
- scikit-learn

## Usage