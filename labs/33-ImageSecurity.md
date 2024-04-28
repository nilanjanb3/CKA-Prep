```sh
$ k create secret -h

$ k get deployments web -o yaml | grep -i "image:"

$ k create secret docker-registry private-reg-cred --docker-username='dock_user' \
--docker-password='dock_password' \
--docker-server='myprivateregistry.com:5000' \
--docker-email='dock_user@myprivateregistry.com'

$ 
```