```sh
$ kubectl get clusterroles --no-headers  | wc -l

$ k get clusterrolebinding --no-headers |  wc -l

$ k get clusterrole | grep -i "cluster-admin"

$ k get clusterrolebindings cluster-admin -o yaml
```