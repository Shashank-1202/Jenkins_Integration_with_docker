# 🚀  Jenkins CI/CD Pipeline with Docker & Docker Hub Integration


This project demonstrates a complete CI/CD pipeline built using Jenkins Declarative Pipeline to automate the Docker workflow:

- Pulling source code and Docker-related files from GitHub

- Building Docker images

- Pushing images to Docker Hub using credentials

- Deploying the container on an EC2 Ubuntu instance using Docker Compose
#

# 🔧 Prerequisites

- **Jenkins** installed on EC2 (master/worker setup)

- Docker and Docker Compose installed on the Jenkins node

- **GitHub Repository with:**

  - Dockerfile

  - docker-compose.yml

  - Application source code

**Docker Hub Account**

**Jenkins Credentials** for Docker Hub (PAT-based)

# 🔑 Jenkins Credentials Setup

1. Navigate to: **Jenkins Dashboard > Manage Jenkins** > Credentials

2. Create a new **Username and Password** credential:

- **ID**: dockerhub_cred

- **Username**: Your Docker Hub username

- **Password**: Docker Personal Access Token (PAT)

# 🐳 Docker Hub

Make sure the image name used in the pipeline matches your Docker Hub repo:

```sh
shashanki12/new-file:latest
```

You can find this at: https://hub.docker.com/repository/docker/shashanki12/new-file

# ☁️ Deployment Target

**Target**: Ubuntu EC2 Instance (can be the Jenkins worker or another node)

**Ports**: Ensure required ports are open (e.g., 80/8080) in the Security Groups

**Docker Compose**: Must be available on the deployment target

# ✅ Output

Once the pipeline runs:

- The latest code is cloned

- Docker image is built and tagged

- Image is pushed to Docker Hub

- Docker Compose starts the container in detached mode (-d) on EC2




