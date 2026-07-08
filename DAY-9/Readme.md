-> Kubernetes Website
Going deeper into architecture and practical considerations:

Control plane components:
kube-apiserver: front-end that exposes the Kubernetes API; all interactions (kubectl, dashboards, other components) go through it
etcd: distributed key-value store holding all cluster state — the "source of truth"
kube-scheduler: decides which node a new pod should run on, based on resource needs, constraints, and affinity rules
kube-controller-manager: runs controller processes that watch cluster state and drive it toward the desired state (e.g., node controller, replication controller)
cloud-controller-manager: integrates with cloud provider APIs (load balancers, storage, networking)

Node components:
kubelet: agent ensuring containers described in pod specs are running and healthy
kube-proxy: maintains network rules, enabling communication to and from pods
Container runtime: containerd or CRI-O executes the actual containers

Networking model: Every pod gets its own IP address, and pods can communicate with each other across nodes without NAT. Services provide stable virtual IPs and DNS names so other components don't need to track pod IPs directly, since pods are ephemeral and get replaced often.

Security practices: Role-Based Access Control (RBAC) restricts who can do what within a cluster. Network Policies control traffic flow between pods. Secrets should ideally be encrypted at rest and integrated with external secret managers (like HashiCorp Vault) rather than stored in plain YAML.

Common real-world patterns:
Blue-green and canary deployments for safer releases
StatefulSets for databases and other apps needing stable identities/storage
DaemonSets for running a pod on every node (e.g., log collectors, monitoring agents)
Jobs and CronJobs for batch or scheduled tasks
Where to go next:
- Architecture overview: https://kubernetes.io/docs/concepts/overview/components/
- Networking: https://kubernetes.io/docs/concepts/services-networking/
- Security: https://kubernetes.io/docs/concepts/security/

Want me to package this into a document, or go deeper on any specific piece (networking, security, a particular workload type)?
