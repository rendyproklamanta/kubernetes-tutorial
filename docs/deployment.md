# Deployment

- Make sure you have been deployed traefik :
<https://github.com/rendyproklamanta/kubernetes-traefik>

- Using gitlab token : [click here](myapp-production-token.md)

- Deploy all from kustomization.yaml

```shell
kubectl apply -k <app-dir>
kubectl apply -k k8s/production
```

- Get Deployment

```shell
kubectl get deployment -n <namespace>
```

- Restart Deployment

```shell
kubectl rollout restart <DEPLOYMENT_NAME> -n <namespace>
```