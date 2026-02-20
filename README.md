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
