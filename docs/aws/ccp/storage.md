# Storage
|         Service Name         	|                                  Storage Type                                 	|                                                             Use Cases                                                             	|                                                           Benefits                                                           	|                               Pricing                               	| Notes 	|
|:----------------------------:	|:-----------------------------------------------------------------------------:	|:---------------------------------------------------------------------------------------------------------------------------------:	|:----------------------------------------------------------------------------------------------------------------------------:	|:-------------------------------------------------------------------:	|-------	|
| Simple Storage Solution (S3) 	| Object storage                                                                	| Data lakes, backups, archives                                                                                                     	| Stores exabytes,<br>Supports server/client-side encryption<br>Autoscaling, <br>high data durability                          	| Low price per performance                                           	|       	|
| Elastic File System          	| File storage                                                                  	| Mount file system onto AWS services (EC2/ECS/EKS)<br>Machine Learning<br>Share code, files securely<br>Content Management Systems 	| Serverless: No provisioning, maintenance<br>Up to petabytes of storage<br>GB/s of throughput<br>Backup w/ AWS Backup         	| Multi-AZ/Single-AZ offerings<br>No data transfer charges in same AZ 	|       	|
| FSx                          	| File Systems<br>(NetApp ONTAP,<br>OpenZFS,<br>Windows File Server,<br>Lustre) 	| Cloud migration<br>Machine Learning, Analytics<br>Media/Entertainment workloads                                                   	| Replicates data across AZs<br>Auto encrypts data at-rest (AWS KMS)<br>Low latency<br>Sync w/ on-premise for hybrid workloads 	|                                                                     	|       	|
| File Cache                   	| File Caching                                                                  	| Media Production<br>Compute intensive analytics<br>ML training                                                                    	| Hundreds of GB/s throughput<br>Unify on-premise/cloud data sources<br>S3 integration                                         	|                                                                     	|       	|
| Elastic Block Store          	| Block Storage                                                                 	| Mission critical, high perf, I/O intense apps<br>Relational/NoSQL dbs<br>Big data analytics                                       	| High performance & scability<br>Optimize storage & cost<br>Simple data protection w/ EBS Snapshots                           	|                                                                     	|       	|
| DataSync                     	| Data Migration                                                                	| Cloud migration<br>Migrate to S3 glacier (archiving)                                                                              	| Migrate w/ end-to-end security<br>Manage data movement workloads<br>Migrate file/object data                                 	|                                                                     	|       	|
| Snowball                     	| Data Migration                                                                	| Transfer data to physical devices, ship to AWS<br>Processing, analyzing data locally                                              	| Run workloads w/ little/no connectivity                                                                                      	|                                                                     	|       	|
| Storage Gateway              	| Hybrid Cloud Storage<br>(S3/Tape/Volume)                                      	| Hybrid cloud storage solution for on-premise apps                                                                                 	| Access to limitless cloud storage on-premise<br>Low latency data access                                                      	|                                                                     	|       	|
| Transfer Family              	| Managed File Transfer                                                         	| Modernize secure file transfers<br>Integrate business-to-business data                                                            	|                                                                                                                              	|                                                                     	|       	|
| Elastic Disaster Recovery    	| Disaster Recovery                                                             	| AWS region recovery<br>On-premise to AWS fallback                                                                                 	| Test, recover, fail back apps<br>Automate env configuration, clean up                                                        	|                                                                     	|       	|
| AWS Backup                   	| Disaster Recovery                                                             	| Hybrid data protection<br><br>Cloud backup                                                                                        	| Managed/automated data protection<br>Monitor/audit compliance policies                                                       	|                                                                     	|       	|

## S3
Durable, scalable, secure. Automatically distributes data across 3 AZs in a region.

Use versioning for backups (Accidental deletions).

Can be used to create data lakes

Strong read-after-write consistency. 

### Storage Classes

#### Standard
High throughput, low latency

#### Intelligent
Automatically moves data to the most cost-effective storage tier

#### Standard Infrequent
Accessed monthly, millisecond retrieval

#### Glacier
Archive for long-lived data

#### Tiers
* Instant Retrieval
* Flexible: Can take minutes to hours
* Deep: Can take up to 12 hours. Long archive

## FSx
Managed storage for different file systems like:

* Windows File Server
* OpenZFS
* NetApp ONTAP

## Elastic Disaster Recovery
Minimize downtime and data loss

## Elastic Block Store
Persistent storage after stopping EC2 instance

Offers snapshots

**IOPS**: Input/Output operations per second

### Volume Types


#### SSD batch
Fast, expensive, high OPs

#### General
NOTE: Maximum 16k IOPS

* gp3: 3K IOPS consistently, 125 MiB/s throughput, 20% lower pricing to gp2
* gp2: 3 IOPS/GB consistently, 250 MB/s throughput

#### Provisioned
* io2 (256k IOPS)
* io1 (64k IOPS)

#### HDD volumes
    
* Slow, cheap, throughput tasks
* st1: 40 MB/s per TB baseline throughput
* sc1: 12 MB/s per TB baseline throughput

## Storage Gateway
Access to cloud storage for on-premise applications

#### Gateway Types

##### S3 File Gateway
*Server Message Block* or *Network File System* based access to data in S3

##### Tape Gateway
Virtual tapes leading to backup applications for storage in S3/S3 Glacier

##### Volume Gateway
iSCSI block storage volumes to store in S3 or migrate to EBS

## AWS Backup
Managed service to automate data protection across AWS and hybrid workloads.

