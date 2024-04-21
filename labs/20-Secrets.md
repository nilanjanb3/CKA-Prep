```sh
$ k get secrets

$ k get secrets dashboard-token -o yaml

$ k create secret generic db-secret --dry-run=client -o yaml > db-secret.yaml

apiVersion: v1
data:
  DB_Host: c3FsMDE=
  DB_Password: cGFzc3dvcmQxMjM=
  DB_User: cm9vdA==
kind: Secret
metadata:
  name: db-secret
  namespace: default
type: Opaque

spec:
  containers:
  - image: nilanjan/my-app
    imagePullPolicy: Always
    name: webapp
    envFrom:
      - secretRef:
          name: db-secret
```