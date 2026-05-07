# Docker Commands and Notes

## What is Docker?

Docker is a containerization platform used to:
- Build applications
- Package applications
- Run applications inside containers

Docker helps developers:
- Ensure consistency across environments
- Deploy applications faster
- Reduce dependency issues

---

# Why Docker?

Before Docker:
- Applications worked differently on different systems
- Dependency conflicts occurred frequently

Docker solves this problem by packaging:
- Code
- Libraries
- Dependencies
- Runtime

into a single container.

---

# Docker Architecture

```text
Docker Client
      ↓
Docker Daemon
      ↓
Containers
      ↓
Docker Images
```

---

# Important Docker Components

| Component | Description |
|---|---|
| Docker Engine | Main Docker service |
| Docker Image | Blueprint/template |
| Docker Container | Running instance of image |
| Dockerfile | Instructions to build image |
| Docker Hub | Public image repository |
| Docker Compose | Multi-container management |

---

# Install Docker

## Ubuntu

```bash
sudo apt update
sudo apt install docker.io -y
```

---

# Check Docker Version

```bash
docker --version
```

---

# Start Docker Service

```bash
sudo systemctl start docker
```

---

# Enable Docker on Boot

```bash
sudo systemctl enable docker
```

---

# Check Docker Status

```bash
sudo systemctl status docker
```

---

# Docker Basic Commands

---

# Pull Docker Image

Download image from Docker Hub.

```bash
docker pull nginx
```

---

# List Images

```bash
docker images
```

---

# Run Container

```bash
docker run nginx
```

---

# Run Container in Background

```bash
docker run -d nginx
```

Options:
- `-d` → detached mode

---

# Run Container with Port Mapping

```bash
docker run -d -p 8080:80 nginx
```

Meaning:
- Local port 8080 mapped to container port 80

---

# List Running Containers

```bash
docker ps
```

---

# List All Containers

```bash
docker ps -a
```

---

# Stop Container

```bash
docker stop container_id
```

---

# Start Container

```bash
docker start container_id
```

---

# Restart Container

```bash
docker restart container_id
```

---

# Remove Container

```bash
docker rm container_id
```

---

# Remove Docker Image

```bash
docker rmi image_name
```

---

# Execute Command Inside Container

```bash
docker exec -it container_id bash
```

Options:
- `-it` → interactive terminal

---

# View Container Logs

```bash
docker logs container_id
```

---

# Dockerfile

## What is Dockerfile?

A Dockerfile contains instructions to create Docker images automatically.

---

# Example Dockerfile

```dockerfile
FROM python:3.10

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

CMD ["python", "app.py"]
```

---

# Dockerfile Instructions

| Instruction | Purpose |
|---|---|
| FROM | Base image |
| WORKDIR | Set working directory |
| COPY | Copy files |
| RUN | Execute commands |
| CMD | Default command |

---

# Build Docker Image

```bash
docker build -t myapp .
```

Options:
- `-t` → image tag/name

---

# Run Built Image

```bash
docker run -d -p 5000:5000 myapp
```

---

# Docker Volumes

Used for persistent storage.

---

# Create Volume

```bash
docker volume create myvolume
```

---

# Attach Volume

```bash
docker run -v myvolume:/data nginx
```

---

# Docker Networks

Used for container communication.

---

# List Networks

```bash
docker network ls
```

---

# Create Network

```bash
docker network create mynetwork
```

---

# Docker Compose

Used to manage multiple containers.

---

# docker-compose.yml Example

```yaml
version: '3'

services:
  web:
    image: nginx
    ports:
      - "8080:80"

  redis:
    image: redis
```

---

# Start Docker Compose

```bash
docker-compose up
```

---

# Run in Background

```bash
docker-compose up -d
```

---

# Stop Docker Compose

```bash
docker-compose down
```

---

# Docker Hub

Docker Hub is a cloud repository used to:
- Store images
- Share images
- Pull images

---

# Login to Docker Hub

```bash
docker login
```

---

# Push Image to Docker Hub

```bash
docker push username/image_name
```

---

# Docker Useful Commands Summary

| Command | Purpose |
|---|---|
| docker images | List images |
| docker ps | Running containers |
| docker pull | Download image |
| docker run | Run container |
| docker stop | Stop container |
| docker rm | Remove container |
| docker rmi | Remove image |
| docker logs | View logs |
| docker exec | Enter container |
| docker build | Build image |

---

# Advantages of Docker

- Lightweight
- Fast deployment
- Easy scaling
- Portable
- Environment consistency

---

# Docker vs Virtual Machine

| Docker | Virtual Machine |
|---|---|
| Lightweight | Heavy |
| Shares OS kernel | Separate OS |
| Faster startup | Slower |
| Less memory usage | More memory usage |

---

# Real-World Docker Use Cases

- Microservices
- CI/CD pipelines
- Cloud deployment
- Web applications
- Machine Learning deployment

---

# Docker in DevOps

Docker is heavily used in:
- CI/CD pipelines
- Kubernetes
- Cloud-native applications
- DevOps automation

---

# Learning Outcome

After learning Docker:
- You can containerize applications
- Build production-ready images
- Deploy applications consistently
- Work with DevOps pipelines

---

# Recommended Next Topics

After Docker learn:
1. Docker Compose
2. Kubernetes
3. Jenkins + Docker
4. Docker in CI/CD
5. Kubernetes Deployments

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

Docker is one of the most important DevOps tools used for containerization and deployment. It simplifies application development, deployment, scaling, and environment management.
