replicasを10にしたので10pod立ち上がる

```
kubectl get pod
```

```
hello-9bn2j   1/1     Running   0          38s
hello-bkbgv   1/1     Running   0          38s
hello-f5rmq   1/1     Running   0          38s
hello-g292d   1/1     Running   0          38s
hello-k2xdh   1/1     Running   0          38s
hello-kz545   1/1     Running   0          38s
hello-v55kk   1/1     Running   0          38s
hello-v5nf8   1/1     Running   0          38s
hello-wczq4   1/1     Running   0          38s
hello-zsfgj   1/1     Running   0          38s
```

全削除

```
kubectl delete -f simple-replicaset.yml 
```