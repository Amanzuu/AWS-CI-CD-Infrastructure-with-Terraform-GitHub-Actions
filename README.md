# 🚀 AWS CI/CD Infrastructure with Terraform & GitHub Actions

An end-to-end DevOps project that automates infrastructure provisioning and application deployment on AWS using Terraform and GitHub Actions.

---

## 📌 Project Overview

This project demonstrates a **production-style CI/CD pipeline** where:

- Infrastructure is provisioned using **Terraform**
- Deployment is automated using **GitHub Actions**
- Application is deployed to EC2 instances using **AWS Systems Manager (SSM)**
- Traffic is distributed via an **Application Load Balancer (ALB)**

---

## 🏗️ Architecture

User → ALB → Auto Scaling Group → EC2 Instances → Nginx Web Server

---

## ⚙️ Tech Stack

- **Cloud**: AWS (EC2, ALB, Auto Scaling, VPC, IAM, SSM)
- **IaC**: Terraform
- **CI/CD**: GitHub Actions
- **Web Server**: Nginx
- **Version Control**: Git & GitHub

---

## 🔄 CI/CD Workflow

1. Developer pushes code to GitHub
2. GitHub Actions pipeline is triggered
3. Terraform initializes and applies infrastructure changes
4. Instance IDs are fetched dynamically
5. AWS SSM executes deployment commands on all EC2 instances
6. Nginx serves updated application via ALB

---

## 🔐 Security Features

- No SSH access required (SSM used instead)
- IAM roles used for secure access
- GitHub Secrets for AWS credentials

---

## 🌐 Features

- ⚡ Automated Infrastructure Provisioning
- 🔁 Load Balancing across multiple instances
- 🔄 Auto Scaling enabled
- 🚫 No manual server access required
- 🎯 Dynamic UI showing instance hostname
- 🎨 Animated deployment dashboard

---

## 📸 Demo

- Access the application via ALB DNS
- Refresh page to observe load balancing across instances

---

## 🚧 Challenges Faced

- Handling JSON escaping in CI/CD pipelines
- Passing correct instance IDs to SSM
- Debugging Terraform resource conflicts
- Fixing encoding issues in HTML deployment

---

## 🧠 Key Learnings

- Real-world CI/CD pipeline design
- Infrastructure as Code (IaC) best practices
- Secure AWS resource management
- Debugging cloud-based deployments
- Automating deployments without SSH

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/AWS-Infrastructure-with-Terraform.git
cd AWS-Infrastructure-with-Terraform
2. Initialize Terraform
terraform init
3. Apply Infrastructure
terraform apply
4. Push code to trigger CI/CD
git add .
git commit -m "trigger pipeline"
git push origin main
🧹 Cleanup

To destroy all resources:

terraform destroy
📈 Future Improvements
Dockerize application
Deploy using ECS/EKS
Add monitoring (CloudWatch / Prometheus / Grafana)
Implement Blue-Green Deployment
Add HTTPS with ACM
🙌 Author

Aman Dhalla
