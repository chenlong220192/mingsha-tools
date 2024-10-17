-
```
helm upgrade --install \
  --create-namespace redis-cluster \
  --namespace redis-cluster \
  --version 11.0.6 \
  ./chart/bitnami:redis-cluster-11.0.6
```
