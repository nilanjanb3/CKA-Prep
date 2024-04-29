```sh
$ 
>> Host Path Volume 

---
apiVersion: v1
kind: Pod
metadata:
  name: webapp
  namespace: default
spec:
  containers:
  - env:
    - name: LOG_HANDLERS
      value: file
    image: kodekloud/event-simulator
    imagePullPolicy: Always
    name: event-simulator
    volumeMounts:
    - mountPath: /log
      name: logs-volume
  volumes:
  - name: logs-volume
    hostPath:
      path: /var/log/webapp
      type: Directory
---

---
apiVersion: v1
kind: PersistentVolume
metadata:
  name: pv-log
spec:
  accessModes:
  - ReadWriteMany
  capacity:
    storage: 100Mi
  hostPath:
    path: "/pv/log"
  persistentVolumeReclaimPolicy: Retain
---
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: claim-log-1
spec:
  accessModes:
    - ReadWriteMany
  resources:
    requests:
      storage: 50Mi
---
apiVersion: v1
kind: Pod
metadata:
  name: webapp
  namespace: default
spec:
  containers:
  - env:
    - name: LOG_HANDLERS
      value: file
    image: kodekloud/event-simulator
    imagePullPolicy: Always
    name: event-simulator
    volumeMounts:
    - mountPath: /log
      name: logs-volume
  volumes:
  - name: logs-volume
    persistentVolumeClaim:
      claimName: claim-log-1


$ k get pv


$ k get pvc
```