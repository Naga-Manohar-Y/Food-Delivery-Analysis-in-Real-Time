# Real-Time Food Delivery Analytics Pipeline
This project implements a real-time data processing pipeline for food delivery orders, leveraging AWS services for efficient data ingestion, processing, storage, and analysis.

## Project Description

This pipeline addresses the need for real-time insights into food delivery operations. By capturing order data in real-time using AWS Kinesis, we process and transform it using PySpark Streaming on Amazon EMR. The processed data is then loaded into a star schema on Amazon Redshift for optimized storage and analytical querying. Finally, we visualize key metrics and trends using an interactive QuickSight dashboard. The project also incorporates a CI/CD pipeline built with AWS CodeBuild to ensure reliable and automated deployments.

## Architecture

The architecture consists of the following components:




## Key Features
Real-time Data Processing: Processes food delivery orders in real-time for immediate insights.
Scalable Architecture: Leverages AWS services for scalability and reliability.
Optimized Data Storage: Employs a star schema on Redshift for efficient data warehousing.
Interactive Dashboards: Provides real-time visualizations and insights through QuickSight.
Automated Deployment: Implements a CI/CD pipeline for streamlined deployments.
Orchestration: Utilizes Apache Airflow (MWAA) for pipeline management.

## Technologies Used
* **AWS Kinesis:** Used for real-time ingestion of food delivery order data.
* **Amazon EMR (Elastic MapReduce) with PySpark Streaming:** Processes and transforms the streaming data in real-time.
* **Amazon MWAA (Managed Workflows for Apache Airflow):** Orchestrates the data pipeline, including EMR job submissions and Redshift data loading.
* **Amazon Redshift:** Stores the processed data in a star schema for efficient analysis.
* **Amazon QuickSight:** Provides interactive dashboards for visualizing key metrics and trends.
* **AWS CodeBuild:** Implemented a CI/CD pipeline for automated builds and deployments.
* **SQL:** For querying and manipulating data in Redshift.
* **Python:** For PySpark and Airflow DAG development.

## Star Schema
The Redshift data warehouse utilizes a star schema, consisting of:

- Fact Table: Contains the core metrics, such as order ID, delivery time, and total amount.
- Dimension Tables: Provide context for the fact table, such as customer information, restaurant details, and delivery location.

## QuickSight Dashboard
The QuickSight dashboard provides insights into:
- Real-time order volume.
- Delivery time trends.
- Sales performance by restaurant and location.
- Customer behavior patterns.

## CI/CD Pipeline
The CI/CD pipeline automates the deployment process, including:
- Code building and testing.
- EMR job submission.
- Redshift schema updates.
- QuickSight dashboard updates.

## Getting Started
AWS Account: You will need an AWS account with the necessary permissions.
Infrastructure Setup: Deploy the required AWS resources using CloudFormation or Terraform.
Data Ingestion: Configure Kinesis to ingest food delivery order data.
EMR Configuration: Set up the PySpark Streaming job to process the data.
Airflow DAGs: Create Airflow DAGs to orchestrate the pipeline.
Redshift Schema: Define the star schema in Redshift.
QuickSight Dashboard: Build the dashboard to visualize the data.
CI/CD Setup: Configure AWS CodeBuild for automated deployments.

## Future Enhancements
Implement anomaly detection for delivery delays.
Integrate machine learning models for predictive analytics.
Add support for real-time location tracking.
Extend the dashboard with more advanced visualizations.
Add data quality checks and monitoring.
