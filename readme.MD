## AWS Microservices Infrastructure Platform (Terraform + EKS)

#### 📌 Overview

This repository provisions a complete AWS cloud infrastructure for hosting a production‑grade microservices application using Terraform, Amazon EKS, and Jenkins‑based CI/CD. It follows modular Infrastructure‑as‑Code principles, ensuring scalability, repeatability, security, and operational efficiency.

#### Repository Structure
**
    ├── 00-vpc/ # Custom VPC, Subnets, Internet/NAT Gateways, Route Tables
    ├── 10-sg/ # Security Groups for nodes, load balancers, and bastion
    ├── 20-bastion/ # Bastion host for secured cluster access
    ├── 30-ecr/ # Elastic Container Registry for application images
    ├── 40-iam/ # IAM roles, OIDC providers, instance profiles
    ├── 60-acm/ # SSL Certificates for secure ingress via ACM
    ├── 70-frontend-alb/ # Application Load Balancer for public ingress
    ├── 80-eks/ # Amazon EKS cluster, managed node groups, add‑ons
    └── README.md # Documentation **

#### 🏗️ Architecture Summary

* Custom VPC with public & private subnets across AZs
* Amazon EKS cluster with managed node groups
* Public Application Load Balancer with SSL (ACM)
* Elastic Container Registry
* Bastion host for privileged cluster access
* IAM roles for service accounts (IRSA)
* Security Groups aligned with least privilege