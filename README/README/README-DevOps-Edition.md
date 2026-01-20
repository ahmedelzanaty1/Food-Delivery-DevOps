# 🍅 TOMATO - Food Ordering Website (DevOps Edition)

This project is a Fork of the [Original TOMATO Project](https://github.com/Mshandev/Food-Delivery), enhanced with a full-scale DevOps lifecycle implementation. I have transformed this MERN stack application into a production-ready system using modern Infrastructure as Code (IaC) and CI/CD practices.

## 🚀 DevOps Stack & Tools

* **Cloud Provider:** AWS (EC2, VPC, Security Groups).
* **Infrastructure as Code:** Terraform (Modular setup for provisioning).
* **Configuration Management:** Ansible (Automated server hardening & Docker setup).
* **Containerization:** Docker & Docker Compose (Multi-stage builds for optimization).
* **CI/CD Pipeline:** GitHub Actions (Automated Build, Push to DockerHub, and Deploy to EC2).
* **OS:** Ubuntu Linux.

## 🛠️ Infrastructure Overview

### 1. Provisioning (Terraform)
- Automated the creation of AWS EC2 instances.
- Managed Security Groups and Networking components programmatically.

### 2. Configuration (Ansible)
- Automated the installation of Docker and Docker Compose.
- Managed user permissions and system updates without manual intervention.

### 3. Containerization
- Built optimized Docker images for **Frontend**, **Admin**, and **Backend**.
- Implemented **Multi-stage builds** to reduce image size (using Nginx for static serving).

### 4. CI/CD Workflow
- **Continuous Integration:** Every push triggers a build process, tagging images and pushing them to Docker Hub.
- **Continuous Deployment:** Seamlessly updates the application on the AWS server via SSH and Docker Compose.

## 🏁 How to Run
The infrastructure is fully automated. To replicate:
1. Initialize Terraform: `terraform init && terraform apply`
2. Run Ansible Playbook: `ansible-playbook setup-docker.yml`
3. Push code to GitHub to trigger the Deployment.
