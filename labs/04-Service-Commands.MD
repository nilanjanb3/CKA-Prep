```sh
$ k get svc

$ k describe svc <svc-name> | grep -i "Port:"

$ k get svc <svc-name> -o jsonpath="{.metadata.labels}"

$ k create service nodeport <svc-name> --tcp=8080:8080 --node-port=30080  --dry-run=client -o yaml > svc.yaml


```