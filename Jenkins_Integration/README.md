# 🚀  Jenkins CI/CD Pipeline with Docker & Docker Hub Integration


This project demonstrates a complete CI/CD pipeline built using Jenkins Declarative Pipeline to automate the Docker workflow:

- Pulling source code and Docker-related files from GitHub

- Building Docker images

- Pushing images to Docker Hub using credentials

- Deploying the container on an EC2 Ubuntu instance using Docker Compose
#

# 🔧 Prerequisites

Jenkins installed on EC2 (master/worker setup)

Docker and Docker Compose installed on the Jenkins node

GitHub Repository with:

Dockerfile

docker-compose.yml

Application source code

Docker Hub Account

Jenkins Credentials for Docker Hub (PAT-based)
