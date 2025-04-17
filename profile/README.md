# **Microservices Application Deployment on Kubernetes (Azure) - README**

## **Overview**

This project demonstrates the deployment of a **microservices-based application** using **Kubernetes (K8s)** on **Azure Cloud**, following best practices in:

✅ **Automation** (Infrastructure as Code, GitOps)

✅ **CI/CD** (Continuous Integration & Deployment)

✅ **IaC** (Infrastructure as Code using Terraform)

✅ **Observability** (Monitoring, Logging, and Tracing)

## **Architecture**

The microservices application consists of:

- **Frontend** (Angular)
- **Backend services** (Node.js, Spring Boot, Go)
- **Database** (PostgreSQL, Redis)
- **API Gateway** (NGINX)

Deployed in an **AKS (Azure Kubernetes Service)** cluster with **NGINX Ingress Controller** for traffic routing.

---

## **Tech Stack**

| Category | Tools/Technologies |
| --- | --- |
| **Cloud** | GCP |
| **Kubernetes** | GKE (Google Kubernetes Engine) |
| **IaC** | Terraform |
| **CI/CD** | GitHub Actions - Jenkins |
| **Containerization** | Docker |
| **Ingress Controller** | NGINX Ingress |
| **Monitoring & Logging** | Prometheus, Grafana |
| **Secrets Management** | GitHub Secrets |

---

## **Deployment Workflow**

1. **Infrastructure Setup (IaC)**
    - Use **Terraform** to provision GKE, networking, and databases.
    - Secure configurations with **GitHub Secrets**.
2. **Containerization & CI/CD**
    - **Build & push Docker images** to **google artifact registry repository**.
    - Use **GitHub Actions** to deploy workloads.
3. **Kubernetes Deployment**
    - Set up **Ingress & Service Mesh**.
    - Configure **autoscaling & security policies**.
4. **Observability & Security**
    - Monitor logs with **Prometheus, Grafana**.
    - Implement **Network Policies**.
