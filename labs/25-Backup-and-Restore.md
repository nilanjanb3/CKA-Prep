```sh
$ k get deployments

$ k get po etcd-controlplane -n kube-system -o yaml | grep -i "image:"

$ kubectl describe pod etcd-controlplane -n kube-system | grep "listen-client-urls"

$ kubectl describe pod etcd-controlplane -n kube-system | grep -i "cert-file"

$ export ETCDCTL_API=3

$ etcdctl --endpoints https://127.0.0.1:2379 \
--cert=/etc/kubernetes/pki/etcd/server.crt \
--key=/etc/kubernetes/pki/etcd/server.key \
--cacert=/etc/kubernetes/pki/etcd/ca.crt \
snapshot save /opt/snapshot-pre-boot.db

$ etcdctl --endpoints https://127.0.0.1:2379 \
--cert=/etc/kubernetes/pki/etcd/server.crt \
--key=/etc/kubernetes/pki/etcd/server.key \
--cacert=/etc/kubernetes/pki/etcd/ca.crt \
--data-dir /var/lib/etcd-from-backup snapshot restore /opt/snapshot-pre-boot.db

$ ps -aux | grep "kubelet" | grep "config"

$ cat /var/lib/kubelet/config.yaml | grep -i "staticPodPath:"

$ cd /etc/kubernetes/manifests

$ vi etcd.yaml

volumes:
- hostPath:
  name: etcd-data
    path: /var/lib/etcd-from-backup
    type: DirectoryOrCreate
```