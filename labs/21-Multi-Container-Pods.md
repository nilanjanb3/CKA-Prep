```sh
$ k run yellow --dry-run=client --image=busybox -o yaml > yellow.yaml

apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: null
  labels:
    run: yellow
  name: yellow
spec:
  containers:
  - image: busybox
    name: lemon
    command: ["sleep", "1000"]
  - image: redis
    name: gold
    resources: {}
  dnsPolicy: ClusterFirst
  restartPolicy: Always
status: {}

$ k -n <namespace> exec <pod-name> -it /bin/sh

$ 
```