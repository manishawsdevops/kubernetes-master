# kubernetes-master
This course contains about the information related to Kubernetes.

Basically two certifications:
  1. Certified Kubernetes Administrator
  2. Certified Kubernetes Developers

### Kubernetes Overview - K8s
- Kubernetes is basically the containers and their orchestration
- Process of deploying and managing containers automatically is called Container Orchestration
- Kubernetes is from Google is similar to Docker Swarn or Apache Mesos.
- Kubernetes is now supported on all AWS, GCP and Azure.

### Kubernetes Architecture
- **Node(Minions):** Is it a physical or Virtual machine where Kubernetes is installed and this is worker node. If application fails on a node, the app failes. So, we need to have multiple nodes for an application.
- **Cluster:** It is a set of Nodes grouped together. Even if one node fails another can serve the application and also share the load.
- **Master:** It is another node kubernetes installed in it and monitors all the worker nodes. This is resposible for cluster management.
- **Components:** when we install kubernetes, we install below services
  - API Server: acts as Front End for Kubernetes. User, management service, kubectl all talk to API Server to manage kubernetes cluster.
  - etcd: Distributed key value store, used to store data. Its responsible for logs within in the cluster to ensure no conflicts within master.
  - kubelet: It is the agent that runs on each node on the cluster and make sure that containers running on nodes as expected.
  - Container Runtime: Underlying software used to run containers ( Here it is Docker )
  - Controller: These are brains for Clusters for orchestration. They monitor the nodes and bring nodes if something goes wrong.
  - Scheduler: Responsible for distributing containers for work loads.

### Master vs Worker Nodes
- Master node consists of majorly kube-apiserver, etcd, controller, scheduler.
- Worker node consits of Container runtime like Docker and kubelet agent.

### kubectl
- kubectl is the command line utility of kubernetes. This CLI is used to deploy and manage kubernetes cluster.
  - kubectl run hello-world
  - kubectl cluster-info
  - kubectl get nodes

