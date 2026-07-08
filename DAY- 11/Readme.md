☸️ Kubernetes Learning Project

A simple Kubernetes learning project built for understanding Kubernetes architecture, Pods, Deployments, and container orchestration concepts.

Technologies Used
- Kubernetes
- Docker
- AWS EC2
- YAML
- Kubectl

Topics Covered

- Kubernetes Cluster
- Control Plane
- API Server
- etcd
- Scheduler
- Controller Manager
- Worker Node
- Kubelet
- Container Runtime
- kube-proxy
- Pods
- ReplicaSet
- Deployment
- Services

Run Kubernetes Commands

```bash
kubectl get nodes
kubectl get pods
kubectl get deployments
```

Create Pod

```bash
kubectl apply -f pod.yml
kubectl get pods
```

Create Deployment

```bash
kubectl apply -f deployment.yml
kubectl get deployments
```

Port Forward

```bash
kubectl port-forward hospital-pod 5000:5000 --address=0.0.0.0
```

Open in browser:

```bash
http://<EC2-Public-IP>:5000
```

Features

- Beginner-friendly Kubernetes notes
- Pod and Deployment examples
- Basic kubectl commands
- Kubernetes architecture explanation
- Hands-on practical learning

Learning Outcome

- Understanding Kubernetes architecture
- Learning Pods and Deployments
- Working with Kubernetes commands
- Deploying applications using Kubernetes
