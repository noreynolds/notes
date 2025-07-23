# Compute
## Exam Tips

* Pricing
* Scaling options
* ECS vs EKS
* Lambda default timeout 15s
* Lambda pricing

## Elastic Cloud Compute (EC2)

??? info "Things to Know"
    - [ ] Define EC2 & what it does
    - [ ] Know what instance types are for EC2/capabilities covered
        - Instance store: Ephemeral storage attached to the host. 
        - Elastic Block Storage: Persistent storage separate from host instance
    - [ ] Different EC2 purchase types
        - On-demand: pay by the second
        - Reserved: 1/3 year plans (All upfront/Partial upfront/None upfront)
        - Savings: commit to a level of usage of EC2/Fargate/Lambda for 1/3 years
        - Spot: Leverage unused EC2 capacity in a region for large discounts
        - Dedicated: Dedicated physical server
    - [ ] What an AMI is & does for EC2


* Scalable
* Can host applications or databases
* On-Demand capacity reservations
    * Uses: 
        * Business-critical events
        * Disaster recovery
        * Spiky, unreliable workloads
* Dedicated Host
    * Save licensing costs
    * For workloads that need dedicated physical servers

### Billing*

* On-Demand:
    * Pay by the hour or second
    * Uses:
        * Applications with short-term or unpredictable workloads that cannot be interrupted.
        * Application development/testing on EC2 for the first time.
        * **No upfront payment or long-term commitment**
