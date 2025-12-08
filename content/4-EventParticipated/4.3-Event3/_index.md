---
title: "Event 3"
date: 2025-09-09
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Summary Report: "Workshop – Data Science on AWS"

### Event Overview

- **Event Name:** Workshop – Data Science on AWS  
- **Date:** October 16, 2025  
- **Role:** Attendee  
- **Format:** Hands-on workshop with guided labs  
- **Location:** FPT University, Thu Duc, Ho Chi Minh City, Viet Nam

This comprehensive workshop provided a complete walkthrough of an end-to-end data science workflow on AWS, from initial data ingestion and preparation through model training, evaluation, and deployment. The format combined focused lectures with hands-on guided labs, allowing participants to experiment directly in the AWS environment and gain practical experience with real services.

### Workshop Structure

The workshop was divided into several modules, each building on the previous one:

#### Module 1: Data Ingestion and Storage
- **Amazon S3 as a data lake foundation**: Understanding S3's role as the central storage for data science projects
- **Data organization**: Best practices for organizing data in S3 (raw, processed, curated layers)
- **Data formats**: Choosing between CSV, Parquet, JSON, and other formats for different use cases
- **S3 features for data science**: Versioning, lifecycle policies, and access controls
- **Hands-on lab**: Setting up an S3 bucket structure and uploading sample datasets

#### Module 2: Data Preparation and ETL
- **AWS Glue overview**: Serverless ETL service for data transformation
- **Glue Data Catalog**: Centralized metadata repository for data discovery
- **AWS Glue DataBrew**: Visual data preparation tool for cleaning and transforming data
- **ETL workflows**: Building data transformation pipelines
- **Data quality**: Identifying and handling missing values, duplicates, and outliers
- **Hands-on lab**: Creating a Glue job to transform raw data into a processed format

#### Module 3: Data Exploration and Analysis
- **Amazon Athena**: Serverless interactive query service for S3 data
- **SQL queries on S3**: Writing SQL queries against data stored in S3
- **Query optimization**: Partitioning strategies and cost optimization
- **Amazon Redshift**: Data warehousing for complex analytics
- **Redshift Spectrum**: Querying S3 data directly from Redshift
- **Hands-on lab**: Running exploratory queries on datasets using Athena

#### Module 4: Model Development with Amazon SageMaker
- **SageMaker Studio**: Integrated development environment for ML
- **SageMaker Notebooks**: Jupyter notebooks with pre-configured environments
- **Built-in algorithms**: Using SageMaker's pre-built algorithms for common ML tasks
- **Custom model training**: Training models using custom code and frameworks
- **Hyperparameter tuning**: Using SageMaker's automatic model tuning
- **Experiment tracking**: Managing and comparing different model experiments
- **Hands-on lab**: Building and training a machine learning model using SageMaker

#### Module 5: Model Deployment and Monitoring
- **Model deployment**: Deploying models as real-time endpoints
- **Batch inference**: Running predictions on large datasets
- **A/B testing**: Testing multiple model versions in production
- **Model monitoring**: Tracking model performance and data drift
- **Cost optimization**: Right-sizing endpoints and using Spot Instances
- **Hands-on lab**: Deploying a trained model and making predictions

### Detailed Technical Content

#### Data Lake Architecture
The workshop emphasized the importance of a well-designed data lake:
- **Raw layer**: Storing data exactly as received from source systems
- **Processed layer**: Cleaned and transformed data ready for analysis
- **Curated layer**: Business-ready datasets optimized for specific use cases
- **Benefits**: Data lineage, reproducibility, and flexibility for different analytics needs

#### AWS Glue Deep Dive
- **Crawlers**: Automatically discovering schema and creating table definitions
- **ETL jobs**: Writing transformation logic in Python or Scala
- **Job scheduling**: Using EventBridge to trigger ETL jobs
- **Cost optimization**: Understanding Glue pricing and optimizing job execution

#### SageMaker Capabilities
- **Managed infrastructure**: No need to provision or manage servers
- **Auto-scaling**: Automatically scaling training and inference resources
- **Spot Instances**: Using Spot Instances for cost-effective training
- **Model registry**: Versioning and managing model artifacts
- **Pipelines**: Building ML pipelines for automated workflows

#### Integration Patterns
- **End-to-end pipeline**: Connecting S3 → Glue → Athena → SageMaker
- **Event-driven workflows**: Using EventBridge to orchestrate data science workflows
- **CI/CD for ML**: Integrating ML workflows into DevOps practices
- **Monitoring and alerting**: Using CloudWatch for monitoring ML workloads

### Key Learnings

#### Data Science Workflow on AWS
- Understanding how different AWS services fit together in a complete data science project
- The importance of data organization and governance from the start
- How managed services reduce infrastructure management overhead

#### Best Practices
- **Data organization**: Separating raw, processed, and curated data layers
- **Reproducibility**: Using versioning and experiment tracking
- **Cost optimization**: Right-sizing resources and using appropriate instance types
- **Security**: Implementing proper access controls and encryption

#### Practical Skills
- Setting up a data lake architecture on S3
- Creating ETL jobs with AWS Glue
- Querying data with Athena
- Training models with SageMaker
- Deploying and monitoring models in production

### Personal Takeaways

#### Technical Understanding
- I gained a comprehensive understanding of what a complete data science pipeline on AWS looks like in practice
- The hands-on labs helped me feel confident using services like S3, Glue, Athena, and SageMaker together
- I understand how to design data architectures that support both analytics and machine learning

#### Workflow Insights
- The importance of thinking about the entire pipeline, not just model training
- How data preparation often takes more time than model development
- The value of managed services in allowing data scientists to focus on analysis rather than infrastructure

#### Future Applications
- This workshop inspired me to think about how to design reproducible experiments
- I learned better ways to organize datasets for future projects
- I understand how to structure data science projects for scalability and maintainability

#### Career Development
- The workshop reinforced my interest in data science and ML on AWS
- I see how data engineering and ML engineering skills complement each other
- I'm motivated to continue learning about advanced SageMaker features and MLOps practices

### Hands-On Experience

The workshop's hands-on format was particularly valuable. Working through actual labs helped me:
- Understand the practical steps involved in each phase of a data science project
- See how services integrate and work together
- Build confidence in using AWS console and services
- Learn from mistakes in a safe, guided environment

The combination of theory and practice made the concepts much more concrete and memorable than lecture-only sessions would have been.

### Event Experience

This workshop was one of the most practical and hands-on events I attended. The step-by-step approach, combined with real AWS services and actual datasets, made it feel like working on a real project rather than just learning theory.

The instructors were knowledgeable and helpful, providing guidance when we encountered issues and explaining the "why" behind best practices, not just the "how."

This workshop significantly improved my understanding of how to build production-ready data science solutions on AWS, and I'm excited to apply these learnings to future projects.

### Event Photos

_Add your event photos here_





