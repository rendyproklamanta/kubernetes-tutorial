# How to use gitlab token

- Click project repo
- Setting > Repository (in left sidebar)
- Create deploy token
- filename : app-production-token | app-sandbox-token
- Checklist all
- Copy deploy token
- Run in kubectl

## Create token for production

```shell
kubectl create secret docker-registry app-production-token --docker-server="gitlab.com:{5050|port}" --docker-username="TOKEN_PROD_USERNAME" --docker-password="TOKEN_PROD_PASSWORD" -n app-production
```

## Create token for sandbox

```shell
kubectl create secret docker-registry app-sandbox-token --docker-server="gitlab.com:{5050|port}" --docker-username="TOKEN_SANDBOX_USERNAME" --docker-password="TOKEN_SANDBOX_PASSWORD" -n app-sandbox
```
