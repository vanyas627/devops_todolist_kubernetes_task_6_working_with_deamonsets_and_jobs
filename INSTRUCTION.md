# 1) How to deploy cronjon.yaml and daemonset.yaml:

    kubectl apply -f daemonset.yaml
    kubectl apply -f cronjob.yaml

# 2) How to validate the solution:

**DaemonSetLogs:**

Firstly try to get the list our pods:

    kubectl -n mateapp get pods -l app=daemonset-todoapp

And then we can check the logs our pods:

    kubectl -n mateapp logs <name-pod>

**CronJob logs:**

Check list our pods:

    kubectl -n mateapp get pods --selector=job-name=<cronjob-todoapp>


Check logs: 

    kubectl -n mateapp logs <name-pod>
