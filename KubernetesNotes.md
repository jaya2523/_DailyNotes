--
Kubernetes
--
- Open source container orchestration framework.
- Developed by google.
- Helps to manage 100s or 1000s of containerized applications.
- In different deploymeny environtments - physical, virtual, hybrid.

--
What problems kubernetes solve
--
--
What are the tasks of an orchestration tool?
--

- <b>The need for container orchestration tool</b>
- Trend from mono to microservices increased usage of containers, demand for a proper way of managing those hundreds of containers is so difficult to do in scripts.
<br>
<b>What features do orchestration tool offer?</b>
- High Availabity or No downtime
- Scalability or high performance
- Disaster recovery - backup and restore.

--
Kubernetes Components
--
1. Node(physical machine) and pods
2. Service and Ingress
3. ConfigMap and Secret
4. Volumes
5. Deployment and Stateful State.

--
Kubernetes Architecture
--
1. Worker Nodes
   - Each node has multiple pods on it, 3 processes must be installed on everynode and worker nodes do the actual work.
   - Kubelet schedule those pods inside the nodes.
   - Kubelet work as interface interacts with both - the container and node.
   - Kubelet starts the pod with a container inside.
   - 1. Container Runtime + Kubelete
   - 2. Communication Service
   - 3. Kube Proxy sends the request from services to the pods.

   Overcome Network overhead
   --
   How do we interact with the cluster, how to
   schedule pod, monitor, re-schedule/re-start pod?, join a new node?
   --

   - All the above mentioned managing things are done by master processes.
   -  API Server -> Scheduler -> Controll Manager -> etcd.

   --
   To add new master/node server
   --
   1. get new bare server
   2. install all the master/worker node processes
   3. add it to the cluster

--
Minicube and Kubectl
--
Product cluser setup 
- multiple master and worker nodes
- seperate virtual or physical machines
- Minikube = Node -> VirtualBox
-   Creates virtual box on your laptop
-   nodes runs in that virtual box.
-   1 Node k8s cluster
-   for testing purposes

**Kubectl** - cli
mini kubes -- worker process + master process 

kubectl create deployment NAME --image = image_name [options to create more than one replica].
kubectl get deployments
kubectl get replicaset
kubectl edit deploymnet name.
kubectl describe pod_name
kubectl exec pod_name -- bin/bash
kubectl apply -f 
kubectl expose deployment my-nginx --port=8080 --type=loadBalancer



• minikube start/delete
• minikube status
• minikube dashboard
• kubectl create deployment my-app --image-link
• kubectl get deployments
• kubectl get pods
• kubectl delete deployment my-app

•
kubectl expose deployment my-app -- type=LoadBalancer --port=80
minikube service my-app
•
kubectl get services
 
