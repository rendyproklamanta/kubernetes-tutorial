# Deploy using gitlab registry
- Make sure you installed docker and kubectl in your runner

- Create token:
https://gitlab.com/{project-path}/settings/access_tokens

- Create secret:
```
kubectl create secret docker-registry gitlab-token --docker-server=https://registry.gitlab.com --docker-username=<username> --docker-password="<personal access token>" -n <my-app>
```

- Create environment variable:
https://malgasm.com/blog/166/how-to-deploy-to-kubernetes-using-gitlab-ci
