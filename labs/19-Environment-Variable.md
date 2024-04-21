```sh
$ k get po

$ k get cm

$ k describe cm db-config 

$ k create cm webapp-config-map --dry-run=client -o yaml > cm1.yaml

$
apiVersion: v1
kind: ConfigMap
metadata:
  creationTimestamp: null
  name: webapp-config-map
data: 
  APP_COLOR: darkblue
  APP_OTHER: disregard

pod configuration
spec:
  containers:
  - env:
    - name: APP_COLOR
      valueFrom:
        configMapKeyRef:
          name: webapp-config-map
          key: APP_COLOR
```