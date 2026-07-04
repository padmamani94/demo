                                             AWS Three-Tier Django E-Commerce Application Deployment

A production-inspired deployment of a Django E-Commerce application on Amazon Web Services (AWS) using a secure three-tier architecture with Amazon VPC, Application Load Balancer, Auto Scaling Group, and PostgreSQL.

Overview :

This project demonstrates the deployment of a Django-based E-Commerce application in a highly available and scalable AWS environment. The solution follows a three-tier architecture, separating the presentation, application, and database layers to improve security, scalability, and maintainability.

The application servers are deployed in private subnets behind an Application Load Balancer (ALB), while the PostgreSQL database runs on a dedicated EC2 instance in a separate private subnet. The infrastructure is designed using Amazon VPC with public and private subnets, NAT Gateway, Internet Gateway, Launch Templates, and Auto Scaling Group.

Architecture:
                                                   Internet
                                                      │
                                                      ▼
                                          Application Load Balancer (ALB)
                                                Public Subnets
                                                      │
                                                      ▼
                                         Auto Scaling Group (EC2 Instances)
                                              Django Application Servers
                                                 Private Subnets
                                                      │
                                                      ▼
                                         PostgreSQL Database Server (EC2)
                                                Private Database Sub

Key Features:

Designed and deployed a secure three-tier AWS architecture.
Configured a custom Amazon VPC with public and private subnets.
Deployed Django application on Amazon EC2 instances.
Migrated the application database from SQLite to PostgreSQL.
Configured PostgreSQL on a dedicated EC2 database server.
Implemented Application Load Balancer for traffic distribution.
Configured Auto Scaling Group with Launch Templates.
Automated application deployment using EC2 User Data.
Configured secure communication using AWS Security Groups.
Used NAT Gateway to provide outbound internet access for private instances.
Configured Target Groups and Health Checks for application monitoring.
Verified secure connectivity between application and database servers.
 
AWS Services Used :

Amazon EC2
Amazon VPC
Application Load Balancer (ALB)
Auto Scaling Group (ASG)
Launch Templates
Internet Gateway
NAT Gateway
Route Tables
Security Groups
Elastic IP

Deployment Workflow :

Create a custom Amazon VPC.
Configure public and private subnets.
Create Internet Gateway and NAT Gateway.
Configure Route Tables.
Create Security Groups.
Launch PostgreSQL EC2 instance in a private subnet.
Configure PostgreSQL for remote access.
Launch Django application EC2 instance in a private subnet.
Install project dependencies.
Configure PostgreSQL database settings.
Run Django database migrations.
Create Launch Template with User Data.
Create Auto Scaling Group.
Configure Application Load Balancer.
Register instances with Target Group.
Verify application accessibility through the ALB DNS endpoint.

Security Architecture:

Application servers deployed in private subnets.
PostgreSQL database isolated in a dedicated private subnet.
Application Load Balancer deployed in public subnets.
Security Groups configured with least-privilege access.
Database accepts connections only from application servers.
Private instances access the internet through a NAT Gateway.

Scalability & Availability:

Application Load Balancer distributes incoming requests.
Auto Scaling Group automatically launches or terminates EC2 instances based on demand.
Deployment spans multiple Availability Zones to improve availability and resilience.
Health checks ensure traffic is routed only to healthy application instances.

Database Migration:

The application was successfully migrated from SQLite to PostgreSQL by:

Updating Django database configuration.
Installing the PostgreSQL adapter (psycopg2-binary).
Running Django migrations.
Verifying connectivity between application and database servers.

Learning Outcomes:

Through this project, I gained practical experience in:

AWS Networking (VPC, Subnets, Route Tables)
EC2 Instance Management
PostgreSQL Administration
Django Deployment
Application Load Balancer Configuration
Auto Scaling Group Implementation
EC2 User Data Automation
Security Group Design
Troubleshooting AWS Networking and Connectivity
Building Highly Available Cloud Architectures

Future Enhancements:

HTTPS using AWS Certificate Manager (ACM)
Amazon Route 53 Domain Integration
Amazon RDS for PostgreSQL
Docker Containerization
CI/CD Pipeline using Jenkins
Infrastructure as Code with Terraform
CloudWatch Monitoring and Alarms
AWS Systems Manager Session Manager
Amazon S3 for Static and Media Files

Author:
Padmavathi Mani

AWS | DevOps | Linux | Python | Django | PostgreSQL
