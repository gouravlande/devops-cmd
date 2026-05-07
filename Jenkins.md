# Jenkins Commands and Notes

## What is Jenkins?

Jenkins is an open-source automation server used for:

- Continuous Integration (CI)
- Continuous Deployment (CD)
- Build Automation
- Testing Automation
- Deployment Automation

Jenkins helps automate the software development lifecycle.

---

# Why Jenkins?

Before Jenkins:
- Manual builds
- Manual testing
- Slow deployments
- Human errors

Jenkins automates:
- Building
- Testing
- Deploying applications

---

# Jenkins Workflow

```text
Developer Pushes Code
          ↓
GitHub/GitLab Repository
          ↓
Jenkins Pipeline Triggered
          ↓
Build Application
          ↓
Run Tests
          ↓
Deploy Application
```

---

# Jenkins Architecture

```text
Jenkins Master
       ↓
Jenkins Agents/Nodes
       ↓
Build & Deployment Tasks
```

---

# Important Jenkins Components

| Component | Description |
|---|---|
| Jenkins Server | Main automation server |
| Job | Task executed by Jenkins |
| Pipeline | CI/CD workflow |
| Agent/Node | Machine executing jobs |
| Plugin | Adds extra functionality |
| Jenkinsfile | Pipeline configuration file |

---

# Install Jenkins (Ubuntu)

## Update Packages

```bash
sudo apt update
```

---

## Install Java

```bash
sudo apt install openjdk-17-jdk -y
```

---

## Verify Java

```bash
java -version
```

---

## Install Jenkins

```bash
sudo apt install jenkins -y
```

---

# Start Jenkins

```bash
sudo systemctl start jenkins
```

---

# Enable Jenkins on Boot

```bash
sudo systemctl enable jenkins
```

---

# Check Jenkins Status

```bash
sudo systemctl status jenkins
```

---

# Access Jenkins

Default URL:

```text
http://localhost:8080
```

---

# Get Jenkins Initial Password

```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

---

# Jenkins Basic Concepts

---

# 1. Job

A Jenkins job is a task performed by Jenkins.

Examples:
- Build application
- Run tests
- Deploy application

---

# 2. Pipeline

Pipeline defines automation stages.

Example:

```text
Build → Test → Push → Deploy
```

---

# 3. Jenkinsfile

A Jenkinsfile contains pipeline code.

Written using:
- Groovy syntax

---

# Simple Jenkins Pipeline

```groovy
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
            }
        }
    }
}
```

---

# Pipeline Stages

| Stage | Purpose |
|---|---|
| Build | Compile/build application |
| Test | Run automated tests |
| Push | Push Docker image/artifacts |
| Deploy | Deploy application |

---

# Jenkins Important Commands

---

# Restart Jenkins

```bash
sudo systemctl restart jenkins
```

---

# Stop Jenkins

```bash
sudo systemctl stop jenkins
```

---

# View Jenkins Logs

```bash
sudo journalctl -u jenkins
```

---

# Check Running Port

```bash
sudo netstat -tulnp | grep 8080
```

---

# Jenkins Plugins

Plugins extend Jenkins functionality.

Popular Plugins:
- Git Plugin
- Docker Plugin
- Kubernetes Plugin
- Pipeline Plugin
- Blue Ocean

---

# Jenkins + GitHub Integration

Jenkins can:
- Pull code from GitHub
- Trigger builds automatically

---

# GitHub Webhook Flow

```text
GitHub Push
      ↓
Webhook Trigger
      ↓
Jenkins Build Starts
```

---

# Jenkins + Docker

Jenkins can:
- Build Docker images
- Push images to Docker Hub
- Deploy containers

---

# Example Docker Build in Jenkins

```groovy
stage('Docker Build') {
    steps {
        sh 'docker build -t myapp .'
    }
}
```

---

# Jenkins + Kubernetes

Jenkins can deploy applications into Kubernetes clusters.

Example:

```groovy
stage('Deploy to Kubernetes') {
    steps {
        sh 'kubectl apply -f deployment.yaml'
    }
}
```

---

# Jenkins Freestyle Project

GUI-based Jenkins project.

Features:
- Easy for beginners
- No coding required

---

# Jenkins Pipeline Project

Code-based automation.

Advantages:
- Better scalability
- Version controlled
- Production-ready

---

# CI/CD Concepts

## Continuous Integration (CI)

Automatically:
- Build code
- Run tests
- Detect bugs early

---

## Continuous Deployment (CD)

Automatically deploy application after successful testing.

---

# Jenkins Security Concepts

- RBAC (Role-Based Access Control)
- Credentials Management
- Secret Handling
- Authentication & Authorization

---

# Jenkins Backup

Backup important folders:

```bash
/var/lib/jenkins
```

---

# Common Jenkins Errors

| Error | Reason |
|---|---|
| Build Failed | Compilation/Test failure |
| Permission Denied | User permission issue |
| Port Already Used | Another service using 8080 |
| Plugin Error | Plugin conflict |

---

# Advantages of Jenkins

- Open-source
- Huge plugin ecosystem
- Easy automation
- Supports CI/CD
- Integrates with many tools

---

# Jenkins Real-World Use Cases

- CI/CD pipelines
- Automated testing
- Docker automation
- Kubernetes deployment
- Cloud deployment

---

# Jenkins in DevOps

Jenkins is one of the most important DevOps tools for:
- Automation
- Continuous Integration
- Continuous Deployment

---

# Technologies Integrated with Jenkins

| Tool | Purpose |
|---|---|
| GitHub | Source Code |
| Docker | Containerization |
| Kubernetes | Orchestration |
| AWS | Cloud Deployment |
| SonarQube | Code Quality |
| Maven | Build Tool |

---

# Learning Outcome

After learning Jenkins:
- You can automate CI/CD pipelines
- Integrate GitHub with Jenkins
- Build and deploy applications automatically
- Work on DevOps automation projects

---

# Recommended Next Topics

After Jenkins learn:
1. Docker + Jenkins
2. Kubernetes + Jenkins
3. GitHub Actions
4. Terraform
5. ArgoCD
6. DevSecOps

---

# Author

## Gourav Lande

Interested in:
- DevOps
- Cloud Computing
- AI Engineering
- MLOps

GitHub:
https://github.com/gouravlande

---

# Conclusion

Jenkins is one of the most powerful automation tools used in DevOps for CI/CD pipelines, automated testing, and deployment workflows. It helps teams deliver software faster and more reliably.
