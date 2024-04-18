```sh
$ k get deployments

$ k describe deployment frontend | grep -i "Image:"

$ k describe deployment frontend | grep -i "StrategyType:"

$ k set image deployment/frontend simple-webapp=kodekloud/webapp-color:v2

$ k rollout status deployment/frontend

$ k rollout history deployment/frontend

$ k rollout undo deployment/frontend
```