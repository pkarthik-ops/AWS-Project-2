<h1 align="center">AWS Project 2</h1>


# Project Description: Data Protection, Governance, and Monitoring
* This project involves setting up a comprehensive data analytics platform using AWS services to manage the City of Vancouver’s animal control data. 
## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 2
* This project involves setting up a comprehensive data analytics platform using AWS services to manage  to give a better protection on data monitoring and enriching the City of Vancouver’s animal control data. 
## Project Objective:
* This project aims to design and implement a Data Analytics Platform (DAP) using Amazon Web Services (AWS) to Data Enriching, Data Protection, Governance, and Monitoring
## Methodology:
* The process of providing Data Enriching, Data Protection, Governance, and Monitoring for DAP designed as follows.
### 1. Data Enriching
- Data Enriching is the process of making raw data more valuable, effective or better which can be done by incorporating attributes from internal as well as external sources. Data mining is especially important in business as it is helpful for data analysis in the different sectors including marketing and business intelligence.

![Screenshot (81)](https://github.com/user-attachments/assets/e9e49c06-facd-426f-9330-acc5d2f2b60a)
- Data Enriching is the process of making raw data more valuable, effective or better which can be done by incorporating attributes from internal as well as external sources. Data mining is especially important in business as it is helpful for data analysis in the different sectors including marketing and business intelligence.
Figure: Database creation for Data Enriching.
![Screenshot (82)](https://github.com/user-attachments/assets/68d1039a-f757-4072-84f0-0ac5409e4722)

Figure: Crawler Creation for Data Enriching.  
![Screenshot (83)](https://github.com/user-attachments/assets/0e9ec639-095d-49ca-a6a4-b4f3c69f6478)
Figure: Athena for Serverless Interactive Analytics Services.
![Screenshot (84)](https://github.com/user-attachments/assets/1a8b57cd-6129-4db1-8883-eb6a52650a38)

### 2. Data Protection
- The main purpose of this phase was to maintain data security within the AWS S3 client environment. The following screenshots describe main security settings like Bucket Policies and Encryption, Replication that enhances the secure data management on the platform.

![Screenshot (85)](https://github.com/user-attachments/assets/16e17846-691e-440b-b42f-576348fb1161)


1. 	In this setup, a new key was created to create extra security measure using AWS Key Management Service (KMS). The NAME of the key created on AWS is “grp6-prt2-anmlcnvin-lstfnd-kms-karthik it is a SYMMETRIC type and is designed to perform the ENCRYPTION and DECRYPTION within the confines of the AWS. This key will serve a lot of importance in keeping secured the data placed in AWS S3.
The following screenshots show basic steps in setting up protection of an S3 bucket on AWS using encryption and replication capabilities.
2. Encryption: 
 	By default, the S3 bucket has server-side enforcement of encryption of data at rest with AWS Key Management Service (KMS). Data protection at rest is achieved with the help of an encryption key that KMS uses in order to encrypt data. The last figure in the right corner of the heading Illustrates that a KMS key (ARN) belongs to the bucket and show that the bucket key is enabled to minimize costs through minimizing Encryption requests to AWS KMS. It ensures protection of sensitive data, and addresses compliance standards.
![Screenshot (86)](https://github.com/user-attachments/assets/373a4314-6219-48a4-beab-df81c747d22e)

3.	Replication: 
 	They have set up a replication rule that would create an asynchronous copy of the objects from a source bucket to another different destination bucket within the same region of US East. Replication helps to make data copies, which leads to a feature known as high availability, and the overlapping also makes copies, and is termed as redundancy. It applies to the whole bucket, and replicating objects encrypted using SSE-KMS uses the same KMS key. Another advantage of replication is to produce a second copy of the data simply to use in case of disaster.
![Screenshot (87)](https://github.com/user-attachments/assets/923838da-3b33-4f14-b572-21b2aa4e6cb3)

4.	Versioning:
When enabled, S3 versioning enables the creation of many versions of an object within a single bucket in order to retain, recall, and restore each version of an object that replaced by or eliminated by other versions. When versioning is on, one can always get a previous version of the object despite the fact that it has been deleted or perhaps altered, which of course offers another extra layer of security to accidental data deletion or modification. This is especially true when several files must be edited now and then.
SSE-KMS besides replication and versioning increases the durability of data. When used together with replication, it makes not only the current versions of the objects stored in the bucket replicated to the destination bucket but also the previous versions of an object.
![Screenshot (88)](https://github.com/user-attachments/assets/5b815730-4a71-43cf-9982-a682cd3d4e6a)



### 3. Data Governance
- To achieve better data management and data availability I created a data pipeline with AWS Glue and S3. The pipeline starts with data accumulation in an S3 bucket and contains stages for the identification of, for instance, personal information. It then assesses the quality of the data thus improving on the quality of the data gathered for integrity. A row-level transformation is turned on to change the data then a conditional router filters the data according to set conditions. Specific columns not relevant for judgments are deleted by altering the scheme so that only relevant data is stored.
![Screenshot (89)](https://github.com/user-attachments/assets/69bb10c9-6279-4d90-93a3-73cd66b3d176)


Then, the processed data is transferred and stored in the Trusted folder in S3 for further use.
![Screenshot (90)](https://github.com/user-attachments/assets/e0ce4f3a-a329-472d-9b1f-55d94fe97b20)


### 4. Data Monitoring

- In general, the ability to monitor data adequately is important to determine system status and utilization rates. The examples of the screenshots imply use of Amazon CloudWatch to customize dashboard which in turn help in monitoring and controlling the performance of systems.

![Screenshot (91)](https://github.com/user-attachments/assets/4ab9937a-c026-4249-b5b9-7539f2ec5336)


-The CloudWatch dashboard, named " grp6-prt2-anmlcnvn-lstfnd-DAP_DASH-karthik" includes:
 •	Estimated Charges: Features a meter which shows the current estimates of costs.
 •	Number of Objects: Mostly contains a graph to describe the count of objects over time.
 •	Bucket Size in Bytes: It clears an understanding to depict the size of the bucket in byte so that it will be convenient to mention about the storage usage.
 •	Alam: An alarm named “grp6-prt2-anmlcnvn-lstfnd-alarm-karthik” is raised for certain limit like number of objects or even estimated charges. This means that beyond the limits, the system has a capacity to send an email alert to encourage active monitoring.

![Screenshot (92)](https://github.com/user-attachments/assets/56cc2017-6b0e-4c61-b118-3b432b488a65)



- Additionally, AWS Glue job monitoring is depicted, summarizing job runs with details such as:
•	Total Runs: One job executed, with One successful run.
•	Run Success Rate: 100% success rate.
•	Resource Usage: The graphical display of resource use over time for the purpose of identification and analysis.

