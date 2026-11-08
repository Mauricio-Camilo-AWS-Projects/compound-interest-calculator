# Compound Interest Calculator on AWS 3-Tier Architecture
## About the Project

Personal DevOps and Cloud Engineering project focused on building and automating AWS infrastructure for a three-tier web application.

The main focus is on Infrastructure as Code, CI/CD, containerization, deployment automation, and multi-environment management.

This repository contains the backend source code, Docker configuration, and Terraform files related to the infrastructure.

The application used as a workload is a compound interest calculator consisting of a frontend, backend API, and PostgreSQL database. While the primary focus is on Cloud and DevOps, the application can also evolve with new features and capabilities over time.

## Architecture

The architecture uses the following AWS services:

| Component | Service |
|---|---|
| Frontend | Amazon S3 + CloudFront |
| Backend | Amazon ECS + Fargate |
| Container Registry | Amazon ECR |
| Database | Amazon RDS (PostgreSQL) |
| Networking | Amazon VPC |
| Load Balancing | Application Load Balancer |

**Infrastructure as Code:** Terraform

**CI/CD:** GitHub Actions

## Related Repositories

- **Frontend:** https://github.com/Mauricio-Camilo-AWS-Projects/compound-interest-calculator-frontend
- **Pipelines:** https://github.com/Mauricio-Camilo-AWS-Projects/compound-interest-calculator-pipelines

## Tech Stack

- **Cloud:** AWS
- **Infrastructure as Code:** Terraform
- **CI/CD:** GitHub Actions
- **Containers:** Docker
- **Container Orchestration:** Amazon ECS (Fargate)
- **Container Registry:** Amazon ECR
- **Database:** PostgreSQL
- **Backend:** Typescript

## CI/CD & Infrastructure

GitHub Actions is used to automate application integration, infrastructure provisioning, and deployment processes.

The project includes:

- Backend and frontend CI pipelines.
- Docker image building and publishing.
- Infrastructure provisioning with Terraform.
- Automated backend deployment to ECS Fargate.
- Frontend deployment to S3 and CloudFront.
- Multi-environment management.

## Running Locally

**Prerequisites:**
- Git
- Docker
- Docker Compose

Clone this repository:

```bash
git clone https://github.com/Mauricio-Camilo-AWS-Projects/ecs-backend.git
```

Build and start the backend and PostgreSQL database:

```bash
docker compose up --build
```

The following services will be started:

| Service | Address |
|---|---|
| Backend API | http://localhost:3000 |
| PostgreSQL | localhost:5432 |

Docker Compose automatically configures the application environment and database connection.

To stop the services:

```bash
docker compose down
```

## Roadmap

### CI/CD
- [x] Backend CI pipeline.
- [x] Frontend CI pipeline.
- [ ] Automated Docker image publishing.
- [ ] Automated backend and frontend deployments.
- [ ] Infrastructure CI/CD workflows.

### AWS Infrastructure
- [x] Initial Terraform configuration for backend infrastructure.
- [ ] Refactor Terraform into reusable modules.
- [ ] Implement multi-environment management.
- [ ] Complete three-tier AWS architecture.
- [ ] Implement Multi-AZ infrastructure.
- [ ] Configure IAM and network security.
- [ ] Implement monitoring and logging.
- [ ] Implement backup and disaster recovery.

### Kubernetes
- [ ] Migrate backend workloads from ECS Fargate to Amazon EKS.
- [ ] Implement Kubernetes Deployment and Service configurations.
- [ ] Integrate Kubernetes deployments into CI/CD workflows.
