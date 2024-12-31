# Data Engineering Resource
Data Engineering Foundations

Segmentation of tools
- Storage: Databases
- Processing Frameworks
- Automation: Scheduling

Processing Frameworks
- Data cleaning
- Data aggregation 
- Data clustering 
- Batch and stream processing
- Tools: Apache Spark, Hive, Flink and Kafka. 

Automation: Scheduling 
- Set up and manage workflows 
- Plan jobs with specific intervals
- Resolve dependency requirements of jobs
- Tools: Airflow, Oozie, Luigi 

Storage: Databases vs File System 
Databases
- effeciently organized 
- Offers functionalities like search, replication, indexing 

File system
- Less organized 
- Offers minimal features and functionality 

* Definition of Databases: Databases are large collections of data organized in efficient structures and formats designed to support rapid search and retrieval.
* Types of Data: There are three types of data:
    * Structured Data: Data organized in well-defined structures, like tables in relational databases (e.g., MySQL, PostgreSQL).
    * Semi-Structured Data: Data that doesn't follow the tabular structure but contains tags or markers (e.g., JSON).
    * Unstructured Data: Schema-less data like photographs or videos.
* SQL vs. NoSQL Databases:
    * SQL Databases: Relational databases with defined schemas and relationships (e.g., MySQL, PostgreSQL).
    * NoSQL Databases: Non-relational databases often used for unstructured data, with types like key-value stores (e.g., Redis) and document databases (e.g., MongoDB).

* Database Schema: Describes the structure and relationships between tables in a database. It includes defining properties such as primary keys and foreign keys.
* Primary and Foreign Keys: Primary keys uniquely identify each instance in a table, while foreign keys connect tables by referring to primary keys in other tables.
* Star Schema: Often used in data warehouses, it consists of a central fact table (e.g., orders) and several dimension tables (e.g., customer, restaurant, time, dish) to model large databases for analytical purposes.

Distributive computing":

* Importance of Distributed Computing: Essential for handling large datasets by splitting tasks into smaller subtasks and distributing them across multiple computers, which speeds up processing.
* Benefits: Increases processing power and reduces memory requirements by partitioning data across several machines, enhancing fault tolerance and cost efficiency.
* Practical Example: Calculating the average age of Olympic participants using multiple processing units to illustrate how tasks can be distributed and processed in parallel.


Data engineers transforms raw data into analytical data for data scientists 

"MapReduce and Hadoop":

* Hadoop: An ecosystem of open-source tools maintained by the Apache Software Foundation, used for storing, processing, and analyzing large datasets.
* HDFS (Hadoop Distributed File System): A distributed file system that stores data across multiple computers, essential for big data and parallel computing.
* MapReduce: A processing technique that splits tasks into subtasks, distributing them across several computers in a cluster. It was one of the first popular big data processing paradigms but has some limitations in terms of ease of use.

HDFS has being replaced by cloud storage like s3.


"Hive":

* Hive Overview: Hive is a layer on top of the Hadoop ecosystem that makes data from several sources queryable in a structured way using Hive SQL, an SQL-like interface.
* Data Extraction: Hive aids in the extraction part of the ETL data pipeline, allowing data extraction from databases and file systems that integrate with Hadoop.
* Ease of Use: Hive simplifies querying by transforming SQL-like queries into jobs that can operate on a cluster of computers using MapReduce algorithms, making it easier than writing MapReduce jobs directly.


"Spark":

* Purpose of Spark: Spark is a parallel computation framework designed to distribute data processing tasks between clusters of computers, addressing the limitations of MapReduce by keeping as much processing as possible in memory.
* Core Components: Spark uses a data structure called Resilient Distributed Datasets (RDDs) for distributed data, which supports transformations (e.g., filter, map) and actions (e.g., count, collect).
* Performance: Spark can be up to 100 times faster than Hadoop for large-scale data processing due to its in-memory processing capabilities.

"Airflow":

* Workflow Scheduling: Airflow is a workflow scheduling framework that orchestrates complex data pipelines, managing dependencies between tasks using Directed Acyclic Graphs (DAGs).
* DAGs: DAGs are used to visualize and manage task dependencies, ensuring tasks are executed in the correct order without cycles.
* Airflow's Origin and Use: Created by Airbnb and now maintained by Apache, Airflow allows developers to create and test DAGs using Python, making it a powerful tool for managing and scheduling data workflows.

"Sources of data extraction":

* Data Extraction: Involves extracting data from persistent storage into memory, which is necessary before transforming the data.
* Common Data Sources: These include plain text files (e.g., .csv, .tsv), JSON files, and web APIs.
* Databases: Data can be extracted from application databases, which are optimized for online transaction processing (OLTP), and analytical databases, optimized for online analytical processing (OLAP).

"Data extraction from a PostgreSQL database":

* Setting Up PostgreSQL Database: The video walks through the steps to start a PostgreSQL server, create a database, and create tables within the database.
* Data Import: It explains how to import data from CSV files into the PostgreSQL tables using the \copy command.
* Connecting with Python and Spark: The video demonstrates how to connect the PostgreSQL database with a Python script using PySpark, including setting up a SparkSession and reading data from the database into a DataFrame.




