# UK Food Standards Agency Data Analysis

This repository contains code and data for analyzing food hygiene ratings data from the UK Food Standards Agency. The analysis includes data import, database setup, data cleaning, and exploratory analysis.

## Part 1: Database Setup

### Importing Data
To set up the database and import the data, follow these steps:
1. Open a terminal.
2. Navigate to the project directory.
3. Run the following command to import the data:
   ```shell
   mongoimport --type json -d uk_food -c establishments --drop --jsonArray /Users/edrinngadze/Documents/GitHub/nosql-challenge/Starter_Code/Resources/establishments.json

## Deliverables

### 1. NoSQL Database Setup (`NoSQL_setup_starter.ipynb`)
In this Jupyter Notebook, we have:
- Imported and set up a MongoDB database named `uk_food`.
- Created a collection within the database called `establishments`.
- Loaded data from `establishments.json` into the MongoDB collection.
- Executed several data manipulation operations to prepare the dataset for analysis, such as changing data types and verifying data integrity.

### 2. NoSQL Data Analysis (`NoSQL_analysis_starter.ipynb`)
This Jupyter Notebook contains:
- Comprehensive analysis of the food establishment data.
- Implementation of MongoDB queries to answer key business questions such as:
  - Identifying establishments with specific hygiene scores.
  - Analyzing the distribution of establishments across different local authorities.
  - Finding top-rated establishments based on various criteria.

## Key Findings and Insights

Through the analysis of the UK Food Standards Agency data, several important insights were revealed:

1. **Hygiene Score Analysis:**
   - A query identified 41 establishments with a hygiene score of 20, highlighting a critical need for improved hygiene standards in these locations. The example of "The Chase Rest Home" in Eastbourne with extremely poor hygiene scores indicates potential health risks.

2. **Establishments in London:**
   - An analysis of establishments in London revealed 33 locations with a `RatingValue` of 4 or higher, suggesting a generally high standard of hygiene in the area. An example includes "Charlie's" in the City of London Corporation.

3. **Proximity Analysis around Penang Flavours:**
   - A proximity search identified the top 5 establishments with a `RatingValue` of 5 near "Penang Flavours," sorted by the lowest hygiene score. This analysis aids in understanding the competitive landscape and hygiene standards in the vicinity of Penang Flavours.

4. **Local Authority Hygiene Score Analysis:**
   - A detailed breakdown of establishments with a hygiene score of 0 in each Local Authority area was conducted. The top three local authorities with the highest number of such establishments were Thanet (1130), Greenwich (882), and Maidstone (713). This information is crucial for local authorities to target hygiene inspections and interventions.

5. **Dataframe Creation and Analysis:**
   - Dataframes were created to facilitate the analysis of the extracted data, allowing for a detailed and structured review of the findings. For example, the dataframe containing London establishments provided insights into hygiene ratings within the city.

These findings offer valuable insights for stakeholders in the food industry, health and safety inspectors, and policymakers to understand the landscape of food hygiene standards and to take necessary actions for improvements.


## Technologies Used
- MongoDB
- Python
  - Libraries: `pymongo`, `pandas`

