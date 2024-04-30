```sh
$ ip addr

$ k get po -n kube-system weave-net-gdwpn -o yaml
# Check for ip alloc range for pod ip addresses

$ k -n kube-system get po kube-apiserver-controlplane -o yaml | grep -i "ip-range"
# This will display service ip ranges

$ k -n kube-system logs kube-proxy-9mfhj
# This will help finding which routing tool is being used
```