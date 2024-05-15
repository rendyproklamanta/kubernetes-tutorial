# Install Metric Server

```shell
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/high-availability.yaml
```

- TOP to check memory usage

```shell
kubectl top node
kubectl top pods --all-namespaces
```

- HPA (Horizontal Pod Autoscaller)

```shell
kubectl get hpa -n coreacademy
```
