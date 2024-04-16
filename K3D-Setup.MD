# Cluster Setup using K3D

### Refer the Docs for Installation
https://k3d.io/v5.6.3/#installation

### My Commands
```$ k3d cluster create two-node-cluster --agents 2```

**Stopping Cluster:**
</br>
```$ k3d cluster stop two-node-cluster```


**Starting Cluster:**
</br>
```$ K3d cluster start two-node-cluster```


**Getting Context:**
</br>
```$ kubectl config get-contexts```

**Using Context:**
</br>
```$ kubectl config use-context k3d-two-node-cluster```
