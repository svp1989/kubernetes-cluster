# kubernetes-cluster
### Simple kubernetes cluster for test

Run **./master.sh** for install cluster kubernetes on you node <br>
For check run command **kubectl get all -A**

### Install dashboard
Command **kubectl apply -f dashboard** <br>
Get access token for dashboard **kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"**