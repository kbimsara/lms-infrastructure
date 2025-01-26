# Library Management System Infrastructure

AWS-based cloud infrastructure for a scalable library management system.

## Architecture Overview
- VPC with public/private subnets
- Auto Scaling EC2 instances (t2.micro)
- RDS MySQL database
- Application Load Balancer
- S3 storage
- Lambda for notifications
- CloudWatch monitoring

## Prerequisites
- AWS Account
- Terraform installed
- AWS CLI configured

## Deployment
1. Clone repository
```bash
git clone [repository-url]
cd LMS-infrastructure
```

2. Initialize Terraform
```bash
terraform init
```

3. Set DB password in GitHub Secrets:
- TF_VAR_db_password

4. Deploy infrastructure
```bash
terraform apply
```

## Infrastructure Components
- VPC (10.0.0.0/16)
  - Public Subnet: 10.0.1.0/24
  - Private Subnet: 10.0.2.0/24
- EC2: t2.micro instances
- RDS: db.t3.micro MySQL 8.0
- Lambda: Node.js 18.x

## Clean Up
```bash
terraform destroy
```

## Project Structure
```
LMS-infrastructure/
├── terraform/
│   ├── main.tf
│   └── notification.zip
└── README.md
```