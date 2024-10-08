# Create a Secret

- From Literal Values

```shell
kubectl create secret generic my-secret --from-literal=username=myuser --from-literal=password=mypassword -n <namespace>
```

- From a File

```shell
kubectl create secret generic my-secret --from-file=path/to/your/file -n <namespace>
```

- From Directory (all files in the directory)

```shell
kubectl create secret generic my-secret --from-file=path/to/directory/ -n <namespace>
```

- From Environment Variables

```shell
kubectl create secret generic my-secret --from-env-file=path/to/.env -n <namespace>
```

## View Secrets

- List All Secrets

```shell
kubectl get secrets -n <namespace>
```

- Describe a Specific Secret

```shell
kubectl describe secret my-secret -n <namespace>
```

- Get the Secret in YAML Format

```shell
kubectl get secret my-secret -o yaml -n <namespace>
```

- Decode Secret Data

```shell
kubectl get secret my-secret -o jsonpath='{.data.username}' | base64 --decode -n <namespace>
```

## Update a Secret

- Update a Secret from Literal Values

```shell
kubectl create secret generic my-secret --from-literal=username=newuser --dry-run=client -o yaml -n <namespace> | kubectl apply -f -
```

- Update a Secret from a File

```shell
kubectl create secret generic my-secret --from-file=path/to/newfile --dry-run=client -o yaml -n <namespace> | kubectl apply -f -
```

## Delete a Secret

- Delete a Specific Secret

```shell
kubectl delete secret my-secret -n <namespace>
```

- Delete All Secrets in a Namespace

```shell
kubectl delete secrets --all -n <namespace>
```

## Use Secrets in Pods

- Using Secrets as Environment Variables

```yaml
spec:
   containers:
      - name: my-container
         image: my-image:latest
         envFrom:
         - secretRef:
               name: my-secret
```

## Export Secrets

- Export to a File

```shell
kubectl get secret my-secret -o json | jq '.data | map_values(@base64d)' > my-secret.json -n <namespace>
```
