The organization managed patient data from multiple EHR systems, stored in different formats (JSON, CSV, and XML), making it difficult to perform unified analysis or meet compliance requirements (e.g., HIPAA). 
Manual data integration processes were error-prone and time-consuming, delaying decision-making.

Solution
Data Extraction:

Used AWS S3 as a centralized data lake to store raw files from EHR systems.
Automated ingestion of data using AWS Glue Crawlers to classify the data schema.
Data Transformation:

Developed a transformation pipeline in Python to clean and standardize data into FHIR-compliant resources (e.g., Patient, Observation, MedicationRequest).
Applied data validation rules (e.g., ensuring ICD-10 and RxNorm codes were consistent across datasets).
Data Loading:

Leveraged AWS Glue Jobs to load transformed data into Snowflake for analysis.
Configured Snowflake auto-clustering and time travel for optimal query performance and historical data access.
Real-Time Analytics:

Implemented a change data capture (CDC) mechanism using AWS Glue and Snowflake to enable near real-time updates for dashboards and reports.
