<h1 align="center">AWS Project 2</h1>


# Project Description: Data Protection, Governance, and Monitoring
* This project involves setting up a comprehensive data analytics platform using AWS services to manage the City of Vancouver’s animal control data. 
## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 2
* This project aims to design and implement a Data Analytics Platform (DAP) using Amazon Web Services (AWS) to Data Protection, Governance, and Monitoring
## Project Objective:
* Designing & Implementing DAP.
## Methodology:
* The process of providing Data Protection, Governance, and Monitoring for DAP designed as follows.
### 1. Data Protection
- To secure the data, multiple AWS services were used:
  - **S3 Bucket Policies**: Restricted access to the data to authorized users only.
  - **AWS KMS (Key Management Service)**: Enabled encryption using a symmetric key created through AWS KMS, ensuring all data stored in S3 buckets was encrypted.
  - **Data Replication**: Established backup procedures to replicate data across AWS regions, preventing data loss and ensuring disaster recovery
![Keys](https://github.com/user-attachments/assets/8df67627-e1bf-4e58-b5cf-a7520dac7910)
![replication rule](https://github.com/user-attachments/assets/277268ff-e59b-4634-8ff0-ce0dd9261463)
![S3 bucket](https://github.com/user-attachments/assets/d3ef2738-d090-494e-9ce8-eaddfe6e4028)


### 2. Data Governance
- To enhance data governance and secure data access, I set up a data pipeline using AWS Glue and S3. The pipeline begins with storing data in an S3 bucket and includes steps to detect sensitive information, such as personal data. It then evaluates the data quality to ensure integrity. A row-level transformation is applied to modify the data, followed by a conditional router that filters the data based on defined criteria. Unnecessary columns are removed by changing the schema, ensuring that only essential information is retained. 
![Dataprotection ETL 2023](https://github.com/user-attachments/assets/a8336c80-f224-4314-b3fd-618923a69f2e)
![Dataprotection ETL 2024](https://github.com/user-attachments/assets/705ac2d6-508e-4556-9f8d-50ac77dd5fc5)
![Screenshot 2024-09-14 153814](https://github.com/user-attachments/assets/429dd708-0b51-475c-80a6-40738c3c570c)
![Screenshot 2024-09-14 153832](https://github.com/user-attachments/assets/80f1ddda-2f75-4b22-a98d-418c06852b48)


### 3. Data Monitoring
- Monitoring data effectively is crucial for ensuring system health and keeping track of usage metrics. The screenshots show the use of Amazon CloudWatch to create custom dashboards, which aid in tracking and managing system performance.
 ![Alam](https://github.com/user-attachments/assets/da99a858-5709-443e-a284-5b23912e7c06)


- The CloudWatch dashboard, named "part2-parksrecreandpets-animalconinv-kalyan," includes:
* Estimated Charges: Displays a gauge indicating the current estimated costs.
* Number of Objects: Shows a graph tracking the count of objects over time.
* Bucket Size in Bytes: Illustrates the size of the bucket in bytes, providing insights into storage usage.
* Alam: An alarm named "animalcoinv-Alam-kalyan" is configured to monitor specific thresholds, such as the number of objects or estimated charges. When these thresholds are exceeded, an email alert is triggered, ensuring proactive monitoring.

![ETL Monitoring](https://github.com/user-attachments/assets/63f30d20-2d85-4cfd-868c-cfe06fededa9)


- AWS Glue job monitoring is depicted, summarizing job runs with details such as:
* Total Runs: Three jobs executed, with two successful and one failed.
* Run Success Rate: 67% success rate.
* Resource Usage: Visual representation of resource utilization over time.
- Lastly, the CloudTrail screenshot shows a trail named "part2-animalconinv-trail-kalyan" configured in the US East (N. Virginia) region, with logging enabled to track user activity and API usage.
![Screenshot 2024-09-14 154930](https://github.com/user-attachments/assets/8e466dd3-ebeb-40c3-a30b-9783402bface)

## AWS CloudTrail
The CloudTrail configuration includes a trail named "part2-animalconinv-trail-kalyan" in the US East (N. Virginia) region. Logging is enabled, capturing user activity and API usage for enhanced security and compliance.


