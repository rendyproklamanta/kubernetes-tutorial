# Cron Commands

```sh
kubectl --kubeconfig="file.yaml" get jobs -n <namespace>
kubectl --kubeconfig="file.yaml" get job <cron-name> -o yaml -n <namespace>
kubectl --kubeconfig="file.yaml" logs -l job-name=<cron-name> -n <namespace>
kubectl --kubeconfig="file.yaml" get cronjobs -n <namespace>
kubectl --kubeconfig="file.yaml" delete cronjob <cron-name> -n <namespace>
```

## Test execute the CronJob Manually if any errors

- Create cronjob debug

```sh
kubectl --kubeconfig="file.yaml" get cronjobs -n <namespace>
kubectl --kubeconfig="file.yaml" create job --from=cronjob/cron-name cron-name-debug -n <namespace>
```

- Then monitor debug pod

```sh
kubectl --kubeconfig="file.yaml" get pods -l job-name=cron-name-debug -n <namespace>
kubectl --kubeconfig="file.yaml" logs cron-name-debug-cdfc7 -n <namespace>
```

- Delete cron debug if no longer needed

```sh
kubectl --kubeconfig="file.yaml" delete job cron-name-debug -n movinite
```
