replicate_setから世代管理機能を追加 -> deployment

記録を保持して立ち上げ
```
kubectl apply -f simple-deployment.yml --record

```

deploymentリソース取得
```
kubectl get deployment

```

replicasetリソース取得
```
kubectl get replicaset

```

世代確認
```
kubectl rollout history deployment hello

```

port番号やイメージを変えたら世代が増える
```
deployment.apps/hello 
REVISION  CHANGE-CAUSE
1         kubectl apply --filename=simple-deployment.yml --record=true
2         kubectl apply --filename=simple-deployment.yml --record=true
3         kubectl apply --filename=simple-deployment.yml --record=true
4         kubectl apply --filename=simple-deployment.yml --record=true

```

詳細な世代情報の確認

```
kubectl rollout history deployment hello --revision=1

```

ロールバック


```
kubectl rollout undo deployment hello
kubectl rollout undo deployment hello --to-revision=1
```

現在あがっているdevploymentリソースの詳細

```
kubectl describe deployment hello
```