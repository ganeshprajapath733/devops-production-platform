# Cloud-Native Production-Ready DevOps Platform

A complete end-to-end DevOps project demonstrating infrastructure automation, container orchestration, GitOps, CI/CD pipelines, and observability.

## 🏗️ Architecture
```
GitHub (Source) → GitHub Actions (CI/CD) → Docker → AWS ECR
                                                      ↓
                                          ArgoCD (GitOps) 
                                                      ↓
                                          Kubernetes Cluster
                                                      ↓
                                    Prometheus + Grafana (Monitoring)
```

## 🛠️ Technologies Used

- **Infrastructure as Code**: Terraform
- **Cloud Platform**: AWS (VPC, ECR, IAM)
- **Container Orchestration**: Kubernetes
- **GitOps**: ArgoCD
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus, Grafana
- **Container Registry**: AWS ECR

## 📁 Project Structure
```
.
├── terraform/
│   ├── vpc/          # VPC, Subnets, Internet Gateway
│   ├── ecr/          # Container Registry
│   └── eks/          # EKS Cluster (ready to deploy)
├── k8s/
│   ├── dev/          # Development manifests
│   ├── stage/        # Staging manifests
│   └── prod/         # Production manifests
├── .github/workflows/
│   └── ci-cd.yaml    # GitHub Actions pipeline
└── monitoring/       # Prometheus & Grafana configs
```

## 🚀 Key Features

✅ **Infrastructure as Code** - All infrastructure defined in Terraform  
✅ **Multi-Environment** - Separate dev/stage/prod namespaces  
✅ **GitOps Deployment** - ArgoCD automates K8s deployments from Git  
✅ **CI/CD Pipeline** - Automated build, test, and deploy  
✅ **Auto-Scaling** - HPA configured for pod autoscaling  
✅ **Observability** - Prometheus metrics + Grafana dashboards  
✅ **Security** - IAM roles, image scanning, secrets management  

## 📊 Monitoring

- **Prometheus**: Collects metrics from Kubernetes cluster
- **Grafana**: Visualizes metrics with pre-built dashboards
- **Alerting**: Configured for CPU, memory, and availability

## 🔄 CI/CD Pipeline

1. Code pushed to GitHub
2. GitHub Actions triggers build
3. Docker image built and pushed to ECR
4. ArgoCD detects change in Git
5. Automatically deploys to Kubernetes

## 💰 Cost Optimization

- VPC, Subnets, IGW: **FREE**
- ECR: **FREE tier** (500MB)
- Local Kubernetes (Kind): **FREE**
- No EKS, NAT Gateway, or Load Balancers (cost control)

## 📝 Setup Instructions

See [SETUP.md](./SETUP.md) for detailed deployment steps.

## 👤 Author

**Ganesh Prajapath**  
[GitHub](https://github.com/ganeshprajapath733) | [LinkedIn](#)

---

**Skills Demonstrated**: AWS, Terraform, Kubernetes, Docker, GitOps, CI/CD, Prometheus, Grafana, ArgoCD, Infrastructure Automation

## 📸 Screenshots

### ArgoCD GitOps Dashboard
![ArgoCD](./screenshots/argocd.png)

### Grafana Monitoring
![Grafana](./screenshots/grafana.png)
