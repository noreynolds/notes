# AWS Cloud Practitioner

## Checklist
- [ ] EC2 instances and plans
- [ ] Cloud Adoption Framework
- [ ] Less popular services (Appsync, Polly, Kafka, Xray)
- [ ] Note differences between similar services
- [ ] EC2/RDS responsibilites (Who takes care of what?)
- [ ] Learn about security within AWS
- [ ] CIDR/Subnet Masks/IP Address

## Quick Notes

* [1/10/25 | Practice Exam](exam_01_10_2025.md)
* [3/19/25 | Practice Exam](exam_03_19_2025.md)

## Topics

* [Cloud Adoption Framework](caf.md)
* [Well-Architected Framwork](waf.md)
* [Services](services.md)
* [Databases](databases.md)

## Definitions

| Term            	| Definition                                                                                                                                                                                                                                                                 	|
|-----------------	|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| IaaS          	| *Infrastructure as a Service*<br>A business model that offers IT infrastructure like compute, storage and network resources. You are responsible for deploying, maintaining and support your applications, meanwhile the cloud provider handles the physical infrastructure. 	|
| SaaS          	| *Software as a Service*<br>Customers pay for software products, typically on a subscription model.                                                                                                                                                                           	|
| PaaS          	| *Platform as a Service*<br>Manages hardware and software resources to develop applications. (Kubernetes)                                                                                                                                                                     	|
| Private Cloud 	| Cloud computing environment dedicated to a single organization.                                                                                                                                                                                                            	|
| Public Cloud  	| Computing resources provided by a third-party, allowing anyone to use or purchase resources over the internet.                                                                                                                                                             	|
| Hybrid Cloud  	| Integrated between a third-party provider and a company's internal IT infrastructure. Usually for performance benefits (local processing) and regulatory compliance.                                                                                                       	|


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

## Managing AWS Resources

* Use tags to sort and visualize resources

### Systems Manager
Centrally view, manage and operate AWS, on-premise and multicloud resources. Allows for automation and viewing of aggregated data on resource groups. Offered in the systems manager is `Parameter Store`, a tool for managing configuration data dn secrets management. It can store passwords, database strings, AMI IDs and license codes in plain text or encrypted formats.

### Managing Service Health
Use AWS Health Dashboard to monitor the status of AWS services. Can also be accessed through the AWS Health API.

#### Trusted Advisor
A support tool that inspects your AWS environment to offer recommendations to save money, improve system availability, improve performance or close security gaps. On the Basic/Developer support plan, it checks for service limits and some security measures.

Basic/Developer checks:
* Any open security groups?
* Are you using IAM users?
* Is MFA enabled on the root account?
* Are services near resource limits?
* EBS Public Snapshots
* RDS Public Snapshots
* S3 Bucket Permissions

## AWS Auditing
Continuous checks to guarantee compliance.

Monitors: 
* Data encryption in transit and at rest
* Secure cloudtrail
* Resources with public access
* Resources configuration and provisioning are up to standards
* Network security
* Credentials

### AWS Config
Provides insight into the configuration of AWS resources. Detects and alerts against pre-defined recommendations for auditing or security measures. Custom rules can also be applied, but any enforcement must be done through IAM.
