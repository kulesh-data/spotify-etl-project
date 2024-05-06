# Spotify End-to-end ETL Project

### Introduction
In this project, we will build ETL (extract, Transform, Load) pipeline using the Spotify API on AWS. It will extract data from Spotify API about the top 50 Indian songs, transform into desired format and store into an AWS data store.

### Architecture
![Architecture Diagram](https://github.com/kulesh-data/spotify-etl-project/blob/main/Spotify-etl-project-architecture.jpeg)

### Dataset/API
This API contains information about music artist, albums and songs: [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used:
1. **S3 (Simple Storage Service):** Amazon S3 is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups and static website files.

2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use lambda to run code in response to events like changes in S3, DynamoDB or other AWS services.

3. **Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use CloudWatch to collect and track metrics, collect and monitor log files and set alarms.

4. **Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies data and infer schemas to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. You can use the Glue Data Catalog with other AWS services, such as Athena.

6. **Amazon Athena:** Athena is an interactive query service that makes it easy to analyze data in Amazon S3.You can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

### Install Packages:
'''

pip install pandas

pip install numpy

pip install spotipy

'''

### Project Execution Flow
Extract Data From Spotify API -> Lambda Trigger (every 1 day) -> Run Extract Code -> Store Raw Data -> Trigger Tranform Function -> Tranform Data and Load it -> Query using Athena


