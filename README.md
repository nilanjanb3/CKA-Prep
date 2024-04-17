# CKA-Prep
This is an in-progress repo to prepare for CKA.
> **Note:** For playing with Kubernetes we all need a local cluster. After carefully using and analyzing all the options such as Minikube, KinD, K3S, K3D etc.
> I mostly prefer using WSL as a Windows User, on top of it I have Docker installed (As Docker Desktop is not completely free). Finally on top of WSL K3D works awesome 😎.
> Pretty much you can expect a production like performance. Those who also wanna try Load Balancers can use Metal LB.
### Table of Contents
* 01-Introduction
    * [01-What is Kubernetes?](https://kubernetes.io/docs/concepts/overview/)
    * [02-Why CKA?](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/)
    * [03-CKA Roadmap Official](https://training.linuxfoundation.org/wp-content/uploads/2023/07/CKA_CurriculumPath_Jul23.pdf)
    * [04-Kubestronaut Program](https://www.cncf.io/training/kubestronaut/)
* 02-Core Concepts
    * [01-Cluster Architecture](https://kubernetes.io/docs/concepts/architecture/)
    * [02-Kubernetes Components](https://kubernetes.io/docs/concepts/overview/components/)
    * [03-Docker vs ContainerD](https://kodekloud.com/blog/docker-vs-containerd/)
    * [04-ETCD for K8s](https://learnk8s.io/etcd-kubernetes)
    * [05-Kube-API Sever](https://medium.com/devops-technical-notes-and-manuals/kube-api-server-how-it-communicates-with-other-kubernetes-cluster-components-cc60b041163d)
    * [06-Controller Manager](https://able8.medium.com/kubernetes-controllers-overview-b6ec086c1fb)
    * [07-Kube Scheduler](https://romanglushach.medium.com/kubernetes-scheduling-understanding-the-math-behind-the-magic-2305b57d45b1)
    * [08-Kubelet](https://kdmalviyan.medium.com/understanding-kubernetes-kubelet-a-deep-dive-into-the-engine-of-kubernetes-node-management-6b3e401bff17)
    * [09-Kube Proxy](https://medium.com/@amroessameldin/kube-proxy-what-is-it-and-how-it-works-6def85d9bc8f)
    * [10-Pods](https://kubernetes.io/docs/concepts/workloads/pods/)
    * [11-Replica Set](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/)
    * [12-Deployments in Kubernetes](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
    * [13-Deployments vs ReplicaSet](https://www.baeldung.com/ops/kubernetes-deployment-vs-replicaset)
    * [14-Services in K8s](https://kubernetes.io/docs/concepts/services-networking/service/)
    * [15-ClusterIP Service](https://medium.com/the-programmer/working-with-clusterip-service-type-in-kubernetes-45f2c01a89c8)
    * [16-NodePort Service](https://kubernetes.io/docs/concepts/services-networking/service/#type-nodeport)
    * [17-Load Balancer Service](https://kubernetes.io/docs/concepts/services-networking/service/#loadbalancer)
    * [18-Ingress Service](https://kubernetes.io/docs/concepts/services-networking/ingress/)
    * [19-HeadLess Service](https://kodekloud.com/blog/kubernetes-headless-service/)
    * [20-External Name Service](https://kubernetes.io/docs/concepts/services-networking/service/#externalname)
    * [21-Namespaces in K8s](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)
    * [22-Imperative vs Declarative Commands](https://kubeops.net/blog/imperative-vs-declarative)
    * [23-DNS for Service in K8s](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/)
    * [24-Kubectl Apply Command](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#apply)
* 03-Scheduling
    * [01-Scheduler in K8s](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/)
    * [02-Assigning Pods to Nodes](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/)
    * [03-Schedule using nodeName Property](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#nodename)
    * [04-Labels and Selectors in Kubernetes](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/)
    * [05-Taints and Tolerations](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)
    * [06-Node Selector](https://technos.medium.com/node-selectors-in-kubernetes-27638e62bfd6)
    * [07-Node Affinity](https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes-using-node-affinity/)
    * [08-Taints-Tolerations vs Node Affinity](https://blog.devops.dev/taints-and-tollerations-vs-node-affinity-42ec5305e11a)
    * [09-Resource Requests and Limits Management in K8s](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/)
    * [10-OOM Killed Error in K8s](https://komodor.com/learn/how-to-fix-oomkilled-exit-code-137/)
    * [11-Best Practices in Requests and Limits](https://blog.kubecost.com/blog/requests-and-limits/)
    * [12-Limit Range in K8s](https://kubernetes.io/docs/concepts/policy/limit-range/)
    * [13-Resource Quota for Namespaces in K8s](https://medium.com/@prateek.malhotra004/a-comprehensive-guide-to-resource-quotas-in-kubernetes-key-concepts-and-usage-examples-8ac4222027e2)
    * [14-DeamonSet in K8s](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/)
    * [15-Static Pods in K8s](https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/)
    * [16-Multiple Scheduler in K8s](https://kubernetes.io/docs/tasks/extend-kubernetes/configure-multiple-schedulers/)
    * [17-Pod Priority - PriorityClass - Preemption](https://devopscube.com/pod-priorityclass-preemption/)
    * [18-Scheduling Profiles](https://kubernetes-docsy-staging.netlify.app/docs/reference/scheduling/profiles/)
    * [19-Configuring Scheduler Profiles](https://kubernetes.io/docs/reference/scheduling/config/)
* 04-Logging and Monitoring
    * [01-Monittoring in Kubernetes](https://kubernetes.io/docs/tasks/debug/debug-cluster/resource-metrics-pipeline/)
    * [02-Deploying Metrics Server](https://github.com/kubernetes-sigs/metrics-server?tab=readme-ov-file#installation)
    * [03-Kubectl Top Commands](https://kubernetes.io/docs/reference/kubectl/generated/kubectl_top/)
    * [04-Kubectl Logs Commands](https://spacelift.io/blog/kubectl-logs)
* 05-Application Lifecycle Management
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    * []()
    
    