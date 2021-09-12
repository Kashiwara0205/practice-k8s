## pod

```
- 新規作成
- 内容変更
kubectl apply -f simple_pod.yml
```

```
状態取得
kubectl get pod
```

```
ポッドの中に入る
kubectl exec -ti simple-hello /bin/bash
```

```
ポッド削除
kubectl delete pod simple-hello
```