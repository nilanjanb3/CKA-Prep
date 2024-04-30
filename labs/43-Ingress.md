```sh
$ k get all -A

$ k get ingress -A

$ kubectl describe ingress --namespace app-space

$ kubectl get deploy ingress-nginx-controller -n ingress-nginx -o yaml | grep -i "default-backend"

---
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: test-ingress
  namespace: critical-space
  annotations:
    nginx.ingress.kubernetes.io/rewrite-target: /
    nginx.ingress.kubernetes.io/ssl-redirect: "false"
spec:
  rules:
  - http:
      paths:
      - path: /pay
        pathType: Prefix
        backend:
          service:
           name: pay-service
           port:
            number: 8282


```