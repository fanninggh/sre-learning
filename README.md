# Learning SRE: Container Orchestration

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

> **Part of my journey from Database Reliability Engineer to Site Reliability Engineer**

## What I Built
A simple Python Flask application demonstrating:
- Docker containerization best practices
- Kubernetes deployment with 3 replicas for high availability
- Service exposure and load balancing

## Why This Matters for SRE
Understanding container orchestration is fundamental to modern infrastructure work. 
This project demonstrates:
- Building production-ready containers
- Managing application lifecycles with Kubernetes
- Implementing basic high-availability patterns
- Infrastructure declarative configuration

## Technical Stack
- **Language:** Python 3.9 with Flask
- **Containerization:** Docker
- **Orchestration:** Kubernetes (tested with minikube)
- **Deployment:** 3 replicas with NodePort service

## Running Locally

### With Docker
\`\`\`bash
docker build -t myapp .
docker run -p 5000:5000 myapp
# Visit: http://localhost:5000
\`\`\`

### With Kubernetes
\`\`\`bash
# Start local cluster
minikube start

# Build image (load into minikube)
eval $(minikube docker-env)
docker build -t myapp:latest .

# Deploy
kubectl apply -f deployment.yaml

# Check status
kubectl get pods
kubectl get svc

# Access the service
minikube service myapp-service
\`\`\`

## What I Learned
- Container image optimization (multi-stage builds, layer caching)
- Kubernetes resource management (CPU/memory requests and limits)
- Service discovery and load balancing in K8s
- Health checks and readiness probes

## Next Steps
- [ ] Add Prometheus metrics endpoint
- [ ] Implement readiness and liveness probes
- [ ] Set up Horizontal Pod Autoscaler
- [ ] Add Helm chart for easier deployment
- [ ] CI/CD pipeline with GitHub Actions

## About This Project
This is part of my transition from Database Reliability Engineering to full-stack Site Reliability Engineering. 
You can follow my journey at [linkedin.com/in/fanningcareers](https://linkedin.com/in/fanningcareers)


# Learning SRE: Container Orchestration

## What I Built
A simple Python Flask application demonstrating:
- Docker containerization
- Kubernetes deployment with 3 replicas
- Service exposure via NodePort

## Why This Matters
Understanding container orchestration is fundamental to modern SRE work. 
This project demonstrates:
- Building production-ready containers
- Managing application lifecycles with K8s
- Load balancing across multiple replicas

## Running Locally
\`\`\`bash
# Build and run with Docker
docker build -t myapp .
docker run -p 5000:5000 myapp

# Deploy to Kubernetes
minikube start
kubectl apply -f deployment.yaml
\`\`\`

## Next Steps
- Add health checks and readiness probes
- Implement rolling updates
- Add monitoring with Prometheus
