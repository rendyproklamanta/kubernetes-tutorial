## Useful Commands

- Get with namespace
```
kubectl get pod --all-namespaces
kubectl get namespaces
kubectl get all -n {namespace_name} -o wide
kubectl get all --all-namespaces
kubectl delete all --all -n {namespace_name}
helm delete -n {namespace_name} {release_name}
```

- Use additonal kubeconfig yaml:
```
kubectl --kubeconfig=test.yaml create namespace traefik-network
```