* Savings Plan:
    * Up to 72% reduction from On-Demand pricing
    * Requires a commitment to consistent usage for 1 or 3 year terms.
    * Plans:
        * Compute Savings
        * EC2 Instance Savings
        * Amazon SageMaker Savings
    * Uses:
        * Committed and steady-state usage`
* Reserved Instances:
    * Similar savings to the Savings Plan
* Spot Instances:
    * Up to 90% reduction form On-Demand pricing
    * Uses:
        * Fault tolerant or stateless workloads
        * Apps with flexible start and end times

### Instance Types*

* General Purpose
* Compute Optimized
    * Best for compute bound applications that need high performance processors.
    * Uses:
        * Batch processing
        * Media transcoding
        * High performance web servers
        * Gaming servers
* Memory Optimized
    * Best for processing large data sets in memory
* Accelerated Computing
    * Uses hardware accelerates to perform functions
    * Uses:
        * Floating point number calculations
        * Graphics processing
        * Data pattern matching
* Storage Optimized
* HPC Optimized
    * High performance computing for large, complex simulations and deep learning workloads.

### Features
* Load Balancer
    * Classic
    * Gateway
    * App
    * Network
* Auto Scaling
    * Horizontal (Multiple AZs)
    * Vertical (More performant CPU/GPU)
* Compute Optimizer
    * Rightsizing
    * Recommendations for optimization

## AWS Lambda

??? info "Things To Know"
    - [ ] Define Lambda, difference from EC2/Beanstalk
        - Serverless compute.
    - [ ] Lambda usage pricing
        - Only pay for compute time used
    - [ ] Lambdas are essential for serverless approach

* Serverless
* Optimal for operations under 15 minutes

## Fargate
* Serverless compute engine. Works w/ EKS/ECS
* Optimal for operations over 15 minutes
* Event driven

## Outposts
* Fully managed on-premise solution

## Lightsail
* Easy to use virtual private server instances, containers, storage, databases, etc.
* Optimal for small projects
* Uses:
    * Blogs
    * Ecommerce
    * Personal websites
    * Small business applications

## Batch

Batch computing service that plans, schedules and runs containerized batch ML, simulation and analytics workloads.

## Wavelength

Run applications in AWS telco partners' data centers for low latency, data residency and resiliency.

## AWS Elastic Beanstalk

??? info "Things to Know"
    - [ ] What Elastic Beanstalk is & difference from EC2
        - PaaS offering. Upload code (zip) and deploy
    - [ ] Different capabilities it provides

## Products
| Service Name                                                                                                                                                                                                          	| Category                     	| Service description                                                                                 	|
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|------------------------------	|-----------------------------------------------------------------------------------------------------	|
| AWS Elastic Beanstalk - Run and manage web apps.                                                                                                                                                                      	| Instances (Virtual machines) 	| Easy-to-use service for deploying and scaling web applications and services                         	|
| Amazon Elastic Compute Cloud (EC2) - Secure and resizable compute capacity in the cloud. Launch applications when needed without upfront commitments.                                                                 	| Instances (virtual machines) 	| Secure and resizable compute capacity (virtual servers) in the cloud                                	|
| Amazon EC2 Spot - Take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices.                                                          	| Instances (virtual machines) 	| Run fault-tolerant workloads for up to 90% off                                                      	|
| Amazon EC2 Autoscaling - Maintain application availability and automatically add or remove EC2 instances according to conditions you define.                                                                          	| Instances (virtual machines) 	| Automatically add or remove compute capacity to meet changes in demand                              	|
| Amazon Lightsail - Virtual servers, storage, databases, and networking for a low, predictable price.                                                                                                                  	| Instances (virtual machines) 	| Easy-to-use cloud platform that offers you everything you need to build an application or website   	|
| AWS Batch - Run batch jobs at any scale.                                                                                                                                                                              	| Instances (virtual machines) 	| Fully managed batch processing at any scale                                                         	|
| AWS Parallel Computing Service-Easily run HPC workloads at virtually any scale.                                                                                                                                       	| Instances (virtual machines) 	| Managed service to run and scale High Performance Computing workloads                               	|
| Amazon Elastic Container Service (ECS) - Run and manage Docker containers.                                                                                                                                            	| Containers                   	| Highly secure, reliable, and scalable way to run containers                                         	|
| Amazon EKS Anywhere                                                                                                                                                                                                   	| Containers                   	| Run containers on customer-managed infrastructure                                                   	|
| Amazon Elastic Container Registry (ECR)                                                                                                                                                                               	| Containers                   	| Easily store, manage, and deploy container images                                                   	|
| Amazon Elastic Kubernetes Service (EKS) - Run managed Kubernetes on AWS                                                                                                                                               	| Containers                   	| Fully managed Kubernetes service                                                                    	|
| Amazon EKS Anywhere                                                                                                                                                                                                   	| Containers                   	| Create and operate Kubernetes clusters on your own infrastructure                                   	|
| AWS Fargate - Run containers without managing servers or clusters.                                                                                                                                                    	| Containers                   	| Serverless compute for containers                                                                   	|
| AWS App Runner - Production web applications at scale made easy for developers.                                                                                                                                       	| Containers                   	| Build and run containerized applications on a fully managed service                                 	|
| AWS Lambda - Run code without provisioning or managing servers.                                                                                                                                                       	| Serverless                   	| Run code without thinking about servers. Pay only for the compute time you consume                  	|
| AWS Outposts - Fully managed service that extends AWS infrastructure, AWS services, APIs, and tools to virtually any datacenter, co-location space, or on-premises facility for a truly consistent hybrid experience. 	| Edge and hybrid              	| Run AWS infrastructure and services on premises for a truly consistent hybrid experience            	|
| AWS Snow Family - The Snow Family, comprised of AWS Snowcone and AWS Snowball, offers a number of physical devices and capacity points with built-in computing capabilities.                                          	| Edge and hybrid              	| Collect and process data in rugged or disconnected edge environments                                	|
| AWS Wavelength - Build applications that deliver single-digit millisecond latencies to mobile devices and end-users                                                                                                   	| Edge and hybrid              	| Deliver ultra-low latency application for 5G devices                                                	|
| VMware Cloud on AWS - Build a hybrid cloud without custom hardware.                                                                                                                                                   	| Edge and hybrid              	| Preferred service for all vSphere workloads to rapidly extend and migrate to the cloud              	|
| AWS Local Zones - Easily run latency-sensitive portions of applications local to end-users and resources in a specific geography, delivering single-digit millisecond latency.                                        	| Edge and hybrid              	| Run latency sensitive applications closer to end-users                                              	|
| AWS Savings Plan - Flexible pricing model that provides savings of up to 72% on AWS compute usage                                                                                                                     	| Cost and capacity management 	| Flexible pricing model that provides savings of up to 72% on AWS compute usage                      	|
| AWS Compute Optimizer - Identify optimal AWS compute resources.                                                                                                                                                       	| Cost and capacity management 	| Recommends optimal AWS compute resources for your workloads to reduce costs and improve performance 	|
| EC2 Image Builder - Build and maintain secure images.                                                                                                                                                                 	| Cost and capacity management 	| Build and maintain secure Linux or Windows Server images                                            	|
| Elastic Load Balancing - Achieve fault tolerance for any application by ensuring scalability, performance, and security.                                                                                              	| Cost and capacity management 	| Automatically distribute incoming application traffic across multiple targets                       	|
