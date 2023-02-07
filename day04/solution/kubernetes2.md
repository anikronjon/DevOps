## Deploy app
```
# kubectl create deployment _deployment_name_ --image=_image_name_
kubectl create deployment ubuntuApp --image=ubuntu
```

### List the deployments
```
kubectl get deployment
```

### List pods and nodes
```
# List pods
kubectl get pods

# List nodes
kubectl get nodes
```