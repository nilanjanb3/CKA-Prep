```sh
$ cat <<EOF | sudo tee /etc/sysctl.d/k8s.conf
net.ipv4.ip_forward = 1
EOF


$ sudo sysctl --system

$ sysctl net.ipv4.ip_forward

$ sudo apt-get update 


$ sudo apt-get install -y apt-transport-https ca-certificates curl gpg

$ sudo mkdir -p -m 755 /etc/apt/keyrings

$ curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg

$ echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list

$ sudo apt-get update

$ sudo apt-cache madison kubeadm

$ sudo apt-get install -y kubelet=1.29.0-1.1 kubeadm=1.29.0-1.1 kubectl=1.29.0-1.1

$ sudo apt-mark hold kubelet kubeadm kubectl

$ sudo systemctl enable --now kubelet

$ kubelet --version

$ kubectl get nodes

$ ip addr show
$ kubeadm init --apiserver-advertise-address 192.19.46.9 --pod-network-cidr 10.244.0.0/16 --apiserver-cert-extra-sans controlplane

$ ssh node01

$ kubeadm join 192.19.46.9:6443 --token nmw2w4.zxjwab0a5rkqpyrm \
        --discovery-token-ca-cert-hash sha256:e591ddaaa5a83535f49063fbe7a08c8a6cc5a10ca68503656152bddf0bba5d43


On Master Node

$ sudo mkdir -p  ~/.kube/

$ sudo cp /etc/kubernetes/admin.conf ~/.kube/config

$ wget https://github.com/flannel-io/flannel/releases/latest/download/kube-flannel.yml

in container args this shall be present 
- args:
    - --ip-masq
    - --kube-subnet-mgr
    - --iface=eth0

$ k apply -f kube-flannel.yaml
```