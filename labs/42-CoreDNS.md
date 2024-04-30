```sh
$ k -n kube-system logs kube-proxy-9mfhj

$ k get svc  -A

$ k -n kube-system get deployments.apps coredns -o yaml

$ k -n kube-system get cm coredns -o yaml

$ k exec -it hr -- nslookup http://mysql.payroll.svc.cluster.local > /root/CKA/nslookup.out
```