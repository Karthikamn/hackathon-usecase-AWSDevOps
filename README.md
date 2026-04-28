**Overview**
Welcome to the DevOps Hackathon Challenge!
In this hackathon, you will demonstrate your skills in containerization, Infrastructure as Code (IaC), CI/CD automation, and cloud deployment using Amazon Web Services (AWS).
You will be working with a simple healthcare application consisting of two microservices, deployed in a cloud native, automated, and scalable AWS environment.
___________________________________________________________________________________________________________________________________________________________________________
**Microservices**
You will work with two backend microservices:
1. Patient Service (Node.js)
  •	Manages patient details
  •	REST APIs for CRUD operations
2. Appointment Service (Node.js)
_____________________________________________________________________________________________________________________________________________________________________________
**CI Pipeline (GitHub Actions)**
Your CI pipeline should perform the following:
•	Checkout code from GitHub
•	Build microservices locally 
  o	Node.js build (npm install, npm test)
  o	Java build (mvn clean package)
•	Dockerize each microservice
•	Create Kubernetes manifests (recommended: Helm charts – internal)
•	Push Docker images to Amazon ECR

**CD Deployment**
Your CD pipeline should:
•	Pull container images from Amazon ECR
•	Deploy services to: 
 o	Amazon EKS (Kubernetes)
 OR
 o	Amazon ECS (Fargate preferred)
•	Support rolling or blue/green deployments
•	Ensure zero downtime releases

**Secrets Management**
•	Secure handling of secrets is mandatory.
**Containerization**
•	Containerize all microservices using Docker
•	Use optimized and secure Dockerfiles
•	Prefer multi stage builds where possible
•	Ensure containers run as non root users
**Infrastructure as Code (Terraform)**
•	Set up a Terraform project structure supporting multiple environments:
 o	dev, staging, prod
•	Provision the following AWS resources using Terraform:
 o	VPC with public and private subnets across two availability zones
 o	Internet Gateway and NAT Gateway
 o	Security Groups and Network ACLs
 o	IAM roles and policies
 o	ECS / EKS cluster resources (based on chosen deployment model)
 o	Application Load Balancer
 o	Amazon ECR repositories

**GitHub Actions:**
Create workflows for:
1.	CI/CD: Implement a CI/CD pipeline using GitHub Actions for your application code.
2.	Terraform fmt and validate on all PRs
3.	Terraform plan on pull requests
4.	Terraform apply on merges to main branch



