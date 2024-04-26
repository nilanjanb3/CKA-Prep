```sh
$ k get po -n kube-system kube-apiserver-controlplane -o yaml

$ k get roles

$ k get role kube-proxy -n kube-system -o yaml

$ k get rolebinding kube-proxy -n kube-system  -o yaml

$ k auth can-i get pods --as dev-user

---
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  name: developer
  namespace: default
rules:
- apiGroups:
  - ""
  resources:
  - pods
  verbs:
  - list
  - create
  - delete
---
apiVersion: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  name: dev-user-binding
  namespace: default
roleRef:
  apiGroup: rbac.authorization.k8s.io
  kind: Role
  name: developer
subjects:
- apiGroup: rbac.authorization.k8s.io
  kind: User
  name: dev-user

---

apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  creationTimestamp: "2024-04-26T08:21:22Z"
  name: developer
  namespace: blue
  resourceVersion: "2291"
  uid: 35bb5815-8c9a-426f-96c8-c48eefe4d9f0
rules:
- apiGroups:
  - ""
  resourceNames:
  - blue-app
  - dark-blue-app
  resources:
  - pods
  verbs:
  - get
  - watch
  - create
  - delete
- apiGroups:
  - apps
  resources:
  - deployments
  verbs:
  - create


$ k auth can-i '*' '*' --as dev-user
```