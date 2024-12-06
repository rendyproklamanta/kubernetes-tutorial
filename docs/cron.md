# Cron Commands

```sh
kubectl --kubeconfig="file.yaml" get jobs -n <namespace>
kubectl --kubeconfig="file.yaml" get job <cron_name> -o yaml -n <namespace>
kubectl --kubeconfig="file.yaml" logs -l job-name=<cron_name> -n <namespace>
kubectl --kubeconfig="file.yaml" get cronjobs -n <namespace> -n <namespace>
kubectl --kubeconfig="file.yaml" delete cronjob <cron_name> -n <namespace>
```

## Test the CronJob Manually if any errors

```sh
kubectl --kubeconfig="file.yaml" create job --from=cronjob/cron-name cron-name-debug -n <namespace>
```

## Then monitor the pods

```sh
kubectl --kubeconfig="file.yaml" get pods -l job-name=cron-name-debug -n <namespace>
kubectl --kubeconfig="file.yaml" logs cron-name-debug-cdfc7 -n <namespace>
```

## Delete cron debug

```sh
kubectl --kubeconfig="file.yaml" delete job cron-name-debug -n movinite
```
