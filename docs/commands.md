# Useful Commands

- Get with namespace

```shell
kubectl get pod --all-namespaces
kubectl get namespaces
kubectl get all -n {namespace_name} -o wide
kubectl get all --all-namespaces
```

- Delete

```shell
kubectl delete all --all -n {namespace_name}
helm delete -n {namespace_name} {release_name}
```

- Use additonal kubeconfig yaml

```shell
kubectl --kubeconfig=test.yaml get node
```
