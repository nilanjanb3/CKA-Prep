```sh
$ k get ds -A

$ k describe ds kube-flannel -n kube-flannel | grep -i "Image:"

```
An easy way to create a DaemonSet is to first generate a YAML file for a Deployment with the command ```kubectl create deployment elasticsearch --image=registry.k8s.io/fluentd-elasticsearch:1.20 -n kube-system --dry-run=client -o yaml > fluentd.yaml```. Next, remove the replicas, strategy and status fields from the YAML file using a text editor. Also, change the kind from Deployment to DaemonSet.

Finally, ```create the Daemonset by running kubectl create -f fluentd.yaml```