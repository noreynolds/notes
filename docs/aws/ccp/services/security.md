# Security, Identity, Compliance

## Identity Access Management
Service to securely control access to AWS resources.


### Best Practices
* Require multi-factor authentication (MFA)
* Protect root user credentials
* Apply least-privilege permissions
* Use IAM Access Analyzer to validate IAM policies.

### Terms
Root User: The central identity created with your AWS account. Should not be used for every day tasks, and secured with MFA.

IAM user: Specific permissions for a single person or application.

IAM role: Identity with specific permissions. Similar to a user but not associated with a specific person.

IAM group: A collection of IAM users. Allows for specific permissions of multiple users.

Principals: An AWS account root user, IAM user, IAM role that can make a request for an action or operation on an AWS resource.
Human users are recommended to be Federated, meaning another identity provider like Active Directory or Okta is being used.

## Amazon Inspector
Automated vulnerability management service for software vulnerabilities and unintended network exposure.

### Support Services
* EC2
* Lambda 
* ECR
* CI/CD tools


### Features
* Centrally manage software bill of materials
* Automate workflows/ticket routing with AWS Security Hub and Amazon EventBridge
* AWS Organizations integration
