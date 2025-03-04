# Exam Tips

* Pricing
* Scaling options
* ECS vs EKS
* Lambda default timeout 15s

# Elastic Cloud Compute (EC2)

* Scalable
* Can host applications or databases
* On-Demand capacity reservations
    * Uses: 
        * Business-critical events
        * Disaster recovery
* Dedicated Host
    * Save licensing costs
    * For workloads that need dedicated physical servers

## Billing

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
* Reversed Instances:
    * Similar savings to the Savings Plan
* Spot Instances:
    * Up to 90% reduction form On-Demand pricing
    * Uses:
        * Fault tolerant or stateless workloads
        * Apps with flexible start and end times

## Instance Types

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

## Features
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

# AWS Lambda
* Serverless
* Optimal for operations under 15 minutes

# Fargate
* Optimal for operations over 15 minutes
* Event driven

# Outposts
* Fully managed on-premise solution

# Lightsail
* Easy to use virtual private server instances, containers, storage, databases, etc.
* Optimal for small projects
* Uses:
    * Blogs
    * Ecommerce
    * Personal websites
    * Small business applications

# Batch

Batch computing service that plans, schedules and runs containerized batch ML, simulation and analytics workloads.

# Wavelength

Run applications in AWS telco partners' data centers for low latency, data residency and resiliency.

