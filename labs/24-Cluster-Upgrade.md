### Upgrading Conrtrolplane
```sh
$ k get nodes -o wide

$ kubeadm upgrade plan

$ k drain controlplane --ignore-daemonsets 

$ echo "deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /" | sudo tee /etc/apt/sources.list.d/kubernetes.list

$ curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg

$ sudo apt update

$ sudo apt-cache madison kubeadm

$ sudo apt-mark unhold kubeadm && \
>  sudo apt-get update && sudo apt-get install -y kubeadm='1.29.0-1.1' && \
>  sudo apt-mark hold kubeadm

$ kubeadm version

$ sudo kubeadm upgrade plan

$ sudo kubeadm upgrade apply v1.29.0

$ sudo apt-mark unhold kubelet kubectl && \
>  sudo apt-get update && sudo apt-get install -y kubelet='1.29.0-1.1' kubectl='1.29.0-1.1' && \
>  sudo apt-mark hold kubelet kubectl

$ sudo systemctl daemon-reload

$ sudo systemctl restart kubelet

$ k uncordon controlplane

```

### Upgrading Worked Node
```sh
$ ssh node01

$ echo "deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /" | sudo tee /etc/apt/sources.list.d/kubernetes.list && \
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg && \
sudo apt update && \
sudo apt-mark unhold kubeadm && \
sudo apt-get update && sudo apt-get install -y kubeadm='1.29.0-1.1' && \
sudo apt-mark hold kubeadm && \
sudo kubeadm upgrade node && \
sudo apt-mark unhold kubelet kubectl && \
sudo apt-get update && sudo apt-get install -y kubelet='1.29.0-1.1' kubectl='1.29.0-1.1' && \
sudo apt-mark hold kubelet kubectl && \
sudo systemctl daemon-reload && \
sudo systemctl restart kubelet && \
```