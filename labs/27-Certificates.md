```sh
$ k -n kube-system get po kube-apiserver-controlplane -o yaml | grep -i "cert"

$ k -n kube-system get po kube-apiserver-controlplane -o yaml | grep -i "key"

$ k -n kube-system get po etcd-controlplane -o yaml

$ openssl x509 -in /etc/kubernetes/pki/apiserver.crt -text -noout
```