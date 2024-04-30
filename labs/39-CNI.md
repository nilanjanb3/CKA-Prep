```sh
$ ps -aux | grep -i "Kubelet" | grep -i "\-\-container-runtime-endpoint"

CNI Binaries are locared in: /opt/cni/bin by default.

$ ls -al /opt/cni/bin

$ cat /etc/cni/net.d/10-flannel.conflist 
```