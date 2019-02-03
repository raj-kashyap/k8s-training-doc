+++
menutitle = "Jobs"
date = 2018-12-29T17:15:52Z
weight = 1
chapter = false
pre = "<b>- </b>"
+++

# Job

```
$ kubectl run date-print --image=ansilh/debug-tools  --restart=OnFailure  -- /bin/sh -c date

k8s@k8s-master-ah-01:~$ kubectl get jobs
NAME         COMPLETIONS   DURATION   AGE
date-print   0/1           3s         3s
k8s@k8s-master-ah-01:~$ kubectl get pods
NAME               READY   STATUS      RESTARTS   AGE
date-print-psxw6   0/1     Completed   0          8s
k8s@k8s-master-ah-01:~$ kubectl get jobs
NAME         COMPLETIONS   DURATION   AGE
date-print   1/1           4s         10s
k8s@k8s-master-ah-01:~$

k8s@k8s-master-ah-01:~$ kubectl logs date-print-psxw6
Sun Feb  3 18:10:45 UTC 2019
k8s@k8s-master-ah-01:~$
```