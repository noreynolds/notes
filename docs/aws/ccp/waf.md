# AWS Well Architected Framework

## General Notes
* Stop guessing capacity needs
* Test systems at production scale
* Consider evolutionary architectures
* Drive architecture through data
* Review architecture often, but not intensely (think hours, not days)
* Apply reviews early in the design phase

## Operational Excellence
The ability to support development and run workloads effectively, gain insight into their operations and to continuously improve supported processes and procedures.

### Design Principles
* Organize -> Prepare -> Operate -> Resolve
* Organize teams around business outcomes
* Implement observability for actionable insights
* Automate where possible
* Perform small, frequent, reversible changes
* Anticipate failure

## Security
Take advantage of cloud technologies to protect data, systems and assets to improve security.

### Design Principles
* Maintain traceacility
* Automate security best practices
* Protect data in transit and at rest
* Prepare for security events
* How do you protect compute and network resources?

## Reliability
The ability of a workload to perform its intended function correctly and when it's supposed to. Includes the ability to operate and test workload through it's lifecycle.

### Design Principles
* Automatically recover from failure
* Test recovery procedures
* Replace one large resource with multiple small resources
* Stop guessing capacity
* Manage change through automation (tracing, monitoring, etc.)
* How do you backup data?

## Performance Efficiency
use computing resources efficiently to meet system requirements and maintain that when demand grows.


### Design Principles
* Democratize advanced technology (Use vendor solutions when you can)
* Go global in minutes
* Consider serverless implementations
* Experiment more often

## Cost Optimization
Run systems to deliver business value at a low cost.

### Design Principles
* Invest in cloud financial management
* Adopt a consumption model (Shut down dev/test during off hours)
* Measure overall efficiency
* Analyze and attribute expenditure

## Sustainability
Continually improve sustainability impacts by reducing energy consumption, increase efficiency from provisioned resources and minimizing resources required.

### Design Principles
* Understand your impact (metrics)
* Establish sustainability goals (reduce compute/storage per transaction)
* Anticipate or adopt new hardware or software solutions
* Utilize managed services
* Test with device farms to understand impacts

