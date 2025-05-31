# mongodb_public_health_pipeline
## Introduction
This project involves the migration of a real-world public health survey dataset from a relational database strucutre into a NoSQL database (MongoDB). It showcases how document-based modeling can support dynamic and evolving health data, focusing on schema design, data integrity, and Python-based automation. 

## Dataset Overview
### CDC Behavioral Risk Factor Surveillance System (BRFSS), 2023
The  dataset chosen for this project is from the publicly available CDC Behavioral Risk Factor Surveillance System (BRFSS). This nationwide survey collects data on health-related risk behaviors, chronic health conditions, and preventive service use across the U.S.

- Over **430,000+ records**
- Covers demographics, general health, chronic disease, habits (smoking, exercise), and healthcare access
- Downloaded in **SAS Transport Format (XPT)** and transformed into tabular CSVs

[Explore the dataset source](https://www.cdc.gov/brfss/annual_data/annual_2023.html)

## Project Pipeline
This project transforms BRFSS relational data into a document-oriented schema using MongoDB.
Some features of this project include:

- CSV exports from SAS/XPT format
- Structured schema models for `patients`,  survey_responses`, and optional `visits`
- Python scripts to handle ETL (Extract, Transform, Load)
- Validation checks for referential integrity & data consistency

## Features & Tools
### Schema Modeling
* Designed MongoDB collections for:
  * `patients` - demographics, contact infO
  * `survey_responses` - BRFSS variables per participant
  * **(Optional) `visits`** 
 
## Python Automation
* Data generation using `Faker` + `Pandas`
* ETL pipeline using `PyMongo` and `Pandas`
* Custom scripts for:
    * Simulating data migration
    * Validating referntial integrity
    * Logging errors and inconsistencies
 
## Quality Control & Auditing
* Ensures:
  * No orphaned references
  * Field type consistency
  * Proper indexing (patientID, timestamp, etc)
 
## Project Motivation
I am using this project to explore scalable data management for public health/ biomedical research, with MongoDB as a tool for:
* Handling semi-structured survey data
* Adapting to evolving health metrics over time
* Building pipelines that align with clinic informatics and research data management practices.

## Tech Stack
* MongoDB - flexible NoSQL document store
* Python - data generation, migration scripts (`PyMongo`, `Pandas`, `Faker`)
* Pandas - preprocessing CSV data
* VS Code, Jupyter, MongoDB Compass

```
## Project Structure
|-- data/
|   |-- patients.csv
|   |-- visits.csv
|   |__ survey_responses.csv
|-- scripts/
|   |-- migrate_to_mongo.py
|   |--validate_data.py
|   |__ generate_mock_data.py
|-- mongo_schemas.md
|-- README.md
```

## Contact
Developed by Jacob Ketchum, aspiring health data engineer.
Connect with me on [LinkedIn](https://www.linkedin.com/in/jacobket/) or check out my other projects [here](https://github.com/jacobket)!
