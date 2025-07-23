# Networking

## Checklist
- Understand the purpose of:
    - [ ] Amazon Route 53
        - Global service, Domain Name System (DNS), domain name registration
    - [ ] Amazon Virtual Private Cloud (VPC)
    - [ ] AWS Direct Connect
        - Service for data center -> AWS connection
    - [ ] Amazon API Gateway
        - API management service
    - [ ] Amazon Cloudfront
    - [ ] Elastic Load Balancing
        - Application Load Balancer
        - Network Load Balancer 
        - Classic Load Balancer
- Under cloud scaling approaches:
    - [ ] Vertical Scaling (scale up/upgrade instance style)
    - [ ] Horizontal Scaling (scale out/additional instances)
        - Can be managed through Elastic Load Balancing

## CloudFront
CDN

Uses AWS edge locations to deliver

### Uses
* Streaming videos
* Secure transactions
* Traffic spikes
* Analytics
* Static/dynamic content

## Global Accelerator

### Uses
* Global traffic manager
* API acceleration
* Global static IP
* Low-latency gaming/media workloads

## Virtual Private Cloud
A logically isolated virtual network defined by the user. Closely resembles a traditional network in a data center. 

### Uses
* Hybrid connections
* Host multi-tier web applications

### Features
* Public/private subnet
* Route table
    * Determine where network traffic from the subnet/gateway is directed.
* Gateway
    * Connect VPC to another network (ex: Internet). 
* NACL (Network Access Control List)
    * Rules to determine network traffic by allowing or denying access to specific resources (IP addresses, protocols, ports).
* DNS (Route 53)
* Direct Connect (Hybrid Connections)
    * Large scale data transfer, consistent performance, good for sensitive data
* VPN
