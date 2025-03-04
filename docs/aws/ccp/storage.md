# Storage
## S3
Durable, scalable, secure

Can be used to create data lakes

#### Storage Classes

###### Standard
High throughput, low latency

###### Intelligent
Automatically moves data to the most cost-effective storage tier

###### Standard Infrequent
Accessed monthly, millisecond retrieval

###### Glacier
Archive for long-lived data

######## Tiers
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

#### Volume Types


###### SSD batch
Fast, expensive, high OPs

######## General
Maximum 16k IOPS

* gp3: 3K IOPS consistently, 125 MiB/s throughput, 20% lower pricing to gp2
* gp2: 3 IOPS/GB consistently, 250 MB/s throughput

######## Provisioned
* io2 (256k IOPS)
* io1 (64k IOPS)

###### HDD volumes
    
* Slow, cheap, throughput tasks
* st1: 40 MB/s per TB baseline throughput
* sc1: 12 MB/s per TB baseline throughput

## Storage Gateway
Access to cloud storage for on-premise applications

#### Gateway Types

###### S3 File Gateway
*Server Message Block* or *Network File System* based access to data in S3

###### Tape Gateway
Virtual tapes leading to backup applications for storage in S3/S3 Glacier

###### Volume Gateway
iSCSI block storage volumes to store in S3 or migrate to EBS

## AWS Backup
Managed service to automate data protection across AWS and hybrid workloads.

