# Deployment

- Make sure you have been deployed traefik :
<https://github.com/rendyproklamanta/kubernetes-traefik>

- Using gitlab token : [click here](myapp-production-token.md)

- Deploy all from kustomization.yaml

```shell
kubectl apply -k <app-dir>
kubectl apply -k k8s/production
```

- Commands

```shell
kubectl get deployment -n <namespace>
```
