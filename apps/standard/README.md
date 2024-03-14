- Deploy test my-app
```
kubectl create configmap index.html --from-file index.html
kubectl apply -k simple-nginx
```