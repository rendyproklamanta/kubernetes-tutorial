# Upgrade

- After upgrade, redeploy the traefik to re-deploy accross nodes

```shell
kubectl rollout restart deployment/traefik -n traefik-network
```