# Deployment

- Make sure you have been deployed traefik :
<https://github.com/rendyproklamanta/kubernetes-traefik>

- Using gitlab token : [click here](gitlab-token.md)

- Deploy all from kustomization.yaml

```shell
kubectl apply -k <app-dir>
```

example : kubectl apply -k k8s/production
