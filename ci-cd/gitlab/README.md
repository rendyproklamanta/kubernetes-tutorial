# Deploy using gitlab registry

## Variable
- Assign variable for kubernetes

## Runner
- Assign runner for kubernetes

## Deploy token
- Click project repo
- Setting > Repository (in left sidebar)
- Create deploy token
- Checklist all
- Run in kubectl to create secret

```
kubectl create secret docker-registry <app-production-token> --docker-server="<repo.domain.com:5050>" --docker-username="<deploy-token-name>" --docker-password="<deploy-token-pass>" -n <namespace>
```

- Create environment variable:
https://malgasm.com/blog/166/how-to-deploy-to-kubernetes-using-gitlab-ci
