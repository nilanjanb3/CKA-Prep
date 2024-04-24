```sh
$ k config get-clusters

$ kubectl config use-context cluster1

$ k get nodes -o wide

$ kubectl config use-context cluster2

$ k get nodes -o wide

$ ssh cluster2-controlplane

$ ps -aux | grep "kubelet" | grep "config"

$ cat /var/lib/kubelet/config.yaml

$ ls -al /etc/kubernetes/manifests
No manifests related to etcd

$ ps -aux | grep -i etcd

$ ssh etcd-server

$ ps -aux | grep etcd

$ ETCDCTL_API=3 etcdctl \
>  --endpoints=https://127.0.0.1:2379 \
>  --cacert=/etc/etcd/pki/ca.pem \
>  --cert=/etc/etcd/pki/etcd.pem \
>  --key=/etc/etcd/pki/etcd-key.pem \
>   member list

$ k config use-context cluster1

$  ETCDCTL_API=3 etcdctl --endpoints=https://192.8.224.11:2379 --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key snapshot save /opt/cluster1.db
Snapshot saved at /opt/cluster1.db

controlplane $ scp cluster1-controlplane:/opt/cluster1.db /opt/cluster1.db

$ scp /opt/cluster2.db etcd-server:/root/cluster2.db

$ ssh etcd-server

$ ETCDCTL_API=3 etcdctl --endpoints=https://127.0.0.1:2379 --cacert=/etc/etcd/pki/ca.pem --cert=/etc/etcd/pki/etcd.pem --key=/etc/etcd/pki/etcd-key.pem snapshot restore /root/cluster2.db --data-dir /var/lib/etcd-data-new

$  sudo vi /etc/systemd/system/etcd.service 

Change : --data-dir=/var/lib/etcd-data-new \

$ sudo chown -R etcd:etcd /var/lib/etcd-data-new/

$ systemctl daemon-reload

$ systemctl restart etcd
```