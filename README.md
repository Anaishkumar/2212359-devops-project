DevOps Final Project

**Name:** Anaish Kumar
**Registration Number:** 2212359

## 1. Project Overview
This project is a containerized microservice deployed on AWS EC2.demonstrates complete DevOps CI/CD + FastAPI application with a PostgreSQL database.

## 2. Architecture Description
* **Web Service:** FastAPI + REST API endpoints on port 8000.
* **Database:** PostgreSQL 15 running on port 5432 with a save named volume.
* **Containerization:** Multi-stage Dockerfile for the web app with a non-root user. Services are orchestrated using Docker Compose.
* **CI/CD Pipeline:** Fully automated via GitHub Actions.
  * **CI Pipeline:** Runs `flake8` for linting and `pytest` for automated testing.
  * **CD Pipeline:** Automatically SSHs into the AWS EC2 instance and redeploys the containers.
* **Cloud Infrastructure:** Hosted on an AWS EC2 `t2.micro` (Ubuntu) instance with required security groups.

## 3. Setup Instructions (Local Development)

1. **Clone the repository:**
   `git clone https://github.com/Anaishkumar/2212359-devops-project.git`
   `cd 2212359-devops-project`

2. **Set up environment variables:**
   `cp .env.example .env`

3. **Start the application:**
   `docker compose up -d --build`

4. **Verify Health:**
   Navigate to `http://localhost:8000/health` in your web browser.
