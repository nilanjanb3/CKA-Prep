```sh
$ k create ns ingress-nginx

apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: watch-wear
  namespace: app-space
  annotations:
    nginx.ingress.kubernetes.io/rewrite-target: /
spec:
  ingressClassName: ingress-nginx
  rules:
  - http:
      paths:
      - path: /wear
        pathType: Prefix
        backend:
          service:
            name: wear-service
            port:
              number: 8080
      - path: /watch
        pathType: Prefix
        backend:
          service:
            name: video-service
            port:
              number: 8080
```