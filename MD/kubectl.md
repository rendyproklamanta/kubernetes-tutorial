# How to Use kubectl with kubeconfig

- Open your file {filename}.yaml > rename contexts
- Inside VSCode > Open new terminal "Power Shell"
- Export all your yaml to kubeconfig

```shell
# Go to your list kubeconfig directory:
cd /path/kubeconfig

# Export all yaml to the environment KUBECONFIG:
- $env:KUBECONFIG="cluster1.yaml;cluster2.yaml"
- kubectl config view --raw > C:\Users\User\.kube\config # <- your .kube directory
```

- Use context your cluster\

```shell
kubectl config get-contexts 
kubectl config use-context {context_name}
kubectl get node
```
