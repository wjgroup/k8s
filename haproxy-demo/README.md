# Set up azure k8s service
## 1. Create aks in azure
You can do this in azure portal

## 2. Connection aks cluster with kubectl
```
az login
az aks get-credentials --resource-group group_name --name cluster_name
```

## 3. Deploy 2 services by using the attached yaml files
```
$ kubectl apply -f ingress-default-backend.yaml 
kubectl adeployment.extensions/ingress-default-backend created
ppservice/ingress-default-backend created

$ kubectl apply -f http-svc.yaml 
deployment.extensions/http-svc created
service/http-svc created
```