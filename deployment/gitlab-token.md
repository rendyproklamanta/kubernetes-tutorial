- Click project repo
- Setting > Repository (in left sidebar)
- Create deploy token
- Checklist all
- Run in kubectl

```
kubectl create secret docker-registry gitlab-token --docker-server="gitlab.com:<5050-PORT>" --docker-username="<namespace>" --docker-password="YOUR_TOKEN" -n <namespace>
```