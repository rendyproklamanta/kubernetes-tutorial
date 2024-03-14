- Make sure you have been deployed traefik :
https://github.com/rendyproklamanta/kubernetes-traefik

- Using gitlab token : [click here](gitlab-token.md)

- Deploy all from kustomization.yaml :
```
kubectl apply -k <app-dir>

example : kubectl apply -k sample
```