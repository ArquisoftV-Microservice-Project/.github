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
---

## 🚀 Release Notes – GKE Microservices Platform `v1.0.0`

📅 **Fecha:** 2025-04-23  
🌐 **Cluster:** GKE con infraestructura automatizada vía Terraform  
🔒 **Enfoque:** Seguridad, escalabilidad y calidad continua

---

### 🧩 Arquitectura y Namespace Design

- **Namespaces implementados:**
  - `frontend`: apps de cara al usuario
  - `backend`: lógica de negocio
  - `database`: servicios de persistencia
  - `monitoring`: observabilidad (Prometheus, Grafana, Sonar)

- **Ingress NGINX** configurado para:
  - Exponer solo los servicios necesarios públicamente
  - Aplicar reglas de seguridad y routing centralizado

---

### ⚙️ CI/CD + Calidad de Código

- **Terraform** para provisión del cluster y recursos
- **GitHub Actions** con workflows para:
  - Construcción y push de imagenes a registry privado     
  - Deploy automático al actualizar imagenes
  - Tests y análisis estático con **SonarQube**

---

### 🔍 Observabilidad y Seguridad

- Stack de monitoreo: Prometheus + Grafana
- Seguridad:
  - Workload Identity
  - Secrets gestionados con GitHub secrets
  - Network Policies activadas

---

### 📈 Escalabilidad

- Node pools por tipo de servicio
- Load Balancer a nivel de cluster habilitado

---

