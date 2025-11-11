# AWS Terraform ALB Project

This project uses **Terraform** to deploy a complete AWS setup for a sample Spring Boot application.

## 🔧 Components Deployed
- 3 EC2 instances (running a Spring Boot JAR)
- Application Load Balancer (ALB)
- S3 bucket for the application JAR
- IAM role for EC2 with S3 access
- S3 bucket for application logs

## 🚀 How It Works
1. The **JAR** file is uploaded manually to the S3 bucket.
2. Terraform creates:
   - EC2 instances
   - ALB
   - S3 bucket for logs
   - IAM role for S3 read/write
3. The EC2 instances automatically download and run the JAR from S3 using user data.
4. The ALB exposes the app to the internet on port 80.

## 🧰 Terraform Commands
```bash
terraform init
terraform plan
terraform apply
```
Then open the ALB DNS name in your browser → `/hello` endpoint.

## 📂 Project Structure
```
aws-terraform-alb-project/
├── main.tf
├── .gitignore
└── README.md
```

## 🧑‍💻 Author
**Sudhin Swain**  
Cloud & DevOps Enthusiast
