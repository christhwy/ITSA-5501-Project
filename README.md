# ITSA-5501 Project

## Project Overview
This project demonstrates the setup and deployment of a containerized multi-service application using Docker and Docker Compose. It is completed in two milestones, where Milestone 1 focuses on project structure and foundational setup, and Milestone 2 implements a fully functional multi-container system with monitoring capabilities.

---

## Milestone 1 – Project Setup and Foundation

Milestone 1 established the foundational environment required for containerized application development and deployment.

### Objectives
- Initialize project repository
- Create a standardized folder structure
- Prepare for containerization and orchestration
- Set up version control workflow

### Key Activities
- Created GitHub repository for version control
- Organized project into modular folders:
  - `docker/` for container configurations
  - `k8s/` for future Kubernetes deployment
  - `iac/` for infrastructure-as-code components
- Prepared placeholder files for Docker workflows
- Practiced Git commands:
  - `git init`
  - `git add`
  - `git commit`
  - `git push`
- Established a clean and scalable project structure for future expansion

### Outcome
A well-structured repository that serves as the foundation for implementing a multi-container system in Milestone 2.

---

## Milestone 2 – Multi-Container Application Deployment

Milestone 2 focuses on building and deploying a multi-container application using Docker Compose, along with monitoring using Prometheus.

### Objectives
- Develop a frontend application
- Configure multiple services using Docker Compose
- Implement persistent storage
- Set up monitoring
- Scale application components

---

## Frontend Implementation
A static webpage was created to represent a vacation destination.

### Features
- Displays a travel destination (e.g., Kyoto, Japan)
- Includes:
  - Title
  - Image
  - Description
  - Attractions
  - Activities

### Technology Used
- HTML
- Served using Nginx container

---

## Docker Compose Configuration

A multi-container architecture was implemented using `docker-compose.yml`.

### Services

#### 1. Frontend
- Image: `nginx:alpine`
- Port: `9090`
- Purpose: Serve static HTML page

#### 2. User Database
- Image: `mongo`
- Volume: `user_data`
- Purpose: Store user-related data

#### 3. Product Database
- Image: `postgres`
- Environment Variables:
  - `POSTGRES_USER`
  - `POSTGRES_PASSWORD`
  - `POSTGRES_DB`
- Volume: `product_data`
- Purpose: Store product-related data

#### 4. Cache
- Image: `redis`
- Purpose: Provide in-memory caching

#### 5. Monitoring (Prometheus)
- Image: `prom/prometheus`
- Port: `9091`
- Purpose: Monitor system performance

---

## Networking and Storage

### Network
- Custom bridge network: `app-network`
- Allows communication between all services

### Volumes
- `user_data` → MongoDB persistence
- `product_data` → PostgreSQL persistence

---

## Prometheus Configuration

A configuration file (`prometheus.yml`) was created to define monitoring behavior.

### Features
- Scrape interval: 15 seconds
- Monitors Prometheus service itself

---

## Container Deployment

The application was deployed using Docker Compose.

### Commands Used
docker compose up -d
docker compose ps
docker compose up -d --scale frontend=3