# CKA-Prep
This is an in-progress repo to prepare for CKA.
> **Note:** For playing with Kubernetes we all need a local cluster. After carefully using and analyzing all the options such as Minikube, KinD, K3S, K3D etc.
> I mostly prefer using WSL as a Windows User, on top of it I have Docker installed (As Docker Desktop is not completely free). Finally on top of WSL K3D works awesome 😎.
> Pretty much you can expect a production like performance. Those who also wanna try Load Balancers can use Metal LB.
### Table of Contents
* 01-Introduction
    * [01-What is Kubernetes?](https://kubernetes.io/docs/concepts/overview/)
    * [02-K8s Architecture Simplified](https://www.simform.com/blog/kubernetes-architecture/)
    * [03-Why CKA?](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/)
    * [04-CKA Roadmap Official](https://training.linuxfoundation.org/wp-content/uploads/2023/07/CKA_CurriculumPath_Jul23.pdf)
    * [05-Kubestronaut Program](https://www.cncf.io/training/kubestronaut/)
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
    * [01-Monitoring in Kubernetes](https://kubernetes.io/docs/tasks/debug/debug-cluster/resource-metrics-pipeline/)
    * [02-Deploying Metrics Server](https://github.com/kubernetes-sigs/metrics-server?tab=readme-ov-file#installation)
    * [03-Kubectl Top Commands](https://kubernetes.io/docs/reference/kubectl/generated/kubectl_top/)
    * [04-Kubectl Logs Commands](https://spacelift.io/blog/kubectl-logs)
* 05-Application Lifecycle Management
    * [01-Kubernetes Workload Management](https://kubernetes.io/docs/concepts/workloads/controllers/)
    * [02-Kubernetes Official Deployment Strategies](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#strategy)
    * [03-Some Other Deployment Strategies](https://codefresh.io/learn/kubernetes-deployment/top-6-kubernetes-deployment-strategies-and-how-to-choose/)
    * [04-Application Lifecycle Management in K8s](https://medium.com/the-techlife/application-life-cycle-management-kubernetes-4a52a6f8e5d8)
    * [05-CMD vs ENTRYPOINT in Dockerfile](https://kodekloud.com/blog/docker-entrypoint-cmd/)
    * [06-Command, Entrypoint Usage and Differences](https://yuminlee2.medium.com/kubernetes-command-and-arguments-in-pod-c3f1be61ba1a)
    * [07-Environment Variables](https://kubernetes.io/docs/tasks/inject-data-application/define-environment-variable-container/)
    * [08-Config Maps](https://kubernetes.io/docs/concepts/configuration/configmap/)
    * [09-Using ConfigMaps for Environment Variables](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#define-container-environment-variables-using-configmap-data)
    * [10-Secrets in Kubernetes](https://kubernetes.io/docs/concepts/configuration/secret/)
    * [11-Secrets as Environment Variable](https://kubernetes.io/docs/tasks/inject-data-application/distribute-credentials-secure/#define-container-environment-variables-using-secret-data)
    * [12-Kubernetes Secret Best Practices](https://kubernetes.io/docs/concepts/security/secrets-good-practices/)
    * [13-Encrypting Secret Data at Rest](https://kubernetes.io/docs/tasks/administer-cluster/encrypt-data/)
    * [14-Sidecars in Kubernetes (Multi-Container Pods)](https://kodekloud.com/blog/kubernetes-sidecar-container/)
    * [15-Multi Container Pod Design Pattern](https://k21academy.com/docker-kubernetes/multi-container-pods/)
    * [16-Init-Container in K8s](https://kubernetes.io/docs/concepts/workloads/pods/init-containers/)
    * [17-Self Healing App in K8s](https://www.cncf.io/blog/2020/05/26/decoding-the-self-healing-kubernetes-step-by-step/)
* 06-Cluster Maintenance 
    * [01-Upgrade Activities in K8s](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-upgrade/#drain-the-node)
    * [02-Drain and Cordon](https://medium.com/@cldop.com/differences-similarities-between-kubectl-drain-cordon-commands-05b860367817)
    * [03-Drain K8s Docs](https://kubernetes.io/docs/tasks/administer-cluster/safely-drain-node/)
    * [04-Cordon K8s Docs](https://kubernetes.io/docs/concepts/architecture/nodes/#manual-node-administration)
    * [05-K8s Releases](https://github.com/kubernetes/kubernetes/releases)
    * [06-Kubernetes Component Upgrade Compatibility](https://kubernetes.io/releases/version-skew-policy/)
    * [07-Kubernetes Versions Official Support](https://kubernetes.io/releases/)
    * [08-Kubernetes Upgrade Best Practices](https://www.kubecost.com/kubernetes-best-practices/kubernetes-upgrade/)
    * [09-Cluster Upgrade Official Docs](https://kubernetes.io/docs/tasks/administer-cluster/cluster-upgrade/)
    * [10-Kubeadm Cluster Upgrade](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-upgrade/)
    * [11-Upgrading Linux Worker Node](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/upgrading-linux-nodes/)
    * [12-Backup and Restore with ETCD in Kubernetes](https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/)
    * [13-Operating ETCD Cluster for K8s](https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/)
    * [14-Disaster Recovery with Kubernetes Cluster](https://www.youtube.com/watch?v=qRPNuT080Hk)
* 07-Security
    * [01-Security in K8s](https://kubernetes.io/docs/concepts/security/)
    * [02-Authentication in Cluster](https://kubernetes.io/docs/reference/access-authn-authz/authentication/)
    * [03-Basic AuthN - Deprecated](https://www.linkedin.com/pulse/how-set-up-basic-authentication-kubernetes-tahmid-ul-muntakim/)
    * [04-How TLS/SSL Certificate Works](https://youtu.be/j9QmMEWmcfo)
    * [05-TLS Certificates in Kubernetes](https://yuminlee2.medium.com/kubernetes-tls-certificates-b75fee80670d)
    * [06-Generating Certificates for Kubernetes Components](https://github.com/kodekloudhub/certified-kubernetes-administrator-course/blob/master/docs/07-Security/07-TLS-in-Kubernetes-Certificate-Creation.md)
    * [07-Certificate Management with Kubeadm](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-certs/)
    * [08-Managing Certificates Manually](https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/)
    * [09-Kubernetes Certificate Paths](https://kubernetes.io/docs/setup/best-practices/certificates/)
    * [10-Kubernetes Certificate API](https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/)
    * [11-Kubeconfig](https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/)
    * [12-Configure Access to Multiple Clusters](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/)
    * [13-Kubectl Config Commands](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#config)
    * [14-K8s API Groups](https://medium.com/@seifeddinerajhi/understanding-kubernetes-api-groups-and-versions-1043d26f455e)
    * [15-Kubectl Proxy](https://kubernetes.io/docs/tasks/extend-kubernetes/http-proxy-access-api/)
    * [16-AuthZ in K8s](https://kubernetes.io/docs/reference/access-authn-authz/authorization/)
    * [17-RBAC in K8s](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
    * [18-ClusterRole and ClusterRoleBinding](https://octopus.com/blog/k8s-rbac-roles-and-bindings)
    * [19-Service Accounts](https://kubernetes.io/docs/concepts/security/service-accounts/)
    * [20-Configure Pods with ServiceAccount](https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/)
    * [21-Pulling Images from Private Registry](https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/)
    * [22-Security in Docker](https://docs.docker.com/engine/security/)
    * [23-Run as a User in Docker](https://www.baeldung.com/ops/docker-set-user-container-host)
    * [24-Runtime Capabilities in Docker Container](https://docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities)
    * [25-Security Context in Kubernetes](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/)
    * [26-Network Policies in K8s](https://kubernetes.io/docs/concepts/services-networking/network-policies/)
    * [27-kubectx & kubens](https://github.com/ahmetb/kubectx)
* 08-Storage
    * [01-Storage in Docker](https://k21academy.com/docker-kubernetes/docker-storage/)
    * [02-Storage Driver vs Docker Volume](https://docs.docker.com/storage/storagedriver/#storage-drivers-versus-docker-volumes)
    * [03-Docker Volume Plugin](https://docs.docker.com/engine/extend/legacy_plugins/#volume-plugins)
    * [04-CSI in Kubernetes Specs](https://github.com/container-storage-interface/spec/blob/master/spec.md)
    * [05-Volumes in Kubernetes](https://kubernetes.io/docs/concepts/storage/volumes/)
    * [06-Persistent Volume in Kubernetes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)
    * [07-Persistent Volume Claim in K8s](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#persistentvolumeclaims)
    * [08-Configuring Pods with PV and PVC](https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/)
    * [09-Storage Class in K8s](https://kubernetes.io/docs/concepts/storage/storage-classes/)
    * [10-Dynamic Provisioning with Storage Class and PVC](https://kubernetes.io/docs/concepts/storage/storage-classes/)
* 09-Networking
    * [01-Linux Networking - Switching, Routing and Gateway](https://yuminlee2.medium.com/linux-networking-switching-routing-and-gateway-4e3c09fac616)
    * [02-How to configure a Linux Machine as a Router](https://www.computernetworkingnotes.com/linux-tutorials/how-to-configure-and-use-linux-as-a-router.html)
    * [03-Understanding DNS](https://www.linode.com/docs/guides/introduction-to-dns-on-linux/)
    * [04-CoreDNS for K8s](https://coredns.io/plugins/kubernetes/)
    * [05-Network Namespaces in Linux](https://ramesh-sahoo.medium.com/linux-network-namespace-and-five-use-cases-using-various-methods-f45b1ec5db8f)
    * [06-Docker Networking](https://docs.docker.com/network/)
    * [07-CNI in K8s](https://www.tigera.io/learn/guides/kubernetes-networking/kubernetes-cni/)
    * [08-K8s Cluster Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/)
    * [09-Installing Networking Addons](https://kubernetes.io/docs/concepts/cluster-administration/addons/)
    * [10-Understanding Pod Networking](https://medium.com/google-cloud/understanding-kubernetes-networking-pods-7117dd28727)
    * [11-Weave CNI for K8s](https://github.com/weaveworks/weave/blob/master/README.md)
    * [12-Weave CNI Comparison with Other CNIs](https://www.techtarget.com/searchitoperations/tutorial/Step-by-step-guide-Get-started-with-Weave-for-Kubernetes)
    * [13-Service Networking in K8s](https://medium.com/google-cloud/understanding-kubernetes-networking-services-f0cb48e4cc82)
    * [14-DNS in K8s](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/)
    * [15-How CoreDNS Works](https://waytoeasylearn.com/learn/core-dns-in-kubernetes/)
    * [16-Ingress in K8s](https://kubernetes.io/docs/concepts/services-networking/ingress/)
    * [17-Ingress Controller in Kubernetes](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/)
    * [18-Ingress Nginx Controller](https://github.com/kubernetes/ingress-nginx)
* 10-Design and Install K8s Cluster
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
    
    
    