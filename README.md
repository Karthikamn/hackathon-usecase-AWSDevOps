**Overview**
Welcome to the DevOps Hackathon Challenge!
In this hackathon, you will demonstrate your skills in containerization, Infrastructure as Code (IaC), CI/CD automation, and cloud deployment using Amazon Web Services (AWS).
You will be working with a simple healthcare application consisting of two microservices, deployed in a cloud native, automated, and scalable AWS environment.
________________________________________
**Microservices**
You will work with two backend microservices:
1. Patient Service
2. Appointment Service
________________________________________
**CI Pipeline (GitHub Actions)**
Your CI pipeline should perform the following:
1.	Checkout code from GitHub
2.	Build microservices locally 
3.	Dockerize each microservice
4.	Create Kubernetes manifests (recommended: Helm charts – internal)
5.	Push Docker images to Amazon ECR

**CD Deployment**
Your CD pipeline should:
1.	Pull container images from Amazon ECR
2.	Deploy services to: 
Amazon EKS (Kubernetes)
OR
Amazon ECS (Fargate preferred)
3.	Support rolling or blue/green deployments
4.	Ensure zero downtime releases

**Secrets Management**
Secure handling of secrets is mandatory.

**Containerization**
1.	Containerize all microservices using Docker
2.	Use optimized and secure Dockerfiles
3.	Prefer multi stage builds where possible
4.	Ensure containers run as non root users
   
**Infrastructure as Code (Terraform)**
Set up a Terraform project structure supporting multiple environments:
     dev, staging, prod
Provision the following AWS resources using Terraform:
1.	VPC with public and private subnets across two availability zones
2.	Internet Gateway and NAT Gateway
3.	Security Groups and Network ACLs
4.	IAM roles and policies
5.	ECS / EKS cluster resources (based on chosen deployment model)
6.	Application Load Balancer
7.	Amazon ECR repositories

**GitHub Actions**
Create workflows for:
1.	CI/CD: Implement a CI/CD pipeline using GitHub Actions for your application code.
2.	Terraform fmt and validate on all PRs
3.	Terraform plan on pull requests
4.	Terraform apply on merges to main branch
