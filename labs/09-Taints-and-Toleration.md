```sh
$ k get nodes

$ k describe node node01 | grep -i "Taints:"

$ k taint node node01 spray=mortein:NoSchedule

$ k run mosquito --image=nginx 

$ k taint node controlplane node-role.kubernetes.io/control-plane:NoSchedule-

$

$

$

$


```