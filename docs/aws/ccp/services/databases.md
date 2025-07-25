# Databases

## Relational

### Aurora
High performance for MySQL, PostgreSQL and DSQL.

Up to 5x throughput of MySQL and 3x throughput of PostgreSQL.

### RDS
Easy-to-manage service for total cost of ownership. Automates provisioning, configuring, backing up and patching. Eight engines, two deployment options and numerous features to optimize performance.

#### Backup and Restoration

* Automated Backups
    * Enabled by default, can be customized through `CreateDBInstance` API.*
    * Performs a full daily backup, and applies changes from the transaction log to restore to the specific time requested.
    * Retains backups for 7 days by default, but can be set to 35 days.
    * Stored in S3
* Database Snapshots
    * User initiated
    * Can be created within AWS management console, CreateDBSnapshot API, create-db-snapshot commands.

Automated backups can be copied with `copy-db-snapshot` command.

If an instance is deleted, a final DB snapshot is made if the user decides to restore the instance later.

#### Security

All logs, backups and snapshots are encrypted in an encrypted DB instance.

Supports encryption at rest for all DB engines. Uses keys from KMS (Key Management Service). 

Encryption can be added to an unencrypted DB instance:

1. Create a DB snapshot
2. Create a copy of the snapshot and specify a KMS encryption key.
3. Restore an encrypted DB instance from the encrypted snapshot.


### Redshift
SQL data warehousing service. 3x better price-performance and 7x better throughput than other cloud warehousing offerings. Seamless integration with SageMaker Lakehouse to perform analysis across Redshift, S3 data lakes, databases and federated data sources.

## Key-Value

### DynamoDB
Serverless NoSQL database service that has no cold starts, version upgrades, maintenance windows, patching or downtime maintenance. Offers DynamoDB streams for event-driven applications.

Maximum allowed item size: 400 KB.

Full encryption of user data in transit (SSL) and at rest (AES-256, KMS key).

## In-memory

### ElastiCache
Fully managed Valkey/Memcached/Redis OSS-compatible service. Consider this service when caching with an existing primary database/data store.

### MemoryDB
Valkey/Redis OSS-compatible in-memory database. For workloads that require a fast primary database. 

## Document

### DocumentDB (MongoDB compatible)
JSON document database.

## Graph

### Neptune
Serverless graph daatbase. 

## Wide Column

### Keyspaces
Apache Cassandra compatible database service. Serverless, managed and data is encrypted by default.

## Time Series

### Timestream
Fully managed time-series database.

