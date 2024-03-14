- Install
```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/high-availability.yaml
```

- TOP to check memory usage
```
kubectl top node
kubectl top pods --all-namespaces
```

- HPA (Horizontal Pod Autoscaller)
```
kubectl get hpa -n coreacademy
```