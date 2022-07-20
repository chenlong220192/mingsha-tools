-
```
helm upgrade --install \
  --create-namespace redis-cluster \
  --namespace redis-cluster \
  --version 7.2.4 \
  ./chart/bitnami:redis-cluster-7.2.4
```
