# aws-cloud-projects-portfolio

# Nomeer Sheikh | AWS Cloud Architecting & Implementation Portfolio ☁️

Welcome to my AWS portfolio! This repository contains documentation, architecture diagrams, and implementation details for various hands-on cloud projects I have completed. 

These projects demonstrate my practical ability to design, deploy, secure, and troubleshoot scalable infrastructure on Amazon Web Services (AWS).

### 🏆 Certifications
* **AWS Certified Cloud Practitioner (Foundational)**
https://www.credly.com/badges/cf87de1f-27ce-4d4f-9be6-e1ed3f74deff/public_url

## 🛠️ Technologies & Services Used
* **Compute & Scaling:** Amazon EC2, Auto Scaling Groups, Launch Templates, Application Load Balancer (ALB)
* **Storage:** Amazon S3, Amazon EBS, Amazon EFS
* **Databases:** Amazon RDS (Multi-AZ, Read Replicas), Amazon DynamoDB
* **Networking & Content Delivery:** Amazon VPC, Subnets, Route Tables, Internet Gateways, VPC Peering, Amazon Route 53, Amazon CloudFront
* **Security & Identity:** IAM (Users, Groups, Policies, Least Privilege), Security Groups
* **Management & Monitoring:** Amazon CloudWatch, AWS Systems Manager, AWS Pricing Calculator

---

## 📂 Project Directory

### 1. Troubleshoot an AWS Cloud Architecture
* **Objective:** Audited and resolved issues within a complex, multi-tier cloud architecture to ensure proper functionality and security.
* **Implementation:** Added a secondary application server to an Application Load Balancer (ALB), updated Security Groups for secure App-to-Database interaction, and set up an Amazon S3 bucket for static website hosting.
* **Database & Security Optimization:** Created an Amazon RDS reader instance to reduce write latency, developed a DynamoDB table for user session data, and granted specific user access to DynamoDB via IAM group attachments.

### 2. Highly Available Web Applications
* **Objective:** Deployed a resilient web application across multiple Availability Zones to guarantee uptime.
* **Implementation:** Configured an Auto Scaling group to utilize an Application Load Balancer (ALB) and established strict load balancer health checks.
* **Scaling:** Expanded the infrastructure by adding a third Availability Zone to the Auto Scaling group to further distribute traffic and eliminate single points of failure.

### 3. Connecting VPCs (Network Peering)
* **Objective:** Enabled secure, internal communication between isolated departmental networks.
* **Implementation:** Configured VPC Peering connections between separate Marketing, Finance, and Developer VPCs.
* **Routing:** Updated custom route tables to ensure traffic was successfully and securely routed between the peered VPCs without traversing the public internet.

### 4. Auto-Healing and Scaling Applications
* **Objective:** Implemented infrastructure that automatically adjusts capacity to maintain performance and optimize costs.
* **Implementation:** Created Amazon EC2 Auto Scaling groups using custom Amazon Machine Images (AMIs) and Launch Templates. Integrated CloudWatch alarms to monitor workloads.
* **Cost Optimization:** Configured a scheduled scaling policy to automatically scale the environment down to 0 resources during off-hours (01:00 AM daily).

### 5. Networking Concepts (VPC Architecture)
* **Objective:** Configured core networking components to enable secure internet connectivity and isolate backend resources.
* **Implementation:** Built a custom VPC with public and private subnets, configured an Internet Gateway, and set up Route Tables. Restricted inbound access by specifically allowing traffic over port 3306 to isolated database servers.

### 6. Databases in Practice (Amazon RDS)
* **Objective:** Migrated to Amazon RDS to automate database administration and improve performance.
* **Implementation:** Deployed a Multi-AZ RDS instance with automated backups and created a read replica using a `db.t3.xlarge` instance to offload read traffic.

### 7. First NoSQL Database (Amazon DynamoDB)
* **Objective:** Implemented a highly performant NoSQL database to store and process dynamic viewer behavior data.
* **Implementation:** Provisioned an Amazon DynamoDB table with a dynamic schema, creating custom records with specific numeric attributes (e.g., `rating`) to query device analytics.

### 8. File Systems in the Cloud (Amazon EFS)
* **Objective:** Provided a fully managed, scalable file system accessible across multiple server locations.
* **Implementation:** Launched Amazon EFS, configured mount targets across three Availability Zones, and successfully mounted the file system to multiple EC2 instances simultaneously to share logs.

### 9. Core Security Concepts (IAM & Least Privilege)
* **Objective:** Implemented strict access control using the principle of least privilege.
* **Implementation:** Created an IAM "SupportEngineers" Group and attached AWS managed policies to grant explicit, read-only access to Amazon RDS while restricting other permissions.

### 10. Cloud Computing Essentials (S3 Static Hosting)
* **Objective:** Improved website reliability by migrating web assets to cloud storage.
* **Implementation:** Enabled static website hosting on an Amazon S3 bucket and authored custom S3 bucket policies to securely host public-facing content.

### 11. Cloud First Steps (EC2 & Multi-AZ)
* **Objective:** Deployed a highly available stabilization system using compute instances.
* **Implementation:** Launched multiple Amazon EC2 instances with attached EBS volumes across different Availability Zones to ensure high availability.

### 12. Computing Solutions (EC2 Vertical Scaling)
* **Objective:** Scaled up application performance by modifying compute resources.
* **Implementation:** Explored instance attributes and successfully changed an EC2 instance type from a micro instance to a larger, general-purpose instance (`m4.large`).

### 13. Cloud Economics (Cost Estimation)
* **Objective:** Analyzed and optimized infrastructure costs for a varying demand architecture.
* **Implementation:** Created logical pricing groups and generated specific price estimates for elastic cloud resources using the AWS Pricing Calculator.
