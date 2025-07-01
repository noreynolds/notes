# Services

## Categories

* [Analytics](analytics.md)
* [Compute](compute.md)
* [Storage](storage.md)
* [Networking](networking.md)
* [Developer Tools](dev_tools.md)

## Advantages:

* High Availability
* Elasticity
* Agility
* Durability

## Cloudwatch vs Cloudtrail

In simplest terms, Cloudwatch provides logs and Cloudtrail allows tracking of account activity.

| Cloudwatch                            	| Cloudtrail                                     	|
|---------------------------------------	|------------------------------------------------	|
| Visibility to cloud resources & apps  	| Accountability for account actions             	|
| Dashboard for metrics                 	| Centralizes activity logs across regions in S3 	|
| Stores logs                           	| Track API activity in AWS                      	|
| Trigger events with Cloudwatch Alarms 	| Creates breadcrumbs for account activity       	|

### Cloudwatch with EC2

Application and instance metrics cannot be collected without a cloudwatch agent installed on the instance.

* Metrics with agent provides the following measures:
    * Free memory
    * Percentage of disc space used
    * Custom application metrics

### Exam

* Cloudwatch log groups have indefinite retainment by default
    * Take note, may cause potential unexpected costs
* Cloudwatch dashboards

# Regions

| Term              	| Definition                                                                                                                                	|
|-------------------	|-------------------------------------------------------------------------------------------------------------------------------------------	|
| Availability Zone 	| One or more discrete data centers in an AWS Region. All AZs in a region are within 100 miles of each other.                               	|
| Region            	| A physical location that represents a cluster of data centers. Regions are completely independent, have a minimum of three separate AZs.  	|
| Local Zones       	| An extension of a region that places AWS services closer to end-users. Beneficial for low-latency.                                        	|
| Outposts          	| Brings AWS services to nearly any data center or on-premise facility.                                                                     	|
| CloudFront POPs   	| *Point of Presence* a.k.a Edge Location<br>Caching mechanism in CloudFront                                                                	|

As of March 4, 2025, AWS has:

* 36 Regions
* 114 Availability Zones
* 700 CloudFront POPs
* 13 Regional edge caches
