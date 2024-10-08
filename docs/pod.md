# Commands

## Get Pods

```shell
kubectl get pods                                            # List all pods in the current namespace
kubectl get pods -n <namespace>                             # List pods in a specific namespace
kubectl get pods -o wide                                    # Get more information about the pods
```

## Describe a Pod

```shell
kubectl describe pod <pod-name>                             # Describe a specific pod
kubectl describe pod <pod-name> -n <namespace>              # Describe a pod in a specific namespace
```

## Get Pod Logs

```shell
kubectl logs <pod-name>                                     # Get logs from a specific pod
kubectl logs <pod-name> -n <namespace>                      # Get logs from a pod in a specific namespace
kubectl logs <pod-name> --previous                          # Get logs from the previous instance of a container
```

## Execute a Command in a Pod

```shell
kubectl exec -it <pod-name> -- <command>                    # Execute a command in a running pod
kubectl exec -it <pod-name> -- /bin/shell                   # Start a shell shell in a pod
```

## Port Forward to a Pod

```shell
kubectl port-forward <pod-name> <local-port>:<pod-port>     # Forward a local port to a port on a pod
```

## Create a Pod

```shell
kubectl run <pod-name> --image=<image-name>                 # Create a pod from an image
```

## Apply a Pod Configuration

```shell
kubectl apply -f <pod-config.yaml>                          # Apply a YAML file to create/update a pod
```

## Delete a Pod

```shell
kubectl delete pod <pod-name>                               # Delete a specific pod
kubectl delete pod <pod-name> -n <namespace>                # Delete a pod in a specific namespace
kubectl delete pods --all                                   # Delete all pods in the current namespace
```

## Get Pod Status

```shell
kubectl get pod <pod-name> -o jsonpath='{.status.phase}'    # Get the status phase of a pod
```

## View Pod Resource Usage

```shell
kubectl top pod <pod-name>                                  # Show resource usage of a pod
```

## Delete All Pods in a Namespace

```shell
kubectl delete pods --all -n <namespace>                    # Delete all pods in a specific namespace
```
