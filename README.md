# DevOps Commands Repository

## Overview

This repository contains important DevOps commands, notes, and practical references used in real-world DevOps workflows.

The main purpose of this repository is to:
- Maintain all commonly used DevOps commands in one place
- Help beginners learn DevOps tools faster
- Provide quick command references
- Build a strong DevOps knowledge base

This repository includes commands and concepts related to:

- Linux
- Git & GitHub
- Docker
- Kubernetes
- Jenkins
- AWS
- Terraform
- Ansible
- CI/CD
- Shell Scripting
- Monitoring Tools

---

# Repository Structure

```bash
DevOps-Commands/
│
├── Linux/
│   ├── basic_commands.md
│   ├── file_permissions.md
│
├── Git_GitHub/
│   ├── git_commands.md
│   ├── github_workflow.md
│
├── Docker/
│   ├── docker_commands.md
│   ├── dockerfile_notes.md
│
├── Kubernetes/
│   ├── kubectl_commands.md
│   ├── pods_services.md
│
├── Jenkins/
│   ├── pipeline_commands.md
│   ├── cicd_notes.md
│
├── AWS/
│   ├── ec2_commands.md
│   ├── s3_commands.md
│
├── Terraform/
│   ├── terraform_commands.md
│
├── Ansible/
│   ├── ansible_commands.md
│
├── Monitoring/
│   ├── prometheus.md
│   ├── grafana.md
│
└── README.md
```

---

# Topics Covered

---

# 1. Linux Commands

Contains:
- File handling commands
- Directory operations
- User management
- Permissions
- Networking commands
- Process management

Example:

```bash
ls
pwd
mkdir
chmod
top
ps
```

---

# 2. Git & GitHub Commands

Includes:
- Git initialization
- Clone repositories
- Commit changes
- Push and pull
- Branch management

Example:

```bash
git init
git clone
git add .
git commit -m "message"
git push
```

---

# 3. Docker Commands

Covers:
- Docker images
- Containers
- Dockerfile
- Docker Compose

Example:

```bash
docker build
docker run
docker ps
docker images
```

---

# 4. Kubernetes Commands

Includes:
- Pod management
- Services
- Deployments
- Scaling
- Namespace management

Example:

```bash
kubectl get pods
kubectl apply -f deployment.yml
kubectl describe pod
```

---

# 5. Jenkins Commands & CI/CD

Contains:
- Jenkins pipeline concepts
- CI/CD workflow
- Pipeline stages
- Jenkinsfile examples

Example:

```groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
    }
}
```

---

# 6. AWS Commands

Includes:
- EC2
- S3
- IAM
- Cloud concepts

Example:

```bash
aws s3 ls
aws ec2 describe-instances
```

---

# 7. Terraform Commands

Infrastructure as Code (IaC) commands.

Example:

```bash
terraform init
terraform plan
terraform apply
terraform destroy
```

---

# 8. Ansible Commands

Automation and configuration management.

Example:

```bash
ansible all -m ping
ansible-playbook playbook.yml
```

---

# 9. Monitoring Tools

Commands and concepts related to:
- Prometheus
- Grafana
- Logging
- Monitoring systems

---

# Technologies Included

| Technology | Purpose |
|---|---|
| Linux | Operating System |
| Git | Version Control |
| Docker | Containerization |
| Kubernetes | Container Orchestration |
| Jenkins | CI/CD |
| AWS | Cloud Computing |
| Terraform | Infrastructure as Code |
| Ansible | Automation |
| Prometheus | Monitoring |
| Grafana | Visualization |

---

# Purpose of This Repository

This repository is created for:

- DevOps interview preparation
- Daily DevOps practice
- Quick command reference
- Learning CI/CD pipelines
- Building strong DevOps fundamentals

---

# Who Can Use This Repository?

Useful for:
- Beginners learning DevOps
- Students
- DevOps Engineers
- Cloud Engineers
- Software Engineers

---

# How to Use

## Clone Repository

```bash
git clone https://github.com/yourusername/devops-commands.git
```

---

# Learning Roadmap

This repository supports learning:

```text
Linux
   ↓
Git & GitHub
   ↓
Docker
   ↓
Jenkins
   ↓
Kubernetes
   ↓
AWS
   ↓
Terraform & Ansible
   ↓
Monitoring & CI/CD
```

---

# Future Improvements

Planned additions:
- Advanced Kubernetes
- Helm Charts
- ArgoCD
- GitHub Actions
- DevSecOps
- MLOps
- Production-level CI/CD pipelines

---

# Author

## Gourav Lande

Interested in:
- DevOps
- Cloud Computing
- AI Engineering
- MLOps
- Machine Learning

GitHub:
https://github.com/gouravlande

---

# Contributions

Contributions are welcome.

You can:
- Fork the repository
- Add commands
- Improve documentation
- Create pull requests

---

# License

This repository is open-source and free to use for learning purposes.

---

# Support

If this repository helped you, consider giving it a ⭐ on GitHub.

---
# Conclusion

This repository serves as a complete DevOps command reference and learning resource for beginners and intermediate learners. It helps in understanding real-world DevOps tools and workflows used in industry environments.
