# DevOps Lifecycle Implementation for Abode Software

This project demonstrates the implementation of the DevOps lifecycle for Abode Software, a product-based company. The project automates the software delivery process using Jenkins, Docker, and GitHub, ensuring seamless CI/CD workflows.

## Project Overview

The lifecycle includes the following key steps:
1. Installing necessary software using a configuration management tool.
2. Implementing Git workflow for version control.
3. Automating build and test pipelines triggered by commits to specific branches.
4. Containerizing the application using Docker for consistent deployment.
5. Defining Jenkins pipelines for build, test, and production deployment.

---

## Project Workflow

### 1. **Configuration Management**
Necessary software is installed and configured on target machines using a configuration management tool.

### 2. **Git Workflow**
- The code is hosted on the GitHub repository: [website repository](https://github.com/hshar/website.git).
- Branches:
  - `master`: For production-ready code.
  - `develop`: For testing new changes.

### 3. **Build and Deployment Pipeline**
The pipeline triggers actions based on the branch:
- **Master Branch:**
  - Automatically builds the application.
  - Tests the application.
  - Deploys the application to the production environment.

- **Develop Branch:**
  - Automatically builds the application.
  - Tests the application without deploying to production.

### 4. **Containerization**
- The application is containerized using Docker.
- Pre-built container used: `hshar/webapp`.
- The code resides in `/var/www/html` within the container.

### 5. **Jenkins Pipeline**
The CI/CD process is managed using a Jenkins pipeline with the following jobs:
- **Job 1: Build** - Builds the application and Docker image.
- **Job 2: Test** - Runs automated tests on the application.
- **Job 3: Prod** - Deploys the application to the production environment (for the `master` branch).

---

## Prerequisites

- Git
- Docker
- Jenkins
- Configuration Management Tool (e.g., Ansible, Chef, or Puppet)

---

## Usage

### Clone the Repository
```bash
git clone https://github.com/hshar/website.git
/var/www/html
├── index.html
├── css/
├── js/
└── images/
Authors
This project was implemented by Biswajit Sahoo , Aws , Azure , Gcp DevOps  specializing in CI/CD workflows, automation, and containerization. The project was completed as part of the IntelliPaat DevOps Certification Training.

