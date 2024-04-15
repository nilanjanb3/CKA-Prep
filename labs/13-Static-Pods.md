```sh
$ k get po -A -o wide
If a pod name has controlplane attached, then it is a static pod

$ ps -aux | grep kubelet

$ cd /etc/kubernetes/manifests

$ ls -al

$ cat kube-apiserver.yaml

$ k get po static-greenbox-node01 -o wide

$ ssh node01

$ ps -aux | grep -i "kubelet"

$ cat /var/lib/kubelet/config.yaml

$  cd /etc/just-to-mess-with-you

$ rm -rf greenbox.yaml

$ k delete po static-greenbox-node01
```