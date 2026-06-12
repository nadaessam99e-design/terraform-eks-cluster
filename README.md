# **🚀 Terraform EKS Cluster on AWS**

This project provisions a fully managed Kubernetes (EKS) cluster on AWS using Terraform.  
It includes networking (VPC), managed node groups, IAM roles, and secure cluster configuration.

---

## 📦 Project Overview

Using Terraform modules, this project creates:

- 🏗️ Custom VPC with public & private subnets
- ☸️ Amazon EKS Cluster (Kubernetes 1.29)
- 🖥️ Managed Node Group (EC2 worker nodes)
- 🔐 IAM Roles & Policies for EKS
- 🌐 Internet Gateway + NAT Gateway for private networking
- 🔑 Kubernetes access configured via AWS IAM

---

## 🧱 Architecture

- VPC: `10.0.0.0/16`
- Public Subnets: For load balancers / NAT
- Private Subnets: For worker nodes
- Region: `us-east-1`
- Node Type: `t3.medium`

---

## ⚙️ Prerequisites

Make sure you have:

- AWS CLI configured
- Terraform >= 1.5
- kubectl installed
- IAM user with EKS permissions

---

## 🚀 Deployment Steps

```bash
terraform init
terraform plan
terraform apply
🔗 Configure kubectl

After deployment:

aws eks update-kubeconfig --name my-eks-cluster --region us-east-1
kubectl get nodes
📁 Project Structure
.

├── main.tf

├── providers.tf

├── variables.tf

├── outputs.tf

└── README.md
🧹 Cleanup

To destroy resources:

terraform destroy