## Products
| Database type                                                                                                                                                                                                                                 	| Examples                                                                                                                                                                                                                                             	| AWS service                                                                                         	|
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|-----------------------------------------------------------------------------------------------------	|
| Relational<br>Relational databases store data with predefined schemas and relationships between them. These databases are designed to support ACID transactions, and maintain referential integrity and strong data consistency.              	| Traditional applications, enterprise resource planning (ERP), customer relationship management (CRM), ecommerce, generative AI use cases (such as chatbots with Retrieval Augmented Generation, similarity search, recommendation systems, and more) 	| Amazon Aurora<br>Amazon RDS<br>Amazon Redshift                                                      	|
| Key-value<br>Key-value databases are optimized for common access patterns, typically to store and retrieve large volumes of data. These databases deliver quick response times, even in extreme volumes of concurrent requests.               	| High-traffic web applications, ecommerce systems, gaming applications, generative AI use cases (such as similarity search using DynamoDB zero-ETL integration with Amazon OpenSearch Service)                                                        	| Amazon DynamoDB                                                                                     	|
| In-memory<br>In-memory databases are used for applications that require real-time access to data. By storing data directly in memory, these databases deliver microsecond latency to applications for whom millisecond latency is not enough. 	| Caching, session management, gaming leaderboards, geospatial applications, generative AI use cases (such as chatbots with Retrieval Augmented Generation, semantic caching, recommendation systems, fraud detection, and more)                       	| Amazon ElastiCache<br>Amazon MemoryDB                                                               	|
| Document<br>A document database is designed to store semistructured data as JSON-like documents. These databases help developers build and update applications quickly.                                                                       	| Content management, catalogs, user profiles, generative AI use cases (such as chatbots with Retrieval Augmented Generation, similarity search, recommendation systems, and more)                                                                     	| Amazon DocumentDB (with MongoDB compatibility)                                                      	|
| Graph<br>Graph databases are for applications that need to navigate and query millions of relationships between highly connected graph datasets with millisecond latency at large scale.                                                      	| Fraud detection, social networking, recommendation engines, generative AI use cases (such as GraphRAG, enhanced fraud detection, discovery of new answers, and more)                                                                                 	| Amazon Neptune                                                                                      	|
| Wide column<br>A wide column store is a type of NoSQL database. It uses tables, rows, and columns, but unlike a relational database, the names and format of the columns can vary from row to row in the same table.                          	| High-scale industrial apps for equipment maintenance, fleet management, and route optimization                                                                                                                                                       	| Amazon Keyspaces                                                                                    	|
| Time series<br>Time-series databases efficiently collect, synthesize, and derive insights from data that changes over time and with queries spanning time intervals.                                                                          	| Internet of Things (IoT) applications, DevOps, industrial telemetry                                                                                                                                                                                  	| Amazon Timestream                                                                                   	|
| Amazon Elastic Container Service (ECS) - Run and manage Docker containers.                                                                                                                                                                    	| Containers                                                                                                                                                                                                                                           	| Highly secure, reliable, and scalable way to run containers                                         	|
| Amazon EKS Anywhere                                                                                                                                                                                                                           	| Containers                                                                                                                                                                                                                                           	| Run containers on customer-managed infrastructure                                                   	|
| Amazon Elastic Container Registry (ECR)                                                                                                                                                                                                       	| Containers                                                                                                                                                                                                                                           	| Easily store, manage, and deploy container images                                                   	|
| Amazon Elastic Kubernetes Service (EKS) - Run managed Kubernetes on AWS                                                                                                                                                                       	| Containers                                                                                                                                                                                                                                           	| Fully managed Kubernetes service                                                                    	|
| Amazon EKS Anywhere                                                                                                                                                                                                                           	| Containers                                                                                                                                                                                                                                           	| Create and operate Kubernetes clusters on your own infrastructure                                   	|
| AWS Fargate - Run containers without managing servers or clusters.                                                                                                                                                                            	| Containers                                                                                                                                                                                                                                           	| Serverless compute for containers                                                                   	|
| AWS App Runner - Production web applications at scale made easy for developers.                                                                                                                                                               	| Containers                                                                                                                                                                                                                                           	| Build and run containerized applications on a fully managed service                                 	|
| AWS Lambda - Run code without provisioning or managing servers.                                                                                                                                                                               	| Serverless                                                                                                                                                                                                                                           	| Run code without thinking about servers. Pay only for the compute time you consume                  	|
| AWS Outposts - Fully managed service that extends AWS infrastructure, AWS services, APIs, and tools to virtually any datacenter, co-location space, or on-premises facility for a truly consistent hybrid experience.                         	| Edge and hybrid                                                                                                                                                                                                                                      	| Run AWS infrastructure and services on premises for a truly consistent hybrid experience            	|
| AWS Snow Family - The Snow Family, comprised of AWS Snowcone and AWS Snowball, offers a number of physical devices and capacity points with built-in computing capabilities.                                                                  	| Edge and hybrid                                                                                                                                                                                                                                      	| Collect and process data in rugged or disconnected edge environments                                	|
| AWS Wavelength - Build applications that deliver single-digit millisecond latencies to mobile devices and end-users                                                                                                                           	| Edge and hybrid                                                                                                                                                                                                                                      	| Deliver ultra-low latency application for 5G devices                                                	|
| VMware Cloud on AWS - Build a hybrid cloud without custom hardware.                                                                                                                                                                           	| Edge and hybrid                                                                                                                                                                                                                                      	| Preferred service for all vSphere workloads to rapidly extend and migrate to the cloud              	|
| AWS Local Zones - Easily run latency-sensitive portions of applications local to end-users and resources in a specific geography, delivering single-digit millisecond latency.                                                                	| Edge and hybrid                                                                                                                                                                                                                                      	| Run latency sensitive applications closer to end-users                                              	|
| AWS Savings Plan - Flexible pricing model that provides savings of up to 72% on AWS compute usage                                                                                                                                             	| Cost and capacity management                                                                                                                                                                                                                         	| Flexible pricing model that provides savings of up to 72% on AWS compute usage                      	|
| AWS Compute Optimizer - Identify optimal AWS compute resources.                                                                                                                                                                               	| Cost and capacity management                                                                                                                                                                                                                         	| Recommends optimal AWS compute resources for your workloads to reduce costs and improve performance 	|
| EC2 Image Builder - Build and maintain secure images.                                                                                                                                                                                         	| Cost and capacity management                                                                                                                                                                                                                         	| Build and maintain secure Linux or Windows Server images                                            	|
| Elastic Load Balancing - Achieve fault tolerance for any application by ensuring scalability, performance, and security.                                                                                                                      	| Cost and capacity management                                                                                                                                                                                                                         	| Automatically distribute incoming application traffic across multiple targets                       	|
