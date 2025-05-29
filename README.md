# mongodb_public_health_pipeline
## Introduction
This project simulates the migration of a commmunity health survey dataset from a relational database strucutre into MongoDB, showcasing the flexibility of document-based data modeling for healthcare workflows. It's designed to reflect real-world public health and clinical data use cases, with a focus on data integrity, schema design, and python-based automation. 

## Project Overview
The fictional dataset mimics responses from a community health survey involving patient demographics, visit records, and self-reported health metrics. The project simulates:
* A relational-style data source (CSV tables)
* A fully document-oriented schema in MongoDB
* Python scripts to migrate, validate, and audit the data
* Modular design for future expansion (e.g. visualization, analysis)

## Features & Tools
### Schema Modeling
* Designed MongoDB collections for:
  * `patients` (demographics, contact info)
  * `visits` (linked records of clinic visits)
  * `survey_responses` (structured health survey responses)
 
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
