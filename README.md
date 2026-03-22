# ITSA 5501 – DevOps and System Integration

This repository is used for the ITSA 5501 project.
It demonstrates Git version control, branching, and DevOps-style project organization.

## Project Purpose
This project demonstrates DevOps workflows including Git branching, merging, and tagging.

## Repository Structure
- docker/ : Docker-related files
- k8s/    : Kubernetes YAML files
- iac/    : Infrastructure-as-Code scripts

Milestone 2 Container Operations

This milestone demonstrates the setup and deployment of a multi-container application using Docker Compose.

Services Used
frontend: Nginx container serving static HTML content on port 9090
user-db: MongoDB container with persistent storage
product-db: PostgreSQL container with environment variables and persistent storage
cache: Redis container for caching
prometheus: Prometheus monitoring service on port 9091
Docker Operations Performed
Created a frontend HTML page
Created a multi-container Docker Compose file
Created Prometheus configuration
Started all containers in detached mode
Verified services using localhost
Scaled frontend service to 3 instances
Commands Used
docker compose up -d
docker compose ps
docker compose up -d --scale frontend=3