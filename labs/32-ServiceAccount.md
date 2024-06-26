```sh
$ k get sa

$ kubectl describe serviceaccount default

$ k describe deployments web-dashboard 

$ k get po web-dashboard-74cbcd9494-z52vt -o yaml | grep -i "serviceaccount"

$ k create sa dashboard-sa --dry-run=client -o yaml > dashboard-sa.yaml

$ k apply -f dashboard-sa.yaml 

>> Service Account with RBAC

apiVersion: v1
kind: ServiceAccount
metadata:
  creationTimestamp: null
  name: dashboard-sa
  namespace: default

---
kind: Role
apiVersion: rbac.authorization.k8s.io/v1
metadata:
  namespace: default
  name: pod-reader
rules:
- apiGroups:
  - ''
  resources:
  - pods
  verbs:
  - get
  - watch
  - list

---
kind: RoleBinding
apiVersion: rbac.authorization.k8s.io/v1
metadata:
  name: read-pods
  namespace: default
subjects:
- kind: ServiceAccount
  name: dashboard-sa # Name is case sensitive
  namespace: default
roleRef:
  kind: Role #this must be Role or ClusterRole
  name: pod-reader # this must match the name of the Role or ClusterRole you wish to bind to
  apiGroup: rbac.authorization.k8s.io


$ k create token dashboard-sa




```