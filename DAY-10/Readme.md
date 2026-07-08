 ☸️ Kubernetes Notes

This repository contains simple notes on Kubernetes Architecture and Deployments for beginners.

 📚 Topics Covered

- What is Kubernetes?
- Kubernetes Cluster
- Control Plane
- API Server
- etcd
- Scheduler
- Controller Manager
- Cloud Controller Manager
- Worker Node
- Kubelet
- Container Runtime
- kube-proxy
- Pods
- ReplicaSet
- Deployment
- Services

---

What is Kubernetes?

Kubernetes is an open-source container orchestration platform used to automate deployment, scaling, and management of containerized applications.

Kubernetes Cluster

A Kubernetes Cluster consists of:

- Control Plane
- Worker Nodes

Control Plane Components

API Server
- Acts as the communication center of Kubernetes.

etcd
- Stores cluster information and configuration data.

Scheduler
- Assigns Pods to available nodes.

Controller Manager
- Maintains desired cluster state.

Worker Node Components

Kubelet
- Communicates with the control plane.

Container Runtime
- Runs containers.

kube-proxy
- Handles networking and communication.

Conclusion

Kubernetes helps manage applications efficiently with scalability and automation.
