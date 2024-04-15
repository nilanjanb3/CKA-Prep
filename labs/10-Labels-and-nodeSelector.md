```sh
$ k label node node01 color=blue

$ k create deployment blue --image=nginx --replicas=3

apiVersion: apps/v1
kind: Deployment
metadata:
  annotations:
    deployment.kubernetes.io/revision: "1"
  generation: 1
  labels:
    app: red
  name: red
  namespace: default
  resourceVersion: "2342"
  uid: 6df2a71e-4668-48b3-895e-45bc12c8b8b2
spec:
  progressDeadlineSeconds: 600
  replicas: 2
  revisionHistoryLimit: 10
  selector:
    matchLabels:
      app: red
  template:
    metadata:
      creationTimestamp: null
      labels:
        app: red
    spec:
      affinity:
        nodeAffinity:
          requiredDuringSchedulingIgnoredDuringExecution:
            nodeSelectorTerms:
              - matchExpressions:
                - key: node-role.kubernetes.io/control-plane
                  operator: Exists

      containers:
      - image: nginx
        imagePullPolicy: Always
        name: nginx


```