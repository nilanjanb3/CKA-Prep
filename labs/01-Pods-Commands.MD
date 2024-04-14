```sh
$ k get po

$ k run nginx --image=nginx

$ k describe po <pod-name>  | grep -i "Image:"

$ k describe po <pod-name> | grep -i "Node:"

$ k describe po <pod-name>

$ k delete po webapp

$ k edit po <pod-name>

$ k run nginx --image=nginx --dry-run=client -o yaml > nginx.yaml

$ cat nginx.yaml


```