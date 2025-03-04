# AWS Cloud Practicitioner

## Definitions

| Term            	| Definition                                                                                                                                                                                                                                                                 	|
|-----------------	|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| IaaS          	| *Infrastructure as a Service*<br>A business model that offers IT infrastructure like compute, storage and network resources. You are responsible for deploying, maintaining and support your applications, meanwhile the cloud provider handles the physical infrastructure. 	|
| SaaS          	| *Software as a Service*<br>Customers pay for software products, typically on a subscription model.                                                                                                                                                                           	|
| PaaS          	| *Platform as a Service*<br>Manages hardware and software resources to develop applications. (Kubernetes)                                                                                                                                                                     	|
| Private Cloud 	| Cloud computing environment dedicated to a single organization.                                                                                                                                                                                                            	|
| Public Cloud  	| Computing resources provided by a third-party, allowing anyone to use or purchase resources over the internet.                                                                                                                                                             	|
| Hybrid Cloud  	| Integrated between a third-party provider and a company's internal IT infrastructure. Usually for performance benefits (local processing) and regulatory compliance.                                                                                                       	|

## Services

### Categories

* [Analytics](analytics.md)
* [Compute](compute.md)
* [Storage](storage.md)
* [Networking](networking.md)
* [Developer Tools](dev_tools.md)

### Advantages:

* High Availability
* Elasticity
* Agility
* Durability

## Regions

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

## Decoupling Applications

### Monolithic Apps
Identify dependencies between components

### Microservices
Less waiting between components

### Integrations

| AWS Service 	|               	|
|-------------	|---------------	|
| SQS         	| Queues        	|
| SNS         	| Notifications 	|
| Eventbridge 	| Events        	|

