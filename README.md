🚀 Terraform EKS Cluster on AWS

This project provisions a fully working Amazon EKS cluster using Terraform, including networking, compute, and Kubernetes access configuration.

📦 What This Project Creates

Using Infrastructure as Code (Terraform), this setup deploys:

🌐 VPC (public + private subnets across AZs)
⚙️ Amazon EKS Cluster (Kubernetes 1.29)
🖥️ Managed Node Group (EC2 worker nodes)
🔐 IAM roles and access configuration
🌍 Public API endpoint access for kubectl
📡 NAT Gateway for private subnet connectivity
🏗️ Architecture Overview
EKS Control Plane managed by AWS
Worker Nodes deployed in private subnets
NAT Gateway allows outbound internet access
kubectl access via public endpoint
🛠️ Tech Stack
Terraform
AWS (EKS, VPC, IAM, EC2)
Kubernetes
AWS CLI
kubectl
📁 Project Structure
.
├── main.tf

├── providers.tf

├── variables.tf (optional)

├── outputs.tf (optional)

└── README.md

🚀 How to Use

1. Initialize Terraform
terraform init
3. Review the plan
terraform plan
4. Apply infrastructure
terraform apply
🔗 Configure kubectl access

After cluster creation:

aws eks update-kubeconfig --name my-eks-cluster --region us-east-1
kubectl get nodes


State files are excluded via .gitignore
No sensitive credentials are stored in the repository
IAM access is controlled via access_entries
