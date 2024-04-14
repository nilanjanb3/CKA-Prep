```sh
$ k get rs

$ k describe rs new-replica-set | grep -i "Image:"

$ kubectl api-resources

$ kubectl api-resources | grep replicaset

$ kubectl explain replicaset | grep VERSION

$ k delete rs <rs-name>

$ k delete po  -n <ns-name> --all

$ k scale rs new-replica-set --replicas=5

```